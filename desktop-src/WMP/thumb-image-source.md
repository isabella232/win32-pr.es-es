---
title: Origen de la imagen de Thumb
description: Origen de la imagen de Thumb
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Aspectos de Windows Media Player Mobile, trackbars
- máscaras, trackbars
- referencia de las máscaras, trackbars
- trackbars en máscaras, origen de imagen
- trackbars en máscaras, origen de la imagen de Thumb
- origen de imagen para máscaras, trackbars
- Thumb, origen de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac19053b58c7d12543d38c639abe5a43c01ff64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075384"
---
# <a name="thumb-image-source"></a>Origen de la imagen de Thumb

Debe definir el nombre del archivo que contiene la imagen de Thumb. Debe ser un nombre de archivo válido con la extensión. bmp,. gif,. jpg o. png. El archivo debe contener tres imágenes en paralelo de tamaño idéntico. Deben ser adyacentes entre sí sin espacio. La posición superior izquierda de la imagen izquierda debe estar en la esquina superior izquierda del archivo. La imagen del lado izquierdo es la imagen normal de la imagen Thumb y la imagen en el centro representa el estado pushd y la imagen de la derecha describe el Estado deshabilitado.


```C++
SeekThumb.bmp

```



Puede que desee que determinadas áreas de la imagen de Thumb sean transparentes. Esto le permitirá crear imágenes Thumb en formas que no sean rectangulares. Cualquier región de la imagen de Thumb que rellene con el color especificado por el valor RGB 255, 0 y 255 aparecerá transparente en la máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trackbars**](trackbars.md)
</dt> </dl>

 

 




