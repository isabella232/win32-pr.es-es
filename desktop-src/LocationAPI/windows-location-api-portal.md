---
description: .
ms.assetid: 0182461a-df06-46ea-a9c2-7aedbde5033b
title: API de ubicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f643565e80f72ffcefe6981c924b3739b1c4f5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909490"
---
# <a name="location-api"></a>API de ubicación

\[La API de ubicación de Win32 y está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) . Para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). \]

## <a name="purpose"></a>Propósito

Hoy en día, los equipos son más móviles que nunca. Desde pequeños portátiles hasta Tablet PC, muchos equipos pueden ir dondequiera que el usuario desee ir. Los programas que aprovechan la movilidad del equipo pueden agregar un valor significativo a la vida de las personas. Por ejemplo, un programa que puede buscar restaurantes cercanos y proporcionar instrucciones de conducción parece ser un ajuste natural para un equipo portátil. Pero aunque la tecnología para determinar la ubicación actual del usuario es habitual y asequible, la creación de soluciones en esta tecnología puede ser una tarea desalentadora.

Para crear un programa con reconocimiento de ubicación, es posible que tenga que solucionar una serie de problemas, entre los que se incluyen:

-   Dispositivos del sistema de posicionamiento global (GPS) que usan puertos COM virtuales, que proporcionan acceso solo a un programa a la vez.
-   Comprensión y programación de protocolos, como la especificación National Marine Electronics Association (NMEA), así como las extensiones de proveedor de propiedad.
-   Se limita a la programación de soluciones de hardware conocidas y verticales.
-   Implementación de lógica para controlar las transiciones entre varios proveedores de ubicación, como receptores de GPS, redes conectadas, redes de telefonía móvil, Internet y configuración de usuario.

En esta documentación se describe la interfaz de programación de aplicaciones (API) de ubicación de Windows. La API de ubicación ayuda a simplificar la programación compatible con la ubicación, ya que proporciona una manera estándar de recuperar datos sobre la ubicación del usuario y estandarizar formatos para los informes de datos de ubicación. La API de ubicación controla automáticamente las transiciones entre los proveedores de datos de ubicación y siempre elige el proveedor más preciso para la situación actual.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de ubicación proporciona su funcionalidad a través de un conjunto de interfaces COM. La funcionalidad de la API de ubicación la pueden usar los programadores que están familiarizados con el uso de COM mediante el lenguaje de programación C++ o con objetos COM en lenguajes de scripting, como Microsoft JScript.

## <a name="in-this-section"></a>En esta sección

-   [Referencia de programación de C++ de API de ubicación](windows-location-programming-reference.md)
-   [Referencia del modelo de objetos de API de ubicación](windows-location-script-programming-reference.md)

 

 
