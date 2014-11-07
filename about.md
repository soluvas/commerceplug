---
layout: page
title: About
permalink: /about/
---

**CommercePlug** is an Extensible Open E-commerce Hypermedia API-based Protocol, inspired by [FoxyCart Hypermedia API](http://www.foxycart.com/features/feature/integration/api).

CommercePlug is the native Integration Protocol for [Bippo Commerce](http://www.bippo.co.id/).

## E-commerce APIs

1. [FoxyCart Hypermedia API v1](http://www.foxycart.com/features/feature/integration/api)
2. [SpreeCommerce API](http://guides.spreecommerce.com/api/)
3. [Shopify API](http://docs.shopify.com/api)
4. [Bippo Commerce API (CommercePlug)](http://soluvas.github.io/commerceplug)
5. [Demandware Open Commerce API](http://www.programmableweb.com/api/demandware-open-commerce). I can't find any documentation. -Hendy

## Target Protocols for Request-Response Style

1. Hypermedia API using [application/hal+json media type](http://stateless.co/hal_specification.html).
   Make it browsable using [HAL Browser](https://github.com/mikekelly/hal-browser).
2. TODO: OData endpoint
3. TODO: SPARQL endpoint. See [LB2CO Semantic Ontology Framework](http://www.ijorcs.org/uploads/archive/Vol4-Iss1-01-lb2co-a-semantic-ontology-framework.pdf).

## Target Protocols for Messaging Style

1. TODO: MQTT
2. TODO: AMQP

## Deliverables

1. [Specification](https://github.com/soluvas/commerceplug)
2. TODO: SDK for Java, includes Core Library (usable for both server and client), SPI, and Client Library
3. TODO: CLI client implemented using Spring Boot
4. TODO: AngularJS client library (required for Ionic client)
5. TODO: mobile-friendly web-based client implemented using Ionic
6. TODO: Client SDK for other programming languages?

## Resources

1. [GoodRelations ontology](http://www.heppnetz.de/projects/goodrelations/)
2. [Vocabularies](http://wiki.goodrelations-vocabulary.org/Vocabularies). Primary vocabularies are [Product Ontology](http://www.productontology.org/) and [OPDM](http://www.ebusiness-unibw.org/ontologies/opdm/)
3. [Examples of Hypermedia API calls for E-commerce platforms](https://gist.github.com/hjr3/2289546)
4. [The Hypermedia Debate by FoxyCart](http://www.foxycart.com/blog/the-hypermedia-debate)

## Naming Conventions

CommercePlug uses lowerCamel for fields and paths, similar to Google's API conventions.
It makes mapping to [Linked Data](http://www.w3.org/standards/semanticweb/data) technologies ([schema.org](http://schema.org/), RDF, SPARQL) more natural, and also natural to JavaScript programmers.

CommercePlug uses plural path names. Spree, Shopify, FoxyCart, Twitter, Google, Facebook, use plural e.g. `people`.

Some considerations:

* Spree, FoxyCart, Shopify, Twitter uses lower_under for everything
* Google uses lowerCamel including for URI paths (e.g. "/calendarList") -- which makes sense since they use Java
* LinkedIn uses lower-dash for both URI paths and fields (note: XML only, not JSON)
* Foursquare uses lowerCamel for fields and lowermerged for paths

## Versioning

CommercePlug uses required header which is sent in all requests, but especially important in the main endpoint URI (`api.domain.com` or `www.domain.com/api`):

    CommercePlug-Version: 1.0

Considerations:

* "FoxyCart uses Required Header: Include FOXYCART-API-VERSION: 1
* Spree & Shopify use no versioning (and shouldn't be required on HATEOAS-compliant endpoint?)
* Google & LinkedIn uses /v1, Twitter uses /1.1, Facebook uses /v2.2"

## Contact Me

[hendy@soluvas.com](mailto:hendy@soluvas.com)
