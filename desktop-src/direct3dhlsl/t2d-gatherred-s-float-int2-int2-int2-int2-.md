---
title: 'Texture2D:: GatherRed (S, Float, INT2, INT2, INT2, INT2) (función)'
description: 'Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal. | Texture2D:: GatherRed (S, Float, INT2, INT2, INT2, INT2) (función)'
ms.assetid: 85C321CB-B77C-430B-921D-D56E5597B24A
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
ms.openlocfilehash: b17e192388b6fc439d31cfe35eca99168da1c3f5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279923"
---
# <a name="texture2dgatherredsfloatint2int2int2int2-function"></a><span data-ttu-id="76c8b-105">Texture2D:: GatherRed (S, Float, INT2, INT2, INT2, INT2) (función)</span><span class="sxs-lookup"><span data-stu-id="76c8b-105">Texture2D::GatherRed(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="76c8b-106">Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="76c8b-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="76c8b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76c8b-107">Syntax</span></span>


``` syntax
TemplateType GatherRed(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="76c8b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76c8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76c8b-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="76c8b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76c8b-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="76c8b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="76c8b-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="76c8b-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="76c8b-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="76c8b-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76c8b-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="76c8b-113">Type: **float**</span></span>

<span data-ttu-id="76c8b-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="76c8b-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="76c8b-115">*Offset1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="76c8b-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76c8b-116">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="76c8b-116">Type: **int2**</span></span>

<span data-ttu-id="76c8b-117">Primer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="76c8b-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="76c8b-118">*Offset2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="76c8b-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76c8b-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="76c8b-119">Type: **int2**</span></span>

<span data-ttu-id="76c8b-120">Segundo componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="76c8b-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="76c8b-121">*Offset3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="76c8b-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76c8b-122">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="76c8b-122">Type: **int2**</span></span>

<span data-ttu-id="76c8b-123">Tercer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="76c8b-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="76c8b-124">*Offset4* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="76c8b-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76c8b-125">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="76c8b-125">Type: **int2**</span></span>

<span data-ttu-id="76c8b-126">Cuarto componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="76c8b-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76c8b-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76c8b-127">Return value</span></span>

<span data-ttu-id="76c8b-128">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="76c8b-128">Type: **TemplateType**</span></span>

<span data-ttu-id="76c8b-129">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="76c8b-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="76c8b-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76c8b-130">Remarks</span></span>

<span data-ttu-id="76c8b-131">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="76c8b-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="76c8b-132">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="76c8b-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="76c8b-133">Vértice</span><span class="sxs-lookup"><span data-stu-id="76c8b-133">Vertex</span></span> | <span data-ttu-id="76c8b-134">Casco</span><span class="sxs-lookup"><span data-stu-id="76c8b-134">Hull</span></span> | <span data-ttu-id="76c8b-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="76c8b-135">Domain</span></span> | <span data-ttu-id="76c8b-136">Geometría</span><span class="sxs-lookup"><span data-stu-id="76c8b-136">Geometry</span></span> | <span data-ttu-id="76c8b-137">Píxel</span><span class="sxs-lookup"><span data-stu-id="76c8b-137">Pixel</span></span> | <span data-ttu-id="76c8b-138">Compute</span><span class="sxs-lookup"><span data-stu-id="76c8b-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="76c8b-139">x</span><span class="sxs-lookup"><span data-stu-id="76c8b-139">x</span></span>      | <span data-ttu-id="76c8b-140">x</span><span class="sxs-lookup"><span data-stu-id="76c8b-140">x</span></span>    | <span data-ttu-id="76c8b-141">x</span><span class="sxs-lookup"><span data-stu-id="76c8b-141">x</span></span>      | <span data-ttu-id="76c8b-142">x</span><span class="sxs-lookup"><span data-stu-id="76c8b-142">x</span></span>        | <span data-ttu-id="76c8b-143">x</span><span class="sxs-lookup"><span data-stu-id="76c8b-143">x</span></span>     | <span data-ttu-id="76c8b-144">x</span><span class="sxs-lookup"><span data-stu-id="76c8b-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="76c8b-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="76c8b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76c8b-146">Métodos GatherRed</span><span class="sxs-lookup"><span data-stu-id="76c8b-146">GatherRed methods</span></span>](texture2d-gatherred.md)
</dt> </dl>

 

 




