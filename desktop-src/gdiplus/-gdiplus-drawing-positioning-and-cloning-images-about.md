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
# <a name="drawing-positioning-and-cloning-images"></a><span data-ttu-id="17d5b-103">Dibujo, posicionamiento y clonación de imágenes</span><span class="sxs-lookup"><span data-stu-id="17d5b-103">Drawing, Positioning, and Cloning Images</span></span>

<span data-ttu-id="17d5b-104">Puede usar la clase de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) para cargar y mostrar imágenes de trama (mapas de bits) e imágenes vectoriales (metaarchivos).</span><span class="sxs-lookup"><span data-stu-id="17d5b-104">You can use the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class to load and display raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="17d5b-105">Para mostrar una imagen, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto **Image** .</span><span class="sxs-lookup"><span data-stu-id="17d5b-105">To display an image, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and an **Image** object.</span></span> <span data-ttu-id="17d5b-106">El objeto **Graphics** proporciona el método [**graphics::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) , que recibe la dirección del objeto de **imagen** como argumento.</span><span class="sxs-lookup"><span data-stu-id="17d5b-106">The **Graphics** object provides the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) method, which receives the address of the **Image** object as an argument.</span></span>

<span data-ttu-id="17d5b-107">En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo Climber.jpg y, a continuación, se muestra la imagen.</span><span class="sxs-lookup"><span data-stu-id="17d5b-107">The following example constructs an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Climber.jpg and then displays the image.</span></span> <span data-ttu-id="17d5b-108">El punto de destino de la esquina superior izquierda de la imagen, (10, 10), se especifica en el segundo y tercer parámetro del método [**Graphics::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="17d5b-108">The destination point for the upper-left corner of the image, (10, 10), is specified in the second and third parameters of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint)) method.</span></span>


```
Image myImage(L"Climber.jpg");
myGraphics.DrawImage(&myImage, 10, 10);
```



<span data-ttu-id="17d5b-109">El código anterior, junto con un archivo determinado, Climber.jpg, generó el siguiente resultado.</span><span class="sxs-lookup"><span data-stu-id="17d5b-109">The preceding code, along with a particular file, Climber.jpg, produced the following output.</span></span>

![captura de pantalla de una ventana que contiene una foto](images/aboutgdip03-art04.png)

<span data-ttu-id="17d5b-111">Puede crear objetos de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir de una variedad de formatos de archivo de gráficos: BMP, GIF, JPEG, EXIF, PNG, TIFF, WMF, EMF e icono.</span><span class="sxs-lookup"><span data-stu-id="17d5b-111">You can construct [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects from a variety of graphics file formats: BMP, GIF, JPEG, Exif, PNG, TIFF, WMF, EMF, and ICON.</span></span>

<span data-ttu-id="17d5b-112">En el ejemplo siguiente se crean objetos de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir de diversos tipos de archivo y, a continuación, se muestran las imágenes.</span><span class="sxs-lookup"><span data-stu-id="17d5b-112">The following example constructs [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects from a variety of file types and then displays the images.</span></span>


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



<span data-ttu-id="17d5b-113">La clase [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) proporciona un [**método Image:: Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) que puede usar para hacer una copia de un objeto de **imagen**, [**metarchivo**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile)o mapa de [**bits**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) existente.</span><span class="sxs-lookup"><span data-stu-id="17d5b-113">The [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class provides a [**Image::Clone**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-image-clone) method that you can use to make a copy of an existing **Image**, [**Metafile**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-metafile), or [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="17d5b-114">El método [Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) se sobrecarga en la clase **Bitmap** y una de las variaciones tiene un parámetro de rectángulo de origen que puede usar para especificar la parte de la imagen original que desea copiar.</span><span class="sxs-lookup"><span data-stu-id="17d5b-114">The [Clone](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-clone(inconstrectf__inpixelformat)) method is overloaded in the **Bitmap** class, and one of the variations has a source-rectangle parameter that you can use to specify the portion of the original image that you want to copy.</span></span> <span data-ttu-id="17d5b-115">En el ejemplo siguiente se crea un objeto de **mapa de bits** mediante la clonación de la mitad superior de un objeto de **mapa de bits** existente.</span><span class="sxs-lookup"><span data-stu-id="17d5b-115">The following example creates a **Bitmap** object by cloning the top half of an existing **Bitmap** object.</span></span> <span data-ttu-id="17d5b-116">A continuación, se muestran las dos imágenes.</span><span class="sxs-lookup"><span data-stu-id="17d5b-116">Then both images are displayed.</span></span>


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



<span data-ttu-id="17d5b-117">El código anterior, junto con un archivo determinado, Spiral.png, generó el siguiente resultado.</span><span class="sxs-lookup"><span data-stu-id="17d5b-117">The preceding code, along with a particular file, Spiral.png, produced the following output.</span></span>

![Ilustración de una imagen, seguida de la mitad superior de la imagen original](images/aboutgdip03-art05.png)

 

 
