# Esempi di Uso e Specifiche

* Esempi di Uso e Specifiche 
  * [Gestire un catalogo nella modalità multinegozio](esempi-di-uso-e-specifiche.md#gestire-un-catalogo-nella-modalita-multinegozio)
  * [Scambio di Dati tra Negozio](esempi-di-uso-e-specifiche.md#EsempidiUsoeSpecifiche-ScambiodiDatitraNegozio)
    * [Duplicazione di dati tra negozi](esempi-di-uso-e-specifiche.md#EsempidiUsoeSpecifiche-Duplicazionedidatitranegozi)
    * [Condividere dati tra negozi e gruppi di negozi](esempi-di-uso-e-specifiche.md#EsempidiUsoeSpecifiche-Condivideredatitranegoziegruppidinegozi)
    * [Condividere prodotti e categorie](esempi-di-uso-e-specifiche.md#EsempidiUsoeSpecifiche-Condividereprodottiecategorie)
    * [Condividere clienti e gruppi di clienti](esempi-di-uso-e-specifiche.md#EsempidiUsoeSpecifiche-Condividereclientiegruppidiclienti)
    * [Condividere ordini](esempi-di-uso-e-specifiche.md#EsempidiUsoeSpecifiche-Condividereordini)
    * [Usare un tema differente per ogni negozio/ogni gruppo di negozi](esempi-di-uso-e-specifiche.md#EsempidiUsoeSpecifiche-Usareuntemadifferenteperogninegozio/ognigruppodinegozi)
    * [Usare specifiche impostazioni per ogni negozio/gruppo di negozi](esempi-di-uso-e-specifiche.md#EsempidiUsoeSpecifiche-Usarespecificheimpostazioniperogninegozio/gruppodinegozi)
  * [Gestire pagine in modalità multinegozio](esempi-di-uso-e-specifiche.md#gestire-pagine-in-modalita-multinegozio)
  * [Gestire sconti in modalità multinegozio](esempi-di-uso-e-specifiche.md#gestire-sconti-in-modalita-multinegozio)
  * [Servizi Web e multinegozio](esempi-di-uso-e-specifiche.md#EsempidiUsoeSpecifiche-ServiziWebemultinegozio)

## Gestire un catalogo nella modalità multinegozio

In modalità multinegozio, alcune delle pagine di amministrazione di PrestaShop dispongono di un menu a discesa, intitolato "Configurazione multinegozio per". Questo menu fornisce il quadro globale di ciò che stai facendo: consente di impostare il negozio o il gruppo di negozi a cui si applicano le modifiche apportate.

Ad esempio, quando si crea un nuovo prodotto, la selezione in questo menu determinerà se il prodotto sarà disponibile per tutti i negozi, solo per un gruppo di negozi o per un singolo negozio.

Quando si modifica un prodotto, PrestaShop mostra delle notifiche per aiutarti a comprendere l'ambito delle modifiche. Ad esempio, durante la modifica di un prodotto nel contesto "Negozio A", la notifica sarà "Attenzione, se si modifica il valore dei campi con il pulsante arancione, il valore di questo prodotto verrà modificato in tutti gli altri negozi”; questo pulsante arancio apparirà su tutti i relativi campi, ad esempio "Tipo di prodotto", "Riferimento", dimensione del pacchetto ecc.

Allo stesso modo, se si modifica un prodotto nel contesto "Tutti i negozi" o nel contesto di un gruppo di negozi, alcuni campi saranno disattivati: dato che hanno un impatto globale, non è possibile modificarli. Se hai veramente bisogno di modificare questi contenuti, puoi farlo tramite la casella contenuta in ogni campo in tutti i negozi del relativo contesto.

Se si modifica un campo disabilitato, il prodotto viene creato in tutti i negozi del contesto che non lo hanno già nel proprio catalogo. Assicurati di verificare il contesto.

## Scambio di Dati tra Negozio <a id="EsempidiUsoeSpecifiche-ScambiodiDatitraNegozio"></a>

### Duplicazione di dati tra negozi <a id="EsempidiUsoeSpecifiche-Duplicazionedidatitranegozi"></a>

I dati duplicati in PrestaShop vengono impostati durante la configurazione di un singolo negozio, importando tutto o parte del contenuto da un negozio esistente a quello nuovo. I contenuti importabili variano: prodotti, categorie, dipendenti, moduli, regole del carrello, fornitori, ecc. L'importazione dei dati viene eseguita in modo definitivo: una volta creato un archivio, non è possibile importare facilmente i dati da un altro negozio.

### Condividere dati tra negozi e gruppi di negozi <a id="EsempidiUsoeSpecifiche-Condivideredatitranegoziegruppidinegozi"></a>

I negozi possono condividere dati. I dati condivisi vengono trattati fondamentalmente a livello dei gruppi di negozi: una delle cose importanti da capire quando si tratta della modalità multinegozio di PrestaShop è che tutti i negozi all'interno di un gruppo di negozi possono condividere i singoli dati di condivisione - o più precisamente, tre tipi di contenuti: clienti, quantità disponibili e ordini. Una volta impostato il gruppo di negozi, la condivisione di dati tra i negozi è per lo più terminata: mentre è possibile modificare l'impostazione delle quantità disponibili, non è più possibile modificare le impostazioni dei clienti e degli ordini non appena un negozio all'interno del gruppo ha almeno un cliente o un ordine.

### Condividere prodotti e categorie <a id="EsempidiUsoeSpecifiche-Condividereprodottiecategorie"></a>

Quando si crea un nuovo negozio all'interno di un gruppo, è possibile scegliere di avere tutte o alcune delle categorie nel nuovo negozio come duplicati esatti delle categorie in qualsiasi altro negozio dell'installazione di PrestaShop.

Quando si crea una categoria, per un negozio specifico o per tutti i negozi nell'installazione di PrestaShop, PrestaShop registra la categoria per tutti i negozi: resta semplicemente nascosta nei negozi dove non è stata impostata.

Associando i nuovi negozi a una determinata categoria, qualsiasi modifica di questa categoria influirà su tutti i negozi associati, anche se i negozi sono provenienti da gruppi di negozi diversi. Puoi quindi modificare una volta per tutte il contenuto della categoria da un negozio, inclusi i suoi prodotti.

### Condividere clienti e gruppi di clienti <a id="EsempidiUsoeSpecifiche-Condividereclientiegruppidiclienti"></a>

Come indicato in precedenza, i negozi all'interno dello stesso gruppo di negozi possono condividere i clienti: tutto ciò che devi fare è impostare l'opzione appropriata quando crei il gruppo di negozi.

I gruppi hanno meno dettagli: se modifichi un gruppo di clienti predefinito in un negozio, la modifica viene applicata a tutti gli altri negozi, a prescindere dal gruppo di negozi.

Se si desidera avere gruppi di clienti diversi per ogni negozio, è necessario creare un nuovo gruppo e utilizzare il selettore "Configurazione multinegozio per" per associare il gruppo al relativo gruppo.

Se l'opzione "Condividi clienti" è stata disattivata, la tua lista clienti dovrà essere vuota prima di attivarla.

Se preferisci mantenere la tua lista clienti, puoi eseguire le seguenti operazioni:

* Vai al software di gestione del database come phpMyAdmin.
* Cerca la tabella `ps_customer`. Potrebbe essere diversa, a seconda del prefisso del database.
* Esporta questa tabella.
* Svuota la tabella. NON rilasciarla. Se vuoi farlo accertati di ricreare subito la tabella.
* Torna alle impostazioni multinegozio per il gruppo negozio.
* Attiva l'opzione "Condividi clienti".
* Importa la tabella.

La condivisione dei clienti tra il gruppo di negozi è stata abilitata senza perdita di informazioni sui clienti.

### Condividere ordini <a id="EsempidiUsoeSpecifiche-Condividereordini"></a>

È possibile che i negozi all'interno dello stesso gruppo di negozi condividano gli ordini: tutto ciò che devi fare è impostare l'opzione appropriata quando crei il gruppo clienti.

Se l'opzione "Ordini condivisione" è stata disattivata, l'elenco ordini deve essere vuoto prima di poter attivare questa opzione.

Se preferisci mantenere i tuoi ordini puoi fare quanto segue:

* Vai al software di gestione del database come phpMyAdmin.
* Cerca la tabella `ps_order`. Potrebbe essere diversa, a seconda del prefisso del database.
* Esporta questa tabella.
* Svuota la tabella. NON rilasciarla. Se vuoi farlo accertati di ricreare subito la tabella.
* Torna alle impostazioni multinegozio per il gruppo negozio.
* Abilita l'opzione "Ordini azioni".
* Importa la tabella.

La condivisione di ordini tra il gruppo negozio è stata abilitata senza la perdita di informazioni sugli ordini.

### Usare un tema differente per ogni negozio/ogni gruppo di negozi <a id="EsempidiUsoeSpecifiche-Usareuntemadifferenteperogninegozio/ognigruppodinegozi"></a>

Una volta installato un tema sul tuo PrestaShop, puoi usare la pagina "Tema & Logo" nel menu "Design" per modificare il tema del relativo negozio o del gruppo di negozi, a seconda di come la "Configurazione Multinegozio per" è stata impostata.

### Usare specifiche impostazioni per ogni negozio/gruppo di negozi <a id="EsempidiUsoeSpecifiche-Usarespecificheimpostazioniperogninegozio/gruppodinegozi"></a>

Il selettore "Configurazione Multinegozio per" è l'opzione da usare quando si desidera che le modifiche abbiano un impatto su un determinato negozio o insieme di negozi. Dovrebbe essere anche la prima opzione da guardare quando si apre una schermata di amministrazione, in quanto PrestaShop cambierà le opzioni disponibili a seconda del contesto in cui si trova: negozio, gruppo di negozi o tutti i negozi.

Ciò consente di:

* Utilizzare diversi formati di immagine per ogni gruppo di negozi/negozio
* Attivare/configurare un modulo su ogni negozio
* Posizionare/visualizzare blocchi per il front office su ogni negozio
* ... e molto di più!

## Gestire pagine in modalità multinegozio

Quando si visualizza l'elenco delle pagine del contenuto nel contesto "Tutti i negozi", vengono mostrate tutte le pagine di tutti i negozi. Allo stesso modo, in un contesto gruppo di negozi vengono visualizzate tutte le pagine di tutti i negozi di quel gruppo.

Quando si crea una pagina in un gruppo di negozi, tutti i negozi di quel gruppo visualizzeranno quella pagina, tuttavia la pagina sarà unica: la modifica in un negozio applica le modifiche a tutti i negozi di quel gruppo.

Nella pagina di creazione viene visualizzata una sezione con un elenco che indica quali negozi saranno interessati.

## Gestire sconti in modalità multinegozio

Quando si creano regole di carrello o regole dei prezzi di catalogo in un contesto multinegozio, è disponibile una condizione aggiuntiva con la quale è possibile scegliere i negozi per i quali la regola deve essere disponibile.

## **Servizi Web e multinegozio** <a id="EsempidiUsoeSpecifiche-ServiziWebemultinegozio"></a>

L'accesso al servizio web è inoltre molto configurabile, sia a livello di negozio che a livello di gruppo di negozi. Quando crei servizi web chiave, è possibile scegliere di associarli a tutti i negozi, ad alcuni gruppi di negozi o ai negozi selezionati.

