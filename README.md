# Páginas públicas

Repositório **público** para hospedar HTML/CSS exigido pelas lojas (privacidade, termos, etc.), enquanto os apps podem permanecer em repos privados.

GitHub Pages (plano free) **não** publica repos privados — este repo desbloqueia as URLs HTTPS.

## Estrutura

```
.
├── index.html              # Índice de apps
├── assets/site.css
├── cura.li/                # Landing + legal do Cura.li
│   ├── index.html          # Landing (store / publicidade)
│   ├── assets/landing.css
│   ├── assets/legal.css
│   ├── privacidade/
│   └── termos/
├── .cursor/rules/general.mdc
└── .github/workflows/pages.yml
```

Cada app = uma pasta na raiz. Ao adicionar outro app, copie o HTML para `nome-do-app/` e inclua o link em `index.html`.

## URLs

| Página | URL |
| :--- | :--- |
| Índice | `https://sthaynny.github.io/pages-public/` |
| Landing Cura.li | `https://sthaynny.github.io/pages-public/cura.li/` |
| Privacidade | `https://sthaynny.github.io/pages-public/cura.li/privacidade/` |
| Termos | `https://sthaynny.github.io/pages-public/cura.li/termos/` |

## Publicar

1. Repo público no GitHub (`Sthaynny/pages-public`).
2. **Settings → Pages → Build and deployment** → source = **GitHub Actions**.
3. Push em `main` (ou *Run workflow*).
4. Atualizar URLs no app (`AppLegalConstants`) e nas fichas das lojas.

Pré-visualizar localmente:

```bash
npx --yes serve .
# http://localhost:3000/cura.li/privacidade/
```

## Fonte canônica (Cura.li)

O Markdown legal continua em `Cura.li/docs/legal/`.  
O HTML aqui é o espelho publicado. Ao mudar o texto legal, atualize o MD no app **e** o HTML nesta pasta.
