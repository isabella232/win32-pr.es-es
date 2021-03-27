---
title: 'Texture2D:: GatherCmp (S, Float, Float, int, uint) (función)'
description: 'Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve su comparación con un valor de comparación junto con el estado de asignación de mosaicos. | Texture2D:: GatherCmp (S, Float, Float, int, uint) (función)'
ms.assetid: A6610587-97C3-4CE5-86A7-3411D422BC8F
keywords:
- GatherCmp de función HLSL
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be8246053e0f7ba6357bdd68dc59059fd225bbc8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986595"
---
# <a name="texture2dgathercmpsfloatfloatintuint-function"></a><span data-ttu-id="b21b4-105">Texture2D:: GatherCmp (S, Float, Float, int, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="b21b4-105">Texture2D::GatherCmp(S,float,float,int,uint) function</span></span>

<span data-ttu-id="b21b4-106">Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve su comparación con un valor de comparación junto con el estado de asignación de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="b21b4-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="b21b4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b21b4-107">Syntax</span></span>


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="b21b4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b21b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b21b4-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b21b4-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b21b4-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="b21b4-110">Type: **SamplerState**</span></span>

<span data-ttu-id="b21b4-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="b21b4-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="b21b4-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b21b4-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b21b4-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b21b4-113">Type: **float**</span></span>

<span data-ttu-id="b21b4-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="b21b4-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="b21b4-115">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b21b4-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b21b4-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="b21b4-116">Type: **float**</span></span>

<span data-ttu-id="b21b4-117">Valor que se va a comparar cada uno con cada valor muestreado.</span><span class="sxs-lookup"><span data-stu-id="b21b4-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="b21b4-118">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b21b4-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b21b4-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="b21b4-119">Type: **int2**</span></span>

<span data-ttu-id="b21b4-120">Desplazamiento en textura aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="b21b4-120">The offset in texels applied to the texture coordinates before sampling.</span></span> <span data-ttu-id="b21b4-121">Debe ser un valor literal.</span><span class="sxs-lookup"><span data-stu-id="b21b4-121">Must be a literal value.</span></span>

</dd> <dt>

<span data-ttu-id="b21b4-122">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b21b4-122">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b21b4-123">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b21b4-123">Type: **uint**</span></span>

<span data-ttu-id="b21b4-124">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="b21b4-124">The status of the operation.</span></span> <span data-ttu-id="b21b4-125">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="b21b4-125">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b21b4-126">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="b21b4-126">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b21b4-127">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="b21b4-127">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b21b4-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b21b4-128">Return value</span></span>

<span data-ttu-id="b21b4-129">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="b21b4-129">Type: **TemplateType**</span></span>

<span data-ttu-id="b21b4-130">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="b21b4-130">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="b21b4-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b21b4-131">Remarks</span></span>

<span data-ttu-id="b21b4-132">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="b21b4-132">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="b21b4-133">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b21b4-133">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b21b4-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="b21b4-134">Vertex</span></span> | <span data-ttu-id="b21b4-135">Casco</span><span class="sxs-lookup"><span data-stu-id="b21b4-135">Hull</span></span> | <span data-ttu-id="b21b4-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="b21b4-136">Domain</span></span> | <span data-ttu-id="b21b4-137">Geometría</span><span class="sxs-lookup"><span data-stu-id="b21b4-137">Geometry</span></span> | <span data-ttu-id="b21b4-138">Píxel</span><span class="sxs-lookup"><span data-stu-id="b21b4-138">Pixel</span></span> | <span data-ttu-id="b21b4-139">Compute</span><span class="sxs-lookup"><span data-stu-id="b21b4-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b21b4-140">x</span><span class="sxs-lookup"><span data-stu-id="b21b4-140">x</span></span>      | <span data-ttu-id="b21b4-141">x</span><span class="sxs-lookup"><span data-stu-id="b21b4-141">x</span></span>    | <span data-ttu-id="b21b4-142">x</span><span class="sxs-lookup"><span data-stu-id="b21b4-142">x</span></span>      | <span data-ttu-id="b21b4-143">x</span><span class="sxs-lookup"><span data-stu-id="b21b4-143">x</span></span>        | <span data-ttu-id="b21b4-144">x</span><span class="sxs-lookup"><span data-stu-id="b21b4-144">x</span></span>     | <span data-ttu-id="b21b4-145">x</span><span class="sxs-lookup"><span data-stu-id="b21b4-145">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b21b4-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="b21b4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b21b4-147">Métodos GatherCmp</span><span class="sxs-lookup"><span data-stu-id="b21b4-147">GatherCmp methods</span></span>](texture2d-gathercmp.md)
</dt> </dl>

 

 
