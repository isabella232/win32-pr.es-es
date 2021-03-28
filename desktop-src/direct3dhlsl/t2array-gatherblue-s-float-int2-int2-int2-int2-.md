---
title: GatherBlue (S, Float, INT2, INT2, INT2, INT2) (función, referencia de HLSL)
description: Devuelve los componentes azules de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal. | GatherBlue (S, Float, INT2, INT2, INT2, INT2) (función, referencia de HLSL)
ms.assetid: 0DDD3235-4F12-4D74-975A-F70A271C1FC0
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
ms.openlocfilehash: a5676d9d6b25c6e67123c59dac14efa234386d4e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362307"
---
# <a name="gatherbluesfloatint2int2int2int2-function-hlsl-reference"></a><span data-ttu-id="72f2a-105">GatherBlue (S, Float, INT2, INT2, INT2, INT2) (función, referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="72f2a-105">GatherBlue(S,float,int2,int2,int2,int2) function (HLSL reference)</span></span>

<span data-ttu-id="72f2a-106">Devuelve los componentes azules de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="72f2a-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="72f2a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72f2a-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="72f2a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72f2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72f2a-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="72f2a-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f2a-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="72f2a-110">Type: **SamplerState**</span></span>

<span data-ttu-id="72f2a-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="72f2a-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="72f2a-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="72f2a-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f2a-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="72f2a-113">Type: **float**</span></span>

<span data-ttu-id="72f2a-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="72f2a-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="72f2a-115">*Offset1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72f2a-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f2a-116">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="72f2a-116">Type: **int2**</span></span>

<span data-ttu-id="72f2a-117">Primer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="72f2a-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="72f2a-118">*Offset2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72f2a-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f2a-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="72f2a-119">Type: **int2**</span></span>

<span data-ttu-id="72f2a-120">Segundo componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="72f2a-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="72f2a-121">*Offset3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72f2a-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f2a-122">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="72f2a-122">Type: **int2**</span></span>

<span data-ttu-id="72f2a-123">Tercer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="72f2a-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="72f2a-124">*Offset4* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="72f2a-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f2a-125">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="72f2a-125">Type: **int2**</span></span>

<span data-ttu-id="72f2a-126">Cuarto componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="72f2a-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72f2a-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72f2a-127">Return value</span></span>

<span data-ttu-id="72f2a-128">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="72f2a-128">Type: **TemplateType**</span></span>

<span data-ttu-id="72f2a-129">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="72f2a-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="72f2a-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72f2a-130">Remarks</span></span>

<span data-ttu-id="72f2a-131">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="72f2a-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="72f2a-132">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="72f2a-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="72f2a-133">Vértice</span><span class="sxs-lookup"><span data-stu-id="72f2a-133">Vertex</span></span> | <span data-ttu-id="72f2a-134">Casco</span><span class="sxs-lookup"><span data-stu-id="72f2a-134">Hull</span></span> | <span data-ttu-id="72f2a-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="72f2a-135">Domain</span></span> | <span data-ttu-id="72f2a-136">Geometría</span><span class="sxs-lookup"><span data-stu-id="72f2a-136">Geometry</span></span> | <span data-ttu-id="72f2a-137">Píxel</span><span class="sxs-lookup"><span data-stu-id="72f2a-137">Pixel</span></span> | <span data-ttu-id="72f2a-138">Compute</span><span class="sxs-lookup"><span data-stu-id="72f2a-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="72f2a-139">x</span><span class="sxs-lookup"><span data-stu-id="72f2a-139">x</span></span>      | <span data-ttu-id="72f2a-140">x</span><span class="sxs-lookup"><span data-stu-id="72f2a-140">x</span></span>    | <span data-ttu-id="72f2a-141">x</span><span class="sxs-lookup"><span data-stu-id="72f2a-141">x</span></span>      | <span data-ttu-id="72f2a-142">x</span><span class="sxs-lookup"><span data-stu-id="72f2a-142">x</span></span>        | <span data-ttu-id="72f2a-143">x</span><span class="sxs-lookup"><span data-stu-id="72f2a-143">x</span></span>     | <span data-ttu-id="72f2a-144">x</span><span class="sxs-lookup"><span data-stu-id="72f2a-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="72f2a-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="72f2a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f2a-146">Métodos GatherBlue</span><span class="sxs-lookup"><span data-stu-id="72f2a-146">GatherBlue methods</span></span>](texture2darray-gatherblue.md)
</dt> </dl>

 

 




