---
title: dcl_input vOutputControlPointID (SM5-ASM)
description: Declare el identificador del punto de control de salida en una fase del punto de control del sombreador de casco.
ms.assetid: 376ECA4F-DD71-4466-8A9D-E92A536832BC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cee49a8a825f25b0fbbccff027d5ad1b9ade514
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077134"
---
# <a name="dcl_input-voutputcontrolpointid-sm5---asm"></a><span data-ttu-id="90245-103">\_vOutputControlPointID de entrada de DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="90245-103">dcl\_input vOutputControlPointID (sm5 - asm)</span></span>

<span data-ttu-id="90245-104">Declare el identificador del punto de control de salida en una fase del punto de control del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="90245-104">Declare the output control point ID in a hull shader control point phase.</span></span>



| <span data-ttu-id="90245-105">vOutputControlPointID de entrada de DCL \_</span><span class="sxs-lookup"><span data-stu-id="90245-105">dcl\_input vOutputControlPointID</span></span> |
|----------------------------------|



 



| <span data-ttu-id="90245-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="90245-106">Item</span></span>                                                                                                                                                       | <span data-ttu-id="90245-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="90245-107">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="90245-108"><span id="vOutputControlPointID"></span><span id="voutputcontrolpointid"></span><span id="VOUTPUTCONTROLPOINTID"></span>*vOutputControlPointID*</span><span class="sxs-lookup"><span data-stu-id="90245-108"><span id="vOutputControlPointID"></span><span id="voutputcontrolpointid"></span><span id="VOUTPUTCONTROLPOINTID"></span>*vOutputControlPointID*</span></span><br/> | <span data-ttu-id="90245-109">\[en \] el identificador del punto de control de salida.</span><span class="sxs-lookup"><span data-stu-id="90245-109">\[in\] The output control point ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="90245-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90245-110">Remarks</span></span>

<span data-ttu-id="90245-111">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="90245-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="90245-112">Vértice</span><span class="sxs-lookup"><span data-stu-id="90245-112">Vertex</span></span> | <span data-ttu-id="90245-113">Casco</span><span class="sxs-lookup"><span data-stu-id="90245-113">Hull</span></span> | <span data-ttu-id="90245-114">Dominio</span><span class="sxs-lookup"><span data-stu-id="90245-114">Domain</span></span> | <span data-ttu-id="90245-115">Geometría</span><span class="sxs-lookup"><span data-stu-id="90245-115">Geometry</span></span> | <span data-ttu-id="90245-116">Píxel</span><span class="sxs-lookup"><span data-stu-id="90245-116">Pixel</span></span> | <span data-ttu-id="90245-117">Compute</span><span class="sxs-lookup"><span data-stu-id="90245-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="90245-118">X</span><span class="sxs-lookup"><span data-stu-id="90245-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="90245-119">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="90245-119">Minimum Shader Model</span></span>

<span data-ttu-id="90245-120">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="90245-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="90245-121">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="90245-121">Shader Model</span></span>                                              | <span data-ttu-id="90245-122">Compatible</span><span class="sxs-lookup"><span data-stu-id="90245-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="90245-123">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="90245-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="90245-124">sí</span><span class="sxs-lookup"><span data-stu-id="90245-124">yes</span></span>       |
| [<span data-ttu-id="90245-125">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="90245-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="90245-126">no</span><span class="sxs-lookup"><span data-stu-id="90245-126">no</span></span>        |
| [<span data-ttu-id="90245-127">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="90245-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="90245-128">no</span><span class="sxs-lookup"><span data-stu-id="90245-128">no</span></span>        |
| [<span data-ttu-id="90245-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="90245-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="90245-130">no</span><span class="sxs-lookup"><span data-stu-id="90245-130">no</span></span>        |
| [<span data-ttu-id="90245-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="90245-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="90245-132">no</span><span class="sxs-lookup"><span data-stu-id="90245-132">no</span></span>        |
| [<span data-ttu-id="90245-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="90245-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="90245-134">no</span><span class="sxs-lookup"><span data-stu-id="90245-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="90245-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90245-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90245-136">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="90245-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





