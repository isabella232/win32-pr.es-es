---
title: dmov (SM5-ASM)
description: Movimiento de componentes. | dmov (SM5-ASM)
ms.assetid: 05DBB9E2-10EC-4324-BB8F-1A9E315DE90C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b7d9c5ca0da1671ddf30fb9746333617f7688a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003740"
---
# <a name="dmov-sm5---asm"></a><span data-ttu-id="587a3-104">dmov (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="587a3-104">dmov (sm5 - asm)</span></span>

<span data-ttu-id="587a3-105">Movimiento de componentes.</span><span class="sxs-lookup"><span data-stu-id="587a3-105">Component-wise move.</span></span>



| <span data-ttu-id="587a3-106">dmov \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="587a3-106">dmov\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="587a3-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="587a3-107">Item</span></span>                                                            | <span data-ttu-id="587a3-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="587a3-108">Description</span></span>                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="587a3-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="587a3-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="587a3-110">\[en \] el destino de movimiento.</span><span class="sxs-lookup"><span data-stu-id="587a3-110">\[in\] The move destination.</span></span> <span data-ttu-id="587a3-111">*dest*  =  *src0*.</span><span class="sxs-lookup"><span data-stu-id="587a3-111">*dest* = *src0*.</span></span><br/> |
| <span data-ttu-id="587a3-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="587a3-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="587a3-113">\[en \] los componentes que se van a desplace.</span><span class="sxs-lookup"><span data-stu-id="587a3-113">\[in\] The components to be moved.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="587a3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="587a3-114">Remarks</span></span>

<span data-ttu-id="587a3-115">Los modificadores, a excepción de swizzle, suponen que los datos son de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="587a3-115">The modifiers, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="587a3-116">La ausencia de modificadores mueve los datos sin modificar los bits.</span><span class="sxs-lookup"><span data-stu-id="587a3-116">The absence of modifiers moves data without altering bits.</span></span>

<span data-ttu-id="587a3-117">El swizzles válido para los parámetros de origen son. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="587a3-117">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="587a3-118">Las siguientes asignaciones *src* son post-swizzle:</span><span class="sxs-lookup"><span data-stu-id="587a3-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="587a3-119">*src0* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="587a3-119">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="587a3-120">*SRC1* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="587a3-120">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="587a3-121">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="587a3-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="587a3-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="587a3-122">Vertex</span></span> | <span data-ttu-id="587a3-123">Casco</span><span class="sxs-lookup"><span data-stu-id="587a3-123">Hull</span></span> | <span data-ttu-id="587a3-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="587a3-124">Domain</span></span> | <span data-ttu-id="587a3-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="587a3-125">Geometry</span></span> | <span data-ttu-id="587a3-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="587a3-126">Pixel</span></span> | <span data-ttu-id="587a3-127">Compute</span><span class="sxs-lookup"><span data-stu-id="587a3-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="587a3-128">X</span><span class="sxs-lookup"><span data-stu-id="587a3-128">X</span></span>      | <span data-ttu-id="587a3-129">X</span><span class="sxs-lookup"><span data-stu-id="587a3-129">X</span></span>    | <span data-ttu-id="587a3-130">X</span><span class="sxs-lookup"><span data-stu-id="587a3-130">X</span></span>      | <span data-ttu-id="587a3-131">X</span><span class="sxs-lookup"><span data-stu-id="587a3-131">X</span></span>        | <span data-ttu-id="587a3-132">X</span><span class="sxs-lookup"><span data-stu-id="587a3-132">X</span></span>     | <span data-ttu-id="587a3-133">X</span><span class="sxs-lookup"><span data-stu-id="587a3-133">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="587a3-134">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="587a3-134">Minimum Shader Model</span></span>

<span data-ttu-id="587a3-135">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="587a3-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="587a3-136">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="587a3-136">Shader Model</span></span>                                              | <span data-ttu-id="587a3-137">Compatible</span><span class="sxs-lookup"><span data-stu-id="587a3-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="587a3-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="587a3-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="587a3-139">sí</span><span class="sxs-lookup"><span data-stu-id="587a3-139">yes</span></span>       |
| [<span data-ttu-id="587a3-140">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="587a3-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="587a3-141">no</span><span class="sxs-lookup"><span data-stu-id="587a3-141">no</span></span>        |
| [<span data-ttu-id="587a3-142">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="587a3-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="587a3-143">no</span><span class="sxs-lookup"><span data-stu-id="587a3-143">no</span></span>        |
| [<span data-ttu-id="587a3-144">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="587a3-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="587a3-145">no</span><span class="sxs-lookup"><span data-stu-id="587a3-145">no</span></span>        |
| [<span data-ttu-id="587a3-146">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="587a3-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="587a3-147">no</span><span class="sxs-lookup"><span data-stu-id="587a3-147">no</span></span>        |
| [<span data-ttu-id="587a3-148">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="587a3-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="587a3-149">no</span><span class="sxs-lookup"><span data-stu-id="587a3-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="587a3-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="587a3-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="587a3-151">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="587a3-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





