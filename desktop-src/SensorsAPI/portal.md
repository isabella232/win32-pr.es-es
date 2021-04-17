---
description: .
ms.assetid: a6ea76e6-9721-453a-a657-96f53660e09d
title: API de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c4d6fd7805607afa80fcee27568004906a0a8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666371"
---
# <a name="sensor-api"></a>API de sensor

## <a name="purpose"></a>Propósito

Windows 7 incluye compatibilidad nativa con sensores, que son dispositivos que pueden medir fenómenos físicos, como la temperatura o la ubicación. En esta documentación se describe la API del sensor, que permite a las aplicaciones obtener y usar los datos de los sensores de una manera estandarizada.

Como humanos, confiamos en nuestros sentidos para proporcionarnos información sobre todo el mundo. Cuando creamos máquinas para realizar parte de nuestro trabajo, se agregan mecanismos de sensor para que las máquinas puedan responder adecuadamente a las condiciones cambiantes.

Por ejemplo, los motores automóviles suelen usar diversos sensores. Estos sensores se supervisan mediante un equipo incorporado que ajusta continuamente la configuración, como la temporización del motor, para maximizar la eficacia y la eficiencia. Un televisor puede usar un sensor de luz ambiente para ajustar el brillo de la imagen para que coincida con las condiciones de la habitación cambiante. Incluso algo tan sencillo como un botón de doorbell actúa como un sensor rudimentario para detectar una presencia humana en la puerta.

Aunque el doorbell puramente mecánico cumple su finalidad, la información proporcionada por sensores complejos es mucho más eficaz cuando se combina con el software. Los sensores modernos pueden proporcionar una gran cantidad de datos de forma muy rápida y en una gran variedad de formatos, por lo que el software proporciona un mecanismo natural para tener sentido en los datos de los sensores.

En la actualidad, los desarrolladores de software pueden escribir programas que usan sensores, pero una falta de normalización hace que la programación de los sensores sea una tarea ardua. Una vez completado un programa basado en sensores, normalmente depende de un determinado tipo de hardware. El uso de una o varias soluciones verticales para habilitar la implementación de un sistema basado en software ha limitado la integración de sensores con el hardware del equipo y, hasta ahora, los equipos basados en Windows no han producido ninguna excepción.

Windows 7 incluye compatibilidad nativa con sensores, ampliada por una nueva plataforma de desarrollo para trabajar con sensores, incluidos sensores de ubicación, como dispositivos GPS. El sensor de Windows y la plataforma de ubicación proporcionan un método estándar para que los fabricantes de dispositivos expongan dispositivos de sensor a los desarrolladores y consumidores de software, a la vez que proporcionan a los desarrolladores una interfaz de programación de aplicaciones (API) normalizada para trabajar con sensores y datos de sensores.

Los sensores son dispositivos o mecanismos que pueden medir fenómenos físicos, proporcionar datos descriptivos o proporcionar información sobre el estado de un objeto o entorno físico. Los equipos pueden usar sensores integrados, sensores que se conectan a través de conexiones cableadas o inalámbricas, o sensores que proporcionan datos a través de una red o Internet.

La API de sensor proporciona un método estándar para acceder mediante programación a los datos proporcionados por los sensores. La API de sensor se normaliza:

-   Categorías, tipos y propiedades de sensor.
-   Formatos de datos para los tipos de sensores estándar.
-   Interfaces COM para trabajar con sensores y recopilaciones de sensores.
-   Mecanismos de eventos para recibir datos de sensor de forma asincrónica.

La API de sensor también le permite definir categorías de sensor, tipos, propiedades, formatos de datos y eventos personalizados.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de sensor proporciona su funcionalidad a través de un conjunto de interfaces COM. En esta documentación se supone que tiene conocimientos prácticos de la programación con el lenguaje de programación de C++ y tiene conocimientos básicos sobre cómo usar interfaces y objetos COM. Por motivos de brevedad, muchos ejemplos de código de esta documentación (así como en los ejemplos de código) utilizan objetos Active Template Library (ATL) para implementar la funcionalidad COM.

## <a name="in-this-section"></a>En esta sección

-   [Introducción](getting-started.md)
-   [Acerca de la API de sensor](about-the-sensor-api.md)
-   [Guía de programación de la API de sensor](sensor-api-programming-guide.md)
-   [Referencia de programación de API de sensor](sensor-api-programming-reference.md)

 

 



