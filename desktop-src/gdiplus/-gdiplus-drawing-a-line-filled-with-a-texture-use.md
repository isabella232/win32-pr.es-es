---
description: En lugar de dibujar una línea o curva con un color sólido, puede dibujar con una textura.
ms.assetid: 326170a5-d21f-49d6-9f60-10b9bc8d97b4
title: Dibujar una línea rellena con una textura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13cc8f93adee4792836c4166d5787e20d9c54040448d3a7efde36ff6a580d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467045"
---
# <a name="drawing-a-line-filled-with-a-texture"></a>Dibujar una línea rellena con una textura

En lugar de dibujar una línea o curva con un color sólido, puede dibujar con una textura. Para dibujar líneas y curvas con una textura, cree un objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) y pase la dirección de ese objeto **TextureBrush** a un constructor [**Pen.**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) La imagen asociada al pincel de textura se usa para crear mosaicos en el plano (de forma invisible) y, cuando el lápiz dibuja una línea o curva, el trazo del lápiz descubre ciertos píxeles de la textura en mosaico.

En el ejemplo siguiente se crea [**un objeto Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo Texture1.jpg. Esa imagen se usa para construir un [**objeto TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) y el objeto **TextureBrush** se usa para construir un [**objeto Pen.**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) La llamada a [**Graphics::D rawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) dibuja la imagen con su esquina superior izquierda en (0, 0). La llamada a [**Graphics::D rawFormatpse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) usa el **objeto Pen** para dibujar una elipse con textura.


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



En la ilustración siguiente se muestra la imagen y la elipse con textura.

![ilustración en la que se muestra una imagen rectangular pequeña y, a continuación, un segmento de línea elíptico relleno con la imagen original](images/pens7.png)

 

 
