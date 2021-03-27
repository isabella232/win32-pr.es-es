---
title: 'Texture2DArray:: GatherCmpBlue (S, Float, Float, int) (función)'
description: 'En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación. | Texture2DArray:: GatherCmpBlue (S, Float, Float, int) (función)'
ms.assetid: 5fa23e27-368a-4c55-b6d6-33506c932a43
keywords:
- GatherCmpBlue de función HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42c645333cc45c6de55a609439445936f65b85f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820634"
---
# <a name="texture2darraygathercmpbluesfloatfloatint-function"></a><span data-ttu-id="fbd38-105">Texture2DArray:: GatherCmpBlue (S, Float, Float, int) (función)</span><span class="sxs-lookup"><span data-stu-id="fbd38-105">Texture2DArray::GatherCmpBlue(S,float,float,int) function</span></span>

<span data-ttu-id="fbd38-106">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="fbd38-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd38-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fbd38-107">Syntax</span></span>

``` syntax
float4 GatherCmpBlue(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="fbd38-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbd38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbd38-109">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="fbd38-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbd38-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="fbd38-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="fbd38-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="fbd38-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="fbd38-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fbd38-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbd38-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="fbd38-113">Type: **float3**</span></span>

<span data-ttu-id="fbd38-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="fbd38-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="fbd38-115">*comparar \_ valor* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="fbd38-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbd38-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fbd38-116">Type: **float**</span></span>

<span data-ttu-id="fbd38-117">Valor que se va a comparar cada uno con cada valor muestreado.</span><span class="sxs-lookup"><span data-stu-id="fbd38-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="fbd38-118">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fbd38-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbd38-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="fbd38-119">Type: **int2**</span></span>

<span data-ttu-id="fbd38-120">Desplazamiento que se aplica a la coordenada de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="fbd38-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbd38-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fbd38-121">Return value</span></span>

<span data-ttu-id="fbd38-122">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="fbd38-122">Type: **float4**</span></span>

<span data-ttu-id="fbd38-123">Un valor de cuatro componentes, cada componente es el resultado de una comparación por componente.</span><span class="sxs-lookup"><span data-stu-id="fbd38-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbd38-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fbd38-124">Remarks</span></span>

<span data-ttu-id="fbd38-125">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="fbd38-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="fbd38-126">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="fbd38-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fbd38-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="fbd38-127">Vertex</span></span> | <span data-ttu-id="fbd38-128">Casco</span><span class="sxs-lookup"><span data-stu-id="fbd38-128">Hull</span></span> | <span data-ttu-id="fbd38-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="fbd38-129">Domain</span></span> | <span data-ttu-id="fbd38-130">Geometría</span><span class="sxs-lookup"><span data-stu-id="fbd38-130">Geometry</span></span> | <span data-ttu-id="fbd38-131">Píxel</span><span class="sxs-lookup"><span data-stu-id="fbd38-131">Pixel</span></span> | <span data-ttu-id="fbd38-132">Compute</span><span class="sxs-lookup"><span data-stu-id="fbd38-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fbd38-133">x</span><span class="sxs-lookup"><span data-stu-id="fbd38-133">x</span></span>      | <span data-ttu-id="fbd38-134">x</span><span class="sxs-lookup"><span data-stu-id="fbd38-134">x</span></span>    | <span data-ttu-id="fbd38-135">x</span><span class="sxs-lookup"><span data-stu-id="fbd38-135">x</span></span>      | <span data-ttu-id="fbd38-136">x</span><span class="sxs-lookup"><span data-stu-id="fbd38-136">x</span></span>        | <span data-ttu-id="fbd38-137">x</span><span class="sxs-lookup"><span data-stu-id="fbd38-137">x</span></span>     | <span data-ttu-id="fbd38-138">x</span><span class="sxs-lookup"><span data-stu-id="fbd38-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fbd38-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbd38-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbd38-140">Métodos GatherCmpBlue</span><span class="sxs-lookup"><span data-stu-id="fbd38-140">GatherCmpBlue methods</span></span>](texture2darray-gathercmpblue.md)
</dt> <dt>

[<span data-ttu-id="fbd38-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fbd38-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




