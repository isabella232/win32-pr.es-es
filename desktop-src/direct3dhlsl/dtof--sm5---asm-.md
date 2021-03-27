---
title: dtof (SM5-ASM)
description: Conversión de componentes de datos de punto flotante de precisión doble en datos de punto flotante de precisión sencilla.
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a66e72cf4c2cb1ac49adc492a586b4cbb9eef3b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358469"
---
# <a name="dtof-sm5---asm"></a><span data-ttu-id="5ab6f-103">dtof (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5ab6f-103">dtof (sm5 - asm)</span></span>

<span data-ttu-id="5ab6f-104">Conversión de componentes de datos de punto flotante de precisión doble en datos de punto flotante de precisión sencilla.</span><span class="sxs-lookup"><span data-stu-id="5ab6f-104">Component-wise conversion from double-precision floating-point data to single-precision floating-point data.</span></span>



| <span data-ttu-id="5ab6f-105">dtof dest \[ . Mask \] , \[ - \] src \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="5ab6f-105">dtof dest\[.mask\], \[-\]src\[.swizzle\],</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="5ab6f-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="5ab6f-106">Item</span></span>                                                            | <span data-ttu-id="5ab6f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ab6f-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5ab6f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5ab6f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5ab6f-109">\[en \] la dirección de los datos convertidos.</span><span class="sxs-lookup"><span data-stu-id="5ab6f-109">\[in\] The address of the converted data.</span></span><br/> |
| <span data-ttu-id="5ab6f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5ab6f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5ab6f-111">\[en \] los datos que se van a convertir.</span><span class="sxs-lookup"><span data-stu-id="5ab6f-111">\[in\] The data to be converted.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="5ab6f-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ab6f-112">Remarks</span></span>

<span data-ttu-id="5ab6f-113">Cada componente del origen se convierte a partir de la representación de precisión doble en la representación de precisión sencilla mediante el redondeo de redondeo a la más cercana.</span><span class="sxs-lookup"><span data-stu-id="5ab6f-113">Each component of the source is converted from the double-precision representation to the single-precision representation using round-to-nearest-even rounding.</span></span>

<span data-ttu-id="5ab6f-114">El swizzles válido para el parámetro de origen es. xyzw,. xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="5ab6f-114">The valid swizzles for the source parameter are .xyzw, .xyxy, .zwxy, .zwzw.</span></span>

<span data-ttu-id="5ab6f-115">Las máscaras de *destino* válidas son uno o dos componentes.</span><span class="sxs-lookup"><span data-stu-id="5ab6f-115">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="5ab6f-116">Es decir:. x,. y,. z,. w,. XY,. XZ,. XW,. YZ,. YW,. ZW el resultado de la primera conversión va al primer componente de la máscara, y el resultado del segundo componente entra en el segundo componente de la máscara, si está presente.</span><span class="sxs-lookup"><span data-stu-id="5ab6f-116">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The result of the first conversion goes to the first component in the mask, and the result of the second component goes in the second component in the mask, if present.</span></span>

<span data-ttu-id="5ab6f-117">los componentes de *dest* son float32.</span><span class="sxs-lookup"><span data-stu-id="5ab6f-117">*dest* components are float32.</span></span>

<span data-ttu-id="5ab6f-118">*src* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB) post swizzle.</span><span class="sxs-lookup"><span data-stu-id="5ab6f-118">*src* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB) post swizzle.</span></span>

<span data-ttu-id="5ab6f-119">En el caso de las conversiones de tipo float32<->Double, las implementaciones pueden aceptar desnormativas float32 o vaciarlas.</span><span class="sxs-lookup"><span data-stu-id="5ab6f-119">For float32<->double conversions, implementations may either honor float32 denorms or may flush them.</span></span>

<span data-ttu-id="5ab6f-120">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="5ab6f-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5ab6f-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="5ab6f-121">Vertex</span></span> | <span data-ttu-id="5ab6f-122">Casco</span><span class="sxs-lookup"><span data-stu-id="5ab6f-122">Hull</span></span> | <span data-ttu-id="5ab6f-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="5ab6f-123">Domain</span></span> | <span data-ttu-id="5ab6f-124">Geometría</span><span class="sxs-lookup"><span data-stu-id="5ab6f-124">Geometry</span></span> | <span data-ttu-id="5ab6f-125">Píxel</span><span class="sxs-lookup"><span data-stu-id="5ab6f-125">Pixel</span></span> | <span data-ttu-id="5ab6f-126">Compute</span><span class="sxs-lookup"><span data-stu-id="5ab6f-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5ab6f-127">X</span><span class="sxs-lookup"><span data-stu-id="5ab6f-127">X</span></span>      | <span data-ttu-id="5ab6f-128">X</span><span class="sxs-lookup"><span data-stu-id="5ab6f-128">X</span></span>    | <span data-ttu-id="5ab6f-129">X</span><span class="sxs-lookup"><span data-stu-id="5ab6f-129">X</span></span>      | <span data-ttu-id="5ab6f-130">X</span><span class="sxs-lookup"><span data-stu-id="5ab6f-130">X</span></span>        | <span data-ttu-id="5ab6f-131">X</span><span class="sxs-lookup"><span data-stu-id="5ab6f-131">X</span></span>     | <span data-ttu-id="5ab6f-132">X</span><span class="sxs-lookup"><span data-stu-id="5ab6f-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5ab6f-133">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="5ab6f-133">Minimum Shader Model</span></span>

<span data-ttu-id="5ab6f-134">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="5ab6f-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5ab6f-135">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="5ab6f-135">Shader Model</span></span>                                              | <span data-ttu-id="5ab6f-136">Compatible</span><span class="sxs-lookup"><span data-stu-id="5ab6f-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5ab6f-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="5ab6f-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5ab6f-138">sí</span><span class="sxs-lookup"><span data-stu-id="5ab6f-138">yes</span></span>       |
| [<span data-ttu-id="5ab6f-139">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="5ab6f-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5ab6f-140">no</span><span class="sxs-lookup"><span data-stu-id="5ab6f-140">no</span></span>        |
| [<span data-ttu-id="5ab6f-141">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="5ab6f-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5ab6f-142">no</span><span class="sxs-lookup"><span data-stu-id="5ab6f-142">no</span></span>        |
| [<span data-ttu-id="5ab6f-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ab6f-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5ab6f-144">no</span><span class="sxs-lookup"><span data-stu-id="5ab6f-144">no</span></span>        |
| [<span data-ttu-id="5ab6f-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ab6f-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5ab6f-146">no</span><span class="sxs-lookup"><span data-stu-id="5ab6f-146">no</span></span>        |
| [<span data-ttu-id="5ab6f-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ab6f-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5ab6f-148">no</span><span class="sxs-lookup"><span data-stu-id="5ab6f-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5ab6f-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ab6f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ab6f-150">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ab6f-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





