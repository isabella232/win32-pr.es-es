---
title: dmovc (SM5-ASM)
description: Movimiento condicional por componente. | dmovc (SM5-ASM)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e364e6340733c42ae69412db726851329eb2809d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424199"
---
# <a name="dmovc-sm5---asm"></a><span data-ttu-id="67258-104">dmovc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="67258-104">dmovc (sm5 - asm)</span></span>

<span data-ttu-id="67258-105">Movimiento condicional por componente.</span><span class="sxs-lookup"><span data-stu-id="67258-105">Component-wise conditional move.</span></span>



| <span data-ttu-id="67258-106">dmovc \[ \_ SAT \] dest \[ . Mask \] , src0 \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="67258-106">dmovc\[\_sat\] dest\[.mask\], src0\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\],</span></span> |
|-----------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="67258-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="67258-107">Item</span></span>                                                            | <span data-ttu-id="67258-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="67258-108">Description</span></span>                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67258-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="67258-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="67258-110">\[en \] el destino de movimiento.</span><span class="sxs-lookup"><span data-stu-id="67258-110">\[in\] The move destination.</span></span><br/> <span data-ttu-id="67258-111">Si *src0*, *dest*  =  *SRC1* else *dest*  =  *src2*.</span><span class="sxs-lookup"><span data-stu-id="67258-111">If *src0*, then *dest* = *src1* else *dest* = *src2*.</span></span><br/> |
| <span data-ttu-id="67258-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="67258-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="67258-113">\[en \] los componentes de los que se va a probar la condición.</span><span class="sxs-lookup"><span data-stu-id="67258-113">\[in\] The components to test the condition against.</span></span><br/>                                          |
| <span data-ttu-id="67258-114"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="67258-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="67258-115">\[en \] los componentes que se van a desplace si la condición es true.</span><span class="sxs-lookup"><span data-stu-id="67258-115">\[in\] The components to move if the condition is true.</span></span><br/>                                       |
| <span data-ttu-id="67258-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="67258-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="67258-117">\[en \] los componentes que se van a desplace si la condición es falsa.</span><span class="sxs-lookup"><span data-stu-id="67258-117">\[in\] The components to move if the condition is false.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="67258-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67258-118">Remarks</span></span>

<span data-ttu-id="67258-119">En el ejemplo siguiente se muestra cómo utilizar esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="67258-119">The following example shows how to use this instruction.</span></span>

``` syntax
                if(the dest mask contains .xy)
                {
                    if(the first 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the first double from src1 (post swizzle)
                        into dest.xy
                    }
                    else
                    {
                        copy the first double from src2 (post swizzle)
                        into dest.xy
                    }
                }
                if(the dest mask contains .zw)
                {
                    if(the second 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the second double from src1 (post swizzle)
                        into dest.zw
                    }
                    else
                    {
                        copy the second double from src2 (post swizzle)
                        into dest.zw
                    }
                }
```

<span data-ttu-id="67258-120">Las máscaras válidas para dest son. XY,. ZW,. xyzw.</span><span class="sxs-lookup"><span data-stu-id="67258-120">The valid masks for dest are .xy, .zw, .xyzw.</span></span>

<span data-ttu-id="67258-121">El valor de swizzles válido para *src0* es cualquier cosa.</span><span class="sxs-lookup"><span data-stu-id="67258-121">The valid swizzles for *src0* are anything.</span></span> <span data-ttu-id="67258-122">Los dos primeros componentes posteriores a swizzle se usan para facilite los valores de condición de 2 32 bits.</span><span class="sxs-lookup"><span data-stu-id="67258-122">The first two components post-swizzle are used to indentify two 32-bit condition values.</span></span>

<span data-ttu-id="67258-123">El valor de swizzles válido para *SRC1* y *src2* que contienen valores double es. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="67258-123">The valid swizzles for *src1* and *src2* containing doubles are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="67258-124">son. XY,. ZW y. xyzw.</span><span class="sxs-lookup"><span data-stu-id="67258-124">are .xy, .zw, and .xyzw.</span></span>

