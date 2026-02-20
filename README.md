# d4c-service-ows

A collection of deployment configurations and code for serving Open Geospatial Consortium (OGC) compliant services. This repository provides the infrastructure to serve Canadian geospatial data via:

* **Web Map Service (WMS)** and **Web Map Tile Service (WMTS)**
* **Web Processing Service (WPS)**
* **XYZ Tiles (Raster & Vector)**

## Purpose

The goal of this repository is to provide the service layer for the **Data for Canada (d4c)** project. It acts as the gateway for legacy and standard-compliant GIS clients to interact with a decentralized, cloud-native open data infrastructure. By containerizing services like GeoServer and Martin, we ensure high-performance access to national datasets via traditional OGC standards, and next-generation tile formats.

## Core Technologies

This service layer is built to interface with modern cloud-native formats while maintaining broad compatibility:

* **[FAIR Data Catalogue](https://stac-geoparquet.org/):** For cataloging and discovering underlying datasets.
* **[GeoParquet](https://geoparquet.org/):** An efficient, columnar storage format for vector data, providing the high-performance backend for our services.
* **[GeoZarr](https://github.com/zarr-developers/geozarr-spec):** For multidimensional data processing and visualization.
* **HTTP & [P2P](https://tixati.com/specs/bittorrent):** For efficient, decentralized data retrieval and backend distribution.

## Supported Services

We utilize industry-standard open-source applications to provide specific spatial capabilities:

* **GeoServer:** Primary engine for WMS, WMTS, and WFS layers, capable of connecting to cloud-native data stores.
* **Martin:** High-speed raster and vector tile server (MVT) providing XYZ access to modern file formats.
* **ZOO-Project:** WPS implementation for server-side geospatial processing and analytics, leveraging modern file formats for complex computations.

## Contributing

New service configurations or updates to existing layers should be proposed via pull requests. All changes to service logic must align with the d4c goal of decentralized distribution.

All contributors must be verified via **[Vouch](https://github.com/mitchellh/vouch)** before their pull requests are reviewed.
