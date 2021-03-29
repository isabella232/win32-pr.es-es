---
title: Trasladar curvas de NURBS
description: Las funciones de OpenGL para dibujar curvas NURBS son muy similares a las funciones de contabilidad de IRIS. Se especifican las secuencias de nudos y los puntos de control mediante una función gluNurbsCurve, que debe estar contenida dentro de un par gluBeginCurve/gluEndCurve.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- Migración de la contabilidad de IRIS, curvas de NURBS
- trasladar de IRIS GL, curvas de NURBS
- trasladar a OpenGL desde IRIS GL, curvas de NURBS
- Exportación de OpenGL desde IRIS GL, curvas de NURBS
- Curvas NURBS
- curvas
- Migración de la contabilidad de IRIS, curvas
- trasladar de IRIS GL, curvas
- trasladar a OpenGL desde IRIS GL, curvas
- Exportación de OpenGL de IRIS GL, curvas
- NURBS (no uniforme, B-spline racional)
- B-spline racional no uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f539e466ce8ade17d135c9369e1f641831792e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418878"
---
# <a name="porting-nurbs-curves"></a><span data-ttu-id="c7f09-116">Trasladar curvas de NURBS</span><span class="sxs-lookup"><span data-stu-id="c7f09-116">Porting NURBS Curves</span></span>

<span data-ttu-id="c7f09-117">Las funciones de OpenGL para dibujar curvas NURBS son muy similares a las funciones de contabilidad de IRIS.</span><span class="sxs-lookup"><span data-stu-id="c7f09-117">The OpenGL functions for drawing NURBS curves are very similar to the IRIS GL functions.</span></span> <span data-ttu-id="c7f09-118">Se especifican las secuencias de nudos y los puntos de control mediante una función [**gluNurbsCurve**](glunurbscurve.md) , que debe estar dentro de un par gluEndCurve de [**gluBeginCurve**](glubegincurve.md)  /  [](gluendcurve.md) .</span><span class="sxs-lookup"><span data-stu-id="c7f09-118">You specify knot sequences and control points using a [**gluNurbsCurve**](glunurbscurve.md) function, which must be contained within a [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md) pair.</span></span>

<span data-ttu-id="c7f09-119">En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para dibujar curvas NURBS y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="c7f09-119">The following table lists the IRIS GL functions for drawing NURBS curves and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="c7f09-120">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="c7f09-120">IRIS GL function</span></span> | <span data-ttu-id="c7f09-121">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="c7f09-121">OpenGL function</span></span>                        | <span data-ttu-id="c7f09-122">Significado</span><span class="sxs-lookup"><span data-stu-id="c7f09-122">Meaning</span></span>                     |
|------------------|----------------------------------------|-----------------------------|
| <span data-ttu-id="c7f09-123">**bgncurve**</span><span class="sxs-lookup"><span data-stu-id="c7f09-123">**bgncurve**</span></span>     | [<span data-ttu-id="c7f09-124">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="c7f09-124">**gluBeginCurve**</span></span>](glubegincurve.md) | <span data-ttu-id="c7f09-125">Comienza una definición de curva.</span><span class="sxs-lookup"><span data-stu-id="c7f09-125">Begins a curve definition.</span></span>  |
| <span data-ttu-id="c7f09-126">**nurbscurve**</span><span class="sxs-lookup"><span data-stu-id="c7f09-126">**nurbscurve**</span></span>   | [<span data-ttu-id="c7f09-127">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="c7f09-127">**gluNurbsCurve**</span></span>](glunurbscurve.md) | <span data-ttu-id="c7f09-128">Especifica los atributos de la curva.</span><span class="sxs-lookup"><span data-stu-id="c7f09-128">Specifies curve attributes.</span></span> |
| <span data-ttu-id="c7f09-129">**endcurve**</span><span class="sxs-lookup"><span data-stu-id="c7f09-129">**endcurve**</span></span>     | [<span data-ttu-id="c7f09-130">**gluEndCurve**</span><span class="sxs-lookup"><span data-stu-id="c7f09-130">**gluEndCurve**</span></span>](gluendcurve.md)     | <span data-ttu-id="c7f09-131">Finaliza una definición de curva.</span><span class="sxs-lookup"><span data-stu-id="c7f09-131">Ends a curve definition.</span></span>    |



 

