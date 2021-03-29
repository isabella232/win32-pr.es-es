---
title: Teselar polígonos
description: Teselar polígonos
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- Utilidad OpenGL (GLU), Teselación
- GLU (utilidad OpenGL), Teselación
- Utilidad OpenGL (GLU), polígonos simples
- GLU (utilidad OpenGL), polígonos simples
- polígonos sencillos OpenGL
- Utilidad OpenGL (GLU), polígonos complejos
- GLU (utilidad OpenGL), polígonos complejos
- polígonos complejos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475076f6372042d61c1662b445b7573709134c65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665728"
---
# <a name="tessellating-polygons"></a><span data-ttu-id="861d7-111">Teselar polígonos</span><span class="sxs-lookup"><span data-stu-id="861d7-111">Tessellating Polygons</span></span>

<span data-ttu-id="861d7-112">OpenGL puede mostrar directamente solo polígonos convexo sencillos.</span><span class="sxs-lookup"><span data-stu-id="861d7-112">OpenGL can directly display only simple convex polygons.</span></span> <span data-ttu-id="861d7-113">Un polígono es sencillo si:</span><span class="sxs-lookup"><span data-stu-id="861d7-113">A polygon is simple if:</span></span>

-   <span data-ttu-id="861d7-114">Los bordes solo se cruzan en los vértices.</span><span class="sxs-lookup"><span data-stu-id="861d7-114">The edges intersect only at vertices.</span></span>
-   <span data-ttu-id="861d7-115">No hay vértices duplicados.</span><span class="sxs-lookup"><span data-stu-id="861d7-115">There are no duplicate vertices.</span></span>
-   <span data-ttu-id="861d7-116">Exactamente dos bordes se encuentran en cualquier vértice.</span><span class="sxs-lookup"><span data-stu-id="861d7-116">Exactly two edges meet at any vertex.</span></span>

<span data-ttu-id="861d7-117">Para mostrar polígonos sencillos o polígonos simples que contienen huecos, primero debe triangular los polígonos (subdividirlos en polígonos convexa).</span><span class="sxs-lookup"><span data-stu-id="861d7-117">To display simple nonconvex polygons or simple polygons containing holes, you must first triangulate the polygons (subdivide them into convex polygons).</span></span> <span data-ttu-id="861d7-118">Esta subdivisión se denomina *teselación*.</span><span class="sxs-lookup"><span data-stu-id="861d7-118">Such subdivision is called *tessellation*.</span></span> <span data-ttu-id="861d7-119">GLU proporciona una colección de funciones que realizan la teselación.</span><span class="sxs-lookup"><span data-stu-id="861d7-119">GLU provides a collection of functions that perform tessellation.</span></span> <span data-ttu-id="861d7-120">Tenga en cuenta que las funciones de teselación GLU no pueden controlar polígonos no simples; no hay ningún método OpenGL estándar para controlar estos polígonos.</span><span class="sxs-lookup"><span data-stu-id="861d7-120">Note that the GLU tessellation functions can't handle nonsimple polygons; there is no standard OpenGL method to handle such polygons.</span></span>

<span data-ttu-id="861d7-121">Dado que la teselación suele ser necesaria y puede ser bastante complicada, en esta sección se describen en detalle las funciones de teselación GLU.</span><span class="sxs-lookup"><span data-stu-id="861d7-121">Because tessellation is often required and can be rather tricky, this section describes the GLU tessellation functions in detail.</span></span> <span data-ttu-id="861d7-122">Estas funciones toman como entrada polígonos simples arbitrarios que pueden incluir agujeros y devuelven una combinación de triángulos, mallas de triángulo y ventiladores de triángulo.</span><span class="sxs-lookup"><span data-stu-id="861d7-122">These functions take as input arbitrary simple polygons that might include holes, and they return some combination of triangles, triangle meshes, and triangle fans.</span></span> <span data-ttu-id="861d7-123">Si no desea trabajar con mallas ni ventiladores, puede especificar que las funciones de teselación devuelvan solo triángulos.</span><span class="sxs-lookup"><span data-stu-id="861d7-123">If you don't want to deal with meshes or fans, you can specify that the tessellation functions return only triangles.</span></span> <span data-ttu-id="861d7-124">Sin embargo, la información de la malla y del ventilador mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="861d7-124">However, mesh and fan information improves performance.</span></span> <span data-ttu-id="861d7-125">Las funciones de teselación de polígonos triangulan un polígono cóncavo con uno o varios contornos.</span><span class="sxs-lookup"><span data-stu-id="861d7-125">The polygon tessellation functions triangulate a concave polygon with one or more contours.</span></span>

<span data-ttu-id="861d7-126">**Para usar la teselación poligonal**</span><span class="sxs-lookup"><span data-stu-id="861d7-126">**To use polygon tessellation**</span></span>

1.  <span data-ttu-id="861d7-127">Cree un objeto de teselación con [**gluNewTess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="861d7-127">Create a tessellation object with [**gluNewTess**](glunewtess.md).</span></span>
2.  <span data-ttu-id="861d7-128">Use [*gluTessCallBack*](glutess.md) para definir las funciones de devolución de llamada que se usarán para procesar los triángulos generados por del teselador.</span><span class="sxs-lookup"><span data-stu-id="861d7-128">Use [*gluTessCallBack*](glutess.md) to define callback functions you will use to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="861d7-129">Con [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)y [**gluEndPolygon**](gluendpolygon.md), especifique el polígono con huecos o el polígono cóncavo que se va a teselar.</span><span class="sxs-lookup"><span data-stu-id="861d7-129">With [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md), and [**gluEndPolygon**](gluendpolygon.md), specify the polygon with holes or the concave polygon to be tessellated.</span></span>

    <span data-ttu-id="861d7-130">Una vez completada la descripción del polígono, la utilidad de teselación invoca las funciones de devolución de llamada según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="861d7-130">When the polygon description is complete, the tessellation facility invokes your callback functions as necessary.</span></span>

    <span data-ttu-id="861d7-131">Puede destruir objetos de teselación innecesarios con [**gluDeleteTess**](gludeletetess.md).</span><span class="sxs-lookup"><span data-stu-id="861d7-131">You can destroy unneeded tessellation objects with [**gluDeleteTess**](gludeletetess.md).</span></span>

<span data-ttu-id="861d7-132">Para obtener más información sobre cómo guardar los datos de teselación, vea [usar funciones de devolución de llamada](using-callback-functions.md).</span><span class="sxs-lookup"><span data-stu-id="861d7-132">For more information on saving the tessellation data, see [Using Callback Functions](using-callback-functions.md).</span></span>

 

 




