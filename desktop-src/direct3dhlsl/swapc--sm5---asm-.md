---
title: swapc (SM5-ASM)
description: Realiza un intercambio condicional en componentes de los valores entre dos registros de entrada.
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d2ee674a1cb1067594b0e96c739ff8df73b152
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996912"
---
# <a name="swapc-sm5---asm"></a><span data-ttu-id="de437-103">swapc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="de437-103">swapc (sm5 - asm)</span></span>

<span data-ttu-id="de437-104">Realiza un intercambio condicional en componentes de los valores entre dos registros de entrada.</span><span class="sxs-lookup"><span data-stu-id="de437-104">Performs a component-wise conditional swap of the values between two input registers.</span></span>



| <span data-ttu-id="de437-105">swapc dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle \] , src2 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="de437-105">swapc dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="de437-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="de437-106">Item</span></span>                                                               | <span data-ttu-id="de437-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="de437-107">Description</span></span>                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de437-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="de437-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="de437-109">\[en \] el registro con máscaras de escritura no vacías arbitrarias.</span><span class="sxs-lookup"><span data-stu-id="de437-109">\[in\] Register with arbitrary nonempty write masks.</span></span> <span data-ttu-id="de437-110">Debe ser diferente de *dest1*.</span><span class="sxs-lookup"><span data-stu-id="de437-110">Must be different than *dest1*.</span></span><br/> |
| <span data-ttu-id="de437-111"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="de437-111"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="de437-112">\[en \] el registro con máscaras de escritura no vacías arbitrarias.</span><span class="sxs-lookup"><span data-stu-id="de437-112">\[in\] Register with arbitrary nonempty write masks.</span></span> <span data-ttu-id="de437-113">Debe ser diferente de *dest0*.</span><span class="sxs-lookup"><span data-stu-id="de437-113">Must be different than *dest0*.</span></span><br/> |
| <span data-ttu-id="de437-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="de437-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="de437-115">\[en \] proporciona 4 condiciones.</span><span class="sxs-lookup"><span data-stu-id="de437-115">\[in\] Provides 4 conditions.</span></span> <span data-ttu-id="de437-116">Un valor entero distinto de cero significa **true**.</span><span class="sxs-lookup"><span data-stu-id="de437-116">A nonzero integer value means **true**.</span></span> <br/>               |
| <span data-ttu-id="de437-117"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="de437-117"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="de437-118">\[en \] uno de los valores que se van a intercambiar.</span><span class="sxs-lookup"><span data-stu-id="de437-118">\[in\] One of the values to be swapped.</span></span><br/>                                              |
| <span data-ttu-id="de437-119"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="de437-119"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/>    | <span data-ttu-id="de437-120">\[en \] uno de los valores que se van a intercambiar.</span><span class="sxs-lookup"><span data-stu-id="de437-120">\[in\] One of the values to be swapped.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="de437-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de437-121">Remarks</span></span>

<span data-ttu-id="de437-122">La codificación de esta instrucción intenta expresar de forma compacta varios intercambios condicionales paralelos de escalares en registros de componentes 2 4, con una flexibilidad menor en la disposición de los pares de números implicados en el intercambio.</span><span class="sxs-lookup"><span data-stu-id="de437-122">The encoding of this instruction attempts to compactly express multiple parallel conditional swaps of scalars across two 4-component registers, with minor flexibility in the arrangement of the pairs of numbers involved in swapping.</span></span>

