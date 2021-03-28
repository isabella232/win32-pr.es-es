---
title: 'Texture2DArray:: GatherGreen (S, Float, int) (función)'
description: 'Devuelve los componentes verdes de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal. | Texture2DArray:: GatherGreen (S, Float, int) (función)'
ms.assetid: bfe9ab9f-64f7-4a50-aa46-2ec6effebce2
keywords:
- GatherGreen de función HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 48a5d968ffe5eeb12fdb0240d1823a9b1834ae19
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279940"
---
# <a name="texture2darraygathergreensfloatint-function"></a><span data-ttu-id="67ca0-105">Texture2DArray:: GatherGreen (S, Float, int) (función)</span><span class="sxs-lookup"><span data-stu-id="67ca0-105">Texture2DArray::GatherGreen(S,float,int) function</span></span>

<span data-ttu-id="67ca0-106">Devuelve los componentes verdes de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="67ca0-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ca0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67ca0-107">Syntax</span></span>

``` syntax
TemplateType GatherGreen(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="67ca0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67ca0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67ca0-109">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="67ca0-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67ca0-110">Tipo: **muestra**</span><span class="sxs-lookup"><span data-stu-id="67ca0-110">Type: **sampler**</span></span>

<span data-ttu-id="67ca0-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="67ca0-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="67ca0-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="67ca0-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67ca0-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="67ca0-113">Type: **float3**</span></span>

<span data-ttu-id="67ca0-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="67ca0-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="67ca0-115">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="67ca0-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67ca0-116">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="67ca0-116">Type: **int2**</span></span>

<span data-ttu-id="67ca0-117">Desplazamiento que se aplica a la coordenada de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="67ca0-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67ca0-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67ca0-118">Return value</span></span>

<span data-ttu-id="67ca0-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="67ca0-119">Type: **TemplateType**</span></span>

<span data-ttu-id="67ca0-120">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="67ca0-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="67ca0-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67ca0-121">Remarks</span></span>

<span data-ttu-id="67ca0-122">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="67ca0-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="67ca0-123">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="67ca0-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="67ca0-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="67ca0-124">Vertex</span></span> | <span data-ttu-id="67ca0-125">Casco</span><span class="sxs-lookup"><span data-stu-id="67ca0-125">Hull</span></span> | <span data-ttu-id="67ca0-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="67ca0-126">Domain</span></span> | <span data-ttu-id="67ca0-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="67ca0-127">Geometry</span></span> | <span data-ttu-id="67ca0-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="67ca0-128">Pixel</span></span> | <span data-ttu-id="67ca0-129">Compute</span><span class="sxs-lookup"><span data-stu-id="67ca0-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="67ca0-130">x</span><span class="sxs-lookup"><span data-stu-id="67ca0-130">x</span></span>      | <span data-ttu-id="67ca0-131">x</span><span class="sxs-lookup"><span data-stu-id="67ca0-131">x</span></span>    | <span data-ttu-id="67ca0-132">x</span><span class="sxs-lookup"><span data-stu-id="67ca0-132">x</span></span>      | <span data-ttu-id="67ca0-133">x</span><span class="sxs-lookup"><span data-stu-id="67ca0-133">x</span></span>        | <span data-ttu-id="67ca0-134">x</span><span class="sxs-lookup"><span data-stu-id="67ca0-134">x</span></span>     | <span data-ttu-id="67ca0-135">x</span><span class="sxs-lookup"><span data-stu-id="67ca0-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="67ca0-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="67ca0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ca0-137">Métodos GatherGreen</span><span class="sxs-lookup"><span data-stu-id="67ca0-137">GatherGreen methods</span></span>](texture2darray-gathergreen.md)
</dt> <dt>

[<span data-ttu-id="67ca0-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="67ca0-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




