---
title: Super Files
description: Super Files
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Reproductor de Windows Media Máscaras móviles, archivos de arte
- skins,art files
- archivos para máscaras, arte
- archivos art para máscaras,archivos super files
- Reproductor de Windows Media Máscaras móviles, archivos super files
- skins,Super files
- Super files in skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbd6734e0491b5fc0e6552db14b3c0ab4489e466e7851ef4b474e84d2d85183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122874"
---
# <a name="super-files"></a>Super Files

Los archivos super se usan para almacenar las imágenes deshabilitadas para las barras de seguimiento. Dado que la imagen de la barra de seguimiento principal se muestra en el archivo de fondo y el usuario pulsa en la imagen de control, no en la imagen de la barra de seguimiento, solo se necesita la imagen deshabilitada para las barras de seguimiento. Se almacena en el archivo definido por Super en la sección Mapas de bits del archivo de definición de máscara. Un archivo Super también puede almacenar las imágenes Pushed y Disabled para otros botones, como Mute, que no es necesario que sea un botón de tipo hit.

> [!Note]  
> Los archivos de superágenes no se usan en máscaras para Reproductor de Windows Media 10 Mobile o posterior porque las imágenes deshabilitadas para las barras de seguimiento de búsqueda se encuentran en el archivo seekthumb.

 

La siguiente imagen es un archivo Super típico.

![super file](images/cesdksup.png)

Esto almacena las imágenes deshabilitadas para las barras de seguimiento y el botón de exclusión mutua. Estas imágenes se desplazan según se define en la sección Mapas de bits.

El área de fondo de la imagen de barra de seguimiento deshabilitada coincide exactamente con el área correspondiente en el archivo de fondo. Esto es importante, ya que todo el rectángulo definido para la imagen de barra de seguimiento deshabilitada reemplazará el área correspondiente en el archivo de fondo. Esto garantiza que la imagen de la barra de seguimiento deshabilitada se combina perfectamente con la imagen de fondo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de arte**](art-files-mobile.md)
</dt> </dl>

 

 




