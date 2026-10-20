# Financial Statements — Windows, Fedora e macOS

Applicazione per analizzare bilanci SEC/ESEF e creare file Excel con indicatori finanziari.

## Download

Scarica il pacchetto per il tuo sistema:

| Sistema | Ultima versione |
| --- | --- |
| Windows x64 | [Scarica l’eseguibile v1.1.2](https://github.com/lorbb/financialStatements-releases/releases/download/v1.1.2/FinancialStatements-1.1.2-windows-x64.exe) |
| Fedora 44 x64 | [Scarica il pacchetto con icona e collegamento](https://github.com/lorbb/financialStatements-releases/releases/download/v1.1.2/FinancialStatements-1.1.2-fedora-x64-desktop.tar.gz) |
| macOS 15 Apple Silicon (M1 e successivi) | [Scarica il pacchetto ARM64](https://github.com/lorbb/financialStatements-releases/releases/latest/download/FinancialStatements-macos-arm64.tar.gz) |
| macOS 15 Intel | [Scarica il pacchetto x64](https://github.com/lorbb/financialStatements-releases/releases/latest/download/FinancialStatements-macos-x64.tar.gz) |

Il download Windows usa un nome con la versione per evitare che Esplora file riutilizzi l’icona Python di un eseguibile precedente. Conservare il nome scaricato. Il programma è la stessa v1.1.2; il file originale rimane disponibile per gli aggiornamenti automatici.

[Versioni e checksum SHA-256](https://github.com/lorbb/financialStatements-releases/releases)

Non occorre installare Python o Codex. Su Windows salva l’eseguibile in una cartella personale scrivibile. Su Fedora estrai l’intera cartella nella destinazione definitiva, apri un terminale nella cartella ed esegui `sh ./Installa-collegamento.sh`. Poi avvia **Financial Statements** dal menu applicazioni o dal collegamento `FinancialStatements.desktop`. Se richiesto dal file manager, seleziona **Consenti avvio**. Se sposti la cartella, riesegui lo script. Il collegamento mostra il logo; il file ELF può mantenere un’icona generica in alcuni file manager. Su macOS estrai l’archivio e apri `Financial Statements.app`, collocandola in una cartella scrivibile, per esempio `~/Applications`. Le app macOS sono firmate ad-hoc e non notarizzate Apple; la prima apertura è soggetta ai normali controlli del sistema.

## Utilizzo

Apri l’applicazione, cerca una società e premi **Crea o aggiorna analisi Excel**. La destinazione predefinita è la sottocartella **financialStatements** della cartella di lavoro da cui viene avviata l’app. Se Finder avvia l’app dalla radice del sistema o dall’interno del bundle macOS, viene usata la home dell’utente (`~/financialStatements`). Il percorso effettivo è mostrato nella GUI.

Da **Cartella di salvataggio → Cambia cartella…** puoi scegliere un’altra destinazione per la sessione. La cartella viene creata solo quando avvii il salvataggio dei bilanci: aprire l’app, cercare una società o scegliere il percorso non crea una cartella di bilanci. I file esistenti non vengono spostati. Per conservare le rettifiche, mantieni il file `.source.json` accanto al relativo Excel.

## Aggiornamenti

All’avvio, su Windows, Fedora e macOS, l’app controlla se è disponibile una nuova versione e chiede conferma prima di scaricarla e installarla. Verifica dimensione e checksum SHA-256, riavvia l’app e rimuove la copia precedente dopo la conferma che la nuova versione funziona. Se l’avvio fallisce, tenta il ripristino della versione precedente. Gli Excel salvati vengono conservati.

Puoi ripetere il controllo dal menu **Aggiornamenti**. Senza connessione il controllo non blocca l’apertura dell’app; il download di nuovi bilanci richiede Internet.

Questo repository pubblico contiene i pacchetti per Windows, Fedora e macOS e le istruzioni. Il progetto sorgente è mantenuto in un repository privato.
