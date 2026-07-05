# Atualização v6 — foto do especialista

Atualização realizada em 2026-06-30 21:54 UTC.

## O que foi ajustado

- A seção "Conheça o especialista" agora usa a foto enviada pelo usuário.
- A imagem foi otimizada para web em `marcilio-especialista.jpg`, mantendo a proporção retrato e reduzindo o peso do carregamento.
- O HTML deixou de usar a imagem antiga em base64 como fundo do bloco do especialista.
- A foto agora é um `<img>` real com `alt`, `loading="lazy"` e `decoding="async"`, melhorando acessibilidade e performance.
- O CSS da foto foi ajustado com `object-fit: cover` e `object-position: 50% 18%` para preservar rosto e enquadramento no card quadrado.

## Arquivos alterados

- `index.html`
- `marcilio-especialista.jpg`
- `marcilio-especialista-thumb.png`
- `guia-atendimento-que-vira-contrato-v6.zip`