<span data-ttu-id="c7f09-132">Asocie coordenadas de posición, textura y color presentando cada una de ellas como un **gluNurbsCurve** independiente dentro del par Begin/end.</span><span class="sxs-lookup"><span data-stu-id="c7f09-132">Associate position, texture, and color coordinates by presenting each as a separate **gluNurbsCurve** inside the begin/end pair.</span></span> <span data-ttu-id="c7f09-133">No puede hacer más de una llamada a **gluNurbsCurve** para cada parte de los datos de color, posición y textura dentro de un solo par **gluBeginCurve/gluEndCurve** .</span><span class="sxs-lookup"><span data-stu-id="c7f09-133">You can make no more than one call to **gluNurbsCurve** for each piece of color, position, and texture data within a single **gluBeginCurve/gluEndCurve** pair.</span></span> <span data-ttu-id="c7f09-134">Debe hacer exactamente una llamada para describir la posición de la curva (una descripción de \_ MAP1 de vértice \_ \_ 3 o \_ GL \_ MAP1 \_ ).</span><span class="sxs-lookup"><span data-stu-id="c7f09-134">You must make exactly one call to describe the position of the curve (a GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4 description).</span></span> <span data-ttu-id="c7f09-135">Cuando se llama a **gluEndCurve**, la curva se Tesela en segmentos de línea y, a continuación, se representa.</span><span class="sxs-lookup"><span data-stu-id="c7f09-135">When you call **gluEndCurve**, the curve is tessellated into line segments and then rendered.</span></span>

<span data-ttu-id="c7f09-136">En la tabla siguiente se enumeran los tipos de curva IRIS GL y OpenGL NURBS.</span><span class="sxs-lookup"><span data-stu-id="c7f09-136">The following table lists IRIS GL and OpenGL NURBS curve types.</span></span>



| <span data-ttu-id="c7f09-137">Tipo de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="c7f09-137">IRIS GL type</span></span> | <span data-ttu-id="c7f09-138">Tipo de OpenGL</span><span class="sxs-lookup"><span data-stu-id="c7f09-138">OpenGL type</span></span>                  | <span data-ttu-id="c7f09-139">Significado</span><span class="sxs-lookup"><span data-stu-id="c7f09-139">Meaning</span></span>                                 |
|--------------|------------------------------|-----------------------------------------|
| <span data-ttu-id="c7f09-140">N \_ V3D</span><span class="sxs-lookup"><span data-stu-id="c7f09-140">N\_V3D</span></span>       | <span data-ttu-id="c7f09-141">\_ \_ Vértice \_ 3 de GL MAP1</span><span class="sxs-lookup"><span data-stu-id="c7f09-141">GL\_MAP1\_VERTEX\_3</span></span>          | <span data-ttu-id="c7f09-142">Curva polinómica.</span><span class="sxs-lookup"><span data-stu-id="c7f09-142">Polynomial curve.</span></span>                       |
| <span data-ttu-id="c7f09-143">N \_ V3DR</span><span class="sxs-lookup"><span data-stu-id="c7f09-143">N\_V3DR</span></span>      | <span data-ttu-id="c7f09-144">\_ \_ Vértice \_ 4 de GL MAP1</span><span class="sxs-lookup"><span data-stu-id="c7f09-144">GL\_MAP1\_VERTEX\_4</span></span>          | <span data-ttu-id="c7f09-145">Curva racional.</span><span class="sxs-lookup"><span data-stu-id="c7f09-145">Rational curve.</span></span>                         |
|              | <span data-ttu-id="c7f09-146">GL \_ MAP1 \_ Texture \_ coordenadas\_\*</span><span class="sxs-lookup"><span data-stu-id="c7f09-146">GL\_MAP1\_TEXTURE\_COORD\_\*</span></span> | <span data-ttu-id="c7f09-147">Los puntos de control son coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="c7f09-147">Control points are texture coordinates.</span></span> |
|              | <span data-ttu-id="c7f09-148">GL \_ MAP1 \_ normal</span><span class="sxs-lookup"><span data-stu-id="c7f09-148">GL\_MAP1\_NORMAL</span></span>             | <span data-ttu-id="c7f09-149">Los puntos de control son normales.</span><span class="sxs-lookup"><span data-stu-id="c7f09-149">Control points are normals.</span></span>             |



 

<span data-ttu-id="c7f09-150">Para obtener más información sobre los tipos de evaluador disponibles, vea [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="c7f09-150">For more information on available evaluator types, see [**glMap1**](glmap1.md).</span></span>

<span data-ttu-id="c7f09-151">??</span><span class="sxs-lookup"><span data-stu-id="c7f09-151">??</span></span>

 

 




