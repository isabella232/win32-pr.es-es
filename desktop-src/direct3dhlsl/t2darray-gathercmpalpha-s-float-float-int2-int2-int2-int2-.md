---
title: 'Texture2DArray:: GatherCmpAlpha (S, Float, Float, INT2, INT2, INT2, INT2) (función)'
description: 'En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con respecto a un valor de comparación. | Texture2DArray:: GatherCmpAlpha (S, Float, Float, INT2, INT2, INT2, INT2) (función)'
ms.assetid: 0D6EC888-AB90-47C8-87D1-7B25E3EEB436
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
ms.openlocfilehash: e4fd93ed3925d9eaa27b369ffa44b2cc2ffde0f2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986462"
---
# <a name="texture2darraygathercmpalphasfloatfloatint2int2int2int2-function"></a><span data-ttu-id="83353-105">Texture2DArray:: GatherCmpAlpha (S, Float, Float, INT2, INT2, INT2, INT2) (función)</span><span class="sxs-lookup"><span data-stu-id="83353-105">Texture2DArray::GatherCmpAlpha(S,float,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="83353-106">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente alfa con respecto a un valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="83353-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="83353-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83353-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpAlpha(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="83353-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83353-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83353-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="83353-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83353-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="83353-110">Type: **SamplerState**</span></span>

<span data-ttu-id="83353-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="83353-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="83353-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="83353-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83353-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="83353-113">Type: **float**</span></span>

<span data-ttu-id="83353-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="83353-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="83353-115">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83353-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83353-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="83353-116">Type: **float**</span></span>

<span data-ttu-id="83353-117">Valor que se va a comparar cada uno con cada valor muestreado.</span><span class="sxs-lookup"><span data-stu-id="83353-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="83353-118">*Offset1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83353-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83353-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="83353-119">Type: **int2**</span></span>

<span data-ttu-id="83353-120">Primer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="83353-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="83353-121">*Offset2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83353-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83353-122">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="83353-122">Type: **int2**</span></span>

<span data-ttu-id="83353-123">Segundo componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="83353-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="83353-124">*Offset3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83353-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83353-125">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="83353-125">Type: **int2**</span></span>

<span data-ttu-id="83353-126">Tercer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="83353-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="83353-127">*Offset4* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83353-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83353-128">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="83353-128">Type: **int2**</span></span>

<span data-ttu-id="83353-129">Cuarto componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="83353-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83353-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83353-130">Return value</span></span>

<span data-ttu-id="83353-131">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="83353-131">Type: **TemplateType**</span></span>

<span data-ttu-id="83353-132">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="83353-132">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="83353-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83353-133">Remarks</span></span>

<span data-ttu-id="83353-134">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="83353-134">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="83353-135">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="83353-135">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="83353-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="83353-136">Vertex</span></span> | <span data-ttu-id="83353-137">Casco</span><span class="sxs-lookup"><span data-stu-id="83353-137">Hull</span></span> | <span data-ttu-id="83353-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="83353-138">Domain</span></span> | <span data-ttu-id="83353-139">Geometría</span><span class="sxs-lookup"><span data-stu-id="83353-139">Geometry</span></span> | <span data-ttu-id="83353-140">Píxel</span><span class="sxs-lookup"><span data-stu-id="83353-140">Pixel</span></span> | <span data-ttu-id="83353-141">Compute</span><span class="sxs-lookup"><span data-stu-id="83353-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="83353-142">x</span><span class="sxs-lookup"><span data-stu-id="83353-142">x</span></span>      | <span data-ttu-id="83353-143">x</span><span class="sxs-lookup"><span data-stu-id="83353-143">x</span></span>    | <span data-ttu-id="83353-144">x</span><span class="sxs-lookup"><span data-stu-id="83353-144">x</span></span>      | <span data-ttu-id="83353-145">x</span><span class="sxs-lookup"><span data-stu-id="83353-145">x</span></span>        | <span data-ttu-id="83353-146">x</span><span class="sxs-lookup"><span data-stu-id="83353-146">x</span></span>     | <span data-ttu-id="83353-147">x</span><span class="sxs-lookup"><span data-stu-id="83353-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="83353-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="83353-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83353-149">Métodos GatherCmpAlpha</span><span class="sxs-lookup"><span data-stu-id="83353-149">GatherCmpAlpha methods</span></span>](texture2darray-gathercmpalpha.md)
</dt> </dl>

 

 




