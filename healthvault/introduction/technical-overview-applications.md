---
title: Overview | Applications
author: jhutchings1
ms.author: justhu
ms.date: 04/12/2017
ms.topic: article
ms.prod: healthvault
description: Learn about how HealthVault works with 3rd party apps. 
---

Technical overview: applications
================================

Applications
------------

A HealthVault-integrated application is permitted to call the production service APIs in order to read and write health data. The onboarding process is as follows:

-   The developer configures an application entry in the [Application Configuration Center (ACC)](https://config.healthvault-ppe.com).
-   The developer builds and tests the application against the PPE (pre-production) environment (<https://www.healthvault-ppe.com>).
-   The developer initiates the <a href="/healthvault/publishing/go-live" id="Introduction_14442_17">go-live process</a> to move the configuration entry to production.

Development tools
-----------------

HealthVault provides an XML-based web service API.  Interactive technical documentation can be found on this site. However, most applications will use a software development kit (SDK) instead of the native XML API.  HealthVault <a href="/healthvault/index#pivot=sdkstools">supports a variety of SDKs</a> for common platforms such as .NET and Windows 8 RT. An SDK makes it easier to execute scenarios such as uploading large chunks of data.

Go-live process
---------------

The go-live process is series of steps to validate and approve an application. This is necessary because HealthVault applications have access to sensitive information and must be implemented in a manner that protects patients and the integrity of the service.

-   The developer signs a solution provider agreement with the HealthVault business team.
-   The developer completes a walkthrough and profile of the application for review by the HealthVault team.
-   The developer schedules a go-live review during which the application is demonstrated.
-   HealthVault enables the application to call the production service APIs.

Learn more with the <a href="/healthvault/publishing/go-live" id="Introduction_14442_20">go-live guide</a>.

Next, read about <a href="/healthvault/introduction/technical-overview-permissions" id="Introduction_14442_16">application permissions</a>.

<span id="singleColInThreeColLayout"></span>

### Technical Overview

-   <a href="/healthvault/introduction/technical-overview" id="RightRailLinkListSection_14442_10">1. Terminology</a>
-   <a href="/healthvault/introduction/technical-overview-applications" id="RightRailLinkListSection_14442_11">2. Applications</a>
-   <a href="/healthvault/introduction/technical-overview-permissions" id="RightRailLinkListSection_14442_12">3. Permissions</a>
-   <a href="/healthvault/introduction/technical-overview-connectivity" id="RightRailLinkListSection_14442_13">4. Connectivity</a>
-   <a href="/healthvault/introduction/technical-overview-exchanging-data" id="RightRailLinkListSection_14442_14">5. Exchanging data</a>

See also

-   <a href="https://config.healthvault-ppe.com" id="RightRailLinkListSection_14442_9">Application Configuration Center</a>
