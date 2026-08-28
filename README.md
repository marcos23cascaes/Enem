# 100 Palavras-Chave para a Redação do ENEM — Página de Vendas

Landing page estática (um único arquivo `index.html`, sem dependências, sem build).

## Antes de publicar

Abra o `index.html`, vá até o final do arquivo e preencha o link do seu checkout:

```js
var CHECKOUT_URL = 'https://pay.hotmart.com/SEU-LINK';
```

Enquanto estiver vazio, todos os botões apenas rolam a página até a seção de oferta.

## Como publicar (opções gratuitas)

### GitHub Pages (já configurado)
1. No GitHub: **Settings → Pages → Source: GitHub Actions**.
2. Faça merge deste branch na `main`. O workflow `.github/workflows/deploy-pages.yml` publica sozinho.
3. Site em `https://<usuario>.github.io/<repositorio>/`.

### Netlify
- Arraste a pasta do projeto em <https://app.netlify.com/drop>, ou conecte o repositório.
- Build command: vazio · Publish directory: `.` (já definido em `netlify.toml`).

### Vercel
- `Add New → Project`, importe o repositório. Framework: **Other**. Root: `.`.

### Cloudflare Pages
- `Create a project` → conecte o repositório. Build command vazio, output directory `/`.

## Estrutura

```
index.html                        página completa (HTML + CSS + JS inline)
netlify.toml / vercel.json        configuração de deploy
.nojekyll                         evita processamento Jekyll no GitHub Pages
robots.txt
.github/workflows/deploy-pages.yml
```

## Personalização rápida

Cores no bloco `:root` do CSS: `--azul`, `--amarelo`, `--verde`, `--vermelho`.

## Observações

A página não faz promessa de nota e inclui aviso de não afiliação ao INEP/MEC no rodapé,
conforme o conteúdo aprovado.
