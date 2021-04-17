---
title: deriv_rtx (SM4-ASM)
description: Velocidad de cambio de contenido de cada componente float32 de src0 (post-swizzle), con respecto a la dirección RenderTarget x Direction (RTX) o a la dirección de RenderTarget y.
ms.assetid: 2438DB36-C348-4854-AE1B-EC3C890B0B42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d4543805c02cf70d9c6b7856461c427788f616
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419895"
---
# <a name="deriv_rtx-sm4---asm"></a><span data-ttu-id="ceb35-103">derivar \_ RTX (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ceb35-103">deriv\_rtx (sm4 - asm)</span></span>

<span data-ttu-id="ceb35-104">Velocidad de cambio de contenido de cada componente float32 de *src0* (post-swizzle), con respecto a la dirección rendertarget x Direction (RTX) o a la dirección de rendertarget y.</span><span class="sxs-lookup"><span data-stu-id="ceb35-104">Rate of change of contents of each float32 component of *src0* (post-swizzle), with regard to RenderTarget x direction (rtx) or RenderTarget y direction.</span></span>



| <span data-ttu-id="ceb35-105">derive \_ RTX \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="ceb35-105">deriv\_rtx\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="ceb35-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="ceb35-106">Item</span></span>                                                            | <span data-ttu-id="ceb35-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceb35-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ceb35-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ceb35-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ceb35-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ceb35-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="ceb35-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ceb35-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ceb35-111">\[en \] el componente de la operación.</span><span class="sxs-lookup"><span data-stu-id="ceb35-111">\[in\] The component in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="ceb35-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ceb35-112">Remarks</span></span>

<span data-ttu-id="ceb35-113">Solo se calcula un par derivado de x, y para cada sello de 2x2 de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ceb35-113">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="ceb35-114">Esta operación depende del hardware.</span><span class="sxs-lookup"><span data-stu-id="ceb35-114">This operation is hardware dependent.</span></span>

<span data-ttu-id="ceb35-115">Implementación de rasterizador de referencia para triángulos:</span><span class="sxs-lookup"><span data-stu-id="ceb35-115">Reference rasterizer implementation for triangles:</span></span>

-   <span data-ttu-id="ceb35-116">El sombreador de píxeles siempre ejecuta el sombreador en cuatro puntos de píxeles en lógico (incluso a través del control de flujo, enmascarando los píxeles deshabilitados).</span><span class="sxs-lookup"><span data-stu-id="ceb35-116">Pixel Shader always runs Shader over 2x2 quad of pixels in lockstep (even through flow control, masking disabled pixels).</span></span>
-   <span data-ttu-id="ceb35-117">Las cuádruples siempre tienen coordenadas de píxeles numeradas pares (x e y) para el píxel superior izquierdo.</span><span class="sxs-lookup"><span data-stu-id="ceb35-117">Quads always have even numbered pixel coordinates (both x and y) for top-left pixel.</span></span>
-   <span data-ttu-id="ceb35-118">Los píxeles ficticios se ejecutan en el primitivo si el primitivo es demasiado pequeño para rellenar un cuádruple 2x2.</span><span class="sxs-lookup"><span data-stu-id="ceb35-118">Dummy pixels run off primitive if primitive is too small to fill a 2x2 quad.</span></span>
-   <span data-ttu-id="ceb35-119">**derive \_ RTX** se calcula seleccionando primero 2 píxeles: el píxel actual y el otro píxel con la misma coordenada y de la cuádruple.</span><span class="sxs-lookup"><span data-stu-id="ceb35-119">**deriv\_rtx** is computed by first choosing 2 pixels: the current pixel and the other pixel with the same y coordinate from the quad.</span></span> <span data-ttu-id="ceb35-120">Después, el resultado se calcula como: *src0*(impar x píxel)- *src0*(incluso x píxeles) \[ por componente.\]</span><span class="sxs-lookup"><span data-stu-id="ceb35-120">Then, the result is calculated as: *src0*(odd x pixel) - *src0*(even x pixel) \[per-component\]</span></span>
-   <span data-ttu-id="ceb35-121">[derive \_ propiedad](deriv-rty--sm4---asm-.md) se calcula seleccionando primero 2 píxeles: el píxel actual y el otro píxel con la misma coordenada x de la cuádruple.</span><span class="sxs-lookup"><span data-stu-id="ceb35-121">[deriv\_rty](deriv-rty--sm4---asm-.md) is computed by first choosing 2 pixels: the current pixel and the other pixel with the same x coordinate from the quad.</span></span> <span data-ttu-id="ceb35-122">A continuación, el resultado se calcula como: *src0*(impar y píxel)- *src0*(incluso píxel) \[ por componente.\]</span><span class="sxs-lookup"><span data-stu-id="ceb35-122">Then, the result is calculated as: *src0*(odd y pixel) - *src0*(even y pixel) \[per-component\]</span></span>

<span data-ttu-id="ceb35-123">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="ceb35-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ceb35-124">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="ceb35-124">Vertex Shader</span></span> | <span data-ttu-id="ceb35-125">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="ceb35-125">Geometry Shader</span></span> | <span data-ttu-id="ceb35-126">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ceb35-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="ceb35-127">x</span><span class="sxs-lookup"><span data-stu-id="ceb35-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ceb35-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="ceb35-128">Minimum Shader Model</span></span>

<span data-ttu-id="ceb35-129">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ceb35-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ceb35-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ceb35-130">Shader Model</span></span>                                              | <span data-ttu-id="ceb35-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="ceb35-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ceb35-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ceb35-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ceb35-133">sí</span><span class="sxs-lookup"><span data-stu-id="ceb35-133">yes</span></span>       |
| [<span data-ttu-id="ceb35-134">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ceb35-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ceb35-135">sí</span><span class="sxs-lookup"><span data-stu-id="ceb35-135">yes</span></span>       |
| [<span data-ttu-id="ceb35-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ceb35-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ceb35-137">sí</span><span class="sxs-lookup"><span data-stu-id="ceb35-137">yes</span></span>       |
| [<span data-ttu-id="ceb35-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ceb35-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ceb35-139">no</span><span class="sxs-lookup"><span data-stu-id="ceb35-139">no</span></span>        |
| [<span data-ttu-id="ceb35-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ceb35-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ceb35-141">no</span><span class="sxs-lookup"><span data-stu-id="ceb35-141">no</span></span>        |
| [<span data-ttu-id="ceb35-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ceb35-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ceb35-143">no</span><span class="sxs-lookup"><span data-stu-id="ceb35-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ceb35-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ceb35-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ceb35-145">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ceb35-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





