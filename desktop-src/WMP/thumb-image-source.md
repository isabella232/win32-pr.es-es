---
title: Origen de la imagen de thumb
description: Origen de la imagen de thumb
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Reproductor de Windows Media Máscaras móviles, barras de seguimiento
- máscaras, barras de seguimiento
- referencia de máscaras, barras de seguimiento
- barras de seguimiento en máscaras, origen de imagen
- barras de seguimiento en máscaras, origen de imagen de thumb
- origen de imagen para máscaras, barras de seguimiento
- thumb,image source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac19053b58c7d12543d38c639abe5a43c01ff64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465849"
---
# <a name="thumb-image-source"></a>Origen de la imagen de thumb

Debe definir el nombre del archivo que contiene la imagen thumb. Debe ser un nombre de archivo válido con la extensión .bmp, .gif, .jpg o .png. El archivo debe contener tres imágenes en paralelo de tamaño idéntico. Deben ser adyacentes entre sí sin espacio entre ellos. La posición superior izquierda de la imagen izquierda debe estar en la esquina superior izquierda del archivo. La imagen del lado izquierdo es la imagen normal de la imagen thumb, y la imagen en el centro muestra el estado de inserción y la imagen de la derecha representa el estado deshabilitado.


```C++
SeekThumb.bmp

```



Es posible que quiera hacer transparentes determinadas áreas de la imagen digital. Esto le permitirá crear imágenes de posición en formas distintas de rectangulares. Cualquier región de la imagen digital que rellene con el color especificado por el valor RGB 255, 0, 255 aparecerá transparente en la máscara.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Barras de seguimiento**](trackbars.md)
</dt> </dl>

 

 




