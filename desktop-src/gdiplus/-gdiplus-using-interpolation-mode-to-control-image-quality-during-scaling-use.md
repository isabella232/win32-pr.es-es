---
description: El modo de interpolación de un objeto gráfico influye en la forma en que Windows GDI+ escala (estira y reduce) las imágenes.
ms.assetid: 3aeead47-78da-4ab3-9126-2fbe9e341e48
title: Usar el modo de interpolación para controlar la calidad de la imagen durante el ajuste de escala
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a829f2edf2f341f50bee771d909f7c4eef98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984426"
---
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a>Usar el modo de interpolación para controlar la calidad de la imagen durante el ajuste de escala

El modo de interpolación de un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) influye en la forma en que Windows GDI+ escala (estira y reduce) las imágenes. La enumeración [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) en Gdiplusenums. h define varios modos de interpolación, algunos de los cuales se muestran en la lista siguiente:

-   InterpolationModeNearestNeighbor
-   InterpolationModeBilinear
-   InterpolationModeHighQualityBilinear
-   InterpolationModeBicubic
-   InterpolationModeHighQualityBicubic

Para ajustar una imagen, cada píxel de la imagen original debe estar asignado a un grupo de píxeles de la imagen más grande. Para reducir una imagen, los grupos de píxeles de la imagen original deben estar asignados a píxeles individuales de la imagen más pequeña. La eficacia de los algoritmos que realizan estas asignaciones determina la calidad de una imagen escalada. Los algoritmos que generan imágenes escaladas de mayor calidad suelen requerir más tiempo de procesamiento. En la lista anterior, InterpolationModeNearestNeighbor es el modo de menor calidad y InterpolationModeHighQualityBicubic es el modo de mayor calidad.

Para establecer el modo de interpolación, pase uno de los miembros de la enumeración [**InterpolationMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) al método **SetInterpolationMode** de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

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

![Ilustración en la que se muestra una imagen original grande y las tres imágenes más pequeñas de calidad variable](images/grapes1.png)

 

 



