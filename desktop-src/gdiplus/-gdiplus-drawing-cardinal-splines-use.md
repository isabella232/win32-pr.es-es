---
description: Una curva spline cardinal es una curva que se pasa sin problemas a través de un conjunto determinado de puntos.
ms.assetid: 0bb84f55-18d0-4a4c-bc5b-7803aa807954
title: Dibujar curvas spline cardinales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c780cb4486f579acb57170a8eda4fd187a421ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560899"
---
# <a name="drawing-cardinal-splines"></a><span data-ttu-id="0b9be-103">Dibujar curvas spline cardinales</span><span class="sxs-lookup"><span data-stu-id="0b9be-103">Drawing Cardinal Splines</span></span>

<span data-ttu-id="0b9be-104">Una curva spline cardinal es una curva que se pasa sin problemas a través de un conjunto determinado de puntos.</span><span class="sxs-lookup"><span data-stu-id="0b9be-104">A cardinal spline is a curve that passes smoothly through a given set of points.</span></span> <span data-ttu-id="0b9be-105">Para dibujar una curva spline cardinal, cree un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y pase la dirección de una matriz de puntos al método [**graphics::D rawcurve**](/previous-versions//ms536070(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0b9be-105">To draw a cardinal spline, create a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and pass the address of an array of points to the [**Graphics::DrawCurve**](/previous-versions//ms536070(v=vs.85)) method.</span></span> <span data-ttu-id="0b9be-106">En el ejemplo siguiente se dibuja una curva spline cardinal en forma de campana que pasa a través de cinco puntos designados:</span><span class="sxs-lookup"><span data-stu-id="0b9be-106">The following example draws a bell-shaped cardinal spline that passes through five designated points:</span></span>


```
Point points[] = {Point(0, 100),
                  Point(50, 80),
                  Point(100, 20),
                  Point(150, 80),
                  Point(200, 100)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5);
```



<span data-ttu-id="0b9be-107">En la ilustración siguiente se muestra la curva y cinco puntos.</span><span class="sxs-lookup"><span data-stu-id="0b9be-107">The following illustration shows the curve and five points.</span></span>

![Ilustración de una curva spline cardinal que pasa a través de un conjunto de cinco puntos](images/cardinalspline1.png)

<span data-ttu-id="0b9be-109">Puede usar el método [**Graphics::D rawclosedcurve**](/previous-versions//ms536143(v=vs.85)) de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para dibujar una curva spline cardinal cerrada.</span><span class="sxs-lookup"><span data-stu-id="0b9be-109">You can use the [**Graphics::DrawClosedCurve**](/previous-versions//ms536143(v=vs.85)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw a closed cardinal spline.</span></span> <span data-ttu-id="0b9be-110">En una curva spline cardinal cerrada, la curva continúa hasta el último punto de la matriz y se conecta con el primer punto de la matriz.</span><span class="sxs-lookup"><span data-stu-id="0b9be-110">In a closed cardinal spline, the curve continues through the last point in the array and connects with the first point in the array.</span></span>

<span data-ttu-id="0b9be-111">En el ejemplo siguiente se dibuja una curva spline cardinal cerrada que pasa por seis puntos designados.</span><span class="sxs-lookup"><span data-stu-id="0b9be-111">The following example draws a closed cardinal spline that passes through six designated points.</span></span>


```
Point points[] = {Point(60, 60),
   Point(150, 80),
   Point(200, 40),
   Point(180, 120),
   Point(120, 100),
   Point(80, 160)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawClosedCurve(&pen, points, 6);
```



<span data-ttu-id="0b9be-112">En la ilustración siguiente se muestra la curva spline cerrada junto con los seis puntos:</span><span class="sxs-lookup"><span data-stu-id="0b9be-112">The following illustration shows the closed spline along with the six points:</span></span>

![Ilustración de una curva spline cardinal cerrada que pasa a través de un conjunto de seis puntos](images/cardinalspline1a.png)

<span data-ttu-id="0b9be-114">Puede cambiar la forma en que una curva spline cardinal se curva pasando un argumento de tensión al método [**Graphics::D rawcurve**](/previous-versions//ms536070(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0b9be-114">You can change the way a cardinal spline bends by passing a tension argument to the [**Graphics::DrawCurve**](/previous-versions//ms536070(v=vs.85)) method.</span></span> <span data-ttu-id="0b9be-115">En el ejemplo siguiente se dibujan tres curvas spline cardinales que pasan por el mismo conjunto de puntos:</span><span class="sxs-lookup"><span data-stu-id="0b9be-115">The following example draws three cardinal splines that pass through the same set of points:</span></span>


```
Point points[] = {Point(20, 50),
                  Point(100, 10),
                  Point(200, 100),
                  Point(300, 50),
                  Point(400, 80)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5, 0.0f);  // tension 0.0
graphics.DrawCurve(&pen, points, 5, 0.6f);  // tension 0.6
graphics.DrawCurve(&pen, points, 5, 1.0f);  // tension 1.0
```



<span data-ttu-id="0b9be-116">En la ilustración siguiente se muestran las tres curvas spline junto con sus valores de tensión.</span><span class="sxs-lookup"><span data-stu-id="0b9be-116">The following illustration shows the three splines along with their tension values.</span></span> <span data-ttu-id="0b9be-117">Tenga en cuenta que cuando la tensión es 0, los puntos están conectados mediante líneas rectas.</span><span class="sxs-lookup"><span data-stu-id="0b9be-117">Note that when the tension is 0, the points are connected by straight lines.</span></span>

![Ilustración de tres curvas spline cardinales que pasan por el mismo conjunto de puntos, pero en diferentes tensiones](images/cardinalspline2.png)

 

 
