---
title: Acerca del recorte y el escalado de imágenes GDI+
description: Puede usar el método DrawImage de la clase Graphics para dibujar y colocar imágenes.
ms.assetid: 81d20adc-0481-4b1b-80aa-ae218fdecd84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b44a13b5cee632e6ceafe327f94eca48edd93dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156200"
---
# <a name="about-cropping-and-scaling-gdi-images"></a>Acerca del recorte y el escalado de imágenes GDI+

Puede usar el método [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para dibujar y colocar imágenes. DrawImage es un método sobrecargado, por lo que hay varias formas de proporcionarle argumentos. Una variación de los [**gráficos::D método rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) recibe la dirección de un objeto de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) y una referencia a un objeto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) . El rectángulo especifica el destino de la operación de dibujo; es decir, especifica el rectángulo en el que se dibujará la imagen. Si el tamaño del rectángulo de destino es diferente del tamaño de la imagen original, la imagen se escala para ajustarse al rectángulo de destino. En el ejemplo siguiente se dibuja la misma imagen tres veces: una vez sin escalado, una vez con una expansión y otra con una compresión.


```
Bitmap myBitmap(L"Spiral.png");
Rect expansionRect(80, 10, 2 * myBitmap.GetWidth(), myBitmap.GetHeight());
Rect compressionRect(210, 10, myBitmap.GetWidth() / 2, 
   myBitmap.GetHeight() / 2);

myGraphics.DrawImage(&myBitmap, 10, 10);
myGraphics.DrawImage(&myBitmap, expansionRect);
myGraphics.DrawImage(&myBitmap, compressionRect);
```



El código anterior, junto con un archivo determinado, Spiral.png, generó el siguiente resultado.

![Ilustración que muestra tres versiones de una imagen: normal, ancho ensanchado y reducido a la mitad del tamaño original](images/aboutgdip03-art06.png)

Algunas variaciones del método [**Graphics::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) tienen un parámetro de rectángulo de origen, así como un parámetro de rectángulo de destino. El rectángulo de origen especifica la parte de la imagen original que se va a dibujar. El rectángulo de destino especifica dónde se dibujará la parte de la imagen. Si el tamaño del rectángulo de destino es diferente del tamaño del rectángulo de origen, la imagen se escala para ajustarse al rectángulo de destino.

En el ejemplo siguiente se crea un objeto de [**mapa de bits**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) a partir del archivo Runner.jpg. Toda la imagen se dibuja sin escalar en (0,0). Después, una pequeña parte de la imagen se dibuja dos veces: una vez con una compresión y otra con una expansión.


```
Bitmap myBitmap(L"Runner.jpg"); 

// The rectangle (in myBitmap) with upper-left corner (80, 70), 
// width 80, and height 45, encloses one of the runner's hands.

// Small destination rectangle for compressed hand.
Rect destRect1(200, 10, 20, 16);

// Large destination rectangle for expanded hand.
Rect destRect2(200, 40, 200, 160);

// Draw the original image at (0, 0).
myGraphics.DrawImage(&myBitmap, 0, 0);

// Draw the compressed hand.
myGraphics.DrawImage(
   &myBitmap, destRect1, 80, 70, 80, 45, UnitPixel);

// Draw the expanded hand. 
myGraphics.DrawImage(
   &myBitmap, destRect2, 80, 70, 80, 45, UnitPixel);
```



En la ilustración siguiente se muestra la imagen sin escala y las partes de la imagen comprimida y expandida.

![captura de pantalla que muestra una imagen, una parte de la imagen comprimida y, a continuación, la misma parte expandida](images/aboutgdip03-art07.png)

 

 