<span data-ttu-id="de437-123">La elección del registro y el valor para *src0*, *SRC1* y *src2* no están restringidos de ningún modo, como [MOVC](movc--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="de437-123">The choice of register and value for *src0*, *src1*, and *src2* are unconstrained in any way, like [movc](movc--sm4---asm-.md).</span></span>

<span data-ttu-id="de437-124">La semántica de esta instrucción se puede describir mediante las operaciones equivalentes con la instrucción **MOVC** .</span><span class="sxs-lookup"><span data-stu-id="de437-124">The semantics of this instruction can be described by the equivalent operations with the **movc** instruction.</span></span> <span data-ttu-id="de437-125">El peor de los casos se muestra en el ejemplo siguiente, asegurándose de que los registros de destino no se actualizan hasta el final.</span><span class="sxs-lookup"><span data-stu-id="de437-125">The worst case is shown in the following example, making sure destination registers are not updated until the end.</span></span>

``` syntax
                swapc dest0[.mask], 
                      dest1[.mask],
                      src0[.swizzle],
                      src1[.swizzle],
                      src2[.swizzle]

                expands to:

                movc temp[dest0 s mask], 
                     src0[.swizzle], 
                     src2[.swizzle], src1[.swizzle]

                movc dest1[.mask], 
                     src0[.swizzle], 
                     src1[.swizzle], src2[.swizzle]

                mov  dest0.mask, temp
```

<span data-ttu-id="de437-126">Puede elegir cómo abordar la tarea, si no directamente.</span><span class="sxs-lookup"><span data-stu-id="de437-126">You can choose how to tackle the task, if not directly.</span></span> <span data-ttu-id="de437-127">Por ejemplo, se puede lograr el mismo efecto mediante una secuencia de hasta 4 intercambios condicionales simples escalares, o como arriba, dos instrucciones **MOVC** vectoriales, además de cualquier sobrecarga para asegurarse de que los valores de origen no se clobbered por operaciones anteriores en medio de la expansión.</span><span class="sxs-lookup"><span data-stu-id="de437-127">For example, the same effect can be achieved by a sequence of up to 4 simple scalar conditional swaps, or as above, two vector **movc** instructions, plus any overhead to make sure the source values are not clobbered by earlier operations in the midst of the expansion.</span></span>

<span data-ttu-id="de437-128">Use esta instrucción para la ordenación.</span><span class="sxs-lookup"><span data-stu-id="de437-128">Use this instruction for sorting.</span></span>

<span data-ttu-id="de437-129">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="de437-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="de437-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="de437-130">Vertex</span></span> | <span data-ttu-id="de437-131">Casco</span><span class="sxs-lookup"><span data-stu-id="de437-131">Hull</span></span> | <span data-ttu-id="de437-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="de437-132">Domain</span></span> | <span data-ttu-id="de437-133">Geometría</span><span class="sxs-lookup"><span data-stu-id="de437-133">Geometry</span></span> | <span data-ttu-id="de437-134">Píxel</span><span class="sxs-lookup"><span data-stu-id="de437-134">Pixel</span></span> | <span data-ttu-id="de437-135">Compute</span><span class="sxs-lookup"><span data-stu-id="de437-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="de437-136">X</span><span class="sxs-lookup"><span data-stu-id="de437-136">X</span></span>      | <span data-ttu-id="de437-137">X</span><span class="sxs-lookup"><span data-stu-id="de437-137">X</span></span>    | <span data-ttu-id="de437-138">X</span><span class="sxs-lookup"><span data-stu-id="de437-138">X</span></span>      | <span data-ttu-id="de437-139">X</span><span class="sxs-lookup"><span data-stu-id="de437-139">X</span></span>        | <span data-ttu-id="de437-140">X</span><span class="sxs-lookup"><span data-stu-id="de437-140">X</span></span>     | <span data-ttu-id="de437-141">X</span><span class="sxs-lookup"><span data-stu-id="de437-141">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="de437-142">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="de437-142">Minimum Shader Model</span></span>

<span data-ttu-id="de437-143">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="de437-143">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="de437-144">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="de437-144">Shader Model</span></span>                                              | <span data-ttu-id="de437-145">Compatible</span><span class="sxs-lookup"><span data-stu-id="de437-145">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="de437-146">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="de437-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="de437-147">sí</span><span class="sxs-lookup"><span data-stu-id="de437-147">yes</span></span>       |
| [<span data-ttu-id="de437-148">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="de437-148">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="de437-149">no</span><span class="sxs-lookup"><span data-stu-id="de437-149">no</span></span>        |
| [<span data-ttu-id="de437-150">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="de437-150">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="de437-151">no</span><span class="sxs-lookup"><span data-stu-id="de437-151">no</span></span>        |
| [<span data-ttu-id="de437-152">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de437-152">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="de437-153">no</span><span class="sxs-lookup"><span data-stu-id="de437-153">no</span></span>        |
| [<span data-ttu-id="de437-154">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de437-154">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="de437-155">no</span><span class="sxs-lookup"><span data-stu-id="de437-155">no</span></span>        |
| [<span data-ttu-id="de437-156">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de437-156">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="de437-157">no</span><span class="sxs-lookup"><span data-stu-id="de437-157">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="de437-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="de437-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de437-159">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de437-159">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





