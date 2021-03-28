---
title: dcl_uav_typed (SM5-ASM)
description: Declare una vista de acceso desordenado (UAV) para su uso por parte de un sombreador. | dcl_uav_typed (SM5-ASM)
ms.assetid: F9F5583F-E3D0-447F-9227-BBB1B4E71934
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b789714c7ec825620b73e387fa8a4dd73e1a590d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998257"
---
# <a name="dcl_uav_typed-sm5---asm"></a><span data-ttu-id="e54a7-104">DCL \_ UAV \_ con tipo (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e54a7-104">dcl\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="e54a7-105">Declare una vista de acceso desordenado (UAV) para su uso por parte de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="e54a7-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="e54a7-106">DCL \_ UAV \_ con tipo \[ \_ GLC \] dstUAV, Dimension, tipo</span><span class="sxs-lookup"><span data-stu-id="e54a7-106">dcl\_uav\_typed\[\_glc\] dstUAV, dimension, type</span></span> |
|--------------------------------------------------|



 



| <span data-ttu-id="e54a7-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="e54a7-107">Item</span></span>                                                                                           | <span data-ttu-id="e54a7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e54a7-108">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e54a7-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="e54a7-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="e54a7-110">\[en \] UAV.</span><span class="sxs-lookup"><span data-stu-id="e54a7-110">\[in\] The UAV.</span></span><br/>                                                                        |
| <span data-ttu-id="e54a7-111"><span id="dimension"></span><span id="DIMENSION"></span>*Galería*</span><span class="sxs-lookup"><span data-stu-id="e54a7-111"><span id="dimension"></span><span id="DIMENSION"></span>*dimension*</span></span><br/>                 | <span data-ttu-id="e54a7-112">\[en \] especifica el número de dimensiones que proporcionan las instrucciones de acceso a UAV.</span><span class="sxs-lookup"><span data-stu-id="e54a7-112">\[in\] Specifies how many dimensions the instructions accessing the UAV are providing.</span></span><br/> |
| <span data-ttu-id="e54a7-113"><span id="type"></span><span id="TYPE"></span>*automáticamente*</span><span class="sxs-lookup"><span data-stu-id="e54a7-113"><span id="type"></span><span id="TYPE"></span>*type*</span></span><br/>                                | <span data-ttu-id="e54a7-114">\[en \] el tipo de UAV.</span><span class="sxs-lookup"><span data-stu-id="e54a7-114">\[in\] The type of the UAV.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="e54a7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e54a7-115">Remarks</span></span>

<span data-ttu-id="e54a7-116">*dstUAV* es un registro u que \# se declara como una referencia a un UnorderedAccessView que se debe enlazar a \# la ranura UAV de la API.</span><span class="sxs-lookup"><span data-stu-id="e54a7-116">*dstUAV* is a u\# register being declared as a reference to an UnorderedAccessView that must be bound to UAV slot \# at the API.</span></span>

<span data-ttu-id="e54a7-117">La dimensión debe ser buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray o Texture3D.</span><span class="sxs-lookup"><span data-stu-id="e54a7-117">The dimension must be buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray, or Texture3D.</span></span> <span data-ttu-id="e54a7-118">Esto indica el número de dimensiones que tienen las instrucciones de acceso a UAV: 1 (Texture1D, buffer), 2 (Texture1DArray, Texture2D) o 3 (Texture2DArray, Texture3D).</span><span class="sxs-lookup"><span data-stu-id="e54a7-118">This indicates how many dimensions any instructions accessing the UAV are providing: 1 (Texture1D, Buffer), 2 (Texture1DArray, Texture2D) or 3 (Texture2DArray, Texture3D).</span></span>

<span data-ttu-id="e54a7-119">El tipo es {UNORM, SNORM, UINT, SINT, FLOAT}.</span><span class="sxs-lookup"><span data-stu-id="e54a7-119">Type is {UNORM,SNORM,UINT,SINT,FLOAT}.</span></span> <span data-ttu-id="e54a7-120">Las operaciones realizadas con la u declarada \# deben ser compatibles con el tipo declarado aquí, y la UAV enlazada a la ranura \# también debe tener el mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="e54a7-120">Operations done with the declared u\# must be compatible with the type declared here, and the UAV bound to slot \# must also have the same type.</span></span>

