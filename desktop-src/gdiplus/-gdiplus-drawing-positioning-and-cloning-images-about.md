---
description: Puede usar la clase Image para cargar y mostrar imágenes de trama (mapas de bits) e imágenes vectoriales (metarchivos).
ms.assetid: 0ad2a132-6db6-4099-81a2-10e1cd1b1f61
title: Dibujo, posicionamiento y clonación de imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37e53ce3937d4f10b91a92e64feec57c6b39e718e7b551e4e4130569d4dd90d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015155"
---
# <a name="drawing-positioning-and-cloning-images"></a>Dibujo, posicionamiento y clonación de imágenes

Puede usar la clase [**Image para**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) cargar y mostrar imágenes de trama (mapas de bits) e imágenes vectoriales (metarchivos). Para mostrar una imagen, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un **objeto Image.** El **objeto Graphics** proporciona el método [**Graphics::D rawImage,**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) que recibe la dirección del objeto **Image** como argumento.

En el ejemplo siguiente se construye un [**objeto Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del Climber.jpg y, a continuación, se muestra la imagen. El punto de destino de la esquina superior izquierda de la imagen (10, 10) se especifica en el segundo y tercer parámetro del método [**Graphics::D rawImage.**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint))


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



El código anterior, junto con un archivo determinado, Climber.jpg, generaba la siguiente salida.

![captura de pantalla de una ventana que contiene una foto](images/aboutgdip03-art04.png)

Puede construir objetos [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir de diversos formatos de archivo de gráficos: BMP, GIF, JPEG, Exif, PNG, TIFF, WMF, EMF e ICON.

En el ejemplo siguiente se [**construyen objetos Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir de diversos tipos de archivo y, a continuación, se muestran las imágenes.


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



La [**clase Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) proporciona un método [**Image::Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) que puede usar para realizar una copia de un objeto **Image,** [**Metafile**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)o [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) existente. El [método Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) está sobrecargado en la clase **Bitmap** y una de las variaciones tiene un parámetro source-rectangle que puede usar para especificar la parte de la imagen original que desea copiar. En el ejemplo siguiente se crea **un objeto Bitmap** clonando la mitad superior de un objeto **Bitmap** existente. A continuación, se muestran ambas imágenes.


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



El código anterior, junto con un archivo determinado, Spiral.png, generaba la siguiente salida.

![ilustración de una imagen, seguida de la mitad superior de la imagen orignal](images/aboutgdip03-art05.png)

 

 
