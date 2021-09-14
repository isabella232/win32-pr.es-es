---
description: TAPI versión 3.1 es una API basada en COM que combina telefonía IP y clásica. Las aplicaciones posibles van desde llamadas de voz simples a través de la red telefónica conmutada pública (RTC) hasta conferencias IP multimedia multidifusión con calidad de servicio (QOS).
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: Información general de TAPI 3.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30b70ccdc1c4a0985107d2bd2fc36bfbe4e3fca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068704"
---
# <a name="tapi-31-overview"></a>Información general de TAPI 3.1

TAPI versión 3.1 es una API basada en COM que combina telefonía IP y clásica. Las aplicaciones posibles van desde llamadas de voz simples a través de la red telefónica conmutada pública (RTC) hasta conferencias IP multimedia multidifusión con calidad de servicio (QOS).

Para obtener información adicional sobre las funcionalidades de telefonía IP de TAPI 3.1, consulte las white paper "IP Telephony with TAPI 3" (Telefonía IP con TAPI 3), que se pueden encontrar en el sitio web de Microsoft.

Hay cuatro componentes principales de TAPI 3.1:

-   COM API
-   Servidor TAPI
-   Proveedores de servicios de telefonía (TSP)
-   Proveedores de secuencias multimedia (MSP)

En el diagrama siguiente se muestra la arquitectura tapi 3.1:

![Arquitectura de tapi 3](images/callarc-gif-1.png)

La API se implementa como un conjunto de objetos del Modelo de objetos componentes (COM). Mover TAPI al modelo COM orientado a objetos permite a los desarrolladores escribir aplicaciones habilitadas para TAPI en muchos lenguajes, como Java, Visual Basic o C/C++. El uso de COM habilita las actualizaciones de componentes de las características de TAPI.

El proceso del servidor TAPI (TAPISRV) abstrae la interfaz del proveedor de servicios TAPI (TSPI) de TAPI 3.x y TAPI 2.x, lo que permite que los proveedores de servicios de telefonía tapi 2.x se usen con TAPI 3.x, manteniendo el estado interno de TAPI. TAPISRV se implementa como un proceso de servicio dentro de SVCHOST.

[Proveedores de servicios](./tapi-service-providers.md) abstrae los mecanismos de transporte multimedia específicos del proveedor. Normalmente existen en pares: un proveedor de servicios de telefonía (TSP) para el control de llamadas y un proveedor de servicios multimedia (MSP) para el control de medios.

[Los proveedores de servicios de](./telephony-service-providers-start-page.md) telefonía (TSP) son responsables de resolver el modelo de llamada independiente del protocolo de TAPI en mecanismos de control de llamadas específicos del protocolo. TAPI 3.1 proporciona compatibilidad con versiones anteriores con TSP de TAPI 2.1. Dos proveedores de servicios de telefonía IP (y sus MSP asociados) se envían de forma predeterminada con TAPI 3.1: el TSP H.323 y el TSP de conferencia de multidifusión IP.

[Los](media-service-providers-start-page.md) proveedores de servicios multimedia<sup>(MSP)</sup> proporcionan una manera uniforme de acceder a las secuencias multimedia en una llamada, que admite la API de TM de DirectShow como controlador de flujo multimedia principal. Los MSP de TAPI DirectShow interfaces para un TSP determinado y son necesarios para cualquier servicio de telefonía que use DirectShow streaming. La aplicación controla los flujos genéricos.

 

 
