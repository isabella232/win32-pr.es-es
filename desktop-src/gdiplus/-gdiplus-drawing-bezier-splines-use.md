---
description: 'Una \# curva spline de bézier&233; se define con cuatro puntos: un punto inicial, dos puntos de control y un punto final.'
ms.assetid: af19e82b-0d13-4fb0-981e-8d5dd1bbfb36
title: Dibujar curvas spline de Bézier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea97d25f482372c387239e8f9083b31e3b2d912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812937"
---
# <a name="drawing-bezier-splines"></a><span data-ttu-id="1c127-103">Dibujar curvas spline de Bézier</span><span class="sxs-lookup"><span data-stu-id="1c127-103">Drawing Bezier Splines</span></span>

<span data-ttu-id="1c127-104">Una curva spline de Bézier se define mediante cuatro puntos: un punto inicial, dos puntos de control y un punto final.</span><span class="sxs-lookup"><span data-stu-id="1c127-104">A Bézier spline is defined by four points: a start point, two control points, and an end point.</span></span> <span data-ttu-id="1c127-105">En el ejemplo siguiente se dibuja una curva spline de Bézier con un punto inicial (10, 100) y un punto final (200, 100).</span><span class="sxs-lookup"><span data-stu-id="1c127-105">The following example draws a Bézier spline with start point (10, 100) and end point (200, 100).</span></span> <span data-ttu-id="1c127-106">Los puntos de control son (100, 10) y (150, 150):</span><span class="sxs-lookup"><span data-stu-id="1c127-106">The control points are (100, 10) and (150, 150):</span></span>


```
Point p1(10, 100);   // start point
Point c1(100, 10);   // first control point
Point c2(150, 150);  // second control point
Point p2(200, 100);  // end point
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBezier(&pen, p1, c1, c2, p2);
```



<span data-ttu-id="1c127-107">En la ilustración siguiente se muestra la curva spline de Bézier resultante junto con el punto inicial, los puntos de control y el punto final.</span><span class="sxs-lookup"><span data-stu-id="1c127-107">The following illustration shows the resulting Bézier spline along with its start point, control points, and end point.</span></span> <span data-ttu-id="1c127-108">La ilustración también muestra el casco convexo de la spline, que es un polígono formado mediante la conexión de los cuatro puntos con líneas rectas.</span><span class="sxs-lookup"><span data-stu-id="1c127-108">The illustration also shows the spline's convex hull, which is a polygon formed by connecting the four points with straight lines.</span></span>

![Ilustración en la que se muestra una curva spline Bézier con dos puntos finales y dos puntos de control](images/bezierspline1.png)

<span data-ttu-id="1c127-110">Puede usar el método [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para dibujar una secuencia de curvas spline de Bézier conectadas.</span><span class="sxs-lookup"><span data-stu-id="1c127-110">You can use the [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw a sequence of connected Bézier splines.</span></span> <span data-ttu-id="1c127-111">En el ejemplo siguiente se dibuja una curva que consta de dos curvas spline de Bézier conectadas.</span><span class="sxs-lookup"><span data-stu-id="1c127-111">The following example draws a curve that consists of two connected Bézier splines.</span></span> <span data-ttu-id="1c127-112">El punto final de la primera curva spline de Bézier es el punto inicial de la segunda curva spline de Bézier.</span><span class="sxs-lookup"><span data-stu-id="1c127-112">The end point of the first Bézier spline is the start point of the second Bézier spline.</span></span>


```
Point p[] = {
   Point(10, 100),   // start point of first spline
   Point(75, 10),    // first control point of first spline
   Point(80, 50),    // second control point of first spline
   Point(100, 150),  // end point of first spline and 
                     // start point of second spline
   Point(125, 80),   // first control point of second spline
   Point(175, 200),  // second control point of second spline
   Point(200, 80)};  // end point of second spline
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBeziers(&pen, p, 7);
```



<span data-ttu-id="1c127-113">En la ilustración siguiente se muestran las curvas spline conectadas junto con los siete puntos.</span><span class="sxs-lookup"><span data-stu-id="1c127-113">The following illustration shows the connected splines along with the seven points.</span></span>

![Ilustración en la que se muestran los puntos finales y los puntos de control de dos splines que comparten uno de los extremos](images/bezierspline2.png)

 

 



