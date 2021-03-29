---
title: Plataforma de sensor
description: Windows 7 ha cambiado la forma en que los desarrolladores usan sensores.
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94fd48ffa16080054a22b4d377ab4757d61d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077989"
---
# <a name="sensor-platform"></a>Plataforma de sensor

Windows 7 ha cambiado la forma en que los desarrolladores usan sensores. Incluye compatibilidad nativa con sensores, ampliada por una nueva plataforma de desarrollo para trabajar con sensores, incluidos sensores de ubicación, como dispositivos de sistemas de posicionamiento global (GPS).

Basado en la plataforma de sensores, las API de *Ubicación de Windows* son una nueva característica de Windows 7 que permite a los desarrolladores de aplicaciones tener acceso a la información de ubicación física del usuario. Las API de *Ubicación de Windows* pueden abstraer el hardware, admitir simultáneamente varias aplicaciones y cambiar sin problemas entre distintas tecnologías, lo que alivia al desarrollador de la aplicación de la carga de administrar estas restricciones. Los programadores pueden usar las API de *Ubicación* a través del lenguaje de programación C++ (los programadores familiarizados con el modelo de objetos componentes (com)) o el uso de objetos com en lenguajes de scripting, como Microsoft JScript. La compatibilidad con scripting proporciona un acceso fácil a los datos de ubicación de proyectos como gadgets.

Windows 7 proporciona una plataforma sólida y fácil de usar para el uso de dispositivos de sensor, como un sensor de luz ambiente o un medidor de temperatura, para crear un reconocimiento medioambiental en aplicaciones Windows. Los equipos pueden usar sensores integrados en el equipo, conectados a través de conexiones cableadas o inalámbricas, o conectados a través de una red o *Internet*.

Las API de *sensor* y *Ubicación* proporcionan una manera estándar de detectar sensores y obtener acceso mediante programación a los datos proporcionados por los sensores.

El panel de control *del sensor* permite a los usuarios habilitar o deshabilitar sensores, controlar el acceso a los sensores que pueden exponer datos confidenciales, ver las propiedades del sensor y cambiar las descripciones de los sensores.

La [extensión de clase de sensor](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) es una parte fundamental del modelo de desarrollo de controladores para la plataforma de sensor. Proporciona los mecanismos siguientes, que se usan al escribir un controlador de sensor del [marco de trabajo de controladores de modo de usuario (UMDF)](https://developer.microsoft.com/windows/hardware) :

-   Integración con la plataforma de sensores
-   Cumplimiento de seguridad

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de sensor](../sensorsapi/portal.md)
</dt> <dt>