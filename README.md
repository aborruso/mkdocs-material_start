# Sito MkDocs Material di esempio

Questo repository contiene un esempio di configurazione per creare un sito documentazione utilizzando MkDocs con il tema Material.

## Caratteristiche principali

Il template include già configurato:
- Tema Material con funzionalità avanzate
- Plugin per galleria immagini (glightbox)
- Integrazione social media
- Supporto per emoji, diagrammi e snippet di codice
- Navigazione avanzata con tabs e indici
- Ricerca integrata

## Come usare questo repository

1. Fai un fork di questo repository o clonalo localmente
2. Modifica il file `mkdocs.yml` con le informazioni del tuo progetto
3. Aggiungi i tuoi file markdown nella cartella `docs/`
4. Personalizza la configurazione secondo le tue esigenze

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

Il sito sarà disponibile all'indirizzo:
`https://<tuo-username>.github.io/<nome-repo>/`

## Sviluppo locale

Per testare il sito in locale:

```bash
pip install mkdocs-material[imaging] mkdocs-glightbox
mkdocs serve
```

Il sito sarà disponibile all'indirizzo http://127.0.0.1:8000
