# PDC Component

## PDC Component aan de hand van de Single Digital Gateway Invoervoorziening

Met deze repository kan het PDC Commponent als API gebruikt en getest worden. Daarnaast voorziet deze repository doormiddel van een [publiccode.yaml](https://yml.publiccode.tools/) in een API implemenatie die door middel van de commongateway op kubernetes/haven omgevingen geinstaleerd kan worden.

Er zit ook een testdata set die kan worden meegeladen bij het gebruik van de API. Deze kan je vinden in /data/sdg.json.

Als je meer wilt lezen over de Single Digital Gateway Invoervoorziening kan dat op de [pagina van de VNG](https://vng.nl/projecten/single-digital-gateway).

Als je de documentatie van de API wilt bekijken kan dat op de [redoc pagina](https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/maykinmedia/sdg-invoervoorziening/master/src/openapi.yaml&nocors).

### Local setup

Voor het locaal gebruik van deze API is [Docker desktop](https://www.docker.com/get-started/) nodig.

Na het installeren van docker kan de API locaal worden opgestart door het clonen van de repository en naar de map te gaan waar de code heen is geclonded. 

De container kan vervolgens vnuit de repro via de commandline worden opgestart met: 
```sh
docker-compose up
```
Als de  container laat zien: "Ready to handle connections" is de api gereed.

Bij eventuele problemen kan het verstandig zijn de image eerst te pullen: 
```sh
docker-compose pull
```

De API draait op port :80 en de calls van deze API vallen op /api/. Documentatie is na opstarten ebschikbaar via [localhost/api/](http://localhost/api/).

Andere ports die gebruikt worden zijn: :82, :5342

