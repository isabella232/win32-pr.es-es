---
description: Windows GDI+ proporciona las clases Image y Bitmap para almacenar y manipular imágenes.
ms.assetid: fcd7f3d9-8bad-44f8-8c9c-c2f5df4a7241
title: Uso de una matriz de colores para transformar un color único
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db56d0a64c36c08a5415d76e3fb184158d473268
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474300"
---
# <a name="using-a-color-matrix-to-transform-a-single-color"></a>Uso de una matriz de colores para transformar un color único

Windows GDI+ proporciona las clases [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) y [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) para almacenar y manipular imágenes. **Los** objetos **Image y Bitmap** almacenan el color de cada píxel como un número de 32 bits: 8 bits cada uno para rojo, verde, azul y alfa. Cada uno de los cuatro componentes es un número de 0 a 255, con 0 que representa ninguna intensidad y 255 representa la intensidad completa. El componente alfa especifica la transparencia del color: 0 es totalmente transparente y 255 es totalmente opaco.

Un vector de color es una tupla de 4 de la forma (rojo, verde, azul, alfa). Por ejemplo, el vector de color (0, 255, 0, 255) representa un color opaco que no tiene rojo o azul, pero tiene verde a plena intensidad.

Otra convención para representar colores usa el número 1 para la intensidad máxima y el número 0 para la intensidad mínima. Con esa convención, el color descrito en el párrafo anterior se representaría mediante el vector (0, 1, 0, 1). GDI+ usa la convención de 1 como intensidad completa cuando realiza transformaciones de color.

Puede aplicar transformaciones lineales (rotación, escalado y otros) a vectores de color multiplicando por una matriz de 4 ×4. Sin embargo, no puede usar una matriz de 4 ×4 para realizar una traducción (no lineal). Si agrega una quinta coordenada ficticia (por ejemplo, el número 1) a cada uno de los vectores de color, puede usar una matriz de 5 ×5 para aplicar cualquier combinación de transformaciones y traducciones lineales. Una transformación que consta de una transformación lineal seguida de una traducción se denomina transformación afín. Una matriz de 5 ×5 que representa una transformación afín se denomina matriz homogénea para una transformación de 4 espacios. El elemento de la quinta fila y la quinta columna de una matriz homogénica de 5 ×5 debe ser 1 y todas las demás entradas de la quinta columna deben ser 0.

Por ejemplo, supongamos que quiere empezar con el color (0.2, 0.0, 0.4, 1.0) y aplicar las transformaciones siguientes:

1.  Duplicar el componente rojo
2.  Agregue 0,2 a los componentes rojo, verde y azul.

La siguiente multiplicación de matriz realizará el par de transformaciones en el orden indicado.

![ilustración en la que se muestra una matriz de números de 5x1 multiplicada por una matriz de 5x5 para crear una nueva matriz 5x1](images/recoloring01.png)

Los elementos de una matriz de colores se indexa (basado en cero) por fila y, a continuación, por columna. Por ejemplo, M 4 2 indica la entrada de la quinta fila y la tercera columna de la matriz \[ \] \[ \] M.

La matriz de ×5 (que se muestra en la ilustración siguiente) tiene 1s en la diagonal y 0s en cualquier otro lugar. Si multiplica un vector de color por la matriz de identidad, el vector de color no cambia. Una manera cómoda de formar la matriz de una transformación de color es comenzar con la matriz de identidad y realizar un pequeño cambio que produzca la transformación deseada.

![ilustración que muestra una matriz de identidad de 5x5; 1s en la esquina superior izquierda a diagonal inferior derecha y 0s en cualquier otro lugar](images/recoloring02.png)

Para obtener una explicación más detallada de las matrices y transformaciones, vea [Sistemas y transformaciones de coordenadas.](-gdiplus-coordinate-systems-and-transformations-about.md)

En el ejemplo siguiente se toma una imagen que es todo un color (0.2, 0.0, 0.4, 1.0) y se aplica la transformación descrita en los párrafos anteriores.


```
Image            image(L"InputColor.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   2.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.2f, 0.2f, 0.2f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10);

graphics.DrawImage(
   &image, 
   Rect(120, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



En la ilustración siguiente se muestra la imagen original a la izquierda y la imagen transformada a la derecha.

![ilustración que muestra un rectángulo relleno por un color sólido oscuro y, a continuación, uno rellenado por un color sólido más claro ](images/colortrans1.png)

El código del ejemplo anterior usa los pasos siguientes para realizar el cambio de color:

1.  Inicialice [**una estructura ColorMatrix.**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix)
2.  Cree un [**objeto ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) y pase la dirección de la estructura [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) al método [**ImageAttributes::SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) del **objeto ImageAttributes.**
3.  Pase la dirección del objeto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) al método [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) de un [**objeto Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)

 

 



