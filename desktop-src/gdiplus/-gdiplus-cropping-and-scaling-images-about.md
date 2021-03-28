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
# <a name="about-cropping-and-scaling-gdi-images"></a><span data-ttu-id="898b6-103">Acerca del recorte y el escalado de imágenes GDI+</span><span class="sxs-lookup"><span data-stu-id="898b6-103">About cropping and scaling GDI+ images</span></span>

<span data-ttu-id="898b6-104">Puede usar el método [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para dibujar y colocar imágenes.</span><span class="sxs-lookup"><span data-stu-id="898b6-104">You can use the [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw and position images.</span></span> <span data-ttu-id="898b6-105">DrawImage es un método sobrecargado, por lo que hay varias formas de proporcionarle argumentos.</span><span class="sxs-lookup"><span data-stu-id="898b6-105">DrawImage is an overloaded method, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="898b6-106">Una variación de los [**gráficos::D método rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) recibe la dirección de un objeto de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) y una referencia a un objeto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) .</span><span class="sxs-lookup"><span data-stu-id="898b6-106">One variation of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method receives the address of an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object and a reference to a [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object.</span></span> <span data-ttu-id="898b6-107">El rectángulo especifica el destino de la operación de dibujo; es decir, especifica el rectángulo en el que se dibujará la imagen.</span><span class="sxs-lookup"><span data-stu-id="898b6-107">The rectangle specifies the destination for the drawing operation; that is, it specifies the rectangle in which the image will be drawn.</span></span> <span data-ttu-id="898b6-108">Si el tamaño del rectángulo de destino es diferente del tamaño de la imagen original, la imagen se escala para ajustarse al rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="898b6-108">If the size of the destination rectangle is different from the size of the original image, the image is scaled to fit the destination rectangle.</span></span> <span data-ttu-id="898b6-109">En el ejemplo siguiente se dibuja la misma imagen tres veces: una vez sin escalado, una vez con una expansión y otra con una compresión.</span><span class="sxs-lookup"><span data-stu-id="898b6-109">The following example draws the same image three times: once with no scaling, once with an expansion, and once with a compression.</span></span>


```
Bitmap myBitmap(L"Spiral.png");
Rect expansionRect(80, 10, 2 * myBitmap.GetWidth(), myBitmap.GetHeight());
Rect compressionRect(210, 10, myBitmap.GetWidth() / 2, 
   myBitmap.GetHeight() / 2);

myGraphics.DrawImage(&myBitmap, 10, 10);
myGraphics.DrawImage(&myBitmap, expansionRect);
myGraphics.DrawImage(&myBitmap, compressionRect);
```



<span data-ttu-id="898b6-110">El código anterior, junto con un archivo determinado, Spiral.png, generó el siguiente resultado.</span><span class="sxs-lookup"><span data-stu-id="898b6-110">The preceding code, along with a particular file, Spiral.png, produced the following output.</span></span>

![Ilustración que muestra tres versiones de una imagen: normal, ancho ensanchado y reducido a la mitad del tamaño original](images/aboutgdip03-art06.png)

<span data-ttu-id="898b6-112">Algunas variaciones del método [**Graphics::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) tienen un parámetro de rectángulo de origen, así como un parámetro de rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="898b6-112">Some variations of the [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method have a source-rectangle parameter as well as a destination-rectangle parameter.</span></span> <span data-ttu-id="898b6-113">El rectángulo de origen especifica la parte de la imagen original que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="898b6-113">The source rectangle specifies the portion of the original image that will be drawn.</span></span> <span data-ttu-id="898b6-114">El rectángulo de destino especifica dónde se dibujará la parte de la imagen.</span><span class="sxs-lookup"><span data-stu-id="898b6-114">The destination rectangle specifies where that portion of the image will be drawn.</span></span> <span data-ttu-id="898b6-115">Si el tamaño del rectángulo de destino es diferente del tamaño del rectángulo de origen, la imagen se escala para ajustarse al rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="898b6-115">If the size of the destination rectangle is different from the size of the source rectangle, the image is scaled to fit the destination rectangle.</span></span>

<span data-ttu-id="898b6-116">En el ejemplo siguiente se crea un objeto de [**mapa de bits**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) a partir del archivo Runner.jpg.</span><span class="sxs-lookup"><span data-stu-id="898b6-116">The following example constructs a [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object from the file Runner.jpg.</span></span> <span data-ttu-id="898b6-117">Toda la imagen se dibuja sin escalar en (0,0).</span><span class="sxs-lookup"><span data-stu-id="898b6-117">The entire image is drawn with no scaling at (0, 0).</span></span> <span data-ttu-id="898b6-118">Después, una pequeña parte de la imagen se dibuja dos veces: una vez con una compresión y otra con una expansión.</span><span class="sxs-lookup"><span data-stu-id="898b6-118">Then a small portion of the image is drawn twice: once with a compression and once with an expansion.</span></span>


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



<span data-ttu-id="898b6-119">En la ilustración siguiente se muestra la imagen sin escala y las partes de la imagen comprimida y expandida.</span><span class="sxs-lookup"><span data-stu-id="898b6-119">The following illustration shows the unscaled image, and the compressed and expanded image portions.</span></span>

![captura de pantalla que muestra una imagen, una parte de la imagen comprimida y, a continuación, la misma parte expandida](images/aboutgdip03-art07.png)

 

 



