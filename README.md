# battle-royale-chat

Battle royale pra live do TikTok, em temporada. Todo mundo que comenta entra na arena e vai sendo eliminado rodada por rodada até sobrar um campeão. Layout vertical 9:16, arquivo único (`index.html`).

## Como funciona

- **Temporada:** 3 partidas com ranking de pontos acumulado. No fim sai o campeão e começa outra temporada. O ranking fica salvo no navegador.
- **Partida:** lobby de 30s onde quem comenta entra, depois rodadas de eliminação e um duelo final.
- **Rodadas:**
  - Zona de perigo: o chat escolhe uma zona com `!1` a `!4` e a tempestade cai em 1 ou 2 zonas.
  - Maratona: quem tiver menos atividade cai.
  - Roleta: eliminação por sorte.
- **Duelo final:** os 3 melhores brigam e quem já caiu vota com `!1`, `!2` ou `!3`.
- **Escudo:** presente, 30 curtidas ou compartilhar. Salva de uma eliminação.
- **Vida extra:** seguir. Quem cai volta na rodada seguinte.
- **Pontos:** pela colocação (100, 70, 50...) mais 5 por rodada sobrevivida.

## Como usar

1. TikFinity aberto e conectado na live (WebSocket em `ws://localhost:21213`).
2. Abre o `index.html` no navegador e captura a janela no TikTok Live Studio ou no OBS.

Aperta **T** pro modo teste (espectadores falsos, jogadores automáticos, pular fase). **Espaço** pula a fase atual.

Parâmetros na URL: `?speed=4` acelera tudo, `?matches=2` muda o número de partidas, `?ws=ws://localhost:PORTA/` troca a porta. Durações, cortes e pontos ficam no bloco `CFG` do script.

## Nota

Testei uma partida inteira com jogadores falsos, mas não com o TikFinity ligado de verdade.
