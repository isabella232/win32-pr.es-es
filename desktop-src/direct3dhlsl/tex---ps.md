---
title: Tex-PS
description: Carga el registro de destino con datos de color (RGBA) muestreados a partir de una textura. La textura debe estar enlazada a una fase de textura determinada (n) mediante SetTexture. El muestreo de textura está controlado por SetSamplerState.
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3070883b167d26cf31f7d7f388f6bd3736a4bde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995410"
---
# <a name="tex---ps"></a><span data-ttu-id="8191e-105">Tex-PS</span><span class="sxs-lookup"><span data-stu-id="8191e-105">tex - ps</span></span>

<span data-ttu-id="8191e-106">Carga el registro de destino con datos de color (RGBA) muestreados a partir de una textura.</span><span class="sxs-lookup"><span data-stu-id="8191e-106">Loads the destination register with color data (RGBA) sampled from a texture.</span></span> <span data-ttu-id="8191e-107">La textura debe estar enlazada a una fase de textura determinada (n) mediante [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span><span class="sxs-lookup"><span data-stu-id="8191e-107">The texture must be bound to a particular texture stage (n) using [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="8191e-108">El muestreo de textura está controlado por [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="8191e-108">Texture sampling is controlled by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span>

## <a name="syntax"></a><span data-ttu-id="8191e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8191e-109">Syntax</span></span>



| <span data-ttu-id="8191e-110">Tex DST</span><span class="sxs-lookup"><span data-stu-id="8191e-110">tex dst</span></span> |
|---------|



 

<span data-ttu-id="8191e-111">, donde</span><span class="sxs-lookup"><span data-stu-id="8191e-111">where</span></span>

-   <span data-ttu-id="8191e-112">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="8191e-112">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="8191e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8191e-113">Remarks</span></span>



| <span data-ttu-id="8191e-114">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="8191e-114">Pixel shader versions</span></span> | <span data-ttu-id="8191e-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="8191e-115">1\_1</span></span> | <span data-ttu-id="8191e-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="8191e-116">1\_2</span></span> | <span data-ttu-id="8191e-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8191e-117">1\_3</span></span> | <span data-ttu-id="8191e-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="8191e-118">1\_4</span></span> | <span data-ttu-id="8191e-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8191e-119">2\_0</span></span> | <span data-ttu-id="8191e-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8191e-120">2\_x</span></span> | <span data-ttu-id="8191e-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8191e-121">2\_sw</span></span> | <span data-ttu-id="8191e-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8191e-122">3\_0</span></span> | <span data-ttu-id="8191e-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8191e-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="8191e-124">tex</span><span class="sxs-lookup"><span data-stu-id="8191e-124">tex</span></span>                   | <span data-ttu-id="8191e-125">x</span><span class="sxs-lookup"><span data-stu-id="8191e-125">x</span></span>    | <span data-ttu-id="8191e-126">x</span><span class="sxs-lookup"><span data-stu-id="8191e-126">x</span></span>    | <span data-ttu-id="8191e-127">x</span><span class="sxs-lookup"><span data-stu-id="8191e-127">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="8191e-128">El número de registro de destino especifica el número de fase de textura.</span><span class="sxs-lookup"><span data-stu-id="8191e-128">The destination register number specifies the texture stage number.</span></span>

<span data-ttu-id="8191e-129">El muestreo de textura usa coordenadas de textura para buscar, o muestra, un valor de color en las coordenadas especificadas (u, v, w, q), teniendo en cuenta los atributos de estado de fase de textura.</span><span class="sxs-lookup"><span data-stu-id="8191e-129">Texture sampling uses texture coordinates to look up, or sample, a color value at the specified (u,v,w,q) coordinates while taking into account the texture stage state attributes.</span></span>

<span data-ttu-id="8191e-130">Los datos de coordenadas de textura se interpolan a partir de los datos de coordenadas de textura de vértices y se asocian a una fase de textura específica.</span><span class="sxs-lookup"><span data-stu-id="8191e-130">The texture coordinate data is interpolated from the vertex texture coordinate data and is associated with a specific texture stage.</span></span> <span data-ttu-id="8191e-131">La Asociación predeterminada es una asignación de uno a uno entre el número de fase de textura y el orden de las declaraciones de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="8191e-131">The default association is a one-to-one mapping between texture stage number and texture coordinate declaration order.</span></span> <span data-ttu-id="8191e-132">Esto significa que el primer conjunto de coordenadas de textura definido en el formato de vértice está asociado de forma predeterminada a la fase de textura 0.</span><span class="sxs-lookup"><span data-stu-id="8191e-132">This means that the first set of texture coordinates defined in the vertex format are by default associated with texture stage 0.</span></span>

<span data-ttu-id="8191e-133">Las coordenadas de textura pueden estar asociadas a cualquier fase mediante dos técnicas.</span><span class="sxs-lookup"><span data-stu-id="8191e-133">Texture coordinates may be associated with any stage using two techniques.</span></span> <span data-ttu-id="8191e-134">Cuando se usa un sombreador de vértices de función fijo o la canalización de funciones fijas, la marca de estado de fase de textura TSS \_ TEXCOORDINDEX se puede usar en [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) para asociar coordenadas a una fase.</span><span class="sxs-lookup"><span data-stu-id="8191e-134">When using a fixed function vertex shader or the fixed function pipeline, the texture stage state flag TSS\_TEXCOORDINDEX can be used in [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) to associate coordinates to a stage.</span></span> <span data-ttu-id="8191e-135">De lo contrario, el sombreador de vértices oTn registra las coordenadas de textura cuando se usa un sombreador de vértices programable.</span><span class="sxs-lookup"><span data-stu-id="8191e-135">Otherwise, the texture coordinates are output by the vertex shader oTₙ registers when using a programmable vertex shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8191e-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8191e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8191e-137">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="8191e-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 