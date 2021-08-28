---
description: En el tema Using a Color Matrix to Set Alpha Values in Images (Usar una matriz de colores para establecer valores alfa en imágenes) se muestra un método no destructivo para cambiar los valores alfa de una imagen.
ms.assetid: 38c6254d-5191-4948-804a-1a4427aab7c6
title: Establecer los valores alfa de píxeles individuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c88c7ef8cc343b99f7a50c3fad012b62ef2a8d79ab38de6988efb6b5643e0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830735"
---
# <a name="setting-the-alpha-values-of-individual-pixels"></a>Establecer los valores alfa de píxeles individuales

En el tema [Using a Color Matrix to Set Alpha Values in Images](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) (Usar una matriz de colores para establecer valores alfa en imágenes) se muestra un método no destructivo para cambiar los valores alfa de una imagen. El ejemplo de ese tema representa una imagen de forma semitransparente, pero los datos de píxel del mapa de bits no cambian. Los valores alfa solo se modifican durante la representación.

En el ejemplo siguiente se muestra cómo cambiar los valores alfa de píxeles individuales. El código del ejemplo cambia realmente la información alfa en un [**objeto Bitmap.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) El enfoque es mucho más lento que usar una matriz de colores y un objeto [**ImageAttributes,**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) pero le proporciona control sobre los píxeles individuales del mapa de bits.


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

![ilustración que muestra una imagen que se vuelve más opaca de izquierda a derecha, sobre un rectángulo negro](images/image3.png)

En el ejemplo de código anterior se usan bucles anidados para cambiar el valor alfa de cada píxel del mapa de bits. Para cada píxel, [**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) obtiene el color existente, [**Color::SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) crea un color temporal que contiene el nuevo valor alfa y, a continuación, [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) establece el nuevo color. El valor alfa se establece en función de la columna del mapa de bits. En la primera columna, alpha se establece en 0. En la última columna, alpha se establece en 255. Por lo tanto, la imagen resultante va de totalmente transparente (en el borde izquierdo) a totalmente opaca (en el borde derecho).

[**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) y [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) le dan control de los valores de píxel individuales. Sin embargo, el uso de **Bitmap::GetPixel** y **Bitmap::SetPixel** no es tan rápido como usar la clase [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) y la [**estructura ColorMatrix.**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix)

 

 



