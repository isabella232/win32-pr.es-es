---
title: imm_atomic_alloc (SM5-ASM)
description: Incremente de forma atómica el contador de 32 bits oculto almacenado con un recuento o anexe la vista de acceso desordenado (UAV), devolviendo el valor original.
ms.assetid: 534FA3C3-6FAC-41DC-AC07-0E53FEED000C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a97709629497bae9af0298789453ef1d1172b7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784961"
---
# <a name="imm_atomic_alloc-sm5---asm"></a><span data-ttu-id="70ab4-103">\_asignación atómica \_ de Imm (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="70ab4-103">imm\_atomic\_alloc (sm5 - asm)</span></span>

<span data-ttu-id="70ab4-104">Incremente de forma atómica el contador de 32 bits oculto almacenado con un recuento o anexe la vista de acceso desordenado (UAV), devolviendo el valor original.</span><span class="sxs-lookup"><span data-stu-id="70ab4-104">Atomically increment the hidden 32-bit counter stored with a Count or Append unordered access view (UAV), returning the original value.</span></span>



| <span data-ttu-id="70ab4-105">\_ \_ dst0 de asignación atómica \[ de IMM \_ . \_ máscara \] de componente único, dstUAV</span><span class="sxs-lookup"><span data-stu-id="70ab4-105">imm\_atomic\_alloc dst0\[.single\_component\_mask\], dstUAV</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="70ab4-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="70ab4-106">Item</span></span>                                                                                           | <span data-ttu-id="70ab4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="70ab4-107">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="70ab4-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="70ab4-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                | <span data-ttu-id="70ab4-109">\[en \] contiene el valor del contador devuelto.</span><span class="sxs-lookup"><span data-stu-id="70ab4-109">\[in\] Contains the returned counter value.</span></span><br/>                    |
| <span data-ttu-id="70ab4-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="70ab4-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="70ab4-111">\[en \] un búfer estructurado UAV con la marca Count o Append.</span><span class="sxs-lookup"><span data-stu-id="70ab4-111">\[in\] A Structured Buffer UAV with the Count or Append flag.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="70ab4-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70ab4-112">Remarks</span></span>

<span data-ttu-id="70ab4-113">Hay un valor de contador de entero de bits sin signo 32 oculto asociado a cada recuento o vista de búfer de anexión que se inicializa cuando la vista está enlazada a la canalización, incluida la opción para mantener el valor anterior.</span><span class="sxs-lookup"><span data-stu-id="70ab4-113">There is a hidden unsigned 32-bit integer counter value associated with each Count or Append Buffer view which is initialized when the view is bound to the pipeline, including the option to keep the previous value.</span></span>

<span data-ttu-id="70ab4-114">Esta instrucción realiza un incremento atómico del valor del contador y devuelve el original a *dst0*.</span><span class="sxs-lookup"><span data-stu-id="70ab4-114">This instruction does an atomic increment of the counter value, returning the original to *dst0*.</span></span>

<span data-ttu-id="70ab4-115">En el caso de Append UAV, el valor devuelto solo es válido para la duración de la invocación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="70ab4-115">For an Append UAV, the returned value is only valid for the duration of the shader invocation.</span></span> <span data-ttu-id="70ab4-116">después, la implementación puede reorganizar el diseño de memoria.</span><span class="sxs-lookup"><span data-stu-id="70ab4-116">after that the implementation may rearrange the memory layout.</span></span> <span data-ttu-id="70ab4-117">Cualquier direccionamiento de memoria basado en el valor devuelto se debe limitar a la invocación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="70ab4-117">Any memory addressing based on the returned value must be limited to the shader invocation.</span></span>

<span data-ttu-id="70ab4-118">En el caso de Append UAV, dentro de la invocación del sombreador, el compilador de HLSL puede usar el valor devuelto como índice de estructura que se va a usar para tener acceso al búfer estructurado.</span><span class="sxs-lookup"><span data-stu-id="70ab4-118">For an Append UAV, within the shader invocation the HLSL compiler can use the returned value as the struct index to use for accessing the structured buffer.</span></span> <span data-ttu-id="70ab4-119">El acceso a cualquier índice struct distinto de las ubicaciones devueltas por las llamadas a la **\_ \_ asignación atómica de IMM** o [ \_ consumo](imm-atomic-consume--sm5---asm-.md) producen resultados indefinidos en que exactamente la ubicación de memoria dentro del UAV al que se está accediendo es aleatoria y solo se fija para la duración de la invocación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="70ab4-119">Accessing any struct index other than those locations returned by call(s) to **imm\_atomic\_alloc** or [\_consume](imm-atomic-consume--sm5---asm-.md) produce undefined results in that exactly which memory location within the UAV is being accessed is random and only fixed for the lifetime of the shader invocation.</span></span>

<span data-ttu-id="70ab4-120">En el caso de un UAV de recuento, la aplicación puede guardar el valor devuelto como referencia a una ubicación fija dentro de UAV que sea significativa después de que la invocación del sombreador haya finalizado.</span><span class="sxs-lookup"><span data-stu-id="70ab4-120">For a Count UAV, the returned value can be saved by the application as a reference to a fixed location within the UAV that is meaningful after the shader invocation is over.</span></span> <span data-ttu-id="70ab4-121">Siempre se puede tener acceso a cualquier ubicación de un UAV de recuento independientemente de cuál sea el valor de recuento.</span><span class="sxs-lookup"><span data-stu-id="70ab4-121">Any location in a Count UAV may always be accessed independent of what the count value is.</span></span>

