---
title: DMín (SM5-ASM)
description: Mínimo de doble precisión de componentes.
ms.assetid: 77331B4D-C4B5-49B2-BB6A-77BD5050B575
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e199b01c68acca6609123425438f309af872fb4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077098"
---
# <a name="dmin-sm5---asm"></a><span data-ttu-id="9a123-103">DMín (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9a123-103">dmin (sm5 - asm)</span></span>

<span data-ttu-id="9a123-104">Mínimo de doble precisión de componentes.</span><span class="sxs-lookup"><span data-stu-id="9a123-104">Component-wise double-precision minimum.</span></span>



| <span data-ttu-id="9a123-105">dmin \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9a123-105">dmin\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="9a123-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="9a123-106">Item</span></span>                                                            | <span data-ttu-id="9a123-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a123-107">Description</span></span>                                                                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a123-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9a123-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9a123-109">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="9a123-109">\[in\] The address of the results of the operation.</span></span><br/> <span data-ttu-id="9a123-110">*dest*  =  *src0*  <  *SRC1* ?</span><span class="sxs-lookup"><span data-stu-id="9a123-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="9a123-111">*src0* : *SRC1*</span><span class="sxs-lookup"><span data-stu-id="9a123-111">*src0* : *src1*</span></span><br/> <span data-ttu-id="9a123-112">< se usa en lugar de <=, de modo que si es min (x, y) = x y después Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="9a123-112">< is used instead of <= so that if min(x,y) = x then max(x,y) = y.</span></span> <br/> |
| <span data-ttu-id="9a123-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9a123-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9a123-114">\[en \] los componentes que se van a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="9a123-114">\[in\] The components to compare with *src1*.</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="9a123-115"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="9a123-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="9a123-116">\[en \] los componentes que se van a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="9a123-116">\[in\] The components to compare with *src0*.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="9a123-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a123-117">Remarks</span></span>

<span data-ttu-id="9a123-118">NaN tiene un tratamiento especial.</span><span class="sxs-lookup"><span data-stu-id="9a123-118">NaN has special handling.</span></span> <span data-ttu-id="9a123-119">Si un operando de origen es NaN, se devuelve el otro operando de origen.</span><span class="sxs-lookup"><span data-stu-id="9a123-119">If one source operand is NaN, then the other source operand is returned.</span></span> <span data-ttu-id="9a123-120">La elección se realiza por componente.</span><span class="sxs-lookup"><span data-stu-id="9a123-120">The choice is made per-component.</span></span> <span data-ttu-id="9a123-121">Si ambos son NaN, se devuelve cualquier representación NaN.</span><span class="sxs-lookup"><span data-stu-id="9a123-121">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="9a123-122">El swizzles válido para los parámetros de origen son. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="9a123-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="9a123-123">Las máscaras de *destino* válidas son. XY,. ZW y. xyzw.</span><span class="sxs-lookup"><span data-stu-id="9a123-123">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="9a123-124">Las siguientes asignaciones *src* son post-swizzle:</span><span class="sxs-lookup"><span data-stu-id="9a123-124">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="9a123-125">*dest* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="9a123-125">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="9a123-126">*src0* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="9a123-126">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="9a123-127">*SRC1* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="9a123-127">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="9a123-128">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="9a123-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9a123-129">Vértice</span><span class="sxs-lookup"><span data-stu-id="9a123-129">Vertex</span></span> | <span data-ttu-id="9a123-130">Casco</span><span class="sxs-lookup"><span data-stu-id="9a123-130">Hull</span></span> | <span data-ttu-id="9a123-131">Dominio</span><span class="sxs-lookup"><span data-stu-id="9a123-131">Domain</span></span> | <span data-ttu-id="9a123-132">Geometría</span><span class="sxs-lookup"><span data-stu-id="9a123-132">Geometry</span></span> | <span data-ttu-id="9a123-133">Píxel</span><span class="sxs-lookup"><span data-stu-id="9a123-133">Pixel</span></span> | <span data-ttu-id="9a123-134">Compute</span><span class="sxs-lookup"><span data-stu-id="9a123-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9a123-135">X</span><span class="sxs-lookup"><span data-stu-id="9a123-135">X</span></span>      | <span data-ttu-id="9a123-136">X</span><span class="sxs-lookup"><span data-stu-id="9a123-136">X</span></span>    | <span data-ttu-id="9a123-137">X</span><span class="sxs-lookup"><span data-stu-id="9a123-137">X</span></span>      | <span data-ttu-id="9a123-138">X</span><span class="sxs-lookup"><span data-stu-id="9a123-138">X</span></span>        | <span data-ttu-id="9a123-139">X</span><span class="sxs-lookup"><span data-stu-id="9a123-139">X</span></span>     | <span data-ttu-id="9a123-140">X</span><span class="sxs-lookup"><span data-stu-id="9a123-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9a123-141">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="9a123-141">Minimum Shader Model</span></span>

<span data-ttu-id="9a123-142">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="9a123-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9a123-143">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="9a123-143">Shader Model</span></span>                                              | <span data-ttu-id="9a123-144">Compatible</span><span class="sxs-lookup"><span data-stu-id="9a123-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9a123-145">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9a123-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9a123-146">sí</span><span class="sxs-lookup"><span data-stu-id="9a123-146">yes</span></span>       |
| [<span data-ttu-id="9a123-147">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="9a123-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9a123-148">no</span><span class="sxs-lookup"><span data-stu-id="9a123-148">no</span></span>        |
| [<span data-ttu-id="9a123-149">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="9a123-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9a123-150">no</span><span class="sxs-lookup"><span data-stu-id="9a123-150">no</span></span>        |
| [<span data-ttu-id="9a123-151">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9a123-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9a123-152">no</span><span class="sxs-lookup"><span data-stu-id="9a123-152">no</span></span>        |
| [<span data-ttu-id="9a123-153">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9a123-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9a123-154">no</span><span class="sxs-lookup"><span data-stu-id="9a123-154">no</span></span>        |
| [<span data-ttu-id="9a123-155">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9a123-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9a123-156">no</span><span class="sxs-lookup"><span data-stu-id="9a123-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9a123-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a123-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a123-158">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9a123-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





