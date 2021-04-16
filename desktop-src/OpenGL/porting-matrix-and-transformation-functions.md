---
title: Portabilidad de funciones de transformación y de matriz
description: La administración de las matrices y las transformaciones de IRIS GL y OpenGL es similar.
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- Puerto de GL de IRIS, matrices
- portabilidad de IRIS GL, matrices
- trasladar a OpenGL desde IRIS GL, matrices
- Exportación de OpenGL desde IRIS GL, matrices
- matrices
- Migración de la contabilidad de IRIS, transformaciones
- portabilidad de IRIS GL, transformaciones
- trasladar a OpenGL desde IRIS GL, transformaciones
- Exportación de OpenGL desde IRIS GL, transformaciones
- transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6219640085370202b8dbebad9a2e9d4992b4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357357"
---
# <a name="porting-matrix-and-transformation-functions"></a><span data-ttu-id="cc12a-113">Portabilidad de funciones de transformación y de matriz</span><span class="sxs-lookup"><span data-stu-id="cc12a-113">Porting Matrix and Transformation Functions</span></span>

<span data-ttu-id="cc12a-114">La administración de las matrices y las transformaciones de IRIS GL y OpenGL es similar.</span><span class="sxs-lookup"><span data-stu-id="cc12a-114">IRIS GL and OpenGL handle matrices and transformations in a similar manner.</span></span> <span data-ttu-id="cc12a-115">Pero hay varias diferencias que hay que tener en cuenta al migrar código de IRIS GL:</span><span class="sxs-lookup"><span data-stu-id="cc12a-115">But there are several differences to keep in mind when porting code from IRIS GL:</span></span>

-   <span data-ttu-id="cc12a-116">En OpenGL siempre está en modo de doble matriz; no hay ningún modo de matriz única.</span><span class="sxs-lookup"><span data-stu-id="cc12a-116">In OpenGL you are always in double-matrix mode; there is no single-matrix mode.</span></span>
-   <span data-ttu-id="cc12a-117">Los ángulos se miden en grados, en lugar de en las décimas de grados.</span><span class="sxs-lookup"><span data-stu-id="cc12a-117">Angles are measured in degrees, instead of tenths of degrees.</span></span>
-   <span data-ttu-id="cc12a-118">Las llamadas de la matriz de proyección, como [**glFrustum**](glfrustum.md) y [**glOrtho**](glortho.md), ahora se multiplican en la matriz actual, en lugar de cargarse en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="cc12a-118">Projection matrix calls, like [**glFrustum**](glfrustum.md) and [**glOrtho**](glortho.md), now multiply onto the current matrix, instead of being loaded onto the current matrix.</span></span>
-   <span data-ttu-id="cc12a-119">La función de OpenGL, [**glRotate**](glrotate.md), es muy diferente de la **rotación**.</span><span class="sxs-lookup"><span data-stu-id="cc12a-119">The OpenGL function, [**glRotate**](glrotate.md), is very different from **rotate**.</span></span> <span data-ttu-id="cc12a-120">Puede girar alrededor de cualquier eje arbitrario, en lugar de limitarse a los ejes x, y y z.</span><span class="sxs-lookup"><span data-stu-id="cc12a-120">You can rotate around any arbitrary axis, instead of being confined to the x-, y-, and z- axes.</span></span> <span data-ttu-id="cc12a-121">Por ejemplo, puede traducir:</span><span class="sxs-lookup"><span data-stu-id="cc12a-121">For example, you can translate:</span></span>

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    <span data-ttu-id="cc12a-122">a:</span><span class="sxs-lookup"><span data-stu-id="cc12a-122">to:</span></span>

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    <span data-ttu-id="cc12a-123">Al traducir de **rotar** a **glRotate** , cambie a grados desde las décimas de grado y reemplace ' z ' con un vector para el eje z.</span><span class="sxs-lookup"><span data-stu-id="cc12a-123">When translating from **rotate** to **glRotate** you switch to degrees from tenths of degrees and replace 'z' with a vector for the z-axis.</span></span>