<span data-ttu-id="70ab4-122">No hay ninguna compresión del recuento, por lo que se ajusta en caso de desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="70ab4-122">There is no clamping of the count, so it wraps on overflow.</span></span>

<span data-ttu-id="70ab4-123">El mismo sombreador no puede intentar usar la **\_ \_ asignación atómica de IMM** y el **IMM \_ atómico \_** en el mismo UAV.</span><span class="sxs-lookup"><span data-stu-id="70ab4-123">The same shader cannot attempt both **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span> <span data-ttu-id="70ab4-124">Además, la GPU no puede permitir que varias invocaciones del sombreador mezclen la **\_ \_ asignación atómica de IMM** y el **IMM atómico de IMM \_ \_** en el mismo UAV.</span><span class="sxs-lookup"><span data-stu-id="70ab4-124">Further, the GPU cannot allow multiple shader invocations to mix **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span>

<span data-ttu-id="70ab4-125">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="70ab4-125">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="70ab4-126">Vértice</span><span class="sxs-lookup"><span data-stu-id="70ab4-126">Vertex</span></span> | <span data-ttu-id="70ab4-127">Casco</span><span class="sxs-lookup"><span data-stu-id="70ab4-127">Hull</span></span> | <span data-ttu-id="70ab4-128">Dominio</span><span class="sxs-lookup"><span data-stu-id="70ab4-128">Domain</span></span> | <span data-ttu-id="70ab4-129">Geometría</span><span class="sxs-lookup"><span data-stu-id="70ab4-129">Geometry</span></span> | <span data-ttu-id="70ab4-130">Píxel</span><span class="sxs-lookup"><span data-stu-id="70ab4-130">Pixel</span></span> | <span data-ttu-id="70ab4-131">Compute</span><span class="sxs-lookup"><span data-stu-id="70ab4-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="70ab4-132">X</span><span class="sxs-lookup"><span data-stu-id="70ab4-132">X</span></span>     | <span data-ttu-id="70ab4-133">X</span><span class="sxs-lookup"><span data-stu-id="70ab4-133">X</span></span>       |



 

<span data-ttu-id="70ab4-134">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="70ab4-134">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="70ab4-135">Vértice</span><span class="sxs-lookup"><span data-stu-id="70ab4-135">Vertex</span></span> | <span data-ttu-id="70ab4-136">Casco</span><span class="sxs-lookup"><span data-stu-id="70ab4-136">Hull</span></span> | <span data-ttu-id="70ab4-137">Dominio</span><span class="sxs-lookup"><span data-stu-id="70ab4-137">Domain</span></span> | <span data-ttu-id="70ab4-138">Geometría</span><span class="sxs-lookup"><span data-stu-id="70ab4-138">Geometry</span></span> | <span data-ttu-id="70ab4-139">Píxel</span><span class="sxs-lookup"><span data-stu-id="70ab4-139">Pixel</span></span> | <span data-ttu-id="70ab4-140">Compute</span><span class="sxs-lookup"><span data-stu-id="70ab4-140">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="70ab4-141">X</span><span class="sxs-lookup"><span data-stu-id="70ab4-141">X</span></span>      | <span data-ttu-id="70ab4-142">X</span><span class="sxs-lookup"><span data-stu-id="70ab4-142">X</span></span>    | <span data-ttu-id="70ab4-143">X</span><span class="sxs-lookup"><span data-stu-id="70ab4-143">X</span></span>      | <span data-ttu-id="70ab4-144">X</span><span class="sxs-lookup"><span data-stu-id="70ab4-144">X</span></span>        | <span data-ttu-id="70ab4-145">X</span><span class="sxs-lookup"><span data-stu-id="70ab4-145">X</span></span>     | <span data-ttu-id="70ab4-146">X</span><span class="sxs-lookup"><span data-stu-id="70ab4-146">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="70ab4-147">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="70ab4-147">Minimum Shader Model</span></span>

<span data-ttu-id="70ab4-148">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="70ab4-148">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="70ab4-149">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="70ab4-149">Shader Model</span></span>                                              | <span data-ttu-id="70ab4-150">Compatible</span><span class="sxs-lookup"><span data-stu-id="70ab4-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="70ab4-151">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="70ab4-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="70ab4-152">sí</span><span class="sxs-lookup"><span data-stu-id="70ab4-152">yes</span></span>       |
| [<span data-ttu-id="70ab4-153">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="70ab4-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="70ab4-154">no</span><span class="sxs-lookup"><span data-stu-id="70ab4-154">no</span></span>        |
| [<span data-ttu-id="70ab4-155">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="70ab4-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="70ab4-156">no</span><span class="sxs-lookup"><span data-stu-id="70ab4-156">no</span></span>        |
| [<span data-ttu-id="70ab4-157">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="70ab4-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="70ab4-158">no</span><span class="sxs-lookup"><span data-stu-id="70ab4-158">no</span></span>        |
| [<span data-ttu-id="70ab4-159">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="70ab4-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="70ab4-160">no</span><span class="sxs-lookup"><span data-stu-id="70ab4-160">no</span></span>        |
| [<span data-ttu-id="70ab4-161">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="70ab4-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="70ab4-162">no</span><span class="sxs-lookup"><span data-stu-id="70ab4-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="70ab4-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="70ab4-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70ab4-164">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="70ab4-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





