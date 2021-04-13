---
title: DNE (SM5-ASM)
description: Comparación de igualdad de precisión de doble precisión de componentes.
ms.assetid: 7C69A86D-0820-4640-AF5A-2993EC77D2AA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae00e0e5f4c0269b14a7a0f330d5af8760a1312f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419938"
---
# <a name="dne-sm5---asm"></a><span data-ttu-id="85769-103">DNE (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="85769-103">dne (sm5 - asm)</span></span>

<span data-ttu-id="85769-104">Comparación de igualdad de precisión de doble precisión de componentes.</span><span class="sxs-lookup"><span data-stu-id="85769-104">Component-wise double-precision not equality comparison.</span></span>



| <span data-ttu-id="85769-105">DNE \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="85769-105">dne\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="85769-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="85769-106">Item</span></span>                                                            | <span data-ttu-id="85769-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="85769-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="85769-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="85769-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="85769-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="85769-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="85769-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="85769-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="85769-111">\[en \] los componentes que se van a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="85769-111">\[in\] The components to compare with *src1*.</span></span><br/>      |
| <span data-ttu-id="85769-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="85769-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="85769-113">\[en \] los componentes que se van a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="85769-113">\[in\] The components to compare with *src0*.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="85769-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85769-114">Remarks</span></span>

<span data-ttu-id="85769-115">Esta instrucción realiza la comparación de punto flotante de precisión doble (*src0* ! = *SRC1*) de cada componente y escribe el resultado en *dest*.</span><span class="sxs-lookup"><span data-stu-id="85769-115">This instruction performs the double-precision floating-point comparison (*src0* != *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="85769-116">Si la comparación es true, se devuelve 32-bit 0xFFFFFFFF para ese componente.</span><span class="sxs-lookup"><span data-stu-id="85769-116">If the comparison is true, then 32-bit 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="85769-117">De lo contrario, se devuelve 32-bit 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="85769-117">Otherwise 32-bit 0x00000000 is returned.</span></span>

<span data-ttu-id="85769-118">La comparación con NaN devuelve true.</span><span class="sxs-lookup"><span data-stu-id="85769-118">Comparison with NaN returns true.</span></span>

<span data-ttu-id="85769-119">Las máscaras de *destino* válidas son uno o dos componentes.</span><span class="sxs-lookup"><span data-stu-id="85769-119">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="85769-120">Es decir:. x,. y,. z,. w,. XY,. XZ,. XW,. YZ,. YW,. ZW el primer componente *dest* de la máscara recibe el resultado de 32 bits para la primera comparación Double.</span><span class="sxs-lookup"><span data-stu-id="85769-120">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The first *dest* component in the mask receives the 32-bit result for the first double comparison.</span></span> <span data-ttu-id="85769-121">El segundo componente de la máscara, si está presente, recibe el resultado de 32 bits para la segunda comparación Double.</span><span class="sxs-lookup"><span data-stu-id="85769-121">The second component in the mask, if present, receives the 32-bit result for the second double comparison.</span></span>

<span data-ttu-id="85769-122">El swizzles válido para los parámetros de origen son. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="85769-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="85769-123">Las siguientes asignaciones *src* son post-swizzle:</span><span class="sxs-lookup"><span data-stu-id="85769-123">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="85769-124">*src0* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="85769-124">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="85769-125">*SRC1* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="85769-125">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="85769-126">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="85769-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="85769-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="85769-127">Vertex</span></span> | <span data-ttu-id="85769-128">Casco</span><span class="sxs-lookup"><span data-stu-id="85769-128">Hull</span></span> | <span data-ttu-id="85769-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="85769-129">Domain</span></span> | <span data-ttu-id="85769-130">Geometría</span><span class="sxs-lookup"><span data-stu-id="85769-130">Geometry</span></span> | <span data-ttu-id="85769-131">Píxel</span><span class="sxs-lookup"><span data-stu-id="85769-131">Pixel</span></span> | <span data-ttu-id="85769-132">Compute</span><span class="sxs-lookup"><span data-stu-id="85769-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="85769-133">X</span><span class="sxs-lookup"><span data-stu-id="85769-133">X</span></span>      | <span data-ttu-id="85769-134">X</span><span class="sxs-lookup"><span data-stu-id="85769-134">X</span></span>    | <span data-ttu-id="85769-135">X</span><span class="sxs-lookup"><span data-stu-id="85769-135">X</span></span>      | <span data-ttu-id="85769-136">X</span><span class="sxs-lookup"><span data-stu-id="85769-136">X</span></span>        | <span data-ttu-id="85769-137">X</span><span class="sxs-lookup"><span data-stu-id="85769-137">X</span></span>     | <span data-ttu-id="85769-138">X</span><span class="sxs-lookup"><span data-stu-id="85769-138">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="85769-139">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="85769-139">Minimum Shader Model</span></span>

<span data-ttu-id="85769-140">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="85769-140">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="85769-141">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="85769-141">Shader Model</span></span>                                              | <span data-ttu-id="85769-142">Compatible</span><span class="sxs-lookup"><span data-stu-id="85769-142">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="85769-143">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="85769-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="85769-144">sí</span><span class="sxs-lookup"><span data-stu-id="85769-144">yes</span></span>       |
| [<span data-ttu-id="85769-145">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="85769-145">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="85769-146">no</span><span class="sxs-lookup"><span data-stu-id="85769-146">no</span></span>        |
| [<span data-ttu-id="85769-147">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="85769-147">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="85769-148">no</span><span class="sxs-lookup"><span data-stu-id="85769-148">no</span></span>        |
| [<span data-ttu-id="85769-149">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85769-149">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="85769-150">no</span><span class="sxs-lookup"><span data-stu-id="85769-150">no</span></span>        |
| [<span data-ttu-id="85769-151">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85769-151">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="85769-152">no</span><span class="sxs-lookup"><span data-stu-id="85769-152">no</span></span>        |
| [<span data-ttu-id="85769-153">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85769-153">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="85769-154">no</span><span class="sxs-lookup"><span data-stu-id="85769-154">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="85769-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85769-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85769-156">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85769-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





