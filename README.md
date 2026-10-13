# Landing page — Grupo de Achados do Mercado Livre

Página estática de captação para o grupo gratuito do WhatsApp.
Arquivo único, sem build, sem dependência de node.

## Estrutura

```
index.html      → a página inteira (HTML + CSS + JS)
vercel.json     → cabeçalhos de cache e segurança
```

## Publicar na Vercel

1. Crie um repositório novo no GitHub (pode ser público ou privado).
2. Suba os arquivos: `index.html`, `vercel.json` e este `README.md` na raiz do repositório.
3. Em vercel.com → **Add New → Project → Import Git Repository** e escolha o repositório.
4. Não mude nada nas configurações:
   - Framework Preset: **Other**
   - Build Command: **vazio**
   - Output Directory: **vazio**
5. Clique em **Deploy**. Em segundos a página está no ar.

Qualquer `git push` na branch principal republica a página automaticamente.

## Subir pelo terminal

```bash
git init
git add .
git commit -m "landing page do grupo de achados"
git branch -M main
git remote add origin https://siegezf.github.io
git push -u origin main
```

## O que editar

| O que | Onde no `index.html` |
|---|---|
| Link do grupo | busque por `chat.whatsapp.com` — aparece **2 vezes** (botão principal e barra fixa) |
| Título da página | tag `<title>` e `og:title` |
| Texto dos benefícios | blocos `<article class="card">` |
| Cores | bloco `:root` no `<style>` |

## Domínio próprio

Na Vercel: **Settings → Domains → Add**. Aponte o domínio para os servidores indicados
e o HTTPS é emitido sozinho.
