---
title: 'Texture2D:: GatherRed (S, Float, int) (función)'
description: 'Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente rojo con respecto a un valor de comparación. | Texture2D:: GatherRed (S, Float, int) (función)'
ms.assetid: 6d2d1556-d52f-4625-93ca-34da399f9a8b
keywords:
- GatherRed de función HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f05196063f6a17cc34865157c17a92bc2bb116bf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986514"
---
# <a name="texture2dgatherredsfloatint-function"></a><span data-ttu-id="c46b4-105">Texture2D:: GatherRed (S, Float, int) (función)</span><span class="sxs-lookup"><span data-stu-id="c46b4-105">Texture2D::GatherRed(S,float,int) function</span></span>

<span data-ttu-id="c46b4-106">Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente rojo con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="c46b4-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c46b4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c46b4-107">Syntax</span></span>

``` syntax
TemplateType GatherRed(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="c46b4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c46b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c46b4-109">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="c46b4-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c46b4-110">Tipo: **muestra**</span><span class="sxs-lookup"><span data-stu-id="c46b4-110">Type: **sampler**</span></span>

<span data-ttu-id="c46b4-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="c46b4-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="c46b4-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c46b4-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c46b4-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="c46b4-113">Type: **float2**</span></span>

<span data-ttu-id="c46b4-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="c46b4-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="c46b4-115">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c46b4-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c46b4-116">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="c46b4-116">Type: **int2**</span></span>

<span data-ttu-id="c46b4-117">Desplazamiento que se aplica a la coordenada de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="c46b4-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c46b4-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c46b4-118">Return value</span></span>

<span data-ttu-id="c46b4-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="c46b4-119">Type: **TemplateType**</span></span>

<span data-ttu-id="c46b4-120">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="c46b4-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c46b4-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c46b4-121">Remarks</span></span>

<span data-ttu-id="c46b4-122">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="c46b4-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="c46b4-123">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="c46b4-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c46b4-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="c46b4-124">Vertex</span></span> | <span data-ttu-id="c46b4-125">Casco</span><span class="sxs-lookup"><span data-stu-id="c46b4-125">Hull</span></span> | <span data-ttu-id="c46b4-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="c46b4-126">Domain</span></span> | <span data-ttu-id="c46b4-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="c46b4-127">Geometry</span></span> | <span data-ttu-id="c46b4-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="c46b4-128">Pixel</span></span> | <span data-ttu-id="c46b4-129">Compute</span><span class="sxs-lookup"><span data-stu-id="c46b4-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c46b4-130">x</span><span class="sxs-lookup"><span data-stu-id="c46b4-130">x</span></span>      | <span data-ttu-id="c46b4-131">x</span><span class="sxs-lookup"><span data-stu-id="c46b4-131">x</span></span>    | <span data-ttu-id="c46b4-132">x</span><span class="sxs-lookup"><span data-stu-id="c46b4-132">x</span></span>      | <span data-ttu-id="c46b4-133">x</span><span class="sxs-lookup"><span data-stu-id="c46b4-133">x</span></span>        | <span data-ttu-id="c46b4-134">x</span><span class="sxs-lookup"><span data-stu-id="c46b4-134">x</span></span>     | <span data-ttu-id="c46b4-135">x</span><span class="sxs-lookup"><span data-stu-id="c46b4-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c46b4-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="c46b4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c46b4-137">Métodos GatherRed</span><span class="sxs-lookup"><span data-stu-id="c46b4-137">GatherRed methods</span></span>](texture2d-gatherred.md)
</dt> <dt>

[<span data-ttu-id="c46b4-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c46b4-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




