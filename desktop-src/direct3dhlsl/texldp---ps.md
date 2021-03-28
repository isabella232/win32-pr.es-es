---
title: texldp-PS
description: Instrucción de carga de textura proyectada. Esta instrucción divide la coordenada de textura de entrada por el cuarto elemento (. a o. w) justo antes del muestreo.
ms.assetid: 82e62ba3-a9f5-4afb-8dca-4c54a00843eb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 045caf6ec922183893df252488946546602d2459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359393"
---
# <a name="texldp---ps"></a><span data-ttu-id="3b8ef-104">texldp-PS</span><span class="sxs-lookup"><span data-stu-id="3b8ef-104">texldp - ps</span></span>

<span data-ttu-id="3b8ef-105">Instrucción de carga de textura proyectada.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-105">Projected texture load instruction.</span></span> <span data-ttu-id="3b8ef-106">Esta instrucción divide la coordenada de textura de entrada por el cuarto elemento (. a o. w) justo antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-106">This instruction divides the input texture coordinate by the fourth element (.a or .w) just before sampling.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b8ef-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b8ef-107">Syntax</span></span>



| <span data-ttu-id="3b8ef-108">texldp DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="3b8ef-108">texldp dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="3b8ef-109">, donde</span><span class="sxs-lookup"><span data-stu-id="3b8ef-109">where</span></span>

