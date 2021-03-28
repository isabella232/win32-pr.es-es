---
description: Windows GDI+ proporciona las clases Image y Bitmap para almacenar y manipular imágenes.
ms.assetid: fcd7f3d9-8bad-44f8-8c9c-c2f5df4a7241
title: Uso de una matriz de colores para transformar un color único
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db56d0a64c36c08a5415d76e3fb184158d473268
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557670"
---
# <a name="using-a-color-matrix-to-transform-a-single-color"></a>Uso de una matriz de colores para transformar un color único

Windows GDI+ proporciona las clases [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) y [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) para almacenar y manipular imágenes. Los objetos **Image** y **Bitmap** almacenan el color de cada píxel como un número de 32 bits: 8 bits para rojo, verde, azul y alfa. Cada uno de los cuatro componentes es un número del 0 al 255, con 0 que no representa ninguna intensidad y 255 que representa intensidad total. El componente alfa especifica la transparencia del color: 0 es totalmente transparente y 255 es totalmente opaco.

Un vector de color es una tupla de 4 de la forma (rojo, verde, azul, alfa). Por ejemplo, el vector de color (0, 255, 0, 255) representa un color opaco que no tiene rojo o azul, pero tiene una intensidad de color verde.

Otra Convención para representar colores utiliza el número 1 para la intensidad máxima y el número 0 para la intensidad mínima. Con esa Convención, el color descrito en el párrafo anterior se representaría mediante el vector (0, 1, 0, 1). GDI+ utiliza la Convención de 1 como intensidad completa cuando realiza transformaciones de color.

Puede aplicar transformaciones lineales (giro, escala y similares) a vectores de color multiplicando por una matriz de 4 x 4. Sin embargo, no puede usar una matriz de 4 × 4 para realizar una traducción (no lineal). Si agrega una quinta coordenada ficticia (por ejemplo, el número 1) a cada uno de los vectores de color, puede utilizar una matriz de 5 × 5 para aplicar cualquier combinación de transformaciones lineales y traducciones. Una transformación formada por una transformación lineal seguida de una traducción se denomina transformación afín. Una matriz de 5 × 5 que representa una transformación afín se denomina matriz homogénea para una transformación de 4 espacios. El elemento de la quinta fila y la quinta columna de una matriz homogénea 5 × 5 deben ser 1 y todas las demás entradas de la quinta columna deben ser 0.

Por ejemplo, supongamos que desea empezar con el color (0,2, 0,0, 0,4, 1,0) y aplicar las transformaciones siguientes:

1.  Doble del componente rojo
2.  Agregar 0,2 a los componentes rojo, verde y azul

La multiplicación de matrices siguiente realizará el par de transformaciones en el orden mostrado.

![Ilustración en la que se muestra una matriz 5x1 de números multiplicada por una matriz 5x5 para crear una nueva matriz 5x1](images/recoloring01.png)

Los elementos de una matriz de colores se indexan (de base cero) por fila y después por columna. Por ejemplo, la entrada de la quinta fila y la tercera columna de la matriz M se indican mediante M \[ 4 \] \[ 2 \] .

La matriz de identidad 5 × 5 (que se muestra en la ilustración siguiente) tiene un 1 en la diagonal y 0s en cualquier otro lugar. Si multiplica un vector de color por la matriz de identidad, el vector de color no cambia. Una manera cómoda de formar la matriz de una transformación de color es comenzar con la matriz de identidad y hacer un pequeño cambio que genere la transformación deseada.

![Ilustración que muestra una matriz de identidad 5x5; 1S en la parte superior izquierda a la diagonal inferior derecha y 0s en cualquier otro lugar](images/recoloring02.png)

Para obtener una explicación más detallada de las matrices y las transformaciones, vea [sistemas de coordenadas y transformaciones](-gdiplus-coordinate-systems-and-transformations-about.md).

En el siguiente ejemplo se toma una imagen de un color (0,2, 0,0, 0,4, 1,0) y se aplica la transformación descrita en los párrafos anteriores.


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



En la ilustración siguiente se muestra la imagen original de la izquierda y la imagen transformada a la derecha.

![Ilustración que muestra un rectángulo relleno con un color sólido oscuro y, a continuación, un relleno con un color sólido más claro ](images/colortrans1.png)

En el código del ejemplo anterior se usan los pasos siguientes para realizar el recoloreado:

1.  Inicialice una estructura [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .
2.  Cree un objeto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) y pase la dirección de la estructura [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) al método [**ImageAttributes:: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) del objeto **ImageAttributes** .
3.  Pase la dirección del objeto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) al método [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) Methods de un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

 

 



