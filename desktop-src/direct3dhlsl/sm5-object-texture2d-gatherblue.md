---
title: 'Texture2D:: GatherBlue (S, Float, int) (función)'
description: 'Devuelve los componentes azules de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal. | Texture2D:: GatherBlue (S, Float, int) (función)'
ms.assetid: 6d753ef2-2818-4990-81df-52dda044d21d
keywords:
- GatherBlue de función HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54885ccd8f31fdf55270b6c9ac2dbafa1805d866
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986418"
---
# <a name="texture2dgatherbluesfloatint-function"></a><span data-ttu-id="d5d33-105">Texture2D:: GatherBlue (S, Float, int) (función)</span><span class="sxs-lookup"><span data-stu-id="d5d33-105">Texture2D::GatherBlue(S,float,int) function</span></span>

<span data-ttu-id="d5d33-106">Devuelve los componentes azules de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="d5d33-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d33-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5d33-107">Syntax</span></span>

``` syntax
TemplateType GatherBlue(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="d5d33-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5d33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5d33-109">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d5d33-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d33-110">Tipo: **muestra**</span><span class="sxs-lookup"><span data-stu-id="d5d33-110">Type: **sampler**</span></span>

<span data-ttu-id="d5d33-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="d5d33-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="d5d33-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d5d33-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d33-113">Tipo: **float2**</span><span class="sxs-lookup"><span data-stu-id="d5d33-113">Type: **float2**</span></span>

<span data-ttu-id="d5d33-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="d5d33-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="d5d33-115">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5d33-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d33-116">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="d5d33-116">Type: **int2**</span></span>

<span data-ttu-id="d5d33-117">Desplazamiento que se aplica a la coordenada de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="d5d33-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5d33-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5d33-118">Return value</span></span>

<span data-ttu-id="d5d33-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="d5d33-119">Type: **TemplateType**</span></span>

<span data-ttu-id="d5d33-120">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="d5d33-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5d33-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5d33-121">Remarks</span></span>

<span data-ttu-id="d5d33-122">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="d5d33-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="d5d33-123">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="d5d33-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d5d33-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="d5d33-124">Vertex</span></span> | <span data-ttu-id="d5d33-125">Casco</span><span class="sxs-lookup"><span data-stu-id="d5d33-125">Hull</span></span> | <span data-ttu-id="d5d33-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="d5d33-126">Domain</span></span> | <span data-ttu-id="d5d33-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="d5d33-127">Geometry</span></span> | <span data-ttu-id="d5d33-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="d5d33-128">Pixel</span></span> | <span data-ttu-id="d5d33-129">Compute</span><span class="sxs-lookup"><span data-stu-id="d5d33-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d5d33-130">x</span><span class="sxs-lookup"><span data-stu-id="d5d33-130">x</span></span>      | <span data-ttu-id="d5d33-131">x</span><span class="sxs-lookup"><span data-stu-id="d5d33-131">x</span></span>    | <span data-ttu-id="d5d33-132">x</span><span class="sxs-lookup"><span data-stu-id="d5d33-132">x</span></span>      | <span data-ttu-id="d5d33-133">x</span><span class="sxs-lookup"><span data-stu-id="d5d33-133">x</span></span>        | <span data-ttu-id="d5d33-134">x</span><span class="sxs-lookup"><span data-stu-id="d5d33-134">x</span></span>     | <span data-ttu-id="d5d33-135">x</span><span class="sxs-lookup"><span data-stu-id="d5d33-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d5d33-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5d33-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d33-137">Métodos GatherBlue</span><span class="sxs-lookup"><span data-stu-id="d5d33-137">GatherBlue methods</span></span>](texture2d-gatherblue.md)
</dt> <dt>

[<span data-ttu-id="d5d33-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d5d33-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




