---
description: Una traducción agrega un valor a uno o varios de los cuatro componentes de color. En la tabla siguiente se proporcionan las entradas de la matriz de colores que representan las traducciones.
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: Traducir colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c769a24c02e977c3e32ff913852d4b6b8d54441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559684"
---
# <a name="translating-colors"></a>Traducir colores

Una traducción agrega un valor a uno o varios de los cuatro componentes de color. En la tabla siguiente se proporcionan las entradas de la matriz de colores que representan las traducciones.



| Componente que se va a traducir | Entrada de matriz |
|----------------------------|--------------|
| Rojo                        | \[4 \] \[ 0\]   |
| Verde                      | \[4 \] \[ 1\]   |
| Azul                       | \[4 \] \[ 2\]   |
| Alpha                      | \[4 \] \[ 3\]   |



 

En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo ColorBars.bmp. Después, el código agrega 0,75 al componente rojo de cada píxel de la imagen. La imagen original se dibuja junto con la imagen transformada.


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f,  0.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  1.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 1.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 0.0f, 1.0f, 0.0f,
   0.75f, 0.0f, 0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



En la ilustración siguiente se muestra la imagen original de la izquierda y la imagen transformada a la derecha.

![Ilustración que muestra cuatro barras coloreadas y, a continuación, las mismas barras con distintos colores](images/colortrans2.png)

En la tabla siguiente se enumeran los vectores de color de las cuatro barras antes y después de la traducción roja. Tenga en cuenta que, dado que el valor máximo de un componente de color es 1, el componente rojo de la segunda fila no cambia. (De igual forma, el valor mínimo de un componente de color es 0).



| Original           | Traducidos      |
|--------------------|-----------------|
| Negro (0,0, 0, 1) | (0.75, 0, 0, 1) |
| Rojo (1, 0, 0, 1)   | (1, 0, 0, 1)    |
| Verde (0, 1, 0, 1) | (0.75, 1, 0, 1) |
| Blue (0, 0, 1, 1)  | (0.75, 0, 1, 1) |



 

 

 



