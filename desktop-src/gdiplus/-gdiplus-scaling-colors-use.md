---
description: Una transformación de escalado multiplica uno o varios de los cuatro componentes de color por un número. Las entradas de la matriz de colores que representan el escalado se incluyen en la tabla siguiente.
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: Escalado de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370155306f7b1a177358d7cf28d329ebb0d75f8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248661"
---
# <a name="scaling-colors"></a>Escalado de colores

Una transformación de escalado multiplica uno o varios de los cuatro componentes de color por un número. Las entradas de la matriz de colores que representan el escalado se incluyen en la tabla siguiente.



| Componente que se va a escalar | Entrada de matriz |
|------------------------|--------------|
| Rojo                    | \[0 \] \[ 0\]   |
| Verde                  | \[1 \] \[ 1\]   |
| Azul                   | \[2 \] \[ 2\]   |
| Alpha                  | \[3 \] \[ 3\]   |



 

En el ejemplo siguiente se construye un [**objeto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo ColorBars2.bmp. A continuación, el código escala el componente azul de cada píxel de la imagen en un factor de 2. La imagen original se dibuja junto con la imagen transformada.


```
Image            image(L"ColorBars2.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 2.0f, 0.0f, 0.0f,
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



En la ilustración siguiente se muestra la imagen original a la izquierda y la imagen escalada a la derecha.

![Muestra cuatro barras de color y, a continuación, las mismas barras con colores diferentes.](images/colortrans3.png)

En la tabla siguiente se muestran los vectores de color de las cuatro barras antes y después del escalado azul. Tenga en cuenta que el componente azul de la cuarta barra de colores ha pasado de 0,8 a 0,6. Esto se debe a GDI+ conserva solo la parte fraccionera del resultado. Por ejemplo, (2)(0,8) = 1,6 y la parte fraccionera de 1,6 es 0,6. Conservar solo la parte fraccionera garantiza que el resultado siempre esté en el \[ intervalo 0, 1 \] .



| Original           | Escala             |
|--------------------|--------------------|
| (0.4, 0.4, 0.4, 1) | (0.4, 0.4, 0.8, 1) |
| (0.4, 0.2, 0.2, 1) | (0.4, 0.2, 0.4, 1) |
| (0.2, 0.4, 0.2, 1) | (0.2, 0.4, 0.4, 1) |
| (0.4, 0.4, 0.8, 1) | (0.4, 0.4, 0.6, 1) |



 

En el ejemplo siguiente se construye un [**objeto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo ColorBars2.bmp. A continuación, el código escala los componentes rojo, verde y azul de cada píxel de la imagen. Los componentes rojos se escalan verticalmente un 25 por ciento, los componentes verdes se escalan verticalmente un 35 por ciento y los componentes azules se escalan hacia abajo un 50 por ciento.


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   0.75f, 0.0f,  0.0f, 0.0f, 0.0f,
   0.0f,  0.65f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.5f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 1.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 0.0f, 1.0f};
   
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



En la ilustración siguiente se muestra la imagen original a la izquierda y la imagen escalada a la derecha.

![ilustración en la que se muestran cuatro barras de color y, a continuación, esas barras con colores diferentes](images/colortrans4.png)

En la tabla siguiente se muestran los vectores de color de las cuatro barras antes y después del escalado rojo, verde y azul.



| Original           | Escala               |
|--------------------|----------------------|
| (0.6, 0.6, 0.6, 1) | (0.45, 0.39, 0.3, 1) |
| (0, 1, 1, 1)       | (0, 0.65, 0.5, 1)    |
| (1, 1, 0, 1)       | (0.75, 0.65, 0, 1)   |
| (1, 0, 1, 1)       | (0.75, 0, 0.5, 1)    |



 

 

 



