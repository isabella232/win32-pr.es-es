---
title: Trasladar comandos de borrado de pantalla y de búfer
description: OpenGL reemplaza una variedad de funciones claras de la contabilidad de IRIS (como zclear, aclear, sclear, etc.) con una sola función, glClear. Especifique exactamente lo que desea borrar pasando las máscaras a glClear.
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- Migración de la contabilidad de IRIS, borrar funciones
- portabilidad desde IRIS GL, borrar funciones
- trasladar a OpenGL desde IRIS GL, borrar funciones
- Exportación de OpenGL desde IRIS GL, borrar funciones
- borrar funciones
- Migración de la contabilidad de IRIS, comandos de borrado de pantalla
- portabilidad desde IRIS GL, comandos de borrado de pantalla
- trasladar a OpenGL desde IRIS GL, comandos de borrado de pantalla
- Exportación de OpenGL desde IRIS GL, comandos de borrado de pantalla
- comandos de borrado de pantalla
- Migración de la contabilidad de IRIS, comandos de borrado de búfer
- portabilidad desde IRIS GL, comandos de borrado de búfer
- trasladar a OpenGL desde IRIS GL, comandos de borrado de búfer
- Exportación de OpenGL desde IRIS GL, comandos de borrado de búfer
- comandos de borrado de búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53566c9fe14922f3965133cef9e30cbea4548b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665689"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a><span data-ttu-id="f3e0f-119">Trasladar comandos de borrado de pantalla y de búfer</span><span class="sxs-lookup"><span data-stu-id="f3e0f-119">Porting Screen and Buffer Clearing Commands</span></span>

<span data-ttu-id="f3e0f-120">OpenGL reemplaza una variedad de funciones **claras** de la contabilidad de iris (como **zclear**, **aclear**, **sclear**, etc.) con una sola función, [**glClear**](glclear.md).</span><span class="sxs-lookup"><span data-stu-id="f3e0f-120">OpenGL replaces a variety of IRIS GL **clear** functions (such as **zclear**, **aclear**, **sclear**, and so on) with a single function, [**glClear**](glclear.md).</span></span> <span data-ttu-id="f3e0f-121">Especifique exactamente lo que desea borrar pasando las máscaras a **glClear**.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-121">Specify exactly what you want to clear by passing masks to **glClear**.</span></span>

<span data-ttu-id="f3e0f-122">Tenga en cuenta los siguientes puntos al trasladar comandos de pantalla y de búfer:</span><span class="sxs-lookup"><span data-stu-id="f3e0f-122">Keep the following points in mind when porting screen and buffer commands:</span></span>

-   <span data-ttu-id="f3e0f-123">OpenGL mantiene los colores de borrado por separado de los colores de dibujo, con llamadas como [**glClearColor**](glclearcolor.md) y [**glClearIndex**](glclearindex.md).</span><span class="sxs-lookup"><span data-stu-id="f3e0f-123">OpenGL maintains clearing colors separately from drawing colors, with calls like [**glClearColor**](glclearcolor.md) and [**glClearIndex**](glclearindex.md).</span></span> <span data-ttu-id="f3e0f-124">Asegúrese de establecer el color Clear para cada búfer antes de borrarlo.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-124">Be sure to set the clear color for each buffer before clearing.</span></span>
-   <span data-ttu-id="f3e0f-125">En lugar de usar una de varias llamadas claras con un nombre diferente, ahora se borran varios búferes con una llamada, [**glClear**](glclear.md), y se agrupan las **máscaras de búfer** .</span><span class="sxs-lookup"><span data-stu-id="f3e0f-125">Instead of using one of several differently named clear calls, you now clear several buffers with one call, [**glClear**](glclear.md), by **OR** ing together buffer masks.</span></span> <span data-ttu-id="f3e0f-126">Por ejemplo, **czclear** se reemplaza por:</span><span class="sxs-lookup"><span data-stu-id="f3e0f-126">For example, **czclear** is replaced by:</span></span>

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   <span data-ttu-id="f3e0f-127">IRIS GL hace referencia al punteado de polígono y al color writemask.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-127">IRIS GL references the polygon stipple and the color writemask.</span></span> <span data-ttu-id="f3e0f-128">OpenGL omite el punteado de polígono, pero hace referencia al color writemask.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-128">OpenGL ignores the polygon stipple but references the color writemask.</span></span> <span data-ttu-id="f3e0f-129">(La función **czclear** omite los dos elementos de polígono y writemask de color).</span><span class="sxs-lookup"><span data-stu-id="f3e0f-129">(The **czclear** function ignores both the polygon stipple and the color writemask.)</span></span>

