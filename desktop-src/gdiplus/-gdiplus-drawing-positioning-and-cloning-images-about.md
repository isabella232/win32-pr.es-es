---
description: Puede usar la clase de imagen para cargar y mostrar imágenes de trama (mapas de bits) e imágenes vectoriales (metaarchivos).
ms.assetid: 0ad2a132-6db6-4099-81a2-10e1cd1b1f61
title: Dibujo, posicionamiento y clonación de imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa265a8f75cbfcaf0ff614ded4466482e5b986b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276393"
---
# <a name="drawing-positioning-and-cloning-images"></a>Dibujo, posicionamiento y clonación de imágenes

Puede usar la clase de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) para cargar y mostrar imágenes de trama (mapas de bits) e imágenes vectoriales (metaarchivos). Para mostrar una imagen, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto **Image** . El objeto **Graphics** proporciona el método [**graphics::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) , que recibe la dirección del objeto de **imagen** como argumento.

En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo Climber.jpg y, a continuación, se muestra la imagen. El punto de destino de la esquina superior izquierda de la imagen, (10, 10), se especifica en el segundo y tercer parámetro del método [**Graphics::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) .


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



El código anterior, junto con un archivo determinado, Climber.jpg, generó el siguiente resultado.

![captura de pantalla de una ventana que contiene una foto](images/aboutgdip03-art04.png)

Puede crear objetos de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir de una variedad de formatos de archivo de gráficos: BMP, GIF, JPEG, EXIF, PNG, TIFF, WMF, EMF e icono.

En el ejemplo siguiente se crean objetos de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir de diversos tipos de archivo y, a continuación, se muestran las imágenes.


```
Image myBMP(L"SpaceCadet.bmp");
Image myEMF(L"Metafile1.emf");
Image myGIF(L"Soda.gif");
Image myJPEG(L"Mango.jpg");
Image myPNG(L"Flowers.png");
Image myTIFF(L"MS.tif");

myGraphics.DrawImage(&myBMP, 10, 10);
myGraphics.DrawImage(&myEMF, 220, 10);
myGraphics.DrawImage(&myGIF, 320, 10);
myGraphics.DrawImage(&myJPEG, 380, 10);
myGraphics.DrawImage(&myPNG, 150, 200);
myGraphics.DrawImage(&myTIFF, 300, 200);
```



La clase [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) proporciona un [**método Image:: Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) que puede usar para hacer una copia de un objeto de **imagen**, [**metarchivo**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)o mapa de [**bits**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) existente. El método [Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) se sobrecarga en la clase **Bitmap** y una de las variaciones tiene un parámetro de rectángulo de origen que puede usar para especificar la parte de la imagen original que desea copiar. En el ejemplo siguiente se crea un objeto de **mapa de bits** mediante la clonación de la mitad superior de un objeto de **mapa de bits** existente. A continuación, se muestran las dos imágenes.


```
Bitmap* originalBitmap = new Bitmap(L"Spiral.png");
RectF sourceRect(
   0.0f,
   0.0f, 
   (REAL)(originalBitmap->GetWidth()), 
   (REAL)(originalBitmap->GetHeight())/2.0f);

Bitmap* secondBitmap = originalBitmap->Clone(sourceRect, PixelFormatDontCare);

myGraphics.DrawImage(originalBitmap, 10, 10);
myGraphics.DrawImage(secondBitmap, 100, 10);
```



El código anterior, junto con un archivo determinado, Spiral.png, generó el siguiente resultado.

![Ilustración de una imagen, seguida de la mitad superior de la imagen original](images/aboutgdip03-art05.png)

 

 