<span data-ttu-id="e54a7-121">La \_ marca GLC significa "Globally coherente".</span><span class="sxs-lookup"><span data-stu-id="e54a7-121">The \_glc flag stands for "globally coherent".</span></span> <span data-ttu-id="e54a7-122">La ausencia de \_ GLC significa que el UAV se declara solo como "coherente con el grupo" en el sombreador de cálculo o "localmente coherente" en una invocación del sombreador de un solo píxel.</span><span class="sxs-lookup"><span data-stu-id="e54a7-122">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="e54a7-123">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="e54a7-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e54a7-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="e54a7-124">Vertex</span></span> | <span data-ttu-id="e54a7-125">Casco</span><span class="sxs-lookup"><span data-stu-id="e54a7-125">Hull</span></span> | <span data-ttu-id="e54a7-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="e54a7-126">Domain</span></span> | <span data-ttu-id="e54a7-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="e54a7-127">Geometry</span></span> | <span data-ttu-id="e54a7-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="e54a7-128">Pixel</span></span> | <span data-ttu-id="e54a7-129">Compute</span><span class="sxs-lookup"><span data-stu-id="e54a7-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e54a7-130">X</span><span class="sxs-lookup"><span data-stu-id="e54a7-130">X</span></span>     | <span data-ttu-id="e54a7-131">X</span><span class="sxs-lookup"><span data-stu-id="e54a7-131">X</span></span>       |



 

<span data-ttu-id="e54a7-132">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e54a7-132">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="e54a7-133">Vértice</span><span class="sxs-lookup"><span data-stu-id="e54a7-133">Vertex</span></span> | <span data-ttu-id="e54a7-134">Casco</span><span class="sxs-lookup"><span data-stu-id="e54a7-134">Hull</span></span> | <span data-ttu-id="e54a7-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="e54a7-135">Domain</span></span> | <span data-ttu-id="e54a7-136">Geometría</span><span class="sxs-lookup"><span data-stu-id="e54a7-136">Geometry</span></span> | <span data-ttu-id="e54a7-137">Píxel</span><span class="sxs-lookup"><span data-stu-id="e54a7-137">Pixel</span></span> | <span data-ttu-id="e54a7-138">Compute</span><span class="sxs-lookup"><span data-stu-id="e54a7-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e54a7-139">X</span><span class="sxs-lookup"><span data-stu-id="e54a7-139">X</span></span>      | <span data-ttu-id="e54a7-140">X</span><span class="sxs-lookup"><span data-stu-id="e54a7-140">X</span></span>    | <span data-ttu-id="e54a7-141">X</span><span class="sxs-lookup"><span data-stu-id="e54a7-141">X</span></span>      | <span data-ttu-id="e54a7-142">X</span><span class="sxs-lookup"><span data-stu-id="e54a7-142">X</span></span>        | <span data-ttu-id="e54a7-143">X</span><span class="sxs-lookup"><span data-stu-id="e54a7-143">X</span></span>     | <span data-ttu-id="e54a7-144">X</span><span class="sxs-lookup"><span data-stu-id="e54a7-144">X</span></span>       |



 

> [!Note]  
> <span data-ttu-id="e54a7-145">Esta instrucción no se admite en el sombreador de cálculo 4. x.</span><span class="sxs-lookup"><span data-stu-id="e54a7-145">This instruction is not supported in compute shader 4.x.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="e54a7-146">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="e54a7-146">Minimum Shader Model</span></span>

<span data-ttu-id="e54a7-147">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e54a7-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e54a7-148">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="e54a7-148">Shader Model</span></span>                                              | <span data-ttu-id="e54a7-149">Compatible</span><span class="sxs-lookup"><span data-stu-id="e54a7-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e54a7-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e54a7-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e54a7-151">sí</span><span class="sxs-lookup"><span data-stu-id="e54a7-151">yes</span></span>       |
| [<span data-ttu-id="e54a7-152">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e54a7-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e54a7-153">no</span><span class="sxs-lookup"><span data-stu-id="e54a7-153">no</span></span>        |
| [<span data-ttu-id="e54a7-154">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e54a7-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e54a7-155">no</span><span class="sxs-lookup"><span data-stu-id="e54a7-155">no</span></span>        |
| [<span data-ttu-id="e54a7-156">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e54a7-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e54a7-157">no</span><span class="sxs-lookup"><span data-stu-id="e54a7-157">no</span></span>        |
| [<span data-ttu-id="e54a7-158">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e54a7-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e54a7-159">no</span><span class="sxs-lookup"><span data-stu-id="e54a7-159">no</span></span>        |
| [<span data-ttu-id="e54a7-160">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e54a7-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e54a7-161">no</span><span class="sxs-lookup"><span data-stu-id="e54a7-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e54a7-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e54a7-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e54a7-163">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e54a7-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





