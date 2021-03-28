---
description: Las rutas de acceso se forman combinando líneas, rectángulos y curvas simples. Recuerde de la información general de los gráficos vectoriales que los siguientes bloques de creación básicos han demostrado ser los más útiles para dibujar imágenes.
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: Rutas de acceso (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768d01d2d945c8252125a43ee2dc79f985703da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556951"
---
# <a name="paths-gdi"></a>Rutas de acceso (GDI+)

Las rutas de acceso se forman combinando líneas, rectángulos y curvas simples. Recuerde de la [información general de los gráficos vectoriales](-gdiplus-overview-of-vector-graphics-about.md) que los siguientes bloques de creación básicos han demostrado ser los más útiles para dibujar imágenes.

-   Líneas
-   Rectángulos
-   Puntos suspensivos
-   -
-   Polígonos
-   Curvas spline cardinales
-   Curvas spline de Bézier

En Windows GDI+, el objeto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) permite recopilar una secuencia de estos bloques de creación en una sola unidad. A continuación, se puede dibujar toda la secuencia de líneas, rectángulos, polígonos y curvas con una llamada al método [**Graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . En la ilustración siguiente se muestra una ruta de acceso creada mediante la combinación de una línea, un arco, una curva spline de Bézier y una curva spline cardinal.

![Ilustración de una ruta de acceso que combina una línea, un arco, una curva spline de Bézier y una curva spline cardinal](images/aboutgdip02-art14.png)

La clase [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) proporciona los métodos siguientes para crear una secuencia de elementos que se van a dibujar: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (para curvas spline cardinales) y [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)). Cada uno de estos métodos está sobrecargado; es decir, cada método se incluye en varias variaciones con listas de parámetros diferentes. Por ejemplo, una variación del método AddLine recibe cuatro enteros y otra variación del método AddLine recibe dos objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) .

Los métodos para agregar líneas, rectángulos y curvas spline de Bézier a un trazado tienen métodos complementarios en plural que agregan varios elementos a la ruta de acceso en una sola llamada: [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))y [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)). Además, el método [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) tiene un método complementario, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), que agrega una curva cerrada a la ruta de acceso.

Para dibujar una ruta de acceso, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) y un objeto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) . El objeto **Graphics** proporciona el método [**graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) y el objeto **Pen** almacena los atributos de la ruta de acceso, como el ancho y el color de la línea. El objeto **GraphicsPath** almacena la secuencia de líneas, rectángulos y curvas que componen la ruta de acceso. Las direcciones del objeto **Pen** y el objeto **GraphicsPath** se pasan como argumentos al método **Graphics::D rawpath** . En el ejemplo siguiente se dibuja un trazado que consta de una línea, una elipse y una curva spline de Bézier.


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



En la ilustración siguiente se muestra la ruta de acceso.

![Ilustración de una ruta de acceso formada por una línea, una elipse y una curva spline de Bézier](images/aboutgdip02-art15.png)

Además de agregar líneas, rectángulos y curvas a un trazado, puede Agregar trazados a un trazado. Esto le permite combinar las rutas de acceso existentes para formar rutas de acceso complejas y grandes. El código siguiente agrega **graphicsPath1** y **graphicsPath2** a **myGraphicsPath**. El segundo parámetro del método [**GraphicsPath:: AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) especifica si la ruta de acceso agregada está conectada a la ruta de acceso existente.


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



Hay otros dos elementos que puede Agregar a una ruta de acceso: cadenas y gráficos circulares. Un gráfico circular es una parte del interior de una elipse. En el ejemplo siguiente se crea una ruta de acceso a partir de un arco, una curva spline cardinal, una cadena y un gráfico circular.


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



En la ilustración siguiente se muestra la ruta de acceso. Tenga en cuenta que no es necesario conectar una ruta de acceso; el arco, la curva spline cardinal, la cadena y el gráfico circular se separan.

![Ilustración de una ruta de acceso formada por líneas desconectadas: un arco, una curva spline cardinal, una cadena y un gráfico circular](images/aboutgdip02-art16.png)

 

 



