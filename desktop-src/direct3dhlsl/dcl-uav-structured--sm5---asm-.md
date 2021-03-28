---
title: dcl_uav_structured (SM5-ASM)
description: Declare una vista de acceso desordenado (UAV) para su uso por parte de un sombreador. | dcl_uav_structured (SM5-ASM)
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc02396f4837a095506e736d81ea8c00eb0669f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280016"
---
# <a name="dcl_uav_structured-sm5---asm"></a><span data-ttu-id="6cf0b-104">DCL \_ UAV \_ estructurado (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6cf0b-104">dcl\_uav\_structured (sm5 - asm)</span></span>

<span data-ttu-id="6cf0b-105">Declare una vista de acceso desordenado (UAV) para su uso por parte de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="6cf0b-106">DCL \_ UAV \_ Structured \[ \_ GLC \] dstUAV, structByteStride</span><span class="sxs-lookup"><span data-stu-id="6cf0b-106">dcl\_uav\_structured\[\_glc\] dstUAV, structByteStride</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="6cf0b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="6cf0b-107">Item</span></span>                                                                                                                                   | <span data-ttu-id="6cf0b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cf0b-108">Description</span></span>                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="6cf0b-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="6cf0b-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/>                                         | <span data-ttu-id="6cf0b-110">\[en \] UAV.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-110">\[in\] The UAV.</span></span><br/>                            |
| <span data-ttu-id="6cf0b-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span><span class="sxs-lookup"><span data-stu-id="6cf0b-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="6cf0b-112">\[en \] el tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-112">\[in\] The size of the structure in bytes.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6cf0b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6cf0b-113">Remarks</span></span>

<span data-ttu-id="6cf0b-114">*dstUAV* es un \# registro u declarado como una referencia a un UnorderedAccessView de un búfer estructurado con el intervalo especificado que se debe enlazar a la ranura UAV \# en la API.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-114">*dstUAV* is a u\# register declared as a reference to an UnorderedAccessView of a structured buffer with the specified stride that must be bound to UAV slot \# at the API.</span></span>

<span data-ttu-id="6cf0b-115">El contenido de la estructura no tiene ningún tipo; las operaciones realizadas en la memoria pueden interpretar implícitamente los datos como si tuvieran un tipo.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-115">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="6cf0b-116">*structByteStride* es el tamaño de la estructura, en bytes, del búfer que se está declarando.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-116">*structByteStride* is the size of the structure in bytes in the buffer being declared.</span></span> <span data-ttu-id="6cf0b-117">Este valor debe ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-117">This value must be greater than zero.</span></span> <span data-ttu-id="6cf0b-118">*structByteStride* es de tipo uint y debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-118">*structByteStride* is of type uint, and must be a multiple of 4.</span></span>

<span data-ttu-id="6cf0b-119">Las instrucciones que hacen referencia a una u estructurada \# toman una dirección 2D, donde el primer componente selecciona \[ struct \] , y el segundo componente selecciona \[ desplazamiento dentro de la estructura, en bytes alineados \] .</span><span class="sxs-lookup"><span data-stu-id="6cf0b-119">Instructions that reference a structured u\# take a 2D address, where the first component picks \[struct\], and the second component picks \[offset within struct, in aligned bytes\].</span></span>

<span data-ttu-id="6cf0b-120">La \_ marca GLC significa "Globally coherente".</span><span class="sxs-lookup"><span data-stu-id="6cf0b-120">The \_glc flag means for"globally coherent".</span></span> <span data-ttu-id="6cf0b-121">La ausencia de \_ GLC significa que el UAV se declara solo como "coherente con el grupo" en el sombreador de cálculo o "localmente coherente" en una invocación del sombreador de un solo píxel.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-121">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="6cf0b-122">La \_ marca OPC es el contador de conservar el orden.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-122">The \_opc flag is the order preserving counter.</span></span> <span data-ttu-id="6cf0b-123">Indica que, si un UAV está enlazado a \# la ranura (u \# ), se debe haber creado con la marca de contador.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-123">It indicates that if a UAV is bound to slot \# (u\#), it must have been created with the COUNTER flag.</span></span> <span data-ttu-id="6cf0b-124">Esto significa que las operaciones de consumo [atómico de IMM \_ \_ ](imm-atomic-alloc--sm5---asm-.md) o del [IMM \_ \_ atómico de IMM](imm-atomic-consume--sm5---asm-.md) en el sombreador manipulan un contador cuyos valores se pueden usar en el sombreador como una referencia permanente a una ubicación en el UAV.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-124">This means that [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) operations in the shader manipulate a counter whose values can be used in the shader as a permanent reference to a location in the UAV.</span></span> <span data-ttu-id="6cf0b-125">Los datos no se pueden reordenar una vez que el sombreador ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-125">Data cannot be reordered after the shader is over.</span></span>

<span data-ttu-id="6cf0b-126">La ausencia de la \_ marca OPC significa que si el sombreador usa[la \_ \_ asignación atómica de IMM](imm-atomic-alloc--sm5---asm-.md) o las instrucciones de [ \_ \_ consumo atómico de IMM](imm-atomic-consume--sm5---asm-.md) y un UAV está enlazado a la ranura \# (u), se debe haber creado con la marca append, que proporciona un contador que no garantiza que el orden se conserva después de la invocación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-126">The absence of the \_opc flag means that if the shader uses[imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) instructions and a UAV is bound to slot \# (u), it must have been created with the APPEND flag, which provides a counter that does not guarantee order is preserved after the shader invocation.</span></span>

