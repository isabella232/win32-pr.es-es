---
title: Barras de seguimiento
description: Barras de seguimiento
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Reproductor de Windows Media Máscaras móviles, barras de seguimiento
- máscaras, barras de seguimiento
- referencia de máscaras, barras de seguimiento
- barras de seguimiento en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb7b64f7bada6f927b25aeecb71d584aa1ec2a68
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465828"
---
# <a name="trackbars"></a>Barras de seguimiento

Una barra de seguimiento muestra una imagen que cambia en incrementos pequeños. Las barras de seguimiento se usan para controles de volumen y controles de posición de reproducción. Puede usar barras de seguimiento para mostrar información sobre el elemento multimedia actual o para permitir que el usuario cambie la configuración o la posición de reproducción. Por ejemplo, puede usar una barra de seguimiento para permitir que el usuario ajuste el volumen y otra barra de seguimiento que pueda mostrar al usuario la posición de reproducción actual. Las barras de seguimiento tienen una imagen de posición que define la configuración actual del valor de la barra de seguimiento.

La sección Barras de seguimiento del archivo de definición de máscara debe comenzar con esta línea:


```C++
[ Trackbars ]

```



A continuación, debe agregar una o varias líneas que contengan información sobre cada una de las barras de seguimiento de la máscara.


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



Puede usar la siguiente plantilla para la sección Trackbars del archivo de definición de máscara:


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



Debe usar el orden siguiente para obtener información de la barra de seguimiento para cada línea de la sección Barras de seguimiento (se requiere cada parte de la línea):

1.  [Tipo de barra de seguimiento](trackbar-type.md)
2.  [Ubicación de la barra de seguimiento](trackbar-location.md)
3.  [Origen de la imagen para la barra de seguimiento deshabilitada](image-source-for-disabled-trackbar.md)
4.  [Origen de la imagen de thumb](thumb-image-source.md)
5.  [Tamaño de la miniatura](thumb-size.md)

Para obtener un ejemplo de código trackbars, consulte [la sección Barras de seguimiento de ejemplo](sample-trackbars-section.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




