---
title: dcl_thread_group (SM5-ASM)
description: Declare el tamaño del grupo de subprocesos.
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8141c80e82f1dfd1ae5a4d360d04fac32ba5221
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077120"
---
# <a name="dcl_thread_group-sm5---asm"></a><span data-ttu-id="dac78-103">\_grupo de subprocesos DCL \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="dac78-103">dcl\_thread\_group (sm5 - asm)</span></span>

<span data-ttu-id="dac78-104">Declare el tamaño del grupo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="dac78-104">Declare thread group size.</span></span>



| <span data-ttu-id="dac78-105">\_grupo de subprocesos DCL \_ x, y, z</span><span class="sxs-lookup"><span data-stu-id="dac78-105">dcl\_thread\_group x, y, z</span></span> |
|----------------------------|



 



| <span data-ttu-id="dac78-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="dac78-106">Item</span></span>                                                   | <span data-ttu-id="dac78-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="dac78-107">Description</span></span>                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="dac78-108"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="dac78-108"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="dac78-109">\[en \] un entero de usigned 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dac78-109">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="dac78-110">1 <= x <= 1024</span><span class="sxs-lookup"><span data-stu-id="dac78-110">1 <= x <= 1024</span></span> <br/> |
| <span data-ttu-id="dac78-111"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="dac78-111"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="dac78-112">\[en \] un entero de usigned 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dac78-112">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="dac78-113">1 <= y <= 1024</span><span class="sxs-lookup"><span data-stu-id="dac78-113">1 <= y <= 1024</span></span><br/>  |
| <span data-ttu-id="dac78-114"><span id="z"></span><span id="Z"></span>*z*</span><span class="sxs-lookup"><span data-stu-id="dac78-114"><span id="z"></span><span id="Z"></span>*z*</span></span><br/> | <span data-ttu-id="dac78-115">\[en \] un entero de usigned 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dac78-115">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="dac78-116">1 <= z <= 64</span><span class="sxs-lookup"><span data-stu-id="dac78-116">1 <= z <= 64</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="dac78-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dac78-117">Remarks</span></span>

<span data-ttu-id="dac78-118">x \* y \* z <= 1024</span><span class="sxs-lookup"><span data-stu-id="dac78-118">x\*y\*z <= 1024</span></span>

<span data-ttu-id="dac78-119">Esta declaración de grupo de subprocesos debe aparecer una vez en un sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="dac78-119">This thread group declaration must appear once in a compute shader.</span></span>

<span data-ttu-id="dac78-120">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="dac78-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dac78-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="dac78-121">Vertex</span></span> | <span data-ttu-id="dac78-122">Casco</span><span class="sxs-lookup"><span data-stu-id="dac78-122">Hull</span></span> | <span data-ttu-id="dac78-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="dac78-123">Domain</span></span> | <span data-ttu-id="dac78-124">Geometría</span><span class="sxs-lookup"><span data-stu-id="dac78-124">Geometry</span></span> | <span data-ttu-id="dac78-125">Píxel</span><span class="sxs-lookup"><span data-stu-id="dac78-125">Pixel</span></span> | <span data-ttu-id="dac78-126">Compute</span><span class="sxs-lookup"><span data-stu-id="dac78-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="dac78-127">X</span><span class="sxs-lookup"><span data-stu-id="dac78-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dac78-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="dac78-128">Minimum Shader Model</span></span>

<span data-ttu-id="dac78-129">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="dac78-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="dac78-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="dac78-130">Shader Model</span></span>                                              | <span data-ttu-id="dac78-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="dac78-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dac78-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="dac78-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dac78-133">sí</span><span class="sxs-lookup"><span data-stu-id="dac78-133">yes</span></span>       |
| [<span data-ttu-id="dac78-134">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="dac78-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dac78-135">no</span><span class="sxs-lookup"><span data-stu-id="dac78-135">no</span></span>        |
| [<span data-ttu-id="dac78-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="dac78-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dac78-137">no</span><span class="sxs-lookup"><span data-stu-id="dac78-137">no</span></span>        |
| [<span data-ttu-id="dac78-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dac78-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dac78-139">no</span><span class="sxs-lookup"><span data-stu-id="dac78-139">no</span></span>        |
| [<span data-ttu-id="dac78-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dac78-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dac78-141">no</span><span class="sxs-lookup"><span data-stu-id="dac78-141">no</span></span>        |
| [<span data-ttu-id="dac78-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dac78-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dac78-143">no</span><span class="sxs-lookup"><span data-stu-id="dac78-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dac78-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dac78-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dac78-145">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dac78-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





