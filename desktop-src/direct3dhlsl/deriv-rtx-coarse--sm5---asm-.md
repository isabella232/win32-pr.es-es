---
title: deriv_rtx_coarse (SM5-ASM)
description: Calcula la tasa de cambio de los componentes. | deriv_rtx_coarse (SM5-ASM)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2355b6db6aef9e85959d6359053fea76b48af0a5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998065"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a><span data-ttu-id="d920e-104">derivar \_ RTX \_ grueso (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="d920e-104">deriv\_rtx\_coarse (sm5 - asm)</span></span>

<span data-ttu-id="d920e-105">Calcula la tasa de cambio de los componentes.</span><span class="sxs-lookup"><span data-stu-id="d920e-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="d920e-106">derive \_ RTX \_ General \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="d920e-106">deriv\_rtx\_coarse\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------|



 



| <span data-ttu-id="d920e-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="d920e-107">Item</span></span>                                                            | <span data-ttu-id="d920e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d920e-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d920e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d920e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d920e-110">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="d920e-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="d920e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d920e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d920e-112">\[en \] los componentes de la operación.</span><span class="sxs-lookup"><span data-stu-id="d920e-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="d920e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d920e-113">Remarks</span></span>

<span data-ttu-id="d920e-114">Esta instrucción calcula la tasa de cambio de contenido de cada componente float32 de *src0* (post-swizzle), con respecto a la dirección rendertarget x Direction (RTX) o a la dirección de rendertarget y (vea [derive \_ propiedad \_ gruesa](deriv-rty-coarse--sm5---asm-.md)).</span><span class="sxs-lookup"><span data-stu-id="d920e-114">This instruction computes the rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction (see [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md)).</span></span> <span data-ttu-id="d920e-115">Solo se calcula un par derivado de x, y para cada sello de 2x2 de píxeles.</span><span class="sxs-lookup"><span data-stu-id="d920e-115">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="d920e-116">Los datos de la invocación del sombreador de píxeles actual pueden participar o no en el cálculo del derivado solicitado, porque el derivado solo se calculará una vez por 2x2 cuádruple.</span><span class="sxs-lookup"><span data-stu-id="d920e-116">The data in the current pixel shader invocation may or may not participate in the calculation of the requested derivative, because the derivative will be calculated only once per 2x2 quad.</span></span> <span data-ttu-id="d920e-117">Por ejemplo, el derivado x podría ser un delta de la fila superior de píxeles y la dirección y ([derivar \_ propiedad \_ gruesa](deriv-rty-coarse--sm5---asm-.md)) podría ser una diferencia de la columna izquierda de píxeles.</span><span class="sxs-lookup"><span data-stu-id="d920e-117">For example, the x derivative could be a delta from the top row of pixels, and the y direction ([deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md)) could be a delta from the left column of pixels.</span></span> <span data-ttu-id="d920e-118">El cálculo exacto depende del proveedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="d920e-118">The exact calculation is up to the hardware vendor.</span></span> <span data-ttu-id="d920e-119">Tampoco hay ninguna especificación que indique cómo se alinearán o colocarán en mosaico las cuatro cuádruples en un primitivo.</span><span class="sxs-lookup"><span data-stu-id="d920e-119">There is also no specification dictating how the 2x2 quads will be aligned or tiled over a primitive.</span></span>

<span data-ttu-id="d920e-120">Los derivados se calculan en un nivel aproximado, una vez por cada 2x2 píxeles cuádruple.</span><span class="sxs-lookup"><span data-stu-id="d920e-120">Derivatives are calculated at a coarse level, once per 2x2 pixel quad.</span></span> <span data-ttu-id="d920e-121">Esta instrucción y [derive \_ propiedad \_ grueso](deriv-rty-coarse--sm5---asm-.md) son alternativas para [derivar \_ RTX \_ Fine](deriv-rtx-fine--sm5---asm-.md) y [derivar \_ propiedad \_ Fine](deriv-rty-fine--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="d920e-121">This instruction and [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md) are alternatives to [deriv\_rtx\_fine](deriv-rtx-fine--sm5---asm-.md) and [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md).</span></span> <span data-ttu-id="d920e-122">Estas \_ instrucciones aproximadas y \_ precisas son un reemplazo **de \_ rtxderiv \_ propiedad derivado** de modelos de sombreador anteriores.</span><span class="sxs-lookup"><span data-stu-id="d920e-122">These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtxderiv\_rty** from previous shader models .</span></span>

<span data-ttu-id="d920e-123">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="d920e-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d920e-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="d920e-124">Vertex</span></span> | <span data-ttu-id="d920e-125">Casco</span><span class="sxs-lookup"><span data-stu-id="d920e-125">Hull</span></span> | <span data-ttu-id="d920e-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="d920e-126">Domain</span></span> | <span data-ttu-id="d920e-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="d920e-127">Geometry</span></span> | <span data-ttu-id="d920e-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="d920e-128">Pixel</span></span> | <span data-ttu-id="d920e-129">Compute</span><span class="sxs-lookup"><span data-stu-id="d920e-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d920e-130">X</span><span class="sxs-lookup"><span data-stu-id="d920e-130">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d920e-131">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="d920e-131">Minimum Shader Model</span></span>

<span data-ttu-id="d920e-132">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="d920e-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d920e-133">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d920e-133">Shader Model</span></span>                                              | <span data-ttu-id="d920e-134">Compatible</span><span class="sxs-lookup"><span data-stu-id="d920e-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d920e-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d920e-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d920e-136">sí</span><span class="sxs-lookup"><span data-stu-id="d920e-136">yes</span></span>       |
| [<span data-ttu-id="d920e-137">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="d920e-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d920e-138">no</span><span class="sxs-lookup"><span data-stu-id="d920e-138">no</span></span>        |
| [<span data-ttu-id="d920e-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="d920e-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d920e-140">no</span><span class="sxs-lookup"><span data-stu-id="d920e-140">no</span></span>        |
| [<span data-ttu-id="d920e-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d920e-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d920e-142">no</span><span class="sxs-lookup"><span data-stu-id="d920e-142">no</span></span>        |
| [<span data-ttu-id="d920e-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d920e-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d920e-144">no</span><span class="sxs-lookup"><span data-stu-id="d920e-144">no</span></span>        |
| [<span data-ttu-id="d920e-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d920e-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d920e-146">no</span><span class="sxs-lookup"><span data-stu-id="d920e-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d920e-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d920e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d920e-148">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d920e-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





