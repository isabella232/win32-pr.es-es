---
description: El tema uso de una matriz de colores para establecer valores alfa en imágenes muestra un método no destructivo para cambiar los valores alfa de una imagen.
ms.assetid: 38c6254d-5191-4948-804a-1a4427aab7c6
title: Establecer los valores alfa de píxeles individuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cd45bf32284ffc9a8cef13f368cff59e1e8a74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541454"
---
# <a name="setting-the-alpha-values-of-individual-pixels"></a>Establecer los valores alfa de píxeles individuales

El tema [uso de una matriz de colores para establecer valores alfa en imágenes](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) muestra un método no destructivo para cambiar los valores alfa de una imagen. En el ejemplo de ese tema se representa una imagen de forma semitransparente, pero los datos de píxeles del mapa de bits no cambian. Los valores alfa solo se modifican durante la representación.

En el ejemplo siguiente se muestra cómo cambiar los valores alfa de píxeles individuales. En realidad, el código del ejemplo cambia la información alfa de un objeto de [**mapa de bits**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) . El enfoque es mucho más lento que el uso de una matriz de colores y un objeto [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , pero proporciona control sobre los píxeles individuales del mapa de bits.


```
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
Color color, colorTemp;
for(INT iRow = 0; iRow < iHeight; iRow++)
{
   for(INT iColumn = 0; iColumn < iWidth; iColumn++)
   {
      bitmap.GetPixel(iColumn, iRow, &color);
      colorTemp.SetValue(color.MakeARGB(
         (BYTE)(255 * iColumn / iWidth), 
         color.GetRed(),
         color.GetGreen(),
         color.GetBlue()));
      bitmap.SetPixel(iColumn, iRow, colorTemp);
   }
}
// First draw a wide black line.
Pen pen(Color(255, 0, 0, 0), 25);
graphics.DrawLine(&pen, 10, 35, 200, 35);
// Now draw the modified bitmap.
graphics.DrawImage(&bitmap, 30, 0, iWidth, iHeight);
```



En la ilustración siguiente se muestra la imagen resultante.

![Ilustración en la que se muestra una imagen más opaca de izquierda a derecha, sobre un rectángulo negro](images/image3.png)

En el ejemplo de código anterior se usan bucles anidados para cambiar el valor alfa de cada píxel del mapa de bits. Para cada píxel, [**Bitmap:: getPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) obtiene el color existente, [**color:: SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) crea un color temporal que contiene el nuevo valor alfa y [**Bitmap:: setPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) establece el nuevo color. El valor alfa se establece basándose en la columna del mapa de bits. En la primera columna, alfa se establece en 0. En la última columna, alfa se establece en 255. Por lo tanto, la imagen resultante pasa de ser completamente transparente (en el borde izquierdo) a totalmente opaca (en el borde derecho).

[**Bitmap:: getPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) y [**Bitmap:: setPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) proporcionan el control de los valores individuales de los píxeles. Sin embargo, el uso de **Bitmap:: getPixel** y **Bitmap:: setPixel** no es casi tan rápido como el uso de la clase [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) y la estructura [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .

 

 



