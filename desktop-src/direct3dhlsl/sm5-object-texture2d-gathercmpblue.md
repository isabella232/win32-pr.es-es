---
title: 'Texture2D:: GatherCmpBlue (S, Float, Float, int) (función)'
description: 'En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación. | Texture2D:: GatherCmpBlue (S, Float, Float, int) (función)'
ms.assetid: d8e03c55-18f1-4598-a700-9ba3a680d78a
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
ms.openlocfilehash: eedeb21141c1e694effe4eb8c7be70c828aa0a3c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998073"
---
# <a name="texture2dgathercmpbluesfloatfloatint-function"></a><span data-ttu-id="904c6-105">Texture2D:: GatherCmpBlue (S, Float, Float, int) (función)</span><span class="sxs-lookup"><span data-stu-id="904c6-105">Texture2D::GatherCmpBlue(S,float,float,int) function</span></span>

<span data-ttu-id="904c6-106">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="904c6-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="904c6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="904c6-107">Syntax</span></span>

``` syntax
float4 GatherCmpBlue(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="904c6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="904c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="904c6-109">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="904c6-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="904c6-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="904c6-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="904c6-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="904c6-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="904c6-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="904c6-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="904c6-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="904c6-113">Type: **float2**</span></span>

<span data-ttu-id="904c6-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="904c6-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="904c6-115">*comparar \_ valor* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="904c6-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="904c6-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="904c6-116">Type: **float**</span></span>

<span data-ttu-id="904c6-117">Valor que se va a comparar cada uno con cada valor muestreado.</span><span class="sxs-lookup"><span data-stu-id="904c6-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="904c6-118">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="904c6-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="904c6-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="904c6-119">Type: **int2**</span></span>

<span data-ttu-id="904c6-120">Desplazamiento que se aplica a la coordenada de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="904c6-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="904c6-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="904c6-121">Return value</span></span>

<span data-ttu-id="904c6-122">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="904c6-122">Type: **float4**</span></span>

<span data-ttu-id="904c6-123">Un valor de cuatro componentes, cada componente es el resultado de una comparación por componente.</span><span class="sxs-lookup"><span data-stu-id="904c6-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="904c6-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="904c6-124">Remarks</span></span>

<span data-ttu-id="904c6-125">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="904c6-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="904c6-126">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="904c6-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="904c6-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="904c6-127">Vertex</span></span> | <span data-ttu-id="904c6-128">Casco</span><span class="sxs-lookup"><span data-stu-id="904c6-128">Hull</span></span> | <span data-ttu-id="904c6-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="904c6-129">Domain</span></span> | <span data-ttu-id="904c6-130">Geometría</span><span class="sxs-lookup"><span data-stu-id="904c6-130">Geometry</span></span> | <span data-ttu-id="904c6-131">Píxel</span><span class="sxs-lookup"><span data-stu-id="904c6-131">Pixel</span></span> | <span data-ttu-id="904c6-132">Compute</span><span class="sxs-lookup"><span data-stu-id="904c6-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="904c6-133">x</span><span class="sxs-lookup"><span data-stu-id="904c6-133">x</span></span>      | <span data-ttu-id="904c6-134">x</span><span class="sxs-lookup"><span data-stu-id="904c6-134">x</span></span>    | <span data-ttu-id="904c6-135">x</span><span class="sxs-lookup"><span data-stu-id="904c6-135">x</span></span>      | <span data-ttu-id="904c6-136">x</span><span class="sxs-lookup"><span data-stu-id="904c6-136">x</span></span>        | <span data-ttu-id="904c6-137">x</span><span class="sxs-lookup"><span data-stu-id="904c6-137">x</span></span>     | <span data-ttu-id="904c6-138">x</span><span class="sxs-lookup"><span data-stu-id="904c6-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="904c6-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="904c6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="904c6-140">Métodos GatherCmpBlue</span><span class="sxs-lookup"><span data-stu-id="904c6-140">GatherCmpBlue methods</span></span>](texture2d-gathercmpblue.md)
</dt> <dt>

[<span data-ttu-id="904c6-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="904c6-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




