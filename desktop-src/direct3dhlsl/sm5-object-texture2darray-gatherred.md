---
title: 'Texture2DArray:: GatherRed (S, Float, int) (función)'
description: 'Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal. | Texture2DArray:: GatherRed (S, Float, int) (función)'
ms.assetid: cb9c21ef-87f4-4c32-b41a-9fc7478713a6
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
ms.openlocfilehash: 431d08b77d13540bb48621a6d5ec76f4c775f796
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998141"
---
# <a name="texture2darraygatherredsfloatint-function"></a><span data-ttu-id="de1bb-105">Texture2DArray:: GatherRed (S, Float, int) (función)</span><span class="sxs-lookup"><span data-stu-id="de1bb-105">Texture2DArray::GatherRed(S,float,int) function</span></span>

<span data-ttu-id="de1bb-106">Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="de1bb-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="de1bb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de1bb-107">Syntax</span></span>

``` syntax
TemplateType GatherRed(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="de1bb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de1bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de1bb-109">*s* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="de1bb-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de1bb-110">Tipo: **muestra**</span><span class="sxs-lookup"><span data-stu-id="de1bb-110">Type: **sampler**</span></span>

<span data-ttu-id="de1bb-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="de1bb-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="de1bb-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="de1bb-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de1bb-113">Tipo: **float3**</span><span class="sxs-lookup"><span data-stu-id="de1bb-113">Type: **float3**</span></span>

<span data-ttu-id="de1bb-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="de1bb-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="de1bb-115">*desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="de1bb-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de1bb-116">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="de1bb-116">Type: **int2**</span></span>

<span data-ttu-id="de1bb-117">Desplazamiento que se aplica a la coordenada de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="de1bb-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de1bb-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de1bb-118">Return value</span></span>

<span data-ttu-id="de1bb-119">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="de1bb-119">Type: **TemplateType**</span></span>

<span data-ttu-id="de1bb-120">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="de1bb-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="de1bb-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de1bb-121">Remarks</span></span>

<span data-ttu-id="de1bb-122">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="de1bb-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="de1bb-123">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="de1bb-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="de1bb-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="de1bb-124">Vertex</span></span> | <span data-ttu-id="de1bb-125">Casco</span><span class="sxs-lookup"><span data-stu-id="de1bb-125">Hull</span></span> | <span data-ttu-id="de1bb-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="de1bb-126">Domain</span></span> | <span data-ttu-id="de1bb-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="de1bb-127">Geometry</span></span> | <span data-ttu-id="de1bb-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="de1bb-128">Pixel</span></span> | <span data-ttu-id="de1bb-129">Compute</span><span class="sxs-lookup"><span data-stu-id="de1bb-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="de1bb-130">x</span><span class="sxs-lookup"><span data-stu-id="de1bb-130">x</span></span>      | <span data-ttu-id="de1bb-131">x</span><span class="sxs-lookup"><span data-stu-id="de1bb-131">x</span></span>    | <span data-ttu-id="de1bb-132">x</span><span class="sxs-lookup"><span data-stu-id="de1bb-132">x</span></span>      | <span data-ttu-id="de1bb-133">x</span><span class="sxs-lookup"><span data-stu-id="de1bb-133">x</span></span>        | <span data-ttu-id="de1bb-134">x</span><span class="sxs-lookup"><span data-stu-id="de1bb-134">x</span></span>     | <span data-ttu-id="de1bb-135">x</span><span class="sxs-lookup"><span data-stu-id="de1bb-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="de1bb-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="de1bb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de1bb-137">Métodos GatherRed</span><span class="sxs-lookup"><span data-stu-id="de1bb-137">GatherRed methods</span></span>](texture2darray-gatherred.md)
</dt> <dt>

[<span data-ttu-id="de1bb-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="de1bb-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




