---
title: texldb-PS
description: Instrucción de carga de textura sesgada. Esta instrucción usa el cuarto elemento (. a o. w) para sesgar el nivel de detalle de muestreo de textura justo antes del muestreo.
ms.assetid: cafd72c9-b7bb-4e3f-8a8c-de26a4446864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 912c4c61f6c1f2b6bef46c7c5b6ea17223df5eb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149345"
---
# <a name="texldb---ps"></a><span data-ttu-id="2674a-104">texldb-PS</span><span class="sxs-lookup"><span data-stu-id="2674a-104">texldb - ps</span></span>

<span data-ttu-id="2674a-105">Instrucción de carga de textura sesgada.</span><span class="sxs-lookup"><span data-stu-id="2674a-105">Biased texture load instruction.</span></span> <span data-ttu-id="2674a-106">Esta instrucción usa el cuarto elemento (. a o. w) para sesgar el nivel de detalle de muestreo de textura justo antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="2674a-106">This instruction uses the fourth element (.a or .w) to bias the texture-sampling level-of-detail just before sampling.</span></span>

## <a name="syntax"></a><span data-ttu-id="2674a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2674a-107">Syntax</span></span>



| <span data-ttu-id="2674a-108">texldb DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="2674a-108">texldb dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="2674a-109">Donde:</span><span class="sxs-lookup"><span data-stu-id="2674a-109">Where:</span></span>

-   <span data-ttu-id="2674a-110">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="2674a-110">dst is the destination register.</span></span>
-   <span data-ttu-id="2674a-111">src0 es un registro de origen que proporciona las coordenadas de textura para el ejemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="2674a-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="2674a-112">Vea [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="2674a-112">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="2674a-113">SRC1 identifica la [muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , donde \# especifica el número de muestra de textura que se muestra.</span><span class="sxs-lookup"><span data-stu-id="2674a-113">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="2674a-114">La muestra le ha asociado una textura y un estado de muestra definido por [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="2674a-114">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="2674a-115">Para conocer las restricciones que se aplican al usar texldb, vea [texld-PS \_ 2 \_ 0 y up](texld---ps-2-0.md) Instruction.</span><span class="sxs-lookup"><span data-stu-id="2674a-115">For the restrictions when using texldb, see the [texld - ps\_2\_0 and up](texld---ps-2-0.md) instruction.</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="2674a-116">PS \_ 2 \_ 0 y PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2674a-116">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="2674a-117">DST debe ser un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) y solo se permite la máscara xyzw (máscara predeterminada).</span><span class="sxs-lookup"><span data-stu-id="2674a-117">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="2674a-118">src0 debe ser un registro de [coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) o un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), sin modificador ni swizzle.</span><span class="sxs-lookup"><span data-stu-id="2674a-118">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="2674a-119">SRC1 debe ser una [muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sin \# modificador o swizzle.</span><span class="sxs-lookup"><span data-stu-id="2674a-119">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="2674a-120">Si \_ \_ no se establece el bit Cap de D3DD3DPSHADERCAPS2 0 NODEPENDENTREADLIMIT (en D3DPSHADERCAPS2 \_ 0), una instrucción de textura determinada (texld, texldp, texldb, texldd) puede depender, como máximo, de tercer orden.</span><span class="sxs-lookup"><span data-stu-id="2674a-120">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction (texld, texldp, texldb, texldd) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="2674a-121">Una instrucción de textura dependiente de primer orden es una instrucción de textura en la que:</span><span class="sxs-lookup"><span data-stu-id="2674a-121">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="2674a-122">src0 es un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="2674a-122">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="2674a-123">DST se escribió previamente y se ha escrito de nuevo.</span><span class="sxs-lookup"><span data-stu-id="2674a-123">dst was previously written, now being written again.</span></span>

<span data-ttu-id="2674a-124">Una instrucción de textura dependiente de segundo orden se define como una instrucción de textura que lee o escribe en un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) cuyo contenido, antes de ejecutar la instrucción de textura, depende (quizás indirectamente) del resultado de una instrucción de textura dependiente de primer orden.</span><span class="sxs-lookup"><span data-stu-id="2674a-124">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="2674a-125">Una instrucción de textura dependiente del orden de<sup>TH</sup>se deriva de una instrucción de textura de n-1)<sup>TH</sup>-order.</span><span class="sxs-lookup"><span data-stu-id="2674a-125">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="2674a-126">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2674a-126">ps\_3\_0</span></span>

