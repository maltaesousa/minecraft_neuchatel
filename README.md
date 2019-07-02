# Minecraft &reg; à la carte - Neuchâtel

## Requirements

* Postgresql with postgis
* Python > 3.6
* Pipenv

## Install

Clone this repository  and open a shell at the root of your project. Get assets by downloading them in the assets folder.

```powershell
curl https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css -o minecraft\static\bootstrap\bootstrap.min.css
curl https://code.jquery.com/jquery-3.3.1.min.js -o minecraft\static\jquery\jquery-3.3.1.min.js
curl https://code.jquery.com/ui/1.12.1/jquery-ui.min.js -o minecraft\static\jquery-ui\jquery-ui.min.js
curl https://cdn.rawgit.com/openlayers/openlayers.github.io/master/en/v5.3.0/build/ol.js -o minecraft\static\ol\ol.js
curl https://cdn.rawgit.com/openlayers/openlayers.github.io/master/en/v5.3.0/css/ol.css -o minecraft\static\ol\ol.css
curl https://raw.githubusercontent.com/proj4js/proj4js/2.5.0/dist/proj4.js -o minecraft\static\proj4\proj4.js
curl https://raw.githubusercontent.com/Viglino/ol-ext/master/dist/ol-ext.min.js -o minecraft\static\ol-ext\ol-ext.min.js
curl https://raw.githubusercontent.com/Viglino/ol-ext/master/dist/ol-ext.min.css -o minecraft\static\ol-ext\ol-ext.min.css
curl https://raw.githubusercontent.com/sitn/sitnlayers/master/js/sitnlayers.js -o minecraft\static\sitnlayers\sitnlayers.js
curl https://use.fontawesome.com/releases/v5.5.0/fontawesome-free-5.5.0-web.zip -o minecraft\static\fa.zip
Expand-Archive minecraft\static\fa.zip -DestinationPath minecraft\static
Get-childitem -Path minecraft\static\fontawesome* | rename-item -NewName fontawesome
del minecraft\static\fa.zip
```

Define environment variables like in `.env.sample` and save it to a .env file.

```powershell
pipenv install
pipenv shell
flask run
```