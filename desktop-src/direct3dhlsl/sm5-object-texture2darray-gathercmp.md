---
title: 'Texture2DArray:: GatherCmp (S, Float, Float, int) (función)'
description: 'Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve su comparación con un valor de comparación. | Texture2DArray:: GatherCmp (S, Float, Float, int) (función)'
ms.assetid: 7bb86448-cc73-4423-9ef4-149427cffc95
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
ms.openlocfilehash: fbac4c231f7a7070d3ca4549f3d1189b81292b8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986259"
---
# <a name="texture2darraygathercmpsfloatfloatint-function"></a><span data-ttu-id="4affe-105">Texture2DArray:: GatherCmp (S, Float, Float, int) (función)</span><span class="sxs-lookup"><span data-stu-id="4affe-105">Texture2DArray::GatherCmp(S,float,float,int) function</span></span>

<span data-ttu-id="4affe-106">Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve su comparación con un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="4affe-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4affe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4affe-107">Syntax</span></span>

``` syntax
float4 GatherCmp(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="4affe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4affe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4affe-109">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="4affe-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4affe-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="4affe-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="4affe-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="4affe-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="4affe-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4affe-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4affe-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="4affe-113">Type: **float3**</span></span>

<span data-ttu-id="4affe-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="4affe-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="4affe-115">*comparar \_ valor* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="4affe-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4affe-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="4affe-116">Type: **float**</span></span>

<span data-ttu-id="4affe-117">Valor que se va a comparar cada uno con cada valor muestreado.</span><span class="sxs-lookup"><span data-stu-id="4affe-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="4affe-118">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4affe-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4affe-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="4affe-119">Type: **int2**</span></span>

<span data-ttu-id="4affe-120">Desplazamiento que se aplica a la coordenada de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="4affe-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4affe-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4affe-121">Return value</span></span>

<span data-ttu-id="4affe-122">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="4affe-122">Type: **float4**</span></span>

<span data-ttu-id="4affe-123">Un valor de cuatro componentes, cada componente es el resultado de una comparación por componente.</span><span class="sxs-lookup"><span data-stu-id="4affe-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="4affe-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4affe-124">Remarks</span></span>

<span data-ttu-id="4affe-125">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="4affe-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="4affe-126">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4affe-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4affe-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="4affe-127">Vertex</span></span> | <span data-ttu-id="4affe-128">Casco</span><span class="sxs-lookup"><span data-stu-id="4affe-128">Hull</span></span> | <span data-ttu-id="4affe-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="4affe-129">Domain</span></span> | <span data-ttu-id="4affe-130">Geometría</span><span class="sxs-lookup"><span data-stu-id="4affe-130">Geometry</span></span> | <span data-ttu-id="4affe-131">Píxel</span><span class="sxs-lookup"><span data-stu-id="4affe-131">Pixel</span></span> | <span data-ttu-id="4affe-132">Compute</span><span class="sxs-lookup"><span data-stu-id="4affe-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4affe-133">x</span><span class="sxs-lookup"><span data-stu-id="4affe-133">x</span></span>      | <span data-ttu-id="4affe-134">x</span><span class="sxs-lookup"><span data-stu-id="4affe-134">x</span></span>    | <span data-ttu-id="4affe-135">x</span><span class="sxs-lookup"><span data-stu-id="4affe-135">x</span></span>      | <span data-ttu-id="4affe-136">x</span><span class="sxs-lookup"><span data-stu-id="4affe-136">x</span></span>        | <span data-ttu-id="4affe-137">x</span><span class="sxs-lookup"><span data-stu-id="4affe-137">x</span></span>     | <span data-ttu-id="4affe-138">x</span><span class="sxs-lookup"><span data-stu-id="4affe-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4affe-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="4affe-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4affe-140">Métodos GatherCmp</span><span class="sxs-lookup"><span data-stu-id="4affe-140">GatherCmp methods</span></span>](texture2darray-gathercmp.md)
</dt> <dt>

[<span data-ttu-id="4affe-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4affe-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




