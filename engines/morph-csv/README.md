# Morph-CSV
This folder contains the Dockerfile needed to run Morph-CSV:1.0.0 over the GTFS-Benchmark

## Ontop Docker image
The created docker image is available at: [https://hub.docker.com/r/oegdataintegration/morph-csv](https://hub.docker.com/r/oegdataintegration/morph-csv)

## Create your own image
Go to Morph-CSV Github and a choose your version from releases, here is an example with Morph-CVS-1.0.0:
```bash
git clone https://github.com/oeg-upm/gtfs-bench
cd gtfs-bench/engines/morph-csv
wget https://github.com/oeg-upm/morph-csv/archive/morph-csv-1.0.0.zip
unzip morph-csv-1.0.0.zip -d .
docker build -t morph-csv .
```

## How to run a query over
```bash
docker exec -it morph-csv /morph-csv/run.sh pathToConfigFile.json
```