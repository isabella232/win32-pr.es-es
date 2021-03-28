---
title: dcl_input vThread (SM5-ASM)
description: Declare los identificadores de entrada del sombreador de cálculo.
ms.assetid: C041863A-32B0-4588-A1A9-E416AF9B723C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf6a7bb19feef95eae9cc153911407b206fde16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785020"
---
# <a name="dcl_input-vthread-sm5---asm"></a><span data-ttu-id="a5cf0-103">\_vThread de entrada de DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a5cf0-103">dcl\_input vThread (sm5 - asm)</span></span>

<span data-ttu-id="a5cf0-104">Declare los identificadores de entrada del sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="a5cf0-104">Declare compute shader input IDs.</span></span>



| <span data-ttu-id="a5cf0-105">entrada de DCL \_ {vThreadID.XYZ </span><span class="sxs-lookup"><span data-stu-id="a5cf0-105">dcl\_input {vThreadID.xyz</span></span>\|<span data-ttu-id="a5cf0-106">vThreadGroupID.xyz </span><span class="sxs-lookup"><span data-stu-id="a5cf0-106">vThreadGroupID.xyz</span></span>\| <span data-ttu-id="a5cf0-107">vThreadIDInGroup.xyz </span><span class="sxs-lookup"><span data-stu-id="a5cf0-107">vThreadIDInGroup.xyz</span></span>\|<span data-ttu-id="a5cf0-108">vThreadIDInGroupFlattened}</span><span class="sxs-lookup"><span data-stu-id="a5cf0-108">vThreadIDInGroupFlattened}</span></span> |
|--------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a5cf0-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="a5cf0-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="a5cf0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5cf0-110">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a5cf0-111"><span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*</span><span class="sxs-lookup"><span data-stu-id="a5cf0-111"><span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*</span></span><br/> | <span data-ttu-id="a5cf0-112">\[en \] el valor de identificador entero de 32 bits sin signo de 3 componentes.</span><span class="sxs-lookup"><span data-stu-id="a5cf0-112">\[in\] The 3-component unsigned 32-bit integer ID value.</span></span><br/> |



 

<span data-ttu-id="a5cf0-113">**la \_ entrada de DCL** es una declaración existente en otras fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="a5cf0-113">**dcl\_input** is an existing declaration in other shader stages.</span></span> <span data-ttu-id="a5cf0-114">Se usa en el sombreador de cálculo para declarar los distintos valores de identificador entero de 32 bits sin signo de tres componentes exclusivos del sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="a5cf0-114">It is used in the compute shader to declare the various 3-component unsigned 32-bit integer ID values unique to the compute shader.</span></span> <span data-ttu-id="a5cf0-115">Son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="a5cf0-115">They are:</span></span>

-   <span data-ttu-id="a5cf0-116">vThreadID.xyz</span><span class="sxs-lookup"><span data-stu-id="a5cf0-116">vThreadID.xyz</span></span>
-   <span data-ttu-id="a5cf0-117">vGroupID.xyz</span><span class="sxs-lookup"><span data-stu-id="a5cf0-117">vGroupID.xyz</span></span>
-   <span data-ttu-id="a5cf0-118">vThreadIDInGroup.xyz</span><span class="sxs-lookup"><span data-stu-id="a5cf0-118">vThreadIDInGroup.xyz</span></span>
-   <span data-ttu-id="a5cf0-119">vThreadIDInGroupFlattened (componente único)</span><span class="sxs-lookup"><span data-stu-id="a5cf0-119">vThreadIDInGroupFlattened (single component)</span></span>

<span data-ttu-id="a5cf0-120">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="a5cf0-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a5cf0-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="a5cf0-121">Vertex</span></span> | <span data-ttu-id="a5cf0-122">Casco</span><span class="sxs-lookup"><span data-stu-id="a5cf0-122">Hull</span></span> | <span data-ttu-id="a5cf0-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="a5cf0-123">Domain</span></span> | <span data-ttu-id="a5cf0-124">Geometría</span><span class="sxs-lookup"><span data-stu-id="a5cf0-124">Geometry</span></span> | <span data-ttu-id="a5cf0-125">Píxel</span><span class="sxs-lookup"><span data-stu-id="a5cf0-125">Pixel</span></span> | <span data-ttu-id="a5cf0-126">Compute</span><span class="sxs-lookup"><span data-stu-id="a5cf0-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="a5cf0-127">X</span><span class="sxs-lookup"><span data-stu-id="a5cf0-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a5cf0-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a5cf0-128">Minimum Shader Model</span></span>

<span data-ttu-id="a5cf0-129">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a5cf0-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a5cf0-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a5cf0-130">Shader Model</span></span>                                              | <span data-ttu-id="a5cf0-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="a5cf0-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a5cf0-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a5cf0-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a5cf0-133">sí</span><span class="sxs-lookup"><span data-stu-id="a5cf0-133">yes</span></span>       |
| [<span data-ttu-id="a5cf0-134">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a5cf0-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a5cf0-135">no</span><span class="sxs-lookup"><span data-stu-id="a5cf0-135">no</span></span>        |
| [<span data-ttu-id="a5cf0-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a5cf0-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a5cf0-137">no</span><span class="sxs-lookup"><span data-stu-id="a5cf0-137">no</span></span>        |
| [<span data-ttu-id="a5cf0-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5cf0-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a5cf0-139">no</span><span class="sxs-lookup"><span data-stu-id="a5cf0-139">no</span></span>        |
| [<span data-ttu-id="a5cf0-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5cf0-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a5cf0-141">no</span><span class="sxs-lookup"><span data-stu-id="a5cf0-141">no</span></span>        |
| [<span data-ttu-id="a5cf0-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5cf0-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a5cf0-143">no</span><span class="sxs-lookup"><span data-stu-id="a5cf0-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a5cf0-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5cf0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5cf0-145">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5cf0-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





