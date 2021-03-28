---
description: La reasignación es el proceso de convertir los colores de una imagen según una tabla de reasignación de colores. La tabla de reasignación de colores es una matriz de estructuras ColorMap. Cada estructura ColorMap de la matriz tiene un miembro oldColor y un miembro newColor.
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: Uso de una tabla de reasignación de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1c07bc0a67a02ea07aeaa3931e661af5665e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154215"
---
# <a name="using-a-color-remap-table"></a>Uso de una tabla de reasignación de colores

La reasignación es el proceso de convertir los colores de una imagen según una tabla de reasignación de colores. La tabla de reasignación de colores es una matriz de estructuras [**colormap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) . Cada estructura **colormap** de la matriz tiene un miembro **oldColor** y un miembro **newColor** .

Cuando GDI+ dibuja una imagen, cada píxel de la imagen se compara con la matriz de colores antiguos. Si el color de un píxel coincide con un color anterior, su color cambia al nuevo color correspondiente. Los colores se cambian solo para la representación; los valores de color de la propia imagen (almacenados en un objeto de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) o de [**mapa de bits**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) ) no cambian.

Para dibujar una imagen reasignada, inicialice una matriz de estructuras [**colormap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) . Pase la dirección de esa matriz al método [**ImageAttributes:: SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) de un objeto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) y, a continuación, pase la dirección del objeto **ImageAttributes** al método [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) Methods de un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo RemapInput.bmp. El código crea una tabla de reasignación de colores formada por una única estructura [**colormap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) . El miembro **oldColor** de la estructura **colormap** es rojo y el miembro **newColor** es Blue. La imagen se dibuja una vez sin reasignar y una vez con reasignación. El proceso de reasignación cambia todos los píxeles rojos a azul.


```
Image            image(L"RemapInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
ColorMap         colorMap[1];

colorMap[0].oldColor = Color(255, 255, 0, 0);  // opaque red
colorMap[0].newColor = Color(255, 0, 0, 255);  // opaque blue

imageAttributes.SetRemapTable(1, colorMap, ColorAdjustTypeBitmap);

graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



En la ilustración siguiente se muestra la imagen original de la izquierda y la imagen reasignada a la derecha.

![Ilustración en la que se muestran dos versiones de una imagen de multicolor: la región roja de la primera versión es azul en la segunda versión](images/colortrans7.png)

 

 



