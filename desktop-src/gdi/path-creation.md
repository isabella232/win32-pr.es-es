---
description: Para crear una ruta de acceso y seleccionarla en un controlador de dominio, primero es necesario definir los puntos que lo describen.
ms.assetid: 3691c3ab-f634-476d-a56b-1c187cb12120
title: Creación de la ruta de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caec86d5d7ca5548d021e3c959eac93633f8880c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275990"
---
# <a name="path-creation"></a><span data-ttu-id="773b0-103">Creación de la ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="773b0-103">Path Creation</span></span>

<span data-ttu-id="773b0-104">Para crear una ruta de acceso y seleccionarla en un controlador de dominio, primero es necesario definir los puntos que lo describen.</span><span class="sxs-lookup"><span data-stu-id="773b0-104">To create a path and select it into a DC, it is first necessary to define the points that describe it.</span></span> <span data-ttu-id="773b0-105">Para ello, se llama a la función [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) , se especifican las funciones de dibujo apropiadas y, a continuación, se llama a la función [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) .</span><span class="sxs-lookup"><span data-stu-id="773b0-105">This is done by calling the [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) function, specifying the appropriate drawing functions, and then by calling the [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) function.</span></span> <span data-ttu-id="773b0-106">Esta combinación de funciones (**BeginPath**, Drawing functions y **EndPath**) constituye un *corchete de trazado*.</span><span class="sxs-lookup"><span data-stu-id="773b0-106">This combination of functions (**BeginPath**, drawing functions, and **EndPath**) constitute a *path bracket*.</span></span> <span data-ttu-id="773b0-107">A continuación se muestra la lista de funciones de dibujo que se pueden usar.</span><span class="sxs-lookup"><span data-stu-id="773b0-107">The following is the list of drawing functions that can be used.</span></span>

-   [<span data-ttu-id="773b0-108">**AngleArc**</span><span class="sxs-lookup"><span data-stu-id="773b0-108">**AngleArc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)
-   [<span data-ttu-id="773b0-109">**Arc**</span><span class="sxs-lookup"><span data-stu-id="773b0-109">**Arc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arc)
-   [<span data-ttu-id="773b0-110">**ArcTo**</span><span class="sxs-lookup"><span data-stu-id="773b0-110">**ArcTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arcto)
-   [<span data-ttu-id="773b0-111">**Chord**</span><span class="sxs-lookup"><span data-stu-id="773b0-111">**Chord**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-chord)
-   [<span data-ttu-id="773b0-112">**CloseFigure**</span><span class="sxs-lookup"><span data-stu-id="773b0-112">**CloseFigure**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)
-   [<span data-ttu-id="773b0-113">**Elipse**</span><span class="sxs-lookup"><span data-stu-id="773b0-113">**Ellipse**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)
-   [<span data-ttu-id="773b0-114">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="773b0-114">**ExtTextOut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [<span data-ttu-id="773b0-115">**LineTo**</span><span class="sxs-lookup"><span data-stu-id="773b0-115">**LineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-lineto)
-   [<span data-ttu-id="773b0-116">**MoveToEx**</span><span class="sxs-lookup"><span data-stu-id="773b0-116">**MoveToEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)
-   [<span data-ttu-id="773b0-117">**Gráfico circular**</span><span class="sxs-lookup"><span data-stu-id="773b0-117">**Pie**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-pie)
-   [<span data-ttu-id="773b0-118">**Polibézier**</span><span class="sxs-lookup"><span data-stu-id="773b0-118">**PolyBezier**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)
-   [<span data-ttu-id="773b0-119">**Polibézierto**</span><span class="sxs-lookup"><span data-stu-id="773b0-119">**PolyBezierTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)
-   [<span data-ttu-id="773b0-120">**Polidraw**</span><span class="sxs-lookup"><span data-stu-id="773b0-120">**PolyDraw**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)
-   [<span data-ttu-id="773b0-121">**Polygon**</span><span class="sxs-lookup"><span data-stu-id="773b0-121">**Polygon**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polygon)
-   [<span data-ttu-id="773b0-122">**Polyline**</span><span class="sxs-lookup"><span data-stu-id="773b0-122">**Polyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polyline)
-   [<span data-ttu-id="773b0-123">**Polilineto**</span><span class="sxs-lookup"><span data-stu-id="773b0-123">**PolylineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)
-   [<span data-ttu-id="773b0-124">**Polipolígono**</span><span class="sxs-lookup"><span data-stu-id="773b0-124">**PolyPolygon**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)
-   [<span data-ttu-id="773b0-125">**Polipolyline**</span><span class="sxs-lookup"><span data-stu-id="773b0-125">**PolyPolyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)
-   [<span data-ttu-id="773b0-126">**Rectángulo**</span><span class="sxs-lookup"><span data-stu-id="773b0-126">**Rectangle**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-rectangle)
-   [<span data-ttu-id="773b0-127">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="773b0-127">**RoundRect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)
-   [<span data-ttu-id="773b0-128">**TextOut**</span><span class="sxs-lookup"><span data-stu-id="773b0-128">**TextOut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

<span data-ttu-id="773b0-129">Cuando una aplicación llama a [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), el sistema selecciona la ruta de acceso asociada al controlador de dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="773b0-129">When an application calls [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), the system selects the associated path into the specified DC.</span></span> <span data-ttu-id="773b0-130">(Si anteriormente se había seleccionado otra ruta de acceso en el controlador de dominio, el sistema la elimina sin guardarla). Una vez que el sistema selecciona la ruta de acceso en el controlador de dominio, una aplicación puede operar en la ruta de uno de los siguientes modos:</span><span class="sxs-lookup"><span data-stu-id="773b0-130">(If another path had previously been selected into the DC, the system deletes that path without saving it.) After the system selects the path into the DC, an application can operate on the path in one of the following ways:</span></span>

-   <span data-ttu-id="773b0-131">Dibuja el contorno del trazado (usando el lápiz actual).</span><span class="sxs-lookup"><span data-stu-id="773b0-131">Draw the outline of the path (using the current pen).</span></span>
-   <span data-ttu-id="773b0-132">Pinte el interior del trazado (usando el pincel actual).</span><span class="sxs-lookup"><span data-stu-id="773b0-132">Paint the interior of the path (using the current brush).</span></span>
-   <span data-ttu-id="773b0-133">Dibuje el contorno y rellene el interior del trazado.</span><span class="sxs-lookup"><span data-stu-id="773b0-133">Draw the outline and fill the interior of the path.</span></span>
-   <span data-ttu-id="773b0-134">Modifique la ruta de acceso (convirtiendo las curvas en segmentos de línea).</span><span class="sxs-lookup"><span data-stu-id="773b0-134">Modify the path (converting curves to line segments).</span></span>
-   <span data-ttu-id="773b0-135">Convierta la ruta de acceso en una ruta de acceso de clip.</span><span class="sxs-lookup"><span data-stu-id="773b0-135">Convert the path into a clip path.</span></span>
-   <span data-ttu-id="773b0-136">Convierta la ruta de acceso en una región.</span><span class="sxs-lookup"><span data-stu-id="773b0-136">Convert the path into a region.</span></span>
-   <span data-ttu-id="773b0-137">Acople la ruta de acceso convirtiendo cada curva del trazado en una serie de segmentos de línea.</span><span class="sxs-lookup"><span data-stu-id="773b0-137">Flatten the path by converting each curve in the path into a series of line segments.</span></span>
-   <span data-ttu-id="773b0-138">Recupera las coordenadas de las líneas y curvas que componen una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="773b0-138">Retrieve the coordinates of the lines and curves that compose a path.</span></span>

 

 



