---
title: DEQ (SM5-ASM)
description: Comparación de igualdad de doble precisión de componentes.
ms.assetid: 99806989-D3A0-43F4-832A-5F1BD9C59A11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ed263deec975815f29050d2de0a877a312258c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532872"
---
# <a name="deq-sm5---asm"></a><span data-ttu-id="a11f4-103">DEQ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a11f4-103">deq (sm5 - asm)</span></span>

<span data-ttu-id="a11f4-104">Comparación de igualdad de doble precisión de componentes.</span><span class="sxs-lookup"><span data-stu-id="a11f4-104">Component-wise double-precision equality comparison.</span></span>



| <span data-ttu-id="a11f4-105">DEQ \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a11f4-105">deq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a11f4-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a11f4-106">Item</span></span>                                                            | <span data-ttu-id="a11f4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a11f4-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="a11f4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a11f4-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a11f4-109">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="a11f4-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="a11f4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a11f4-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a11f4-111">\[en \] los componentes que se van a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="a11f4-111">\[in\] The components to compare to *src1*.</span></span><br/>         |
| <span data-ttu-id="a11f4-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="a11f4-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a11f4-113">\[en \] los componentes que se van a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="a11f4-113">\[in\] The components to compare to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="a11f4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a11f4-114">Remarks</span></span>

<span data-ttu-id="a11f4-115">Esta instrucción realiza la comparación de punto flotante de precisión doble (*src0*  ==  *SRC1*) para cada componente y escribe el resultado en *dest*.</span><span class="sxs-lookup"><span data-stu-id="a11f4-115">This instruction performs the double-precision floating-point comparison (*src0* == *src1*) for each component and writes the result to *dest*.</span></span>

<span data-ttu-id="a11f4-116">Si la comparación es true, se devuelve 32-bit 0xFFFFFFFF para ese componente.</span><span class="sxs-lookup"><span data-stu-id="a11f4-116">If the comparison is true, then 32-bit 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="a11f4-117">De lo contrario, se devuelve 32-bit 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="a11f4-117">Otherwise 32-bit 0x00000000 is returned.</span></span>

<span data-ttu-id="a11f4-118">La comparación con NaN devuelve false.</span><span class="sxs-lookup"><span data-stu-id="a11f4-118">Comparison with NaN returns false.</span></span>

<span data-ttu-id="a11f4-119">Las máscaras de *destino* válidas son uno o dos componentes.</span><span class="sxs-lookup"><span data-stu-id="a11f4-119">The valid *dest* masks are any one or 2 components.</span></span> <span data-ttu-id="a11f4-120">Es decir:. x,. y,. z,. w,. XY,. XZ,. XW,. YZ,. YW,. ZW el primer componente *dest* de la máscara recibe el resultado de 32 bits para la primera comparación Double.</span><span class="sxs-lookup"><span data-stu-id="a11f4-120">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The first *dest* component in the mask receives the 32-bit result for the first double comparison.</span></span> <span data-ttu-id="a11f4-121">El segundo componente de la máscara, si está presente, recibe el resultado de 32 bits para la segunda comparación Double.</span><span class="sxs-lookup"><span data-stu-id="a11f4-121">The second component in the mask, if present, receives the 32-bit result for the second double comparison.</span></span>

<span data-ttu-id="a11f4-122">El swizzles válido para los parámetros de origen son. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="a11f4-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="a11f4-123">Las siguientes asignaciones *src* son post-swizzle:</span><span class="sxs-lookup"><span data-stu-id="a11f4-123">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="a11f4-124">*src0* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="a11f4-124">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="a11f4-125">*SRC1* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="a11f4-125">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="a11f4-126">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="a11f4-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a11f4-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="a11f4-127">Vertex</span></span> | <span data-ttu-id="a11f4-128">Casco</span><span class="sxs-lookup"><span data-stu-id="a11f4-128">Hull</span></span> | <span data-ttu-id="a11f4-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="a11f4-129">Domain</span></span> | <span data-ttu-id="a11f4-130">Geometría</span><span class="sxs-lookup"><span data-stu-id="a11f4-130">Geometry</span></span> | <span data-ttu-id="a11f4-131">Píxel</span><span class="sxs-lookup"><span data-stu-id="a11f4-131">Pixel</span></span> | <span data-ttu-id="a11f4-132">Compute</span><span class="sxs-lookup"><span data-stu-id="a11f4-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a11f4-133">X</span><span class="sxs-lookup"><span data-stu-id="a11f4-133">X</span></span>      | <span data-ttu-id="a11f4-134">X</span><span class="sxs-lookup"><span data-stu-id="a11f4-134">X</span></span>    | <span data-ttu-id="a11f4-135">X</span><span class="sxs-lookup"><span data-stu-id="a11f4-135">X</span></span>      | <span data-ttu-id="a11f4-136">X</span><span class="sxs-lookup"><span data-stu-id="a11f4-136">X</span></span>        | <span data-ttu-id="a11f4-137">X</span><span class="sxs-lookup"><span data-stu-id="a11f4-137">X</span></span>     | <span data-ttu-id="a11f4-138">X</span><span class="sxs-lookup"><span data-stu-id="a11f4-138">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a11f4-139">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a11f4-139">Minimum Shader Model</span></span>

<span data-ttu-id="a11f4-140">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a11f4-140">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a11f4-141">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a11f4-141">Shader Model</span></span>                                              | <span data-ttu-id="a11f4-142">Compatible</span><span class="sxs-lookup"><span data-stu-id="a11f4-142">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a11f4-143">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a11f4-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a11f4-144">sí</span><span class="sxs-lookup"><span data-stu-id="a11f4-144">yes</span></span>       |
| [<span data-ttu-id="a11f4-145">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a11f4-145">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a11f4-146">no</span><span class="sxs-lookup"><span data-stu-id="a11f4-146">no</span></span>        |
| [<span data-ttu-id="a11f4-147">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a11f4-147">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a11f4-148">no</span><span class="sxs-lookup"><span data-stu-id="a11f4-148">no</span></span>        |
| [<span data-ttu-id="a11f4-149">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a11f4-149">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a11f4-150">no</span><span class="sxs-lookup"><span data-stu-id="a11f4-150">no</span></span>        |
| [<span data-ttu-id="a11f4-151">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a11f4-151">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a11f4-152">no</span><span class="sxs-lookup"><span data-stu-id="a11f4-152">no</span></span>        |
| [<span data-ttu-id="a11f4-153">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a11f4-153">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a11f4-154">no</span><span class="sxs-lookup"><span data-stu-id="a11f4-154">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a11f4-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a11f4-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a11f4-156">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a11f4-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





