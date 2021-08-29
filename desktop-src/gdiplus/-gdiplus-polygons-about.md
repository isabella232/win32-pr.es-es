---
description: Un polígono es una figura cerrada con tres o más lados rectas.
ms.assetid: f1155341-83f3-4805-8d42-a1910515db31
title: Polígonos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bf1f8a2b9b3ce30ceadb22a0832ec50fed98c87eba961081760e5a966932e4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036463"
---
# <a name="polygons"></a>Polígonos

Un polígono es una figura cerrada con tres o más lados rectas. Por ejemplo, un triángulo es un polígono con tres lados, un rectángulo es un polígono con cuatro lados y un rectángulo es un polígono con cinco lados. En la ilustración siguiente se muestran varios polígonos.

![ilustración que muestra cinco polígonos de diferentes formas, tamaños y colores](images/aboutgdip02-art07.png)

Para dibujar un polígono, necesita un objeto [**Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) un [**objeto Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) y una matriz de objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (o [**PointF).**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) El **objeto Graphics** proporciona el método [DrawPolygon.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) El **objeto Pen** almacena los atributos del polígono, como el ancho de línea y el color, y la matriz de objetos **Point** almacena los puntos que se conectarán mediante líneas rectas. Las direcciones del objeto **Pen** y la matriz de **objetos Point** se pasan como argumentos al método DrawPolygon. En el ejemplo siguiente se dibuja un polígono de tres lados. Tenga en cuenta que solo hay tres puntos en **myPointArray:**(0, 0), (50, 30) y (30, 60). El método DrawPolygon cierra automáticamente el polígono dibujando una línea de (30, 60) al punto inicial (0, 0);


```
Point myPointArray[] =
   {Point(0, 0), Point(50, 30), Point(30, 60)};
myGraphics.DrawPolygon(&myPen, myPointArray, 3);
```



En la ilustración siguiente se muestra el polígono.

![ilustración en la que se muestra un triángulo con ejes de coordenadas](images/aboutgdip02-art08.png)

 

 



