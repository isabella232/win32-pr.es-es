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
# <a name="creating-figures-from-lines-curves-and-shapes"></a><span data-ttu-id="24856-103">Creación de figuras a partir de líneas, curvas y formas</span><span class="sxs-lookup"><span data-stu-id="24856-103">Creating Figures from Lines, Curves, and Shapes</span></span>

<span data-ttu-id="24856-104">Para crear una ruta de acceso, construya un objeto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) y, a continuación, llame a métodos, como [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) y [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)), para agregar tipos primitivos a la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="24856-104">To create a path, construct a [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object, and then call methods, such as [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) and [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)), to add primitives to the path.</span></span>

<span data-ttu-id="24856-105">En el ejemplo siguiente se crea una ruta de acceso que tiene un único arco. El arco tiene un ángulo de barrido de – 180 grados, que es en sentido contrario a las agujas del reloj en el sistema de coordenadas predeterminado.</span><span class="sxs-lookup"><span data-stu-id="24856-105">The following example creates a path that has a single arc. The arc has a sweep angle of –180 degrees, which is counterclockwise in the default coordinate system.</span></span>


```
Pen pen(Color(255, 255, 0, 0));
GraphicsPath path;
path.AddArc(175, 50, 50, 50, 0, -180);
graphics.DrawPath(&pen, &path);
```



<span data-ttu-id="24856-106">En el ejemplo siguiente se crea una ruta de acceso que tiene dos figuras.</span><span class="sxs-lookup"><span data-stu-id="24856-106">The following example creates a path that has two figures.</span></span> <span data-ttu-id="24856-107">La primera figura es un arco seguido de una línea.</span><span class="sxs-lookup"><span data-stu-id="24856-107">The first figure is an arc followed by a line.</span></span> <span data-ttu-id="24856-108">La segunda figura es una línea seguida de una curva, seguida de una línea.</span><span class="sxs-lookup"><span data-stu-id="24856-108">The second figure is a line followed by a curve, followed by a line.</span></span> <span data-ttu-id="24856-109">La primera figura se deja abierta y la segunda figura está cerrada.</span><span class="sxs-lookup"><span data-stu-id="24856-109">The first figure is left open, and the second figure is closed.</span></span>


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



<span data-ttu-id="24856-110">Además de agregar líneas y curvas a trazados, puede Agregar formas cerradas: rectángulos, elipses, gráficos circulares y polígonos.</span><span class="sxs-lookup"><span data-stu-id="24856-110">In addition to adding lines and curves to paths, you can add closed shapes: rectangles, ellipses, pies, and polygons.</span></span> <span data-ttu-id="24856-111">En el ejemplo siguiente se crea una ruta de acceso que tiene dos líneas, un rectángulo y una elipse.</span><span class="sxs-lookup"><span data-stu-id="24856-111">The following example creates a path that has two lines, a rectangle, and an ellipse.</span></span> <span data-ttu-id="24856-112">El código usa un lápiz para dibujar el trazado y un pincel para rellenar el trazado.</span><span class="sxs-lookup"><span data-stu-id="24856-112">The code uses a pen to draw the path and a brush to fill the path.</span></span>


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



<span data-ttu-id="24856-113">La ruta de acceso del ejemplo anterior tiene tres figuras.</span><span class="sxs-lookup"><span data-stu-id="24856-113">The path in the preceding example has three figures.</span></span> <span data-ttu-id="24856-114">La primera figura consta de las dos líneas, la segunda figura consta del rectángulo y la tercera figura consta de la elipse.</span><span class="sxs-lookup"><span data-stu-id="24856-114">The first figure consists of the two lines, the second figure consists of the rectangle, and the third figure consists of the ellipse.</span></span> <span data-ttu-id="24856-115">Incluso cuando no hay ninguna llamada a [**GraphicsPath:: CloseFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) o [**GraphicsPath:: StartFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure), las formas cerradas intrínsecamente, como rectángulos y elipses, se consideran figuras independientes.</span><span class="sxs-lookup"><span data-stu-id="24856-115">Even when there are no calls to [**GraphicsPath::CloseFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) or [**GraphicsPath::StartFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure), intrinsically closed shapes, such as rectangles and ellipses, are considered separate figures.</span></span>

 

 



