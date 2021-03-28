---
title: 'TextureCube:: GatherGreen (S, Float, uint) (función)'
description: 'Devuelve los componentes verdes de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, junto con el estado de asignación de mosaicos. | TextureCube:: GatherGreen (S, Float, uint) (función)'
ms.assetid: DB0A6386-70ED-4D8C-A4EE-C058496D2F12
keywords:
- GatherGreen de función HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1555b72b095ce0589a8ae9b396c67d29236db82c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998217"
---
# <a name="texturecubegathergreensfloatuint-function"></a><span data-ttu-id="7b6b5-105">TextureCube:: GatherGreen (S, Float, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="7b6b5-105">TextureCube::GatherGreen(S,float,uint) function</span></span>

<span data-ttu-id="7b6b5-106">Devuelve los componentes verdes de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, junto con el estado de asignación de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="7b6b5-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b6b5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b6b5-107">Syntax</span></span>


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="7b6b5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b6b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b6b5-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7b6b5-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b6b5-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="7b6b5-110">Type: **SamplerState**</span></span>

<span data-ttu-id="7b6b5-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="7b6b5-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="7b6b5-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="7b6b5-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b6b5-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="7b6b5-113">Type: **float**</span></span>

<span data-ttu-id="7b6b5-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="7b6b5-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="7b6b5-115">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7b6b5-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b6b5-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7b6b5-116">Type: **uint**</span></span>

<span data-ttu-id="7b6b5-117">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="7b6b5-117">The status of the operation.</span></span> <span data-ttu-id="7b6b5-118">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="7b6b5-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="7b6b5-119">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="7b6b5-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="7b6b5-120">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="7b6b5-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b6b5-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b6b5-121">Return value</span></span>

<span data-ttu-id="7b6b5-122">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="7b6b5-122">Type: **TemplateType**</span></span>

<span data-ttu-id="7b6b5-123">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="7b6b5-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b6b5-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b6b5-124">Remarks</span></span>

<span data-ttu-id="7b6b5-125">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="7b6b5-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="7b6b5-126">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="7b6b5-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7b6b5-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="7b6b5-127">Vertex</span></span> | <span data-ttu-id="7b6b5-128">Casco</span><span class="sxs-lookup"><span data-stu-id="7b6b5-128">Hull</span></span> | <span data-ttu-id="7b6b5-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="7b6b5-129">Domain</span></span> | <span data-ttu-id="7b6b5-130">Geometría</span><span class="sxs-lookup"><span data-stu-id="7b6b5-130">Geometry</span></span> | <span data-ttu-id="7b6b5-131">Píxel</span><span class="sxs-lookup"><span data-stu-id="7b6b5-131">Pixel</span></span> | <span data-ttu-id="7b6b5-132">Compute</span><span class="sxs-lookup"><span data-stu-id="7b6b5-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7b6b5-133">x</span><span class="sxs-lookup"><span data-stu-id="7b6b5-133">x</span></span>      | <span data-ttu-id="7b6b5-134">x</span><span class="sxs-lookup"><span data-stu-id="7b6b5-134">x</span></span>    | <span data-ttu-id="7b6b5-135">x</span><span class="sxs-lookup"><span data-stu-id="7b6b5-135">x</span></span>      | <span data-ttu-id="7b6b5-136">x</span><span class="sxs-lookup"><span data-stu-id="7b6b5-136">x</span></span>        | <span data-ttu-id="7b6b5-137">x</span><span class="sxs-lookup"><span data-stu-id="7b6b5-137">x</span></span>     | <span data-ttu-id="7b6b5-138">x</span><span class="sxs-lookup"><span data-stu-id="7b6b5-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7b6b5-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b6b5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b6b5-140">Métodos GatherGreen</span><span class="sxs-lookup"><span data-stu-id="7b6b5-140">GatherGreen methods</span></span>](texturecube-gathergreen.md)
</dt> <dt>

[<span data-ttu-id="7b6b5-141">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="7b6b5-141">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
