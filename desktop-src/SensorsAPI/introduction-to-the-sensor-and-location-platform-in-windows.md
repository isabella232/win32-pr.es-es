---
description: El Windows operativo 7 proporciona compatibilidad integrada con dispositivos de sensor.
ms.assetid: 751ba2fc-fbff-4418-82ac-eebc8a145b14
title: Información general de la plataforma Windows sensor y ubicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4847d6d6137b91ce577cfce0dbc54cc8c6e19430e1318eaff145c24ce493af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889739"
---
# <a name="overview-of-the-windows-sensor-and-location-platform"></a>Información general de la plataforma Windows sensor y ubicación

El Windows operativo 7 proporciona compatibilidad integrada con dispositivos de sensor. Esto incluye compatibilidad con sensores de ubicación, como dispositivos GPS. Como parte de esta compatibilidad, la plataforma Windows Sensor and Location proporciona una manera estándar para que los fabricantes de dispositivos exponán los dispositivos de sensor a los desarrolladores y consumidores de software. Al mismo tiempo, la plataforma proporciona a los desarrolladores una API estandarizada y una interfaz de controlador de dispositivo (DDI) para trabajar con sensores y datos de sensor.

## <a name="about-sensor-devices"></a>Acerca de los dispositivos de sensor

Los sensores proceden de muchas configuraciones y, desde una perspectiva determinada, casi todo lo que proporciona datos sobre los fenómenos físicos se puede denominar sensor. Aunque normalmente se considera que los sensores son dispositivos de hardware, los sensores lógicos también pueden proporcionar información a través de la emulación de la funcionalidad del sensor en software o firmware. Además, un único dispositivo de hardware puede contener varios sensores.

La Windows sensor y ubicación organiza los sensores en categorías *,* que representan clases amplias de dispositivos de sensor, y tipos *,* que representan tipos específicos de sensores. Por ejemplo, un sensor en un controlador de juegos de vídeo que detecta la posición y el movimiento de la mano de un jugador (quizás para un juego de vídeo) se clasificaría como sensor de orientación, pero su tipo sería Acelerómetro 3D. En el código, Windows representa categorías y tipos mediante identificadores únicos globales (GUID), muchos de los cuales están predefinidos. Los fabricantes de dispositivos pueden crear nuevas categorías y tipos definiendo y publicando nuevos GUID, cuando sea necesario.

Los dispositivos de ubicación son una categoría especialmente interesante. Por ahora, la mayoría de las personas están familiarizados con los sistemas de posicionamiento global (GPS). En Windows, un sensor GPS forma parte de la categoría Ubicación. La categoría Ubicación podría incluir otros tipos de sensor. Algunos de estos tipos de sensores están basados en software, como una resolución IP que proporciona información de ubicación basada en una dirección de Internet, un triangulator de la torre de teléfono móvil que determina la ubicación en función de las proximidades o un proveedor de ubicación de red Wi-Fi que lee información de ubicación desde el centro de red inalámbrica conectado.

## <a name="about-the-platform"></a>Acerca de la plataforma

La plataforma Windows sensor y ubicación consta de los siguientes componentes de desarrollador y usuario:

-   DDI permite a Windows proporcionar una manera estándar para que los dispositivos de sensor se conecten al equipo y proporcionen datos a otros subsistemas.
-   La WINDOWS Sensor API proporciona un conjunto de métodos, propiedades y eventos para trabajar con sensores conectados y datos de sensor.
-   La API Windows Location, que se basa en Windows Sensor API, proporciona un conjunto de objetos de programación, incluidos objetos de scripting, para trabajar con información de ubicación.
-   El Ubicación y otros sensores Panel de control permite a los administradores de equipos establecer sensores, incluidos los sensores de ubicación, para cada usuario.

En las secciones siguientes se describe cada uno de estos componentes.

## <a name="architecture-diagram"></a>Diagrama de la arquitectura

En el diagrama siguiente se muestra la relación entre los componentes.

![diagrama de la plataforma de sensor y ubicación](images/platformarchitecture.png)

## <a name="device-driver-interface"></a>Interfaz del controlador de dispositivo

Los fabricantes de sensores pueden crear controladores de dispositivos para conectar sensores con Windows 7. Los controladores de dispositivos sensores se implementan mediante el modelo de controlador Windows Portable Devices (WPD), que se basa en Windows User Mode Driver Framework (UMDF). Muchos controladores de dispositivos se han escrito mediante estos marcos. Dado que estas tecnologías están establecidas, los programadores experimentados de controladores de dispositivos encontrarán que escribir un controlador de sensor es una tarea familiar. El sensor DDI usa interfaces y tipos de datos ESPECÍFICOs de UMDF y WPD, y también define comandos y parámetros WPD específicos del sensor, donde es necesario. Para obtener más información sobre cómo crear controladores de dispositivo de sensor, consulte el Windows Driver Kit.

## <a name="sensor-api"></a>API de sensor

Sensor API permite a los desarrolladores de C++ crear programas basados en sensores mediante un conjunto de interfaces COM. La API define interfaces para realizar tareas comunes de programación de sensores que incluyen la administración de sensores por categoría, tipo o identificador, la administración de eventos de sensor, el trabajo con sensores individuales y colecciones de sensores y el trabajo con datos de sensor. El SDK Windows incluye archivos de encabezado, documentación, ejemplos y herramientas para ayudar a los desarrolladores de software a guiar a los desarrolladores de software sobre cómo usar sensores en Windows programas. En esta documentación se describe sensor API.

## <a name="location-api"></a>API de ubicación

La API de ubicación, que se basa en Sensor API, proporciona una manera sencilla de recuperar datos sobre la ubicación geográfica y, al mismo tiempo, proteger la privacidad del usuario. Location API proporciona su funcionalidad a través de un conjunto de interfaces COM que representan objetos. Estos objetos pueden ser usados por programadores que comprenden cómo usar COM a través del lenguaje de programación C++, o en lenguajes de scripting, como JScript. La compatibilidad con scripting proporciona un acceso sencillo a los datos de ubicación de los proyectos que se ejecutan en la zona equipo local, como los artefactos. El SDK Windows incluye archivos de encabezado, documentación (incluida la documentación de referencia de scripting), ejemplos y herramientas para ayudar a guiar a los desarrolladores web y de software sobre cómo usar la información de ubicación en sus programas.

## <a name="location-and-other-sensors-control-panel"></a>Ubicación y otros sensores Panel de control

Windows 7 incluye un panel de control que permite a los administradores de equipos habilitar o deshabilitar sensores en todo el sistema o para cada usuario. Dado que algunos sensores pueden exponer datos confidenciales, esta interfaz de usuario proporciona a los administradores control sobre si todos los programas tienen acceso a cada sensor para cada usuario. Los usuarios también pueden ver las propiedades del sensor y cambiar la descripción del sensor que se muestra en la interfaz de usuario.

El Panel de control también proporciona una página Ubicación predeterminada para permitir que los usuarios proporcionen su ubicación. Cuando no hay ningún sensor disponible, la plataforma usará la ubicación proporcionada por el usuario. Los usuarios pueden proporcionar campos de direcciones cívicos, que incluyen la dirección postal, la ciudad, el estado o la provincia, y el país o región.

## <a name="related-topics"></a>Temas relacionados

[Acerca de Sensor API](about-the-sensor-api.md)

[Sitio web central de desarrolladores de hardware de Windows](https://www.microsoft.com/whdc/device/sensors/default.mspx)

[Centro para desarrolladores de Windows](https://msdn.microsoft.com/windows/default.aspx?wt.svl=client)
