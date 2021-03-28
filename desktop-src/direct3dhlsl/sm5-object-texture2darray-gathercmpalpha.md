---
title: 'Texture2DArray:: GatherCmpAlpha (S, Float, Float, int) (función)'
description: 'En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con respecto a un valor de comparación. | Texture2DArray:: GatherCmpAlpha (S, Float, Float, int) (función)'
ms.assetid: d5fc78eb-2378-4e63-a712-c6f4ef9fc729
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
ms.openlocfilehash: 42f11131ebf377ddc64be5309c3edf77214ddd4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362351"
---
# <a name="texture2darraygathercmpalphasfloatfloatint-function"></a><span data-ttu-id="591cb-105">Texture2DArray:: GatherCmpAlpha (S, Float, Float, int) (función)</span><span class="sxs-lookup"><span data-stu-id="591cb-105">Texture2DArray::GatherCmpAlpha(S,float,float,int) function</span></span>

<span data-ttu-id="591cb-106">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="591cb-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="591cb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="591cb-107">Syntax</span></span>

``` syntax
float4 GatherCmpAlpha(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="591cb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="591cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="591cb-109">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="591cb-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="591cb-110">Tipo: **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="591cb-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="591cb-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="591cb-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="591cb-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="591cb-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="591cb-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="591cb-113">Type: **float3**</span></span>

<span data-ttu-id="591cb-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="591cb-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="591cb-115">*comparar \_ valor* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="591cb-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="591cb-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="591cb-116">Type: **float**</span></span>

<span data-ttu-id="591cb-117">Valor que se va a comparar cada uno con cada valor muestreado.</span><span class="sxs-lookup"><span data-stu-id="591cb-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="591cb-118">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="591cb-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="591cb-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="591cb-119">Type: **int2**</span></span>

<span data-ttu-id="591cb-120">Desplazamiento que se aplica a la coordenada de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="591cb-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="591cb-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="591cb-121">Return value</span></span>

<span data-ttu-id="591cb-122">Tipo: **FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="591cb-122">Type: **float4**</span></span>

<span data-ttu-id="591cb-123">Un valor de cuatro componentes, cada componente es el resultado de una comparación por componente.</span><span class="sxs-lookup"><span data-stu-id="591cb-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="591cb-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="591cb-124">Remarks</span></span>

<span data-ttu-id="591cb-125">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="591cb-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="591cb-126">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="591cb-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="591cb-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="591cb-127">Vertex</span></span> | <span data-ttu-id="591cb-128">Casco</span><span class="sxs-lookup"><span data-stu-id="591cb-128">Hull</span></span> | <span data-ttu-id="591cb-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="591cb-129">Domain</span></span> | <span data-ttu-id="591cb-130">Geometría</span><span class="sxs-lookup"><span data-stu-id="591cb-130">Geometry</span></span> | <span data-ttu-id="591cb-131">Píxel</span><span class="sxs-lookup"><span data-stu-id="591cb-131">Pixel</span></span> | <span data-ttu-id="591cb-132">Compute</span><span class="sxs-lookup"><span data-stu-id="591cb-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="591cb-133">x</span><span class="sxs-lookup"><span data-stu-id="591cb-133">x</span></span>      | <span data-ttu-id="591cb-134">x</span><span class="sxs-lookup"><span data-stu-id="591cb-134">x</span></span>    | <span data-ttu-id="591cb-135">x</span><span class="sxs-lookup"><span data-stu-id="591cb-135">x</span></span>      | <span data-ttu-id="591cb-136">x</span><span class="sxs-lookup"><span data-stu-id="591cb-136">x</span></span>        | <span data-ttu-id="591cb-137">x</span><span class="sxs-lookup"><span data-stu-id="591cb-137">x</span></span>     | <span data-ttu-id="591cb-138">x</span><span class="sxs-lookup"><span data-stu-id="591cb-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="591cb-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="591cb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="591cb-140">Métodos GatherCmpAlpha</span><span class="sxs-lookup"><span data-stu-id="591cb-140">GatherCmpAlpha methods</span></span>](texture2darray-gathercmpalpha.md)
</dt> <dt>

[<span data-ttu-id="591cb-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="591cb-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




