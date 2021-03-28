---
title: 'Texture2D:: GatherCmp (S, Float, Float, int) (función)'
description: 'Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve su comparación con un valor de comparación. | Texture2D:: GatherCmp (S, Float, Float, int) (función)'
ms.assetid: 1084bcb3-2834-400a-98ff-4e3182f63f20
keywords:
- GatherCmp de función HLSL
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6005d8a95d3ec5ed5cddd9c4fbe6a42f36b7f55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986354"
---
# <a name="texture2dgathercmpsfloatfloatint-function"></a><span data-ttu-id="6ce17-105">Texture2D:: GatherCmp (S, Float, Float, int) (función)</span><span class="sxs-lookup"><span data-stu-id="6ce17-105">Texture2D::GatherCmp(S,float,float,int) function</span></span>

<span data-ttu-id="6ce17-106">Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve su comparación con un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="6ce17-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ce17-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ce17-107">Syntax</span></span>

``` syntax
float4 GatherCmp(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="6ce17-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ce17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ce17-109">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="6ce17-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce17-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="6ce17-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="6ce17-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="6ce17-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="6ce17-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6ce17-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce17-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="6ce17-113">Type: **float2**</span></span>

<span data-ttu-id="6ce17-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="6ce17-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="6ce17-115">*comparar \_ valor* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="6ce17-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce17-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6ce17-116">Type: **float**</span></span>

<span data-ttu-id="6ce17-117">Valor que se va a comparar cada uno con cada valor muestreado.</span><span class="sxs-lookup"><span data-stu-id="6ce17-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="6ce17-118">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ce17-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce17-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="6ce17-119">Type: **int2**</span></span>

<span data-ttu-id="6ce17-120">Desplazamiento que se aplica a la coordenada de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="6ce17-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ce17-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ce17-121">Return value</span></span>

<span data-ttu-id="6ce17-122">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="6ce17-122">Type: **float4**</span></span>

<span data-ttu-id="6ce17-123">Un valor de cuatro componentes, cada componente es el resultado de una comparación por componente.</span><span class="sxs-lookup"><span data-stu-id="6ce17-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ce17-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ce17-124">Remarks</span></span>

<span data-ttu-id="6ce17-125">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="6ce17-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="6ce17-126">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="6ce17-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6ce17-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="6ce17-127">Vertex</span></span> | <span data-ttu-id="6ce17-128">Casco</span><span class="sxs-lookup"><span data-stu-id="6ce17-128">Hull</span></span> | <span data-ttu-id="6ce17-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="6ce17-129">Domain</span></span> | <span data-ttu-id="6ce17-130">Geometría</span><span class="sxs-lookup"><span data-stu-id="6ce17-130">Geometry</span></span> | <span data-ttu-id="6ce17-131">Píxel</span><span class="sxs-lookup"><span data-stu-id="6ce17-131">Pixel</span></span> | <span data-ttu-id="6ce17-132">Compute</span><span class="sxs-lookup"><span data-stu-id="6ce17-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6ce17-133">x</span><span class="sxs-lookup"><span data-stu-id="6ce17-133">x</span></span>      | <span data-ttu-id="6ce17-134">x</span><span class="sxs-lookup"><span data-stu-id="6ce17-134">x</span></span>    | <span data-ttu-id="6ce17-135">x</span><span class="sxs-lookup"><span data-stu-id="6ce17-135">x</span></span>      | <span data-ttu-id="6ce17-136">x</span><span class="sxs-lookup"><span data-stu-id="6ce17-136">x</span></span>        | <span data-ttu-id="6ce17-137">x</span><span class="sxs-lookup"><span data-stu-id="6ce17-137">x</span></span>     | <span data-ttu-id="6ce17-138">x</span><span class="sxs-lookup"><span data-stu-id="6ce17-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6ce17-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ce17-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ce17-140">Métodos GatherCmp</span><span class="sxs-lookup"><span data-stu-id="6ce17-140">GatherCmp methods</span></span>](texture2d-gathercmp.md)
</dt> <dt>

[<span data-ttu-id="6ce17-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6ce17-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




