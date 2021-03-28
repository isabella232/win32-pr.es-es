---
title: imm_atomic_xor (SM5-ASM)
description: XOR bit a bit insuficiente a la memoria. Devuelve el valor en memoria antes de la XOR.
ms.assetid: 310037F6-F048-4DE1-9A5C-76C919D9E68B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83503f87ef53474502b1e36ba46cfec1f782f63
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904302"
---
# <a name="imm_atomic_xor-sm5---asm"></a><span data-ttu-id="a7e83-104">IMM \_ Atomic \_ XOR (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a7e83-104">imm\_atomic\_xor (sm5 - asm)</span></span>

<span data-ttu-id="a7e83-105">XOR bit a bit insuficiente a la memoria.</span><span class="sxs-lookup"><span data-stu-id="a7e83-105">Immediate atomic bitwise XOR to memory.</span></span> <span data-ttu-id="a7e83-106">Devuelve el valor en memoria antes de la XOR.</span><span class="sxs-lookup"><span data-stu-id="a7e83-106">Returns value in memory before the XOR.</span></span>



| <span data-ttu-id="a7e83-107">IMM \_ Atomic \_ Oex dst0 \[ . \_ \_ máscara de componente único \] , dst1, dstAddress \[ . swizzle \] , src0 \[ . Select ( \_ componente)\]</span><span class="sxs-lookup"><span data-stu-id="a7e83-107">imm\_atomic\_xor dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|-------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a7e83-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a7e83-108">Item</span></span>                                                                                                           | <span data-ttu-id="a7e83-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7e83-109">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e83-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="a7e83-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="a7e83-111">\[en \] contiene el valor de *dst1* antes de XOR.</span><span class="sxs-lookup"><span data-stu-id="a7e83-111">\[in\] Contains the value from *dst1* before the XOR.</span></span><br/>                                                                  |
| <span data-ttu-id="a7e83-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="a7e83-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="a7e83-113">\[en \] una vista de acceso desordenado (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="a7e83-113">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="a7e83-114">En el sombreador de cálculo, también puede ser memoria compartida de grupo de subprocesos (g \# ).</span><span class="sxs-lookup"><span data-stu-id="a7e83-114">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="a7e83-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="a7e83-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="a7e83-116">\[en \] la dirección de memoria.</span><span class="sxs-lookup"><span data-stu-id="a7e83-116">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="a7e83-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a7e83-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="a7e83-118">Valor que se va a XOR con *dst1*.</span><span class="sxs-lookup"><span data-stu-id="a7e83-118">The value to XOR with *dst1*.</span></span><br/>                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="a7e83-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7e83-119">Remarks</span></span>

<span data-ttu-id="a7e83-120">Esta instrucción realiza un único componente XOR bit a bit de 32 bits de operando *src0* con *dst1* en 32 bits por dirección de componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="a7e83-120">This instruction performs a single component 32-bit bitwise XOR of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="a7e83-121">Si *dst1* es un u \# , se puede haber declarado como RAW, con tipo o estructurado.</span><span class="sxs-lookup"><span data-stu-id="a7e83-121">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="a7e83-122">Si tiene un tipo, debe declararse como UINT/SINT con el formato de recurso enlazado R32 \_ uint/ \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="a7e83-122">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="a7e83-123">Si *dst1* es g \# , debe declararse como RAW o Structured.</span><span class="sxs-lookup"><span data-stu-id="a7e83-123">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="a7e83-124">El valor de la memoria *dst1* antes de que se devuelva XOR a *dst0*.</span><span class="sxs-lookup"><span data-stu-id="a7e83-124">The value in *dst1* memory before the XOR is returned to *dst0*.</span></span>

<span data-ttu-id="a7e83-125">Toda la operación se realiza de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="a7e83-125">The entire operation is performed atomically.</span></span>

<span data-ttu-id="a7e83-126">El número de componentes tomado de la dirección viene determinado por la dimensionalidad del recurso declarado en *dst1*.</span><span class="sxs-lookup"><span data-stu-id="a7e83-126">The number of components taken from the address is determined by the dimensionality of the resource declared at *dst1*.</span></span>

<span data-ttu-id="a7e83-127">Si la invocación del sombreador está inactiva, para exammple si el píxel se ha descartado anteriormente en su ejecución, o si solo existe una invocación de píxeles o de ejemplo para servir como ayudante a un píxel o ejemplo real para los derivados, esta instrucción no modifica la memoria *dst1* y el valor devuelto es indefinido.</span><span class="sxs-lookup"><span data-stu-id="a7e83-127">If the shader invocation is inactive, for exammple if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="a7e83-128">Fuera del límite el direccionamiento en u \# hace que no se escriba nada en la memoria, excepto si la u \# está estructurada y el desplazamiento de bytes en el struct (componente de segundo de la dirección) está provocando el acceso fuera de los límites, todo el contenido de UAV se vuelve sin definir.</span><span class="sxs-lookup"><span data-stu-id="a7e83-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="a7e83-129">Fuera de los límites el direccionamiento en u \# o g \# hace que se devuelva un resultado no definido al sombreador de *dst0*.</span><span class="sxs-lookup"><span data-stu-id="a7e83-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="a7e83-130">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="a7e83-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a7e83-131">Vértice</span><span class="sxs-lookup"><span data-stu-id="a7e83-131">Vertex</span></span> | <span data-ttu-id="a7e83-132">Casco</span><span class="sxs-lookup"><span data-stu-id="a7e83-132">Hull</span></span> | <span data-ttu-id="a7e83-133">Dominio</span><span class="sxs-lookup"><span data-stu-id="a7e83-133">Domain</span></span> | <span data-ttu-id="a7e83-134">Geometría</span><span class="sxs-lookup"><span data-stu-id="a7e83-134">Geometry</span></span> | <span data-ttu-id="a7e83-135">Píxel</span><span class="sxs-lookup"><span data-stu-id="a7e83-135">Pixel</span></span> | <span data-ttu-id="a7e83-136">Compute</span><span class="sxs-lookup"><span data-stu-id="a7e83-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a7e83-137">X</span><span class="sxs-lookup"><span data-stu-id="a7e83-137">X</span></span>     | <span data-ttu-id="a7e83-138">X</span><span class="sxs-lookup"><span data-stu-id="a7e83-138">X</span></span>       |



 

<span data-ttu-id="a7e83-139">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a7e83-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="a7e83-140">Vértice</span><span class="sxs-lookup"><span data-stu-id="a7e83-140">Vertex</span></span> | <span data-ttu-id="a7e83-141">Casco</span><span class="sxs-lookup"><span data-stu-id="a7e83-141">Hull</span></span> | <span data-ttu-id="a7e83-142">Dominio</span><span class="sxs-lookup"><span data-stu-id="a7e83-142">Domain</span></span> | <span data-ttu-id="a7e83-143">Geometría</span><span class="sxs-lookup"><span data-stu-id="a7e83-143">Geometry</span></span> | <span data-ttu-id="a7e83-144">Píxel</span><span class="sxs-lookup"><span data-stu-id="a7e83-144">Pixel</span></span> | <span data-ttu-id="a7e83-145">Compute</span><span class="sxs-lookup"><span data-stu-id="a7e83-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a7e83-146">X</span><span class="sxs-lookup"><span data-stu-id="a7e83-146">X</span></span>      | <span data-ttu-id="a7e83-147">X</span><span class="sxs-lookup"><span data-stu-id="a7e83-147">X</span></span>    | <span data-ttu-id="a7e83-148">X</span><span class="sxs-lookup"><span data-stu-id="a7e83-148">X</span></span>      | <span data-ttu-id="a7e83-149">X</span><span class="sxs-lookup"><span data-stu-id="a7e83-149">X</span></span>        | <span data-ttu-id="a7e83-150">X</span><span class="sxs-lookup"><span data-stu-id="a7e83-150">X</span></span>     | <span data-ttu-id="a7e83-151">X</span><span class="sxs-lookup"><span data-stu-id="a7e83-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a7e83-152">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a7e83-152">Minimum Shader Model</span></span>

<span data-ttu-id="a7e83-153">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a7e83-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a7e83-154">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a7e83-154">Shader Model</span></span>                                              | <span data-ttu-id="a7e83-155">Compatible</span><span class="sxs-lookup"><span data-stu-id="a7e83-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a7e83-156">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a7e83-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a7e83-157">sí</span><span class="sxs-lookup"><span data-stu-id="a7e83-157">yes</span></span>       |
| [<span data-ttu-id="a7e83-158">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a7e83-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a7e83-159">no</span><span class="sxs-lookup"><span data-stu-id="a7e83-159">no</span></span>        |
| [<span data-ttu-id="a7e83-160">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a7e83-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a7e83-161">no</span><span class="sxs-lookup"><span data-stu-id="a7e83-161">no</span></span>        |
| [<span data-ttu-id="a7e83-162">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a7e83-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a7e83-163">no</span><span class="sxs-lookup"><span data-stu-id="a7e83-163">no</span></span>        |
| [<span data-ttu-id="a7e83-164">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a7e83-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a7e83-165">no</span><span class="sxs-lookup"><span data-stu-id="a7e83-165">no</span></span>        |
| [<span data-ttu-id="a7e83-166">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a7e83-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a7e83-167">no</span><span class="sxs-lookup"><span data-stu-id="a7e83-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a7e83-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a7e83-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7e83-169">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a7e83-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





