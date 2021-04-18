---
title: Trackbars
description: Trackbars
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Aspectos de Windows Media Player Mobile, trackbars
- máscaras, trackbars
- referencia de las máscaras, trackbars
- trackbars en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb7b64f7bada6f927b25aeecb71d584aa1ec2a68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704743"
---
# <a name="trackbars"></a>Trackbars

Una barra de aumento muestra una imagen que cambia en incrementos pequeños. Trackbars se usan para los controles de volumen y los controles de posición de reproducción. Puede usar trackbars para mostrar información sobre el elemento multimedia actual o para permitir que el usuario cambie la configuración o la posición de reproducción. Por ejemplo, puede utilizar una barra de presentación para permitir que el usuario ajuste el volumen y otro que pueda mostrar al usuario la posición de reproducción actual. Trackbars tienen una imagen Thumb que define la configuración actual del valor de TrackBar.

La sección Trackbars del archivo de definición de máscara debe comenzar con esta línea:


```C++
[ Trackbars ]

```



A continuación, debe agregar una o más líneas que contengan información sobre cada uno de los trackbars de la máscara.


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



Puede usar la siguiente plantilla para la sección Trackbars del archivo de definición de máscara:


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



Debe usar el orden siguiente para obtener información de TrackBar para cada línea de la sección Trackbars (se requiere cada parte de la línea):

1.  [Tipo de barra de texto](trackbar-type.md)
2.  [Ubicación de TrackBar](trackbar-location.md)
3.  [Origen de imagen para TrackBar deshabilitado](image-source-for-disabled-trackbar.md)
4.  [Origen de la imagen de Thumb](thumb-image-source.md)
5.  [Tamaño de Thumb](thumb-size.md)

Para obtener un ejemplo de código Trackbars, consulte la [sección Trackbars de ejemplo](sample-trackbars-section.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




