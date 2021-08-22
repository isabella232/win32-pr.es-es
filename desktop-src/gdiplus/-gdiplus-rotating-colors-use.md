---
description: La rotación en un espacio de colores de cuatro dimensiones es difícil de visualizar.
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: Rotación de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc09a84c4c51181c672c549369783ac476fa1d3c79f1598c1c29ca14604429d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036433"
---
# <a name="rotating-colors"></a>Rotación de colores

La rotación en un espacio de colores de cuatro dimensiones es difícil de visualizar. Podemos facilitar la visualización de la rotación aceptando mantener uno de los componentes de color fijos. Supongamos que aceptamos mantener el componente alfa fijo en 1 (totalmente opaco). A continuación, podemos visualizar un espacio de colores tridimensional con ejes rojo, verde y azul, como se muestra en la ilustración siguiente.

![ilustración de una vista de perspectiva de un espacio de colores tridimensional con ejes etiquetados como rojo, verde y azul](images/recoloring03.png)

Un color se puede pensar como un punto en el espacio 3D. Por ejemplo, el punto (1, 0, 0) del espacio representa el color rojo y el punto (0, 1, 0) del espacio representa el color verde.

En la ilustración siguiente se muestra lo que significa girar el color (1, 0, 0) a través de un ángulo de 60 grados en el Red-Green plano. La rotación en un plano paralelo al plano Red-Green se puede pensar en una rotación sobre el eje azul.

![ilustración que muestra el punto (1, 0, 0) girado 60 grados a (0,5, 0,866, 0)](images/recoloring04.png)

En la ilustración siguiente se muestra cómo inicializar una matriz de colores para realizar rotaciones sobre cada uno de los tres ejes de coordenadas (rojo, verde, azul).

![ilustración que muestra matrices de colores que realizan rotaciones sobre cada uno de los tres ejes de coordenadas](images/recoloring05.png)

En el ejemplo siguiente se toma una imagen que es todo un color (1, 0, 0,6) y se aplica una rotación de 60 grados sobre el eje azul. El ángulo de la rotación se arrastra en un plano que es paralelo al Red-Green rotación.


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



En la ilustración siguiente se muestra la imagen original a la izquierda y la imagen girada por colores a la derecha.

![ilustración en la que se muestran rectángulos rellenos con la imagen original (rojo pico) e imagen girada por colores (verde del mar)](images/colortrans5.png)

La rotación de colores realizada en el ejemplo de código anterior se puede visualizar como se muestra a continuación.

![ilustración que muestra un espacio de color 3d y el punto (1, 0, 0,6) giraba 60 grados a (0,5, 0,866, 0,6)](images/recoloring06.png)

 

 



