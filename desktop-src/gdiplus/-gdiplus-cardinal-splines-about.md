---
description: Una curva spline cardinal es una secuencia de curvas individuales Unidas para formar una curva mayor.
ms.assetid: 4fc62f00-7006-4ade-bfcc-091a3a97d889
title: Curvas spline cardinales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d85c0163e405a6f9346f521b4057eb936108cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276415"
---
# <a name="cardinal-splines"></a>Curvas spline cardinales

Una curva spline cardinal es una secuencia de curvas individuales Unidas para formar una curva mayor. La spline se especifica mediante una matriz de puntos y un parámetro de tensión. Una curva spline cardinal pasa sin problemas a través de cada punto de la matriz; no hay esquinas nítidas ni cambios bruscos en el grado de apriete de la curva. En la ilustración siguiente se muestra un conjunto de puntos y una curva spline cardinal que atraviesa cada punto del conjunto.

![Ilustración que muestra una curva spline cardinal que pasa por seis puntos definidos](images/aboutgdip02-art09.gif)

Una spline física es una pieza fina de madera u otro material flexible. Antes de la llegada de las curvas spline matemáticas, los diseñadores usaban curvas spline físicas para dibujar curvas. Un diseñador colocaría la curva spline en una pieza de papel y la delimitaría a un conjunto determinado de puntos. A continuación, el diseñador puede crear una curva dibujando a lo largo de la curva spline con un lápiz. Un conjunto determinado de puntos podría producir una variedad de curvas, dependiendo de las propiedades de la spline física. Por ejemplo, una spline con una resistencia alta para doblar produciría una curva diferente de una spline extremadamente flexible.

Las fórmulas para las curvas spline matemáticas se basan en las propiedades de las varillas flexibles, por lo que las curvas producidas por las curvas spline matemáticas son similares a las curvas que fueron creadas por las curvas spline físicas. Del mismo modo que las curvas spline físicas de una tensión diferente producirán curvas diferentes a través de un conjunto determinado de puntos, las curvas spline matemáticas con valores diferentes para el parámetro de tensión producirán curvas diferentes a través de un conjunto determinado de puntos. En la ilustración siguiente se muestran cuatro curvas spline cardinales que pasan por el mismo conjunto de puntos. La tensión se muestra para cada spline. Tenga en cuenta que una tensión de 0 corresponde a una tensión física infinita, lo que obliga a que la curva adopte la forma más corta (líneas rectas) entre los puntos. Una tensión de 1 corresponde a ninguna tensión física, lo que permite que la spline tome el trazado de la curva menos total. Con valores de tensión mayores que 1, la curva se comporta como un muelle comprimido, insertado para tomar una ruta de acceso más larga.

![Ilustración que muestra cuatro curvas spline cardinales a través de los mismos tres puntos](images/aboutgdip02-art10.gif)

Tenga en cuenta que las cuatro curvas spline de la ilustración anterior comparten la misma línea tangente en el punto inicial. La tangente es la línea que se dibuja desde el punto inicial hasta el siguiente punto a lo largo de la curva. Del mismo modo, la tangente compartida en el punto final es la línea que se dibuja desde el punto final hasta el punto anterior de la curva.

Para dibujar una curva spline cardinal, se necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) y una matriz de objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) . El objeto **Graphics** proporciona el método [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpointf_inint_inreal)) , que dibuja la spline, y el objeto **Pen** almacena los atributos de la spline, como el ancho y el color de la línea. La matriz de objetos **Point** almacena los puntos a través de los que pasará la curva. En el ejemplo siguiente se dibuja una curva spline cardinal que pasa a través de los puntos de *myPointArray*. El tercer parámetro es la tensión.


```
myGraphics.DrawCurve(&myPen, myPointArray, 3, 1.5f);
```



 

 



