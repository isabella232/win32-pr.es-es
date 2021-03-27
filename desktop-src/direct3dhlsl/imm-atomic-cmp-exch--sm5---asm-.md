---
title: imm_atomic_cmp_exch (SM5-ASM)
description: Compare y intercambie en memoria de inmediato.
ms.assetid: 317A69E1-0E0A-45C8-8E0A-B88659ADBECC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63e1be030d7cce0d6f0a581788db39a599272b2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904300"
---
# <a name="imm_atomic_cmp_exch-sm5---asm"></a><span data-ttu-id="ea2fb-103">IMM \_ Atomic \_ CMP \_ Exch (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ea2fb-103">imm\_atomic\_cmp\_exch (sm5 - asm)</span></span>

<span data-ttu-id="ea2fb-104">Compare y intercambie en memoria de inmediato.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-104">Immediate compare and exchange to memory.</span></span>



| <span data-ttu-id="ea2fb-105">IMM \_ Atomic \_ CMP \_ Exch dst0 \[ . Single \_ Component \_ Mask \] , dst1, dstAddress \[ . swizzle \] , src0 \[ . Select \_ Component \] , SRC1 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="ea2fb-105">imm\_atomic\_cmp\_exch dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\], src1\[.select\_component\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="ea2fb-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="ea2fb-106">Item</span></span>                                                                                                           | <span data-ttu-id="ea2fb-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea2fb-107">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea2fb-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="ea2fb-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="ea2fb-109">\[out \] contiene *dst1* antes de la escritura.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-109">\[out\] Contains *dst1* before the write.</span></span><br/>                                                                              |
| <span data-ttu-id="ea2fb-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="ea2fb-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="ea2fb-111">\[en \] una vista de acceso desordenado (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="ea2fb-111">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="ea2fb-112">En el sombreador de cálculo, también puede ser memoria compartida de grupo de subprocesos (g \# ).</span><span class="sxs-lookup"><span data-stu-id="ea2fb-112">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="ea2fb-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="ea2fb-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="ea2fb-114">\[en \] la memoria de destino.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-114">\[in\] The destination memory.</span></span><br/>                                                                                         |
| <span data-ttu-id="ea2fb-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ea2fb-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="ea2fb-116">\[en \] el valor que se va a comparar con *dst1*.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-116">\[in\] The value to compare to *dst1*.</span></span><br/>                                                                                 |
| <span data-ttu-id="ea2fb-117"><span id="scr1"></span><span id="SCR1"></span>*scr1*</span><span class="sxs-lookup"><span data-stu-id="ea2fb-117"><span id="scr1"></span><span id="SCR1"></span>*scr1*</span></span><br/>                                                | <span data-ttu-id="ea2fb-118">\[en \] el valor escrito en la memoria de destino si los valores comparados son idénticos.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-118">\[in\] The value written to the destination memory if the compared values are identical.</span></span><br/>                               |



 

<span data-ttu-id="ea2fb-119">Esta instrucción realiza una comparación de valores de 32 bits de un solo componente de operando *src0* con *dst1* en 32 bits por dirección de componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-119">This instruction performs a single component 32-bit value compare of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="ea2fb-120">Si *dst1* es un u \# , se puede haber declarado como RAW, con tipo o estructurado.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-120">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="ea2fb-121">Si tiene un tipo, debe declararse como UINT/SINT con el formato de recurso enlazado R32 \_ uint/ \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-121">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="ea2fb-122">Si *dst1* es g \# , debe declararse como RAW o Structured.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-122">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="ea2fb-123">Si los valores comparados son idénticos, el valor de 32 bits de un solo componente de *SRC1* se escribe en la memoria de destino.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-123">If the compared values are identical, the single-component 32-bit value in *src1* is written to the destination memory.</span></span> <span data-ttu-id="ea2fb-124">De lo contrario, no se cambia la memoria de destino.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-124">Otherwise, the destination memory is not changed.</span></span>

<span data-ttu-id="ea2fb-125">El valor original de 32 bits en la memoria de destino siempre se escribe en *dst0*.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-125">The original 32-bit value in the destination memory is always written to *dst0*.</span></span>

<span data-ttu-id="ea2fb-126">Toda la operación se realiza de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-126">The entire operation is performed atomically.</span></span>

<span data-ttu-id="ea2fb-127">Si la invocación del sombreador está inactiva, por ejemplo, si el píxel se ha descartado anteriormente en su ejecución, o si solo existe una invocación de píxel/ejemplo para servir como ayudante a un píxel o ejemplo real para los derivados, esta instrucción no modifica la memoria *dst1* y el valor devuelto es indefinido.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="ea2fb-128">Fuera del límite el direccionamiento en u \# hace que no se escriba nada en la memoria, excepto si la u \# está estructurada y el desplazamiento de bytes en el struct (componente de segundo de la dirección) está provocando el acceso fuera de los límites, todo el contenido de UAV se vuelve sin definir.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="ea2fb-129">Fuera de los límites el direccionamiento en u \# o g \# hace que se devuelva un resultado no definido al sombreador de *dst0*.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="ea2fb-130">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="ea2fb-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ea2fb-131">Vértice</span><span class="sxs-lookup"><span data-stu-id="ea2fb-131">Vertex</span></span> | <span data-ttu-id="ea2fb-132">Casco</span><span class="sxs-lookup"><span data-stu-id="ea2fb-132">Hull</span></span> | <span data-ttu-id="ea2fb-133">Dominio</span><span class="sxs-lookup"><span data-stu-id="ea2fb-133">Domain</span></span> | <span data-ttu-id="ea2fb-134">Geometría</span><span class="sxs-lookup"><span data-stu-id="ea2fb-134">Geometry</span></span> | <span data-ttu-id="ea2fb-135">Píxel</span><span class="sxs-lookup"><span data-stu-id="ea2fb-135">Pixel</span></span> | <span data-ttu-id="ea2fb-136">Compute</span><span class="sxs-lookup"><span data-stu-id="ea2fb-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ea2fb-137">X</span><span class="sxs-lookup"><span data-stu-id="ea2fb-137">X</span></span>     | <span data-ttu-id="ea2fb-138">X</span><span class="sxs-lookup"><span data-stu-id="ea2fb-138">X</span></span>       |



 

<span data-ttu-id="ea2fb-139">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ea2fb-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="ea2fb-140">Vértice</span><span class="sxs-lookup"><span data-stu-id="ea2fb-140">Vertex</span></span> | <span data-ttu-id="ea2fb-141">Casco</span><span class="sxs-lookup"><span data-stu-id="ea2fb-141">Hull</span></span> | <span data-ttu-id="ea2fb-142">Dominio</span><span class="sxs-lookup"><span data-stu-id="ea2fb-142">Domain</span></span> | <span data-ttu-id="ea2fb-143">Geometría</span><span class="sxs-lookup"><span data-stu-id="ea2fb-143">Geometry</span></span> | <span data-ttu-id="ea2fb-144">Píxel</span><span class="sxs-lookup"><span data-stu-id="ea2fb-144">Pixel</span></span> | <span data-ttu-id="ea2fb-145">Compute</span><span class="sxs-lookup"><span data-stu-id="ea2fb-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ea2fb-146">X</span><span class="sxs-lookup"><span data-stu-id="ea2fb-146">X</span></span>      | <span data-ttu-id="ea2fb-147">X</span><span class="sxs-lookup"><span data-stu-id="ea2fb-147">X</span></span>    | <span data-ttu-id="ea2fb-148">X</span><span class="sxs-lookup"><span data-stu-id="ea2fb-148">X</span></span>      | <span data-ttu-id="ea2fb-149">X</span><span class="sxs-lookup"><span data-stu-id="ea2fb-149">X</span></span>        | <span data-ttu-id="ea2fb-150">X</span><span class="sxs-lookup"><span data-stu-id="ea2fb-150">X</span></span>     | <span data-ttu-id="ea2fb-151">X</span><span class="sxs-lookup"><span data-stu-id="ea2fb-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ea2fb-152">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="ea2fb-152">Minimum Shader Model</span></span>

<span data-ttu-id="ea2fb-153">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="ea2fb-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ea2fb-154">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ea2fb-154">Shader Model</span></span>                                              | <span data-ttu-id="ea2fb-155">Compatible</span><span class="sxs-lookup"><span data-stu-id="ea2fb-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ea2fb-156">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ea2fb-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ea2fb-157">sí</span><span class="sxs-lookup"><span data-stu-id="ea2fb-157">yes</span></span>       |
| [<span data-ttu-id="ea2fb-158">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ea2fb-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ea2fb-159">no</span><span class="sxs-lookup"><span data-stu-id="ea2fb-159">no</span></span>        |
| [<span data-ttu-id="ea2fb-160">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ea2fb-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ea2fb-161">no</span><span class="sxs-lookup"><span data-stu-id="ea2fb-161">no</span></span>        |
| [<span data-ttu-id="ea2fb-162">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ea2fb-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ea2fb-163">no</span><span class="sxs-lookup"><span data-stu-id="ea2fb-163">no</span></span>        |
| [<span data-ttu-id="ea2fb-164">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ea2fb-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ea2fb-165">no</span><span class="sxs-lookup"><span data-stu-id="ea2fb-165">no</span></span>        |
| [<span data-ttu-id="ea2fb-166">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ea2fb-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ea2fb-167">no</span><span class="sxs-lookup"><span data-stu-id="ea2fb-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ea2fb-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea2fb-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea2fb-169">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ea2fb-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





