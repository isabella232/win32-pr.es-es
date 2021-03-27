---
description: Para dibujar líneas y rectángulos, necesita un objeto Graphics y un objeto Pen. El objeto Graphics proporciona el método DrawLine y el objeto Pen almacena características de la línea, como el color y el ancho.
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: Uso de un lápiz para dibujar líneas y rectángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b335caf7e2ecbad6bc49965ff757809c3b1179c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001658"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a>Uso de un lápiz para dibujar líneas y rectángulos

Para dibujar líneas y rectángulos, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . El objeto **Graphics** proporciona el método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) y el objeto **Pen** almacena características de la línea, como el color y el ancho.

En el ejemplo siguiente se dibuja una línea de (20, 10) a (300, 100). Supongamos que los **gráficos** son objetos [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) existentes.


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



La primera instrucción de código usa el constructor de clase [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) para crear un lápiz negro. El argumento que se pasa al constructor **Pen** es un objeto de [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . Los valores utilizados para construir el objeto de **color** (255, 0, 0), corresponden a los componentes alfa, rojo, verde y azul del color. Estos valores definen un lápiz negro opaco.

En el ejemplo siguiente se dibuja un rectángulo con la esquina superior izquierda en (10, 10). El rectángulo tiene un ancho de 100 y un alto de 50. El segundo argumento que se pasa al constructor [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) indica que el ancho del lápiz es de 5 píxeles.


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



Cuando se dibuja el rectángulo, el lápiz se centra en el límite del rectángulo. Dado que el ancho del lápiz es 5, los lados del rectángulo se dibujan en 5 píxeles de ancho, de modo que 1 píxel se dibuja en el límite, se dibujan 2 píxeles en el interior y se dibujan 2 píxeles en el exterior. Para obtener más información sobre la alineación del lápiz, vea [establecer el ancho y la alineación del lápiz](-gdiplus-setting-pen-width-and-alignment-use.md).

En la ilustración siguiente se muestra el rectángulo resultante. Las líneas de puntos muestran dónde se habría dibujado el rectángulo si el ancho del lápiz hubiera sido un píxel. La vista ampliada de la esquina superior izquierda del rectángulo muestra que las líneas negras gruesas se centran en esas líneas de puntos.

![Ilustración de un rectángulo dibujado con una línea gruesa de color negro que rodea una línea de guiones fino y gris](images/pens1.png)

 

 



