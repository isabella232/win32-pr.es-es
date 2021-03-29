---
title: Archivo VolumeThumb
description: Archivo VolumeThumb
ms.assetid: de6abfed-a811-44c4-8db2-f3b55ea38756
keywords:
- Aspectos móviles de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, archivos VolumeThumb
- Aspectos de Windows Media Player Mobile, archivos VolumeThumb
- máscaras, archivos VolumeThumb
- VolumeThumb de archivos en máscaras
- Thumb, archivos VolumeThumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b7ba87723025c91b3bdfb5af5fd233197dedb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775096"
---
# <a name="volumethumb-file"></a>Archivo VolumeThumb

El archivo VolumeThumb define la imagen que indica el nivel de volumen de reproducción de una barra de seguimiento de volumen. Puede usar un archivo y definirlo para su uso por SeekThumb y VolumeThumb. A diferencia de los demás archivos de arte, los archivos de control de posición se definen en la sección Trackbars del archivo de definición de máscara.

La siguiente imagen es un archivo VolumeThumb típico.

![archivo volumethumb](images/cesdkvol.png)

Estos dos archivos de botón tienen el mismo aspecto pero tienen tamaños ligeramente diferentes. La imagen izquierda es la vista normal que ve el usuario y la imagen de la derecha es la imagen insertada que el usuario ve al puntear en el botón.

Puede que desee que determinadas áreas de las imágenes de Thumb sean transparentes. Esto le permitirá crear imágenes Thumb en formas que no sean rectangulares. Cualquier región de una imagen Thumb que rellene con el color especificado por el valor RGB 255, 0 y 255 aparecerá transparente en la máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de imagen**](art-files-mobile.md)
</dt> </dl>

 

 




