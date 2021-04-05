---
description: El sistema operativo Windows 7 proporciona compatibilidad integrada para dispositivos de sensor.
ms.assetid: 751ba2fc-fbff-4418-82ac-eebc8a145b14
title: Información general sobre el sensor de Windows y la plataforma de ubicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01b6d3132ad6e1bc299895bc39668edbe19b91c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001038"
---
# <a name="overview-of-the-windows-sensor-and-location-platform"></a>Información general sobre el sensor de Windows y la plataforma de ubicación

El sistema operativo Windows 7 proporciona compatibilidad integrada para dispositivos de sensor. Esto incluye compatibilidad con sensores de ubicación, como dispositivos GPS. Como parte de esta compatibilidad, el sensor de Windows y la plataforma de ubicación proporcionan un método estándar para que los fabricantes de dispositivos expongan dispositivos de sensor a los desarrolladores y consumidores de software. Al mismo tiempo, la plataforma ofrece a los desarrolladores una interfaz de controlador de dispositivo y API estandarizada (DDI) para trabajar con sensores y datos de sensor.

## <a name="about-sensor-devices"></a>Acerca de los dispositivos de sensor

Los sensores se incluyen en muchas configuraciones y, desde una perspectiva determinada, casi todo lo que proporciona datos sobre los fenómenos físicos puede denominarse sensor. Aunque normalmente consideramos que los sensores son dispositivos de hardware, los sensores lógicos también pueden proporcionar información a través de la emulación de la funcionalidad del sensor en software o firmware. Además, un único dispositivo de hardware puede contener varios sensores.

El sensor de Windows y la plataforma de ubicación organizan los sensores en *categorías*, que representan amplias clases de dispositivos de sensor y *tipos* que representan tipos específicos de sensores. Por ejemplo, un sensor de un dispositivo de juego de vídeo que detecta la posición y el movimiento de una mano de un jugador (quizás para un juego de bolos de vídeo) se clasificaría como un sensor de orientación, pero su tipo sería un acelerómetro 3D. En el código, Windows representa categorías y tipos usando identificadores únicos globales (GUID), muchos de los cuales están predefinidos. Los fabricantes de dispositivos pueden crear categorías y tipos nuevos definiendo y publicando nuevos GUID, cuando sea necesario.

Los dispositivos de ubicación constituyen una categoría especialmente interesante. En este momento, la mayoría de los usuarios están familiarizados con los sistemas de posicionamiento global (GPS). En Windows, un sensor GPS forma parte de la categoría ubicación. La categoría ubicación podría incluir otros tipos de sensor. Algunos de estos tipos de sensor están basados en software, como un solucionador IP que proporciona información de ubicación basada en una dirección de Internet, un triangular de torre de teléfono móvil que determina la ubicación basada en las torres cercanas o un Wi-Fi proveedor de ubicación de red que lee la información de ubicación del concentrador de red inalámbrica conectado.

## <a name="about-the-platform"></a>Acerca de la plataforma

El sensor de Windows y la plataforma de ubicación se compone de los siguientes componentes de desarrollador y usuario:

-   DDI permite que Windows proporcione una manera estándar para que los dispositivos de sensor se conecten al equipo y proporcionen datos a otros subsistemas.
-   La API del sensor de Windows proporciona un conjunto de métodos, propiedades y eventos para trabajar con sensores conectados y datos del sensor.
-   La API de ubicación de Windows, que se basa en la API del sensor de Windows, proporciona un conjunto de objetos de programación, incluidos los objetos de scripting, para trabajar con la información de ubicación.
-   Los paneles de control ubicación y otros sensores permiten a los administradores del equipo establecer sensores, incluidos los sensores de ubicación, de cada usuario.

En las secciones siguientes se describe cada uno de estos componentes.

## <a name="architecture-diagram"></a>Diagrama de la arquitectura

En el diagrama siguiente se muestra la relación entre los componentes de.

![diagrama de la plataforma de sensor y ubicación](images/platformarchitecture.png)

## <a name="device-driver-interface"></a>Interfaz de controlador de dispositivo

Los fabricantes de sensores pueden crear controladores de dispositivos para conectar sensores con Windows 7. Los controladores de dispositivos de sensor se implementan mediante el modelo de controladores de dispositivos portátiles de Windows (WPD), que se basa en el marco de trabajo de controladores de modo de usuario de Windows (UMDF). Muchos controladores de dispositivos se han escrito mediante estos marcos de trabajo. Dado que estas tecnologías están establecidas, los programadores de controladores de dispositivos experimentados encontrarán la escritura de un controlador de sensor para que sea una tarea familiar. La DDI del sensor usa interfaces y tipos de datos UMDF y WPD específicos, y también define comandos y parámetros de WPD específicos del sensor, donde es necesario. Para obtener más información acerca de la creación de controladores de dispositivos de sensor, consulte el kit de controladores de Windows.

## <a name="sensor-api"></a>API de sensor

La API de sensor permite a los desarrolladores de C++ crear programas basados en sensores mediante un conjunto de interfaces COM. La API define interfaces para realizar tareas comunes de programación de sensores que incluyen la administración de sensores por categoría, tipo o identificador, administración de eventos del sensor, trabajo con sensores individuales y recopilaciones de sensores, y trabajo con datos de sensor. El Windows SDK incluye archivos de encabezado, documentación, ejemplos y herramientas para ayudar a los programadores de software a utilizar sensores en programas de Windows. En esta documentación se describe la API del sensor.

## <a name="location-api"></a>API de ubicación

Basado en la API de sensor, la API de ubicación proporciona una manera sencilla de recuperar datos sobre la ubicación geográfica a la vez que protege la privacidad de los usuarios. La API de ubicación proporciona su funcionalidad a través de un conjunto de interfaces COM que representan objetos. Estos objetos los pueden usar los programadores que saben cómo usar COM a través del lenguaje de programación C++ o en lenguajes de scripting, como JScript. La compatibilidad con scripting proporciona un acceso fácil a los datos de ubicación de los proyectos que se ejecutan en la zona del equipo local, como los gadgets. El Windows SDK incluye archivos de encabezado, documentación (incluida la documentación de referencia de scripting), ejemplos y herramientas para ayudar a los desarrolladores de software y Web a guiarle a usar la información de ubicación en sus programas.

## <a name="location-and-other-sensors-control-panel"></a>Panel de control ubicación y otros sensores

Windows 7 incluye un panel de control que permite a los administradores del equipo habilitar o deshabilitar sensores en todo el sistema o para cada usuario. Dado que algunos sensores pueden exponer datos confidenciales, esta interfaz de usuario ofrece a los administradores el control sobre si todos los programas tienen acceso a cada sensor para cada usuario. Los usuarios también pueden ver las propiedades del sensor y cambiar la descripción del sensor que se muestra en la interfaz de usuario.

El panel de control también proporciona una página de ubicación predeterminada para permitir que los usuarios proporcionen su ubicación. Cuando no hay ningún sensor disponible, la plataforma usará la ubicación proporcionada por el usuario. Los usuarios pueden proporcionar campos de dirección cívica, que incluyen la dirección, la ciudad, el estado o la provincia y el país o la región.

## <a name="related-topics"></a>Temas relacionados

[Acerca de la API de sensor](about-the-sensor-api.md)

[Sitio web central de desarrolladores de hardware de Windows](https://www.microsoft.com/whdc/device/sensors/default.mspx)

[Centro para desarrolladores de Windows](https://msdn.microsoft.com/windows/default.aspx?wt.svl=client)
