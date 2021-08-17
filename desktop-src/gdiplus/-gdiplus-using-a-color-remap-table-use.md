---
description: Reasignar es el proceso de convertir los colores de una imagen según una tabla de reasignación de colores. La tabla de reasignación de colores es una matriz de estructuras ColorMap. Cada estructura ColorMap de la matriz tiene un miembro oldColor y un miembro newColor.
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: Uso de una tabla de reasignación de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00f36c493bbdc696fa672b2899d4d7c6d3231a9e40c0e4162b5113d78a67164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036303"
---
# <a name="using-a-color-remap-table"></a>Uso de una tabla de reasignación de colores

Reasignar es el proceso de convertir los colores de una imagen según una tabla de reasignación de colores. La tabla de reasignación de colores es una matriz de [**estructuras ColorMap.**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) Cada **estructura ColorMap** de la matriz tiene un **miembro oldColor** y un **miembro newColor.**

Cuando GDI+ dibuja una imagen, cada píxel de la imagen se compara con la matriz de colores antiguos. Si el color de un píxel coincide con un color antiguo, su color cambia al nuevo color correspondiente. Los colores solo se cambian para la representación: los valores de color de la propia imagen (almacenados en un objeto [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) o [**Bitmap)**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) no se cambian.

Para dibujar una imagen reasignada, inicialice una matriz de [**estructuras ColorMap.**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) Pase la dirección de esa matriz al método [**ImageAttributes::SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) de un objeto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) y, a continuación, pase la dirección del objeto **ImageAttributes** al método [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) de un objeto [**Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)

En el ejemplo siguiente se crea [**un objeto Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo RemapInput.bmp. El código crea una tabla de reasignación de colores que consta de una sola [**estructura ColorMap.**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) El **miembro oldColor** de la **estructura ColorMap** es rojo y el **miembro newColor** es azul. La imagen se dibuja una vez sin remapping y otra con remapping. El proceso de remapping cambia todos los píxeles rojos a azul.


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



En la ilustración siguiente se muestra la imagen original a la izquierda y la imagen rematada a la derecha.

![ilustración en la que se muestran dos versiones de una imagen de color de color negro; la región roja de la primera versión es azul en la segunda versión.](images/colortrans7.png)

 

 



