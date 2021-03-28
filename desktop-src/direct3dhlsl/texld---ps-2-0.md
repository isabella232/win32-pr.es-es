---
title: texld-ps_2_0 y arriba
description: Muestra una textura en una muestra determinada, usando las coordenadas de textura proporcionadas. Esta instrucción es diferente de la instrucción texld-PS \_ 1 \_ 4 utilizada en el sombreador de píxeles versión 1 \_ 4.
ms.assetid: 2b0d02b4-d9dd-4388-aa86-03b27bc4fdc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b71990e230290403bca2a5af11eeca11b093402f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533273"
---
# <a name="texld---ps_2_0-and-up"></a><span data-ttu-id="91fe6-104">texld-PS \_ 2 \_ 0 y arriba</span><span class="sxs-lookup"><span data-stu-id="91fe6-104">texld - ps\_2\_0 and up</span></span>

<span data-ttu-id="91fe6-105">Muestra una textura en una muestra determinada, usando las coordenadas de textura proporcionadas.</span><span class="sxs-lookup"><span data-stu-id="91fe6-105">Sample a texture at a particular sampler, using provided texture coordinates.</span></span> <span data-ttu-id="91fe6-106">Esta instrucción es diferente de la instrucción [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) utilizada en el sombreador de píxeles versión 1 \_ 4.</span><span class="sxs-lookup"><span data-stu-id="91fe6-106">This instruction is different from the [texld - ps\_1\_4](texld---ps-1-4.md) instruction used in pixel shader version 1\_4.</span></span>

## <a name="syntax"></a><span data-ttu-id="91fe6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91fe6-107">Syntax</span></span>



| <span data-ttu-id="91fe6-108">texld DST, src0, SRC1</span><span class="sxs-lookup"><span data-stu-id="91fe6-108">texld dst, src0, src1</span></span> |
|-----------------------|



 

<span data-ttu-id="91fe6-109">Donde:</span><span class="sxs-lookup"><span data-stu-id="91fe6-109">Where:</span></span>

-   <span data-ttu-id="91fe6-110">DST es un registro de destino.</span><span class="sxs-lookup"><span data-stu-id="91fe6-110">dst is a destination register.</span></span>
-   <span data-ttu-id="91fe6-111">src0 es un registro de origen que proporciona las coordenadas de textura para el ejemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="91fe6-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span>
-   <span data-ttu-id="91fe6-112">SRC1 identifica la [muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , donde \# especifica el número de muestra de textura que se muestra.</span><span class="sxs-lookup"><span data-stu-id="91fe6-112">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="91fe6-113">La muestra le ha asociado una textura y un estado de muestra definido por [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="91fe6-113">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="91fe6-114">PS \_ 2 \_ 0 y PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="91fe6-114">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="91fe6-115">DST debe ser un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) y solo se permite la máscara xyzw (máscara predeterminada).</span><span class="sxs-lookup"><span data-stu-id="91fe6-115">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="91fe6-116">src0 debe ser un registro de [coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) o un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), sin modificador ni swizzle.</span><span class="sxs-lookup"><span data-stu-id="91fe6-116">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="91fe6-117">SRC1 debe ser una [muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sin \# modificador o swizzle.</span><span class="sxs-lookup"><span data-stu-id="91fe6-117">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="91fe6-118">Si \_ \_ no se establece el bit de límite de D3DD3DPSHADERCAPS2 0 NODEPENDENTREADLIMIT (en D3DPSHADERCAPS2 \_ 0), una instrucción de textura determinada ([texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) puede depender, como máximo, de tercer orden.</span><span class="sxs-lookup"><span data-stu-id="91fe6-118">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction ([texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) ) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="91fe6-119">Una instrucción de textura dependiente de primer orden es una instrucción de textura en la que:</span><span class="sxs-lookup"><span data-stu-id="91fe6-119">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="91fe6-120">src0 es un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="91fe6-120">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="91fe6-121">DST se escribió previamente y se ha escrito de nuevo.</span><span class="sxs-lookup"><span data-stu-id="91fe6-121">dst was previously written, now being written again.</span></span>

<span data-ttu-id="91fe6-122">Una instrucción de textura dependiente de segundo orden se define como una instrucción de textura que lee o escribe en un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) cuyo contenido, antes de ejecutar la instrucción de textura, depende (quizás indirectamente) del resultado de una instrucción de textura dependiente de primer orden.</span><span class="sxs-lookup"><span data-stu-id="91fe6-122">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="91fe6-123">Una instrucción de textura dependiente del orden de<sup>TH</sup>se deriva de una instrucción de textura de n-1)<sup>TH</sup>-order.</span><span class="sxs-lookup"><span data-stu-id="91fe6-123">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="91fe6-124">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="91fe6-124">ps\_3\_0</span></span>

<span data-ttu-id="91fe6-125">SRC1 debe ser una [muestra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) , sin \# modificador.</span><span class="sxs-lookup"><span data-stu-id="91fe6-125">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="91fe6-126">Swizzle se permite en src0 o SRC1.</span><span class="sxs-lookup"><span data-stu-id="91fe6-126">Swizzle is allowed on src0 or src1.</span></span> <span data-ttu-id="91fe6-127">Swizzle se aplica a la textura coordintates antes de la búsqueda de textura.</span><span class="sxs-lookup"><span data-stu-id="91fe6-127">The swizzle is applied to the texture coordintates before texture lookup.</span></span>

