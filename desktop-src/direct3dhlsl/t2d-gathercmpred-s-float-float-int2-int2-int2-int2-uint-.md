---
title: 'Texture2D:: GatherCmpRed (S, Float, Float, INT2, INT2, INT2, INT2, uint) (función)'
description: 'Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente rojo con respecto a un valor de comparación junto con el estado de asignación de mosaicos. | Texture2D:: GatherCmpRed (S, Float, Float, INT2, INT2, INT2, INT2, uint) (función)'
ms.assetid: 69B1F8FF-CE29-49DD-B756-3308E11D866D
keywords:
- GatherCmpRed de función HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d872623d7dcc8ea599e3c790493f2e1a8596b91
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998057"
---
# <a name="texture2dgathercmpredsfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="fe603-105">Texture2D:: GatherCmpRed (S, Float, Float, INT2, INT2, INT2, INT2, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="fe603-105">Texture2D::GatherCmpRed(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="fe603-106">Para cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente rojo con respecto a un valor de comparación junto con el estado de asignación de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="fe603-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe603-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe603-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpRed(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="fe603-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe603-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe603-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="fe603-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe603-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="fe603-110">Type: **SamplerState**</span></span>

<span data-ttu-id="fe603-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="fe603-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="fe603-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fe603-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe603-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fe603-113">Type: **float**</span></span>

<span data-ttu-id="fe603-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="fe603-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="fe603-115">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fe603-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe603-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="fe603-116">Type: **float**</span></span>

<span data-ttu-id="fe603-117">Valor que se va a comparar cada uno con cada valor muestreado.</span><span class="sxs-lookup"><span data-stu-id="fe603-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="fe603-118">*Offset1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fe603-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe603-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="fe603-119">Type: **int2**</span></span>

<span data-ttu-id="fe603-120">Primer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="fe603-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fe603-121">*Offset2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fe603-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe603-122">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="fe603-122">Type: **int2**</span></span>

<span data-ttu-id="fe603-123">Segundo componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="fe603-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fe603-124">*Offset3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fe603-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe603-125">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="fe603-125">Type: **int2**</span></span>

<span data-ttu-id="fe603-126">Tercer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="fe603-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fe603-127">*Offset4* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fe603-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe603-128">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="fe603-128">Type: **int2**</span></span>

<span data-ttu-id="fe603-129">Cuarto componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="fe603-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fe603-130">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fe603-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe603-131">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="fe603-131">Type: **uint**</span></span>

<span data-ttu-id="fe603-132">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fe603-132">The status of the operation.</span></span> <span data-ttu-id="fe603-133">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="fe603-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="fe603-134">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="fe603-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="fe603-135">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="fe603-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe603-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe603-136">Return value</span></span>

<span data-ttu-id="fe603-137">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="fe603-137">Type: **TemplateType**</span></span>

<span data-ttu-id="fe603-138">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="fe603-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe603-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe603-139">Remarks</span></span>

<span data-ttu-id="fe603-140">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="fe603-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="fe603-141">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="fe603-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fe603-142">Vértice</span><span class="sxs-lookup"><span data-stu-id="fe603-142">Vertex</span></span> | <span data-ttu-id="fe603-143">Casco</span><span class="sxs-lookup"><span data-stu-id="fe603-143">Hull</span></span> | <span data-ttu-id="fe603-144">Dominio</span><span class="sxs-lookup"><span data-stu-id="fe603-144">Domain</span></span> | <span data-ttu-id="fe603-145">Geometría</span><span class="sxs-lookup"><span data-stu-id="fe603-145">Geometry</span></span> | <span data-ttu-id="fe603-146">Píxel</span><span class="sxs-lookup"><span data-stu-id="fe603-146">Pixel</span></span> | <span data-ttu-id="fe603-147">Compute</span><span class="sxs-lookup"><span data-stu-id="fe603-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fe603-148">x</span><span class="sxs-lookup"><span data-stu-id="fe603-148">x</span></span>      | <span data-ttu-id="fe603-149">x</span><span class="sxs-lookup"><span data-stu-id="fe603-149">x</span></span>    | <span data-ttu-id="fe603-150">x</span><span class="sxs-lookup"><span data-stu-id="fe603-150">x</span></span>      | <span data-ttu-id="fe603-151">x</span><span class="sxs-lookup"><span data-stu-id="fe603-151">x</span></span>        | <span data-ttu-id="fe603-152">x</span><span class="sxs-lookup"><span data-stu-id="fe603-152">x</span></span>     | <span data-ttu-id="fe603-153">x</span><span class="sxs-lookup"><span data-stu-id="fe603-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fe603-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe603-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe603-155">Métodos GatherCmpRed</span><span class="sxs-lookup"><span data-stu-id="fe603-155">GatherCmpRed methods</span></span>](texture2d-gathercmpred.md)
</dt> </dl>

 

 
