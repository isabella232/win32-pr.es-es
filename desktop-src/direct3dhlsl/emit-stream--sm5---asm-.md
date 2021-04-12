---
title: emit_stream (SM5-ASM)
description: Emite un vértice a un flujo determinado.
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56c2582453d18120e3e95b27af9c7613728fa62
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419918"
---
# <a name="emit_stream-sm5---asm"></a><span data-ttu-id="7721d-103">emisión \_ de flujo (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="7721d-103">emit\_stream (sm5 - asm)</span></span>

<span data-ttu-id="7721d-104">Emite un vértice a un flujo determinado.</span><span class="sxs-lookup"><span data-stu-id="7721d-104">Emit a vertex to a given stream.</span></span>



| <span data-ttu-id="7721d-105">emitir \_ streamIndex de flujo</span><span class="sxs-lookup"><span data-stu-id="7721d-105">emit\_stream streamIndex</span></span> |
|--------------------------|



 



| <span data-ttu-id="7721d-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="7721d-106">Item</span></span>                                                                                                               | <span data-ttu-id="7721d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7721d-107">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="7721d-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="7721d-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="7721d-109">\[en \] el índice de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="7721d-109">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7721d-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7721d-110">Remarks</span></span>

<span data-ttu-id="7721d-111">Esta instrucción hace que todos los registros o declarados \# de la secuencia especificada se lean fuera del sombreador de geometría para generar un vértice.</span><span class="sxs-lookup"><span data-stu-id="7721d-111">This instruction causes all declared o\# registers for the given stream to be read out of the geometry shader to generate a vertex.</span></span> <span data-ttu-id="7721d-112">Tras la emisión, no se inicializan todos los datos de todos los registros de salida de todas las secuencias, no solo la secuencia que se emite a.</span><span class="sxs-lookup"><span data-stu-id="7721d-112">Afer the emit, all data in all output registers for all streams become uninitialized, not just the stream emitted to.</span></span>

<span data-ttu-id="7721d-113">*streamIndex* debe ser un valor inmediato \[ 0.. 3 \] para una secuencia declarada.</span><span class="sxs-lookup"><span data-stu-id="7721d-113">*streamIndex* must be an immediate value \[0..3\] for a declared stream.</span></span>

<span data-ttu-id="7721d-114">Cuando se emiten varias llamadas a la **\_ secuencia de emisión** , se generan primitivas.</span><span class="sxs-lookup"><span data-stu-id="7721d-114">As multiple **emit\_stream** calls are issued, primitives are generated.</span></span>

### <a name="restrictions"></a><span data-ttu-id="7721d-115">Restricciones</span><span class="sxs-lookup"><span data-stu-id="7721d-115">Restrictions</span></span>

-   <span data-ttu-id="7721d-116">**Emit \_ Stream** puede aparecer cualquier número de veces en un sombreador de geometría, incluido en el control de flujo.</span><span class="sxs-lookup"><span data-stu-id="7721d-116">**emit\_stream** can appear any number of times in a geometry shader, including within flow control.</span></span>
-   <span data-ttu-id="7721d-117">Si no se han declarado secuencias, debe usar [Emit](emit--sm4---asm-.md) en lugar de **emitir \_ Stream**.</span><span class="sxs-lookup"><span data-stu-id="7721d-117">If streams have not been declared, then you must use [emit](emit--sm4---asm-.md) instead of **emit\_stream**.</span></span>

<span data-ttu-id="7721d-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="7721d-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7721d-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="7721d-119">Vertex</span></span> | <span data-ttu-id="7721d-120">Casco</span><span class="sxs-lookup"><span data-stu-id="7721d-120">Hull</span></span> | <span data-ttu-id="7721d-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="7721d-121">Domain</span></span> | <span data-ttu-id="7721d-122">Geometría</span><span class="sxs-lookup"><span data-stu-id="7721d-122">Geometry</span></span> | <span data-ttu-id="7721d-123">Píxel</span><span class="sxs-lookup"><span data-stu-id="7721d-123">Pixel</span></span> | <span data-ttu-id="7721d-124">Compute</span><span class="sxs-lookup"><span data-stu-id="7721d-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="7721d-125">X</span><span class="sxs-lookup"><span data-stu-id="7721d-125">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7721d-126">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="7721d-126">Minimum Shader Model</span></span>

<span data-ttu-id="7721d-127">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="7721d-127">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="7721d-128">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="7721d-128">Shader Model</span></span>                                              | <span data-ttu-id="7721d-129">Compatible</span><span class="sxs-lookup"><span data-stu-id="7721d-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7721d-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="7721d-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7721d-131">sí</span><span class="sxs-lookup"><span data-stu-id="7721d-131">yes</span></span>       |
| [<span data-ttu-id="7721d-132">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="7721d-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7721d-133">no</span><span class="sxs-lookup"><span data-stu-id="7721d-133">no</span></span>        |
| [<span data-ttu-id="7721d-134">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="7721d-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7721d-135">no</span><span class="sxs-lookup"><span data-stu-id="7721d-135">no</span></span>        |
| [<span data-ttu-id="7721d-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7721d-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7721d-137">no</span><span class="sxs-lookup"><span data-stu-id="7721d-137">no</span></span>        |
| [<span data-ttu-id="7721d-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7721d-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7721d-139">no</span><span class="sxs-lookup"><span data-stu-id="7721d-139">no</span></span>        |
| [<span data-ttu-id="7721d-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7721d-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7721d-141">no</span><span class="sxs-lookup"><span data-stu-id="7721d-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7721d-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7721d-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7721d-143">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7721d-143">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





