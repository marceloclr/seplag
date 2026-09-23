# Portal de Gestão Financeira e Projetos

Portal particular para pequenos projetos de trabalho da Sistemas de Gestão Pública. Reúne os sistemas publicados no GitHub Pages, sem precisar decorar os endereços.

**Endereço:** https://marceloclr.github.io/seplag/

## Como funciona

- **Tela de senha** no estilo terminal. O campo *user* mostra `root` esmaecido e recebe o cursor verde do terminal; só a senha é exigida. O campo de senha não é do tipo `password` (a senha fica só na memória do script e a tela mostra bolinhas), para que nenhum navegador ofereça salvar ou preencher a senha. A janela pulsa de leve até algo ser digitado; Enter com campos vazios também vibra. Erro treme a janela com borda vermelha; acerto pulsa em verde (a mesma vibração do sistema de comunicação). O fundo é um corredor de data center desenhado em canvas: LEDs brancos, verdes e laranja (status e atividade), poeira na luz, varredura no piso e aproximação lenta da câmera. O código guarda apenas o SHA-256 da senha, e a liberação dura enquanto o navegador estiver aberto (`sessionStorage`). **Sair**, no alto, volta à tela de senha. Atenção: num site estático, essa senha é uma cortina contra quem abre o link por acaso, não uma proteção real. O código é público e os sistemas continuam acessíveis pelos próprios endereços.
- Cada sistema abre numa **aba dentro do portal** (um iframe). Ao trocar de aba, o sistema continua carregado e o trabalho em memória não se perde.
- **Início**: cartões dos sistemas com indicação de "no ar" e data da última publicação (lida do cabeçalho `Last-Modified` do Pages).
- Barra do alto: abas abertas, **Recarregar**, **Nova janela** (abre o sistema numa aba do navegador), **Sair** e tema claro/escuro.
- A busca está oculta enquanto houver poucos sistemas. Para mostrá-la, ponha `BUSCA_VISIVEL = true` no `index.html`.
- Atalhos: <kbd>Alt</kbd>+<kbd>0</kbd> volta ao início; <kbd>Alt</kbd>+<kbd>1</kbd>…<kbd>9</kbd> vai para as abas; o botão do meio do mouse fecha uma aba.
- Link direto para um sistema: `…/seplag/#/saneamento`, `…/seplag/#/sipog`.
- O tema e as abas abertas ficam guardados só neste navegador (`localStorage`, chave `gfp.portal`).

## Sistemas cadastrados

| Sistema | Endereço |
|---|---|
| Saneamento de MAPPs (+ versão essencial e manual) | https://marceloclr.github.io/saneamento/ |
| SIPOG — Projeção Orçamentária e Gestão Financeira | https://marceloclr.github.io/sipog/ |

## Incluir um sistema

No `index.html`, acrescente um objeto à constante `SISTEMAS`: `id`, `nome`, `sigla`, `url`, `descricao`, `etiquetas`, `cores` (duas cores do degradê), `icone` (chave de `ICONES`) e, se houver, `extras` (entradas secundárias que também abrem em aba). O sistema precisa aceitar ser aberto em frame. Os sites do GitHub Pages aceitam.
