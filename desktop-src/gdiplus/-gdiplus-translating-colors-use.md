---
description: Una traducción agrega un valor a uno o varios de los cuatro componentes de color. Las entradas de la matriz de colores que representan traducciones se incluyen en la tabla siguiente.
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: Traducción de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608a0653423d854e6d77bd624949f24ec03cce6c4ed063d4c740dd142b1dfb3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036343"
---
# <a name="translating-colors"></a>Traducción de colores

Una traducción agrega un valor a uno o varios de los cuatro componentes de color. Las entradas de la matriz de colores que representan traducciones se incluyen en la tabla siguiente.



| Componente que se va a traducir | Entrada de matriz |
|----------------------------|--------------|
| Rojo                        | \[4 \] \[ 0\]   |
| Verde                      | \[4 \] \[ 1\]   |
| Azul                       | \[4 \] \[ 2\]   |
| Alpha                      | \[4 \] \[ 3\]   |



 

En el ejemplo siguiente se construye [**un objeto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo ColorBars.bmp. A continuación, el código agrega 0,75 al componente rojo de cada píxel de la imagen. La imagen original se dibuja junto con la imagen transformada.


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



En la ilustración siguiente se muestra la imagen original a la izquierda y la imagen transformada a la derecha.

![ilustración en la que se muestran cuatro barras de color y, a continuación, las mismas barras con colores diferentes](images/colortrans2.png)

En la tabla siguiente se enumeran los vectores de color de las cuatro barras antes y después de la traducción roja. Tenga en cuenta que, dado que el valor máximo de un componente de color es 1, el componente rojo de la segunda fila no cambia. (De forma similar, el valor mínimo de un componente de color es 0).



| Original           | Traducidos      |
|--------------------|-----------------|
| Negro (0, 0, 0, 1) | (0.75, 0, 0, 1) |
| Rojo (1, 0, 0, 1)   | (1, 0, 0, 1)    |
| Verde (0, 1, 0, 1) | (0.75, 1, 0, 1) |
| Azul (0, 0, 1, 1)  | (0.75, 0, 1, 1) |



 

 

 



