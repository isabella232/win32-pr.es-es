---
description: Los registros de spline representan las curvas cuadráticas (es decir, las splines de b cuadrática) utilizadas por TrueType.
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: Registros de spline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e10f36e4a0481f9950f63c4cbbb59d48d24df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813028"
---
# <a name="spline-records"></a><span data-ttu-id="97416-103">Registros de spline</span><span class="sxs-lookup"><span data-stu-id="97416-103">Spline Records</span></span>

<span data-ttu-id="97416-104">Los registros de spline representan las curvas cuadráticas (es decir, las splines de b cuadrática) utilizadas por TrueType.</span><span class="sxs-lookup"><span data-stu-id="97416-104">Spline records represent the quadratic curves (that is, quadratic b-splines) used by TrueType.</span></span> <span data-ttu-id="97416-105">Un registro de spline comienza con el último punto del registro anterior (o para el primer registro del contorno, con el punto inicial).</span><span class="sxs-lookup"><span data-stu-id="97416-105">A spline record begins with the last point in the previous record (or for the first record in the contour, with the starting point).</span></span> <span data-ttu-id="97416-106">En el primer registro de spline, el punto inicial y el último punto del registro se encuentran en el contorno del glifo.</span><span class="sxs-lookup"><span data-stu-id="97416-106">For the first spline record, the starting point and the last point in the record are on the glyph outline.</span></span> <span data-ttu-id="97416-107">En el caso de todos los demás registros de spline, solo el último punto está en el contorno del glifo.</span><span class="sxs-lookup"><span data-stu-id="97416-107">For all other spline records, only the last point is on the glyph outline.</span></span> <span data-ttu-id="97416-108">Todos los demás puntos de los registros de spline están fuera del contorno del glifo y deben representarse como puntos de control de las splines b.</span><span class="sxs-lookup"><span data-stu-id="97416-108">All other points in the spline records are off the glyph outline and must be rendered as the control points of b-splines.</span></span>

<span data-ttu-id="97416-109">El último registro de spline o Polyline de un contorno finaliza siempre con el punto inicial del contorno.</span><span class="sxs-lookup"><span data-stu-id="97416-109">The last spline or polyline record in a contour always ends with the contour's starting point.</span></span> <span data-ttu-id="97416-110">Esta disposición garantiza que todos los contornos estén cerrados.</span><span class="sxs-lookup"><span data-stu-id="97416-110">This arrangement ensures that every contour is closed.</span></span>

<span data-ttu-id="97416-111">Dado que las splines b requieren tres puntos (un punto en el contorno del glifo entre dos puntos que se encuentran en el contorno), debe realizar algunos cálculos cuando un registro de spline contiene más de un punto fuera de curva.</span><span class="sxs-lookup"><span data-stu-id="97416-111">Because b-splines require three points (one point off the glyph outline between two points that are on the outline), you must perform some calculations when a spline record contains more than one off-curve point.</span></span>

<span data-ttu-id="97416-112">Por ejemplo, si un registro de spline contiene tres puntos (A, B y C) y no es el primer registro, los puntos A y B están fuera del contorno del glifo.</span><span class="sxs-lookup"><span data-stu-id="97416-112">For example, if a spline record contains three points (A, B, and C) and it is not the first record, points A and B are off the glyph outline.</span></span> <span data-ttu-id="97416-113">Para interpretar el punto A, use la posición actual (que siempre está en el contorno del glifo) y el punto en el contorno del glifo entre los puntos A y B. Para buscar el punto medio (M) entre A y B, puede realizar el cálculo siguiente.</span><span class="sxs-lookup"><span data-stu-id="97416-113">To interpret point A, use the current position (which is always on the glyph outline) and the point on the glyph outline between points A and B. To find the midpoint (M) between A and B, you can perform the following calculation.</span></span>

<span data-ttu-id="97416-114">M = A + (B A)/2</span><span class="sxs-lookup"><span data-stu-id="97416-114">M = A + (B A)/2</span></span>

<span data-ttu-id="97416-115">El punto medio entre los puntos no contornos consecutivos en un registro de spline es un punto en el contorno del glifo, de acuerdo con la definición del formato de spline usado en las fuentes TrueType.</span><span class="sxs-lookup"><span data-stu-id="97416-115">The midpoint between consecutive off-outline points in a spline record is a point on the glyph outline, according to the definition of the spline format used in TrueType fonts.</span></span>

<span data-ttu-id="97416-116">Si la posición actual se designa mediante P, las dos curvas spline cuadráticas definidas por este registro de spline son (P, A, M) y (M, B, C).</span><span class="sxs-lookup"><span data-stu-id="97416-116">If the current position is designated by P, the two quadratic splines defined by this spline record are (P, A, M) and (M, B, C).</span></span>

 

 



