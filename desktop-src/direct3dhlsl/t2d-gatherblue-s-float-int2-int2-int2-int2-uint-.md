---
title: 'Texture2D:: GatherBlue (S, Float, INT2, INT2, INT2, INT2, uint) (función)'
description: 'Devuelve los componentes azules de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, junto con el estado de asignación de mosaicos. | Texture2D:: GatherBlue (S, Float, INT2, INT2, INT2, INT2, uint) (función)'
ms.assetid: 74B2DAEC-3A94-441D-8A9E-286C2D2E9C8E
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
ms.openlocfilehash: 60df5e94c348af95b81efc8f1b913ac6f7875a79
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362305"
---
# <a name="texture2dgatherbluesfloatint2int2int2int2uint-function"></a><span data-ttu-id="31993-105">Texture2D:: GatherBlue (S, Float, INT2, INT2, INT2, INT2, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="31993-105">Texture2D::GatherBlue(S,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="31993-106">Devuelve los componentes azules de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, junto con el estado de asignación de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="31993-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="31993-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31993-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="31993-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31993-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31993-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="31993-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31993-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="31993-110">Type: **SamplerState**</span></span>

<span data-ttu-id="31993-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="31993-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="31993-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="31993-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31993-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="31993-113">Type: **float**</span></span>

<span data-ttu-id="31993-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="31993-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="31993-115">*Offset1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31993-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31993-116">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="31993-116">Type: **int2**</span></span>

<span data-ttu-id="31993-117">Primer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="31993-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="31993-118">*Offset2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31993-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31993-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="31993-119">Type: **int2**</span></span>

<span data-ttu-id="31993-120">Segundo componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="31993-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="31993-121">*Offset3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31993-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31993-122">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="31993-122">Type: **int2**</span></span>

<span data-ttu-id="31993-123">Tercer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="31993-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="31993-124">*Offset4* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="31993-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31993-125">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="31993-125">Type: **int2**</span></span>

<span data-ttu-id="31993-126">Cuarto componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="31993-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="31993-127">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="31993-127">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31993-128">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="31993-128">Type: **uint**</span></span>

<span data-ttu-id="31993-129">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="31993-129">The status of the operation.</span></span> <span data-ttu-id="31993-130">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="31993-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="31993-131">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="31993-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="31993-132">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="31993-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31993-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31993-133">Return value</span></span>

<span data-ttu-id="31993-134">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="31993-134">Type: **TemplateType**</span></span>

<span data-ttu-id="31993-135">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="31993-135">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="31993-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31993-136">Remarks</span></span>

<span data-ttu-id="31993-137">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="31993-137">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="31993-138">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="31993-138">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="31993-139">Vértice</span><span class="sxs-lookup"><span data-stu-id="31993-139">Vertex</span></span> | <span data-ttu-id="31993-140">Casco</span><span class="sxs-lookup"><span data-stu-id="31993-140">Hull</span></span> | <span data-ttu-id="31993-141">Dominio</span><span class="sxs-lookup"><span data-stu-id="31993-141">Domain</span></span> | <span data-ttu-id="31993-142">Geometría</span><span class="sxs-lookup"><span data-stu-id="31993-142">Geometry</span></span> | <span data-ttu-id="31993-143">Píxel</span><span class="sxs-lookup"><span data-stu-id="31993-143">Pixel</span></span> | <span data-ttu-id="31993-144">Compute</span><span class="sxs-lookup"><span data-stu-id="31993-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="31993-145">x</span><span class="sxs-lookup"><span data-stu-id="31993-145">x</span></span>      | <span data-ttu-id="31993-146">x</span><span class="sxs-lookup"><span data-stu-id="31993-146">x</span></span>    | <span data-ttu-id="31993-147">x</span><span class="sxs-lookup"><span data-stu-id="31993-147">x</span></span>      | <span data-ttu-id="31993-148">x</span><span class="sxs-lookup"><span data-stu-id="31993-148">x</span></span>        | <span data-ttu-id="31993-149">x</span><span class="sxs-lookup"><span data-stu-id="31993-149">x</span></span>     | <span data-ttu-id="31993-150">x</span><span class="sxs-lookup"><span data-stu-id="31993-150">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="31993-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="31993-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31993-152">Métodos GatherBlue</span><span class="sxs-lookup"><span data-stu-id="31993-152">GatherBlue methods</span></span>](texture2d-gatherblue.md)
</dt> </dl>

 

 
