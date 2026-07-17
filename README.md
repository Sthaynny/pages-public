# Páginas públicas

Repositório **público** para hospedar HTML/CSS exigido pelas lojas (privacidade, termos, etc.), enquanto os apps podem permanecer em repos privados.

GitHub Pages (plano free) **não** publica repos privados — este repo desbloqueia as URLs HTTPS.

## Estrutura

```
.
├── index.html              # Índice de apps
├── assets/site.css         # Estilo do índice
├── cura.li/                # Páginas do Cura.li
│   ├── index.html
│   ├── assets/legal.css
│   ├── privacidade/
│   └── termos/
└── .github/workflows/pages.yml
```

Cada app = uma pasta na raiz. Ao adicionar outro app, copie o HTML para `nome-do-app/` e inclua o link em `index.html`.

## URLs (após ativar Pages)

| Página | URL |
| :--- | :--- |
| Índice | `https://sthaynny.github.io/public/` |
| Cura.li | `https://sthaynny.github.io/public/cura.li/` |
| Privacidade | `https://sthaynny.github.io/public/cura.li/privacidade/` |
| Termos | `https://sthaynny.github.io/public/cura.li/termos/` |

## Publicar

1. Repo público no GitHub (`Sthaynny/public`).
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
