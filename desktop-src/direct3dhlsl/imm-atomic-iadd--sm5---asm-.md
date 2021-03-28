---
title: imm_atomic_iadd (SM5-ASM)
description: Entero atómico inmediato agregar a la memoria. Devuelve el valor de la memoria antes de la suma.
ms.assetid: 24136B4C-D37C-4449-A318-57145BB8D8E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2695e23707fb61cd576748e2e83829cd7dc65259
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419961"
---
# <a name="imm_atomic_iadd-sm5---asm"></a><span data-ttu-id="56dc4-104">IMM \_ Atomic \_ iadd (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="56dc4-104">imm\_atomic\_iadd (sm5 - asm)</span></span>

<span data-ttu-id="56dc4-105">Entero atómico inmediato agregar a la memoria.</span><span class="sxs-lookup"><span data-stu-id="56dc4-105">Immediate atomic integer add to memory.</span></span> <span data-ttu-id="56dc4-106">Devuelve el valor de la memoria antes de la suma.</span><span class="sxs-lookup"><span data-stu-id="56dc4-106">Returns the value in memory before the add.</span></span>



| <span data-ttu-id="56dc4-107">IMM \_ Atomic \_ iadd dst0 \[ . \_ \_ máscara de componente único \] , dst1, dstAddress \[ . swizzle \] , src0 \[ . Select ( \_ componente)\]</span><span class="sxs-lookup"><span data-stu-id="56dc4-107">imm\_atomic\_iadd dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="56dc4-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="56dc4-108">Item</span></span>                                                                                                           | <span data-ttu-id="56dc4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="56dc4-109">Description</span></span>                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56dc4-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="56dc4-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="56dc4-111">\[en \] contiene el valor de *dst1* antes de la escritura.</span><span class="sxs-lookup"><span data-stu-id="56dc4-111">\[in\] Contains the value in *dst1* before the write.</span></span> <br/>                                                                           |
| <span data-ttu-id="56dc4-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="56dc4-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="56dc4-113">Este valor debe ser una vista de acceso desordenado (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="56dc4-113">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="56dc4-114">En el sombreador de cálculo, también puede ser memoria compartida de grupo de subprocesos (g \# ).</span><span class="sxs-lookup"><span data-stu-id="56dc4-114">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="56dc4-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="56dc4-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="56dc4-116">\[en \] la memoria naddress.</span><span class="sxs-lookup"><span data-stu-id="56dc4-116">\[in\] The memory naddress.</span></span><br/>                                                                                                      |
| <span data-ttu-id="56dc4-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="56dc4-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="56dc4-118">\[en \] el valor que se va a agregar a *dst1*.</span><span class="sxs-lookup"><span data-stu-id="56dc4-118">\[in\] The value to add to *dst1*.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="56dc4-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56dc4-119">Remarks</span></span>

<span data-ttu-id="56dc4-120">Esta instrucción realiza una adición de entero de 32 bits de un solo componente de *src0* de operando con *dst1* en 32 bits por dirección de componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="56dc4-120">This instruction performs a single component 32-bit integer add of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span> <span data-ttu-id="56dc4-121">No distingue la firma.</span><span class="sxs-lookup"><span data-stu-id="56dc4-121">It is insensitive to sign.</span></span>

<span data-ttu-id="56dc4-122">Si *dst1* es un u \# , se puede haber declarado como RAW, con tipo o estructurado.</span><span class="sxs-lookup"><span data-stu-id="56dc4-122">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="56dc4-123">Si tiene un tipo, debe declararse como UINT/SINT con el formato de recurso enlazado R32 \_ uint/ \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="56dc4-123">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="56dc4-124">Si *dst1* es g \# , debe declararse como RAW o Structured.</span><span class="sxs-lookup"><span data-stu-id="56dc4-124">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="56dc4-125">El valor de la memoria *dst1* antes de la adición se devuelve a *dst0*.</span><span class="sxs-lookup"><span data-stu-id="56dc4-125">The value in *dst1* memory before addition is returned to *dst0*.</span></span>

<span data-ttu-id="56dc4-126">La dimensionalidad de *dst1* determina el número de componentes tomados de la dirección.</span><span class="sxs-lookup"><span data-stu-id="56dc4-126">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="56dc4-127">Toda la operación se realiza de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="56dc4-127">The entire operation is performed atomically.</span></span>

<span data-ttu-id="56dc4-128">Si la invocación del sombreador está inactiva, por ejemplo, si el píxel se ha descartado anteriormente en su ejecución, o si solo existe una invocación de píxel/ejemplo para servir como ayudante a un píxel o ejemplo real para los derivados, esta instrucción no modifica la memoria *dst1* y el valor devuelto es indefinido.</span><span class="sxs-lookup"><span data-stu-id="56dc4-128">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="56dc4-129">Fuera del límite el direccionamiento en u \# hace que no se escriba nada en la memoria, excepto si la u \# está estructurada y el desplazamiento de bytes en el struct (componente de segundo de la dirección) está provocando el acceso fuera de los límites, todo el contenido de UAV se vuelve sin definir.</span><span class="sxs-lookup"><span data-stu-id="56dc4-129">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="56dc4-130">Fuera de los límites el direccionamiento en u \# o g \# hace que se devuelva un resultado no definido al sombreador de *dst0*.</span><span class="sxs-lookup"><span data-stu-id="56dc4-130">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="56dc4-131">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="56dc4-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="56dc4-132">Vértice</span><span class="sxs-lookup"><span data-stu-id="56dc4-132">Vertex</span></span> | <span data-ttu-id="56dc4-133">Casco</span><span class="sxs-lookup"><span data-stu-id="56dc4-133">Hull</span></span> | <span data-ttu-id="56dc4-134">Dominio</span><span class="sxs-lookup"><span data-stu-id="56dc4-134">Domain</span></span> | <span data-ttu-id="56dc4-135">Geometría</span><span class="sxs-lookup"><span data-stu-id="56dc4-135">Geometry</span></span> | <span data-ttu-id="56dc4-136">Píxel</span><span class="sxs-lookup"><span data-stu-id="56dc4-136">Pixel</span></span> | <span data-ttu-id="56dc4-137">Compute</span><span class="sxs-lookup"><span data-stu-id="56dc4-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="56dc4-138">X</span><span class="sxs-lookup"><span data-stu-id="56dc4-138">X</span></span>     | <span data-ttu-id="56dc4-139">X</span><span class="sxs-lookup"><span data-stu-id="56dc4-139">X</span></span>       |



 

<span data-ttu-id="56dc4-140">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="56dc4-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="56dc4-141">Vértice</span><span class="sxs-lookup"><span data-stu-id="56dc4-141">Vertex</span></span> | <span data-ttu-id="56dc4-142">Casco</span><span class="sxs-lookup"><span data-stu-id="56dc4-142">Hull</span></span> | <span data-ttu-id="56dc4-143">Dominio</span><span class="sxs-lookup"><span data-stu-id="56dc4-143">Domain</span></span> | <span data-ttu-id="56dc4-144">Geometría</span><span class="sxs-lookup"><span data-stu-id="56dc4-144">Geometry</span></span> | <span data-ttu-id="56dc4-145">Píxel</span><span class="sxs-lookup"><span data-stu-id="56dc4-145">Pixel</span></span> | <span data-ttu-id="56dc4-146">Compute</span><span class="sxs-lookup"><span data-stu-id="56dc4-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="56dc4-147">X</span><span class="sxs-lookup"><span data-stu-id="56dc4-147">X</span></span>      | <span data-ttu-id="56dc4-148">X</span><span class="sxs-lookup"><span data-stu-id="56dc4-148">X</span></span>    | <span data-ttu-id="56dc4-149">X</span><span class="sxs-lookup"><span data-stu-id="56dc4-149">X</span></span>      | <span data-ttu-id="56dc4-150">X</span><span class="sxs-lookup"><span data-stu-id="56dc4-150">X</span></span>        | <span data-ttu-id="56dc4-151">X</span><span class="sxs-lookup"><span data-stu-id="56dc4-151">X</span></span>     | <span data-ttu-id="56dc4-152">X</span><span class="sxs-lookup"><span data-stu-id="56dc4-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="56dc4-153">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="56dc4-153">Minimum Shader Model</span></span>

<span data-ttu-id="56dc4-154">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="56dc4-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="56dc4-155">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="56dc4-155">Shader Model</span></span>                                              | <span data-ttu-id="56dc4-156">Compatible</span><span class="sxs-lookup"><span data-stu-id="56dc4-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="56dc4-157">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="56dc4-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="56dc4-158">sí</span><span class="sxs-lookup"><span data-stu-id="56dc4-158">yes</span></span>       |
| [<span data-ttu-id="56dc4-159">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="56dc4-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="56dc4-160">no</span><span class="sxs-lookup"><span data-stu-id="56dc4-160">no</span></span>        |
| [<span data-ttu-id="56dc4-161">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="56dc4-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="56dc4-162">no</span><span class="sxs-lookup"><span data-stu-id="56dc4-162">no</span></span>        |
| [<span data-ttu-id="56dc4-163">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56dc4-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="56dc4-164">no</span><span class="sxs-lookup"><span data-stu-id="56dc4-164">no</span></span>        |
| [<span data-ttu-id="56dc4-165">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56dc4-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="56dc4-166">no</span><span class="sxs-lookup"><span data-stu-id="56dc4-166">no</span></span>        |
| [<span data-ttu-id="56dc4-167">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56dc4-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="56dc4-168">no</span><span class="sxs-lookup"><span data-stu-id="56dc4-168">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="56dc4-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56dc4-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56dc4-170">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56dc4-170">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





