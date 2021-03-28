---
description: Es difícil visualizar el giro en un espacio de colores de cuatro dimensiones.
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: Girar colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea322179bd4a46021d181abedd1797d6bdda7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907930"
---
# <a name="rotating-colors"></a>Girar colores

Es difícil visualizar el giro en un espacio de colores de cuatro dimensiones. Podemos facilitar la visualización de la rotación al aceptar que se ha corregido uno de los componentes de color. Supongamos que aceptamos mantener el componente alfa fijo en 1 (totalmente opaco). Después, podemos visualizar un espacio de colores tridimensional con los ejes rojo, verde y azul, como se muestra en la siguiente ilustración.

![Ilustración de una vista en perspectiva de un espacio de colores tridimensional con ejes etiquetados como rojo, verde y azul](images/recoloring03.png)

Un color puede considerarse como un punto en un espacio 3D. Por ejemplo, el punto (1,0) en el espacio representa el color rojo y el punto (0, 1, 0) en el espacio representa el color verde.

En la ilustración siguiente se muestra lo que significa girar el color (1,0) hasta un ángulo de 60 grados en el plano de Red-Green. La rotación en un plano paralelo al plano de Red-Green se puede considerar como giro sobre el eje azul.

![Ilustración que muestra el punto (1,0, 0) girado 60 grados a (0,5, 0,866, 0)](images/recoloring04.png)

En la ilustración siguiente se muestra cómo inicializar una matriz de colores para realizar giros sobre cada uno de los tres ejes de coordenadas (rojo, verde, azul).

![Ilustración en la que se muestran las matrices de colores que realizan giros sobre cada uno de los tres ejes de coordenadas](images/recoloring05.png)

En el siguiente ejemplo se toma una imagen de un color (1, 0, 0,6) y se aplica una rotación de 60 grados sobre el eje azul. El ángulo de rotación se barre en un plano paralelo al plano de Red-Green.


```
Image            image(L"RotationInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
REAL             degrees = 60;
REAL             pi = acos(-1);  // the angle whose cosine is -1.
REAL             r = degrees * pi / 180;  // degrees to radians

ColorMatrix colorMatrix = {
   cos(r),  sin(r), 0.0f, 0.0f, 0.0f,
   -sin(r), cos(r), 0.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   1.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 1.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(130, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



En la ilustración siguiente se muestra la imagen original de la izquierda y la imagen girada en color de la derecha.

![Ilustración en la que se muestran los rectángulos rellenados con la imagen original (rojo violeta) y la imagen girada en color (verde mar)](images/colortrans5.png)

La rotación de color realizada en el ejemplo de código anterior se puede visualizar como se indica a continuación.

![Ilustración que muestra un espacio de colores 3D y el punto (1,0, 0,6) girado 60 grados a (0,5, 0,866, 0,6)](images/recoloring06.png)

 

 



