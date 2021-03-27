---
title: imm_atomic_exch (SM5-ASM)
description: Intercambio atómico inmediato en la memoria.
ms.assetid: D06AE57E-52A4-4579-84FF-7DE9E713A5E3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb38cd696af079c5ae7dc896db619b95dd1d1d6c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104149001"
---
# <a name="imm_atomic_exch-sm5---asm"></a><span data-ttu-id="2c8c9-103">IMM \_ Atomic \_ Exch (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2c8c9-103">imm\_atomic\_exch (sm5 - asm)</span></span>

<span data-ttu-id="2c8c9-104">Intercambio atómico inmediato en la memoria.</span><span class="sxs-lookup"><span data-stu-id="2c8c9-104">Immediate atomic exchange to memory.</span></span>



| <span data-ttu-id="2c8c9-105">IMM \_ Atomic \_ Exch dst0 \[ . una \_ \_ máscara de componente único \] , dst1, dstAddress \[ . swizzle \] , src0 \[ . Select ( \_ componente)\]</span><span class="sxs-lookup"><span data-stu-id="2c8c9-105">imm\_atomic\_exch dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2c8c9-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="2c8c9-106">Item</span></span>                                                                                                           | <span data-ttu-id="2c8c9-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c8c9-107">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8c9-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="2c8c9-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="2c8c9-109">\[en \] contiene el valor de *dst1* antes de la escritura.</span><span class="sxs-lookup"><span data-stu-id="2c8c9-109">\[in\] Contains the value from *dst1* before the write.</span></span><br/>                                                                |
| <span data-ttu-id="2c8c9-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="2c8c9-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="2c8c9-111">\[en \] una vista de acceso desordenado (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="2c8c9-111">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="2c8c9-112">En el sombreador de cálculo, también puede ser memoria compartida de grupo de subprocesos (g \# ).</span><span class="sxs-lookup"><span data-stu-id="2c8c9-112">In the Compute Shader this can also be Thread Group Shared Memory (g\#).</span></span> <br/> |
| <span data-ttu-id="2c8c9-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="2c8c9-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="2c8c9-114">\[en \] la dirección de memoria.</span><span class="sxs-lookup"><span data-stu-id="2c8c9-114">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="2c8c9-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2c8c9-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="2c8c9-116">\[en \] el valor que se va a escribir en *Dst1* en *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="2c8c9-116">\[in\] The value to write to *dst1* at *dstAddress*.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="2c8c9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c8c9-117">Remarks</span></span>

<span data-ttu-id="2c8c9-118">Esta instrucción realiza una escritura de valor de 32 bits de un solo componente de operando *src0* en *dst1* en 32 bits por dirección de componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="2c8c9-118">This instruction performs a single component 32-bit value write of operand *src0* to *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="2c8c9-119">Si *dst1* es un u \# , se puede haber declarado como RAW, con tipo o estructurado.</span><span class="sxs-lookup"><span data-stu-id="2c8c9-119">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="2c8c9-120">Si tiene un tipo, debe declararse como UINT/SINT con el formato de recurso enlazado R32 \_ uint/ \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="2c8c9-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="2c8c9-121">Si *dst1* es g \# , debe declararse como RAW o Structured.</span><span class="sxs-lookup"><span data-stu-id="2c8c9-121">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="2c8c9-122">El número de componentes tomado de la dirección viene determinado por la dimensionalidad del recurso declarado en *dst1*.</span><span class="sxs-lookup"><span data-stu-id="2c8c9-122">The number of components taken from the address is determined by the dimensionality of the resource declared at *dst1*.</span></span>

<span data-ttu-id="2c8c9-123">El valor original de 32 bits en la memoria de destino se escribe en *dst0*.</span><span class="sxs-lookup"><span data-stu-id="2c8c9-123">The original 32-bit value in the destination memory is written to *dst0*.</span></span>

<span data-ttu-id="2c8c9-124">Toda la operación se realiza de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="2c8c9-124">The entire operation is performed atomically.</span></span>

<span data-ttu-id="2c8c9-125">Si la invocación del sombreador está inactiva, por ejemplo, si el píxel se ha descartado anteriormente en su ejecución, o si solo existe una invocación de píxel/ejemplo para servir como ayudante a un píxel o ejemplo real para los derivados, esta instrucción no modifica la memoria *dst1* y el valor devuelto es indefinido.</span><span class="sxs-lookup"><span data-stu-id="2c8c9-125">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="2c8c9-126">Fuera del límite el direccionamiento en u \# hace que no se escriba nada en la memoria, excepto si la u \# está estructurada y el desplazamiento de bytes en el struct (componente de segundo de la dirección) está provocando el acceso fuera de los límites, todo el contenido de UAV se vuelve sin definir.</span><span class="sxs-lookup"><span data-stu-id="2c8c9-126">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="2c8c9-127">Fuera de los límites el direccionamiento en u \# o g \# hace que se devuelva un resultado no definido al sombreador de *dst0*.</span><span class="sxs-lookup"><span data-stu-id="2c8c9-127">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="2c8c9-128">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="2c8c9-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2c8c9-129">Vértice</span><span class="sxs-lookup"><span data-stu-id="2c8c9-129">Vertex</span></span> | <span data-ttu-id="2c8c9-130">Casco</span><span class="sxs-lookup"><span data-stu-id="2c8c9-130">Hull</span></span> | <span data-ttu-id="2c8c9-131">Dominio</span><span class="sxs-lookup"><span data-stu-id="2c8c9-131">Domain</span></span> | <span data-ttu-id="2c8c9-132">Geometría</span><span class="sxs-lookup"><span data-stu-id="2c8c9-132">Geometry</span></span> | <span data-ttu-id="2c8c9-133">Píxel</span><span class="sxs-lookup"><span data-stu-id="2c8c9-133">Pixel</span></span> | <span data-ttu-id="2c8c9-134">Compute</span><span class="sxs-lookup"><span data-stu-id="2c8c9-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2c8c9-135">X</span><span class="sxs-lookup"><span data-stu-id="2c8c9-135">X</span></span>     | <span data-ttu-id="2c8c9-136">X</span><span class="sxs-lookup"><span data-stu-id="2c8c9-136">X</span></span>       |



 

<span data-ttu-id="2c8c9-137">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2c8c9-137">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="2c8c9-138">Vértice</span><span class="sxs-lookup"><span data-stu-id="2c8c9-138">Vertex</span></span> | <span data-ttu-id="2c8c9-139">Casco</span><span class="sxs-lookup"><span data-stu-id="2c8c9-139">Hull</span></span> | <span data-ttu-id="2c8c9-140">Dominio</span><span class="sxs-lookup"><span data-stu-id="2c8c9-140">Domain</span></span> | <span data-ttu-id="2c8c9-141">Geometría</span><span class="sxs-lookup"><span data-stu-id="2c8c9-141">Geometry</span></span> | <span data-ttu-id="2c8c9-142">Píxel</span><span class="sxs-lookup"><span data-stu-id="2c8c9-142">Pixel</span></span> | <span data-ttu-id="2c8c9-143">Compute</span><span class="sxs-lookup"><span data-stu-id="2c8c9-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2c8c9-144">X</span><span class="sxs-lookup"><span data-stu-id="2c8c9-144">X</span></span>      | <span data-ttu-id="2c8c9-145">X</span><span class="sxs-lookup"><span data-stu-id="2c8c9-145">X</span></span>    | <span data-ttu-id="2c8c9-146">X</span><span class="sxs-lookup"><span data-stu-id="2c8c9-146">X</span></span>      | <span data-ttu-id="2c8c9-147">X</span><span class="sxs-lookup"><span data-stu-id="2c8c9-147">X</span></span>        | <span data-ttu-id="2c8c9-148">X</span><span class="sxs-lookup"><span data-stu-id="2c8c9-148">X</span></span>     | <span data-ttu-id="2c8c9-149">X</span><span class="sxs-lookup"><span data-stu-id="2c8c9-149">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2c8c9-150">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2c8c9-150">Minimum Shader Model</span></span>

<span data-ttu-id="2c8c9-151">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2c8c9-151">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2c8c9-152">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2c8c9-152">Shader Model</span></span>                                              | <span data-ttu-id="2c8c9-153">Compatible</span><span class="sxs-lookup"><span data-stu-id="2c8c9-153">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2c8c9-154">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2c8c9-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2c8c9-155">sí</span><span class="sxs-lookup"><span data-stu-id="2c8c9-155">yes</span></span>       |
| [<span data-ttu-id="2c8c9-156">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2c8c9-156">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2c8c9-157">no</span><span class="sxs-lookup"><span data-stu-id="2c8c9-157">no</span></span>        |
| [<span data-ttu-id="2c8c9-158">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2c8c9-158">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2c8c9-159">no</span><span class="sxs-lookup"><span data-stu-id="2c8c9-159">no</span></span>        |
| [<span data-ttu-id="2c8c9-160">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c8c9-160">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2c8c9-161">no</span><span class="sxs-lookup"><span data-stu-id="2c8c9-161">no</span></span>        |
| [<span data-ttu-id="2c8c9-162">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c8c9-162">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2c8c9-163">no</span><span class="sxs-lookup"><span data-stu-id="2c8c9-163">no</span></span>        |
| [<span data-ttu-id="2c8c9-164">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c8c9-164">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2c8c9-165">no</span><span class="sxs-lookup"><span data-stu-id="2c8c9-165">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2c8c9-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c8c9-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c8c9-167">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c8c9-167">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





