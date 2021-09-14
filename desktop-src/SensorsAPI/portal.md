---
description: API de sensor
ms.assetid: a6ea76e6-9721-453a-a657-96f53660e09d
title: API de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a36259910fb7583c91b695f69066aa2abf9be1e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068960"
---
# <a name="sensor-api"></a>API de sensor

## <a name="purpose"></a>Propósito

Windows 7 incluye compatibilidad nativa con sensores, que son dispositivos que pueden medir los fenómenos físicos, como la temperatura o la ubicación. En esta documentación se describe Sensor API, que permite a las aplicaciones obtener y usar datos de sensores de una manera estandarizada.

Como seres humanos, nos basamos en nuestros sentidos para proporcionarnos información sobre el mundo que nos rodea. Cuando creamos máquinas para asumir parte de nuestro trabajo, agregamos mecanismos de sensor para que las máquinas puedan responder adecuadamente a las condiciones cambiantes.

Por ejemplo, los motores de automóviles suelen usar una variedad de sensores. Estos sensores se supervisan mediante un equipo integrado que ajusta continuamente la configuración, como el tiempo del motor, para maximizar la potencia y la eficacia. Una televisión puede usar un sensor de luz ambiente para ajustar el brillo de la imagen para que coincida con las condiciones de la sala de cambios. Incluso algo tan sencillo como un botón de timbre actúa como un sensor rudimentario para detectar una presencia humana en la puerta.

Aunque la puerta puramente mecánica cumple su propósito, la información proporcionada por sensores complejos es mucho más eficaz cuando se combina con software. Los sensores modernos pueden proporcionar una gran cantidad de datos muy rápidamente y en una variedad de formatos, por lo que el software proporciona un mecanismo natural para dar sentido a los datos del sensor.

En la actualidad, los desarrolladores de software pueden escribir programas que usan sensores, pero la falta de normalización hace que la programación de sensores sea una tarea inecontente. Una vez completado un programa basado en sensores, normalmente depende para siempre de un tipo determinado de hardware. El uso de una o varias soluciones verticales para habilitar la implementación de un sistema basado en software ha limitado la integración de sensores con hardware de equipo y, hasta ahora, los equipos basados en Windows no han sido una excepción.

Windows 7 incluye compatibilidad nativa con sensores, expandido por una nueva plataforma de desarrollo para trabajar con sensores, incluidos los sensores de ubicación, como los dispositivos GPS. La plataforma de sensor y ubicación de Windows proporciona una manera estándar para que los fabricantes de dispositivos exponán los dispositivos sensores a los desarrolladores y consumidores de software, al tiempo que proporciona a los desarrolladores una interfaz de programación de aplicaciones (API) estandarizada para trabajar con sensores y datos de sensores.

Los sensores son dispositivos o mecanismos que pueden medir los fenómenos físicos, proporcionar datos descriptivos o proporcionar información sobre el estado de un objeto físico o entorno. Los equipos pueden usar sensores integrados, sensores conectados a través de conexiones cableadas o inalámbricas, o sensores que proporcionan datos a través de una red o Internet.

Sensor API proporciona una manera estándar de acceder mediante programación a los datos que proporcionan los sensores. Sensor API estandariza:

-   Categorías, tipos y propiedades del sensor.
-   Formatos de datos para tipos de sensor estándar.
-   Interfaces COM para trabajar con sensores y colecciones de sensores.
-   Mecanismos de eventos para recibir datos del sensor de forma asincrónica.

Sensor API también permite definir categorías de sensores, tipos, propiedades, formatos de datos y eventos personalizados.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Sensor API proporciona su funcionalidad a través de un conjunto de interfaces COM. En esta documentación se supone que tiene conocimientos prácticos de programación mediante el lenguaje de programación C++, y que tiene una comprensión básica de cómo usar objetos COM e interfaces. Para mayor brevedad, muchos ejemplos de código de esta documentación (así como en los ejemplos de código) usan objetos Active Template Library (ATL) para implementar la funcionalidad COM.

## <a name="in-this-section"></a>En esta sección

-   [Introducción](getting-started.md)
-   [Acerca de Sensor API](about-the-sensor-api.md)
-   [Guía de programación de Sensor API](sensor-api-programming-guide.md)
-   [Referencia de programación de Sensor API](sensor-api-programming-reference.md)

 

 



