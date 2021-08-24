---
title: Uso del proceso de asignación de color con WCS
description: La asignación de colores de WCS se basa en perfiles de dispositivo.
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- Windows Sistema de colores (WCS), asignación de colores
- WCS (Windows de color), asignación de colores
- administración de colores de imagen, asignación de colores
- administración de colores, asignación de colores
- colors,color mapping
- asignación de colores
- Windows Sistema de colores (WCS), perfiles de dispositivo
- WCS (Windows color), perfiles de dispositivo
- administración del color de imagen, perfiles de dispositivo
- administración de colores, perfiles de dispositivo
- colors,device profiles
- Windows Sistema de colores (WCS),perfiles
- WCS (Windows Color System),profiles
- administración de colores de imagen, perfiles
- administración de colores, perfiles
- colors,profiles
- perfiles de dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe785af9fa4160c2aa1e54c6765857edc9c7aacb1a8fa40a0ad04e634b4ab602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934265"
---
# <a name="using-the-color-mapping-process-with-wcs"></a>Uso del proceso de asignación de color con WCS

La asignación de colores de WCS se basa en [perfiles de dispositivo.](d.md) Estos son proporcionados por proveedores de dispositivos de hardware de color y se instalan cuando se instala un dispositivo. Cuando un programa de aplicación usa la asignación de colores, WCS accede al perfil de dispositivo de la imagen para obtener la información necesaria para convertir la imagen en el PCS. La conversión la realiza la CMM.

Un perfil de dispositivo se puede incrustar en la propia imagen. Por lo tanto, el perfil de dispositivo viaja con la imagen, incluso a través de Internet. Un usuario no necesita el dispositivo de origen para obtener una asignación de color precisa. Si una imagen no tiene un perfil de dispositivo, el espacio sRGB se usa como valor predeterminado. Para más información, consulte [Uso de la administración de colores en Internet.](using-color-management-on-the-internet.md)

Tenga en cuenta que las aplicaciones que usan WCS nunca deben insertar el perfil de sRGB en una imagen. El espacio de colores sRGB proporciona un espacio de colores estandarizado que es portátil en todos los dispositivos. Está disponible automáticamente para los usuarios de Windows 98 y versiones posteriores, así como para Windows 2000 y versiones posteriores. Por lo tanto, no es necesario viajar con la imagen.

Una vez que los colores de la imagen están en [el PCS,](p.md)WCS accede al perfil de dispositivo del dispositivo de destino. Obtiene la CMM para convertir los colores de la imagen de PCS a la gama del dispositivo de destino.

También se puede realizar una asignación de colores más compleja con WCS. Por ejemplo, se puede usar para obtener una idea del aspecto que tendría una imagen creada en una pantalla de vídeo cuando se imprime en una impresora de rayos de alta resolución. El ejemplo es más complejo si solo hay una impresora inkjet estándar en la que obtener una vista previa. La imagen se puede convertir de la gama de la pantalla en la gama de la impresora inkjet. Desde allí se puede convertir en la gama de la impresora de rayos. La imagen resultante se puede imprimir en la impresora inkjet. Por supuesto, la imagen tendría una resolución más alta cuando se imprime en la impresora de color de rayos. Sin embargo, los colores de la imagen de prueba impresa en la impresora inkjet coincidirían estrechamente con los colores que imprimiría la impresora de rayos.

La manera en que se logran las conversiones en el ejemplo es convertir los colores de la imagen de la gama de la pantalla en el PCS. Después de convertir los colores de la imagen en el PCS, el perfil de dispositivo de la impresora inkjet se usaría para transformarlos en la gama de la impresora inkjet. A continuación, la gama de transformación PCS se usaría para mover los colores de vuelta al PCS. A partir de ahí, el perfil de dispositivo de la impresora de rayos se usa para convertir los colores de PCS en la gama de la impresora de rayos.

La capacidad de transformar fácilmente los colores de una gama de dispositivos al PCS y volver atrás permite que los colores de imagen diseñados para un dispositivo de salida de color se puedan probar en casi cualquier otro.

En el ejemplo anterior, la descripción varía ligeramente del procedimiento real para mayor claridad. En realidad, todas las transformaciones mencionadas en el párrafo anterior se concatenarán en una sola transformación.

 

 




