---
title: 'Texture2DArray:: GatherAlpha (S, Float, int) (función)'
description: 'Devuelve los componentes alfa de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal. | Texture2DArray:: GatherAlpha (S, Float, int) (función)'
ms.assetid: d7270277-53c1-4034-bf66-9a95bc1b51e4
keywords:
- GatherAlpha de función HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2052b780ab628a6a5bc174729119a9c2c8b8c8f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362164"
---
# <a name="texture2darraygatheralphasfloatint-function"></a><span data-ttu-id="0c95c-105">Texture2DArray:: GatherAlpha (S, Float, int) (función)</span><span class="sxs-lookup"><span data-stu-id="0c95c-105">Texture2DArray::GatherAlpha(S,float,int) function</span></span>

<span data-ttu-id="0c95c-106">Devuelve los componentes alfa de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="0c95c-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c95c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c95c-107">Syntax</span></span>

``` syntax
TemplateType GatherAlpha(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="0c95c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c95c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c95c-109">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="0c95c-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c95c-110">Tipo: **muestra**</span><span class="sxs-lookup"><span data-stu-id="0c95c-110">Type: **sampler**</span></span>

<span data-ttu-id="0c95c-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="0c95c-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="0c95c-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0c95c-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c95c-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="0c95c-113">Type: **float3**</span></span>

<span data-ttu-id="0c95c-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="0c95c-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="0c95c-115">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c95c-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c95c-116">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="0c95c-116">Type: **int2**</span></span>

<span data-ttu-id="0c95c-117">Desplazamiento que se aplica a la coordenada de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="0c95c-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c95c-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c95c-118">Return value</span></span>

<span data-ttu-id="0c95c-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="0c95c-119">Type: **TemplateType**</span></span>

<span data-ttu-id="0c95c-120">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="0c95c-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c95c-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c95c-121">Remarks</span></span>

<span data-ttu-id="0c95c-122">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="0c95c-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="0c95c-123">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="0c95c-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0c95c-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="0c95c-124">Vertex</span></span> | <span data-ttu-id="0c95c-125">Casco</span><span class="sxs-lookup"><span data-stu-id="0c95c-125">Hull</span></span> | <span data-ttu-id="0c95c-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="0c95c-126">Domain</span></span> | <span data-ttu-id="0c95c-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="0c95c-127">Geometry</span></span> | <span data-ttu-id="0c95c-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="0c95c-128">Pixel</span></span> | <span data-ttu-id="0c95c-129">Compute</span><span class="sxs-lookup"><span data-stu-id="0c95c-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0c95c-130">x</span><span class="sxs-lookup"><span data-stu-id="0c95c-130">x</span></span>      | <span data-ttu-id="0c95c-131">x</span><span class="sxs-lookup"><span data-stu-id="0c95c-131">x</span></span>    | <span data-ttu-id="0c95c-132">x</span><span class="sxs-lookup"><span data-stu-id="0c95c-132">x</span></span>      | <span data-ttu-id="0c95c-133">x</span><span class="sxs-lookup"><span data-stu-id="0c95c-133">x</span></span>        | <span data-ttu-id="0c95c-134">x</span><span class="sxs-lookup"><span data-stu-id="0c95c-134">x</span></span>     | <span data-ttu-id="0c95c-135">x</span><span class="sxs-lookup"><span data-stu-id="0c95c-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0c95c-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c95c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c95c-137">Métodos GatherAlpha</span><span class="sxs-lookup"><span data-stu-id="0c95c-137">GatherAlpha methods</span></span>](texture2darray-gatheralpha.md)
</dt> <dt>

[<span data-ttu-id="0c95c-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0c95c-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




