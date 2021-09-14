---
description: El modo de interpolación de un objeto Graphics influye en la Windows GDI+ escala (se ajusta y reduce) imágenes.
ms.assetid: 3aeead47-78da-4ab3-9126-2fbe9e341e48
title: Uso del modo de interpolación para controlar la calidad de la imagen durante el escalado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a829f2edf2f341f50bee771d909f7c4eef98e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063412"
---
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a>Uso del modo de interpolación para controlar la calidad de la imagen durante el escalado

El modo de interpolación de un [**objeto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) influye en la Windows GDI+ escala (se ajusta y reduce) imágenes. La [**enumeración InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) de Gdiplusenums.h define varios modos de interpolación, algunos de los cuales se muestran en la lista siguiente:

-   InterpolationModeNearestNeighbor
-   InterpolationModeBilinear
-   InterpolationModeHighQualityBilinear
-   InterpolationModeBicubic
-   InterpolationModeHighQualityBicubic

Para extender una imagen, cada píxel de la imagen original debe asignarse a un grupo de píxeles en la imagen más grande. Para reducir una imagen, los grupos de píxeles de la imagen original deben asignarse a píxeles únicos en la imagen más pequeña. La eficacia de los algoritmos que realizan estas asignaciones determina la calidad de una imagen escalada. Los algoritmos que producen imágenes escaladas de mayor calidad tienden a requerir más tiempo de procesamiento. En la lista anterior, InterpolationModeNearestNeighbor es el modo de menor calidad y InterpolationModeHighQualityBicubic es el modo de mayor calidad.

Para establecer el modo de interpolación, pase uno de los miembros de la [**enumeración InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) al **método SetInterpolationMode** de un [**objeto Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)

En el ejemplo siguiente se dibuja una imagen y, a continuación, se reduce la imagen con tres modos de interpolación diferentes:


```
Image image(L"GrapeBunch.bmp");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Draw the image with no shrinking or stretching.
graphics.DrawImage(
   &image,
   Rect(10, 10, width, height),  // destination rectangle  
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using low-quality interpolation. 
graphics.SetInterpolationMode(InterpolationModeNearestNeighbor);
graphics.DrawImage(
   &image,
   Rect(10, 250, 0.6*width, 0.6*height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using medium-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBilinear);
graphics.DrawImage(
   &image,
   Rect(150, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using high-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBicubic);
graphics.DrawImage(
   &image,
   Rect(290, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
```



En la ilustración siguiente se muestra la imagen original y las tres imágenes más pequeñas.

![ilustración que muestra una imagen original grande y las tres imágenes más pequeñas de distinta calidad](images/grapes1.png)

 

 



