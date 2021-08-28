---
description: API de ubicación
ms.assetid: 0182461a-df06-46ea-a9c2-7aedbde5033b
title: API de ubicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19850dc1f85b227f2a5c9e03d9e0130b70c42d38e7ca0bee6308f9963042c613
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693115"
---
# <a name="location-api"></a>API de ubicación

\[La API de ubicación de Win32 y está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [**el Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API. Para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). \]

## <a name="purpose"></a>Propósito

Los equipos de hoy en día son más móviles que nunca. Desde portátiles pequeños hasta tabletas, muchos equipos pueden ir a cualquier lugar al que el usuario quiera ir. Los programas que aprovechan la movilidad del equipo pueden agregar un valor significativo a la vida de las personas. Por ejemplo, un programa que puede encontrar restaurantes cercanos y proporcionar instrucciones de conducción parecería ser una opción natural para un equipo portátil. Pero aunque la tecnología para determinar la ubicación actual del usuario es común y asequible, la creación de soluciones en esta tecnología puede ser una tarea desalentador.

Para crear un programa que tenga en cuenta la ubicación, es posible que tenga que superar una serie de problemas, entre los que se incluyen:

-   Dispositivos del sistema de posicionamiento global (GPS) que usan puertos COM virtuales, que proporcionan acceso solo a un programa a la vez.
-   Descripción y programación de protocolos, como la especificación de National Electronics Association (NMEA), así como extensiones de proveedor propietario.
-   Se limita a la programación de soluciones de hardware verticales conocidas.
-   Implementación de lógica para controlar las transiciones entre varios proveedores de ubicación, como receptores GPS, redes conectadas, redes de telefonía móvil, Internet y configuración de usuario.

En esta documentación se describe Windows interfaz de programación de aplicaciones (API) de Windows Location. Location API ayuda a simplificar la programación con respecto a la ubicación al proporcionar una manera estándar de recuperar datos sobre la ubicación del usuario y estandarizar los formatos de los informes de datos de ubicación. Location API controla automáticamente las transiciones entre los proveedores de datos de ubicación y siempre elige el proveedor más preciso para la situación actual.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Location API proporciona su funcionalidad a través de un conjunto de interfaces COM. Los programadores que están familiarizados con el uso de COM a través del lenguaje de programación C++, o con el uso de objetos COM en lenguajes de scripting, como Microsoft JScript.

## <a name="in-this-section"></a>En esta sección

-   [Referencia de programación de C++ de la API de ubicación](windows-location-programming-reference.md)
-   [Referencia del modelo de objetos de la API de ubicación](windows-location-script-programming-reference.md)

 

 