-   <span data-ttu-id="3b8ef-110">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-110">dst is the destination register.</span></span>
-   <span data-ttu-id="3b8ef-111">src0 es un registro de origen que proporciona las coordenadas de textura para el ejemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="3b8ef-112">Vea [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="3b8ef-112">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="3b8ef-113">SRC1 identifica la [muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , donde \# especifica el número de muestra de textura que se muestra.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-113">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="3b8ef-114">La muestra le ha asociado una textura y un estado de muestra definido por [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="3b8ef-114">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="3b8ef-115">Para obtener el conjunto de restricciones cuando se usa texldp, vea [texld](texld---ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="3b8ef-115">For the set of restrictions when using texldp, see [texld](texld---ps-2-0.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3b8ef-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b8ef-116">Remarks</span></span>

<span data-ttu-id="3b8ef-117">texldp realiza la proyección en las coordenadas leídas de src0 antes de realizar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-117">texldp performs projection on the coordinates read from src0 before performing the sample.</span></span> <span data-ttu-id="3b8ef-118">Cada coordenada de textura se divide por src0. w; a continuación, se muestra la textura.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-118">Each texture coordinate is divided by src0.w, then the texture is sampled.</span></span> <span data-ttu-id="3b8ef-119">Cuando texldp se completa, el contenido de src0 no se ve afectado (a menos que el DST sea el mismo registro).</span><span class="sxs-lookup"><span data-stu-id="3b8ef-119">When texldp completes, the contents of src0 are unaffected (unless dst is the same register).</span></span> <span data-ttu-id="3b8ef-120">Una alternativa al uso de texldp es realizar manualmente la división de proyección en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-120">An alternative to using texldp is to manually perform the projection division in the shader.</span></span> <span data-ttu-id="3b8ef-121">Sin embargo, realizar la división en el código del sombreador suele ser más lento que cuando lo realiza la instrucción texldp, por lo que debe evitar este tipo de cálculos adicionales cuando sea posible.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-121">However, performing the division in shader code is usually slower than when performed by the texldp instruction, so avoid such additional math when possible.</span></span>

<span data-ttu-id="3b8ef-122">El número de coordenadas necesarias para que src0 realice el ejemplo de textura depende de cómo se declaró SRC1, además del componente. w.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-122">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="3b8ef-123">Los tipos de muestra se declaran con [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md).</span><span class="sxs-lookup"><span data-stu-id="3b8ef-123">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="3b8ef-124">Si SRC1 se declara como una muestra 2D, src0 debe contener coordenadas. xyw; Si SRC1 se declara como una muestra de cubo o una muestra de volumen, src0 debe contener coordenadas. xyzw.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-124">If src1 is declared as a 2D sampler, then src0 must contain .xyw coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyzw coordinates.</span></span> <span data-ttu-id="3b8ef-125">Se permite el muestreo de una textura 2D con coordenadas. xyzw (se omite la coordenada. z).</span><span class="sxs-lookup"><span data-stu-id="3b8ef-125">Sampling a 2D texture with .xyzw coordinates is allowed (the .z coordinate is ignored).</span></span>

<span data-ttu-id="3b8ef-126">Si la textura de origen contiene menos de cuatro componentes, los valores predeterminados se colocan en los componentes que faltan.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-126">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="3b8ef-127">Los valores predeterminados dependen del formato de textura, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-127">Defaults depend on the texture format as shown in the following table.</span></span>



| <span data-ttu-id="3b8ef-128">Formato de textura</span><span class="sxs-lookup"><span data-stu-id="3b8ef-128">Texture Format</span></span>                                                                                          | <span data-ttu-id="3b8ef-129">Valores predeterminados para los componentes que faltan</span><span class="sxs-lookup"><span data-stu-id="3b8ef-129">Default Values for missing components</span></span> |
|---------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="3b8ef-130">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="3b8ef-130">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="3b8ef-131">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="3b8ef-131">A = 1.0</span></span>                               |
| <span data-ttu-id="3b8ef-132">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="3b8ef-132">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="3b8ef-133">B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="3b8ef-133">B = A = 1.0</span></span>                           |
| <span data-ttu-id="3b8ef-134">D3DFMT \_ A8</span><span class="sxs-lookup"><span data-stu-id="3b8ef-134">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="3b8ef-135">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="3b8ef-135">R = G = B = 0.0</span></span>                       |
| <span data-ttu-id="3b8ef-136">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="3b8ef-136">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="3b8ef-137">G = B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="3b8ef-137">G = B = A = 1.0</span></span>                       |
| <span data-ttu-id="3b8ef-138">Todos los formatos de profundidad/estarcido</span><span class="sxs-lookup"><span data-stu-id="3b8ef-138">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="3b8ef-139">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="3b8ef-139">R = B = 0.0, A = 1.0</span></span>                  |



 

<span data-ttu-id="3b8ef-140">Esta instrucción es compatible con las siguientes versiones:</span><span class="sxs-lookup"><span data-stu-id="3b8ef-140">This instruction is supported in the following versions:</span></span>



| <span data-ttu-id="3b8ef-141">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="3b8ef-141">Pixel shader versions</span></span> | <span data-ttu-id="3b8ef-142">1\_1</span><span class="sxs-lookup"><span data-stu-id="3b8ef-142">1\_1</span></span> | <span data-ttu-id="3b8ef-143">1\_2</span><span class="sxs-lookup"><span data-stu-id="3b8ef-143">1\_2</span></span> | <span data-ttu-id="3b8ef-144">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3b8ef-144">1\_3</span></span> | <span data-ttu-id="3b8ef-145">1\_4</span><span class="sxs-lookup"><span data-stu-id="3b8ef-145">1\_4</span></span> | <span data-ttu-id="3b8ef-146">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3b8ef-146">2\_0</span></span> | <span data-ttu-id="3b8ef-147">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3b8ef-147">2\_x</span></span> | <span data-ttu-id="3b8ef-148">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3b8ef-148">2\_sw</span></span> | <span data-ttu-id="3b8ef-149">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3b8ef-149">3\_0</span></span> | <span data-ttu-id="3b8ef-150">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3b8ef-150">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3b8ef-151">texldp</span><span class="sxs-lookup"><span data-stu-id="3b8ef-151">texldp</span></span>                |      |      |      |      | <span data-ttu-id="3b8ef-152">x</span><span class="sxs-lookup"><span data-stu-id="3b8ef-152">x</span></span>    | <span data-ttu-id="3b8ef-153">x</span><span class="sxs-lookup"><span data-stu-id="3b8ef-153">x</span></span>    | <span data-ttu-id="3b8ef-154">x</span><span class="sxs-lookup"><span data-stu-id="3b8ef-154">x</span></span>     | <span data-ttu-id="3b8ef-155">x</span><span class="sxs-lookup"><span data-stu-id="3b8ef-155">x</span></span>    | <span data-ttu-id="3b8ef-156">x</span><span class="sxs-lookup"><span data-stu-id="3b8ef-156">x</span></span>     |



 

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="3b8ef-157">PS \_ 2 \_ 0 y PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3b8ef-157">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="3b8ef-158">DST debe ser un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) y solo se permite la máscara xyzw (máscara predeterminada).</span><span class="sxs-lookup"><span data-stu-id="3b8ef-158">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="3b8ef-159">src0 debe ser un registro de [coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) o un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), sin modificador ni swizzle.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-159">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="3b8ef-160">SRC1 debe ser una [muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sin \# modificador o swizzle.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-160">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="3b8ef-161">Si \_ \_ no se establece el bit de límite de D3DD3DPSHADERCAPS2 0 NODEPENDENTREADLIMIT (en D3DPSHADERCAPS2 \_ 0), una instrucción de textura determinada ([texld](texld---ps-1-4.md), texldp, [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) puede depender, como máximo, de tercer orden.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-161">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction ([texld](texld---ps-1-4.md), texldp, [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) ) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="3b8ef-162">Una instrucción de textura dependiente de primer orden es una instrucción de textura en la que:</span><span class="sxs-lookup"><span data-stu-id="3b8ef-162">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="3b8ef-163">src0 es un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# )</span><span class="sxs-lookup"><span data-stu-id="3b8ef-163">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#)</span></span>
-   <span data-ttu-id="3b8ef-164">DST se escribió previamente y se ha escrito de nuevo.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-164">dst was previously written, now being written again.</span></span>

<span data-ttu-id="3b8ef-165">Una instrucción de textura dependiente de segundo orden se define como una instrucción de textura que lee o escribe en un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) cuyo contenido, antes de ejecutar la instrucción de textura, depende (quizás indirectamente) del resultado de una instrucción de textura dependiente de primer orden.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-165">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="3b8ef-166">Una instrucción de textura dependiente del orden de<sup>TH</sup>se deriva de una instrucción de textura de n-1)<sup>TH</sup>-order.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-166">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="3b8ef-167">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3b8ef-167">ps\_3\_0</span></span>

<span data-ttu-id="3b8ef-168">Para PS \_ 3 \_ 0, SRC1 debe ser un [muestreador (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , sin modificador.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-168">For ps\_3\_0, src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="3b8ef-169">Swizzle se permite en SRC1 y, cuando se aplica, los resultados de la búsqueda de texturas son swizzled anteriores antes de escribirse en el DST.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-169">Swizzle is allowed on src1, and when applied, the texture lookup results are pre-swizzled before written to dst.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b8ef-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b8ef-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b8ef-171">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="3b8ef-171">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 