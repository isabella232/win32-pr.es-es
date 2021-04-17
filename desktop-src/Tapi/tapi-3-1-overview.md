---
description: La versión 3,1 de TAPI es una API basada en COM que combina la telefonía clásica y la IP. Las aplicaciones posibles van desde llamadas de voz simples a través de la red telefónica conmutada (RTC) pública a conferencias de IP Multimedia multidifusión con calidad de servicio (QOS).
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: Información general de TAPI 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30b70ccdc1c4a0985107d2bd2fc36bfbe4e3fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687489"
---
# <a name="tapi-31-overview"></a>Información general de TAPI 3,1

La versión 3,1 de TAPI es una API basada en COM que combina la telefonía clásica y la IP. Las aplicaciones posibles van desde llamadas de voz simples a través de la red telefónica conmutada (RTC) pública a conferencias de IP Multimedia multidifusión con calidad de servicio (QOS).

Para obtener más información acerca de las capacidades de telefonía IP de TAPI 3,1, consulte las notas del producto "telefonía IP con TAPI 3", que encontrará en el sitio web de Microsoft.

Hay cuatro componentes principales de TAPI 3,1:

-   API DE COM
-   Servidor TAPI
-   Proveedores de servicios de telefonía (profesionales)
-   Proveedores de flujo de medios (MSP)

En el siguiente diagrama se ilustra la arquitectura de TAPI 3,1:

![arquitectura de TAPI 3](images/callarc-gif-1.png)

La API se implementa como un conjunto de objetos del modelo de objetos componentes (COM). Mover TAPI al modelo COM orientado a objetos permite a los desarrolladores escribir aplicaciones habilitadas para TAPI en muchos lenguajes, como Java, Visual Basic o C/C++. El uso de COM permite actualizar componentes de las características de TAPI.

El proceso de servidor TAPI (TAPISRV) abstrae la interfaz del proveedor de servicios TAPI (TSPI) de TAPI 3. x y TAPI 2. x, lo que permite usar los proveedores de servicios de telefonía TAPI 2. x con TAPI 3. x, manteniendo el estado interno de TAPI. TAPISRV se implementa como un proceso de servicio en SVCHOST.

Los [proveedores de servicios](./tapi-service-providers.md) comportan mecanismos de transporte multimedia específicos del proveedor. Normalmente existen en pares: un proveedor de servicios de telefonía (TSP) para el control de llamadas y un proveedor de servicios multimedia (MSP) para el control multimedia.

Los [proveedores de servicios de telefonía](./telephony-service-providers-start-page.md) (profesionales) son responsables de resolver el modelo de llamadas independiente del Protocolo de TAPI en mecanismos de control de llamadas específicos del protocolo. TAPI 3,1 proporciona compatibilidad con versiones anteriores de TAPI 2,1 profesionales. Dos proveedores de servicios de telefonía IP (y sus MSP asociados) se distribuyen de forma predeterminada con TAPI 3,1: el TSP H. 323 y el TSP de conferencias de multidifusión IP.

Los [proveedores de servicios multimedia](media-service-providers-start-page.md) (MSP) proporcionan una forma uniforme de acceder a los flujos multimedia en una llamada, lo que admite la API de DirectShow<sup>TM</sup> como controlador de flujo de medios principal. Los MSP de TAPI implementan interfaces de DirectShow para un TSP determinado y son necesarios para cualquier servicio de telefonía que haga uso de la transmisión por secuencias de DirectShow. La aplicación controla las secuencias genéricas.

 

 
