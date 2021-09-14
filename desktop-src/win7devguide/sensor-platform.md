---
title: Plataforma del sensor
description: Windows 7 ha cambiado la forma en que los desarrolladores usan sensores.
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94fd48ffa16080054a22b4d377ab4757d61d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267327"
---
# <a name="sensor-platform"></a>Plataforma del sensor

Windows 7 ha cambiado la forma en que los desarrolladores usan sensores. Incluye compatibilidad nativa con sensores, expandido por una nueva plataforma de desarrollo para trabajar con sensores, incluidos los sensores de ubicación, como los dispositivos de sistemas de posicionamiento global (GPS).

Las API de ubicación de *Windows* se basa en la plataforma sensor son una nueva característica de Windows 7 que permite a los desarrolladores de aplicaciones acceder a la información de ubicación física del usuario. Las API Windows *Location* pueden abstraer el hardware, admitir varias aplicaciones simultáneamente y cambiar sin problemas entre distintas tecnologías, lo que ayuda al desarrollador de aplicaciones de la carga de administrar estas restricciones. Los programadores pueden usar las API de ubicación a través del lenguaje de programación C++ (por parte de programadores familiarizados con el Modelo de objetos componentes (COM) o mediante el uso de objetos COM en lenguajes de scripting, como Microsoft JScript. La compatibilidad con scripting proporciona un acceso sencillo a los datos de ubicación para proyectos como los guiones.

Windows 7 proporciona una plataforma sólida y fácil de usar para el uso de dispositivos sensores, como un sensor de luz ambiente o un medidor de temperatura, para crear reconocimiento del entorno en Windows aplicaciones. Los equipos pueden usar sensores integrados en el equipo, conectados a través de conexiones cableadas o inalámbricas, o conectados a través de una red o *Internet.*

Las *API de* sensor *y* ubicación proporcionan una manera estándar de detectar sensores y acceder mediante programación a los datos que proporcionan los sensores.

El *panel de* control Sensor permite a los usuarios habilitar o deshabilitar sensores, controlar el acceso a los sensores que podrían exponer datos confidenciales, ver las propiedades del sensor y cambiar las descripciones de los sensores.

La [extensión de clase sensor](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) es una parte fundamental del modelo de desarrollo de controladores para la plataforma sensor. Proporciona los siguientes mecanismos, que se usan al escribir un controlador de sensor de [User-Mode Driver Framework (UMDF):](https://developer.microsoft.com/windows/hardware)

-   Integración con la plataforma sensor
-   Aplicación de seguridad

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de sensor](../sensorsapi/portal.md)
</dt> <dt>