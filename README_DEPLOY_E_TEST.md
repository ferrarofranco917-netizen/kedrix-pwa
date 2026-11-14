# KEDRIX PWA — CANDIDATA HTTPS, SOLO TEST

**14 novembre 2026 — Non pubblicata, non integrata nella PROD.**

## Baseline accertata
- K ufficiale V19 (SVG originale trasformato in PNG). L'utente ha confermato che Edge visualizza la K installando il prototipo localhost.
- La navigazione dal prototipo locale a KEDRIX TEST in una finestra app è stata vista nello screenshot; autenticazione effettiva, salvataggio e PDF non sono stati collaudati end-to-end.
- TEST Apps Script P2.10.12; PROD V19 @19 non modificata.
- RECAP MASTER nella Libreria datato 03/11: storico, non rappresenta l'ultima baseline; prevalgono i log di collaudo P2.10.12 forniti dall'utente.

## Scopo e architettura
È una pagina statica installabile PWA e il suo manifesto. **Non è il gestionale, né un proxy o iframe**. L'URL del vero gestionale resta su Google Apps Script, con autenticazione originale. La K è l'icona della pagina d'accesso. Una navigazione fuori dallo scope verso Google può comportare barre del browser o nuova scheda secondo versione/configurazione Edge; non promettere 'stessa finestra' per tutti.

## Pubblicazione HTTPS suggerita (DOPO autorizzazione)
Usare un **nuovo repository dedicato** di GitHub Pages pubblico (non repository originali KEDRIX). Pubblicare i file contenuti in questo pacchetto nella radice del repository e abilitare *Settings → Pages → Deploy from a branch* (branch main, root). Attendere URL HTTPS Pages, verificare manifesto/icone con DevTools Application e installazione Edge da URL HTTPS. Il repository pubblico mostra tutti i file, **compreso URL TEST**: accesso effettivo deve rimanere protetto da Google; non inserire credenziali o segreti. Non attivare GitHub Pages senza consenso espresso sulla pubblicazione pubblica dell'indirizzo di accesso.

Per pubblicazioni con contenuto non pubblico verificare un hosting con controllo accessi diverso da GitHub Pages (lato server, non nascosto solo in JavaScript). Non usare Cloudflare già esistente senza autorizzazione.

## Collaudo web richiesto
1. Aprire HTTPS, verificare logo, nome, manifesto, installare da Edge.
2. Chiudere e riaprire la nuova app dal menu Start: deve mostrare K senza server PowerShell.
3. Premere `Apri KEDRIX TEST`: verificare che compaia `/dev`, non `/exec`.
4. Verificare account Google corretto, salvataggio/riapertura di quotazione fittizia, PDF e download, navigazione ed eventuale logout.
5. Ripetere da PC diverso. Non dichiarare PWA definitiva prima di questi test.

## Limitazioni deliberate
- Non esiste ancora un dominio HTTPS assegnato al pacchetto. Nessun deploy.
- Manifest `id`, `start_url`, `scope` e icone sono **relativi** per supportare un sottopercorso GitHub Pages.
- Nessun service worker/offline o cache applicativa: evitare dati obsoleti.
- Non contiene script di tracking, analytics, API, form credenziali o integrazioni produttive.
- Non ha alcun link alla PROD e non la pubblica.
- L'installazione PWA come launcher permanente non è identica all'installazione nativa della Web App Google: per aggiornare l'icona di quest'ultima serve una soluzione supportata dallo stesso origin o diversa distribuzione.

## Rollback
Eliminare la PWA TEST da edge://apps e disabilitare le Pages del solo repository dedicato (quando creato). Nessun rollback su GAS o Sheets richiesto.
