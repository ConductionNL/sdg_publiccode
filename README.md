# sdg_publiccode

## Single Digital Gateway Invoervoorziening

Met deze repository kan de SDG Invoervoorziening API gebruikt en getest worden op [Conductions gateway](https://github.com/ConductionNL/commonground-gateway). Ook dankzij de publiccode.yaml kan de API gevonden worden via github's API en daarmee gebruikt/geinstalleerd worden op omgevingen waar de gateway gebruikt wordt.

Er zit ook een testdata set die standaard meegeladen wordt bij het gebruik van de API. Deze kan je vinden in /data/sdg.json.

Als je meer wilt lezen over de Single Digital Gateway Invoervoorziening kan dat op de [pagina van de VNG](https://vng.nl/projecten/single-digital-gateway).

Als je de documentatie van de API wilt bekijken kan dat op de [redoc pagina](https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/maykinmedia/sdg-invoervoorziening/master/src/openapi.yaml&nocors).

### Local setup

Je hebt [Docker desktop](https://www.docker.com/get-started/) nodig als je deze API lokaal wilt gebruiken op de gateway.

Zodra je docker geinstalleerd hebt moet je met een cmd naar de root van het project.
Dan kan je de image pullen met:
```sh
docker-compose pull
```
Daarna kan je de image draaien met: 
```sh
docker-compose up
```
Als de php container laat zien: "Ready to handle connections" is de gateway gereed.

De API draait op port :80 en de calls van deze API vallen op /api/
Om bijvoorbeeld contactmomenten te bevragen kan dat lokaal op localhost/api/producten

Andere ports die door de gateway gebruikt worden zijn: :82, :5342

