---
title: Usar curvas y superficies de NURBS
description: Las funciones no uniformes de la spline B (NURBS) proporcionan descripciones generales y eficaces de curvas y superficies en dos y tres dimensiones, convirtiendo las curvas y las superficies en evaluadores de OpenGL.
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- Utilidad OpenGL (GLU), B-spline racional no uniforme (NURBS)
- GLU (utilidad OpenGL), B-spline racional no uniforme (NURBS)
- OpenGL B-spline no uniforme (NURBS)
- NURBS (no uniforme, B-spline racional) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f85e9a2045c417007c34d714ae6635ebfaf1180
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356903"
---
# <a name="using-nurbs-curves-and-surfaces"></a><span data-ttu-id="024af-107">Usar curvas y superficies de NURBS</span><span class="sxs-lookup"><span data-stu-id="024af-107">Using NURBS Curves and Surfaces</span></span>

<span data-ttu-id="024af-108">Las funciones no uniformes de la spline B (NURBS) proporcionan descripciones generales y eficaces de curvas y superficies en dos y tres dimensiones, convirtiendo las curvas y las superficies en evaluadores de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="024af-108">Non-Uniform Rational B-Spline (NURBS) functions provide general and powerful descriptions of curves and surfaces in two and three dimensions, converting the curves and surfaces to OpenGL evaluators.</span></span> <span data-ttu-id="024af-109">Las funciones de NURBS pueden representar geometría en muchos sistemas de diseño mecánico asistidos por PC.</span><span class="sxs-lookup"><span data-stu-id="024af-109">The NURBS functions can represent geometry in many computer-aided mechanical design systems.</span></span> <span data-ttu-id="024af-110">Pueden representar curvas y superficies en una variedad de estilos, y pueden controlar automáticamente la subdivisión adaptable que tessellates el dominio en triángulos más pequeños en regiones de bordes de gran curvatura y de siluetas cercanos.</span><span class="sxs-lookup"><span data-stu-id="024af-110">They can render curves and surfaces in a variety of styles, and they can automatically handle adaptive subdivision that tessellates the domain into smaller triangles in regions of high curvature and near silhouette edges.</span></span> <span data-ttu-id="024af-111">Las funciones de NURBS se dividen en las siguientes categorías.</span><span class="sxs-lookup"><span data-stu-id="024af-111">NURBS functions fall into the following categories.</span></span>

<span data-ttu-id="024af-112">Para administrar un objeto NURBS, use:</span><span class="sxs-lookup"><span data-stu-id="024af-112">To manage a NURBS object, use:</span></span>

