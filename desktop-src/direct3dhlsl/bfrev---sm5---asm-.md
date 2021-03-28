---
title: bfrev (SM5-ASM)
description: Invierta un número de 32 bits.
ms.assetid: 24F8209A-093E-4737-BF50-12F228024E9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11bf0f07b6c66babf8e7f91108f86ba753420fc2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996928"
---
# <a name="bfrev-sm5---asm"></a><span data-ttu-id="5c89a-103">bfrev (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5c89a-103">bfrev (sm5 - asm)</span></span>

<span data-ttu-id="5c89a-104">Invierta un número de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5c89a-104">Reverse a 32-bit number.</span></span>



| <span data-ttu-id="5c89a-105">bfrev dest \[ . Mask \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="5c89a-105">bfrev dest\[.mask\], src0\[.swizzle\]</span></span> |
|---------------------------------------|



 



| <span data-ttu-id="5c89a-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="5c89a-106">Item</span></span>                                                            | <span data-ttu-id="5c89a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c89a-107">Description</span></span>                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5c89a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5c89a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5c89a-109">\[en \] la dirección de *src0* con bits invertidos.</span><span class="sxs-lookup"><span data-stu-id="5c89a-109">\[in\] The address for *src0* with bits reversed.</span></span><br/> |
| <span data-ttu-id="5c89a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5c89a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5c89a-111">\[en \] el número de 32 bits que se va a invertir.</span><span class="sxs-lookup"><span data-stu-id="5c89a-111">\[in\] The 32-bit number to reverse.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="5c89a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c89a-112">Remarks</span></span>

<span data-ttu-id="5c89a-113">Por ejemplo, dado 0x12345678, el resultado sería 0x1e6a2c48.</span><span class="sxs-lookup"><span data-stu-id="5c89a-113">For example, given 0x12345678 the result would be 0x1e6a2c48.</span></span>

<span data-ttu-id="5c89a-114">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="5c89a-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5c89a-115">Vértice</span><span class="sxs-lookup"><span data-stu-id="5c89a-115">Vertex</span></span> | <span data-ttu-id="5c89a-116">Casco</span><span class="sxs-lookup"><span data-stu-id="5c89a-116">Hull</span></span> | <span data-ttu-id="5c89a-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="5c89a-117">Domain</span></span> | <span data-ttu-id="5c89a-118">Geometría</span><span class="sxs-lookup"><span data-stu-id="5c89a-118">Geometry</span></span> | <span data-ttu-id="5c89a-119">Píxel</span><span class="sxs-lookup"><span data-stu-id="5c89a-119">Pixel</span></span> | <span data-ttu-id="5c89a-120">Compute</span><span class="sxs-lookup"><span data-stu-id="5c89a-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5c89a-121">X</span><span class="sxs-lookup"><span data-stu-id="5c89a-121">X</span></span>      | <span data-ttu-id="5c89a-122">X</span><span class="sxs-lookup"><span data-stu-id="5c89a-122">X</span></span>    | <span data-ttu-id="5c89a-123">X</span><span class="sxs-lookup"><span data-stu-id="5c89a-123">X</span></span>      | <span data-ttu-id="5c89a-124">X</span><span class="sxs-lookup"><span data-stu-id="5c89a-124">X</span></span>        | <span data-ttu-id="5c89a-125">X</span><span class="sxs-lookup"><span data-stu-id="5c89a-125">X</span></span>     | <span data-ttu-id="5c89a-126">X</span><span class="sxs-lookup"><span data-stu-id="5c89a-126">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5c89a-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="5c89a-127">Minimum Shader Model</span></span>

<span data-ttu-id="5c89a-128">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="5c89a-128">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5c89a-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="5c89a-129">Shader Model</span></span>                                              | <span data-ttu-id="5c89a-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="5c89a-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5c89a-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="5c89a-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5c89a-132">sí</span><span class="sxs-lookup"><span data-stu-id="5c89a-132">yes</span></span>       |
| [<span data-ttu-id="5c89a-133">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="5c89a-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5c89a-134">no</span><span class="sxs-lookup"><span data-stu-id="5c89a-134">no</span></span>        |
| [<span data-ttu-id="5c89a-135">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="5c89a-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5c89a-136">no</span><span class="sxs-lookup"><span data-stu-id="5c89a-136">no</span></span>        |
| [<span data-ttu-id="5c89a-137">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c89a-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5c89a-138">no</span><span class="sxs-lookup"><span data-stu-id="5c89a-138">no</span></span>        |
| [<span data-ttu-id="5c89a-139">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c89a-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5c89a-140">no</span><span class="sxs-lookup"><span data-stu-id="5c89a-140">no</span></span>        |
| [<span data-ttu-id="5c89a-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c89a-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5c89a-142">no</span><span class="sxs-lookup"><span data-stu-id="5c89a-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5c89a-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c89a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c89a-144">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5c89a-144">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





