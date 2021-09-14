---
title: Archivo SeekThumb
description: Archivo SeekThumb
ms.assetid: 757aeb93-ebf0-4659-8cb0-686e54485ac4
keywords:
- Reproductor de Windows Media Máscaras móviles, archivos de arte
- skins,art files
- archivos para máscaras, arte
- archivos art para máscaras, archivos SeekThumbd
- Reproductor de Windows Media Máscaras móviles, archivos SeekThumb
- archivos skins,SeekThumb
- Archivos SeekThumb en máscaras
- thumb,SeekThumb files
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9f1e9434a614dbc02e48b63508c7c2c04f553d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070862"
---
# <a name="seekthumb-file"></a>Archivo SeekThumb

El archivo SeekThumb define la imagen que indica la ubicación de reproducción dentro del elemento multimedia para una barra de seguimiento seek. Puede usar un archivo y definirlo para que lo usen SeekThumb y VolumeThumb. A diferencia de los demás archivos de arte, los archivos thumb se definen en la sección Barras de seguimiento del archivo de definición de máscara.

La siguiente imagen es un archivo SeekThumb típico.

![archivo seekthumb](images/cesdksee.gif)

Estos dos archivos de botón tienen el mismo aspecto, pero tienen tamaños ligeramente diferentes. La imagen izquierda es la vista normal que ve el usuario y la imagen derecha es la imagen pushed que el usuario ve cuando pulsa el botón.

> [!Note]  
> Los archivos de arte SeekThumb creados para máscaras usadas en Reproductor de Windows Media 10 Mobile o posterior deben tener las tres imágenes siguientes (de izquierda a derecha): normal, pushed y disabled.

 

Es posible que quiera que ciertas áreas de las imágenes digitales se transparenten. Esto le permitirá crear imágenes de posición en formas distintas de rectangulares. Cualquier región de una imagen de posición que rellene con el color especificado por el valor RGB 255, 0, 255 aparecerá transparente en la máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de arte**](art-files-mobile.md)
</dt> </dl>

 

 