<span data-ttu-id="2674a-127">SRC1 debe ser una [muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sin \# modificador.</span><span class="sxs-lookup"><span data-stu-id="2674a-127">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="2674a-128">Swizzle se permite en SRC1 y, cuando se aplica, los resultados de la búsqueda de texturas son swizzled anteriores antes de escribirse en el DST.</span><span class="sxs-lookup"><span data-stu-id="2674a-128">Swizzle is allowed on src1, and when applied, the texture lookup results are pre-swizzled before written to dst.</span></span>

## <a name="remarks"></a><span data-ttu-id="2674a-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2674a-129">Remarks</span></span>



| <span data-ttu-id="2674a-130">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="2674a-130">Pixel shader versions</span></span> | <span data-ttu-id="2674a-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="2674a-131">1\_1</span></span> | <span data-ttu-id="2674a-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="2674a-132">1\_2</span></span> | <span data-ttu-id="2674a-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2674a-133">1\_3</span></span> | <span data-ttu-id="2674a-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="2674a-134">1\_4</span></span> | <span data-ttu-id="2674a-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2674a-135">2\_0</span></span> | <span data-ttu-id="2674a-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2674a-136">2\_x</span></span> | <span data-ttu-id="2674a-137">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2674a-137">2\_sw</span></span> | <span data-ttu-id="2674a-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2674a-138">3\_0</span></span> | <span data-ttu-id="2674a-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2674a-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2674a-140">texldb</span><span class="sxs-lookup"><span data-stu-id="2674a-140">texldb</span></span>                |      |      |      |      | <span data-ttu-id="2674a-141">x</span><span class="sxs-lookup"><span data-stu-id="2674a-141">x</span></span>    | <span data-ttu-id="2674a-142">x</span><span class="sxs-lookup"><span data-stu-id="2674a-142">x</span></span>    | <span data-ttu-id="2674a-143">x</span><span class="sxs-lookup"><span data-stu-id="2674a-143">x</span></span>     | <span data-ttu-id="2674a-144">x</span><span class="sxs-lookup"><span data-stu-id="2674a-144">x</span></span>    | <span data-ttu-id="2674a-145">x</span><span class="sxs-lookup"><span data-stu-id="2674a-145">x</span></span>     |



 

<span data-ttu-id="2674a-146">texldb sesga el nivel de detalle del mipmap, calculado normalmente como parte del proceso de ejemplo por el valor (con signo) de src0. w.</span><span class="sxs-lookup"><span data-stu-id="2674a-146">texldb biases the mipmap level-of-detail, computed normally as part of the sample process by the (signed) value in src0.w.</span></span> <span data-ttu-id="2674a-147">Los valores de sesgo positivos darán lugar a que se seleccionen los mipmaps más pequeños y viceversa.</span><span class="sxs-lookup"><span data-stu-id="2674a-147">Positive bias values will result in smaller mipmaps being selected and vice versa.</span></span> <span data-ttu-id="2674a-148">En el caso de PS \_ 2 \_ 0 y PS \_ 2 \_ x, los valores de Bias pueden estar en el intervalo \[ de-3,0, + 3,0 \] .</span><span class="sxs-lookup"><span data-stu-id="2674a-148">For ps\_2\_0 and ps\_2\_x, bias values can be within the range \[-3.0, +3.0\].</span></span> <span data-ttu-id="2674a-149">En el caso de PS \_ 3 \_ 0, los valores de diferencia pueden estar en el intervalo \[ de-16,0, + 15,0 \] .</span><span class="sxs-lookup"><span data-stu-id="2674a-149">For ps\_3\_0, bias values can be within the range \[-16.0, +15.0\].</span></span> <span data-ttu-id="2674a-150">Los valores de sesgo fuera de estos intervalos producen resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="2674a-150">Bias values outside these ranges produce undefined results.</span></span> <span data-ttu-id="2674a-151">Se sigue respetando el estado de muestra D3DSAMP \_ MIPMAPLODBIAS y se agrega la inclinación texldb a este, pero en cada píxel.</span><span class="sxs-lookup"><span data-stu-id="2674a-151">The sampler state D3DSAMP\_MIPMAPLODBIAS is still honored, and the texldb bias is added to this, but on a per-pixel basis.</span></span> <span data-ttu-id="2674a-152">Una vez calculado el nivel de detalle sesgado, se \_ sigue respetando D3DSAMP MAXMIPLEVEL y se muestra la textura.</span><span class="sxs-lookup"><span data-stu-id="2674a-152">After the biased level-of-detail is computed, D3DSAMP\_MAXMIPLEVEL is still honored and the texture sample occurs.</span></span> <span data-ttu-id="2674a-153">Después de texldb, el contenido de src0 no se ve afectado (a menos que el DST sea el mismo registro).</span><span class="sxs-lookup"><span data-stu-id="2674a-153">After texldb, the contents of src0 are unaffected (unless dst is the same register).</span></span>

<span data-ttu-id="2674a-154">El número de coordenadas necesarias para que src0 realice el ejemplo de textura depende de cómo se declaró SRC1, además del componente. w.</span><span class="sxs-lookup"><span data-stu-id="2674a-154">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="2674a-155">Los tipos de muestra se declaran con [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md).</span><span class="sxs-lookup"><span data-stu-id="2674a-155">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="2674a-156">Si SRC1 se declara como una muestra 2D, src0 debe contener coordenadas. xyw; Si SRC1 se declara como una muestra de cubo o una muestra de volumen, src0 debe contener coordenadas. xyzw.</span><span class="sxs-lookup"><span data-stu-id="2674a-156">If src1 is declared as a 2D sampler, then src0 must contain .xyw coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyzw coordinates.</span></span> <span data-ttu-id="2674a-157">Se permite el muestreo de una textura 2D con coordenadas. xyzw (se omite la coordenada. z).</span><span class="sxs-lookup"><span data-stu-id="2674a-157">Sampling a 2D texture with .xyzw coordinates is allowed (the .z coordinate is ignored).</span></span>

<span data-ttu-id="2674a-158">Si la textura de origen contiene menos de cuatro componentes, los valores predeterminados se colocan en los componentes que faltan.</span><span class="sxs-lookup"><span data-stu-id="2674a-158">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="2674a-159">Los valores predeterminados dependen del formato de textura, tal como se muestra en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="2674a-159">Defaults depend on the texture format as shown in the following table:</span></span>



| <span data-ttu-id="2674a-160">Formato de textura</span><span class="sxs-lookup"><span data-stu-id="2674a-160">Texture Format</span></span>                                                                                          | <span data-ttu-id="2674a-161">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="2674a-161">Default Values</span></span>       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="2674a-162">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="2674a-162">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="2674a-163">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="2674a-163">A = 1.0</span></span>              |
| <span data-ttu-id="2674a-164">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="2674a-164">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="2674a-165">B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="2674a-165">B = A = 1.0</span></span>          |
| <span data-ttu-id="2674a-166">D3DFMT \_ A8</span><span class="sxs-lookup"><span data-stu-id="2674a-166">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="2674a-167">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="2674a-167">R = G = B = 0.0</span></span>      |
| <span data-ttu-id="2674a-168">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="2674a-168">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="2674a-169">G = B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="2674a-169">G = B = A = 1.0</span></span>      |
| <span data-ttu-id="2674a-170">Todos los formatos de profundidad/estarcido</span><span class="sxs-lookup"><span data-stu-id="2674a-170">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="2674a-171">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="2674a-171">R = B = 0.0, A = 1.0</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2674a-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2674a-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2674a-173">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="2674a-173">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 