-   <span data-ttu-id="cc12a-124">OpenGL no tiene equivalente a la función **polarview** .</span><span class="sxs-lookup"><span data-stu-id="cc12a-124">OpenGL has no equivalent to the **polarview** function.</span></span> <span data-ttu-id="cc12a-125">Puede reemplazarlo fácilmente con una traducción y tres giros.</span><span class="sxs-lookup"><span data-stu-id="cc12a-125">You can replace it easily with a translation and three rotations.</span></span> <span data-ttu-id="cc12a-126">Por ejemplo, puede traducir:</span><span class="sxs-lookup"><span data-stu-id="cc12a-126">For example, you can translate:</span></span>

    ```C++
    polarview(distance, azimuth, incidence, twist);
     
    ```

    

    <span data-ttu-id="cc12a-127">a:</span><span class="sxs-lookup"><span data-stu-id="cc12a-127">to:</span></span>

    ```C++
    glTranslatef( 0.0, 0.0, -distance); 
    glRotatef( -twist * 10.0, 0.0, 0.0, 1.0); 
    glRotatef( -incidence * 10.0, 1.0, 0.0, 0.0); 
    glRotatef( -azimuth * 10.0, 0.0, 0.0, 1.0);
    ```

    

<span data-ttu-id="cc12a-128">En la tabla siguiente se enumeran las funciones de matriz de OpenGL y sus funciones de contabilidad de IRIS equivalentes.</span><span class="sxs-lookup"><span data-stu-id="cc12a-128">The following table lists the OpenGL matrix functions and their equivalent IRIS GL functions.</span></span>



