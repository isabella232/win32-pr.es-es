---
title: 'Texture2DArray:: GatherRed (S, Float, INT2, INT2, INT2, INT2, uint) (función)'
description: 'Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, junto con el estado de asignación de mosaicos. | Texture2DArray:: GatherRed (S, Float, INT2, INT2, INT2, INT2, uint) (función)'
ms.assetid: 9DD399A4-E6ED-499B-ACA3-28028C0AB271
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
ms.openlocfilehash: 8ce2ce0ab8b79a2335cc8e02d89751da3b30d856
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998069"
---
# <a name="texture2darraygatherredsfloatint2int2int2int2uint-function"></a><span data-ttu-id="2d100-105">Texture2DArray:: GatherRed (S, Float, INT2, INT2, INT2, INT2, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="2d100-105">Texture2DArray::GatherRed(S,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="2d100-106">Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, junto con el estado de asignación de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="2d100-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d100-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d100-107">Syntax</span></span>


``` syntax
TemplateType GatherRed(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="2d100-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d100-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d100-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="2d100-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d100-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="2d100-110">Type: **SamplerState**</span></span>

<span data-ttu-id="2d100-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="2d100-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="2d100-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2d100-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d100-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="2d100-113">Type: **float**</span></span>

<span data-ttu-id="2d100-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="2d100-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="2d100-115">*Offset1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d100-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d100-116">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="2d100-116">Type: **int2**</span></span>

<span data-ttu-id="2d100-117">Primer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="2d100-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2d100-118">*Offset2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d100-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d100-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="2d100-119">Type: **int2**</span></span>

<span data-ttu-id="2d100-120">Segundo componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="2d100-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2d100-121">*Offset3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d100-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d100-122">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="2d100-122">Type: **int2**</span></span>

<span data-ttu-id="2d100-123">Tercer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="2d100-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2d100-124">*Offset4* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2d100-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d100-125">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="2d100-125">Type: **int2**</span></span>

<span data-ttu-id="2d100-126">Cuarto componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="2d100-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2d100-127">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2d100-127">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d100-128">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2d100-128">Type: **uint**</span></span>

<span data-ttu-id="2d100-129">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="2d100-129">The status of the operation.</span></span> <span data-ttu-id="2d100-130">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="2d100-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="2d100-131">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="2d100-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="2d100-132">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="2d100-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d100-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d100-133">Return value</span></span>

<span data-ttu-id="2d100-134">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="2d100-134">Type: **TemplateType**</span></span>

<span data-ttu-id="2d100-135">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="2d100-135">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d100-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d100-136">Remarks</span></span>

<span data-ttu-id="2d100-137">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="2d100-137">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="2d100-138">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2d100-138">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2d100-139">Vértice</span><span class="sxs-lookup"><span data-stu-id="2d100-139">Vertex</span></span> | <span data-ttu-id="2d100-140">Casco</span><span class="sxs-lookup"><span data-stu-id="2d100-140">Hull</span></span> | <span data-ttu-id="2d100-141">Dominio</span><span class="sxs-lookup"><span data-stu-id="2d100-141">Domain</span></span> | <span data-ttu-id="2d100-142">Geometría</span><span class="sxs-lookup"><span data-stu-id="2d100-142">Geometry</span></span> | <span data-ttu-id="2d100-143">Píxel</span><span class="sxs-lookup"><span data-stu-id="2d100-143">Pixel</span></span> | <span data-ttu-id="2d100-144">Compute</span><span class="sxs-lookup"><span data-stu-id="2d100-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2d100-145">x</span><span class="sxs-lookup"><span data-stu-id="2d100-145">x</span></span>      | <span data-ttu-id="2d100-146">x</span><span class="sxs-lookup"><span data-stu-id="2d100-146">x</span></span>    | <span data-ttu-id="2d100-147">x</span><span class="sxs-lookup"><span data-stu-id="2d100-147">x</span></span>      | <span data-ttu-id="2d100-148">x</span><span class="sxs-lookup"><span data-stu-id="2d100-148">x</span></span>        | <span data-ttu-id="2d100-149">x</span><span class="sxs-lookup"><span data-stu-id="2d100-149">x</span></span>     | <span data-ttu-id="2d100-150">x</span><span class="sxs-lookup"><span data-stu-id="2d100-150">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2d100-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d100-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d100-152">Métodos GatherRed</span><span class="sxs-lookup"><span data-stu-id="2d100-152">GatherRed methods</span></span>](texture2darray-gatherred.md)
</dt> </dl>

 

 
