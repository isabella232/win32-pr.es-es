---
description: Las rutas de acceso se forman combinando líneas, rectángulos y curvas simples. Recuerde en la introducción a los gráficos vectoriales que los siguientes bloques de creación básicos han demostrado ser los más útiles para dibujar imágenes.
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: Rutas de acceso (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54dae290138314cac3dae8d259591939490764d371e9a2caf9423801e985ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695481"
---
# <a name="paths-gdi"></a>Rutas de acceso (GDI+)

Las rutas de acceso se forman combinando líneas, rectángulos y curvas simples. Recuerde en la [introducción a los gráficos vectoriales](-gdiplus-overview-of-vector-graphics-about.md) que los siguientes bloques de creación básicos han demostrado ser los más útiles para dibujar imágenes.

-   Líneas
-   Rectángulos
-   Puntos suspensivos
-   Arcos
-   Polígonos
-   Splines cardinales
-   Curvas spline de Bézier

En Windows GDI+, el [**objeto GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) permite recopilar una secuencia de estos bloques de creación en una sola unidad. Toda la secuencia de líneas, rectángulos, polígonos y curvas se puede dibujar con una llamada al método [**Graphics::D rawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) de la [**clase Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) En la ilustración siguiente se muestra una ruta de acceso creada mediante la combinación de una línea, un arco, una curva spline de Bézier y una spline cardinal.

![ilustración de un trazado que combina una línea, un arco, una curva spline bézier y una spline cardinal](images/aboutgdip02-art14.png)

La [**clase GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) proporciona los métodos siguientes para crear una secuencia de elementos que se va a dibujar: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle,](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)) [AddDevpse,](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)) [AddEnsa,](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)) [AddPolygon,](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)) [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (para splines cardinales) y [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)). Cada uno de estos métodos está sobrecargado; Es decir, cada método tiene varias variaciones con listas de parámetros diferentes. Por ejemplo, una variación del método AddLine recibe cuatro enteros y otra variación del método AddLine recibe dos [**objetos Point.**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point)

Los métodos para agregar líneas, rectángulos y splines de Bézier a una ruta de acceso tienen métodos complementarios plurales que agregan varios elementos a la ruta de acceso en una sola llamada: [AddLines,](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)) [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))y [AddBeziers.](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)) Además, el [método AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) tiene un método complementario, [AddClosedCurve,](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint))que agrega una curva cerrada a la ruta de acceso.

Para dibujar una ruta de acceso, necesita un objeto [**Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) un [**objeto Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) y un [**objeto GraphicsPath.**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) El **objeto Graphics** proporciona el método [**Graphics::D rawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) y el objeto **Pen** almacena atributos de la ruta de acceso, como el ancho de línea y el color. El **objeto GraphicsPath** almacena la secuencia de líneas, rectángulos y curvas que forma la ruta de acceso. Las direcciones del objeto **Pen** y del **objeto GraphicsPath** se pasan como argumentos al **método Graphics::D rawPath.** En el ejemplo siguiente se dibuja un trazado que consta de una línea, una elipse y una curva spline de Bézier.


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



En la ilustración siguiente se muestra la ruta de acceso.

![ilustración de una ruta de acceso de una línea, una elipse y una curva spline bézier](images/aboutgdip02-art15.png)

Además de agregar líneas, rectángulos y curvas a un trazado, puede agregar rutas de acceso a un trazado. Esto le permite combinar rutas de acceso existentes para formar rutas de acceso grandes y complejas. El código siguiente agrega **graphicsPath1** y **graphicsPath2** a **myGraphicsPath.** El segundo parámetro del método [**GraphicsPath::AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) especifica si la ruta de acceso agregada está conectada a la ruta de acceso existente.


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



Hay otros dos elementos que puede agregar a una ruta de acceso: cadenas y pies. Un gráfico circular es una parte del interior de una elipse. En el ejemplo siguiente se crea una ruta de acceso a partir de un arco, una spline cardinal, una cadena y un gráfico circular.


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



En la ilustración siguiente se muestra la ruta de acceso. Tenga en cuenta que no es necesario conectar una ruta de acceso; el arco, la spline cardinal, la cadena y el gráfico circular están separados.

![ilustración de una ruta de acceso de líneas desconectadas: un arco, una spline cardinal, una cadena y un gráfico circular](images/aboutgdip02-art16.png)

 

 



