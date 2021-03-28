---
description: GDI+ de Windows dibuja líneas, rectángulos y otras figuras en un sistema de coordenadas.
ms.assetid: a43bcb27-473b-4ca2-a937-2b54384ab86b
title: Información general de los gráficos vectoriales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9bfe98585ef8e073cf1c563c237436b7c982bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561379"
---
# <a name="overview-of-vector-graphics"></a>Información general de los gráficos vectoriales

GDI+ de Windows dibuja líneas, rectángulos y otras figuras en un sistema de coordenadas. Puede elegir entre varios sistemas de coordenadas, pero el sistema de coordenadas predeterminado tiene el origen en la esquina superior izquierda con el eje x apuntando hacia la derecha y el eje y apuntando hacia abajo. La unidad de medida del sistema de coordenadas predeterminado es el píxel.

![Ilustración de un sistema de coordenadas con el eje x que se extiende hacia la derecha y el eje y se extiende hacia abajo](images/aboutgdip02-art01.png)

Un monitor de equipo crea su presentación en una matriz rectangular de puntos denominados elementos de imagen o píxeles. El número de píxeles que aparecen en la pantalla varía de un monitor a otro, y el número de píxeles que aparecen en un monitor individual normalmente se puede configurar hasta cierto punto por el usuario.

![Ilustración de una cuadrícula rectangular, con tres celdas en esa cuadrícula etiquetadas por sus coordenadas](images/aboutgdip02-art02.png)

Al utilizar GDI+ para dibujar una línea, un rectángulo o una curva, se proporciona cierta información clave sobre el elemento que se va a dibujar. Por ejemplo, puede especificar una línea proporcionando dos puntos, y puede especificar un rectángulo proporcionando un punto, un alto y un ancho. GDI+ funciona junto con el software del controlador de pantalla para determinar qué píxeles deben estar encendidos para mostrar la línea, el rectángulo o la curva. En la ilustración siguiente se muestran los píxeles que están activados para mostrar una línea desde el punto (4, 2) hasta el punto (12, 8).

![Ilustración en la que se muestra una cuadrícula rectangular con celdas rellenas para indicar una línea entre dos extremos](images/aboutgdip02-art03.png)

Con el tiempo, algunos bloques de creación básicos han demostrado ser los más útiles para crear imágenes bidimensionales. Estos bloques de creación, que son compatibles con GDI+, se proporcionan en la lista siguiente:

-   Líneas
-   Rectángulos
-   Puntos suspensivos
-   -
-   Polígonos
-   Curvas spline cardinales
-   Curvas spline de Bézier

La [**clase Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) de GDI+ proporciona los siguientes métodos para dibujar los elementos de la lista anterior: [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)), [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_)), [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpointf_inint)), [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal)), [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) (para las curvas spline cardinales) y [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpoint__inconstpoint__inconstpoint__inconstpoint_)). Cada uno de estos métodos está sobrecargado; es decir, cada método se incluye en varias variaciones con listas de parámetros diferentes. Por ejemplo, una variación del método DrawLine recibe la dirección de un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) y cuatro enteros, mientras que otra variación del método DrawLine recibe la dirección de un objeto **Pen** y dos referencias a objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) .

Los métodos para dibujar líneas, rectángulos y curvas spline de Bézier tienen métodos complementarios en plural que dibujan varios elementos en una sola llamada: [DrawLines](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawlines(inconstpen_inconstpointf_inint)), [DrawRectangles](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangles(inconstpen_inconstrect_inint))y [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)). Además, el método [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) tiene un método complementario, [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)), que cierra una curva conectando el punto final de la curva al punto inicial.

Todos los métodos de dibujo de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) funcionan junto con un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . Por lo tanto, para poder dibujar cualquier cosa, debe crear al menos dos objetos: un objeto **Graphics** y un objeto **Pen** . El objeto **Pen** almacena los atributos del elemento que se va a dibujar, como el ancho y el color de línea. La dirección del objeto **Pen** se pasa como uno de los argumentos al método Drawing. Por ejemplo, una variación del método [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) recibe la dirección de un objeto **Pen** y cuatro enteros, tal y como se muestra en el código siguiente, que dibuja un rectángulo con un ancho de 100, un alto de 50 y una esquina superior izquierda de (20, 10).


```
myGraphics.DrawRectangle(&myPen, 20, 10, 100, 50);
```



 

 



