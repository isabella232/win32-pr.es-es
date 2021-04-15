---
description: En lugar de dibujar una línea o una curva con un color sólido, puede dibujar con una textura.
ms.assetid: 326170a5-d21f-49d6-9f60-10b9bc8d97b4
title: Dibujar una línea rellena con una textura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6a061399791009fd7c1b645bb09dbba25362f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985186"
---
# <a name="drawing-a-line-filled-with-a-texture"></a><span data-ttu-id="15d45-103">Dibujar una línea rellena con una textura</span><span class="sxs-lookup"><span data-stu-id="15d45-103">Drawing a Line Filled with a Texture</span></span>

<span data-ttu-id="15d45-104">En lugar de dibujar una línea o una curva con un color sólido, puede dibujar con una textura.</span><span class="sxs-lookup"><span data-stu-id="15d45-104">Instead of drawing a line or curve with a solid color, you can draw with a texture.</span></span> <span data-ttu-id="15d45-105">Para dibujar líneas y curvas con una textura, cree un objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) y pase la dirección de ese objeto **TextureBrush** a un constructor [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="15d45-105">To draw lines and curves with a texture, create a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, and pass the address of that **TextureBrush** object to a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor.</span></span> <span data-ttu-id="15d45-106">La imagen asociada al pincel de textura se usa para colocar en mosaico el plano (de manera invisible) y cuando el lápiz dibuja una línea o una curva, el trazo del lápiz detecta determinados píxeles de la textura en mosaico.</span><span class="sxs-lookup"><span data-stu-id="15d45-106">The image associated with the texture brush is used to tile the plane (invisibly), and when the pen draws a line or curve, the stroke of the pen uncovers certain pixels of the tiled texture.</span></span>

<span data-ttu-id="15d45-107">En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo Texture1.jpg.</span><span class="sxs-lookup"><span data-stu-id="15d45-107">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Texture1.jpg.</span></span> <span data-ttu-id="15d45-108">Esa imagen se utiliza para construir un objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) y el objeto **TextureBrush** se utiliza para construir un objeto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="15d45-108">That image is used to construct a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, and the **TextureBrush** object is used to construct a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="15d45-109">La llamada a [**Graphics::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) dibuja la imagen con la esquina superior izquierda en (0,0).</span><span class="sxs-lookup"><span data-stu-id="15d45-109">The call to [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) draws the image with its upper-left corner at (0, 0).</span></span> <span data-ttu-id="15d45-110">La llamada a [**Graphics::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) usa el objeto **Pen** para dibujar una elipse con textura.</span><span class="sxs-lookup"><span data-stu-id="15d45-110">The call to [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) uses the **Pen** object to draw a textured ellipse.</span></span>


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



<span data-ttu-id="15d45-111">En la ilustración siguiente se muestra la imagen y la elipse con textura.</span><span class="sxs-lookup"><span data-stu-id="15d45-111">The following illustration shows the image and the textured ellipse.</span></span>

![Ilustración en la que se muestra una pequeña imagen rectangular, un segmento de línea elíptica rellenado con la imagen original](images/pens7.png)

 

 
