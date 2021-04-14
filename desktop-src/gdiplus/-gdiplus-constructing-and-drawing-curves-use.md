---
description: 'GDI+ admite varios tipos de curvas: elipses, arcos, curvas spline cardinales y B&\# 233; curvas spline de Bézier.'
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: Crear y dibujar curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f61c1aa12e3152ed65cca2da6911d2d53def81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997521"
---
# <a name="constructing-and-drawing-curves"></a><span data-ttu-id="70e35-103">Crear y dibujar curvas</span><span class="sxs-lookup"><span data-stu-id="70e35-103">Constructing and Drawing Curves</span></span>

<span data-ttu-id="70e35-104">GDI+ admite varios tipos de curvas: elipses, arcos, curvas spline cardinales y curvas spline de Bézier.</span><span class="sxs-lookup"><span data-stu-id="70e35-104">GDI+ supports several types of curves: ellipses, arcs, cardinal splines, and Bézier splines.</span></span> <span data-ttu-id="70e35-105">Una elipse se define mediante su rectángulo delimitador; un arco es una parte de una elipse definida por un ángulo inicial y un ángulo de barrido.</span><span class="sxs-lookup"><span data-stu-id="70e35-105">An ellipse is defined by its bounding rectangle; an arc is a portion of an ellipse defined by a starting angle and a sweep angle.</span></span> <span data-ttu-id="70e35-106">Una curva spline cardinal se define mediante una matriz de puntos y un parámetro de tensión: la curva se pasa sin problemas a través de cada punto de la matriz y el parámetro de tensión influye en la forma en que se curva la curva.</span><span class="sxs-lookup"><span data-stu-id="70e35-106">A cardinal spline is defined by an array of points and a tension parameter — the curve passes smoothly through each point in the array, and the tension parameter influences the way the curve bends.</span></span> <span data-ttu-id="70e35-107">Una curva spline de Bézier se define mediante dos puntos de conexión y dos puntos de control: la curva no pasa a través de los puntos de control, pero los puntos de control influyen en la dirección y el plegado a medida que la curva va de un extremo al otro.</span><span class="sxs-lookup"><span data-stu-id="70e35-107">A Bézier spline is defined by two end points and two control points — the curve does not pass through the control points, but the control points influence the direction and bend as the curve goes from one end point to the other.</span></span>

<span data-ttu-id="70e35-108">En los temas siguientes se tratan las curvas spline cardinales y las curvas spline de Bézier con más detalle:</span><span class="sxs-lookup"><span data-stu-id="70e35-108">The following topics cover cardinal splines and Bézier splines in more detail:</span></span>

-   [<span data-ttu-id="70e35-109">Dibujar curvas spline cardinales</span><span class="sxs-lookup"><span data-stu-id="70e35-109">Drawing Cardinal Splines</span></span>](-gdiplus-drawing-cardinal-splines-use.md)
-   [<span data-ttu-id="70e35-110">Dibujar curvas spline de Bézier</span><span class="sxs-lookup"><span data-stu-id="70e35-110">Drawing Bézier Splines</span></span>](-gdiplus-drawing-bezier-splines-use.md)

 

 



