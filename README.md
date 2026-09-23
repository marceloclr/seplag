# Portal SEPLAG

Página única que reúne os sistemas da SEPLAG publicados no GitHub Pages. Assim ninguém precisa decorar os endereços.

**Endereço:** https://marceloclr.github.io/seplag/

## Como funciona

- Cada sistema abre numa **aba dentro do portal** (um iframe). Ao trocar de aba, o sistema continua carregado e o trabalho em memória não se perde.
- **Início**: cartões dos sistemas com busca (<kbd>Ctrl</kbd>+<kbd>K</kbd>), indicação de "no ar" e data da última publicação (lida do cabeçalho `Last-Modified` do Pages).
- Barra do alto: abas abertas, **Recarregar**, **Nova janela** (abre o sistema numa aba do navegador), busca e tema claro/escuro.
- Atalhos: <kbd>Alt</kbd>+<kbd>0</kbd> volta ao início; <kbd>Alt</kbd>+<kbd>1</kbd>…<kbd>9</kbd> vai para as abas; o botão do meio do mouse fecha uma aba.
- Link direto para um sistema: `…/seplag/#/saneamento`, `…/seplag/#/sipog`.
- O tema e as abas abertas ficam guardados só neste navegador (`localStorage`).

## Sistemas cadastrados

| Sistema | Endereço |
|---|---|
| Saneamento de MAPPs (+ versão essencial e manual) | https://marceloclr.github.io/saneamento/ |
| SIPOG — Projeção Orçamentária e Gestão Financeira | https://marceloclr.github.io/sipog/ |

## Incluir um sistema

No `index.html`, acrescente um objeto à constante `SISTEMAS`: `id`, `nome`, `sigla`, `url`, `descricao`, `etiquetas`, `cores` (duas cores do degradê), `icone` (chave de `ICONES`) e, se houver, `extras` (entradas secundárias que também abrem em aba). O sistema precisa aceitar ser aberto em frame. Os sites do GitHub Pages aceitam.
