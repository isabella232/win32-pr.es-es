---
title: imm_atomic_imin (SM5-ASM)
description: Mínimo de memoria con firma atómica. Devuelve el valor en memoria antes de la operación Max.
ms.assetid: 8E104FFA-D086-49FD-9063-B950B6B1548B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c48b39da642105cacc0936abe1874d81c88e79b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358493"
---
# <a name="imm_atomic_imin-sm5---asm"></a><span data-ttu-id="ddebc-104">IMM \_ Atomic \_ Imin (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ddebc-104">imm\_atomic\_imin (sm5 - asm)</span></span>

<span data-ttu-id="ddebc-105">Mínimo de memoria con firma atómica.</span><span class="sxs-lookup"><span data-stu-id="ddebc-105">Immediate atomic signed min to memory.</span></span> <span data-ttu-id="ddebc-106">Devuelve el valor en memoria antes de la operación Max.</span><span class="sxs-lookup"><span data-stu-id="ddebc-106">Returns value in memory before the max operation.</span></span>



| <span data-ttu-id="ddebc-107">IMM \_ Atomic \_ Imin dst0 \[ . \_ \_ máscara de componente único \] , dst1, dstAddress \[ . swizzle \] , src0 \[ . Select ( \_ componente)\]</span><span class="sxs-lookup"><span data-stu-id="ddebc-107">imm\_atomic\_imin dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="ddebc-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ddebc-108">Item</span></span>                                                                                                           | <span data-ttu-id="ddebc-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddebc-109">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddebc-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="ddebc-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="ddebc-111">\[en \] contiene el valor de *dst1* antes de esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="ddebc-111">\[in\] Contains the value from *dst1* before this instruction.</span></span><br/>                                                         |
| <span data-ttu-id="ddebc-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="ddebc-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="ddebc-113">\[en \] una vista de acceso desordenado (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="ddebc-113">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="ddebc-114">En el sombreador de cálculo, también puede ser memoria compartida de grupo de subprocesos (g \# ).</span><span class="sxs-lookup"><span data-stu-id="ddebc-114">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="ddebc-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="ddebc-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="ddebc-116">\[en \] la dirección de memoria.</span><span class="sxs-lookup"><span data-stu-id="ddebc-116">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="ddebc-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ddebc-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="ddebc-118">\[en \] el valor que se va a comparar con *Dst1* en *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="ddebc-118">\[in\] The value to compare to *dst1* at *dstAddress*.</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="ddebc-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddebc-119">Remarks</span></span>

<span data-ttu-id="ddebc-120">Esta instruccióni realiza un único componente de 32 bits con signo como mínimo del operando *src0* con *dst1* en 32 bits por dirección de componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="ddebc-120">Thisi instruction performs a single component 32-bit signed minimum of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="ddebc-121">Si *dst1* es un u \# , se puede haber declarado como RAW, con tipo o estructurado.</span><span class="sxs-lookup"><span data-stu-id="ddebc-121">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="ddebc-122">Si tiene un tipo, debe declararse como UINT/SINT con el formato de recurso enlazado R32 \_ uint/ \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="ddebc-122">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="ddebc-123">Si *dst1* es g \# , debe declararse como RAW o Structured.</span><span class="sxs-lookup"><span data-stu-id="ddebc-123">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="ddebc-124">El valor de *dst1* Memory Before min se devuelve a *dst0*.</span><span class="sxs-lookup"><span data-stu-id="ddebc-124">The value in *dst1* memory before min is returned to *dst0*.</span></span>

<span data-ttu-id="ddebc-125">La dimensionalidad de *dst1* determina el número de componentes tomados de la dirección.</span><span class="sxs-lookup"><span data-stu-id="ddebc-125">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="ddebc-126">Toda la operación se realiza de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="ddebc-126">The entire operation is performed atomically.</span></span>

<span data-ttu-id="ddebc-127">Si la invocación del sombreador está inactiva, por ejemplo, si el píxel se ha descartado anteriormente en su ejecución, o si solo existe una invocación de píxel/ejemplo para servir como ayudante a un píxel o ejemplo real para los derivados, esta instrucción no modifica la memoria *dst1* y el valor devuelto es indefinido.</span><span class="sxs-lookup"><span data-stu-id="ddebc-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="ddebc-128">Fuera del límite el direccionamiento en u \# hace que no se escriba nada en la memoria, excepto si la u \# está estructurada y el desplazamiento de bytes en el struct (componente de segundo de la dirección) está provocando el acceso fuera de los límites, todo el contenido de UAV se vuelve sin definir.</span><span class="sxs-lookup"><span data-stu-id="ddebc-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="ddebc-129">Fuera de los límites el direccionamiento en u \# o g \# hace que se devuelva un resultado no definido al sombreador de *dst0*.</span><span class="sxs-lookup"><span data-stu-id="ddebc-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="ddebc-130">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="ddebc-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ddebc-131">Vértice</span><span class="sxs-lookup"><span data-stu-id="ddebc-131">Vertex</span></span> | <span data-ttu-id="ddebc-132">Casco</span><span class="sxs-lookup"><span data-stu-id="ddebc-132">Hull</span></span> | <span data-ttu-id="ddebc-133">Dominio</span><span class="sxs-lookup"><span data-stu-id="ddebc-133">Domain</span></span> | <span data-ttu-id="ddebc-134">Geometría</span><span class="sxs-lookup"><span data-stu-id="ddebc-134">Geometry</span></span> | <span data-ttu-id="ddebc-135">Píxel</span><span class="sxs-lookup"><span data-stu-id="ddebc-135">Pixel</span></span> | <span data-ttu-id="ddebc-136">Compute</span><span class="sxs-lookup"><span data-stu-id="ddebc-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ddebc-137">X</span><span class="sxs-lookup"><span data-stu-id="ddebc-137">X</span></span>     | <span data-ttu-id="ddebc-138">X</span><span class="sxs-lookup"><span data-stu-id="ddebc-138">X</span></span>       |



 

<span data-ttu-id="ddebc-139">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ddebc-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="ddebc-140">Vértice</span><span class="sxs-lookup"><span data-stu-id="ddebc-140">Vertex</span></span> | <span data-ttu-id="ddebc-141">Casco</span><span class="sxs-lookup"><span data-stu-id="ddebc-141">Hull</span></span> | <span data-ttu-id="ddebc-142">Dominio</span><span class="sxs-lookup"><span data-stu-id="ddebc-142">Domain</span></span> | <span data-ttu-id="ddebc-143">Geometría</span><span class="sxs-lookup"><span data-stu-id="ddebc-143">Geometry</span></span> | <span data-ttu-id="ddebc-144">Píxel</span><span class="sxs-lookup"><span data-stu-id="ddebc-144">Pixel</span></span> | <span data-ttu-id="ddebc-145">Compute</span><span class="sxs-lookup"><span data-stu-id="ddebc-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ddebc-146">X</span><span class="sxs-lookup"><span data-stu-id="ddebc-146">X</span></span>      | <span data-ttu-id="ddebc-147">X</span><span class="sxs-lookup"><span data-stu-id="ddebc-147">X</span></span>    | <span data-ttu-id="ddebc-148">X</span><span class="sxs-lookup"><span data-stu-id="ddebc-148">X</span></span>      | <span data-ttu-id="ddebc-149">X</span><span class="sxs-lookup"><span data-stu-id="ddebc-149">X</span></span>        | <span data-ttu-id="ddebc-150">X</span><span class="sxs-lookup"><span data-stu-id="ddebc-150">X</span></span>     | <span data-ttu-id="ddebc-151">X</span><span class="sxs-lookup"><span data-stu-id="ddebc-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ddebc-152">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="ddebc-152">Minimum Shader Model</span></span>

<span data-ttu-id="ddebc-153">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="ddebc-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ddebc-154">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ddebc-154">Shader Model</span></span>                                              | <span data-ttu-id="ddebc-155">Compatible</span><span class="sxs-lookup"><span data-stu-id="ddebc-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ddebc-156">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ddebc-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ddebc-157">sí</span><span class="sxs-lookup"><span data-stu-id="ddebc-157">yes</span></span>       |
| [<span data-ttu-id="ddebc-158">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ddebc-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ddebc-159">no</span><span class="sxs-lookup"><span data-stu-id="ddebc-159">no</span></span>        |
| [<span data-ttu-id="ddebc-160">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ddebc-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ddebc-161">no</span><span class="sxs-lookup"><span data-stu-id="ddebc-161">no</span></span>        |
| [<span data-ttu-id="ddebc-162">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ddebc-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ddebc-163">no</span><span class="sxs-lookup"><span data-stu-id="ddebc-163">no</span></span>        |
| [<span data-ttu-id="ddebc-164">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ddebc-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ddebc-165">no</span><span class="sxs-lookup"><span data-stu-id="ddebc-165">no</span></span>        |
| [<span data-ttu-id="ddebc-166">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ddebc-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ddebc-167">no</span><span class="sxs-lookup"><span data-stu-id="ddebc-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ddebc-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ddebc-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddebc-169">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ddebc-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





