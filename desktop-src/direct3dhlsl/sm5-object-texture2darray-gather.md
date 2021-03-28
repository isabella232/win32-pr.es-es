---
title: 'Texture2DArray:: Gather (S, Float, int) (función)'
description: 'Devuelve los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal. | Texture2DArray:: Gather (S, Float, int) (función)'
ms.assetid: b0355158-01c8-45a1-bb5d-29a8c43b1685
keywords:
- Recopilación de la función HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46866df18a0836b311443a3dd411d74dfa7fb126
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998032"
---
# <a name="texture2darraygathersfloatint-function"></a><span data-ttu-id="46c92-105">Texture2DArray:: Gather (S, Float, int) (función)</span><span class="sxs-lookup"><span data-stu-id="46c92-105">Texture2DArray::Gather(S,float,int) function</span></span>

<span data-ttu-id="46c92-106">Devuelve los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="46c92-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="46c92-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46c92-107">Syntax</span></span>

``` syntax
TemplateType Gather(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="46c92-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46c92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46c92-109">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="46c92-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c92-110">Tipo: **muestra**</span><span class="sxs-lookup"><span data-stu-id="46c92-110">Type: **sampler**</span></span>

<span data-ttu-id="46c92-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="46c92-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="46c92-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="46c92-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c92-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="46c92-113">Type: **float3**</span></span>

<span data-ttu-id="46c92-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="46c92-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="46c92-115">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46c92-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c92-116">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="46c92-116">Type: **int2**</span></span>

<span data-ttu-id="46c92-117">Desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="46c92-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46c92-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46c92-118">Return value</span></span>

<span data-ttu-id="46c92-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="46c92-119">Type: **TemplateType**</span></span>

<span data-ttu-id="46c92-120">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="46c92-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="46c92-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46c92-121">Remarks</span></span>

<span data-ttu-id="46c92-122">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="46c92-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="46c92-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="46c92-123">Vertex</span></span> | <span data-ttu-id="46c92-124">Casco</span><span class="sxs-lookup"><span data-stu-id="46c92-124">Hull</span></span> | <span data-ttu-id="46c92-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="46c92-125">Domain</span></span> | <span data-ttu-id="46c92-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="46c92-126">Geometry</span></span> | <span data-ttu-id="46c92-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="46c92-127">Pixel</span></span> | <span data-ttu-id="46c92-128">Compute</span><span class="sxs-lookup"><span data-stu-id="46c92-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="46c92-129">x</span><span class="sxs-lookup"><span data-stu-id="46c92-129">x</span></span>      | <span data-ttu-id="46c92-130">x</span><span class="sxs-lookup"><span data-stu-id="46c92-130">x</span></span>    | <span data-ttu-id="46c92-131">x</span><span class="sxs-lookup"><span data-stu-id="46c92-131">x</span></span>      | <span data-ttu-id="46c92-132">x</span><span class="sxs-lookup"><span data-stu-id="46c92-132">x</span></span>        | <span data-ttu-id="46c92-133">x</span><span class="sxs-lookup"><span data-stu-id="46c92-133">x</span></span>     | <span data-ttu-id="46c92-134">x</span><span class="sxs-lookup"><span data-stu-id="46c92-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="46c92-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="46c92-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46c92-136">Recopilar métodos</span><span class="sxs-lookup"><span data-stu-id="46c92-136">Gather methods</span></span>](texture2darray-gather.md)
</dt> <dt>

[<span data-ttu-id="46c92-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="46c92-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




