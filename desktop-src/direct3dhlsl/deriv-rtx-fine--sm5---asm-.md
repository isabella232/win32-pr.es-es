---
title: deriv_rtx_fine (SM5-ASM)
description: Calcula la tasa de cambio de los componentes. | deriv_rtx_fine (SM5-ASM)
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73061e3220704cf2c19e28b4d6d434fda43fb941
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998172"
---
# <a name="deriv_rtx_fine-sm5---asm"></a><span data-ttu-id="d125b-104">derive \_ RTX \_ Fine (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="d125b-104">deriv\_rtx\_fine (sm5 - asm)</span></span>

<span data-ttu-id="d125b-105">Calcula la tasa de cambio de los componentes.</span><span class="sxs-lookup"><span data-stu-id="d125b-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="d125b-106">derive \_ RTX \_ Fine \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="d125b-106">deriv\_rtx\_fine\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="d125b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="d125b-107">Item</span></span>                                                            | <span data-ttu-id="d125b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d125b-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d125b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d125b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d125b-110">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="d125b-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="d125b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d125b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d125b-112">\[en \] los componentes de la operación.</span><span class="sxs-lookup"><span data-stu-id="d125b-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="d125b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d125b-113">Remarks</span></span>

<span data-ttu-id="d125b-114">Esta instrucción calcula la tasa de cambio de contenido de cada componente float32 de *src0* (post-swizzle), con respecto a la dirección rendertarget x Direction (RTX) o a la dirección de rendertarget y (vea [derive \_ propiedad \_ Fine](deriv-rty-fine--sm5---asm-.md)).</span><span class="sxs-lookup"><span data-stu-id="d125b-114">This instruction computes the rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction (see [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md)).</span></span> <span data-ttu-id="d125b-115">Cada píxel de la marca de 2x2 obtiene un par único de cálculos derivados x/y.</span><span class="sxs-lookup"><span data-stu-id="d125b-115">Each pixel in the 2x2 stamp gets a unique pair of x/y derivative calculations</span></span>

<span data-ttu-id="d125b-116">Los datos de la invocación del sombreador de píxeles actual siempre participan en el cálculo del derivado solicitado.</span><span class="sxs-lookup"><span data-stu-id="d125b-116">The data in the current pixel shader invocation always participates in the calculation of the requested derivative.</span></span> <span data-ttu-id="d125b-117">En el píxel de 2x2 píxeles en el que se encuentra el píxel actual, el derivado x es el delta de la fila de 2 píxeles, incluido el píxel actual.</span><span class="sxs-lookup"><span data-stu-id="d125b-117">In the 2x2 pixel quad the current pixel falls within, the x derivative is the delta of the row of 2 pixels including the current pixel.</span></span> <span data-ttu-id="d125b-118">El derivado y es el delta de la columna de 2 píxeles, incluido el píxel actual.</span><span class="sxs-lookup"><span data-stu-id="d125b-118">The y derivative is the delta of the column of 2 pixels including the current pixel.</span></span> <span data-ttu-id="d125b-119">No hay ninguna especificación que indique cómo se alinearán o se colocarán en mosaico las cuatro cuádruples en un primitivo.</span><span class="sxs-lookup"><span data-stu-id="d125b-119">There is no specification dictating how the 2x2 quads will be aligned or tiled over a primitive.</span></span>

<span data-ttu-id="d125b-120">Los derivados se calculan en un nivel más fino (cálculo único del par derivado x/y para cada píxel de un cuádruple 2x2).</span><span class="sxs-lookup"><span data-stu-id="d125b-120">Derivatives are calculated at a fine level (unique calculation of the x/y derivative pair for each pixel in a 2x2 quad).</span></span> <span data-ttu-id="d125b-121">Esta instrucción y [derive \_ propiedad \_ Fine](deriv-rty-fine--sm5---asm-.md) son alternativas para [derivar \_ RTX \_ gruesa](deriv-rtx-coarse--sm5---asm-.md) y [derivar \_ propiedad \_ grueso](deriv-rty-coarse--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="d125b-121">This instruction and [deriv\_rty\_fine](deriv-rty-fine--sm5---asm-.md) are alternatives to [deriv\_rtx\_coarse](deriv-rtx-coarse--sm5---asm-.md) and [deriv\_rty\_coarse](deriv-rty-coarse--sm5---asm-.md).</span></span> <span data-ttu-id="d125b-122">Estas \_ instrucciones aproximadas y \_ precisas son un reemplazo de **derive \_ RTX** estas \_ instrucciones aproximadas y \_ precisas son un sustituto de **derive \_ RTX** y **derive \_ propiedad** de modelos de sombreador anteriores.</span><span class="sxs-lookup"><span data-stu-id="d125b-122">These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtx** These \_coarse and \_fine derivative instructions are a replacement for **deriv\_rtx** and **deriv\_rty** from previous shader models.</span></span>

<span data-ttu-id="d125b-123">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="d125b-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d125b-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="d125b-124">Vertex</span></span> | <span data-ttu-id="d125b-125">Casco</span><span class="sxs-lookup"><span data-stu-id="d125b-125">Hull</span></span> | <span data-ttu-id="d125b-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="d125b-126">Domain</span></span> | <span data-ttu-id="d125b-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="d125b-127">Geometry</span></span> | <span data-ttu-id="d125b-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="d125b-128">Pixel</span></span> | <span data-ttu-id="d125b-129">Compute</span><span class="sxs-lookup"><span data-stu-id="d125b-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d125b-130">X</span><span class="sxs-lookup"><span data-stu-id="d125b-130">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d125b-131">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="d125b-131">Minimum Shader Model</span></span>

<span data-ttu-id="d125b-132">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="d125b-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d125b-133">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d125b-133">Shader Model</span></span>                                              | <span data-ttu-id="d125b-134">Compatible</span><span class="sxs-lookup"><span data-stu-id="d125b-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d125b-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d125b-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d125b-136">sí</span><span class="sxs-lookup"><span data-stu-id="d125b-136">yes</span></span>       |
| [<span data-ttu-id="d125b-137">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="d125b-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d125b-138">no</span><span class="sxs-lookup"><span data-stu-id="d125b-138">no</span></span>        |
| [<span data-ttu-id="d125b-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="d125b-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d125b-140">no</span><span class="sxs-lookup"><span data-stu-id="d125b-140">no</span></span>        |
| [<span data-ttu-id="d125b-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d125b-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d125b-142">no</span><span class="sxs-lookup"><span data-stu-id="d125b-142">no</span></span>        |
| [<span data-ttu-id="d125b-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d125b-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d125b-144">no</span><span class="sxs-lookup"><span data-stu-id="d125b-144">no</span></span>        |
| [<span data-ttu-id="d125b-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d125b-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d125b-146">no</span><span class="sxs-lookup"><span data-stu-id="d125b-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d125b-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d125b-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d125b-148">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d125b-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





