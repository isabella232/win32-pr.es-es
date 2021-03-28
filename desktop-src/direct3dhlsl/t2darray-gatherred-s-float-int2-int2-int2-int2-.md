---
title: 'Texture2DArray:: GatherRed (S, Float, INT2, INT2, INT2, INT2) (función)'
description: 'Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal. | Texture2DArray:: GatherRed (S, Float, INT2, INT2, INT2, INT2) (función)'
ms.assetid: EB367373-D798-4CBA-AEB6-8BF89371D765
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
ms.openlocfilehash: a080580c3735018c9e6459acd6b742ce45e933d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003508"
---
# <a name="texture2darraygatherredsfloatint2int2int2int2-function"></a><span data-ttu-id="23035-105">Texture2DArray:: GatherRed (S, Float, INT2, INT2, INT2, INT2) (función)</span><span class="sxs-lookup"><span data-stu-id="23035-105">Texture2DArray::GatherRed(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="23035-106">Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="23035-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="23035-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23035-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="23035-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23035-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23035-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="23035-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23035-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="23035-110">Type: **SamplerState**</span></span>

<span data-ttu-id="23035-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="23035-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="23035-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="23035-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23035-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="23035-113">Type: **float**</span></span>

<span data-ttu-id="23035-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="23035-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="23035-115">*Offset1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23035-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23035-116">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="23035-116">Type: **int2**</span></span>

<span data-ttu-id="23035-117">Primer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="23035-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="23035-118">*Offset2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23035-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23035-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="23035-119">Type: **int2**</span></span>

<span data-ttu-id="23035-120">Segundo componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="23035-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="23035-121">*Offset3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23035-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23035-122">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="23035-122">Type: **int2**</span></span>

<span data-ttu-id="23035-123">Tercer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="23035-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="23035-124">*Offset4* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23035-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23035-125">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="23035-125">Type: **int2**</span></span>

<span data-ttu-id="23035-126">Cuarto componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="23035-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23035-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23035-127">Return value</span></span>

<span data-ttu-id="23035-128">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="23035-128">Type: **TemplateType**</span></span>

<span data-ttu-id="23035-129">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="23035-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="23035-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23035-130">Remarks</span></span>

<span data-ttu-id="23035-131">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="23035-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="23035-132">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="23035-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="23035-133">Vértice</span><span class="sxs-lookup"><span data-stu-id="23035-133">Vertex</span></span> | <span data-ttu-id="23035-134">Casco</span><span class="sxs-lookup"><span data-stu-id="23035-134">Hull</span></span> | <span data-ttu-id="23035-135">Dominio</span><span class="sxs-lookup"><span data-stu-id="23035-135">Domain</span></span> | <span data-ttu-id="23035-136">Geometría</span><span class="sxs-lookup"><span data-stu-id="23035-136">Geometry</span></span> | <span data-ttu-id="23035-137">Píxel</span><span class="sxs-lookup"><span data-stu-id="23035-137">Pixel</span></span> | <span data-ttu-id="23035-138">Compute</span><span class="sxs-lookup"><span data-stu-id="23035-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="23035-139">x</span><span class="sxs-lookup"><span data-stu-id="23035-139">x</span></span>      | <span data-ttu-id="23035-140">x</span><span class="sxs-lookup"><span data-stu-id="23035-140">x</span></span>    | <span data-ttu-id="23035-141">x</span><span class="sxs-lookup"><span data-stu-id="23035-141">x</span></span>      | <span data-ttu-id="23035-142">x</span><span class="sxs-lookup"><span data-stu-id="23035-142">x</span></span>        | <span data-ttu-id="23035-143">x</span><span class="sxs-lookup"><span data-stu-id="23035-143">x</span></span>     | <span data-ttu-id="23035-144">x</span><span class="sxs-lookup"><span data-stu-id="23035-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="23035-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="23035-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23035-146">Métodos GatherRed</span><span class="sxs-lookup"><span data-stu-id="23035-146">GatherRed methods</span></span>](texture2darray-gatherred.md)
</dt> </dl>

 

 




