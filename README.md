# QuizCraft

QuizCraft è una web app per creare verifiche scolastiche da materiale in formato immagine.

L'interfaccia è pubblicata con GitHub Pages e usa un backend Google Apps Script per:

- suggerire gli argomenti con Gemini;
- generare le verifiche complete e semplificate;
- creare Google Form nell'account che distribuisce il backend.

## Avvio locale

Su Windows, avvia `AvviaConfiguratoreLocale.bat` e apri l'indirizzo mostrato dal terminale. Nell'uso locale la chiave Gemini viene inserita nell'interfaccia e non viene pubblicata nel repository.

## Pubblicazione

I file `index.html`, `help.html`, `logo.png` e i file di supporto possono essere pubblicati dalla cartella principale del branch `main` tramite GitHub Pages.

Il backend è configurato in `Code.gs` e viene distribuito come Web App Apps Script. Su GitHub Pages ogni visitatore usa temporaneamente la propria chiave Gemini; la chiave non viene salvata dal backend né inclusa nel repository.

## Sicurezza e quota

Il backend è raggiungibile pubblicamente per consentire le richieste da GitHub Pages. Le richieste Gemini consumano la quota dell'utente che inserisce la chiave. I Google Form vanno creati nel proprio account tramite lo script generato dall'interfaccia. Non pubblicare credenziali, password o progetti contenenti dati personali.