-   <span data-ttu-id="024af-113">[**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (crear un objeto NURBS)</span><span class="sxs-lookup"><span data-stu-id="024af-113">[**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (create a NURBS object)</span></span>
-   <span data-ttu-id="024af-114">[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (elimina un objeto NURBS)</span><span class="sxs-lookup"><span data-stu-id="024af-114">[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (deletes a NURBS object)</span></span>
-   <span data-ttu-id="024af-115">[*gluNurbsCallback*](glunurbs.md) (establece una función de control de errores)</span><span class="sxs-lookup"><span data-stu-id="024af-115">[*gluNurbsCallback*](glunurbs.md) (establishes an error-handling function)</span></span>

<span data-ttu-id="024af-116">Para especificar las curvas deseadas, use:</span><span class="sxs-lookup"><span data-stu-id="024af-116">To specify the desired curves, use:</span></span>

-   [<span data-ttu-id="024af-117">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="024af-117">**gluBeginCurve**</span></span>](glubegincurve.md)
-   [<span data-ttu-id="024af-118">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="024af-118">**gluNurbsCurve**</span></span>](glunurbscurve.md)
-   [<span data-ttu-id="024af-119">**gluEndCurve**</span><span class="sxs-lookup"><span data-stu-id="024af-119">**gluEndCurve**</span></span>](gluendcurve.md)

<span data-ttu-id="024af-120">Para especificar las superficies deseadas, use:</span><span class="sxs-lookup"><span data-stu-id="024af-120">To specify the desired surfaces, use:</span></span>

-   [<span data-ttu-id="024af-121">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="024af-121">**gluBeginSurface**</span></span>](glubeginsurface.md)
-   [<span data-ttu-id="024af-122">**gluNurbsSurface**</span><span class="sxs-lookup"><span data-stu-id="024af-122">**gluNurbsSurface**</span></span>](glunurbssurface.md)
-   [<span data-ttu-id="024af-123">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="024af-123">**gluEndSurface**</span></span>](gluendsurface.md)

<span data-ttu-id="024af-124">También puede especificar una región de recorte, que define un subconjunto del dominio de la superficie de NURBS que se va a evaluar para que pueda crear superficies que tengan límites suaves o que contengan huecos.</span><span class="sxs-lookup"><span data-stu-id="024af-124">You can also specify a trimming region, which defines a subset of the NURBS surface domain to be evaluated so you can create surfaces that have smooth boundaries or that contain holes.</span></span>

<span data-ttu-id="024af-125">Para especificar la región de recorte, use:</span><span class="sxs-lookup"><span data-stu-id="024af-125">To specify the trimming region, use:</span></span>

-   [<span data-ttu-id="024af-126">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="024af-126">**gluBeginTrim**</span></span>](glubegintrim.md)
-   [<span data-ttu-id="024af-127">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="024af-127">**gluPwlCurve**</span></span>](glupwlcurve.md)
-   [<span data-ttu-id="024af-128">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="024af-128">**gluNurbsCurve**</span></span>](glunurbscurve.md)
-   [<span data-ttu-id="024af-129">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="024af-129">**gluEndTrim**</span></span>](gluendtrim.md)

<span data-ttu-id="024af-130">Al igual que con los objetos quadric, puede controlar cómo se representan las curvas y curvas de NURBS.</span><span class="sxs-lookup"><span data-stu-id="024af-130">As with quadric objects, you can control how NURBS curves and surfaces are rendered.</span></span> <span data-ttu-id="024af-131">Puede determinar:</span><span class="sxs-lookup"><span data-stu-id="024af-131">You can determine:</span></span>

-   <span data-ttu-id="024af-132">Si se va a descartar una curva o superficie cuyo control polyhedron se encuentre fuera de la ventanilla actual.</span><span class="sxs-lookup"><span data-stu-id="024af-132">Whether to discard a curve or surface whose control polyhedron lies outside the current viewport.</span></span>
-   <span data-ttu-id="024af-133">La longitud máxima (en píxeles) de los bordes de polígonos que se usan para representar curvas y superficies.</span><span class="sxs-lookup"><span data-stu-id="024af-133">The maximum length (in pixels) of edges of polygons used to render curves and surfaces.</span></span>
-   <span data-ttu-id="024af-134">Si va a tomar la matriz de proyección, la matriz de MODELVIEW y la ventanilla del servidor OpenGL o proporcionarlas explícitamente con [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).</span><span class="sxs-lookup"><span data-stu-id="024af-134">Whether you will take the projection matrix, modelview matrix, and viewport from the OpenGL server or supply them explictly with [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).</span></span>

<span data-ttu-id="024af-135">Use [**gluNurbsProperty**](glunurbsproperty.md) para establecer estas propiedades o use los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="024af-135">Use [**gluNurbsProperty**](glunurbsproperty.md) to set these properties, or use the default values.</span></span> <span data-ttu-id="024af-136">Puede consultar un objeto NURBS sobre su estilo de representación con [**gluGetNurbsProperty**](glugetnurbsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="024af-136">You can query a NURBS object about its rendering style with [**gluGetNurbsProperty**](glugetnurbsproperty.md).</span></span>

 

 




