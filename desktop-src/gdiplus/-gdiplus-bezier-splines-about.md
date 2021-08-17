---
description: 'Una curva spline B&233;zier es una curva especificada por cuatro puntos: dos puntos finales (p1 y p2) y dos puntos de \# control (c1 y c2).'
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: Curvas spline de Bézier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bcc9c56baa9cd1b3e93187ef00f9d6a2c8c1d218262c946028ed70429de18d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119399575"
---
# <a name="bezier-splines"></a>Curvas spline de Bézier

Una curva spline de Bézier es una curva especificada por cuatro puntos: dos puntos finales (p1 y p2) y dos puntos de control (c1 y c2). La curva comienza en p1 y termina en p2. La curva no pasa a través de los puntos de control, pero los puntos de control actúan como ómanos, extrayendo la curva en determinadas direcciones e influyendo en la forma en que la curva se curva. En la ilustración siguiente se muestra una curva de Bézier junto con sus puntos de conexión y de control.

![ilustración que muestra una curva spline bézier con dos puntos de conexión y dos puntos de control](images/aboutgdip02-art11a.png)

Tenga en cuenta que la curva comienza en p1 y se desplaza hacia el punto de control c1. La línea tangente a la curva en p1 es la línea dibujada de p1 a c1. Tenga en cuenta también que la línea tangente en el punto de conexión p2 es la línea dibujada de c2 a p2.

Para dibujar una curva spline de Bézier, necesita un [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un [**objeto Pen.**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) El **objeto Graphics** proporciona el método [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) y el **objeto Pen** almacena los atributos de la curva, como el ancho de línea y el color. La dirección del **objeto Pen** se pasa como uno de los argumentos al método DrawBezier. Los argumentos restantes pasados al método DrawBezier son los puntos de conexión y los puntos de control. En el ejemplo siguiente se dibuja una curva spline de Bézier con punto inicial (0, 0), puntos de control (40, 20) y (80, 150) y punto final (100, 10).


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



En la ilustración siguiente se muestra la curva, los puntos de control y dos líneas tangentes.

![ilustración que muestra una curva spline bézier con dos puntos de conexión, dos puntos de control y dos líneas tangentes](images/aboutgdip02-art12.png)

Las curvas spline de Bézier fueron desarrolladas originalmente por Pierre Bézier para su diseño en el sector de la automoción. Desde entonces, han demostrado ser muy útiles en muchos tipos de diseño asistido por pc y también se usan para definir los contornos de las fuentes. Las curvas spline de Bézier pueden producir una amplia variedad de formas, algunas de las cuales se muestran en la ilustración siguiente.

![ilustración que muestra tres curvas spline bézier](images/aboutgdip02-art13.png)

 

 



