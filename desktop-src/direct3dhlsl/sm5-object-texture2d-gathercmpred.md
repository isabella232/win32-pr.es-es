---
title: 'Texture2D:: GatherCmpRed (S, Float, Float, int) (función)'
description: 'Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente rojo con respecto a un valor de comparación. | Texture2D:: GatherCmpRed (S, Float, Float, int) (función)'
ms.assetid: bd5fdd3b-c1b0-4cb0-aec5-9fe020420e6c
keywords:
- GatherCmpRed de función HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e221dbe60141eb809d41361a0a6a93d8bf2a7d7e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362217"
---
# <a name="texture2dgathercmpredsfloatfloatint-function"></a><span data-ttu-id="a7f91-105">Texture2D:: GatherCmpRed (S, Float, Float, int) (función)</span><span class="sxs-lookup"><span data-stu-id="a7f91-105">Texture2D::GatherCmpRed(S,float,float,int) function</span></span>

<span data-ttu-id="a7f91-106">Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente rojo con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="a7f91-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7f91-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7f91-107">Syntax</span></span>

``` syntax
float4 GatherCmpRed(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="a7f91-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7f91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7f91-109">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="a7f91-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f91-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="a7f91-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="a7f91-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="a7f91-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="a7f91-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a7f91-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f91-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="a7f91-113">Type: **float2**</span></span>

<span data-ttu-id="a7f91-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="a7f91-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="a7f91-115">*comparar \_ valor* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="a7f91-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f91-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="a7f91-116">Type: **float**</span></span>

<span data-ttu-id="a7f91-117">Valor que se va a comparar cada uno con cada valor muestreado.</span><span class="sxs-lookup"><span data-stu-id="a7f91-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="a7f91-118">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7f91-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f91-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="a7f91-119">Type: **int2**</span></span>

<span data-ttu-id="a7f91-120">Desplazamiento que se aplica a la coordenada de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="a7f91-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7f91-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7f91-121">Return value</span></span>

<span data-ttu-id="a7f91-122">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="a7f91-122">Type: **float4**</span></span>

<span data-ttu-id="a7f91-123">Un valor de cuatro componentes, cada componente es el resultado de una comparación por componente.</span><span class="sxs-lookup"><span data-stu-id="a7f91-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7f91-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7f91-124">Remarks</span></span>

<span data-ttu-id="a7f91-125">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="a7f91-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="a7f91-126">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="a7f91-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a7f91-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="a7f91-127">Vertex</span></span> | <span data-ttu-id="a7f91-128">Casco</span><span class="sxs-lookup"><span data-stu-id="a7f91-128">Hull</span></span> | <span data-ttu-id="a7f91-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="a7f91-129">Domain</span></span> | <span data-ttu-id="a7f91-130">Geometría</span><span class="sxs-lookup"><span data-stu-id="a7f91-130">Geometry</span></span> | <span data-ttu-id="a7f91-131">Píxel</span><span class="sxs-lookup"><span data-stu-id="a7f91-131">Pixel</span></span> | <span data-ttu-id="a7f91-132">Compute</span><span class="sxs-lookup"><span data-stu-id="a7f91-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a7f91-133">x</span><span class="sxs-lookup"><span data-stu-id="a7f91-133">x</span></span>      | <span data-ttu-id="a7f91-134">x</span><span class="sxs-lookup"><span data-stu-id="a7f91-134">x</span></span>    | <span data-ttu-id="a7f91-135">x</span><span class="sxs-lookup"><span data-stu-id="a7f91-135">x</span></span>      | <span data-ttu-id="a7f91-136">x</span><span class="sxs-lookup"><span data-stu-id="a7f91-136">x</span></span>        | <span data-ttu-id="a7f91-137">x</span><span class="sxs-lookup"><span data-stu-id="a7f91-137">x</span></span>     | <span data-ttu-id="a7f91-138">x</span><span class="sxs-lookup"><span data-stu-id="a7f91-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a7f91-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7f91-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7f91-140">Métodos GatherCmpRed</span><span class="sxs-lookup"><span data-stu-id="a7f91-140">GatherCmpRed methods</span></span>](texture2d-gathercmpred.md)
</dt> <dt>

[<span data-ttu-id="a7f91-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a7f91-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




