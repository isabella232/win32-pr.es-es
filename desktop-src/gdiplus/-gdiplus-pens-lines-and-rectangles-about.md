---
description: Para dibujar líneas con GDI+ de Windows, debe crear un objeto Graphics y un objeto Pen.
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: Lápices, líneas y rectángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e9749b1c1af6ca4808e797d016267bb251e6fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985139"
---
# <a name="pens-lines-and-rectangles"></a>Lápices, líneas y rectángulos

Para dibujar líneas con GDI+ de Windows, debe crear un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . El objeto **Graphics** proporciona los métodos que realmente realizan el dibujo y el objeto **Pen** almacena los atributos de la línea, como el color, el ancho y el estilo. Dibujar una línea es simplemente cuestión de llamar al método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) del objeto **Graphics** . La dirección del objeto **Pen** se pasa como uno de los argumentos al método DrawLine. En el ejemplo siguiente se dibuja una línea desde el punto (4, 2) hasta el punto (12, 6).


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) es un método sobrecargado de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , por lo que hay varias formas de proporcionarle argumentos. Por ejemplo, puede construir dos objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) y pasar referencias a los objetos **Point** como argumentos al método DrawLine.


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



Puede especificar ciertos atributos al construir un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . Por ejemplo, un constructor [Pen](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) permite especificar el color y el ancho. En el ejemplo siguiente se dibuja una línea azul de ancho 2 de (0,0) a (60, 30).


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



El objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) también tiene atributos, como el estilo Dash, que puede usar para especificar las características de la línea. Por ejemplo, en el ejemplo siguiente se dibuja una línea discontinua de (100, 50) a (300, 80).


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



Puede usar varios métodos del objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) para establecer muchos más atributos de la línea. Los métodos [**Pen:: SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) y [**Pen:: SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) especifican la apariencia de los extremos de la línea; los extremos pueden ser plano, cuadrado, redondeado, triangular o una forma personalizada. El método [**Pen:: SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) le permite especificar si las líneas conectadas están en ángulo (Unidas con esquinas vivas), biseladas, redondeadas o recortadas. En la ilustración siguiente se muestran líneas con varios estilos de extremo y de combinación.

![Ilustración de dos líneas que muestran extremos redondeados y circulares, esquinas redondeadas y en ángulo y dos estilos de flecha](images/aboutgdip02-art04.png)

Dibujar rectángulos con GDI+ es similar a las líneas de dibujo. Para dibujar un rectángulo, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . El objeto **Graphics** proporciona un método [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) y el objeto **Pen** almacena atributos, como el color y el ancho de línea. La dirección del objeto **Pen** se pasa como uno de los argumentos al método DrawRectangle. En el ejemplo siguiente se dibuja un rectángulo con la esquina superior izquierda en (100, 50), un ancho de 80 y un alto de 40.


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) es un método sobrecargado de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , por lo que hay varias formas de proporcionarle argumentos. Por ejemplo, puede construir un objeto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) y pasar una referencia al objeto **Rect** como argumento para el método DrawRectangle.


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



Un objeto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) tiene métodos para manipular y recopilar información sobre el rectángulo. Por ejemplo, los métodos [Inflate](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) y [offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) cambian el tamaño y la posición del rectángulo. El método [**Rect:: IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) indica si el rectángulo forma una intersección con otro rectángulo determinado y el método [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) indica si un punto determinado se encuentra dentro del rectángulo.

 

 