<span data-ttu-id="f3e0f-130">En la tabla siguiente se enumeran las distintas funciones Clear GL de IRIS con sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-130">The following table lists the various IRIS GL clear functions with their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="f3e0f-131">Llamada de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="f3e0f-131">IRIS GL call</span></span>         | <span data-ttu-id="f3e0f-132">Llamada de OpenGL</span><span class="sxs-lookup"><span data-stu-id="f3e0f-132">OpenGL call</span></span>                                                               | <span data-ttu-id="f3e0f-133">Significado</span><span class="sxs-lookup"><span data-stu-id="f3e0f-133">Meaning</span></span>                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="f3e0f-134">**acbuf**(AC \_ claro)</span><span class="sxs-lookup"><span data-stu-id="f3e0f-134">**acbuf**(AC\_CLEAR)</span></span> | <span data-ttu-id="f3e0f-135">**glClear**(bit de búfer de la acumulación de GL \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="f3e0f-135">**glClear**( GL\_ACCUM\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="f3e0f-136">Borre el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-136">Clear the accumulation buffer.</span></span>                    |
|                      | <span data-ttu-id="f3e0f-137">**glClearColor**</span><span class="sxs-lookup"><span data-stu-id="f3e0f-137">**glClearColor**</span></span>                                                          | <span data-ttu-id="f3e0f-138">Establezca el color libre de RGBA.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-138">Set the RGBA clear color.</span></span>                         |
|                      | <span data-ttu-id="f3e0f-139">**glClearIndex**</span><span class="sxs-lookup"><span data-stu-id="f3e0f-139">**glClearIndex**</span></span>                                                          | <span data-ttu-id="f3e0f-140">Establezca el índice de color claro.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-140">Set the clear-color index.</span></span>                        |
| <span data-ttu-id="f3e0f-141">**clear**</span><span class="sxs-lookup"><span data-stu-id="f3e0f-141">**clear**</span></span>            | <span data-ttu-id="f3e0f-142">**glClear**(bit de búfer de color de contabilidad \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="f3e0f-142">**glClear**( GL\_COLOR\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="f3e0f-143">Borre el búfer de color.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-143">Clear the color buffer.</span></span>                           |
|                      | <span data-ttu-id="f3e0f-144">**glClearDepth**</span><span class="sxs-lookup"><span data-stu-id="f3e0f-144">**glClearDepth**</span></span>                                                          | <span data-ttu-id="f3e0f-145">Especifique el valor sin cifrar para el búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-145">Specify the clear value for the depth buffer.</span></span>     |
| <span data-ttu-id="f3e0f-146">**zclear**</span><span class="sxs-lookup"><span data-stu-id="f3e0f-146">**zclear**</span></span>           | <span data-ttu-id="f3e0f-147">**glClear**(bit de búfer de profundidad de contabilidad \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="f3e0f-147">**glClear**( GL\_DEPTH\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="f3e0f-148">Borre el búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-148">Clear the depth buffer.</span></span>                           |
| <span data-ttu-id="f3e0f-149">**czclear**</span><span class="sxs-lookup"><span data-stu-id="f3e0f-149">**czclear**</span></span>          | <span data-ttu-id="f3e0f-150">**glClear**(bit de búfer de \_ \_ \_ \| \_ profundidad \_ \_ del búfer de color de GL)</span><span class="sxs-lookup"><span data-stu-id="f3e0f-150">**glClear**( GL\_COLOR\_BUFFER\_BIT \|GL\_DEPTH\_BUFFER\_BIT )</span></span><br/> | <span data-ttu-id="f3e0f-151">Borre el búfer de color y el búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-151">Clear the color buffer and the depth buffer.</span></span>      |
|                      | <span data-ttu-id="f3e0f-152">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="f3e0f-152">**glClearAccum**</span></span>                                                          | <span data-ttu-id="f3e0f-153">Especifique los valores claros para el búfer de acumulación.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-153">Specify clear values for the accumulation buffer.</span></span> |
|                      | <span data-ttu-id="f3e0f-154">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="f3e0f-154">**glClearStencil**</span></span>                                                        | <span data-ttu-id="f3e0f-155">Especifique el valor sin cifrar para el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-155">Specify the clear value for the stencil buffer.</span></span>   |
| <span data-ttu-id="f3e0f-156">**sclear**</span><span class="sxs-lookup"><span data-stu-id="f3e0f-156">**sclear**</span></span>           | <span data-ttu-id="f3e0f-157">**glClear**(bit de búfer de estarcido de GL \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="f3e0f-157">**glClear**( GL\_STENCIL\_BUFFER\_BIT )</span></span>                                   | <span data-ttu-id="f3e0f-158">Borrar el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-158">Clear the stencil buffer.</span></span>                         |



 

<span data-ttu-id="f3e0f-159">Cuando el código de la contabilidad de IRIS usa **gclear** y **sclear**, puede combinarlos en una sola llamada a **glClear** ; puede mejorar el rendimiento del programa.</span><span class="sxs-lookup"><span data-stu-id="f3e0f-159">When your IRIS GL code uses both **gclear** and **sclear**, you can combine them into a single **glClear** call; can improve your program's performance.</span></span>

 

 





