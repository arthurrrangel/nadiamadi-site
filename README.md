# nadiamadi · site

Site oficial da filmmaker **Nadia Madi** (@madiifilmm) — Rio de Janeiro.

Single-page, estático, sem build. Pode subir em qualquer hospedagem de arquivos estáticos (Vercel, Netlify, Cloudflare Pages, GitHub Pages).

## Como colocar no ar — 3 opções

### Opção A — Drag & Drop no Vercel (mais rápido, ~30s)

1. Abra https://vercel.com/new
2. Arraste a pasta `nadiamadi-site` inteira para o navegador
3. Confirme o nome do projeto e clique em **Deploy**

Pronto. URL no formato `nadiamadi-site.vercel.app` em segundos.

### Opção B — GitHub + Vercel (recomendado para manutenção)

```bash
cd nadiamadi-site
git init
git add .
git commit -m "site nadiamadi v1"
git branch -M main
# crie um repo vazio em github.com/SEU_USER/nadiamadi-site
git remote add origin git@github.com:SEU_USER/nadiamadi-site.git
git push -u origin main
```

Depois, em https://vercel.com/new, clique **Import Git Repository**, escolha o repo e clique **Deploy**. Cada `git push` futuro vira deploy automático.

### Opção C — Vercel CLI

```bash
npm i -g vercel
cd nadiamadi-site
vercel
```

Siga os prompts. `vercel --prod` publica em produção.

---

## O que você precisa trocar antes de publicar

Tudo abaixo está marcado no código com comentários:

1. **Reel principal** — `index.html`, dentro de `<section id="reel">`. Tem um placeholder com instruções e exemplo de embed Vimeo e YouTube.
2. **Thumbnails dos trabalhos** — `<section id="trabalhos">`. Hoje cada card é um gradiente. Troque por `background-image: url('imagens/seu-projeto.jpg')`. Coloque as imagens dentro de uma pasta `imagens/` no mesmo nível do `index.html`.
3. **Contato** — `<section id="contato">`. Email, Instagram e WhatsApp estão com placeholders:
   - `contato@nadiamadi.com` → email real
   - `https://instagram.com/madiifilmm` → confirmar o handle real
   - `https://wa.me/5521000000000` → trocar o número (formato internacional sem +)
4. **Domínio próprio** — depois do deploy no Vercel, em **Project Settings → Domains**, conecte `nadiamadi.com` (ou outro) seguindo as instruções de DNS.

---

## Estrutura

```
nadiamadi-site/
├── index.html      ← site inteiro (HTML + CSS + JS inline)
├── vercel.json     ← headers de segurança + clean URLs
├── .gitignore
└── README.md
```

Sem dependências, sem build, sem node_modules. Abre direto com duplo clique no `index.html` se quiser ver localmente.

## Identidade

- **Tipografia:** Cormorant Garamond (display, italic) + Inter (corpo)
- **Paleta:** Noir #0E0D0B · Película #F0EBE3 · Ouro velho #C4B89A · Carvão #2A2720
- **Assinaturas:** ponto dourado, monograma NM, grain noise sutil

Baseado no kit `nadiamadi_kit_identidade.html`.
