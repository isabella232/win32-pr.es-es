---
title: 'Texture2DArray:: Gather (S, Float, int, uint) (función)'
description: 'Devuelve los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal. | Texture2DArray:: Gather (S, Float, int, uint) (función)'
ms.assetid: 311A5042-19AA-41C7-8B22-2E34E4554250
keywords:
- Recopilación de la función HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1677fae87d8bbec3c0144cc8da0b5d13f0e0ae9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547619"
---
# <a name="texture2darraygathersfloatintuint-function"></a><span data-ttu-id="12661-105">Texture2DArray:: Gather (S, Float, int, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="12661-105">Texture2DArray::Gather(S,float,int,uint) function</span></span>

<span data-ttu-id="12661-106">Devuelve los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="12661-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="12661-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12661-107">Syntax</span></span>


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="12661-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12661-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12661-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="12661-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12661-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="12661-110">Type: **SamplerState**</span></span>

<span data-ttu-id="12661-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="12661-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="12661-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="12661-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12661-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="12661-113">Type: **float**</span></span>

<span data-ttu-id="12661-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="12661-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="12661-115">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="12661-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12661-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="12661-116">Type: **int**</span></span>

<span data-ttu-id="12661-117">Desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="12661-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="12661-118">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="12661-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12661-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="12661-119">Type: **uint**</span></span>

<span data-ttu-id="12661-120">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="12661-120">The status of the operation.</span></span> <span data-ttu-id="12661-121">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="12661-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="12661-122">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="12661-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="12661-123">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="12661-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12661-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12661-124">Return value</span></span>

<span data-ttu-id="12661-125">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="12661-125">Type: **TemplateType**</span></span>

<span data-ttu-id="12661-126">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="12661-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="12661-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12661-127">Remarks</span></span>

<span data-ttu-id="12661-128">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="12661-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="12661-129">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="12661-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="12661-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="12661-130">Vertex</span></span> | <span data-ttu-id="12661-131">Casco</span><span class="sxs-lookup"><span data-stu-id="12661-131">Hull</span></span> | <span data-ttu-id="12661-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="12661-132">Domain</span></span> | <span data-ttu-id="12661-133">Geometría</span><span class="sxs-lookup"><span data-stu-id="12661-133">Geometry</span></span> | <span data-ttu-id="12661-134">Píxel</span><span class="sxs-lookup"><span data-stu-id="12661-134">Pixel</span></span> | <span data-ttu-id="12661-135">Compute</span><span class="sxs-lookup"><span data-stu-id="12661-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="12661-136">x</span><span class="sxs-lookup"><span data-stu-id="12661-136">x</span></span>      | <span data-ttu-id="12661-137">x</span><span class="sxs-lookup"><span data-stu-id="12661-137">x</span></span>    | <span data-ttu-id="12661-138">x</span><span class="sxs-lookup"><span data-stu-id="12661-138">x</span></span>      | <span data-ttu-id="12661-139">x</span><span class="sxs-lookup"><span data-stu-id="12661-139">x</span></span>        | <span data-ttu-id="12661-140">x</span><span class="sxs-lookup"><span data-stu-id="12661-140">x</span></span>     | <span data-ttu-id="12661-141">x</span><span class="sxs-lookup"><span data-stu-id="12661-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="12661-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="12661-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12661-143">Recopilar métodos</span><span class="sxs-lookup"><span data-stu-id="12661-143">Gather methods</span></span>](texture2darray-gather.md)
</dt> </dl>

 

 
