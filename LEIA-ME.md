# Site da Markes Studio: como publicar (Cloudflare Pages)

## Publicar / atualizar
No PowerShell, dentro da pasta `markes studio`:

    npx wrangler pages deploy site --project-name markes-studio --branch main

Na primeira vez o comando abre o navegador para você entrar na Cloudflare.
O site fica em https://markes-studio.pages.dev (cada deploy também gera um link de prévia).
Também dá para atualizar pelo painel: dash.cloudflare.com → Workers & Pages → markes-studio → "Create deployment" e arrastar a pasta `site`.

## Formulário
O briefing é enviado pelo FormSubmit (formsubmit.co) para markestudio.official@gmail.com.
O formulário já está ativado para https://markes-studio.com (12/11/2026).
O FormSubmit ativa cada endereço separadamente. Por isso o index.html manda quem entra por www.markes-studio.com
ou markes-studio.pages.dev para https://markes-studio.com. Se um dia o site mudar de domínio, chega um novo
e-mail de ativação no primeiro envio: é só clicar em "Activate Form".

## Voltar para uma versão anterior
- As versões salvas ficam em `markes studio/versoes/`. Para voltar, publique a pasta da versão:
  `npx wrangler pages deploy "versoes/v1-inicial-2026-11-12" --project-name markes-studio --branch main`
- Ou no painel da Cloudflare: Deployments → escolha um deploy antigo → "Rollback to this deployment".

## Domínio
O site responde em https://markes-studio.com e https://www.markes-studio.com (domínio comprado na Cloudflare em 12/11/2026).
O DNS tem dois registros CNAME (@ e www) apontando para markes-studio.pages.dev.
A imagem de compartilhamento (og.jpg) usa o endereço https://markes-studio.com/og.jpg no index.html.

## Arquivos
- index.html: o site inteiro (inglês, português e espanhol)
- media/: vídeos e imagens
- og.jpg: imagem que aparece quando o link é compartilhado
- favicon.svg e apple-touch-icon.png: ícone da aba e do celular
- _headers: configurações de cache da Cloudflare
