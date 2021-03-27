---
title: Muestra (Direct3D 9 ASM-PS)
description: Una muestra es un pseudo registro de entrada para un sombreador de píxeles, que se usa para identificar la fase de muestreo.
ms.assetid: 37cc28ae-fbd0-4f81-9e8e-f9609980d84e
keywords:
- Muestra, tipo (Direct3D 9 ASM-PS)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77875eed0827ad6bcb6d89111b13b6a31232dd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077930"
---
# <a name="sampler-direct3d-9-asm-ps"></a><span data-ttu-id="3c649-104">Muestra (Direct3D 9 ASM-PS)</span><span class="sxs-lookup"><span data-stu-id="3c649-104">Sampler (Direct3D 9 asm-ps)</span></span>

<span data-ttu-id="3c649-105">Una muestra es un pseudo registro de entrada para un sombreador de píxeles, que se usa para identificar la fase de muestreo.</span><span class="sxs-lookup"><span data-stu-id="3c649-105">A sampler is a input pseudo-register for a pixel shader, which is used to identify the sampling stage.</span></span> <span data-ttu-id="3c649-106">Hay registros de fase de muestreo de sombreador de 16 píxeles: S0 a S15.</span><span class="sxs-lookup"><span data-stu-id="3c649-106">There are 16 pixel shader sampling stage registers: s0 to s15.</span></span> <span data-ttu-id="3c649-107">Por lo tanto, se pueden leer hasta 16 superficies de textura en una sola fase de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3c649-107">Therefore, up to 16 texture surfaces can be read in a single shader pass.</span></span> <span data-ttu-id="3c649-108">Las instrucciones que usan un registro de muestra son texld y texldp.</span><span class="sxs-lookup"><span data-stu-id="3c649-108">The instructions that use a sampler register are texld and texldp.</span></span>

<span data-ttu-id="3c649-109">La muestra debe declararse antes de usarse con la instrucción [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="3c649-109">Sampler must be declared before use with the [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) instruction.</span></span>



| <span data-ttu-id="3c649-110">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="3c649-110">Pixel shader versions</span></span> | <span data-ttu-id="3c649-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="3c649-111">1\_1</span></span> | <span data-ttu-id="3c649-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="3c649-112">1\_2</span></span> | <span data-ttu-id="3c649-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3c649-113">1\_3</span></span> | <span data-ttu-id="3c649-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="3c649-114">1\_4</span></span> | <span data-ttu-id="3c649-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3c649-115">2\_0</span></span> | <span data-ttu-id="3c649-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3c649-116">2\_sw</span></span> | <span data-ttu-id="3c649-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3c649-117">2\_x</span></span> | <span data-ttu-id="3c649-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3c649-118">3\_0</span></span> | <span data-ttu-id="3c649-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3c649-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="3c649-120">Muestra</span><span class="sxs-lookup"><span data-stu-id="3c649-120">Sampler</span></span>               |      |      |      |      | <span data-ttu-id="3c649-121">x</span><span class="sxs-lookup"><span data-stu-id="3c649-121">x</span></span>    | <span data-ttu-id="3c649-122">x</span><span class="sxs-lookup"><span data-stu-id="3c649-122">x</span></span>     | <span data-ttu-id="3c649-123">x</span><span class="sxs-lookup"><span data-stu-id="3c649-123">x</span></span>    | <span data-ttu-id="3c649-124">x</span><span class="sxs-lookup"><span data-stu-id="3c649-124">x</span></span>    | <span data-ttu-id="3c649-125">x</span><span class="sxs-lookup"><span data-stu-id="3c649-125">x</span></span>     |



 

<span data-ttu-id="3c649-126">Los ejemplos son pseudo registros porque no se pueden leer ni escribir directamente en ellos.</span><span class="sxs-lookup"><span data-stu-id="3c649-126">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

<span data-ttu-id="3c649-127">Una unidad de muestreo corresponde a la fase de muestreo de textura, encapsulando el estado específico del muestreo proporcionado por [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="3c649-127">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="3c649-128">Cada muestra identifica de forma única una superficie de textura única, que se establece en la muestra correspondiente mediante [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="3c649-128">Each sampler uniquely identifies a single texture surface, which is set to the corresponding sampler using the [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="3c649-129">Sin embargo, la misma superficie de textura se puede establecer en varios muestreadores.</span><span class="sxs-lookup"><span data-stu-id="3c649-129">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="3c649-130">En el momento de dibujar, no se puede establecer una textura simultáneamente como un destino de representación y una textura en una fase.</span><span class="sxs-lookup"><span data-stu-id="3c649-130">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="3c649-131">Una muestra puede aparecer como el único argumento de la instrucción de carga de textura: [texldl-PS](texldl---ps.md).</span><span class="sxs-lookup"><span data-stu-id="3c649-131">A sampler might appear as the only argument in the texture load instruction: [texldl - ps](texldl---ps.md).</span></span>

<span data-ttu-id="3c649-132">En PS \_ 3 \_ 0, si se usa una muestra, debe declararse al principio del programa del sombreador mediante la instrucción [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="3c649-132">In ps\_3\_0, if a sampler is used, it needs to be declared at the beginning of the shader program using the [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md) instruction.</span></span>

<span data-ttu-id="3c649-133">El muestreo de una textura con una dimensión superior a la que se encuentra en las coordenadas de textura no es válido.</span><span class="sxs-lookup"><span data-stu-id="3c649-133">Sampling a texture with a higher dimension than is present in the texture coordinates is illegal.</span></span> <span data-ttu-id="3c649-134">El muestreo de una textura con una dimensión inferior a la que se encuentra en las coordenadas de textura omitirá las coordenadas de texturas adicionales.</span><span class="sxs-lookup"><span data-stu-id="3c649-134">Sampling a texture with a lower dimension than is present in the texture coordinates will ignore the extra texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c649-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c649-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c649-136">Registra</span><span class="sxs-lookup"><span data-stu-id="3c649-136">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 