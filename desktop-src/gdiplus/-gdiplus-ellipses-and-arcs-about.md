---
description: Una elipse se especifica mediante su rectángulo delimitador. En la ilustración siguiente se muestra una elipse junto con su rectángulo delimitador.
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: Elipses y arcos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b1aaaff5ff27191ed7f0bf64ddbcb414be6319
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156192"
---
# <a name="ellipses-and-arcs"></a>Elipses y arcos

Una elipse se especifica mediante su rectángulo delimitador. En la ilustración siguiente se muestra una elipse junto con su rectángulo delimitador.

![Ilustración de una elipse incluida dentro de un rectángulo delimitador](images/aboutgdip02-art05.png)

Para dibujar una elipse, necesita un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . El objeto **Graphics** proporciona el método [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) y el objeto **Pen** almacena atributos de la elipse, como el ancho y el color de la línea. La dirección del objeto **Pen** se pasa como uno de los argumentos al método DrawEllipse. Los argumentos restantes pasados al método DrawEllipse especifican el rectángulo delimitador de la elipse. En el ejemplo siguiente se dibuja una elipse; el rectángulo delimitador tiene un ancho de 160, un alto de 80 y una esquina superior izquierda de (100, 50).


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) es un método sobrecargado de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , por lo que hay varias formas de proporcionarle argumentos. Por ejemplo, puede construir un objeto [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) y pasar una referencia al objeto **Rect** como argumento al método DrawEllipse.


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



Un arco es una parte de una elipse. Para dibujar un arco, se llama al método [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Los parámetros del método DrawArc son los mismos que los parámetros del método [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) , salvo que DrawArc requiere un ángulo inicial y un ángulo de barrido. En el ejemplo siguiente se dibuja un arco con un ángulo inicial de 30 grados y un ángulo de barrido de 180 grados.


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



En la ilustración siguiente se muestra el arco, la elipse y el rectángulo delimitador.

![Ilustración de una elipse dentro de un rectángulo delimitador; la mitad inferior izquierda de la elipse se dibuja en rojo](images/aboutgdip02-art06.png)

 

 



