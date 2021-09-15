---
description: Para dibujar líneas y rectángulos, necesita un objeto Graphics y un objeto Pen. El objeto Graphics proporciona el método DrawLine y el objeto Pen almacena características de la línea, como el color y el ancho.
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: Uso de un lápiz para dibujar líneas y rectángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b335caf7e2ecbad6bc49965ff757809c3b1179c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474297"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a>Uso de un lápiz para dibujar líneas y rectángulos

Para dibujar líneas y rectángulos, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un [**objeto Pen.**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) El **objeto Graphics** proporciona el método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) y el **objeto Pen** almacena características de la línea, como el color y el ancho.

En el ejemplo siguiente se dibuja una línea de (20, 10) a (300, 100). Supongamos **que los gráficos** son un [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) existente.


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



La primera instrucción de código usa el constructor de clase [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) para crear un lápiz negro. El argumento que se pasa al constructor **Pen** es un [**objeto Color.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) Los valores usados para construir el **objeto Color** (255, 0, 0, 0) corresponden a los componentes alfa, rojo, verde y azul del color. Estos valores definen un lápiz negro opaco.

En el ejemplo siguiente se dibuja un rectángulo con su esquina superior izquierda en (10, 10). El rectángulo tiene un ancho de 100 y un alto de 50. El segundo argumento pasado al constructor [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) indica que el ancho del lápiz es de 5 píxeles.


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



Cuando se dibuja el rectángulo, el lápiz se centra en el límite del rectángulo. Dado que el ancho del lápiz es 5, los lados del rectángulo se dibujan con 5 píxeles de ancho, de forma que se dibuja 1 píxel en el propio límite, 2 píxeles en el interior y 2 píxeles en el exterior. Para obtener más detalles sobre la alineación del lápiz, vea [Establecer el ancho del lápiz y la alineación.](-gdiplus-setting-pen-width-and-alignment-use.md)

En la ilustración siguiente se muestra el rectángulo resultante. Las líneas de puntos muestran dónde se habría dibujado el rectángulo si el ancho del lápiz hubiera sido de un píxel. La vista ampliada de la esquina superior izquierda del rectángulo muestra que las líneas gruesas de color negro están centradas en esas líneas de puntos.

![ilustración de un rectángulo dibujado con una línea negra gruesa que rodea una línea fina, gris y discontinua](images/pens1.png)

 

 



