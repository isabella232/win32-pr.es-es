---
description: Una elipse se especifica mediante su rectángulo delimitador. En la ilustración siguiente se muestra una elipse junto con su rectángulo delimitador.
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: Elipses y arcos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadd0a34107681d2d155ead5d4f80b7208b8926603f21fa4541d502886edaf73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036753"
---
# <a name="ellipses-and-arcs"></a>Elipses y arcos

Una elipse se especifica mediante su rectángulo delimitador. En la ilustración siguiente se muestra una elipse junto con su rectángulo delimitador.

![ilustración de una elipse incluida dentro de un rectángulo delimitador](images/aboutgdip02-art05.png)

Para dibujar una elipse, necesita un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un [**objeto Pen.**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) El **objeto Graphics** proporciona el método [DrawVelopse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) y el objeto **Pen** almacena los atributos de la elipse, como el ancho de línea y el color. La dirección del **objeto Pen** se pasa como uno de los argumentos al método DrawVelopse. Los argumentos restantes pasados al método DrawVelopse especifican el rectángulo delimitador de la elipse. En el ejemplo siguiente se dibuja una elipse; el rectángulo delimitador tiene un ancho de 160, un alto de 80 y una esquina superior izquierda de (100, 50).


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



[DrawVelopse es](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) un método sobrecargado de la [**clase Graphics,**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) por lo que hay varias maneras de proporcionar argumentos. Por ejemplo, puede construir un [**objeto Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) y pasar una referencia al **objeto Rect** como argumento al método DrawVelopse.


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



Un arco es una parte de una elipse. Para dibujar un arco, llame al [método DrawAsync](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) de la [**clase Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Los parámetros del método DrawVelo son los mismos que los parámetros del método [DrawVelopse,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) salvo que DrawVelo requiere un ángulo inicial y un ángulo de barrido. En el ejemplo siguiente se dibuja un arco con un ángulo inicial de 30 grados y un ángulo de barrido de 180 grados.


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



En la ilustración siguiente se muestra el arco, la elipse y el rectángulo delimitador.

![ilustración de una elipse dentro de un rectángulo delimitador; la mitad inferior izquierda de la elipse se dibuja en rojo](images/aboutgdip02-art06.png)

 

 



