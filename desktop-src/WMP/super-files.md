---
title: Super Files
description: Super Files
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Reproductor de Windows Media Máscaras móviles, archivos art
- skins,art files
- archivos para máscaras, art
- archivos art para máscaras, archivos super files
- Reproductor de Windows Media Máscaras móviles, archivos super files
- skins,Super files
- Archivos super en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece533f81f8866eb0f9848d7296cc23bcd37f453
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569409"
---
# <a name="super-files"></a>Super Files

Los archivos super se usan para almacenar las imágenes deshabilitadas para las barras de seguimiento. Dado que la imagen de la barra de seguimiento principal se muestra en el archivo de fondo y el usuario pulsa en la imagen de posición, no en la imagen de la barra de seguimiento, solo se necesita la imagen Deshabilitada para las barras de seguimiento. Se almacena en el archivo definido por Super en la sección Mapas de bits del archivo de definición de máscara. Un archivo Super también puede almacenar las imágenes Pushed y Disabled para otros botones, como Exclusión mutua, que no es necesario que sea un botón de tipo de pulsación.

> [!Note]  
> Los archivos superárculos no se usan en máscaras para Reproductor de Windows Media 10 Mobile o posterior porque las imágenes deshabilitadas para las barras de seguimiento de búsqueda se encuentran en el archivo seekthumb.

 

La siguiente imagen es un archivo Super típico.

![super file](images/cesdksup.png)

Esto almacena las imágenes deshabilitadas para las barras de seguimiento y el botón de exclusión mutua. Estas imágenes se desplazan según se define en la sección Mapas de bits.

El área de fondo de la imagen de barra de seguimiento deshabilitada coincide exactamente con el área correspondiente del archivo background. Esto es importante, ya que todo el rectángulo definido para la imagen de barra de seguimiento deshabilitada reemplazará el área correspondiente en el archivo background. Esto garantiza que la imagen de barra de seguimiento deshabilitada se combina perfectamente con la imagen de fondo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de arte**](art-files-mobile.md)
</dt> </dl>

 

 




