---
title: countbits ((SM5-ASM)
description: Cuenta el número de bits establecidos en un número.
ms.assetid: ED75487F-46FF-45F5-BEAA-7A32BEFB0571
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d46fe9c750790d65630a743dd9ddc347fea50e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904288"
---
# <a name="countbits-sm5---asm"></a><span data-ttu-id="1f84e-103">countbits ((SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1f84e-103">countbits (sm5 - asm)</span></span>

<span data-ttu-id="1f84e-104">Cuenta el número de bits establecidos en un número.</span><span class="sxs-lookup"><span data-stu-id="1f84e-104">Counts the number of bits set in a number.</span></span>



| <span data-ttu-id="1f84e-105">countbits (DEST \[ . Mask \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="1f84e-105">countbits dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="1f84e-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="1f84e-106">Item</span></span>                                                            | <span data-ttu-id="1f84e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f84e-107">Description</span></span>                                   |
|-----------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="1f84e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1f84e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1f84e-109">\[en \] la dirección de los resultados.</span><span class="sxs-lookup"><span data-stu-id="1f84e-109">\[in\] The address of the results.</span></span><br/> |
| <span data-ttu-id="1f84e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1f84e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1f84e-111">\[en \] el número de bits 32 de entrada.</span><span class="sxs-lookup"><span data-stu-id="1f84e-111">\[in\] The input 32-bit number.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="1f84e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f84e-112">Remarks</span></span>

<span data-ttu-id="1f84e-113">Esta instrucción se puede usar para calcular el porcentaje de cobertura de entrada del sombreador.</span><span class="sxs-lookup"><span data-stu-id="1f84e-113">This instruction can be used to compute shader input coverage percentage.</span></span>

<span data-ttu-id="1f84e-114">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="1f84e-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1f84e-115">Vértice</span><span class="sxs-lookup"><span data-stu-id="1f84e-115">Vertex</span></span> | <span data-ttu-id="1f84e-116">Casco</span><span class="sxs-lookup"><span data-stu-id="1f84e-116">Hull</span></span> | <span data-ttu-id="1f84e-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="1f84e-117">Domain</span></span> | <span data-ttu-id="1f84e-118">Geometría</span><span class="sxs-lookup"><span data-stu-id="1f84e-118">Geometry</span></span> | <span data-ttu-id="1f84e-119">Píxel</span><span class="sxs-lookup"><span data-stu-id="1f84e-119">Pixel</span></span> | <span data-ttu-id="1f84e-120">Compute</span><span class="sxs-lookup"><span data-stu-id="1f84e-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1f84e-121">X</span><span class="sxs-lookup"><span data-stu-id="1f84e-121">X</span></span>      | <span data-ttu-id="1f84e-122">X</span><span class="sxs-lookup"><span data-stu-id="1f84e-122">X</span></span>    | <span data-ttu-id="1f84e-123">X</span><span class="sxs-lookup"><span data-stu-id="1f84e-123">X</span></span>      | <span data-ttu-id="1f84e-124">X</span><span class="sxs-lookup"><span data-stu-id="1f84e-124">X</span></span>        | <span data-ttu-id="1f84e-125">X</span><span class="sxs-lookup"><span data-stu-id="1f84e-125">X</span></span>     | <span data-ttu-id="1f84e-126">X</span><span class="sxs-lookup"><span data-stu-id="1f84e-126">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1f84e-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="1f84e-127">Minimum Shader Model</span></span>

<span data-ttu-id="1f84e-128">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="1f84e-128">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1f84e-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="1f84e-129">Shader Model</span></span>                                              | <span data-ttu-id="1f84e-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="1f84e-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1f84e-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1f84e-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1f84e-132">sí</span><span class="sxs-lookup"><span data-stu-id="1f84e-132">yes</span></span>       |
| [<span data-ttu-id="1f84e-133">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="1f84e-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1f84e-134">no</span><span class="sxs-lookup"><span data-stu-id="1f84e-134">no</span></span>        |
| [<span data-ttu-id="1f84e-135">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="1f84e-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1f84e-136">no</span><span class="sxs-lookup"><span data-stu-id="1f84e-136">no</span></span>        |
| [<span data-ttu-id="1f84e-137">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f84e-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1f84e-138">no</span><span class="sxs-lookup"><span data-stu-id="1f84e-138">no</span></span>        |
| [<span data-ttu-id="1f84e-139">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f84e-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1f84e-140">no</span><span class="sxs-lookup"><span data-stu-id="1f84e-140">no</span></span>        |
| [<span data-ttu-id="1f84e-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f84e-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1f84e-142">no</span><span class="sxs-lookup"><span data-stu-id="1f84e-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1f84e-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f84e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f84e-144">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f84e-144">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





