# Il Fiore delle Ville - Sito Web

Sito web per la vendita del casale storico "Il Fiore delle Ville" in Toscana.

## Contenuto

- `index.html` - Pagina principale del sito
- `images/` - Cartella con tutte le foto ottimizzate (34 foto, ~18MB totali)
  - `panoramica/` - 4 foto
  - `casale/` - 9 foto
  - `interni/` - 6 foto
  - `uliveta/` - 7 foto
  - `annesso/` - 3 foto
  - `eventi/` - 5 foto

## Come pubblicare su Netlify

### Metodo 1: Deploy da GitHub (CONSIGLIATO)

1. **Crea un repository su GitHub:**
   - Vai su github.com
   - Clicca "New repository"
   - Nome: `fiore-delle-ville` (o quello che preferisci)
   - Pubblico o privato (a tua scelta)
   - NON aggiungere README, .gitignore o licenza
   - Clicca "Create repository"

2. **Carica i file su GitHub:**
   
   Dalla cartella `/mnt/user-data/outputs/`, esegui questi comandi:
   
   ```bash
   # Inizializza git
   git init
   
   # Aggiungi tutti i file
   git add .
   
   # Fai il primo commit
   git commit -m "Primo commit - sito Il Fiore delle Ville"
   
   # Collega al tuo repository (sostituisci TUO-USERNAME con il tuo username GitHub)
   git remote add origin https://github.com/TUO-USERNAME/fiore-delle-ville.git
   
   # Carica tutto su GitHub
   git push -u origin main
   ```

3. **Deploy su Netlify:**
   - Vai su netlify.com
   - Clicca "Add new site" → "Import an existing project"
   - Scegli "GitHub"
   - Autorizza Netlify ad accedere a GitHub (se richiesto)
   - Seleziona il repository `fiore-delle-ville`
   - Impostazioni di build:
     - Branch to deploy: `main`
     - Base directory: (lascia vuoto)
     - Build command: (lascia vuoto)
     - Publish directory: (lascia vuoto o `.`)
   - Clicca "Deploy site"

4. **Il tuo sito è online!**
   - Netlify ti darà un URL tipo: `random-name-123.netlify.app`
   - Puoi personalizzare il nome in "Site settings" → "Change site name"

### Metodo 2: Deploy diretto (più veloce ma meno professionale)

1. Vai su netlify.com
2. Trascina la cartella `/mnt/user-data/outputs/` direttamente sulla homepage di Netlify
3. Il sito viene pubblicato immediatamente

## Come collegare un dominio personalizzato

1. Su Netlify, vai in "Domain settings"
2. Clicca "Add custom domain"
3. Inserisci il tuo dominio (es: `fiore-delle-ville.it`)
4. Netlify ti dirà come configurare i DNS del tuo dominio
5. HTTPS automatico viene attivato in pochi minuti

## Struttura del sito

- **One-page design** con navigazione smooth scroll
- **6 sezioni:**
  - Home (hero)
  - Storia
  - La Proprietà
  - Il Territorio
  - Galleria (6 categorie)
  - Contatti
- **Responsive** per mobile
- **Ottimizzato** per prestazioni (foto compresse)

## Aggiornamenti futuri

Per aggiungere nuove foto o modificare il sito:

1. Modifica i file localmente
2. Fai commit e push su GitHub:
   ```bash
   git add .
   git commit -m "Descrizione modifiche"
   git push
   ```
3. Netlify aggiorna il sito automaticamente

## Note

- Tutte le foto sono state ottimizzate per il web (max 1920px width, quality 85%)
- Il sito è statico (solo HTML/CSS), nessun framework necessario
- Caricamento rapido grazie all'ottimizzazione delle immagini
- Email di contatto: fiore.frizzi@gmail.com
