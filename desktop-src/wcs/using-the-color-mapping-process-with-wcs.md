---
title: Uso del proceso de asignación de color con WCS
description: La asignación de colores WCS se basa en los perfiles de dispositivo.
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- Sistema de color de Windows (WCS), asignación de colores
- WCS (sistema de colores de Windows), asignación de colores
- Administración del color de imagen, asignación de colores
- Administración del color, asignación de colores
- colores, asignación de colores
- asignación de colores
- Sistema de color de Windows (WCS), perfiles de dispositivo
- WCS (sistema de colores de Windows), perfiles de dispositivo
- Administración del color de imagen, perfiles de dispositivo
- Administración del color, perfiles de dispositivo
- colores, perfiles de dispositivo
- Sistema de color de Windows (WCS), perfiles
- WCS (sistema de colores de Windows), perfiles
- Administración del color de imagen, perfiles
- Administración del color, perfiles
- colores, perfiles
- perfiles de dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 428b09749f3781def44e56ff6cea0539259d0464
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105721117"
---
# <a name="using-the-color-mapping-process-with-wcs"></a>Uso del proceso de asignación de color con WCS

La asignación de colores WCS se basa en los [perfiles de dispositivo](d.md). Los proporcionan los proveedores de dispositivos de hardware de color y se instalan cuando se instala un dispositivo. Cuando un programa de aplicación utiliza la asignación de colores, WCS accede al perfil de dispositivo de la imagen para obtener la información necesaria para convertir la imagen en los equipos. La conversión se realiza mediante la CMM.

Un perfil de dispositivo se puede incrustar en la propia imagen. Por lo tanto, el perfil del dispositivo viaja con la imagen, incluso a través de Internet. Un usuario no necesita el dispositivo de origen para obtener una asignación de color precisa. Si una imagen no tiene un perfil de dispositivo, el espacio sRGB se utiliza como valor predeterminado. Para obtener más información, consulte [uso de la administración del color en Internet](using-color-management-on-the-internet.md).

Tenga en cuenta que las aplicaciones que usan WCS nunca deben insertar el perfil sRGB en una imagen. El espacio de colores sRGB proporciona un espacio de colores estandarizado en todos los dispositivos. Está disponible automáticamente para los usuarios de Windows 98 y versiones posteriores, así como para Windows 2000 y versiones posteriores. Por lo tanto, no es necesario viajar con la imagen.

Una vez que los colores de la imagen están en los [equipos](p.md), WCS accede al perfil de dispositivo del dispositivo de destino. Obtiene la CMM para convertir los colores de la imagen de los equipos a la gama del dispositivo de destino.

También se puede realizar una asignación de colores más compleja con WCS. Por ejemplo, se puede usar para hacerse una idea del aspecto que tendrá una imagen creada en una pantalla de vídeo cuando se imprima en una impresora láser de alta resolución. El ejemplo se obtiene más complejo si solo hay una impresora de inyección de tinta estándar en la que se va a obtener una vista previa. La imagen se puede convertir desde la gama de la pantalla hasta la gama de la impresora de inyección de tinta. Desde allí, se puede convertir en la gama de la impresora láser. La imagen resultante se puede imprimir en la impresora de inyección de tinta. Por supuesto, la imagen tendría una resolución más alta cuando se imprimiera en la impresora láser de color. Sin embargo, los colores de la imagen de prueba que se imprimen en la impresora de inyección de tinta serían una coincidencia aproximada con los colores que imprimiría la impresora láser.

La forma en que se realizan las conversiones en el ejemplo consiste en convertir los colores de la imagen de la gama de la pantalla en los equipos. Una vez convertidos los colores de la imagen en los equipos, el perfil de dispositivo de la impresora de inyección de tinta se utilizaría para transformarlos en la gama de la impresora de inyección de tinta. A continuación, se utilizaría la transformación gama a PCS para devolver los colores a los equipos. A partir de ahí, el perfil de dispositivo de la impresora láser se usa para convertir los colores de los equipos a la gama de la impresora láser.

La capacidad de transformar fácilmente los colores de una gama de dispositivos en los equipos y viceversa permite que los colores de imagen que se destinan a un dispositivo de salida de color se prueben en casi cualquier otro.

En el ejemplo anterior, la descripción varía del procedimiento real en cierto modo para mayor claridad. En realidad, todas las transformaciones mencionadas en el párrafo anterior se concatenarían en una única transformación.

 

 




