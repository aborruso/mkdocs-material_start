# Template per sito MkDocs Material

Questo repository è un template GitHub per creare rapidamente nuovi siti documentazione utilizzando MkDocs con il tema Material.

Per iniziare:
1. Clicca su "Use this template" (in alto a destra nella pagina del repository)
2. Scegli un nome per il nuovo repository
3. Seleziona se renderlo pubblico o privato
4. Clicca su "Create repository from template"

## Caratteristiche principali

Il template include già configurato:
- Tema Material con funzionalità avanzate
- Plugin per galleria immagini (glightbox)
- Integrazione social media
- Supporto per emoji, diagrammi e snippet di codice
- Navigazione avanzata con tabs e indici
- Ricerca integrata

## Come usare questo template

1. Clicca su "Use this template" (in alto a destra nella pagina del repository)
2. Scegli un nome per il nuovo repository
3. Seleziona se renderlo pubblico o privato
4. Clicca su "Create repository from template"

Dopo aver creato il repository:
1. Modifica il file `mkdocs.yml` aggiornando questi valori:
   ```yaml
   site_url: https://<tuo-username>.github.io/<nome-repo>/
   repo_url: https://github.com/<tuo-username>/<nome-repo>
   ```
2. Aggiorna anche il valore `edit_uri` se necessario:
   ```yaml
   edit_uri: edit/<branch-principale>/docs/
   ```
   (sostituisci `<branch-principale>` con il nome del branch principale, tipicamente `main` o `master`)

Il nuovo repository conterrà:
- Configurazione MkDocs preimpostata
- Workflow GitHub Actions per il deploy
- Struttura di base della documentazione

## Abilitare la pubblicazione su GitHub Pages

1. Crea il branch `gh-pages`:
   ```bash
   git checkout --orphan gh-pages
   git rm -rf .
   git commit --allow-empty -m "Initial gh-pages commit"
   git push origin gh-pages
   git checkout main
   ```

2. Vai su Settings > Pages nel tuo repository
3. Nella sezione "Build and deployment":
   - Scegli "Deploy from a branch"
   - Seleziona il branch `gh-pages`
   - Seleziona la cartella `/ (root)`
4. Salva le modifiche

Una volta configurato correttamente:
- GitHub mostrerà l'URL pubblico del sito nella sezione Pages
- Il sito sarà disponibile all'indirizzo:
  `https://<tuo-username>.github.io/<nome-repo>/`
- Potrebbero volerci alcuni minuti prima che il sito sia accessibile

## Sviluppo locale

Per testare il sito in locale:

```bash
pip install mkdocs-material[imaging] mkdocs-glightbox
mkdocs serve
```

Il sito sarà disponibile all'indirizzo http://127.0.0.1:8000
