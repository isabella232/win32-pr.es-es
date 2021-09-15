---
title: Recorte y escalado de GDI+ imágenes
description: La clase Graphics proporciona varios métodos DrawImage, algunos de los cuales tienen parámetros de rectángulo de origen y destino que puede usar para recortar y escalar imágenes.
ms.assetid: cad64615-d8e6-4c03-a6c7-c98267a8f159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c70a7b4f7aa0374602326ab856a01bbadc0047
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580044"
---
# <a name="cropping-and-scaling-gdi-images"></a>Recorte y escalado de GDI+ imágenes

La [**clase Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) proporciona varios **métodos DrawImage,** algunos de los cuales tienen parámetros de rectángulo de origen y destino que puede usar para recortar y escalar imágenes.

En el ejemplo siguiente se construye un [**objeto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo Apple.gif. El código dibuja toda la imagen de apple en su tamaño original. A continuación, el código llama al **método DrawImage** de un [**objeto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para dibujar una parte de la imagen de apple en un rectángulo de destino mayor que la imagen de apple original.

El **método DrawImage** determina qué parte de la manzana se va a dibujar mirando el rectángulo de origen, especificado por los argumentos tercero, cuarto, quinto y sexto. En este caso, la manzana se recorta al 75 por ciento de su ancho y al 75 por ciento de su altura.

El **método DrawImage** determina dónde dibujar la manzana recortada y el tamaño de la manzana recortada al mirar el rectángulo de destino, que se especifica mediante el segundo argumento. En este caso, el rectángulo de destino es un 30 % más ancho y un 30 % más alto que la imagen original.


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



En la ilustración siguiente se muestra la manzana original y la manzana recortada y escalada.

![ilustración en la que se muestra una manzana y, a continuación, una parte ampliada de la manzana original](images/cropscale1.png)

 

 



