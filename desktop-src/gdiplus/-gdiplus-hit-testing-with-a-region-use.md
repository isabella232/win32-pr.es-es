---
description: El propósito de las pruebas de posicionamiento es determinar si el cursor está sobre un objeto determinado, como un icono o un botón.
ms.assetid: 9776b73e-191e-4a8e-9abe-e485ffed954c
title: Pruebas de posicionamiento con una región
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24913d8d890e3e1ded87eb48e2d52f1726663a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997476"
---
# <a name="hit-testing-with-a-region"></a><span data-ttu-id="9c40a-103">Pruebas de posicionamiento con una región</span><span class="sxs-lookup"><span data-stu-id="9c40a-103">Hit Testing with a Region</span></span>

<span data-ttu-id="9c40a-104">El propósito de las pruebas de posicionamiento es determinar si el cursor está sobre un objeto determinado, como un icono o un botón.</span><span class="sxs-lookup"><span data-stu-id="9c40a-104">The purpose of hit testing is to determine whether the cursor is over a given object, such as an icon or a button.</span></span> <span data-ttu-id="9c40a-105">En el ejemplo siguiente se crea una región con forma de signo más formando la Unión de dos regiones rectangulares.</span><span class="sxs-lookup"><span data-stu-id="9c40a-105">The following example creates a plus-shaped region by forming the union of two rectangular regions.</span></span> <span data-ttu-id="9c40a-106">Suponga que el **punto** variable contiene la ubicación del clic más reciente.</span><span class="sxs-lookup"><span data-stu-id="9c40a-106">Assume that the variable **point** holds the location of the most recent click.</span></span> <span data-ttu-id="9c40a-107">El código comprueba si el **punto** está en la región con forma de signo más.</span><span class="sxs-lookup"><span data-stu-id="9c40a-107">The code checks to see whether **point** is in the plus-shaped region.</span></span> <span data-ttu-id="9c40a-108">Si el **punto** está en la región (un acierto), la región se rellena con un pincel rojo opaco.</span><span class="sxs-lookup"><span data-stu-id="9c40a-108">If **point** is in the region (a hit), the region is filled with an opaque red brush.</span></span> <span data-ttu-id="9c40a-109">De lo contrario, la región se rellena con un pincel rojo semitransparente.</span><span class="sxs-lookup"><span data-stu-id="9c40a-109">Otherwise, the region is filled with a semitransparent red brush.</span></span>


```
Point point(60, 10);
// Assume that the variable "point" contains the location
// of the most recent click.
// To simulate a hit, assign (60, 10) to point.
// To simulate a miss, assign (0, 0) to point.
SolidBrush solidBrush(Color());
Region region1(Rect(50, 0, 50, 150));
Region region2(Rect(0, 50, 150, 50));
// Create a plus-shaped region by forming the union of region1 and region2.
// The union replaces region1.
region1.Union(&region2);
if(region1.IsVisible(point, &graphics))
{
   // The point is in the region. Use an opaque brush.
   solidBrush.SetColor(Color(255, 255, 0, 0));
}
else
{
   // The point is not in the region. Use a semitransparent brush.
   solidBrush.SetColor(Color(64, 255, 0, 0));
}
graphics.FillRegion(&solidBrush, &region1);
```



 

 



