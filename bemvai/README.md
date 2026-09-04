# BemVai Auto Socorro — Landing Page

Site estático. Sem build, sem dependências, sem Node. Basta subir o conteúdo desta pasta.

## Estrutura

```
site/
├── index.html      # a página inteira (HTML + CSS inline + 2 scripts vanilla no final)
├── assets/         # imagens (logo, hero, fotos dos serviços, favicon)
└── README.md
```

## Como publicar

**Hospedagem tradicional (cPanel / FTP)**
Suba `index.html` e a pasta `assets/` para a raiz pública do domínio
(`public_html/`, `www/` ou `htdocs/`). Mantenha `assets/` no mesmo nível do `index.html`.

**Vercel / Netlify / Cloudflare Pages**
Publique a pasta `site/` como diretório de saída. Sem comando de build.

Nada mais é necessário — os caminhos são relativos (`./assets/...`).

## O que já está configurado

- `<title>`, meta description, canonical, Open Graph e Twitter Card
- Dados estruturados JSON-LD (`AutoRepair`, 24h, área atendida)
- `lang="pt-BR"`, favicon, `theme-color`
- Responsivo (breakpoints em 900px e 640px)
- Respeita `prefers-reduced-motion`
- Fonte Montserrat via Google Fonts (fallback da Gotham — ver abaixo)

## Pendências antes de ir ao ar

0. ~~**Canonical**~~ — já ajustado para `https://bemvai.com.br/`. **Importante:** foi adicionado `<meta name="robots" content="noindex, nofollow">` no `<head>` porque a página está publicada em `lp.bemvai.com.br` só para aprovação do cliente — remover essa tag quando subir para `bemvai.com.br` definitivo, senão o Google não indexa o site final. Vale conferir a `og:image` para URL absoluta depois de publicado.
2. **Números da faixa de autoridade** — hoje são fictícios: `data-counter="500"` (atendimentos) e `data-counter="30"` (associações). Trocar pelos reais.
3. **Foto de destombamento** — o card 04 de Serviços está com o bloco "FOTO EM BREVE".
4. **Fotos do Alessandro e da Paula** — a seção Quem Somos tem dois espaços marcados.
5. ~~**Depoimentos**~~ — feito: os 3 cards agora trazem avaliações reais do Google Meu Negócio ("Auto Socorro BemVai - Transporte e Logística", Anápolis-GO, 5,0★/45 avaliações), com link para a página do Google. Conteúdo estático (copiado manualmente), sem chamada de API em runtime — se quiser que atualize sozinho no futuro, precisa de backend com Places API.
6. **Gotham** — a página pede `Gotham` e cai para `Montserrat`. Se houver licença, colocar os `.woff2` em `assets/fonts/` e adicionar um `@font-face` no `<style>`; nenhuma outra mudança é necessária.

## Contato usado nos links

WhatsApp e telefone: **(62) 99106-3461** → `https://wa.me/5562991063461` e `tel:+5562991063461`.
Aparece em 6 lugares (topo, hero, seção de assistência no local, CTA final, rodapé e botão flutuante) — buscar por `5562991063461` para trocar todos.
