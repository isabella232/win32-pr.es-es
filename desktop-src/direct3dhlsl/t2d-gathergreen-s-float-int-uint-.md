---
title: 'Texture2D:: GatherGreen (S, Float, int, uint) (función)'
description: 'Devuelve los componentes verdes de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, junto con el estado de asignación de mosaicos. | Texture2D:: GatherGreen (S, Float, int, uint) (función)'
ms.assetid: A50C41BC-FDF4-47E6-9776-F51B2B634713
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
ms.openlocfilehash: 4c9bb997f822e1d0b0ffd482680bf7a57dffee7d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986415"
---
# <a name="texture2dgathergreensfloatintuint-function"></a><span data-ttu-id="2853d-105">Texture2D:: GatherGreen (S, Float, int, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="2853d-105">Texture2D::GatherGreen(S,float,int,uint) function</span></span>

<span data-ttu-id="2853d-106">Devuelve los componentes verdes de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, junto con el estado de asignación de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="2853d-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="2853d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2853d-107">Syntax</span></span>


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="2853d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2853d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2853d-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2853d-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2853d-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="2853d-110">Type: **SamplerState**</span></span>

<span data-ttu-id="2853d-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="2853d-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="2853d-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2853d-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2853d-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2853d-113">Type: **float**</span></span>

<span data-ttu-id="2853d-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="2853d-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="2853d-115">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2853d-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2853d-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="2853d-116">Type: **int**</span></span>

<span data-ttu-id="2853d-117">Desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="2853d-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2853d-118">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2853d-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2853d-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2853d-119">Type: **uint**</span></span>

<span data-ttu-id="2853d-120">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="2853d-120">The status of the operation.</span></span> <span data-ttu-id="2853d-121">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="2853d-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="2853d-122">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="2853d-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="2853d-123">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="2853d-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2853d-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2853d-124">Return value</span></span>

<span data-ttu-id="2853d-125">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="2853d-125">Type: **TemplateType**</span></span>

<span data-ttu-id="2853d-126">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="2853d-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="2853d-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2853d-127">Remarks</span></span>

<span data-ttu-id="2853d-128">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="2853d-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="2853d-129">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2853d-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2853d-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="2853d-130">Vertex</span></span> | <span data-ttu-id="2853d-131">Casco</span><span class="sxs-lookup"><span data-stu-id="2853d-131">Hull</span></span> | <span data-ttu-id="2853d-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="2853d-132">Domain</span></span> | <span data-ttu-id="2853d-133">Geometría</span><span class="sxs-lookup"><span data-stu-id="2853d-133">Geometry</span></span> | <span data-ttu-id="2853d-134">Píxel</span><span class="sxs-lookup"><span data-stu-id="2853d-134">Pixel</span></span> | <span data-ttu-id="2853d-135">Compute</span><span class="sxs-lookup"><span data-stu-id="2853d-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2853d-136">x</span><span class="sxs-lookup"><span data-stu-id="2853d-136">x</span></span>      | <span data-ttu-id="2853d-137">x</span><span class="sxs-lookup"><span data-stu-id="2853d-137">x</span></span>    | <span data-ttu-id="2853d-138">x</span><span class="sxs-lookup"><span data-stu-id="2853d-138">x</span></span>      | <span data-ttu-id="2853d-139">x</span><span class="sxs-lookup"><span data-stu-id="2853d-139">x</span></span>        | <span data-ttu-id="2853d-140">x</span><span class="sxs-lookup"><span data-stu-id="2853d-140">x</span></span>     | <span data-ttu-id="2853d-141">x</span><span class="sxs-lookup"><span data-stu-id="2853d-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2853d-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="2853d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2853d-143">Métodos GatherGreen</span><span class="sxs-lookup"><span data-stu-id="2853d-143">GatherGreen methods</span></span>](texture2d-gathergreen.md)
</dt> </dl>

 

 