<span data-ttu-id="67258-125">Las siguientes asignaciones de *src* son posteriores a swizzle:</span><span class="sxs-lookup"><span data-stu-id="67258-125">The following *src* mappings below are post-swizzle:</span></span>

-   <span data-ttu-id="67258-126">*dest* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="67258-126">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="67258-127">*src0* es un vec2 de 32 bits/componente en x e y (ZW omitido).</span><span class="sxs-lookup"><span data-stu-id="67258-127">*src0* is a 32bit/component vec2 across x and y (zw ignored).</span></span>
-   <span data-ttu-id="67258-128">*SRC1* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="67258-128">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="67258-129">*src2* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="67258-129">*src2* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="67258-130">Los modificadores de *SRC1* y *src2*, excepto swizzle, suponen que los datos son Double.</span><span class="sxs-lookup"><span data-stu-id="67258-130">The modifiers on *src1* and *src2*, other than swizzle, assume the data is double.</span></span> <span data-ttu-id="67258-131">La ausencia de modificadores mueve los datos sin modificar los bits.</span><span class="sxs-lookup"><span data-stu-id="67258-131">The absence of modifiers moves data without altering bits.</span></span>

<span data-ttu-id="67258-132">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="67258-132">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="67258-133">Vértice</span><span class="sxs-lookup"><span data-stu-id="67258-133">Vertex</span></span> | <span data-ttu-id="67258-134">Casco</span><span class="sxs-lookup"><span data-stu-id="67258-134">Hull</span></span> | <span data-ttu-id="67258-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="67258-135">Domain</span></span> | <span data-ttu-id="67258-136">Geometría</span><span class="sxs-lookup"><span data-stu-id="67258-136">Geometry</span></span> | <span data-ttu-id="67258-137">Píxel</span><span class="sxs-lookup"><span data-stu-id="67258-137">Pixel</span></span> | <span data-ttu-id="67258-138">Compute</span><span class="sxs-lookup"><span data-stu-id="67258-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="67258-139">X</span><span class="sxs-lookup"><span data-stu-id="67258-139">X</span></span>      | <span data-ttu-id="67258-140">X</span><span class="sxs-lookup"><span data-stu-id="67258-140">X</span></span>    | <span data-ttu-id="67258-141">X</span><span class="sxs-lookup"><span data-stu-id="67258-141">X</span></span>      | <span data-ttu-id="67258-142">X</span><span class="sxs-lookup"><span data-stu-id="67258-142">X</span></span>        | <span data-ttu-id="67258-143">X</span><span class="sxs-lookup"><span data-stu-id="67258-143">X</span></span>     | <span data-ttu-id="67258-144">X</span><span class="sxs-lookup"><span data-stu-id="67258-144">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="67258-145">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="67258-145">Minimum Shader Model</span></span>

<span data-ttu-id="67258-146">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="67258-146">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="67258-147">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="67258-147">Shader Model</span></span>                                              | <span data-ttu-id="67258-148">Compatible</span><span class="sxs-lookup"><span data-stu-id="67258-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="67258-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="67258-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="67258-150">sí</span><span class="sxs-lookup"><span data-stu-id="67258-150">yes</span></span>       |
| [<span data-ttu-id="67258-151">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="67258-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="67258-152">no</span><span class="sxs-lookup"><span data-stu-id="67258-152">no</span></span>        |
| [<span data-ttu-id="67258-153">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="67258-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="67258-154">no</span><span class="sxs-lookup"><span data-stu-id="67258-154">no</span></span>        |
| [<span data-ttu-id="67258-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67258-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="67258-156">no</span><span class="sxs-lookup"><span data-stu-id="67258-156">no</span></span>        |
| [<span data-ttu-id="67258-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67258-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="67258-158">no</span><span class="sxs-lookup"><span data-stu-id="67258-158">no</span></span>        |
| [<span data-ttu-id="67258-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67258-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="67258-160">no</span><span class="sxs-lookup"><span data-stu-id="67258-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="67258-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="67258-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67258-162">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67258-162">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