| <span data-ttu-id="cc12a-129">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="cc12a-129">IRIS GL function</span></span>              | <span data-ttu-id="cc12a-130">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="cc12a-130">OpenGL function</span></span>                                                                        | <span data-ttu-id="cc12a-131">Significado</span><span class="sxs-lookup"><span data-stu-id="cc12a-131">Meaning</span></span>                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc12a-132">**mmode**</span><span class="sxs-lookup"><span data-stu-id="cc12a-132">**mmode**</span></span>                     | [<span data-ttu-id="cc12a-133">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="cc12a-133">**glMatrixMode**</span></span>](glmatrixmode.md)                                                   | <span data-ttu-id="cc12a-134">Establece el modo de matriz actual.</span><span class="sxs-lookup"><span data-stu-id="cc12a-134">Sets current matrix mode.</span></span>                                                                                                                                                      |
|                               | [<span data-ttu-id="cc12a-135">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="cc12a-135">**glLoadIdentity**</span></span>](glloadidentity.md)                                               | <span data-ttu-id="cc12a-136">Reemplaza la matriz actual por la matriz de identidad.</span><span class="sxs-lookup"><span data-stu-id="cc12a-136">Replaces current matrix with the identity matrix.</span></span>                                                                                                                              |
| <span data-ttu-id="cc12a-137">**loadmatrix**</span><span class="sxs-lookup"><span data-stu-id="cc12a-137">**loadmatrix**</span></span>                | <span data-ttu-id="cc12a-138">[**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="cc12a-138">[**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)</span></span><br/> | <span data-ttu-id="cc12a-139">Reemplaza la matriz actual con la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="cc12a-139">Replaces current matrix with the specified matrix.</span></span>                                                                                                                             |
| <span data-ttu-id="cc12a-140">**multmatrix**</span><span class="sxs-lookup"><span data-stu-id="cc12a-140">**multmatrix**</span></span>                | <span data-ttu-id="cc12a-141">[**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="cc12a-141">[**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)</span></span><br/> | <span data-ttu-id="cc12a-142">Post: multiplica la matriz actual con la matriz especificada (tenga en cuenta que **multmatrix** se multiplica previamente).</span><span class="sxs-lookup"><span data-stu-id="cc12a-142">Post-multiplies current matrix with the specified matrix (note that **multmatrix** pre-multiplied).</span></span>                                                                            |
| <span data-ttu-id="cc12a-143">**mapw**, **mapw2**</span><span class="sxs-lookup"><span data-stu-id="cc12a-143">**mapw**, **mapw2**</span></span>           | [<span data-ttu-id="cc12a-144">**gluUnProject**</span><span class="sxs-lookup"><span data-stu-id="cc12a-144">**gluUnProject**</span></span>](gluunproject.md)                                                   | <span data-ttu-id="cc12a-145">Proyecta las coordenadas de espacio mundial en el espacio de objeto (vea también [**gluProject**](gluproject.md)).</span><span class="sxs-lookup"><span data-stu-id="cc12a-145">Projects world-space coordinates to object space (see also [**gluProject**](gluproject.md)).</span></span>                                                                                  |
| <span data-ttu-id="cc12a-146">**ortho**</span><span class="sxs-lookup"><span data-stu-id="cc12a-146">**ortho**</span></span>                     | [<span data-ttu-id="cc12a-147">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="cc12a-147">**glOrtho**</span></span>](glortho.md)                                                             | <span data-ttu-id="cc12a-148">Multiplica la matriz actual por una matriz de proyección ortográfica.</span><span class="sxs-lookup"><span data-stu-id="cc12a-148">Multiplies current matrix by an orthographic projection matrix.</span></span>                                                                                                                |
| <span data-ttu-id="cc12a-149">**ortho2**</span><span class="sxs-lookup"><span data-stu-id="cc12a-149">**ortho2**</span></span>                    | [<span data-ttu-id="cc12a-150">**gluOrtho2D**</span><span class="sxs-lookup"><span data-stu-id="cc12a-150">**gluOrtho2D**</span></span>](gluortho2d.md)                                                       | <span data-ttu-id="cc12a-151">Define una matriz de proyección ortográfica bidimensional.</span><span class="sxs-lookup"><span data-stu-id="cc12a-151">Defines a two-dimensional orthographic projection matrix.</span></span>                                                                                                                      |
| <span data-ttu-id="cc12a-152">**vista**</span><span class="sxs-lookup"><span data-stu-id="cc12a-152">**perspective**</span></span>               | [<span data-ttu-id="cc12a-153">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="cc12a-153">**gluPerspective**</span></span>](gluperspective.md)                                               | <span data-ttu-id="cc12a-154">Define una matriz de proyección de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="cc12a-154">Defines a perspective projection matrix.</span></span>                                                                                                                                       |
| <span data-ttu-id="cc12a-155">**picksize**</span><span class="sxs-lookup"><span data-stu-id="cc12a-155">**picksize**</span></span>                  | [<span data-ttu-id="cc12a-156">**gluPickMatrix**</span><span class="sxs-lookup"><span data-stu-id="cc12a-156">**gluPickMatrix**</span></span>](glupickmatrix.md)                                                 | <span data-ttu-id="cc12a-157">Define una región de picking.</span><span class="sxs-lookup"><span data-stu-id="cc12a-157">Defines a picking region.</span></span>                                                                                                                                                      |
| <span data-ttu-id="cc12a-158">**popmatrix**</span><span class="sxs-lookup"><span data-stu-id="cc12a-158">**popmatrix**</span></span>                 | [<span data-ttu-id="cc12a-159">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="cc12a-159">**glPopMatrix**</span></span>](glpopmatrix.md)                                                     | <span data-ttu-id="cc12a-160">Extrae la pila de matriz actual, reemplazando la matriz actual por la que se encuentra debajo de ella.</span><span class="sxs-lookup"><span data-stu-id="cc12a-160">Pops current matrix stack, replacing the current matrix with the one below it.</span></span>                                                                                                 |
| <span data-ttu-id="cc12a-161">**pushmatrix**</span><span class="sxs-lookup"><span data-stu-id="cc12a-161">**pushmatrix**</span></span>                | [<span data-ttu-id="cc12a-162">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="cc12a-162">**glPushMatrix**</span></span>](glpushmatrix.md)                                                   | <span data-ttu-id="cc12a-163">Empuja la pila actual de la matriz hacia abajo en uno, duplicando la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="cc12a-163">Pushes current matrix stack down by one, duplicating the current matrix.</span></span>                                                                                                       |
| <span data-ttu-id="cc12a-164">**rotar**,**Rot**</span><span class="sxs-lookup"><span data-stu-id="cc12a-164">**rotate**,**rot**</span></span><br/> | <span data-ttu-id="cc12a-165">[**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)</span><span class="sxs-lookup"><span data-stu-id="cc12a-165">[**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)</span></span><br/>                 | <span data-ttu-id="cc12a-166">Gira el sistema de coordenadas actual por el ángulo especificado sobre el vector desde el origen hasta el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="cc12a-166">Rotates current coordinate system by the given angle about the vector from the origin through the given point.</span></span> <span data-ttu-id="cc12a-167">Tenga en cuenta que **girar** gira solo sobre los ejes x, y y z.</span><span class="sxs-lookup"><span data-stu-id="cc12a-167">Note that **rotate** rotated only about the x-, y-, and z-axes.</span></span> |
| <span data-ttu-id="cc12a-168">**scale**</span><span class="sxs-lookup"><span data-stu-id="cc12a-168">**scale**</span></span>                     | <span data-ttu-id="cc12a-169">[**glScaled**](glscale.md),[**glScalef**](glscale.md)</span><span class="sxs-lookup"><span data-stu-id="cc12a-169">[**glScaled**](glscale.md),[**glScalef**](glscale.md)</span></span><br/>                     | <span data-ttu-id="cc12a-170">Multiplica la matriz actual por una matriz de escala.</span><span class="sxs-lookup"><span data-stu-id="cc12a-170">Multiplies current matrix by a scaling matrix.</span></span>                                                                                                                                 |
| <span data-ttu-id="cc12a-171">**Traducir**</span><span class="sxs-lookup"><span data-stu-id="cc12a-171">**translate**</span></span>                 | <span data-ttu-id="cc12a-172">[**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)</span><span class="sxs-lookup"><span data-stu-id="cc12a-172">[**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)</span></span><br/>     | <span data-ttu-id="cc12a-173">Mueve el origen del sistema de coordenadas al punto especificado, multiplicando la matriz actual por una matriz de traslación.</span><span class="sxs-lookup"><span data-stu-id="cc12a-173">Moves coordinate-system origin to the point specified, by multiplying the current matrix by a translation matrix.</span></span>                                                              |
| <span data-ttu-id="cc12a-174">**ventana**</span><span class="sxs-lookup"><span data-stu-id="cc12a-174">**window**</span></span>                    | [<span data-ttu-id="cc12a-175">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="cc12a-175">**glFrustum**</span></span>](glfrustum.md)                                                         | <span data-ttu-id="cc12a-176">Las coordenadas especificadas para los planos de recorte, multiplican la matriz actual por una matriz de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="cc12a-176">Given coordinates for clipping planes, multiplies the current matrix by a perspective matrix.</span></span>                                                                                  |



 

<span data-ttu-id="cc12a-177">OpenGL tiene tres modos de matriz, que se establecen con [**glMatrixMode**](glmatrixmode.md).</span><span class="sxs-lookup"><span data-stu-id="cc12a-177">OpenGL has three matrix modes, which are set with [**glMatrixMode**](glmatrixmode.md).</span></span> <span data-ttu-id="cc12a-178">En la tabla siguiente se enumeran los modos disponibles como parámetros para **glMatrixMode**.</span><span class="sxs-lookup"><span data-stu-id="cc12a-178">The following table lists the modes available as parameters for **glMatrixMode**.</span></span>



| <span data-ttu-id="cc12a-179">Modo de matriz de contabilidad de IRIS</span><span class="sxs-lookup"><span data-stu-id="cc12a-179">IRIS GL matrix mode</span></span> | <span data-ttu-id="cc12a-180">Modo OpenGL</span><span class="sxs-lookup"><span data-stu-id="cc12a-180">OpenGL mode</span></span>    | <span data-ttu-id="cc12a-181">Significado</span><span class="sxs-lookup"><span data-stu-id="cc12a-181">Meaning</span></span>                                  | <span data-ttu-id="cc12a-182">Profundidad de pila mínima</span><span class="sxs-lookup"><span data-stu-id="cc12a-182">Min stack depth</span></span> |
|---------------------|----------------|------------------------------------------|-----------------|
| <span data-ttu-id="cc12a-183">**MTEXTURE**</span><span class="sxs-lookup"><span data-stu-id="cc12a-183">**MTEXTURE**</span></span>        | <span data-ttu-id="cc12a-184">\_textura GL</span><span class="sxs-lookup"><span data-stu-id="cc12a-184">GL\_TEXTURE</span></span>    | <span data-ttu-id="cc12a-185">Opera en la pila de la matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="cc12a-185">Operates on the texture matrix stack.</span></span>    | <span data-ttu-id="cc12a-186">2</span><span class="sxs-lookup"><span data-stu-id="cc12a-186">2</span></span>               |
| <span data-ttu-id="cc12a-187">**MVIEWING**</span><span class="sxs-lookup"><span data-stu-id="cc12a-187">**MVIEWING**</span></span>        | <span data-ttu-id="cc12a-188">GL \_ MODELVIEW</span><span class="sxs-lookup"><span data-stu-id="cc12a-188">GL\_MODELVIEW</span></span>  | <span data-ttu-id="cc12a-189">Funciona en la pila de matrices de la vista de modelo.</span><span class="sxs-lookup"><span data-stu-id="cc12a-189">Operates on the model view matrix stack.</span></span> | <span data-ttu-id="cc12a-190">32</span><span class="sxs-lookup"><span data-stu-id="cc12a-190">32</span></span>              |
| <span data-ttu-id="cc12a-191">**MPROJECTION**</span><span class="sxs-lookup"><span data-stu-id="cc12a-191">**MPROJECTION**</span></span>     | <span data-ttu-id="cc12a-192">\_proyección GL</span><span class="sxs-lookup"><span data-stu-id="cc12a-192">GL\_PROJECTION</span></span> | <span data-ttu-id="cc12a-193">Opera en la pila de la matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="cc12a-193">Operates on the projection matrix stack.</span></span> | <span data-ttu-id="cc12a-194">2</span><span class="sxs-lookup"><span data-stu-id="cc12a-194">2</span></span>               |



 

 

 





