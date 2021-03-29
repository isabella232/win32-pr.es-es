---
title: imm_atomic_consume (SM5-ASM)
description: Disminuya de forma atómica el contador de 32 bits oculto almacenado con un recuento o anexe la vista de acceso desordenado (UAV), devolviendo el nuevo valor.
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1c6fe01ddb92b2ce870b16254f75c52cadd341
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996932"
---
# <a name="imm_atomic_consume-sm5---asm"></a><span data-ttu-id="c976c-103">IMM \_ Atomic \_ consume (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c976c-103">imm\_atomic\_consume (sm5 - asm)</span></span>

<span data-ttu-id="c976c-104">Disminuya de forma atómica el contador de 32 bits oculto almacenado con un recuento o anexe la vista de acceso desordenado (UAV), devolviendo el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="c976c-104">Atomically decrement the hidden 32-bit counter stored with a Count or Append unordered access view (UAV), returning the new value.</span></span>



| <span data-ttu-id="c976c-105">IMM \_ Atomic \_ consumo dst0 \[ . \_ \_ máscara de componente único \] , dstUAV</span><span class="sxs-lookup"><span data-stu-id="c976c-105">imm\_atomic\_consume dst0\[.single\_component\_mask\], dstUAV</span></span> |
|---------------------------------------------------------------|



 



| <span data-ttu-id="c976c-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="c976c-106">Item</span></span>                                                                                           | <span data-ttu-id="c976c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c976c-107">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="c976c-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="c976c-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                | <span data-ttu-id="c976c-109">\[en \] contiene el valor del contador original devuelto.</span><span class="sxs-lookup"><span data-stu-id="c976c-109">\[in\] Contains the returned original counter value.</span></span><br/>           |
| <span data-ttu-id="c976c-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="c976c-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="c976c-111">\[en \] un búfer estructurado UAV con la marca Count o Append.</span><span class="sxs-lookup"><span data-stu-id="c976c-111">\[in\] A structured buffer UAV with the Count or Append flag.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="c976c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c976c-112">Remarks</span></span>

<span data-ttu-id="c976c-113">Vea [la \_ \_ asignación atómica de IMM](imm-atomic-alloc--sm5---asm-.md) para obtener una explicación sobre la validez del valor de recuento devuelto en función de si UAV es Count o Append.</span><span class="sxs-lookup"><span data-stu-id="c976c-113">See [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) for a discussion about the validity of the returned count value depending on whether the UAV is Count or Append.</span></span> <span data-ttu-id="c976c-114">Lo mismo se aplica para el **\_ \_ consumo atómico de IMM**.</span><span class="sxs-lookup"><span data-stu-id="c976c-114">The same applies for **imm\_atomic\_consume**.</span></span>

<span data-ttu-id="c976c-115">**el \_ \_ consumo atómico de IMM** realiza una reducción atómica del valor del contador y devuelve el nuevo valor a *dst0*.</span><span class="sxs-lookup"><span data-stu-id="c976c-115">**imm\_atomic\_consume** does an atomic decrement of the counter value, returning the new value to *dst0*.</span></span>

<span data-ttu-id="c976c-116">No hay ninguna compresión del recuento, por lo que se ajusta en el subdesbordamiento.</span><span class="sxs-lookup"><span data-stu-id="c976c-116">There is no clamping of the count, so it wraps on underflow.</span></span>

<span data-ttu-id="c976c-117">El mismo sombreador no puede intentar usar la **\_ \_ asignación atómica de IMM** y el **IMM \_ atómico \_** en el mismo UAV.</span><span class="sxs-lookup"><span data-stu-id="c976c-117">The same shader cannot attempt both **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span> <span data-ttu-id="c976c-118">Además, la GPU no puede permitir que varias invocaciones del sombreador mezclen la **\_ \_ asignación atómica de IMM** y el **IMM atómico de IMM \_ \_** en el mismo UAV.</span><span class="sxs-lookup"><span data-stu-id="c976c-118">Further, the GPU cannot allow multiple shader invocations to mix **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span>

