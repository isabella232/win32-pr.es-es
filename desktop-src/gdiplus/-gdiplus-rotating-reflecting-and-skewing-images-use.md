---
description: Puede girar, reflejar y sesgar una imagen especificando puntos de destino para las esquinas superior izquierda, superior derecha e inferior izquierda de la imagen original.
ms.assetid: 1e982d84-8749-451b-89a8-81440fcee439
title: Rotación, reflexión y asimetría de imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637cb8be0290d96a164042086e997bc878c0227
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248666"
---
# <a name="rotating-reflecting-and-skewing-images"></a>Rotación, reflexión y asimetría de imágenes

Puede girar, reflejar y sesgar una imagen especificando puntos de destino para las esquinas superior izquierda, superior derecha e inferior izquierda de la imagen original. Los tres puntos de destino determinan una transformación afín que asigna la imagen rectangular original a un paralelogramo. (La esquina inferior derecha de la imagen original se asigna a la cuarta esquina del paralelograma, que se calcula a partir de los tres puntos de destino especificados).

Por ejemplo, supongamos que la imagen original es un rectángulo con la esquina superior izquierda en (0, 0), la esquina superior derecha en (100, 0) y la esquina inferior izquierda en (0, 50). Ahora supongamos que asignamos esos tres puntos a los puntos de destino como se indica a continuación.



| Punto original       | Punto de destino |
|----------------------|-------------------|
| Esquina superior izquierda (0, 0)    | (200, 20)         |
| Esquina superior derecha (100, 0) | (110, 100)        |
| Inferior izquierda (0, 50)   | (250, 30)         |



 

En la ilustración siguiente se muestra la imagen original y la imagen asignada al paralelismo. La imagen original se ha sesgado, reflejado, girado y traducido. El eje x a lo largo del borde superior de la imagen original se asigna a la línea que se ejecuta a través de (200, 20) y (110, 100). El eje y a lo largo del borde izquierdo de la imagen original se asigna a la línea que se ejecuta a través de (200, 20) y (250, 30).

![ilustración que muestra franjas de color en el origen de los ejes de coordenadas y las mismas franjas sesgadas y en una ubicación, rotación y tamaño diferentes](images/stripes1.png)

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



En la ilustración siguiente se muestra una transformación similar aplicada a una imagen de fotografía.

![ilustración que muestra la misma foto dos veces; el segundo se invierte, sesga y tiene un tamaño, una rotación y una ubicación diferentes.](images/transformedclimber.png)

En la ilustración siguiente se muestra una transformación similar aplicada a un metarchivo.

![ilustración en la que se muestran formas y texto, de nuevo pero invertidos, sesgados y con una ubicación, rotación y tamaño diferentes](images/transformedmetafile.png)

 

 



