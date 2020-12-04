# Installazione di PrestaShop con lo script della riga di comando

PrestaShop offre anche un programma di installazione per le installazioni da riga di comando. 

## Che cos'è? <a id="InstallazionediPrestaShopconloscriptdellarigadicomando-Checos&apos;&#xE8;?"></a>

Questo programma di installazione speciale ti permette di installare PrestaShop senza dover utilizzare un browser web: ti basterà inserire il contenuto dell'archivio ZIP sul server web, quindi installare PrestaShop tramite l'interfaccia della riga di comando \(CLI\). Puoi utilizzare qualsiasi software CLI purché sia compatibile con i comandi del server: Bash, Windows PowerShell, OS X Terminal, PuTTY ecc.

La possibilità di disporre di un programma di installazione CLI oltre al normale programma di installazione nel browser consente di soddisfare le esigenze di alcuni utenti avanzati, che spesso preferiscono le interfacce della riga di comando, in quanto offrono metodi più precisi e avanzati per controllare un programma o un sistema operativo.

## Come utilizzarlo <a id="InstallazionediPrestaShopconloscriptdellarigadicomando-Comeutilizzarlo"></a>

Il programma di installazione CLI è di facile utilizzo: dal terminale, vai alla cartella `/install` \(o `/install-dev`\) \(si presuppone che tu abbia già decompresso il file prestashop.zip\) e avvia lo script con questo comando:

```text
$ php index_cli.php
```

```text
Verranno visualizzate le varie opzioni disponibili.
```

Sono disponibili tutte le normali opzioni del programma di installazione nel browser, con i relativi valori predefiniti. La maggior parte dei valori predefiniti può essere lasciata così com'è, in quanto puoi modificarli tutti nel back office di PrestaShop al termine dell'installazione. Nota: l'indirizzo email e la password corrispondono a quelli utilizzati per creare l'account di back office dell'amministratore.

Per avviare l'installazione, devi specificare soltanto un argomento. In realtà ne devi indicare più di uno:

* **domain**: la posizione in cui desideri visualizzare il tuo negozio.
* **db\_server**: l'indirizzo del server di database.
* **db\_name**: il nome del database che desideri utilizzare.
* **db\_user**: il nome utente del database che desideri utilizzare.
* **db\_password**: la password del nome utente del database indicato sopra.

Ad esempio:

```text
$ php index_cli.php --domain=example.com --db_server=sql.example.com --db_name=prestashop --db_user=root --db_password=123456789
```

  
If you also set the `--email` value to your own address, a recap e-mail will be sent to you once the installation is done.

## List of arguments <a id="InstallazionediPrestaShopconloscriptdellarigadicomando-Listofarguments"></a>

Here is the list of arguments for index\_cli.php as of version 1.6:

| Name | Default setting | Description |
| :--- | :--- | :--- |
| --step | process |  |
| --language | en | language iso code |
| --timezone | localhost |  |
| --domain | localhost |  |
| --db\_server | localhost |  |
| --db\_user | root |  |
| --db\_password | \(blank\) |  |
| --db\_name | prestashop |  |
| --db\_clear | 1 \(true\) | Drop existing tables |
| --db\_create | 0 \(false\) | Create the database if it does not exist yet |
| --prefix | ps\_ |  |
| --engine | InnoDB | InnoDB/MyISAM |
| --name | PrestaShop | Name of the shop |
| --activity | 0 |  |
| --country | fr |  |
| --firstname | John |  |
| --lastname | Doe |  |
| --password | 0123456789 |  |
| --email | [pub@prestashop.com](mailto:pub@prestashop.com) |  |
| --license | 0 \(false\) | Show PrestaShop's license |
| --newsletter | 1 \(true\) | Subscribe administrator to PrestaShop's newsletter |
| --send\_email | 1 \(true\) | Send an email to the administrator after installation |

