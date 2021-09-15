---
description: La cizallamiento aumenta o reduce un componente de color en una cantidad proporcional a otro componente de color.
ms.assetid: 12f83f35-33f1-4ac9-b45d-f8700e54053a
title: Colores de cizallamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d632fded9f2b4d1e4682ae9f8ffbfedee85a46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473136"
---
# <a name="shearing-colors"></a>Colores de cizallamiento

La cizallamiento aumenta o reduce un componente de color en una cantidad proporcional a otro componente de color. Por ejemplo, considere la transformación en la que el componente rojo aumenta en una mitad el valor del componente azul. En este tipo de transformación, el color (0,2, 0,5, 1) se convertiría en (0,7, 0,5, 1). El nuevo componente rojo es 0,2 + (1/2)(1) = 0,7.

En el ejemplo siguiente se construye un [**objeto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo ColorBars4.bmp. A continuación, el código aplica la transformación de cizallamiento descrita en el párrafo anterior a cada píxel de la imagen.


```
Image            image(L"ColorBars4.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.5f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
   
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



En la ilustración siguiente se muestra la imagen original a la izquierda y la imagen con el mismo tamaño a la derecha.

![ilustración en la que se muestran cuatro barras de color y, a continuación, las mismas barras con colores diferentes](images/colortrans6.png)

En la tabla siguiente se muestran los vectores de color de las cuatro barras antes y después de la transformación de cizallamiento.



| Original           | Esquilada            |
|--------------------|--------------------|
| (0, 0, 1, 1)       | (0.5, 0, 1, 1)     |
| (0.5, 1, 0.5, 1)   | (0.75, 1, 0.5, 1)  |
| (1, 1, 0, 1)       | (1, 1, 0, 1)       |
| (0.4, 0.4, 0.4, 1) | (0.6, 0.4, 0.4, 1) |



 

 

 



