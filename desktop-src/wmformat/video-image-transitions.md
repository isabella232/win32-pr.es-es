---
title: Transiciones de imagen de vídeo
description: Transiciones de imagen de vídeo
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- Windows Media Format, transiciones de vídeo
- Formatos de sistema avanzado (ASF), transiciones de imagen de vídeo
- ASF (formato de sistemas avanzados), transiciones de imagen de vídeo
- transiciones de imagen de vídeo
- Códec de imagen V2 de Windows Media Video 9
- códecs, códec de Windows Media Video 9 Image V2
- secuencias de vídeo, códec de Windows Media Video 9 Image V2
- secuencias de vídeo, transiciones de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfd02628a78196a73750c2c0ff6b9e9c3d6729c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075530"
---
# <a name="video-image-transitions"></a>Transiciones de imagen de vídeo

El códec Windows Media Video 9 Image V2 anima una serie de imágenes, lo que da lugar a una secuencia de vídeo. El códec puede manipular dos imágenes a la vez, combinarlas y crear una transición de una a otra según la configuración proporcionada. En esta sección se describen las transiciones admitidas y los parámetros que requieren.

Las transiciones se muestran en la siguiente tabla por sus identificadores globales.



| Identificador de transición                                                                           | Descripción                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ vinculación de lazo de transición de imagen WMT \_ \_**](wmt-videoimage-transition-bow-tie.md)              | La nueva imagen se revela en un conjunto de triángulos en lados opuestos del marco.                                                                  |
| [**Círculo de transición de \_ imagen WMT \_ \_**](wmt-videoimage-transition-circle.md)                 | La nueva imagen se revela en un círculo.                                                                                                           |
| [**\_ \_ \_ difuminación cruzada de transición de imagen WMT \_**](wmt-videoimage-transition-cross-fade.md)        | Ninguna transición especial, los coeficientes de mezcla de las dos imágenes determinan el fundido transversal (disolver).                                         |
| [**DIAGONAL de transición de imagen de videotransmisión WMT \_ \_ \_**](wmt-videoimage-transition-diagonal.md)             | La nueva imagen se revela a lo largo de una línea diagonal que se origina en una esquina del fotograma.                                                          |
| [**diamante de transición de \_ imágenes WMT \_ \_**](wmt-videoimage-transition-diamond.md)               | La nueva imagen se revela en un rombo.                                                                                                          |
| [**\_ \_ transición de imagen de transmisión de imágenes WMT \_ \_ a \_ color**](wmt-videoimage-transition-fade-to-color.md) | Se resuelve de la imagen en un marco de color sólido.                                                                                          |
| [**\_transición de imagen de vídeo WMT \_ \_ rellenado \_ V**](wmt-videoimage-transition-filled-v.md)            | La nueva imagen se revela en un triángulo que se origina en un lado del marco.                                                                  |
| [**\_volteo de transición de imagen de videoimágenes WMT \_ \_**](wmt-videoimage-transition-flip.md)                     | La imagen anterior se gira en un eje y a través del centro del marco. La nueva imagen se revela como la parte posterior de la imagen anterior.                    |
| [**\_bajorrelieve de transición de imagen de videoimágenes WMT \_ \_**](wmt-videoimage-transition-inset.md)                   | Una nueva imagen se revela mediante un rectángulo que se origina en una esquina del fotograma.                                                               |
| [**\_iris de transición de imagen de imágenes WMT \_ \_**](wmt-videoimage-transition-iris.md)                     | La nueva imagen se revela a lo largo de un eje x y un eje y.                                                                                          |
| [**\_rollo de página de transición de VIDEOIMAGE WMT \_ \_ \_**](wmt-videoimage-transition-page-roll.md)          | La imagen antigua se transforma en un efecto de volteo de página y revela la nueva imagen debajo.                                                      |
| [**\_rectángulo de transición de imagen de videoimágenes WMT \_ \_**](wmt-videoimage-transition-rectangle.md)           | Una nueva imagen se revela mediante un rectángulo dentro del marco.                                                                                       |
| [**transición de imagen de transmisión de \_ imágenes WMT \_ \_**](wmt-videoimage-transition-reveal.md)                 | La nueva imagen se revela a lo largo de una línea recta que se origina en un lado del marco.                                                          |
| [**diapositiva de transición de \_ imagen WMT \_ \_**](wmt-videoimage-transition-slide.md)                   | La imagen antigua se desliza fuera del fotograma y se revela la nueva imagen debajo.                                                                       |
| [**División de transición de imagen de videotransmisión WMT \_ \_ \_**](wmt-videoimage-transition-split.md)                   | La nueva imagen se revela mediante una división horizontal o vertical en la imagen anterior. La división aparece a lo largo de una línea recta que comienza dentro del marco. |
| [**estrella de transición de \_ imágenes WMT \_ \_**](wmt-videoimage-transition-star.md)                     | La nueva imagen se revela mediante una estrella de cinco puntas dentro del marco.                                                                               |
| [**\_rueda de transición de VIDEOIMAGE WMT \_ \_**](wmt-videoimage-transition-wheel.md)                   | La nueva imagen se revela con cuatro radios rotatorios con un punto de pivote común.                                                                     |



 

Cada transición se describe completamente en su propio tema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> <dt>

[**\_SAMPLE2 de imágenes \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




