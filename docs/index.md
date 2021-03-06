# Building SDIs and geoportals with GeoNode and a search engine


## Organizers

* Paolo Corti - Center for Geographic Analysis, Harvard University
* Ben Lewis - Center for Geographic Analysis, Harvard University
* Devika Kakkar - Center for Geographic Analysis, Harvard University

## Abstract

[WorldMap](http://worldmap.harvard.edu/) is an SDI/GeoPortal project running since 2010 by the [Center for Geographic Analysis, Harvard University](http://gis.harvard.edu/), that exposes 25k+ internal layers, 200k+ remote layers, 7k+ maps and used by 20k+ registered users. It is built on top of [GeoNode](http://docs.geonode.org/) and its core components ([Django](https://www.djangoproject.com/), [GeoServer](http://geoserver.org/), [GeoWebCache](http://www.geowebcache.org/), [PostgreSQL](https://www.postgresql.org/)/[PostGIS](http://postgis.net/), [pycsw](http://pycsw.org/)).

Users can build maps with a web browser using the internal layers (stored in the PostGIS database and the filesystem and exposed by GeoServer as OGC web services) and the remote layers, exposed by external OGC and Esri Rest Web Services. Remote layers are harvested, health checked, processed and exposed with a system based on Django and [MapProxy](https://mapproxy.org/), named [Harvard Hypermap (HHypermap)](https://github.com/cga-harvard/HHypermap). A search engine, based on [Solr](http://lucene.apache.org/solr/) or [Elasticsearch](https://www.elastic.co/products/elasticsearch), enriches the WorldMap user's experience providing powerful features such as keyword, spatial and temporal facets, full text search, natural language processing, weighted results and much more.

The organizers will lead the workshop’s participants, with a series of step by step tutorials, to setup a development environment containing all the needed components, to get a basic understanding of the solution stack involved to replicate such an architecture in their own geoportals/SDIs implementation, and to discuss optimization techniques for taking advantage of the solution for handling a large number of datasets.

The workshop is targeted to geospatial developers who should have a basic understanding of web development, OGC standards and spatial databases.

## Prerequisites

You need to take your notebook at the workshop. The notebook should have at least 4GB of RAM. You can use any operating system (Linux, OS X, Windows), provided that you install the following tools:

* [git](https://git-scm.com/downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
* [QGIS](http://www.qgis.org/en/site/forusers/download.html)
* [Firefox](https://www.mozilla.org/en-US/firefox/new/)

Note: you could use [Chrome](https://www.google.com/chrome/browser/desktop/index.html) in place of Firefox for all of the tutorials of this workshop. Though, one tutorial will use the [Firefox Developer Tools](https://developer.mozilla.org/en-US/docs/Tools/Tools_Toolbox) to inspect requests to the OGC services. If using Chrome you should be able to follow along that tutorial using the [Chrome Developer Tools](https://developer.chrome.com/devtools)

## Outline of tutorials

* Introduction
* [Setup the workshop environment](00_setup_the_workshop_environment.md)
* [A GeoNode quickstart](01_geonode_quickstart.md)
* [Programming GeoNode with Python](02_programming_geonode_with_python.md)
* [OGC services with GeoServer](03_geoserver.md)
* [Tiles caching with GeoWebCache](04_geowebcache.md)
* [Catalogue services with pycsw](05_pycsw.md)
* [Spatial queries with PostGIS](06_postgis.md)
* [Using GeoNode OGC services with external clients](07_ows_integration.md)
* [Using GeoNode management commands](08_geonode_commands.md)
* [Using a search engine with GeoNode: a quick tour of Solr](09_solr.md)
* [Developing a custom application for GeoNode](10_customization.md)
* [Running asynchronous tasks using a task queue (Celery/RabbitMQ)](11_celery.md)
