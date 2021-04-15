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
# <a name="drawing-a-line-filled-with-a-texture"></a>Dibujar una línea rellena con una textura

En lugar de dibujar una línea o una curva con un color sólido, puede dibujar con una textura. Para dibujar líneas y curvas con una textura, cree un objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) y pase la dirección de ese objeto **TextureBrush** a un constructor [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . La imagen asociada al pincel de textura se usa para colocar en mosaico el plano (de manera invisible) y cuando el lápiz dibuja una línea o una curva, el trazo del lápiz detecta determinados píxeles de la textura en mosaico.

En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo Texture1.jpg. Esa imagen se utiliza para construir un objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) y el objeto **TextureBrush** se utiliza para construir un objeto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . La llamada a [**Graphics::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) dibuja la imagen con la esquina superior izquierda en (0,0). La llamada a [**Graphics::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) usa el objeto **Pen** para dibujar una elipse con textura.


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



En la ilustración siguiente se muestra la imagen y la elipse con textura.

![Ilustración en la que se muestra una pequeña imagen rectangular, un segmento de línea elíptica rellenado con la imagen original](images/pens7.png)

 

 