<span data-ttu-id="6cf0b-127">Si la \_ marca OPC no está presente y el sombreador no contiene las instrucciones de uso de la [ \_ \_ asignación atómica de IMM](imm-atomic-alloc--sm5---asm-.md) o de [IMM \_ Atomic \_ ](imm-atomic-consume--sm5---asm-.md) , se permite que se haya creado un UAV enlazado a \# la ranura (u) con la marca de contador (el contador pasará a no usarse por este sombreador), sin marca (ningún contador), pero no con la marca de anexado.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-127">If the \_opc flag is absent and the shader does not contain [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) instructions, a UAV bound to slot \# (u) is permitted to have been created with the COUNTER flag (the counter will go unused by this shader), no flag (no counter), but not with the APPEND flag.</span></span>

> [!Note]  
> <span data-ttu-id="6cf0b-128">CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten la **\_ TGSM \_ de DCL**, pero no la de [DCL \_ TGSM \_ raw](dcl-tgsm-raw--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="6cf0b-128">cs\_4\_0 and cs\_4\_1 supports **dcl\_tgsm\_structured**, but not [dcl\_tgsm\_raw](dcl-tgsm-raw--sm5---asm-.md).</span></span>

 

<span data-ttu-id="6cf0b-129">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="6cf0b-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6cf0b-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="6cf0b-130">Vertex</span></span> | <span data-ttu-id="6cf0b-131">Casco</span><span class="sxs-lookup"><span data-stu-id="6cf0b-131">Hull</span></span> | <span data-ttu-id="6cf0b-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="6cf0b-132">Domain</span></span> | <span data-ttu-id="6cf0b-133">Geometría</span><span class="sxs-lookup"><span data-stu-id="6cf0b-133">Geometry</span></span> | <span data-ttu-id="6cf0b-134">Píxel</span><span class="sxs-lookup"><span data-stu-id="6cf0b-134">Pixel</span></span> | <span data-ttu-id="6cf0b-135">Compute</span><span class="sxs-lookup"><span data-stu-id="6cf0b-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6cf0b-136">X</span><span class="sxs-lookup"><span data-stu-id="6cf0b-136">X</span></span>     | <span data-ttu-id="6cf0b-137">X</span><span class="sxs-lookup"><span data-stu-id="6cf0b-137">X</span></span>       |



 

<span data-ttu-id="6cf0b-138">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-138">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="6cf0b-139">Vértice</span><span class="sxs-lookup"><span data-stu-id="6cf0b-139">Vertex</span></span> | <span data-ttu-id="6cf0b-140">Casco</span><span class="sxs-lookup"><span data-stu-id="6cf0b-140">Hull</span></span> | <span data-ttu-id="6cf0b-141">Dominio</span><span class="sxs-lookup"><span data-stu-id="6cf0b-141">Domain</span></span> | <span data-ttu-id="6cf0b-142">Geometría</span><span class="sxs-lookup"><span data-stu-id="6cf0b-142">Geometry</span></span> | <span data-ttu-id="6cf0b-143">Píxel</span><span class="sxs-lookup"><span data-stu-id="6cf0b-143">Pixel</span></span> | <span data-ttu-id="6cf0b-144">Compute</span><span class="sxs-lookup"><span data-stu-id="6cf0b-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6cf0b-145">X</span><span class="sxs-lookup"><span data-stu-id="6cf0b-145">X</span></span>      | <span data-ttu-id="6cf0b-146">X</span><span class="sxs-lookup"><span data-stu-id="6cf0b-146">X</span></span>    | <span data-ttu-id="6cf0b-147">X</span><span class="sxs-lookup"><span data-stu-id="6cf0b-147">X</span></span>      | <span data-ttu-id="6cf0b-148">X</span><span class="sxs-lookup"><span data-stu-id="6cf0b-148">X</span></span>        | <span data-ttu-id="6cf0b-149">X</span><span class="sxs-lookup"><span data-stu-id="6cf0b-149">X</span></span>     | <span data-ttu-id="6cf0b-150">X</span><span class="sxs-lookup"><span data-stu-id="6cf0b-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6cf0b-151">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="6cf0b-151">Minimum Shader Model</span></span>

<span data-ttu-id="6cf0b-152">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6cf0b-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6cf0b-153">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="6cf0b-153">Shader Model</span></span>                                              | <span data-ttu-id="6cf0b-154">Compatible</span><span class="sxs-lookup"><span data-stu-id="6cf0b-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6cf0b-155">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6cf0b-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6cf0b-156">sí</span><span class="sxs-lookup"><span data-stu-id="6cf0b-156">yes</span></span>       |
| [<span data-ttu-id="6cf0b-157">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="6cf0b-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6cf0b-158">no</span><span class="sxs-lookup"><span data-stu-id="6cf0b-158">no</span></span>        |
| [<span data-ttu-id="6cf0b-159">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6cf0b-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6cf0b-160">no</span><span class="sxs-lookup"><span data-stu-id="6cf0b-160">no</span></span>        |
| [<span data-ttu-id="6cf0b-161">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6cf0b-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6cf0b-162">no</span><span class="sxs-lookup"><span data-stu-id="6cf0b-162">no</span></span>        |
| [<span data-ttu-id="6cf0b-163">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6cf0b-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6cf0b-164">no</span><span class="sxs-lookup"><span data-stu-id="6cf0b-164">no</span></span>        |
| [<span data-ttu-id="6cf0b-165">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6cf0b-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6cf0b-166">no</span><span class="sxs-lookup"><span data-stu-id="6cf0b-166">no</span></span>        |



 

> [!Note]  
> <span data-ttu-id="6cf0b-167">Esta instrucción es compatible con CS \_ 4 \_ 0 y CS \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="6cf0b-167">This instruction is supported in cs\_4\_0 and cs\_4\_1.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6cf0b-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6cf0b-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cf0b-169">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6cf0b-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





