---
title: Recorte y escalado de GDI+ imágenes
description: La clase Graphics proporciona varios métodos DrawImage, algunos de los cuales tienen parámetros de rectángulo de origen y destino que puede usar para recortar y escalar imágenes.
ms.assetid: cad64615-d8e6-4c03-a6c7-c98267a8f159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3684089ddab4ba963a79b80aafa67e94f94d988de5aa7d7d9f65ad31e48bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118067555"
---
# <a name="cropping-and-scaling-gdi-images"></a>Recorte y escalado de GDI+ imágenes

La [**clase Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) proporciona varios métodos **DrawImage,** algunos de los cuales tienen parámetros de rectángulo de origen y destino que puede usar para recortar y escalar imágenes.

En el ejemplo siguiente se construye un [**objeto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo Apple.gif. El código dibuja toda la imagen de apple en su tamaño original. A continuación, el código llama al **método DrawImage** de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para dibujar una parte de la imagen de apple en un rectángulo de destino mayor que la imagen de apple original.

El **método DrawImage** determina qué parte de la manzana se va a dibujar observando el rectángulo de origen, especificado por los argumentos tercero, cuarto, quinto y sexto. En este caso, la manzana se recorta al 75 por ciento de su ancho y al 75 por ciento de su alto.

El **método DrawImage** determina dónde dibujar la manzana recortada y el tamaño de la manzana recortada observando el rectángulo de destino, que se especifica mediante el segundo argumento. En este caso, el rectángulo de destino es un 30 por ciento más ancho y un 30 por ciento más alto que la imagen original.


```
Image image(L"Apple.gif");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Make the destination rectangle 30 percent wider and
// 30 percent taller than the original image.
// Put the upper-left corner of the destination
// rectangle at (150, 20).
Rect destinationRect(150, 20, 1.3 * width, 1.3 * height);
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw a portion of the image. Scale that portion of the image
// so that it fills the destination rectangle.
graphics.DrawImage(
   &image,
   destinationRect,
   0, 0,              // upper-left corner of source rectangle
   0.75 * width,      // width of source rectangle
   0.75 * height,     // height of source rectangle
   UnitPixel);
```



En la ilustración siguiente se muestra la manzana original y la manzana escalada y recortada.

![ilustración en la que se muestra una manzana y, a continuación, una parte ampliada de la manzana original](images/cropscale1.png)

 

 



