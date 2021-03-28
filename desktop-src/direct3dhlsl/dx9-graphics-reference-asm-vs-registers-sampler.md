---
title: Muestra (Direct3D 9 ASM-vs)
description: Una muestra es un pseudo registro de entrada para un sombreador de vértices, que se usa para identificar la fase de muestreo. Hay cuatro muestreadores de sombreador de vértices S0 a S3. Se pueden leer cuatro superficies de textura en una sola fase de sombreador.
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- Muestra, tipo (Direct3D 9 ASM-vs)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 685f261da9d56dc29c0632d01cabbf29cd13a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421353"
---
# <a name="sampler-direct3d-9-asm-vs"></a><span data-ttu-id="edffa-106">Muestra (Direct3D 9 ASM-vs)</span><span class="sxs-lookup"><span data-stu-id="edffa-106">Sampler (Direct3D 9 asm-vs)</span></span>

<span data-ttu-id="edffa-107">Una muestra es un pseudo registro de entrada para un sombreador de vértices, que se usa para identificar la fase de muestreo.</span><span class="sxs-lookup"><span data-stu-id="edffa-107">A sampler is a input pseudo-register for a vertex shader, which is used to identify the sampling stage.</span></span> <span data-ttu-id="edffa-108">Hay cuatro muestreadores de sombreador de vértices: S0 a S3.</span><span class="sxs-lookup"><span data-stu-id="edffa-108">There are four vertex shader samplers: s0 to s3.</span></span> <span data-ttu-id="edffa-109">Se pueden leer cuatro superficies de textura en una sola fase de sombreador.</span><span class="sxs-lookup"><span data-stu-id="edffa-109">Four texture surfaces can be read in a single shader pass.</span></span>

<span data-ttu-id="edffa-110">El muestreador (Direct3D 9 ASM-vs) es un pseudo registro porque no se puede leer ni escribir directamente en ellos.</span><span class="sxs-lookup"><span data-stu-id="edffa-110">Sampler (Direct3D 9 asm-vs)s are pseudo registers because you cannot directly read or write to them.</span></span>

<span data-ttu-id="edffa-111">Una unidad de muestreo corresponde a la fase de muestreo de textura, encapsulando el estado específico del muestreo proporcionado por [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="edffa-111">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="edffa-112">Cada muestra identifica de forma única una superficie de textura única, que se establece en la muestra correspondiente mediante [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="edffa-112">Each sampler uniquely identifies a single texture surface, which is set to the corresponding sampler using the [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="edffa-113">Sin embargo, la misma superficie de textura se puede establecer en varios muestreadores.</span><span class="sxs-lookup"><span data-stu-id="edffa-113">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="edffa-114">En el momento de dibujar, no se puede establecer una textura simultáneamente como un destino de representación y una textura en una fase.</span><span class="sxs-lookup"><span data-stu-id="edffa-114">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="edffa-115">Dado que hay cuatro muestras, se pueden leer hasta cuatro superficies de textura desde en una única fase del sombreador.</span><span class="sxs-lookup"><span data-stu-id="edffa-115">Because there are four samplers, up to four texture surfaces can be read from in a single shader pass.</span></span> <span data-ttu-id="edffa-116">Una muestra puede aparecer como el único argumento de la instrucción de carga de textura: [texldl-vs](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="edffa-116">A sampler might appear as the only argument in the texture load instruction: [texldl - vs](texldl---vs.md).</span></span>

<span data-ttu-id="edffa-117">En vs \_ 3 \_ 0, si se usa una muestra, debe declararse al principio del programa del sombreador mediante la instrucción [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="edffa-117">In vs\_3\_0, if a sampler is used, it needs to be declared at the beginning of the shader program using the [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md) instruction.</span></span>



| <span data-ttu-id="edffa-118">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="edffa-118">Vertex shader versions</span></span> | <span data-ttu-id="edffa-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="edffa-119">1\_1</span></span> | <span data-ttu-id="edffa-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="edffa-120">2\_0</span></span> | <span data-ttu-id="edffa-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="edffa-121">2\_sw</span></span> | <span data-ttu-id="edffa-122">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="edffa-122">2\_x</span></span> | <span data-ttu-id="edffa-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="edffa-123">3\_0</span></span> | <span data-ttu-id="edffa-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="edffa-124">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="edffa-125">Muestra</span><span class="sxs-lookup"><span data-stu-id="edffa-125">Sampler</span></span>                |      |      |       |      | <span data-ttu-id="edffa-126">x</span><span class="sxs-lookup"><span data-stu-id="edffa-126">x</span></span>    | <span data-ttu-id="edffa-127">x</span><span class="sxs-lookup"><span data-stu-id="edffa-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="edffa-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="edffa-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edffa-129">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="edffa-129">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[<span data-ttu-id="edffa-130">Texturas de vértices en vs \_ 3 \_ 0 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="edffa-130">Vertex Textures in vs\_3\_0 (DirectX HLSL)</span></span>](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 