## <a name="remarks"></a><span data-ttu-id="91fe6-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91fe6-128">Remarks</span></span>

<span data-ttu-id="91fe6-129">Esta instrucción es compatible con las siguientes versiones:</span><span class="sxs-lookup"><span data-stu-id="91fe6-129">This instruction is supported in the following versions:</span></span>



| <span data-ttu-id="91fe6-130">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="91fe6-130">Pixel shader versions</span></span> | <span data-ttu-id="91fe6-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="91fe6-131">1\_1</span></span> | <span data-ttu-id="91fe6-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="91fe6-132">1\_2</span></span> | <span data-ttu-id="91fe6-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="91fe6-133">1\_3</span></span> | <span data-ttu-id="91fe6-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="91fe6-134">1\_4</span></span> | <span data-ttu-id="91fe6-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="91fe6-135">2\_0</span></span> | <span data-ttu-id="91fe6-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="91fe6-136">2\_x</span></span> | <span data-ttu-id="91fe6-137">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="91fe6-137">2\_sw</span></span> | <span data-ttu-id="91fe6-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="91fe6-138">3\_0</span></span> | <span data-ttu-id="91fe6-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="91fe6-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="91fe6-140">texld</span><span class="sxs-lookup"><span data-stu-id="91fe6-140">texld</span></span>                 |      |      |      |      | <span data-ttu-id="91fe6-141">x</span><span class="sxs-lookup"><span data-stu-id="91fe6-141">x</span></span>    | <span data-ttu-id="91fe6-142">x</span><span class="sxs-lookup"><span data-stu-id="91fe6-142">x</span></span>    | <span data-ttu-id="91fe6-143">x</span><span class="sxs-lookup"><span data-stu-id="91fe6-143">x</span></span>     | <span data-ttu-id="91fe6-144">x</span><span class="sxs-lookup"><span data-stu-id="91fe6-144">x</span></span>    | <span data-ttu-id="91fe6-145">x</span><span class="sxs-lookup"><span data-stu-id="91fe6-145">x</span></span>     |



 

<span data-ttu-id="91fe6-146">El número de coordenadas necesarias para que src0 realice el ejemplo de textura depende de cómo se declaró SRC1, además del componente. w.</span><span class="sxs-lookup"><span data-stu-id="91fe6-146">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="91fe6-147">Los tipos de muestra se declaran con [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md).</span><span class="sxs-lookup"><span data-stu-id="91fe6-147">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="91fe6-148">Si SRC1 se declara como una muestra 2D, src0 debe contener coordenadas. XY; Si SRC1 se declara como una muestra de cubo o una muestra de volumen, src0 debe contener coordenadas. XYZ.</span><span class="sxs-lookup"><span data-stu-id="91fe6-148">If src1 is declared as a 2D sampler, then src0 must contain .xy coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyz coordinates.</span></span> <span data-ttu-id="91fe6-149">Se permite el muestreo de una textura con menos dimensiones que las presentes en la coordenada de textura, ya que los componentes de coordenadas de textura adicionales se omiten.</span><span class="sxs-lookup"><span data-stu-id="91fe6-149">Sampling a texture with fewer dimensions than are present in the texture coordinate is allowed since the extra texture coordinate component(s) are ignored.</span></span>

<span data-ttu-id="91fe6-150">Si la textura de origen contiene menos de cuatro componentes, los valores predeterminados se colocan en los componentes que faltan.</span><span class="sxs-lookup"><span data-stu-id="91fe6-150">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="91fe6-151">Los valores predeterminados dependen del formato de textura, tal como se muestra en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="91fe6-151">Defaults depend on the texture format as shown in the following table:</span></span>



| <span data-ttu-id="91fe6-152">Formato de textura</span><span class="sxs-lookup"><span data-stu-id="91fe6-152">Texture Format</span></span>                                                                                          | <span data-ttu-id="91fe6-153">Valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="91fe6-153">Default Values</span></span>       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="91fe6-154">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="91fe6-154">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="91fe6-155">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="91fe6-155">A = 1.0</span></span>              |
| <span data-ttu-id="91fe6-156">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="91fe6-156">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="91fe6-157">B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="91fe6-157">B = A = 1.0</span></span>          |
| <span data-ttu-id="91fe6-158">D3DFMT \_ A8</span><span class="sxs-lookup"><span data-stu-id="91fe6-158">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="91fe6-159">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="91fe6-159">R = G = B = 0.0</span></span>      |
| <span data-ttu-id="91fe6-160">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="91fe6-160">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="91fe6-161">G = B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="91fe6-161">G = B = A = 1.0</span></span>      |
| <span data-ttu-id="91fe6-162">Todos los formatos de profundidad/estarcido</span><span class="sxs-lookup"><span data-stu-id="91fe6-162">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="91fe6-163">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="91fe6-163">R = B = 0.0, A = 1.0</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="91fe6-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91fe6-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91fe6-165">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="91fe6-165">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 