# Portfólio · Matheus Jorge

Portfólio pessoal de Matheus Jorge, Product Designer e UX Lead. Site estático em HTML e CSS puro — sem build, sem dependências, hospedado no Cloudflare Pages em [matheusojorge.pages.dev](https://matheusojorge.pages.dev).

## Estrutura

```
portfolio/
├── index.html                    Apresentação, projetos, sobre e contato
├── ia-como-infraestrutura.html   Case: IA como infraestrutura de UX
├── gzh-redesign.html             Case: GZH Home Redesign 2024
├── portfolio-publicidade.html    Case: Portfólio de Publicidade GZH
├── css/style.css                 Sistema visual (DM Sans + Fraunces, âmbar/terracota/linho)
└── assets/                       Imagens dos cases e foto de perfil
```

## Desenvolvimento local

Não há build. Basta abrir o `index.html` no navegador, ou servir a pasta com qualquer servidor estático:

```
npx serve .
```

## Deploy

O deploy é feito no Cloudflare Pages via Wrangler:

```
npx wrangler pages deploy . --project-name=matheusojorge
```

Alternativa com Git: no painel do Cloudflare Pages, conecte o repositório do GitHub ("Connect to Git"), deixe o build command vazio e use `/` como output directory. Assim, cada push na branch principal publica automaticamente.

## Ajustes rápidos

- Cores e fontes estão em variáveis no topo de `css/style.css`
- A frase do hero e os textos de contato estão direto no `index.html`
- Para adicionar um novo case, duplique uma página existente e inclua o card correspondente na home
- Imagens novas: exportar em PNG ou WebP com até 1600px de largura para carregar rápido
