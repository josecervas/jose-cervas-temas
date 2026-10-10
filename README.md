# Temas do JC Painel

Loja de temas (`.jctema`) do **JC Painel**, a tela do brassador José Cervas.
O painel lê o `index.json` deste repositório, mostra as prévias e instala o
tema escolhido.

Também hospeda a [política de privacidade do app José Cervas](privacidade/).

## Como funciona

- `index.json` — a lista de temas. Para cada tela do tema há o arquivo e o
  código de conferência (`sha256`). O painel recusa um arquivo que não bate com
  o código, então ninguém troca um tema sem passar por aqui.
- `temas/<id>/` — os arquivos `.rfwtxt` de cada tela e a `previa.png` (800×480).
- Um tema **não é programa**: só usa as peças e os dados que o painel oferece,
  e os botões só mandam eventos de uma lista fixa. Um tema nunca consegue mexer
  na resistência nem pular uma confirmação de segurança. O formato completo está
  em `CONTRATO/jctema.md` no código do painel.

## Enviar um tema

1. Faça um *fork* deste repositório.
2. Crie `temas/<seu-id>/` com os `.rfwtxt` e uma `previa.png`.
3. Acrescente o tema no `index.json` (o `sha256` de cada arquivo:
   `sha256sum arquivo.rfwtxt` ou `Get-FileHash arquivo.rfwtxt` no Windows).
4. Abra um *pull request*. O tema aparece no painel quando for aprovado.

## Publicar (para o dono do repositório)

1. Suba esta pasta inteira para um repositório **público** `jose-cervas-temas`.
2. *Settings › Pages › Deploy from a branch › main › / (root)*.
3. Endereços:
   - Lista de temas: `https://josecervas.github.io/jose-cervas-temas/index.json`
   - Política de privacidade: `https://josecervas.github.io/jose-cervas-temas/privacidade/`