<span data-ttu-id="c976c-119">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="c976c-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c976c-120">Vértice</span><span class="sxs-lookup"><span data-stu-id="c976c-120">Vertex</span></span> | <span data-ttu-id="c976c-121">Casco</span><span class="sxs-lookup"><span data-stu-id="c976c-121">Hull</span></span> | <span data-ttu-id="c976c-122">Dominio</span><span class="sxs-lookup"><span data-stu-id="c976c-122">Domain</span></span> | <span data-ttu-id="c976c-123">Geometría</span><span class="sxs-lookup"><span data-stu-id="c976c-123">Geometry</span></span> | <span data-ttu-id="c976c-124">Píxel</span><span class="sxs-lookup"><span data-stu-id="c976c-124">Pixel</span></span> | <span data-ttu-id="c976c-125">Compute</span><span class="sxs-lookup"><span data-stu-id="c976c-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c976c-126">X</span><span class="sxs-lookup"><span data-stu-id="c976c-126">X</span></span>     | <span data-ttu-id="c976c-127">X</span><span class="sxs-lookup"><span data-stu-id="c976c-127">X</span></span>       |



 

<span data-ttu-id="c976c-128">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c976c-128">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="c976c-129">Vértice</span><span class="sxs-lookup"><span data-stu-id="c976c-129">Vertex</span></span> | <span data-ttu-id="c976c-130">Casco</span><span class="sxs-lookup"><span data-stu-id="c976c-130">Hull</span></span> | <span data-ttu-id="c976c-131">Dominio</span><span class="sxs-lookup"><span data-stu-id="c976c-131">Domain</span></span> | <span data-ttu-id="c976c-132">Geometría</span><span class="sxs-lookup"><span data-stu-id="c976c-132">Geometry</span></span> | <span data-ttu-id="c976c-133">Píxel</span><span class="sxs-lookup"><span data-stu-id="c976c-133">Pixel</span></span> | <span data-ttu-id="c976c-134">Compute</span><span class="sxs-lookup"><span data-stu-id="c976c-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c976c-135">X</span><span class="sxs-lookup"><span data-stu-id="c976c-135">X</span></span>      | <span data-ttu-id="c976c-136">X</span><span class="sxs-lookup"><span data-stu-id="c976c-136">X</span></span>    | <span data-ttu-id="c976c-137">X</span><span class="sxs-lookup"><span data-stu-id="c976c-137">X</span></span>      | <span data-ttu-id="c976c-138">X</span><span class="sxs-lookup"><span data-stu-id="c976c-138">X</span></span>        | <span data-ttu-id="c976c-139">X</span><span class="sxs-lookup"><span data-stu-id="c976c-139">X</span></span>     | <span data-ttu-id="c976c-140">X</span><span class="sxs-lookup"><span data-stu-id="c976c-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c976c-141">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="c976c-141">Minimum Shader Model</span></span>

<span data-ttu-id="c976c-142">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c976c-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c976c-143">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="c976c-143">Shader Model</span></span>                                              | <span data-ttu-id="c976c-144">Compatible</span><span class="sxs-lookup"><span data-stu-id="c976c-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c976c-145">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c976c-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c976c-146">sí</span><span class="sxs-lookup"><span data-stu-id="c976c-146">yes</span></span>       |
| [<span data-ttu-id="c976c-147">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c976c-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c976c-148">no</span><span class="sxs-lookup"><span data-stu-id="c976c-148">no</span></span>        |
| [<span data-ttu-id="c976c-149">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c976c-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c976c-150">no</span><span class="sxs-lookup"><span data-stu-id="c976c-150">no</span></span>        |
| [<span data-ttu-id="c976c-151">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c976c-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c976c-152">no</span><span class="sxs-lookup"><span data-stu-id="c976c-152">no</span></span>        |
| [<span data-ttu-id="c976c-153">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c976c-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c976c-154">no</span><span class="sxs-lookup"><span data-stu-id="c976c-154">no</span></span>        |
| [<span data-ttu-id="c976c-155">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c976c-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c976c-156">no</span><span class="sxs-lookup"><span data-stu-id="c976c-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c976c-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c976c-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c976c-158">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c976c-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





