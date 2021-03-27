---
description: 'Una \# curva spline de bézier&233; es una curva especificada por cuatro puntos: dos extremos (P1 y P2) y dos puntos de control (C1 y C2).'
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: Curvas spline de Bézier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd725e64f9ba0035849d2d1d6fbc03d5efa0b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156232"
---
# <a name="bezier-splines"></a>Curvas spline de Bézier

Una curva spline de Bézier es una curva especificada por cuatro puntos: dos puntos finales (P1 y P2) y dos puntos de control (C1 y C2). La curva comienza en P1 y termina en P2. La curva no pasa a través de los puntos de control, pero los puntos de control actúan como imanes, extrayendo la curva en determinadas direcciones e influindo en la forma en que se dobla la curva. En la ilustración siguiente se muestra una curva de Bézier junto con sus extremos y puntos de control.

![Ilustración en la que se muestra una curva spline Bézier con dos puntos finales y dos puntos de control](images/aboutgdip02-art11a.png)

Tenga en cuenta que la curva comienza en P1 y se desplaza hacia el punto de control C1. La línea tangente a la curva en P1 es la línea que se dibuja de P1 a C1. Tenga en cuenta también que la línea tangente en el extremo P2 es la línea dibujada de C2 a P2.

Para dibujar una curva spline de Bézier, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . El objeto **Graphics** proporciona el método [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) y el objeto **Pen** almacena atributos de la curva, como el color y el ancho de línea. La dirección del objeto **Pen** se pasa como uno de los argumentos al método DrawBezier. Los argumentos restantes que se pasan al método DrawBezier son los extremos y los puntos de control. En el ejemplo siguiente se dibuja una curva spline de Bézier con el punto inicial (0,0), los puntos de control (40, 20) y (80, 150) y el punto final (100, 10).


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



En la ilustración siguiente se muestra la curva, los puntos de control y dos líneas tangentes.

![Ilustración que muestra una curva spline Bézier con dos puntos finales, dos puntos de control y dos líneas tangentes](images/aboutgdip02-art12.png)

Las curvas spline de Bézier fueron desarrolladas originalmente por Pierre Bézier para el diseño en la industria del automóvil. Ya han demostrado ser muy útiles en muchos tipos de diseño asistido por PC y también se usan para definir los contornos de las fuentes. Las curvas spline de Bézier pueden producir una gran variedad de formas, algunas de las cuales se muestran en la ilustración siguiente.

![Ilustración que muestra tres curvas spline de Bézier](images/aboutgdip02-art13.png)

 

 



