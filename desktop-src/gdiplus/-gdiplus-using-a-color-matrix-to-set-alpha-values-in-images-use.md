---
description: La clase Bitmap (que hereda de la clase Image) y la clase ImageAttributes proporcionan funcionalidad para obtener y establecer valores de píxel.
ms.assetid: e3d67431-6098-4b2a-8910-5695a8473216
title: Uso una matriz de colores para establecer valores alfa en imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81180b1f09b11e37b322e37106dab1879a00bbdb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474301"
---
# <a name="using-a-color-matrix-to-set-alpha-values-in-images"></a>Uso una matriz de colores para establecer valores alfa en imágenes

La [**clase Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) (que hereda de la clase [**Image)**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) y la clase [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) proporcionan funcionalidad para obtener y establecer valores de píxel. Puede usar la clase **ImageAttributes** para modificar los valores alfa de una imagen completa, o bien puede llamar al método [**Bitmap::SetPixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) de la clase **Bitmap** para modificar valores de píxel individuales. Para obtener más información sobre cómo establecer valores de píxeles individuales, vea [Establecer los valores alfa de píxeles individuales.](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

En el ejemplo siguiente se dibuja una línea negra ancha y, a continuación, se muestra una imagen opaca que cubre parte de esa línea.


```
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw an image that covers part of the black line.
graphics.DrawImage(&bitmap,
   Rect(30, 0, bitmap.GetWidth(), bitmap.GetHeight()));
```



En la ilustración siguiente se muestra la imagen resultante, que se dibuja en (30, 0). Tenga en cuenta que la línea negra ancha no se muestra a través de la imagen.

![ilustración en la que se muestra una imagen opaca superpuesta a un rectángulo fino, ancho y negro](images/image1.png)

La [**clase ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) tiene muchas propiedades que puede usar para modificar imágenes durante la representación. En el ejemplo siguiente, se **usa un objeto ImageAttributes** para establecer todos los valores alfa en el 80 por ciento de lo que eran. Para ello, inicializa una matriz de colores y establece el valor de escalado alfa de la matriz en 0,8. La dirección de la matriz de colores se pasa al método [**ImageAttributes::SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) del objeto **ImageAttributes** y la dirección del objeto **ImageAttributes** se pasa al método [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) de un objeto [**Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)


```
// Create a Bitmap object and load it with the texture image.
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// Initialize the color matrix.
// Notice the value 0.8 in row 4, column 4.
ColorMatrix colorMatrix = {1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.8f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
// Create an ImageAttributes object and set its color matrix.
ImageAttributes imageAtt;
imageAtt.SetColorMatrix(&colorMatrix, ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw the semitransparent bitmap image.
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
graphics.DrawImage(
   &bitmap, 
   Rect(30, 0, iWidth, iHeight),  // Destination rectangle
   0,                             // Source rectangle X 
   0,                             // Source rectangle Y
   iWidth,                        // Source rectangle width
   iHeight,                       // Source rectangle height
   UnitPixel, 
   &imageAtt);
```



Durante la representación, los valores alfa del mapa de bits se convierten al 80 por ciento de lo que eran. Esto da como resultado una imagen que se combina con el fondo. Como se muestra en la ilustración siguiente, la imagen de mapa de bits tiene un aspecto transparente; puede ver la línea negra sólida a través de ella.

![ilustración similar a la anterior, pero la imagen es transparente sem](images/image2.png)

Cuando la imagen está sobre la parte blanca del fondo, la imagen se ha combinado con el color blanco. Cuando la imagen cruza la línea negra, la imagen se combina con el color negro.

 

 



