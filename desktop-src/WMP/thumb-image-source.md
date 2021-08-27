---
title: Origen de la imagen thumb
description: Origen de la imagen thumb
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Reproductor de Windows Media Máscaras móviles, barras de seguimiento
- máscaras, barras de seguimiento
- referencia de máscaras, barras de seguimiento
- barras de seguimiento en máscaras, origen de imagen
- barras de seguimiento en máscaras, origen de imagen thumb
- origen de imagen para máscaras, barras de seguimiento
- thumb,image source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550569a2858ba283824f28f6793097caa140c6112bccc41b3423413e17b6d89a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122775"
---
# <a name="thumb-image-source"></a>Origen de la imagen thumb

Debe definir el nombre del archivo que contiene la imagen de posición. Debe ser un nombre de archivo válido con la extensión .bmp, .gif, .jpg o .png. El archivo debe contener tres imágenes en paralelo de tamaño idéntico. Deben ser adyacentes entre sí sin espacio entre ellos. La posición superior izquierda de la imagen izquierda debe estar en la esquina superior izquierda del archivo. La imagen del lado izquierdo es la imagen normal de la imagen de posición, y la imagen en el centro representa el estado presionado y la imagen de la derecha representa el estado deshabilitado.


```C++
SeekThumb.bmp

```



Es posible que quiera que ciertas áreas de la imagen digital se transparenten. Esto le permitirá crear imágenes de posición en formas distintas de rectangulares. Cualquier región de la imagen de posición que rellene con el color especificado por el valor RGB 255, 0, 255 aparecerá transparente en la máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Barras de seguimiento**](trackbars.md)
</dt> </dl>

 

 




