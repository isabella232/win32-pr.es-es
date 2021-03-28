---
title: 'TextureCubeArray:: GatherCmpAlpha (S, Float, Float, uint) (función)'
description: 'En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con un valor de comparación junto con el estado de asignación de mosaicos. | TextureCubeArray:: GatherCmpAlpha (S, Float, Float, uint) (función)'
ms.assetid: EA1D7176-3F70-4867-9854-80206A871B23
keywords:
- GatherCmpAlpha de función HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 198179b67a2812417e60a0a1e1512b686d52e98a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998177"
---
# <a name="texturecubearraygathercmpalphasfloatfloatuint-function"></a><span data-ttu-id="cd32c-105">TextureCubeArray:: GatherCmpAlpha (S, Float, Float, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="cd32c-105">TextureCubeArray::GatherCmpAlpha(S,float,float,uint) function</span></span>

<span data-ttu-id="cd32c-106">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con un valor de comparación junto con el estado de asignación de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="cd32c-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd32c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd32c-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpAlpha(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="cd32c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd32c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd32c-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="cd32c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd32c-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="cd32c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="cd32c-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="cd32c-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="cd32c-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="cd32c-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd32c-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="cd32c-113">Type: **float**</span></span>

<span data-ttu-id="cd32c-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="cd32c-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="cd32c-115">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd32c-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd32c-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="cd32c-116">Type: **float**</span></span>

<span data-ttu-id="cd32c-117">Valor que se va a comparar cada uno con cada valor muestreado.</span><span class="sxs-lookup"><span data-stu-id="cd32c-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="cd32c-118">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cd32c-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd32c-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="cd32c-119">Type: **uint**</span></span>

<span data-ttu-id="cd32c-120">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="cd32c-120">The status of the operation.</span></span> <span data-ttu-id="cd32c-121">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="cd32c-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="cd32c-122">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="cd32c-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="cd32c-123">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="cd32c-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd32c-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd32c-124">Return value</span></span>

<span data-ttu-id="cd32c-125">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="cd32c-125">Type: **TemplateType**</span></span>

<span data-ttu-id="cd32c-126">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="cd32c-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd32c-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd32c-127">Remarks</span></span>

<span data-ttu-id="cd32c-128">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="cd32c-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="cd32c-129">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="cd32c-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="cd32c-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="cd32c-130">Vertex</span></span> | <span data-ttu-id="cd32c-131">Casco</span><span class="sxs-lookup"><span data-stu-id="cd32c-131">Hull</span></span> | <span data-ttu-id="cd32c-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="cd32c-132">Domain</span></span> | <span data-ttu-id="cd32c-133">Geometría</span><span class="sxs-lookup"><span data-stu-id="cd32c-133">Geometry</span></span> | <span data-ttu-id="cd32c-134">Píxel</span><span class="sxs-lookup"><span data-stu-id="cd32c-134">Pixel</span></span> | <span data-ttu-id="cd32c-135">Compute</span><span class="sxs-lookup"><span data-stu-id="cd32c-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cd32c-136">x</span><span class="sxs-lookup"><span data-stu-id="cd32c-136">x</span></span>      | <span data-ttu-id="cd32c-137">x</span><span class="sxs-lookup"><span data-stu-id="cd32c-137">x</span></span>    | <span data-ttu-id="cd32c-138">x</span><span class="sxs-lookup"><span data-stu-id="cd32c-138">x</span></span>      | <span data-ttu-id="cd32c-139">x</span><span class="sxs-lookup"><span data-stu-id="cd32c-139">x</span></span>        | <span data-ttu-id="cd32c-140">x</span><span class="sxs-lookup"><span data-stu-id="cd32c-140">x</span></span>     | <span data-ttu-id="cd32c-141">x</span><span class="sxs-lookup"><span data-stu-id="cd32c-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cd32c-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd32c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd32c-143">Métodos GatherCmpAlpha</span><span class="sxs-lookup"><span data-stu-id="cd32c-143">GatherCmpAlpha methods</span></span>](texturecubearray-gathercmpalpha.md)
</dt> <dt>

[<span data-ttu-id="cd32c-144">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="cd32c-144">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
