# Python Maps Mapmatching with Valhalla

## Setup

```
docker login ghcr.io

docker pull ghcr.io/gis-ops/docker-valhalla/valhalla:latest
```

```
wget http://download.geofabrik.de/europe/germany/baden-wuerttemberg-latest.osm.pbf
```

```
docker run -it --rm --name valhalla -p 8002:8002 -v $PWD/valhalla:/custom_files/ -e serve_tiles=True -e build_admins=True ghcr.io/gis-ops/docker-valhalla/valhalla:latestc
```

## Map Matching with Python

## Jupyter with Visual Studio Code

https://code.visualstudio.com/docs/datascience/jupyter-notebooks

## Requests

curl http://localhost:8002/route --data '{"locations":[{"lat":48.632608,"lon":9.010350,"type":"break"},{"lat":48.631776,"lon":9.011528,"type":"break"}],"costing":"auto","directions_options":{"units":"miles"}}' | jq '.'

## Map Matching with Valhalla

https://towardsdatascience.com/map-matching-done-right-using-valhallas-meili-f635ebd17053

https://github.com/zotttttttt/gps-trace-optimization/blob/main/GPS-trace-optimization-via-Valhalla.ipynb

## OpenStreetMap Data Extracts

http://download.geofabrik.de/

## Q&A

https://stackoverflow.com/questions/12141422/error-gdal-config-not-found-while-installing-r-dependent-packages-whereas-gdal

https://stackoverflow.com/questions/54734667/error-installing-geopandas-a-gdal-api-version-must-be-specified-in-anaconda

https://github.com/valhalla/valhalla/issues/3544