---
title: dcl_uav_raw (SM5-ASM)
description: Declare una vista de acceso desordenado (UAV) para su uso por parte de un sombreador. | dcl_uav_raw (SM5-ASM)
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f47614d5a9327f2d686a36db6bfe4afeb653788
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998093"
---
# <a name="dcl_uav_raw-sm5---asm"></a><span data-ttu-id="eacc6-104">DCL \_ UAV \_ raw (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="eacc6-104">dcl\_uav\_raw (sm5 - asm)</span></span>

<span data-ttu-id="eacc6-105">Declare una vista de acceso desordenado (UAV) para su uso por parte de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="eacc6-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="eacc6-106">DCL \_ UAV \_ raw \[ \_ GLC \] dstUAV</span><span class="sxs-lookup"><span data-stu-id="eacc6-106">dcl\_uav\_raw\[\_glc\] dstUAV</span></span> |
|-------------------------------|



 



| <span data-ttu-id="eacc6-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="eacc6-107">Item</span></span>                                                                                           | <span data-ttu-id="eacc6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="eacc6-108">Description</span></span>                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="eacc6-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="eacc6-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="eacc6-110">\[en \] UAV.</span><span class="sxs-lookup"><span data-stu-id="eacc6-110">\[in\] The UAV.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eacc6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eacc6-111">Remarks</span></span>

<span data-ttu-id="eacc6-112">*dstUAV* es un \# registro u declarado como una referencia a un UnorderedAccessView de un búfer, donde el búfer aparece como una matriz 1D simple de entradas sin tipo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="eacc6-112">*dstUAV* is a u\# register declared as a reference to an UnorderedAccessView of a Buffer, where the buffer appears as a simple 1D array of 32-bit untyped entries.</span></span>

<span data-ttu-id="eacc6-113">Las operaciones realizadas en la memoria pueden interpretar implícitamente los datos como si tuvieran un tipo.</span><span class="sxs-lookup"><span data-stu-id="eacc6-113">Operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="eacc6-114">La \_ marca GLC significa "globalmente coherente".</span><span class="sxs-lookup"><span data-stu-id="eacc6-114">The \_glc flag means "globally coherent".</span></span> <span data-ttu-id="eacc6-115">La ausencia de \_ GLC significa que el UAV se declara solo como "coherente con el grupo" en el sombreador de cálculo o "localmente coherente" en una invocación del sombreador de un solo píxel.</span><span class="sxs-lookup"><span data-stu-id="eacc6-115">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="eacc6-116">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="eacc6-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="eacc6-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="eacc6-117">Vertex</span></span> | <span data-ttu-id="eacc6-118">Casco</span><span class="sxs-lookup"><span data-stu-id="eacc6-118">Hull</span></span> | <span data-ttu-id="eacc6-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="eacc6-119">Domain</span></span> | <span data-ttu-id="eacc6-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="eacc6-120">Geometry</span></span> | <span data-ttu-id="eacc6-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="eacc6-121">Pixel</span></span> | <span data-ttu-id="eacc6-122">Compute</span><span class="sxs-lookup"><span data-stu-id="eacc6-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="eacc6-123">X</span><span class="sxs-lookup"><span data-stu-id="eacc6-123">X</span></span>     | <span data-ttu-id="eacc6-124">X</span><span class="sxs-lookup"><span data-stu-id="eacc6-124">X</span></span>       |



 

<span data-ttu-id="eacc6-125">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="eacc6-125">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="eacc6-126">Vértice</span><span class="sxs-lookup"><span data-stu-id="eacc6-126">Vertex</span></span> | <span data-ttu-id="eacc6-127">Casco</span><span class="sxs-lookup"><span data-stu-id="eacc6-127">Hull</span></span> | <span data-ttu-id="eacc6-128">Dominio</span><span class="sxs-lookup"><span data-stu-id="eacc6-128">Domain</span></span> | <span data-ttu-id="eacc6-129">Geometría</span><span class="sxs-lookup"><span data-stu-id="eacc6-129">Geometry</span></span> | <span data-ttu-id="eacc6-130">Píxel</span><span class="sxs-lookup"><span data-stu-id="eacc6-130">Pixel</span></span> | <span data-ttu-id="eacc6-131">Compute</span><span class="sxs-lookup"><span data-stu-id="eacc6-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="eacc6-132">X</span><span class="sxs-lookup"><span data-stu-id="eacc6-132">X</span></span>      | <span data-ttu-id="eacc6-133">X</span><span class="sxs-lookup"><span data-stu-id="eacc6-133">X</span></span>    | <span data-ttu-id="eacc6-134">X</span><span class="sxs-lookup"><span data-stu-id="eacc6-134">X</span></span>      | <span data-ttu-id="eacc6-135">X</span><span class="sxs-lookup"><span data-stu-id="eacc6-135">X</span></span>        | <span data-ttu-id="eacc6-136">X</span><span class="sxs-lookup"><span data-stu-id="eacc6-136">X</span></span>     | <span data-ttu-id="eacc6-137">X</span><span class="sxs-lookup"><span data-stu-id="eacc6-137">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eacc6-138">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="eacc6-138">Minimum Shader Model</span></span>

<span data-ttu-id="eacc6-139">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="eacc6-139">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="eacc6-140">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="eacc6-140">Shader Model</span></span>                                              | <span data-ttu-id="eacc6-141">Compatible</span><span class="sxs-lookup"><span data-stu-id="eacc6-141">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="eacc6-142">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="eacc6-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="eacc6-143">sí</span><span class="sxs-lookup"><span data-stu-id="eacc6-143">yes</span></span>       |
| [<span data-ttu-id="eacc6-144">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="eacc6-144">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="eacc6-145">no</span><span class="sxs-lookup"><span data-stu-id="eacc6-145">no</span></span>        |
| [<span data-ttu-id="eacc6-146">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="eacc6-146">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eacc6-147">no</span><span class="sxs-lookup"><span data-stu-id="eacc6-147">no</span></span>        |
| [<span data-ttu-id="eacc6-148">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eacc6-148">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eacc6-149">no</span><span class="sxs-lookup"><span data-stu-id="eacc6-149">no</span></span>        |
| [<span data-ttu-id="eacc6-150">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eacc6-150">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eacc6-151">no</span><span class="sxs-lookup"><span data-stu-id="eacc6-151">no</span></span>        |
| [<span data-ttu-id="eacc6-152">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eacc6-152">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eacc6-153">no</span><span class="sxs-lookup"><span data-stu-id="eacc6-153">no</span></span>        |



 

> [!Note]  
> <span data-ttu-id="eacc6-154">Esta instrucción es compatible con CS \_ 4 \_ 0 y CS \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="eacc6-154">This instruction is supported in cs\_4\_0 and cs\_4\_1.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="eacc6-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eacc6-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eacc6-156">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eacc6-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





