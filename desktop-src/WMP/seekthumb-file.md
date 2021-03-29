---
title: Archivo SeekThumb
description: Archivo SeekThumb
ms.assetid: 757aeb93-ebf0-4659-8cb0-686e54485ac4
keywords:
- Aspectos móviles de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, archivos SeekThumbd
- Aspectos de Windows Media Player Mobile, archivos SeekThumb
- máscaras, archivos SeekThumb
- SeekThumb de archivos en máscaras
- Thumb, archivos SeekThumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9f1e9434a614dbc02e48b63508c7c2c04f553d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994362"
---
# <a name="seekthumb-file"></a>Archivo SeekThumb

El archivo SeekThumb define la imagen que indica la ubicación de reproducción dentro del elemento multimedia para una barra de búsqueda de búsqueda. Puede usar un archivo y definirlo para su uso por SeekThumb y VolumeThumb. A diferencia de los demás archivos de arte, los archivos de control de posición se definen en la sección Trackbars del archivo de definición de máscara.

La siguiente imagen es un archivo SeekThumb típico.

![archivo seekthumb](images/cesdksee.gif)

Estos dos archivos de botón tienen el mismo aspecto pero tienen tamaños ligeramente diferentes. La imagen izquierda es la vista normal que ve el usuario y la imagen de la derecha es la imagen insertada que el usuario ve al puntear en el botón.

> [!Note]  
> Los archivos de SeekThumb Art creados para las máscaras usadas en Windows Media Player 10 Mobile o posterior deben tener las tres imágenes siguientes (de izquierda a derecha): normal, insertado y deshabilitado.

 

Puede que desee que determinadas áreas de las imágenes de Thumb sean transparentes. Esto le permitirá crear imágenes Thumb en formas que no sean rectangulares. Cualquier región de una imagen Thumb que rellene con el color especificado por el valor RGB 255, 0 y 255 aparecerá transparente en la máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de imagen**](art-files-mobile.md)
</dt> </dl>

 

 




