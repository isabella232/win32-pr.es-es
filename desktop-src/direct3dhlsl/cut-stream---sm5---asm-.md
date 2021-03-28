---
title: cut_stream (SM5-ASM)
description: Instrucción del sombreador de geometría que completa la topología primitiva actual en la secuencia especificada, si se le ha emitido algún vértice, e inicia una nueva topología del tipo declarado por el sombreador de geometría en esa secuencia.
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4650628d7f6b66130568f885e008a5163a9ee44f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419901"
---
# <a name="cut_stream-sm5---asm"></a><span data-ttu-id="4dfd0-103">cortar \_ flujo (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="4dfd0-103">cut\_stream (sm5 - asm)</span></span>

<span data-ttu-id="4dfd0-104">Instrucción del sombreador de geometría que completa la topología primitiva actual en la secuencia especificada, si se le ha emitido algún vértice, e inicia una nueva topología del tipo declarado por el sombreador de geometría en esa secuencia.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-104">The geometry shader instruction that completes the current primitive topology at the specified stream, if any vertices have been emitted to it, and starts a new topology of the type declared by the geometry shader at that stream.</span></span>



| <span data-ttu-id="4dfd0-105">cortar \_ flujo streamIndex</span><span class="sxs-lookup"><span data-stu-id="4dfd0-105">cut\_stream streamIndex</span></span> |
|-------------------------|



 



| <span data-ttu-id="4dfd0-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="4dfd0-106">Item</span></span>                                                                                                               | <span data-ttu-id="4dfd0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="4dfd0-107">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="4dfd0-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="4dfd0-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="4dfd0-109">\[en \] el índice de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-109">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4dfd0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4dfd0-110">Remarks</span></span>

<span data-ttu-id="4dfd0-111">Cuando se ejecuta esta instrucción, se completa cualquier topología emitida previamente por la invocación del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-111">When this instruction is executed, any previously emitted topology by the geometry shader invocation is completed.</span></span> <span data-ttu-id="4dfd0-112">Si no hay suficientes vértices emitidos para la topología primitiva anterior, se descartan.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-112">If there are not enough vertices emitted for the previous primitive topology, then they are discarded.</span></span> <span data-ttu-id="4dfd0-113">Dado que las únicas topologías de salida disponibles para el sombreador de geometría son PointList, linestrip y trianglestrip, nunca hay vértices sobrantes.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-113">Because the only available output topologies for the geometry shader are pointlist, linestrip and trianglestrip, there are never any leftover vertices.</span></span>

<span data-ttu-id="4dfd0-114">*streamIndex* debe ser un valor inmediato \[ 0.. 3 \] para una secuencia declarada.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-114">*streamIndex* must be an immediate value \[0..3\] for a declared stream.</span></span>

<span data-ttu-id="4dfd0-115">Una vez completada la topología anterior, si la hubiera, esta instrucción provoca que se inicie una nueva topología con la topología declarada como la salida del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-115">After the previous topology, if any, is completed, this instruction causes a new topology to begin, using the topology declared as the output for the geometry shader.</span></span>

### <a name="restrictions"></a><span data-ttu-id="4dfd0-116">Restricciones</span><span class="sxs-lookup"><span data-stu-id="4dfd0-116">Restrictions</span></span>

-   <span data-ttu-id="4dfd0-117">Esta instrucción solo se aplica al sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-117">This instruction applies to the geometry shader only.</span></span>
-   <span data-ttu-id="4dfd0-118">**el \_ flujo de corte** puede aparecer cualquier número de veces en el sombreador de geometría, incluido en el control de flujo.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-118">**cut\_stream** can appear any number of times in the geometry shader, including within flow control.</span></span>
-   <span data-ttu-id="4dfd0-119">Si el sombreador de geometría finaliza y se emiten los vértices, se completa la topología que se está compilando, como si se ejecutara una instrucción **Cut \_ Stream** como última instrucción.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-119">If the geometry shader ends and vertices have been emitted, the topology they are building is completed, as if a **cut\_stream** instruction was executed as the last instruction.</span></span>
-   <span data-ttu-id="4dfd0-120">Si no se han declarado secuencias, debe usar [CUT](cut--sm4---asm-.md) en lugar de **Cut \_ Stream**.</span><span class="sxs-lookup"><span data-stu-id="4dfd0-120">If streams have not been declared, you must use [cut](cut--sm4---asm-.md) instead of **cut\_stream**.</span></span>

<span data-ttu-id="4dfd0-121">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="4dfd0-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4dfd0-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="4dfd0-122">Vertex</span></span> | <span data-ttu-id="4dfd0-123">Casco</span><span class="sxs-lookup"><span data-stu-id="4dfd0-123">Hull</span></span> | <span data-ttu-id="4dfd0-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="4dfd0-124">Domain</span></span> | <span data-ttu-id="4dfd0-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="4dfd0-125">Geometry</span></span> | <span data-ttu-id="4dfd0-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="4dfd0-126">Pixel</span></span> | <span data-ttu-id="4dfd0-127">Compute</span><span class="sxs-lookup"><span data-stu-id="4dfd0-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="4dfd0-128">X</span><span class="sxs-lookup"><span data-stu-id="4dfd0-128">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4dfd0-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="4dfd0-129">Minimum Shader Model</span></span>

<span data-ttu-id="4dfd0-130">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="4dfd0-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4dfd0-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="4dfd0-131">Shader Model</span></span>                                              | <span data-ttu-id="4dfd0-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="4dfd0-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4dfd0-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4dfd0-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4dfd0-134">sí</span><span class="sxs-lookup"><span data-stu-id="4dfd0-134">yes</span></span>       |
| [<span data-ttu-id="4dfd0-135">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="4dfd0-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4dfd0-136">no</span><span class="sxs-lookup"><span data-stu-id="4dfd0-136">no</span></span>        |
| [<span data-ttu-id="4dfd0-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="4dfd0-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4dfd0-138">no</span><span class="sxs-lookup"><span data-stu-id="4dfd0-138">no</span></span>        |
| [<span data-ttu-id="4dfd0-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4dfd0-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4dfd0-140">no</span><span class="sxs-lookup"><span data-stu-id="4dfd0-140">no</span></span>        |
| [<span data-ttu-id="4dfd0-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4dfd0-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4dfd0-142">no</span><span class="sxs-lookup"><span data-stu-id="4dfd0-142">no</span></span>        |
| [<span data-ttu-id="4dfd0-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4dfd0-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4dfd0-144">no</span><span class="sxs-lookup"><span data-stu-id="4dfd0-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4dfd0-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4dfd0-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dfd0-146">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4dfd0-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





