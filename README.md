# Perseo Context-Aware CEP

[![FIWARE Processing](https://nexus.lab.fiware.org/static/badges/chapters/processing.svg)](https://www.fiware.org/developers/catalogue/)
[![License: AGPLv3+](https://img.shields.io/badge/License-AGPLv3+-blue.svg)](./LICENSE)
[![Docker Status](https://img.shields.io/docker/pulls/fiware/perseo.svg)](https://hub.docker.com/r/fiware/perseo/)
[![Support badge](https://img.shields.io/badge/tag-fiware--perseo-orange.svg?logo=stackoverflow)](https://stackoverflow.com/questions/tagged/fiware-perseo)
<br> [![Documentation badge](https://img.shields.io/readthedocs/perseo.svg)](https://perseo.readthedocs.io/en/latest/)
[![Build Status](https://travis-ci.org/telefonicaid/perseo-fe.svg?branch=master)](https://travis-ci.org/telefonicaid/perseo-fe)
![Status](https://nexus.lab.fiware.org/static/badges/statuses/perseo.svg)

## Overview

Perseo is a Complex Event Processing (CEP) software designed to be fully _NGSIv2_-compliant. It uses NGSIv2 as the
communication protocol for events, and thus, Perseo is able to seamless and jointly work with _context brokers_ such as
[Orion Context Broker](https://github.com/telefonicaid/fiware-orion).

This project is part of [FIWARE](https://www.fiware.org). You can find more FIWARE components in the
[FIWARE catalogue](https://catalogue.fiware.org).

| :books: [Documentation](https://perseo.readthedocs.io/en/latest) | :whale: [Docker Hub](https://hub.docker.com/r/fiware/perseo/) | :dart: [Roadmap](documentation/roadmap.md) |
| ---------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------ |


## Content

-   [Background](#background)
-   [Installation](#installation)
-   [Usage](#usage)
-   [API](#api)
-   [Testing](#testing)
-   [More Information](#more-information)
-   [License](#license)

## Background

Perseo is an [Esper](http://www.espertech.com/esper/)-based Complex Event Processing (CEP) software supporting the
NGSIv2 protocol.

It follows a straightforward idea: listening to events coming from context information to identify patterns described by
rules, in order to immediately react upon them by triggering actions.

![Perseo Components](docs/images/PerseoComponents.png)

By leveraging on the
[notifications mechanism](http://fiware-orion.readthedocs.io/en/latest/user/walkthrough_apiv2/index.html#subscriptions),
clients instruct Orion CB to notify Perseo of the changes in the entities they care about (`Event API`). Details of this
process are explained in the [Orion Subscription part of the User Manual](user/index.md#orion-subscription). Then, rules
to the CORE Rule Engine can be easily managed using the publicly available
[WireCloud](https://github.com/Wirecloud/wirecloud)) operational dashboard, or making use of any of the REST clients
able to programmaticly use the Perseo's `Rule API`. These rules will identify patterns that will trigger actions with
Orion to create or update entities, or with other different components or external systems, such as Web (HTTP), Email
(SMTP) or SMS (SMPP) servers.

## Installation

The instructions to install Perseo can be found in the [Deployment Guide](docs/admin/deployment.md)

## Usage

Information about how to use Perseo can be found in the [User & Programmers Manual](docs/user/index.md)

## API

APIs and examples of their usage can be found [here](docs/API/api.md)

## Testing

For performing a basic end-to-end test, you can follow the detailed instructions
[here](docs/developer/development.md#Testing).

## More Information

-   Refer to the
    [Esper Reference Documentation](http://esper.espertech.com/release-6.1.0/esper-reference/html/index.html) for info
    on how to use EPL as a rule language.

## License

Perseo FE is licensed under [Affero General Public License (GPL) version 3](./LICENSE).

### Are there any legal issues with AGPL 3.0? Is it safe for me to use?

There is absolutely no problem in using a product licensed under AGPL 3.0. Issues with GPL (or AGPL) licenses are mostly
related with the fact that different people assign different interpretations on the meaning of the term “derivate work”
used in these licenses. Due to this, some people believe that there is a risk in just _using_ software under GPL or AGPL
licenses (even without _modifying_ it).

For the avoidance of doubt, the owners of this software licensed under an AGPL 3.0 license  
wish to make a clarifying public statement as follows:

> Please note that software derived as a result of modifying the source code of this software in order to fix a bug or
> incorporate enhancements is considered a derivative work of the product. Software that merely uses or aggregates (i.e.
> links to) an otherwise unmodified version of existing software is not considered a derivative work, and therefore it
> does not need to be released as under the same license, or even released as open source.
