---
description: Puede girar, reflejar y sesgar una imagen especificando los puntos de destino de las esquinas superior izquierda, superior derecha e inferior izquierda de la imagen original.
ms.assetid: 1e982d84-8749-451b-89a8-81440fcee439
title: Girar, reflejar y sesgar imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637cb8be0290d96a164042086e997bc878c0227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001660"
---
# <a name="rotating-reflecting-and-skewing-images"></a>Girar, reflejar y sesgar imágenes

Puede girar, reflejar y sesgar una imagen especificando los puntos de destino de las esquinas superior izquierda, superior derecha e inferior izquierda de la imagen original. Los tres puntos de destino determinan una transformación afín que asigna la imagen rectangular original a un paralelogramo. (La esquina inferior derecha de la imagen original se asigna a la cuarta esquina del paralelogramo, que se calcula a partir de los tres puntos de destino especificados).

Por ejemplo, supongamos que la imagen original es un rectángulo con la esquina superior izquierda en (0,0), la esquina superior derecha en (100, 0) y la esquina inferior izquierda en (0, 50). Ahora Supongamos que asignamos esos tres puntos a los puntos de destino como se indica a continuación.



| Punto original       | Punto de destino |
|----------------------|-------------------|
| Superior izquierda (0,0)    | (200, 20)         |
| Superior derecha (100) | (110, 100)        |
| Inferior izquierda (0, 50)   | (250, 30)         |



 

En la ilustración siguiente se muestra la imagen original y la imagen asignada al paralelogramo. La imagen original se ha sesgado, reflejado, girado y traducido. El eje x a lo largo del borde superior de la imagen original se asigna a la línea que se ejecuta a través de (200, 20) y (110, 100). El eje y a lo largo del borde izquierdo de la imagen original se asigna a la línea que se ejecuta a través de (200, 20) y (250, 30).

![Ilustración en la que se muestran las franjas en color en el origen de los ejes de coordenadas y las mismas franjas sesgadas y en una ubicación, rotación y tamaño diferentes](images/stripes1.png)

En el ejemplo siguiente se generan las imágenes que se muestran en la ilustración anterior.


```
Point destinationPoints[] = {
   Point(200, 20),   // destination for upper-left point of original
   Point(110, 100),  // destination for upper-right point of original
   Point(250, 30)};  // destination for lower-left point of original
Image image(L"Stripes.bmp");
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw the image mapped to the parallelogram.
graphics.DrawImage(&image, destinationPoints, 3); 
```



En la ilustración siguiente se muestra una transformación similar que se aplica a una imagen fotográfica.

![Ilustración en la que se muestra la misma foto dos veces; la segunda se revierte, sesga y tiene un tamaño, una rotación y una ubicación diferentes](images/transformedclimber.png)

En la ilustración siguiente se muestra una transformación similar que se aplica a un metarchivo.

![Ilustración en la que se muestran formas y texto, pero de nuevo, pero se revierten, se sesgan y con una ubicación, una rotación y un tamaño diferentes.](images/transformedmetafile.png)

 

 



