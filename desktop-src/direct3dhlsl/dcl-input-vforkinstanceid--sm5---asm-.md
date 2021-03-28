---
title: dcl_input vForkInstanceID (SM5-ASM)
description: Declare el identificador de instancia en una fase de bifurcación de sombreador de casco.
ms.assetid: AA73E8B6-C6D7-4483-B46E-C733341F552C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ce5fcf111a59abb0c9a6ccb36de63d94dcb11e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077135"
---
# <a name="dcl_input-vforkinstanceid-sm5---asm"></a><span data-ttu-id="e1871-103">\_vForkInstanceID de entrada de DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e1871-103">dcl\_input vForkInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="e1871-104">Declare el identificador de instancia en una fase de bifurcación de sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="e1871-104">Declare the instance ID in a hull shader fork phase.</span></span>



| <span data-ttu-id="e1871-105">vForkInstanceID de entrada de DCL \_</span><span class="sxs-lookup"><span data-stu-id="e1871-105">dcl\_input vForkInstanceID</span></span> |
|----------------------------|



 



| <span data-ttu-id="e1871-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="e1871-106">Item</span></span>                                                                                                                               | <span data-ttu-id="e1871-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1871-107">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="e1871-108"><span id="vForkInstanceID"></span><span id="vforkinstanceid"></span><span id="VFORKINSTANCEID"></span>*vForkInstanceID*</span><span class="sxs-lookup"><span data-stu-id="e1871-108"><span id="vForkInstanceID"></span><span id="vforkinstanceid"></span><span id="VFORKINSTANCEID"></span>*vForkInstanceID*</span></span><br/> | <span data-ttu-id="e1871-109">\[en \] el ID. de instancia.</span><span class="sxs-lookup"><span data-stu-id="e1871-109">\[in\] The instance ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e1871-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1871-110">Remarks</span></span>

<span data-ttu-id="e1871-111">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="e1871-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e1871-112">Vértice</span><span class="sxs-lookup"><span data-stu-id="e1871-112">Vertex</span></span> | <span data-ttu-id="e1871-113">Casco</span><span class="sxs-lookup"><span data-stu-id="e1871-113">Hull</span></span> | <span data-ttu-id="e1871-114">Dominio</span><span class="sxs-lookup"><span data-stu-id="e1871-114">Domain</span></span> | <span data-ttu-id="e1871-115">Geometría</span><span class="sxs-lookup"><span data-stu-id="e1871-115">Geometry</span></span> | <span data-ttu-id="e1871-116">Píxel</span><span class="sxs-lookup"><span data-stu-id="e1871-116">Pixel</span></span> | <span data-ttu-id="e1871-117">Compute</span><span class="sxs-lookup"><span data-stu-id="e1871-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="e1871-118">X</span><span class="sxs-lookup"><span data-stu-id="e1871-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e1871-119">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="e1871-119">Minimum Shader Model</span></span>

<span data-ttu-id="e1871-120">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e1871-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e1871-121">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="e1871-121">Shader Model</span></span>                                              | <span data-ttu-id="e1871-122">Compatible</span><span class="sxs-lookup"><span data-stu-id="e1871-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e1871-123">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e1871-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e1871-124">sí</span><span class="sxs-lookup"><span data-stu-id="e1871-124">yes</span></span>       |
| [<span data-ttu-id="e1871-125">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e1871-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e1871-126">no</span><span class="sxs-lookup"><span data-stu-id="e1871-126">no</span></span>        |
| [<span data-ttu-id="e1871-127">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e1871-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e1871-128">no</span><span class="sxs-lookup"><span data-stu-id="e1871-128">no</span></span>        |
| [<span data-ttu-id="e1871-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1871-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e1871-130">no</span><span class="sxs-lookup"><span data-stu-id="e1871-130">no</span></span>        |
| [<span data-ttu-id="e1871-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1871-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e1871-132">no</span><span class="sxs-lookup"><span data-stu-id="e1871-132">no</span></span>        |
| [<span data-ttu-id="e1871-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1871-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e1871-134">no</span><span class="sxs-lookup"><span data-stu-id="e1871-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e1871-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1871-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1871-136">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1871-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





