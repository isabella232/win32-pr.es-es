---
description: El propósito de esta guía es ayudar a los usuarios a solucionar los errores detectados al usar las API de detección de WSDAPI, al crear un host de WSDAPI o un proxy de dispositivo, o al usar funciones del sistema operativo (como la detección de funciones o el explorador de red) que se basan en WSDAPI.
ms.assetid: fc01fc66-627a-497f-98dd-613f5d85f6cb
title: Guía de solución de problemas de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c28e9a1fe4cc5b24b386cfb88e39276edc14cb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648273"
---
# <a name="wsdapi-troubleshooting-guide"></a>Guía de solución de problemas de WSDAPI

El propósito de esta guía es ayudar a los usuarios a solucionar los errores detectados al usar las API de detección de WSDAPI, al crear un host de WSDAPI o un proxy de dispositivo, o al usar funciones del sistema operativo (como la [detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal) o el explorador de red) que se basan en WSDAPI. El objetivo principal es ayudarle a solucionar problemas cuando un cliente y un host no se puedan ver entre sí en la red.

En el caso de los usuarios de WSDAPI, esta guía contiene información que le ayudará a solucionar correctamente un proxy de dispositivo (mediante [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)), un proveedor de detección (con [**WSDCreateDiscoveryProvider**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoveryprovider)) o un publicador de detección (mediante [**WSDCreateDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoverypublisher)).

En esta guía se da por supuesto que el cliente y el host pueden interoperar correctamente con WSDAPI en un entorno controlado. En consecuencia, esta guía no está pensada para ayudar a solucionar problemas de pilas de DPWS que pueden generar mensajes de WS incorrectos. Para obtener información sobre cómo probar la interoperabilidad con WSDAPI, vea la [herramienta de interoperabilidad básica de WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) en el kit de controladores de Windows (WDK).

Antes de empezar a solucionar problemas de la aplicación, debe familiarizarse con los [patrones de mensajes de intercambio de metadatos y de detección](discovery-and-metadata-exchange-message-patterns.md).

En esta guía se incluyen las siguientes secciones.

-   [Introducción con la solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
-   [Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
