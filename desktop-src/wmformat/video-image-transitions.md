---
title: Transiciones de imágenes de vídeo
description: Transiciones de imágenes de vídeo
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- Windows SDK de formato multimedia, transiciones de imágenes de vídeo
- Formato de sistemas avanzados (ASF), transiciones de imagen de vídeo
- ASF (formato de sistemas avanzados), transiciones de imagen de vídeo
- transiciones de imágenes de vídeo
- Windows Códec de imagen v2 de Vídeo multimedia 9
- códecs, Windows códec de imagen v2 de Vídeo multimedia 9
- secuencias de vídeo, Windows códec de imagen v2 de Vídeo multimedia 9
- secuencias de vídeo, transiciones de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b0a915f34ac9a2dcc00f8bcec739d48051361c1744e8e455166d56238529d9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771245"
---
# <a name="video-image-transitions"></a>Transiciones de imágenes de vídeo

El códec Windows Media Video 9 Image v2 anima una serie de imágenes, lo que da lugar a una secuencia de vídeo. El códec puede manipular dos imágenes a la vez, combinarlas y crear una transición de una a otra según la configuración que proporcione. En esta sección se describen las transiciones admitidas y los parámetros que requieren.

Las transiciones se enumeran en la tabla siguiente por sus identificadores globales.



| Identificador de transición                                                                           | Descripción                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ BOW \_ TIE**](wmt-videoimage-transition-bow-tie.md)              | La nueva imagen se muestra en un conjunto de triángulos en los lados opuestos del marco.                                                                  |
| [**CÍRCULO DE TRANSICIÓN \_ DE WMT VIDEOIMAGE \_ \_**](wmt-videoimage-transition-circle.md)                 | La nueva imagen se muestra en un círculo.                                                                                                           |
| [**TRANSICIÓN CRUZADA \_ DE WMT VIDEOIMAGE \_ TRANSITION \_ \_**](wmt-videoimage-transition-cross-fade.md)        | Sin transición especial, los coeficientes de mezcla de las dos imágenes determinan la atenuación cruzada (disolver).                                         |
| [**DIAGONAL DE TRANSICIÓN \_ DE WMT VIDEOIMAGE \_ \_**](wmt-videoimage-transition-diagonal.md)             | La nueva imagen se muestra a lo largo de una línea diagonal que se origina en una esquina del marco.                                                          |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ DIAMOND**](wmt-videoimage-transition-diamond.md)               | La nueva imagen se muestra en un rombo.                                                                                                          |
| [**TRANSICIÓN DE \_ WMT VIDEOIMAGE \_ A \_ \_ \_ COLOR**](wmt-videoimage-transition-fade-to-color.md) | Se desvía de la imagen a un marco de color sólido.                                                                                          |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ FILLED \_ V**](wmt-videoimage-transition-filled-v.md)            | La nueva imagen se muestra en un triángulo que se origina en un lado del marco.                                                                  |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ FLIP**](wmt-videoimage-transition-flip.md)                     | La imagen antigua se gira en un eje Y a través del centro del marco. La nueva imagen se muestra como la parte posterior de la imagen anterior.                    |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ INSET**](wmt-videoimage-transition-inset.md)                   | La nueva imagen se muestra mediante un rectángulo que se origina en una esquina del marco.                                                               |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ IRIS**](wmt-videoimage-transition-iris.md)                     | La nueva imagen se muestra a lo largo de un eje X y un eje Y.                                                                                          |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ PAGE \_ ROLL**](wmt-videoimage-transition-page-roll.md)          | La imagen antigua se transforma en un efecto de volteo de página, lo que revela la nueva imagen debajo.                                                      |
| [**RECTÁNGULO DE TRANSICIÓN \_ DE VIDEOIMAGE \_ DE WMT \_**](wmt-videoimage-transition-rectangle.md)           | Un rectángulo dentro del marco muestra una nueva imagen.                                                                                       |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ REVEAL**](wmt-videoimage-transition-reveal.md)                 | La nueva imagen se muestra a lo largo de una línea recta que se origina en un lado del marco.                                                          |
| [**DIAPOSITIVA DE TRANSICIÓN \_ WMT VIDEOIMAGE \_ \_**](wmt-videoimage-transition-slide.md)                   | La imagen antigua se desliza fuera del marco, lo que revela la nueva imagen debajo.                                                                       |
| [**DIVISIÓN DE TRANSICIÓN \_ DE WMT VIDEOIMAGE \_ \_**](wmt-videoimage-transition-split.md)                   | La nueva imagen se revela mediante una división horizontal o vertical en la imagen anterior. La división aparece a lo largo de una línea recta a partir del marco. |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ STAR**](wmt-videoimage-transition-star.md)                     | Una estrella de cinco puntas dentro del marco revela una nueva imagen.                                                                               |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ WHEEL**](wmt-videoimage-transition-wheel.md)                   | La nueva imagen se revela mediante cuatro radios de rotación con un punto de pivote común.                                                                     |



 

Cada transición se describe completamente en su propio tema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> <dt>

[**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




