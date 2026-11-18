# Markes Studio — site

Código do site [markes-studio.com](https://markes-studio.com), um estúdio de vídeo.

- Página única em HTML, CSS e JavaScript, sem framework nem etapa de build.
- Três idiomas na mesma página: inglês, português e espanhol.
- Hospedado no Cloudflare Pages, com o domínio próprio apontado por CNAME.
- Formulário de briefing enviado pelo FormSubmit.

## Estrutura

- `site/index.html`: o site inteiro
- `site/media/`: imagens (os vídeos não são versionados, ficam fora do repositório)
- `site/_headers`: cache e cabeçalhos de segurança no Cloudflare Pages
- `LEIA-ME.md`: como publicar, voltar versão e configurar o domínio

## Publicar

    npx wrangler pages deploy site --project-name markes-studio --branch main

Antes de publicar a partir de um clone novo, coloque os vídeos em `site/media/`.
