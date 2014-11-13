**CommercePlug** is an Extensible Open E-commerce Hypermedia API-based Protocol, inspired by [FoxyCart Hypermedia API](http://www.foxycart.com/features/feature/integration/api).

CommercePlug is the native Integration Protocol for [Bippo Commerce](http://www.bippo.co.id/).

## E-commerce APIs

1. [FoxyCart Hypermedia API v1](http://www.foxycart.com/features/feature/integration/api)
2. [SpreeCommerce API](http://guides.spreecommerce.com/api/)
3. [Shopify API](http://docs.shopify.com/api)
4. [Bippo Commerce API (CommercePlug)](http://soluvas.github.io/commerceplug)
5. [Google Content API for Shopping](https://developers.google.com/shopping-content/)
6. [Demandware Open Commerce API](http://www.programmableweb.com/api/demandware-open-commerce). I can't find any documentation. -Hendy

## Goals

1. Practically adaptable to multiple protocol styles, both request-response and asynchronous messaging.
2. Consistent ontology, representable in OWL, which in turn supports the goals below.
3. Practically adaptable to multiple representation formats, initially [JSON-LD](json-ld.org) + [Hydra](http://www.hydra-cg.com/) + [schema.org](http://schema.org/) but can be represented in [application/hal+json media type](http://stateless.co/hal_specification.html), Siren, XML, Atom, and RDF.
4. Easy object binding using Jackson for Java, Groovy, Scala, Clojure; with [polymorphic deserialization](http://wiki.fasterxml.com/JacksonPolymorphicDeserialization).
5. Easy HATEOAS support using Spring HATEOAS.
6. Extensible, additional relations, classes, and properties are possible and encouraged; a la [XMPP Extensions](http://xmpp.org/xmpp-protocols/xmpp-extensions/).
7. Provides batch operations to support bulk and Big Data scenarios.
8. Provides streaming operations for real time (Fast Data) support.
9. Selective import/export functionality that can be used both for backup-restore and also moving data across environments (development to production and vice versa) and different e-commerce providers.

## Target Protocols for Request-Response Style

1. [JSON-LD](json-ld.org) + [Hydra](http://www.hydra-cg.com/). See below for supported vocabularies.
2. TODO: Hypermedia API using [application/hal+json media type](http://stateless.co/hal_specification.html).
   Make it browsable using [HAL Browser](https://github.com/mikekelly/hal-browser).
3. TODO: OData endpoint
4. TODO: Triple Pattern Fragment / SPARQL endpoint. See [LB2CO Semantic Ontology Framework](http://www.ijorcs.org/uploads/archive/Vol4-Iss1-01-lb2co-a-semantic-ontology-framework.pdf).

## Target Protocols for Asynchronous Messaging Style

1. TODO: MQTT
2. TODO: AMQP

## Vocabularies

1. [schema.org](http://schema.org/). Default vocabulary.
2. [Hydra](http://www.hydra-cg.com/) vocabulary for links and operations (JSON-LD only).
3. [ProductOntology.org](http://www.productontology.org) for product types.
4. [OPDM Ontologies](http://www.ebusiness-unibw.org/ontologies/opdm/) for domain specific vocabularies.

## Deliverables

1. [Specification](https://github.com/soluvas/commerceplug)
2. TODO: SDK for Java, includes Core Library (usable for both server and client), SPI, and Client Library
3. TODO: CLI client implemented using Spring Boot
4. TODO: AngularJS client library (required for Ionic client)
5. TODO: mobile-friendly web-based client implemented using Ionic
6. TODO: Client SDK for other programming languages?

## Resources

1. [schema.org ontology](http://schema.org/)
2. [GoodRelations ontology](http://www.heppnetz.de/projects/goodrelations/)
3. [Vocabularies](http://wiki.goodrelations-vocabulary.org/Vocabularies). Primary vocabularies are [Product Ontology](http://www.productontology.org/) and [OPDM](http://www.ebusiness-unibw.org/ontologies/opdm/)
4. [Examples of Hypermedia API calls for E-commerce platforms](https://gist.github.com/hjr3/2289546)
5. [The Hypermedia Debate by FoxyCart](http://www.foxycart.com/blog/the-hypermedia-debate)

### Acknowledged Submissions to W3C related to Electronic Commerce

Source: http://www.w3.org/TR/EC-related-activities

W3C Member organizations may submit submissions to propose technology or other ideas for consideration by W3C. W3C has acknowledged Submissions from Members that are related to the Electronic Commerce area. These submissions were brought to the attention of the participants in the Electronic Commerce Interest Group for consideration. Related Working Group are invited to pick up these Submissions for discussion as requirements and design input. 
These documents are also made available to the public for consideration.

1. [UCLP](http://www.w3.org/Submission/1999/02/) - The Universal Commerce Language and Protocol is an Extensible Markup Language (XML) application for metadata related to commercial products and companies and that can be used in identifying and retrieving product data residing across the Internet.
2. [ICE](http://www.w3.org/Submission/1998/18/) - The Information and Content Exchange Protocol proposes a protocol and data format to implement the shared business rules in the domain of syndicated content, on top of the Web infrastructure of XML, HTTP, and URIs.
3. [XFDL](http://www.w3.org/Submission/1998/16/) - The Extensible Forms Description Language describes an XML syntax to represent complex forms such as those found in business and government.
4. [SDML](http://www.w3.org/Submission/1998/09/) - The Signed Document Markup Language describes how to structure a complete signed document, with the material being signed as part of the document. We expect that a web-based document signature scheme would have to address external documents, also referenced by URI. SMDL was an important initial contribution to the XML Signature Working Group.

### Other resources related  to Electronic Commerce

Following is a non exhaustive list of resources related  to Electronic Commerce:

1. [Biztalk](http://www.biztalk.org/) - A community of standards users, with the goal of driving the rapid, consistent adoption of XML to enable electronic commerce and application integration.
2. [CommerceNet](http://www.commerce.net/) - CommerceNet is a non-profit membership organization meeting the evolving needs of companies doing electronic commerce. Since its founding in 1994, CommerceNet's mission has been to promote and advance interoperable electronic commerce to support emerging communities of commerce.
3. [ECML](http://www.ecml.org/) - The Electronic Commerce Modeling Language provides a simple set of guidelines for web merchants that will enable digital wallets from multiple vendors to automate the exchange of information between users and merchants.
4. [FSTC](http://www.fstc.org/index.html) - The mission of the Financial Services Technology Consortium (FSTC) is to leverage the strength of US financial services organizations through joint research and development focused on technology opportunities, adding business value, managing risk, and reducing costs.
5. [IOTP](http://www.iotp.org/) - The Open Trading Protocol was developed by a number of organisations, working co-operatively to make widespread Internet trading a convenient and secure reality.
6. [OASIS](http://www.oasis-open.org/) - A community resource designed to provide a credible source of accurate, timely information about the application of XML in industrial and commercial settings.
7. [XML/EDI](http://www.geocities.com/WallStreet/Floor/5815/index.html) - Provides a standard framework to exchange different types of data -- for example, an invoice, healthcare claim, project status -- so that the information be it in a transaction, exchanged via an Application Program Interface (API), web automation, database portal, catalog, a workflow document or message can be searched, decoded, manipulated, and displayed consistently and correctly by first implementing EDI dictionaries and extending our vocabulary via on-line repositories to include our business language, rules and objects.

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

The version follows [semantic versioning](http://semver.org/).

Considerations:

* "FoxyCart uses Required Header: Include `FOXYCART-API-VERSION: 1`
* Spree & Shopify use no versioning (and shouldn't be required on HATEOAS-compliant endpoint?)
* Google & LinkedIn uses /v1, Twitter uses /1.1, Facebook uses /v2.2"

## `@type` Field for Polymorphic Class Mapping

The `@type` field is reserved (and has the exact meaning in JSON-LD). In practice, it is used to aid object mapping/binding using [Jackson](http://wiki.fasterxml.com/JacksonHome), [jenabean](https://code.google.com/p/jenabean/), [JAXB](https://jaxb.java.net/), etc.

The `@type` may refer to a generic superclass e.g. `ProductOrService` or a subclass e.g. `SomeItems`.
An OO class may be an instance of one or more Linked Data classes. e.g. `Product` represents both [schema.org Product](http://schema.org/Product) and [GoodRelations ProductOrService](http://www.heppnetz.de/ontologies/goodrelations/v1.html#ProductOrService) and ProductOntology classes. These are cases in which `additionalType` array will be needed.

Note that a property may be loosely typed, e.g. `Product.brand` can be either `Organization` or `Brand`. In the OO class this results in convenience `OrganizationOrBrand` interface which extends both `Organization` and `Brand`, and the actual runtime instance can be of class `OrganizationImpl` or `BrandImpl`, which implements `OrganizationOrBrand` as well. Unsupported methods throw `UnsupportedOperationException`. The alternative is just to use `Thing` interface which is fine for Groovy and Nashorn but requires casting in Java and Scala.

For cardinality, we opt for common cases. For example, `brand` is singular, and must be represented as a single JSON object when there's only one `Brand`. However, `image` is always represented as an array, because commonly a `Product` has multiple `image`s. This allows naive clients to hardcode the JSON structure, while still complying to JSON-LD spec. There may be a case when a `Product` has multiple `brand`s, the server may choose:

1. Render only the first/primary `brand`, sacrificing detail to make it easy for naive clients.
2. Render `brand` as array, retaining detail while potentially breaking naive clients.

[Issue #611 in Jackson](https://github.com/FasterXML/jackson-databind/issues/611) is proposed to make naive Jackson clients somewhat more robust.

TODO: maybe there needs to be a way to specify "client conformance level" in HTTP request header as negotiation?

## Support for PropertyValue pairs

At Bippo e-commerce provider, in the real world [additionalProperty/PropertyValue](https://www.w3.org/wiki/WebSchemas/PropertyValuePairs) will be very helpful. We're already working to integrate it in http://soluvas.github.io/commerceplug/ as integral part of schema:Product .

While technically these should be part of imported ontology(es), store owners aren't ontology designers! And in order to ensure API interoperability among e-commerce providers and to support naive clients (i.e. non-JSON-LD conformant clients e.g. jQuery scripts) PropertyValue is a simple alternative that is practical to use.

## Java Domain Classes

All `Impl` classes are `Serializable` and annotated with Jackson annotations.

## Contact Me

[hendy@soluvas.com](mailto:hendy@soluvas.com)
