---
title: 'Texture2DArray:: GatherCmpBlue (S, Float, Float, int, uint) (función)'
description: 'En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación junto con el estado de asignación de mosaicos. | Texture2DArray:: GatherCmpBlue (S, Float, Float, int, uint) (función)'
ms.assetid: 60456C17-F7A4-408A-93A2-DF695CBBEEAA
keywords:
- GatherCmpBlue de función HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5bb2d292f63575d6a570296556dbc0622e6672b8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003667"
---
# <a name="texture2darraygathercmpbluesfloatfloatintuint-function"></a><span data-ttu-id="fbcf7-105">Texture2DArray:: GatherCmpBlue (S, Float, Float, int, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="fbcf7-105">Texture2DArray::GatherCmpBlue(S,float,float,int,uint) function</span></span>

<span data-ttu-id="fbcf7-106">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación junto con el estado de asignación de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="fbcf7-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbcf7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fbcf7-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpBlue(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="fbcf7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbcf7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbcf7-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="fbcf7-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbcf7-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="fbcf7-110">Type: **SamplerState**</span></span>

<span data-ttu-id="fbcf7-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="fbcf7-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="fbcf7-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fbcf7-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbcf7-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fbcf7-113">Type: **float**</span></span>

<span data-ttu-id="fbcf7-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="fbcf7-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="fbcf7-115">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fbcf7-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbcf7-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fbcf7-116">Type: **float**</span></span>

<span data-ttu-id="fbcf7-117">Valor que se va a comparar cada uno con cada valor muestreado.</span><span class="sxs-lookup"><span data-stu-id="fbcf7-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="fbcf7-118">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fbcf7-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbcf7-119">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="fbcf7-119">Type: **int**</span></span>

<span data-ttu-id="fbcf7-120">Desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="fbcf7-120">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fbcf7-121">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fbcf7-121">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbcf7-122">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="fbcf7-122">Type: **uint**</span></span>

<span data-ttu-id="fbcf7-123">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fbcf7-123">The status of the operation.</span></span> <span data-ttu-id="fbcf7-124">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="fbcf7-124">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="fbcf7-125">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="fbcf7-125">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="fbcf7-126">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="fbcf7-126">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbcf7-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fbcf7-127">Return value</span></span>

<span data-ttu-id="fbcf7-128">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="fbcf7-128">Type: **TemplateType**</span></span>

<span data-ttu-id="fbcf7-129">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="fbcf7-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbcf7-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fbcf7-130">Remarks</span></span>

<span data-ttu-id="fbcf7-131">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="fbcf7-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="fbcf7-132">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="fbcf7-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fbcf7-133">Vértice</span><span class="sxs-lookup"><span data-stu-id="fbcf7-133">Vertex</span></span> | <span data-ttu-id="fbcf7-134">Casco</span><span class="sxs-lookup"><span data-stu-id="fbcf7-134">Hull</span></span> | <span data-ttu-id="fbcf7-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="fbcf7-135">Domain</span></span> | <span data-ttu-id="fbcf7-136">Geometría</span><span class="sxs-lookup"><span data-stu-id="fbcf7-136">Geometry</span></span> | <span data-ttu-id="fbcf7-137">Píxel</span><span class="sxs-lookup"><span data-stu-id="fbcf7-137">Pixel</span></span> | <span data-ttu-id="fbcf7-138">Compute</span><span class="sxs-lookup"><span data-stu-id="fbcf7-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fbcf7-139">x</span><span class="sxs-lookup"><span data-stu-id="fbcf7-139">x</span></span>      | <span data-ttu-id="fbcf7-140">x</span><span class="sxs-lookup"><span data-stu-id="fbcf7-140">x</span></span>    | <span data-ttu-id="fbcf7-141">x</span><span class="sxs-lookup"><span data-stu-id="fbcf7-141">x</span></span>      | <span data-ttu-id="fbcf7-142">x</span><span class="sxs-lookup"><span data-stu-id="fbcf7-142">x</span></span>        | <span data-ttu-id="fbcf7-143">x</span><span class="sxs-lookup"><span data-stu-id="fbcf7-143">x</span></span>     | <span data-ttu-id="fbcf7-144">x</span><span class="sxs-lookup"><span data-stu-id="fbcf7-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fbcf7-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbcf7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbcf7-146">Métodos GatherCmpBlue</span><span class="sxs-lookup"><span data-stu-id="fbcf7-146">GatherCmpBlue methods</span></span>](texture2darray-gathercmpblue.md)
</dt> </dl>

 

 
