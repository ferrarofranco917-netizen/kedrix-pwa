# KEDRIX — PWA PROD V20 / GitHub Pages

**Ambito:** pubblicare solo il launcher statico `/prod/` sul repository GitHub Pages esistente `ferrarofranco917-netizen/kedrix-pwa`. La pagina root `/kedrix-pwa/` TEST resta invariata. Non modificare Apps Script, Sheets o Drive.

**URL previsto dopo upload:** https://ferrarofranco917-netizen.github.io/kedrix-pwa/prod/

**Destinazione PROD V20 @20:** https://script.google.com/macros/s/AKfycbznoKwTIMrM48cbpUdYIjmXrd-Nn10jfDxr0s5oSE8EevFxDDGmLSc2Azh9-kegFmGS2w/exec

**Caricamento con interfaccia GitHub:** aprire il repository → Add file → Upload files, trascinare la cartella `prod` dalla cartella estratta. Se GitHub non mantiene la directory `prod`, annullare e creare `prod/README.md` con Add file → Create new file; entrare in cartella `prod`, quindi Add file → Upload files e trascinare i sette file presenti dentro `prod`. Commit changes. Non caricare il file README_INSTALLAZIONE.md né lo ZIP, non cancellare i file TEST già in root.

**Verifica:** aprire l’URL `/prod/`, controllare logo K e pulsante V20 PROD. In Edge installare DAL SITO GITHUB, non da Apps Script. Aprire dal menu Start e usare il pulsante. Confermare V20 badge all’interno di Apps Script e funzionalità. **PWA launcher ≠ installazione Google Apps Script**: quando si naviga fuori dal suo scope Edge può aprire un'altra finestra; il launcher mantiene l’icona K, non forza l’icona del sito Google.

**Sicurezza:** GitHub Pages è pubblico e rivela l’URL di accesso, che deve restare protetto da autorizzazioni Google. Nessuna credenziale, dati cliente, secret o API key in questi file.

**Rollback:** rimuovere soltanto la cartella `/prod/` dal repo; TEST root e Web App Google non sono alterati.
