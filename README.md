# Compliance pages

Static pages required by Intuit's production keys checklist: EULA, privacy
policy, launch URL, disconnect URL, connect/reconnect URL.

They describe what the toolkit actually does — a private, local, single-company
integration that stores nothing server-side. Read them before publishing; if the
toolkit's behaviour changes, update them to match.

## Publishing on GitHub Pages (free HTTPS)

```bash
gh repo create quickbooks-app-pages --public --source=site --push
gh api -X POST repos/:owner/quickbooks-app-pages/pages \
  -f 'source[branch]=main' -f 'source[path]=/'
```

Serves at `https://<user>.github.io/quickbooks-app-pages/`.

## URLs for the Intuit checklist

| Intuit field | Page |
|---|---|
| Host domain | `<user>.github.io` |
| Launch URL | `.../index.html` |
| Connect / reconnect URL | `.../connect.html` |
| Disconnect URL | `.../disconnect.html` |
| EULA | `.../eula.html` |
| Privacy policy | `.../privacy.html` |
