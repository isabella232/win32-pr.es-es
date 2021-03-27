---
description: Para crear una ruta de acceso, construya un objeto GraphicsPath y, a continuación, llame a métodos, como AddLine y AddCurve, para agregar tipos primitivos a la ruta de acceso.
ms.assetid: 66faeb73-16fb-4b7f-a4d5-a90ec2590d8c
title: Creación de figuras a partir de líneas, curvas y formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c473dfececcaa86347dc02efdfd62131eb9a63d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001669"
---
# <a name="creating-figures-from-lines-curves-and-shapes"></a>Creación de figuras a partir de líneas, curvas y formas

Para crear una ruta de acceso, construya un objeto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) y, a continuación, llame a métodos, como [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) y [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)), para agregar tipos primitivos a la ruta de acceso.

En el ejemplo siguiente se crea una ruta de acceso que tiene un único arco. El arco tiene un ángulo de barrido de – 180 grados, que es en sentido contrario a las agujas del reloj en el sistema de coordenadas predeterminado.


```
Pen pen(Color(255, 255, 0, 0));
GraphicsPath path;
path.AddArc(175, 50, 50, 50, 0, -180);
graphics.DrawPath(&pen, &path);
```



En el ejemplo siguiente se crea una ruta de acceso que tiene dos figuras. La primera figura es un arco seguido de una línea. La segunda figura es una línea seguida de una curva, seguida de una línea. La primera figura se deja abierta y la segunda figura está cerrada.


```
Point points[] = {Point(40, 60), Point(50, 70), Point(30, 90)};

Pen pen(Color(255, 255, 0, 0), 2);
GraphicsPath path;

// The first figure is started automatically, so there is
// no need to call StartFigure here.
path.AddArc(175, 50, 50, 50, 0.0f, -180.0f);
path.AddLine(100, 0, 250, 20);

path.StartFigure();
path.AddLine(50, 20, 5, 90);
path.AddCurve(points, 3);
path.AddLine(50, 150, 150, 180);
path.CloseFigure();

graphics.DrawPath(&pen, &path);
```



Además de agregar líneas y curvas a trazados, puede Agregar formas cerradas: rectángulos, elipses, gráficos circulares y polígonos. En el ejemplo siguiente se crea una ruta de acceso que tiene dos líneas, un rectángulo y una elipse. El código usa un lápiz para dibujar el trazado y un pincel para rellenar el trazado.


```
GraphicsPath path;
Pen          pen(Color(255, 255, 0, 0), 2);
SolidBrush   brush(Color(255, 0, 0, 200));

path.AddLine(10, 10, 100, 40);
path.AddLine(100, 60, 30, 60);
path.AddRectangle(Rect(50, 35, 20, 40));
path.AddEllipse(10, 75, 40, 30);

graphics.DrawPath(&pen, &path);
graphics.FillPath(&brush, &path);
```



La ruta de acceso del ejemplo anterior tiene tres figuras. La primera figura consta de las dos líneas, la segunda figura consta del rectángulo y la tercera figura consta de la elipse. Incluso cuando no hay ninguna llamada a [**GraphicsPath:: CloseFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) o [**GraphicsPath:: StartFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure), las formas cerradas intrínsecamente, como rectángulos y elipses, se consideran figuras independientes.

 

 



