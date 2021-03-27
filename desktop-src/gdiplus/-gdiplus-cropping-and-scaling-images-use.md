---
title: Recortar y escalar imágenes GDI+
description: La clase Graphics proporciona varios métodos DrawImage, algunos de los cuales tienen parámetros de rectángulo de origen y de destino que puede usar para recortar y escalar imágenes.
ms.assetid: cad64615-d8e6-4c03-a6c7-c98267a8f159
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c70a7b4f7aa0374602326ab856a01bbadc0047
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988283"
---
# <a name="cropping-and-scaling-gdi-images"></a><span data-ttu-id="87f9f-103">Recortar y escalar imágenes GDI+</span><span class="sxs-lookup"><span data-stu-id="87f9f-103">Cropping and scaling GDI+ images</span></span>

<span data-ttu-id="87f9f-104">La clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) proporciona varios métodos **DrawImage** , algunos de los cuales tienen parámetros de rectángulo de origen y de destino que puede usar para recortar y escalar imágenes.</span><span class="sxs-lookup"><span data-stu-id="87f9f-104">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides several **DrawImage** methods, some of which have source and destination rectangle parameters that you can use to crop and scale images.</span></span>

<span data-ttu-id="87f9f-105">En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo Apple.gif.</span><span class="sxs-lookup"><span data-stu-id="87f9f-105">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Apple.gif.</span></span> <span data-ttu-id="87f9f-106">El código dibuja toda la imagen de Apple en su tamaño original.</span><span class="sxs-lookup"><span data-stu-id="87f9f-106">The code draws the entire apple image in its original size.</span></span> <span data-ttu-id="87f9f-107">A continuación, el código llama al método **DrawImage** de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para dibujar una parte de la imagen de Apple en un rectángulo de destino mayor que la imagen de Apple original.</span><span class="sxs-lookup"><span data-stu-id="87f9f-107">The code then calls the **DrawImage** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object to draw a portion of the apple image in a destination rectangle that is larger than the original apple image.</span></span>

<span data-ttu-id="87f9f-108">El método **DrawImage** determina qué parte de la manzana se dibuja examinando el rectángulo de origen, que se especifica mediante los argumentos tercero, cuarto, quinto y sexto.</span><span class="sxs-lookup"><span data-stu-id="87f9f-108">The **DrawImage** method determines which portion of the apple to draw by looking at the source rectangle, which is specified by the third, fourth, fifth, and sixth arguments.</span></span> <span data-ttu-id="87f9f-109">En este caso, la manzana se recorta al 75 por ciento de su ancho y 75 por ciento de su alto.</span><span class="sxs-lookup"><span data-stu-id="87f9f-109">In this case, the apple is cropped to 75 percent of its width and 75 percent of its height.</span></span>

<span data-ttu-id="87f9f-110">El método **DrawImage** determina dónde se debe dibujar la manzana recortada y el tamaño de la manzana recortada examinando el rectángulo de destino, que se especifica mediante el segundo argumento.</span><span class="sxs-lookup"><span data-stu-id="87f9f-110">The **DrawImage** method determines where to draw the cropped apple and how big to make the cropped apple by looking at the destination rectangle, which is specified by the second argument.</span></span> <span data-ttu-id="87f9f-111">En este caso, el rectángulo de destino es un 30 por ciento más amplio y un 30 por ciento más alto que la imagen original.</span><span class="sxs-lookup"><span data-stu-id="87f9f-111">In this case, the destination rectangle is 30 percent wider and 30 percent taller than the original image.</span></span>


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



<span data-ttu-id="87f9f-112">En la ilustración siguiente se muestra la manzana original y la manzana recortada y escalada.</span><span class="sxs-lookup"><span data-stu-id="87f9f-112">The following illustration shows the original apple and the scaled, cropped apple.</span></span>

![Ilustración en la que se muestra una manzana y después una parte ampliada de la manzana original](images/cropscale1.png)

 

 



