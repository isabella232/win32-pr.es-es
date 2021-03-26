---
title: 'Texture2DArray:: GatherBlue (S, Float, int) (función)'
description: 'Devuelve los componentes azules de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal. | Texture2DArray:: GatherBlue (S, Float, int) (función)'
ms.assetid: f81596b5-afd1-4baf-b6c0-ca4661a3ef22
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
ms.openlocfilehash: 1844b898deca767b04aba438f4784a54a5afa112
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998072"
---
# <a name="texture2darraygatherbluesfloatint-function"></a><span data-ttu-id="6b4c9-105">Texture2DArray:: GatherBlue (S, Float, int) (función)</span><span class="sxs-lookup"><span data-stu-id="6b4c9-105">Texture2DArray::GatherBlue(S,float,int) function</span></span>

<span data-ttu-id="6b4c9-106">Devuelve los componentes azules de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="6b4c9-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b4c9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b4c9-107">Syntax</span></span>

``` syntax
TemplateType GatherBlue(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="6b4c9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b4c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b4c9-109">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="6b4c9-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b4c9-110">Tipo: **muestra**</span><span class="sxs-lookup"><span data-stu-id="6b4c9-110">Type: **sampler**</span></span>

<span data-ttu-id="6b4c9-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="6b4c9-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="6b4c9-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6b4c9-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b4c9-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="6b4c9-113">Type: **float3**</span></span>

<span data-ttu-id="6b4c9-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="6b4c9-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="6b4c9-115">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6b4c9-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b4c9-116">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="6b4c9-116">Type: **int2**</span></span>

<span data-ttu-id="6b4c9-117">Desplazamiento que se aplica a la coordenada de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="6b4c9-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b4c9-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b4c9-118">Return value</span></span>

<span data-ttu-id="6b4c9-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="6b4c9-119">Type: **TemplateType**</span></span>

<span data-ttu-id="6b4c9-120">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="6b4c9-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b4c9-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b4c9-121">Remarks</span></span>

<span data-ttu-id="6b4c9-122">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="6b4c9-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="6b4c9-123">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="6b4c9-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6b4c9-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="6b4c9-124">Vertex</span></span> | <span data-ttu-id="6b4c9-125">Casco</span><span class="sxs-lookup"><span data-stu-id="6b4c9-125">Hull</span></span> | <span data-ttu-id="6b4c9-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="6b4c9-126">Domain</span></span> | <span data-ttu-id="6b4c9-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="6b4c9-127">Geometry</span></span> | <span data-ttu-id="6b4c9-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="6b4c9-128">Pixel</span></span> | <span data-ttu-id="6b4c9-129">Compute</span><span class="sxs-lookup"><span data-stu-id="6b4c9-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6b4c9-130">x</span><span class="sxs-lookup"><span data-stu-id="6b4c9-130">x</span></span>      | <span data-ttu-id="6b4c9-131">x</span><span class="sxs-lookup"><span data-stu-id="6b4c9-131">x</span></span>    | <span data-ttu-id="6b4c9-132">x</span><span class="sxs-lookup"><span data-stu-id="6b4c9-132">x</span></span>      | <span data-ttu-id="6b4c9-133">x</span><span class="sxs-lookup"><span data-stu-id="6b4c9-133">x</span></span>        | <span data-ttu-id="6b4c9-134">x</span><span class="sxs-lookup"><span data-stu-id="6b4c9-134">x</span></span>     | <span data-ttu-id="6b4c9-135">x</span><span class="sxs-lookup"><span data-stu-id="6b4c9-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6b4c9-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b4c9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b4c9-137">Métodos GatherBlue</span><span class="sxs-lookup"><span data-stu-id="6b4c9-137">GatherBlue methods</span></span>](texture2darray-gatherblue.md)
</dt> <dt>

[<span data-ttu-id="6b4c9-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6b4c9-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




