---
title: Trasladar greset
description: OpenGL reemplaza la función de contabilidad de IRIS, greset, con las funciones, glPushAttrib y glPopAttrib.
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- Puerto de GL de IRIS, variables de estado
- portabilidad de IRIS GL, variables de estado
- trasladar a OpenGL desde IRIS GL, variables de estado
- Exportación de OpenGL desde IRIS GL, variables de estado
- variables de estado
- Migración de la contabilidad de IRIS, función greset
- portabilidad de IRIS GL, función greset
- portabilidad a OpenGL desde IRIS GL, función greset
- Exportación de OpenGL desde IRIS GL, función greset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078482f47dcaf7fd5f84605e2e0fa32d0cf14729
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418883"
---
# <a name="porting-greset"></a><span data-ttu-id="46803-112">Trasladar greset</span><span class="sxs-lookup"><span data-stu-id="46803-112">Porting greset</span></span>

<span data-ttu-id="46803-113">OpenGL reemplaza la función de contabilidad de IRIS, **greset**, con las funciones, [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="46803-113">OpenGL replaces the IRIS GL function, **greset**, with the functions, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="46803-114">Use estas funciones para guardar y restaurar grupos de variables de estado.</span><span class="sxs-lookup"><span data-stu-id="46803-114">Use these functions to save and restore groups of state variables.</span></span> <span data-ttu-id="46803-115">Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="46803-115">For example,</span></span>

``` syntax
void glPushAttrib( GLbitfield mask );
```

<span data-ttu-id="46803-116">En este ejemplo se toma una operación OR bit a bit de constantes simbólicas, que indican qué grupos de variables de estado se van a enviar a una pila de atributos.</span><span class="sxs-lookup"><span data-stu-id="46803-116">This example takes a bitwise OR of symbolic constants, indicating which groups of state variables to push onto an attribute stack.</span></span> <span data-ttu-id="46803-117">Cada constante hace referencia a un grupo de variables de estado.</span><span class="sxs-lookup"><span data-stu-id="46803-117">Each constant refers to a group of state variables.</span></span> <span data-ttu-id="46803-118">En la tabla siguiente se muestran los grupos de atributos con sus nombres de constantes simbólicos equivalentes.</span><span class="sxs-lookup"><span data-stu-id="46803-118">The following table shows the attribute groups with their equivalent symbolic constant names.</span></span> <span data-ttu-id="46803-119">Para obtener una lista completa de las variables de estado de OpenGL asociadas a cada constante, vea [**glPushAttrib**](glpushattrib.md).</span><span class="sxs-lookup"><span data-stu-id="46803-119">For a complete list of the OpenGL state variables associated with each constant, see [**glPushAttrib**](glpushattrib.md).</span></span>



| <span data-ttu-id="46803-120">Atributo</span><span class="sxs-lookup"><span data-stu-id="46803-120">Attribute</span></span>                       | <span data-ttu-id="46803-121">Constante</span><span class="sxs-lookup"><span data-stu-id="46803-121">Constant</span></span>                  |
|---------------------------------|---------------------------|
| <span data-ttu-id="46803-122">valor de eliminación de búfer de acumulación</span><span class="sxs-lookup"><span data-stu-id="46803-122">accumulation buffer clear value</span></span> | <span data-ttu-id="46803-123">\_bit de \_ búfer de acumulación de GL \_</span><span class="sxs-lookup"><span data-stu-id="46803-123">GL\_ACCUM\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="46803-124">búfer de color</span><span class="sxs-lookup"><span data-stu-id="46803-124">color buffer</span></span>                    | <span data-ttu-id="46803-125">\_bit de \_ búfer de color de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="46803-125">GL\_COLOR\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="46803-126">actuales</span><span class="sxs-lookup"><span data-stu-id="46803-126">current</span></span>                         | <span data-ttu-id="46803-127">\_bits actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="46803-127">GL\_CURRENT\_BIT</span></span>          |
| <span data-ttu-id="46803-128">búfer de profundidad</span><span class="sxs-lookup"><span data-stu-id="46803-128">depth buffer</span></span>                    | <span data-ttu-id="46803-129">\_bit de \_ búfer de profundidad de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="46803-129">GL\_DEPTH\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="46803-130">enable</span><span class="sxs-lookup"><span data-stu-id="46803-130">enable</span></span>                          | <span data-ttu-id="46803-131">\_bit de habilitación de GL \_</span><span class="sxs-lookup"><span data-stu-id="46803-131">GL\_ENABLE\_BIT</span></span>           |
| <span data-ttu-id="46803-132">evaluadores</span><span class="sxs-lookup"><span data-stu-id="46803-132">evaluators</span></span>                      | <span data-ttu-id="46803-133">\_bit de Val de EGL \_</span><span class="sxs-lookup"><span data-stu-id="46803-133">EGL\_VAL\_BIT</span></span>             |
| <span data-ttu-id="46803-134">luz</span><span class="sxs-lookup"><span data-stu-id="46803-134">fog</span></span>                             | <span data-ttu-id="46803-135">\_bit de niebla de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="46803-135">GL\_FOG\_BIT</span></span>              |
| <span data-ttu-id="46803-136">Configuración de base de \_ lista de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="46803-136">GL\_LIST\_BASE setting</span></span>          | <span data-ttu-id="46803-137">\_bit de lista de contab. \_</span><span class="sxs-lookup"><span data-stu-id="46803-137">GL\_LIST\_BIT</span></span>             |
| <span data-ttu-id="46803-138">variables de sugerencia</span><span class="sxs-lookup"><span data-stu-id="46803-138">hint variables</span></span>                  | <span data-ttu-id="46803-139">\_bit de sugerencia de GL \_</span><span class="sxs-lookup"><span data-stu-id="46803-139">GL\_HINT\_BIT</span></span>             |
| <span data-ttu-id="46803-140">variables de iluminación</span><span class="sxs-lookup"><span data-stu-id="46803-140">lighting variables</span></span>              | <span data-ttu-id="46803-141">\_bit de iluminación de GL \_</span><span class="sxs-lookup"><span data-stu-id="46803-141">GL\_LIGHTING\_BIT</span></span>         |
| <span data-ttu-id="46803-142">modo de dibujo de líneas</span><span class="sxs-lookup"><span data-stu-id="46803-142">line drawing mode</span></span>               | <span data-ttu-id="46803-143">\_bit de línea de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="46803-143">GL\_LINE\_BIT</span></span>             |
| <span data-ttu-id="46803-144">variables de modo de píxel</span><span class="sxs-lookup"><span data-stu-id="46803-144">pixel mode variables</span></span>            | <span data-ttu-id="46803-145">\_bit de \_ modo de píxel de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="46803-145">GL\_PIXEL\_MODE\_BIT</span></span>      |
| <span data-ttu-id="46803-146">variables de punto</span><span class="sxs-lookup"><span data-stu-id="46803-146">point variables</span></span>                 | <span data-ttu-id="46803-147">\_bit de punta de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="46803-147">GL\_POINT\_BIT</span></span>            |
| <span data-ttu-id="46803-148">polygon</span><span class="sxs-lookup"><span data-stu-id="46803-148">polygon</span></span>                         | <span data-ttu-id="46803-149">\_bit de polígono de GL \_</span><span class="sxs-lookup"><span data-stu-id="46803-149">GL\_POLYGON\_BIT</span></span>          |
| <span data-ttu-id="46803-150">punteado de polígono</span><span class="sxs-lookup"><span data-stu-id="46803-150">polygon stipple</span></span>                 | <span data-ttu-id="46803-151">\_bit de \_ punteado de los polígonos de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="46803-151">GL\_POLYGON\_STIPPLE\_BIT</span></span> |
| <span data-ttu-id="46803-152">tijera</span><span class="sxs-lookup"><span data-stu-id="46803-152">scissor</span></span>                         | <span data-ttu-id="46803-153">\_bit de tijera de GL \_</span><span class="sxs-lookup"><span data-stu-id="46803-153">GL\_SCISSOR\_BIT</span></span>          |
| <span data-ttu-id="46803-154">búfer de estarcido</span><span class="sxs-lookup"><span data-stu-id="46803-154">stencil buffer</span></span>                  | <span data-ttu-id="46803-155">\_bit de \_ búfer de estarcido GL \_</span><span class="sxs-lookup"><span data-stu-id="46803-155">GL\_STENCIL\_BUFFER\_BIT</span></span>  |
| <span data-ttu-id="46803-156">textura</span><span class="sxs-lookup"><span data-stu-id="46803-156">texture</span></span>                         | <span data-ttu-id="46803-157">\_bit de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="46803-157">GL\_TEXTURE\_BIT</span></span>          |
| <span data-ttu-id="46803-158">transform</span><span class="sxs-lookup"><span data-stu-id="46803-158">transform</span></span>                       | <span data-ttu-id="46803-159">\_bit de transformación de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="46803-159">GL\_TRANSFORM\_BIT</span></span>        |
| <span data-ttu-id="46803-160">ventanilla</span><span class="sxs-lookup"><span data-stu-id="46803-160">viewport</span></span>                        | <span data-ttu-id="46803-161">\_bit de ventanilla de GL \_</span><span class="sxs-lookup"><span data-stu-id="46803-161">GL\_VIEWPORT\_BIT</span></span>         |
|                                 | <span data-ttu-id="46803-162">núm. \_ todos los \_ \_ bits attrib</span><span class="sxs-lookup"><span data-stu-id="46803-162">GL\_ALL\_ATTRIB\_BITS</span></span>     |



 

<span data-ttu-id="46803-163">Para restaurar los valores de las variables de estado a los guardados con el último [**glPushAttrib**](glpushattrib.md), basta con llamar a [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="46803-163">To restore the values of the state variables to those saved with the last [**glPushAttrib**](glpushattrib.md), simply call [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="46803-164">Las variables que no guardó permanecerán sin cambios.</span><span class="sxs-lookup"><span data-stu-id="46803-164">The variables you didn't save will remain unchanged.</span></span> <span data-ttu-id="46803-165">La pila de atributo tiene una profundidad finita de al menos 16.</span><span class="sxs-lookup"><span data-stu-id="46803-165">The attribute stack has a finite depth of at least 16.</span></span>

 

 




