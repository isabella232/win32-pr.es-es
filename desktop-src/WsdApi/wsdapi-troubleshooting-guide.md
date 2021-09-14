---
description: El propósito de esta guía es ayudar a los usuarios a solucionar los errores detectados al usar las API de detección de WSDAPI, al crear un host de WSDAPI o un proxy de dispositivo, o al usar funciones del sistema operativo (como la detección de funciones o Explorador de red) que se basan en WSDAPI.
ms.assetid: fc01fc66-627a-497f-98dd-613f5d85f6cb
title: Guía de solución de problemas de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c28e9a1fe4cc5b24b386cfb88e39276edc14cb3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974383"
---
# <a name="wsdapi-troubleshooting-guide"></a>Guía de solución de problemas de WSDAPI

El propósito de esta guía es ayudar a los usuarios a solucionar los errores detectados al usar las API de detección de [](/previous-versions/windows/desktop/fundisc/fd-portal) WSDAPI, al crear un host de WSDAPI o un proxy de dispositivo, o al usar funciones del sistema operativo (como la detección de funciones o el Explorador de red) que se basan en WSDAPI. El objetivo principal es ayudar a solucionar problemas cuando un cliente y un host no se pueden ver entre sí en la red.

Para los usuarios de WSDAPI, esta guía contiene información que le ayudará a solucionar problemas de un proxy de dispositivo (mediante [**WSDCreateDeviceProxy),**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)un proveedor de detección (mediante [**WSDCreateDiscoveryProvider)**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoveryprovider)o un publicador de detección (mediante [**WSDCreateDiscoveryPublisher).**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoverypublisher)

En esta guía se da por supuesto que tanto el cliente como el host pueden interoperar correctamente con WSDAPI en un entorno controlado. En consecuencia, esta guía no está pensada para ayudar a solucionar problemas de las pilas de DPWS que pueden estar generando mensajes WS incorrectos. Para obtener información sobre cómo probar la interoperabilidad con WSDAPI, vea [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) en Windows Driver Kit (WDK).

Antes de empezar a solucionar problemas de la aplicación, debe familiarizarse con la detección y los [metadatos Exchange de mensajes](discovery-and-metadata-exchange-message-patterns.md).

En esta guía se incluyen las siguientes secciones.

-   [Tareas iniciales solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
-   [Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
