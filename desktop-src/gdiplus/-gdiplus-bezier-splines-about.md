---
description: 'Una \# curva spline de bézier&233; es una curva especificada por cuatro puntos: dos extremos (P1 y P2) y dos puntos de control (C1 y C2).'
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: Curvas spline de Bézier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd725e64f9ba0035849d2d1d6fbc03d5efa0b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156232"
---
# <a name="bezier-splines"></a><span data-ttu-id="6df7f-103">Curvas spline de Bézier</span><span class="sxs-lookup"><span data-stu-id="6df7f-103">Bezier Splines</span></span>

<span data-ttu-id="6df7f-104">Una curva spline de Bézier es una curva especificada por cuatro puntos: dos puntos finales (P1 y P2) y dos puntos de control (C1 y C2).</span><span class="sxs-lookup"><span data-stu-id="6df7f-104">A Bézier spline is a curve specified by four points: two end points (p1 and p2) and two control points (c1 and c2).</span></span> <span data-ttu-id="6df7f-105">La curva comienza en P1 y termina en P2.</span><span class="sxs-lookup"><span data-stu-id="6df7f-105">The curve begins at p1 and ends at p2.</span></span> <span data-ttu-id="6df7f-106">La curva no pasa a través de los puntos de control, pero los puntos de control actúan como imanes, extrayendo la curva en determinadas direcciones e influindo en la forma en que se dobla la curva.</span><span class="sxs-lookup"><span data-stu-id="6df7f-106">The curve doesn't pass through the control points, but the control points act as magnets, pulling the curve in certain directions and influencing the way the curve bends.</span></span> <span data-ttu-id="6df7f-107">En la ilustración siguiente se muestra una curva de Bézier junto con sus extremos y puntos de control.</span><span class="sxs-lookup"><span data-stu-id="6df7f-107">The following illustration shows a Bézier curve along with its endpoints and control points.</span></span>

![Ilustración en la que se muestra una curva spline Bézier con dos puntos finales y dos puntos de control](images/aboutgdip02-art11a.png)

<span data-ttu-id="6df7f-109">Tenga en cuenta que la curva comienza en P1 y se desplaza hacia el punto de control C1.</span><span class="sxs-lookup"><span data-stu-id="6df7f-109">Note that the curve starts at p1 and moves toward the control point c1.</span></span> <span data-ttu-id="6df7f-110">La línea tangente a la curva en P1 es la línea que se dibuja de P1 a C1.</span><span class="sxs-lookup"><span data-stu-id="6df7f-110">The tangent line to the curve at p1 is the line drawn from p1 to c1.</span></span> <span data-ttu-id="6df7f-111">Tenga en cuenta también que la línea tangente en el extremo P2 es la línea dibujada de C2 a P2.</span><span class="sxs-lookup"><span data-stu-id="6df7f-111">Also note that the tangent line at the endpoint p2 is the line drawn from c2 to p2.</span></span>

<span data-ttu-id="6df7f-112">Para dibujar una curva spline de Bézier, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="6df7f-112">To draw a Bézier spline, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="6df7f-113">El objeto **Graphics** proporciona el método [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) y el objeto **Pen** almacena atributos de la curva, como el color y el ancho de línea.</span><span class="sxs-lookup"><span data-stu-id="6df7f-113">The **Graphics** object provides the [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) method, and the **Pen** object stores attributes of the curve, such as line width and color.</span></span> <span data-ttu-id="6df7f-114">La dirección del objeto **Pen** se pasa como uno de los argumentos al método DrawBezier.</span><span class="sxs-lookup"><span data-stu-id="6df7f-114">The address of the **Pen** object is passed as one of the arguments to the DrawBezier method.</span></span> <span data-ttu-id="6df7f-115">Los argumentos restantes que se pasan al método DrawBezier son los extremos y los puntos de control.</span><span class="sxs-lookup"><span data-stu-id="6df7f-115">The remaining arguments passed to the DrawBezier method are the endpoints and the control points.</span></span> <span data-ttu-id="6df7f-116">En el ejemplo siguiente se dibuja una curva spline de Bézier con el punto inicial (0,0), los puntos de control (40, 20) y (80, 150) y el punto final (100, 10).</span><span class="sxs-lookup"><span data-stu-id="6df7f-116">The following example draws a Bézier spline with starting point (0, 0), control points (40, 20) and (80, 150), and ending point (100, 10).</span></span>


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



<span data-ttu-id="6df7f-117">En la ilustración siguiente se muestra la curva, los puntos de control y dos líneas tangentes.</span><span class="sxs-lookup"><span data-stu-id="6df7f-117">The following illustration shows the curve, the control points, and two tangent lines.</span></span>

![Ilustración que muestra una curva spline Bézier con dos puntos finales, dos puntos de control y dos líneas tangentes](images/aboutgdip02-art12.png)

<span data-ttu-id="6df7f-119">Las curvas spline de Bézier fueron desarrolladas originalmente por Pierre Bézier para el diseño en la industria del automóvil.</span><span class="sxs-lookup"><span data-stu-id="6df7f-119">Bézier splines were originally developed by Pierre Bézier for design in the automotive industry.</span></span> <span data-ttu-id="6df7f-120">Ya han demostrado ser muy útiles en muchos tipos de diseño asistido por PC y también se usan para definir los contornos de las fuentes.</span><span class="sxs-lookup"><span data-stu-id="6df7f-120">They have since proven to be very useful in many types of computer-aided design and are also used to define the outlines of fonts.</span></span> <span data-ttu-id="6df7f-121">Las curvas spline de Bézier pueden producir una gran variedad de formas, algunas de las cuales se muestran en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="6df7f-121">Bézier splines can yield a wide variety of shapes, some of which are shown in the following illustration.</span></span>

![Ilustración que muestra tres curvas spline de Bézier](images/aboutgdip02-art13.png)

 

 



