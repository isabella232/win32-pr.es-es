---
title: FTOD (SM5-ASM)
description: Conversión de componentes de datos de punto flotante de precisión sencilla a datos de punto flotante de precisión doble.
ms.assetid: 95297556-41ED-4ED0-8F9A-16B7A440AF25
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6790735745805426d32aefcc5d5d771ade644e43
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358495"
---
# <a name="ftod-sm5---asm"></a><span data-ttu-id="f4ffe-103">FTOD (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f4ffe-103">ftod (sm5 - asm)</span></span>

<span data-ttu-id="f4ffe-104">Conversión de componentes de datos de punto flotante de precisión sencilla a datos de punto flotante de precisión doble.</span><span class="sxs-lookup"><span data-stu-id="f4ffe-104">Component-wise conversion from single-precision floating-point data to double-precision floating-point data.</span></span>



| <span data-ttu-id="f4ffe-105">FTOD dest \[ . Mask \] , \[ - \] src \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="f4ffe-105">ftod dest\[.mask\], \[-\]src\[.swizzle\],</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="f4ffe-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="f4ffe-106">Item</span></span>                                                            | <span data-ttu-id="f4ffe-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4ffe-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f4ffe-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f4ffe-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f4ffe-109">\[en \] la dirección de los datos convertidos.</span><span class="sxs-lookup"><span data-stu-id="f4ffe-109">\[in\] The address of the converted data.</span></span><br/> |
| <span data-ttu-id="f4ffe-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f4ffe-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f4ffe-111">\[en \] los datos que se van a convertir.</span><span class="sxs-lookup"><span data-stu-id="f4ffe-111">\[in\] The data to be converted.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="f4ffe-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4ffe-112">Remarks</span></span>

<span data-ttu-id="f4ffe-113">Cada componente del origen se convierte de la representación de precisión sencilla a la representación de precisión doble.</span><span class="sxs-lookup"><span data-stu-id="f4ffe-113">Each component of the source is converted from the single-precision representation to the double-precision representation.</span></span>

<span data-ttu-id="f4ffe-114">Las máscaras de *destino* válidas son. XY,. ZW y. xyzw.</span><span class="sxs-lookup"><span data-stu-id="f4ffe-114">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="f4ffe-115">. XY recibe el resultado de la primera conversión y. ZW recibe el resultado de la segunda conversión.</span><span class="sxs-lookup"><span data-stu-id="f4ffe-115">.xy receives the result of the first conversion, and .zw receives the result of the second conversion.</span></span>

<span data-ttu-id="f4ffe-116">*dest* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="f4ffe-116">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="f4ffe-117">*src* es un vec2 flotante en x e y (ZW se omite) (post swizzle).</span><span class="sxs-lookup"><span data-stu-id="f4ffe-117">*src* is a float vec2 across x and y (zw ignored) (post swizzle).</span></span>

<span data-ttu-id="f4ffe-118">En el caso de las conversiones de tipo float32<->Double, las implementaciones pueden aceptar desnormativas float32 o vaciarlas.</span><span class="sxs-lookup"><span data-stu-id="f4ffe-118">For float32<->double conversions, implementations may either honor float32 denorms or may flush them.</span></span>

<span data-ttu-id="f4ffe-119">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="f4ffe-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f4ffe-120">Vértice</span><span class="sxs-lookup"><span data-stu-id="f4ffe-120">Vertex</span></span> | <span data-ttu-id="f4ffe-121">Casco</span><span class="sxs-lookup"><span data-stu-id="f4ffe-121">Hull</span></span> | <span data-ttu-id="f4ffe-122">Dominio</span><span class="sxs-lookup"><span data-stu-id="f4ffe-122">Domain</span></span> | <span data-ttu-id="f4ffe-123">Geometría</span><span class="sxs-lookup"><span data-stu-id="f4ffe-123">Geometry</span></span> | <span data-ttu-id="f4ffe-124">Píxel</span><span class="sxs-lookup"><span data-stu-id="f4ffe-124">Pixel</span></span> | <span data-ttu-id="f4ffe-125">Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffe-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f4ffe-126">X</span><span class="sxs-lookup"><span data-stu-id="f4ffe-126">X</span></span>      | <span data-ttu-id="f4ffe-127">X</span><span class="sxs-lookup"><span data-stu-id="f4ffe-127">X</span></span>    | <span data-ttu-id="f4ffe-128">X</span><span class="sxs-lookup"><span data-stu-id="f4ffe-128">X</span></span>      | <span data-ttu-id="f4ffe-129">X</span><span class="sxs-lookup"><span data-stu-id="f4ffe-129">X</span></span>        | <span data-ttu-id="f4ffe-130">X</span><span class="sxs-lookup"><span data-stu-id="f4ffe-130">X</span></span>     | <span data-ttu-id="f4ffe-131">X</span><span class="sxs-lookup"><span data-stu-id="f4ffe-131">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f4ffe-132">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="f4ffe-132">Minimum Shader Model</span></span>

<span data-ttu-id="f4ffe-133">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f4ffe-133">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f4ffe-134">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="f4ffe-134">Shader Model</span></span>                                              | <span data-ttu-id="f4ffe-135">Compatible</span><span class="sxs-lookup"><span data-stu-id="f4ffe-135">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f4ffe-136">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f4ffe-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f4ffe-137">sí</span><span class="sxs-lookup"><span data-stu-id="f4ffe-137">yes</span></span>       |
| [<span data-ttu-id="f4ffe-138">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f4ffe-138">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f4ffe-139">no</span><span class="sxs-lookup"><span data-stu-id="f4ffe-139">no</span></span>        |
| [<span data-ttu-id="f4ffe-140">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f4ffe-140">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f4ffe-141">no</span><span class="sxs-lookup"><span data-stu-id="f4ffe-141">no</span></span>        |
| [<span data-ttu-id="f4ffe-142">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4ffe-142">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f4ffe-143">no</span><span class="sxs-lookup"><span data-stu-id="f4ffe-143">no</span></span>        |
| [<span data-ttu-id="f4ffe-144">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4ffe-144">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f4ffe-145">no</span><span class="sxs-lookup"><span data-stu-id="f4ffe-145">no</span></span>        |
| [<span data-ttu-id="f4ffe-146">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4ffe-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f4ffe-147">no</span><span class="sxs-lookup"><span data-stu-id="f4ffe-147">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f4ffe-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4ffe-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4ffe-149">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4ffe-149">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





