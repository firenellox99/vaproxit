# Stremio Vavoo.to Italia Addon

Un addon per [Stremio](https://www.stremio.com/) che permette di accedere ai canali TV italiani disponibili su Vavoo.to direttamente dall'interfaccia di Stremio.

## Caratteristiche

- 🇮🇹 Filtraggio automatico dei canali italiani da Vavoo.to
- 📺 Streaming di canali TV in diretta
- 🔄 Proxy integrato per gli stream m3u8 
- 🌐 Compatibile con HTTPS per una maggiore sicurezza

## Come funziona

L'addon:

1. Recupera la lista dei canali da https://vavoo.to/channels
2. Filtra solo i canali con paese "Italy"
3. Presenta i canali come catalogo in Stremio
4. Quando si seleziona un canale, genera l'URL dello stream nel formato https://vavoo.to/play/[id]/index.m3u8
5. Utilizza un proxy interno per gestire gli stream m3u8 e i segmenti TS, aggiungendo gli header necessari

## Requisiti tecnici

- Python 3.9+
- Flask
- Requests
- Flask-CORS
- Gunicorn (per ambienti di produzione)

## Installazione

### Utenti finali

Se vuoi semplicemente utilizzare l'addon:

1. Apri Stremio
2. Vai su "Addon" > "Community Addons"
3. In fondo, clicca su "Inserisci URL Addon"
4. Incolla l'URL dell'addon (es. https://stremio-vavoo-addon.onrender.com/manifest.json)
5. Clicca su "Installa"

In alternativa, puoi visitare l'URL /install dell'addon (es. https://stremio-vavoo-addon.onrender.com/install) per una pagina di installazione più semplice.

### Sviluppatori

Per eseguire l'addon in locale o distribuirlo:

1. Clona questo repository
git clone https://github.com/tuousername/stremio-vavoo-addon.git
cd stremio-vavoo-addon
2. Installa le dipendenze
pip install -r requirements.txt
3. Avvia l'addon in locale
python app.py
L'addon sarà disponibile all'indirizzo http://localhost:10000.

## Deployment su Render

Questo addon è configurato per funzionare su [Render](https://render.com/):

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy?repo=https://github.com/ciccioxm3/vaproxit)

1. Crea un nuovo account su Render o accedi
2. Vai su "New" > "Web Service"
3. Collega il tuo repository GitHub
4. Seleziona "Docker" come ambiente
5. Assicurati che la porta sia impostata su 10000
6. Clicca su "Create Web Service"

## Note legali

Questo addon è solo un proxy che facilita l'accesso a contenuti già disponibili pubblicamente su Vavoo.to. L'addon non ospita, archivia o distribuisce contenuti protetti da copyright. Utilizza questo addon solo per accedere a contenuti che hai il diritto di visualizzare nel tuo paese.

## Contributi

Contributi, issues e feature requests sono benvenuti! Sentiti libero di controllare la [pagina delle issues](link-to-your-issues).

## Licenza

[MIT](./LICENSE)
