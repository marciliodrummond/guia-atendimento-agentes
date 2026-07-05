# Correção v7 — conteúdo invisível no miolo do guia

## Problema identificado

O conteúdo do guia estava presente no `index.html`, mas algumas seções do miolo podiam ficar invisíveis em determinados ambientes de visualização.

A causa provável era o uso da classe `reveal` com `opacity: 0` como estado inicial. O conteúdo dependia de JavaScript e IntersectionObserver para receber a classe `visible`. Se o ambiente bloqueasse, atrasasse ou falhasse na execução do script, a página mostrava apenas o fundo escuro, parecendo que o miolo estava preto e sem informações.

## Correção aplicada

- O comportamento de ocultar seções antes da animação agora só acontece quando o navegador confirma JavaScript ativo, por meio da classe `.js` no elemento HTML.
- Se JavaScript estiver desativado ou bloqueado, o conteúdo fica visível por padrão.
- Foi adicionado um fallback que torna todas as seções `reveal` visíveis após alguns milissegundos, mesmo se o IntersectionObserver não executar como esperado.
- Mantidas as animações e a experiência premium quando o navegador executa tudo normalmente.

## Validação

- O conteúdo do título, hero, cenas e seção "Conheça o especialista" segue presente no HTML.
- O JavaScript foi validado com `node --check`.
- O ZIP foi recriado e testado com `unzip -t`.

## Arquivos atualizados

- `index.html`
- `guia-atendimento-que-vira-contrato-v7.zip`
