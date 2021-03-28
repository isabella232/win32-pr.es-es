---
title: 'Texture2D:: GatherCmpAlpha (S, Float, Float, int) (función)'
description: 'En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con respecto a un valor de comparación. | Texture2D:: GatherCmpAlpha (S, Float, Float, int) (función)'
ms.assetid: 6fa60604-1eac-405d-bffa-3055569b7a09
keywords:
- GatherCmpAlpha de función HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a7f7fcdc6e24cac5c04068fda7f781d0bdd376a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424179"
---
# <a name="texture2dgathercmpalphasfloatfloatint-function"></a><span data-ttu-id="b25d9-105">Texture2D:: GatherCmpAlpha (S, Float, Float, int) (función)</span><span class="sxs-lookup"><span data-stu-id="b25d9-105">Texture2D::GatherCmpAlpha(S,float,float,int) function</span></span>

<span data-ttu-id="b25d9-106">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="b25d9-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b25d9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b25d9-107">Syntax</span></span>

``` syntax
float4 GatherCmpAlpha(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="b25d9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b25d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b25d9-109">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b25d9-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b25d9-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="b25d9-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="b25d9-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="b25d9-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="b25d9-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b25d9-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b25d9-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="b25d9-113">Type: **float2**</span></span>

<span data-ttu-id="b25d9-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="b25d9-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="b25d9-115">*comparar \_ valor* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b25d9-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b25d9-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b25d9-116">Type: **float**</span></span>

<span data-ttu-id="b25d9-117">Valor que se va a comparar cada uno con cada valor muestreado.</span><span class="sxs-lookup"><span data-stu-id="b25d9-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="b25d9-118">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b25d9-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b25d9-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="b25d9-119">Type: **int2**</span></span>

<span data-ttu-id="b25d9-120">Desplazamiento que se aplica a la coordenada de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="b25d9-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b25d9-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b25d9-121">Return value</span></span>

<span data-ttu-id="b25d9-122">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="b25d9-122">Type: **float4**</span></span>

<span data-ttu-id="b25d9-123">Un valor de cuatro componentes, cada componente es el resultado de una comparación por componente.</span><span class="sxs-lookup"><span data-stu-id="b25d9-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="b25d9-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b25d9-124">Remarks</span></span>

<span data-ttu-id="b25d9-125">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="b25d9-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="b25d9-126">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b25d9-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b25d9-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="b25d9-127">Vertex</span></span> | <span data-ttu-id="b25d9-128">Casco</span><span class="sxs-lookup"><span data-stu-id="b25d9-128">Hull</span></span> | <span data-ttu-id="b25d9-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="b25d9-129">Domain</span></span> | <span data-ttu-id="b25d9-130">Geometría</span><span class="sxs-lookup"><span data-stu-id="b25d9-130">Geometry</span></span> | <span data-ttu-id="b25d9-131">Píxel</span><span class="sxs-lookup"><span data-stu-id="b25d9-131">Pixel</span></span> | <span data-ttu-id="b25d9-132">Compute</span><span class="sxs-lookup"><span data-stu-id="b25d9-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b25d9-133">x</span><span class="sxs-lookup"><span data-stu-id="b25d9-133">x</span></span>      | <span data-ttu-id="b25d9-134">x</span><span class="sxs-lookup"><span data-stu-id="b25d9-134">x</span></span>    | <span data-ttu-id="b25d9-135">x</span><span class="sxs-lookup"><span data-stu-id="b25d9-135">x</span></span>      | <span data-ttu-id="b25d9-136">x</span><span class="sxs-lookup"><span data-stu-id="b25d9-136">x</span></span>        | <span data-ttu-id="b25d9-137">x</span><span class="sxs-lookup"><span data-stu-id="b25d9-137">x</span></span>     | <span data-ttu-id="b25d9-138">x</span><span class="sxs-lookup"><span data-stu-id="b25d9-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b25d9-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="b25d9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b25d9-140">Métodos GatherCmpAlpha</span><span class="sxs-lookup"><span data-stu-id="b25d9-140">GatherCmpAlpha methods</span></span>](texture2d-gathercmpalpha.md)
</dt> <dt>

[<span data-ttu-id="b25d9-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b25d9-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




