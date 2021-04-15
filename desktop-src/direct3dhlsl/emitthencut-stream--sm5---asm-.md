---
title: emitThenCut_stream (SM5-ASM)
description: Equivalente a un comando Emit seguido de un comando CUT. | emitThenCut_stream (SM5-ASM)
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae3129f2a3fb50664a5dbf070c7a1dae9bf5d6e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986266"
---
# <a name="emitthencut_stream-sm5---asm"></a><span data-ttu-id="7312f-104">emitThenCut \_ Stream (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="7312f-104">emitThenCut\_stream (sm5 - asm)</span></span>

<span data-ttu-id="7312f-105">Equivalente a un comando [Emit](emit--sm4---asm-.md) seguido de un comando [CUT](cut--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="7312f-105">Equivalent to an [emit](emit--sm4---asm-.md) command followed by a [cut](cut--sm4---asm-.md) command.</span></span>



| <span data-ttu-id="7312f-106">emitThenCut \_ Stream streamIndex</span><span class="sxs-lookup"><span data-stu-id="7312f-106">emitThenCut\_stream streamIndex</span></span> |
|---------------------------------|



 



| <span data-ttu-id="7312f-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7312f-107">Item</span></span>                                                                                                               | <span data-ttu-id="7312f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7312f-108">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="7312f-109"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="7312f-109"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="7312f-110">\[en \] el índice de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="7312f-110">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7312f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7312f-111">Remarks</span></span>

<span data-ttu-id="7312f-112">Esta operación es útil cuando se genera de forma consciente el último vértice de una topología.</span><span class="sxs-lookup"><span data-stu-id="7312f-112">This operation is useful when knowingly outputting the last vertex in a topology.</span></span>

<span data-ttu-id="7312f-113">Si no se han declarado secuencias, debe utilizar [emitThenCut](emitthencut--sm4---asm-.md) en lugar de **emitThenCut \_ Stream**.</span><span class="sxs-lookup"><span data-stu-id="7312f-113">If streams have not been declared, then you must use [emitThenCut](emitthencut--sm4---asm-.md) instead of **emitThenCut\_stream**.</span></span>

<span data-ttu-id="7312f-114">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="7312f-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7312f-115">Vértice</span><span class="sxs-lookup"><span data-stu-id="7312f-115">Vertex</span></span> | <span data-ttu-id="7312f-116">Casco</span><span class="sxs-lookup"><span data-stu-id="7312f-116">Hull</span></span> | <span data-ttu-id="7312f-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="7312f-117">Domain</span></span> | <span data-ttu-id="7312f-118">Geometría</span><span class="sxs-lookup"><span data-stu-id="7312f-118">Geometry</span></span> | <span data-ttu-id="7312f-119">Píxel</span><span class="sxs-lookup"><span data-stu-id="7312f-119">Pixel</span></span> | <span data-ttu-id="7312f-120">Compute</span><span class="sxs-lookup"><span data-stu-id="7312f-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="7312f-121">X</span><span class="sxs-lookup"><span data-stu-id="7312f-121">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7312f-122">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="7312f-122">Minimum Shader Model</span></span>

<span data-ttu-id="7312f-123">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="7312f-123">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="7312f-124">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="7312f-124">Shader Model</span></span>                                              | <span data-ttu-id="7312f-125">Compatible</span><span class="sxs-lookup"><span data-stu-id="7312f-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7312f-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="7312f-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7312f-127">sí</span><span class="sxs-lookup"><span data-stu-id="7312f-127">yes</span></span>       |
| [<span data-ttu-id="7312f-128">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="7312f-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7312f-129">no</span><span class="sxs-lookup"><span data-stu-id="7312f-129">no</span></span>        |
| [<span data-ttu-id="7312f-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="7312f-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7312f-131">no</span><span class="sxs-lookup"><span data-stu-id="7312f-131">no</span></span>        |
| [<span data-ttu-id="7312f-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7312f-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7312f-133">no</span><span class="sxs-lookup"><span data-stu-id="7312f-133">no</span></span>        |
| [<span data-ttu-id="7312f-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7312f-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7312f-135">no</span><span class="sxs-lookup"><span data-stu-id="7312f-135">no</span></span>        |
| [<span data-ttu-id="7312f-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7312f-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7312f-137">no</span><span class="sxs-lookup"><span data-stu-id="7312f-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7312f-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7312f-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7312f-139">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7312f-139">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





