# Qual é esse país?

Jogo de geografia em português: descubra o país pela silhueta, use uma dica ou escolha entre quatro alternativas. Cada rodada começa com três vidas.

**Jogar:** <https://leticia-americo.github.io/jogo-silhueta/>

## Rodar no computador

1. Abra o PowerShell nesta pasta.
2. Inicie um servidor local:

   ```powershell
   py -m http.server 8000
   ```

3. Acesse <http://localhost:8000> no navegador.
4. Para parar o servidor, volte ao PowerShell e pressione `Ctrl+C`.

O servidor local é necessário porque o navegador pode bloquear o `fetch` do GeoJSON quando a página é aberta diretamente como arquivo.

## Publicar no GitHub Pages

1. Crie no GitHub um repositório **público** chamado `jogo-silhueta`.
2. Conecte esta pasta ao repositório e envie a branch `main`:

   ```powershell
   git remote add origin https://github.com/leticia-americo/jogo-silhueta.git
   git push -u origin main
   ```

3. No GitHub, abra **Settings → Pages** e escolha **Deploy from a branch**, branch `main` e pasta `/(root)`.
4. Aguarde a publicação em <https://leticia-americo.github.io/jogo-silhueta/>.

## Dados

- Os mapas dos países são carregados em tempo de execução do [datasets/geo-countries](https://github.com/datasets/geo-countries), arquivo [`countries.geojson`](https://raw.githubusercontent.com/datasets/geo-countries/master/data/countries.geojson).
- Os nomes em português e as pistas geográficas incluídos nos arquivos JavaScript foram preparados a partir da base [mledoze/countries](https://github.com/mledoze/countries). Esses dados ficam no projeto; não há uma chamada adicional a essa fonte quando o jogo abre.

O jogo usa HTML, CSS e JavaScript puros, sem frameworks, dependências de build, chaves de API ou backend.
