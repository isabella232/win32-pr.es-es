---
title: 'TextureCube:: Gather (S, Float, uint) (función)'
description: 'Devuelve los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal. | TextureCube:: Gather (S, Float, uint) (función)'
ms.assetid: 23FA8135-ECF0-4CAE-9A1C-B05DA3676453
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
ms.openlocfilehash: e9710343ff9b09e4425bc133db6dab4d118d807e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986251"
---
# <a name="texturecubegathersfloatuint-function"></a><span data-ttu-id="377a7-105">TextureCube:: Gather (S, Float, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="377a7-105">TextureCube::Gather(S,float,uint) function</span></span>

<span data-ttu-id="377a7-106">Devuelve los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.</span><span class="sxs-lookup"><span data-stu-id="377a7-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="377a7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="377a7-107">Syntax</span></span>


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="377a7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="377a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="377a7-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="377a7-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="377a7-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="377a7-110">Type: **SamplerState**</span></span>

<span data-ttu-id="377a7-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="377a7-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="377a7-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="377a7-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="377a7-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="377a7-113">Type: **float**</span></span>

<span data-ttu-id="377a7-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="377a7-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="377a7-115">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="377a7-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="377a7-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="377a7-116">Type: **uint**</span></span>

<span data-ttu-id="377a7-117">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="377a7-117">The status of the operation.</span></span> <span data-ttu-id="377a7-118">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="377a7-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="377a7-119">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="377a7-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="377a7-120">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="377a7-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="377a7-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="377a7-121">Return value</span></span>

<span data-ttu-id="377a7-122">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="377a7-122">Type: **TemplateType**</span></span>

<span data-ttu-id="377a7-123">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="377a7-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="377a7-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="377a7-124">Remarks</span></span>

<span data-ttu-id="377a7-125">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="377a7-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="377a7-126">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="377a7-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="377a7-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="377a7-127">Vertex</span></span> | <span data-ttu-id="377a7-128">Casco</span><span class="sxs-lookup"><span data-stu-id="377a7-128">Hull</span></span> | <span data-ttu-id="377a7-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="377a7-129">Domain</span></span> | <span data-ttu-id="377a7-130">Geometría</span><span class="sxs-lookup"><span data-stu-id="377a7-130">Geometry</span></span> | <span data-ttu-id="377a7-131">Píxel</span><span class="sxs-lookup"><span data-stu-id="377a7-131">Pixel</span></span> | <span data-ttu-id="377a7-132">Compute</span><span class="sxs-lookup"><span data-stu-id="377a7-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="377a7-133">x</span><span class="sxs-lookup"><span data-stu-id="377a7-133">x</span></span>      | <span data-ttu-id="377a7-134">x</span><span class="sxs-lookup"><span data-stu-id="377a7-134">x</span></span>    | <span data-ttu-id="377a7-135">x</span><span class="sxs-lookup"><span data-stu-id="377a7-135">x</span></span>      | <span data-ttu-id="377a7-136">x</span><span class="sxs-lookup"><span data-stu-id="377a7-136">x</span></span>        | <span data-ttu-id="377a7-137">x</span><span class="sxs-lookup"><span data-stu-id="377a7-137">x</span></span>     | <span data-ttu-id="377a7-138">x</span><span class="sxs-lookup"><span data-stu-id="377a7-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="377a7-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="377a7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="377a7-140">Recopilar métodos</span><span class="sxs-lookup"><span data-stu-id="377a7-140">Gather methods</span></span>](texturecube-gather.md)
</dt> <dt>

[<span data-ttu-id="377a7-141">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="377a7-141">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
