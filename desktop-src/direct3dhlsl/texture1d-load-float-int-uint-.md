---
title: 'Texture1D:: Load (int, int, uint) (función)'
description: 'Lee los datos de textura y devuelve el estado de la operación. | Texture1D:: Load (int, int, uint) (función)'
ms.assetid: 5C489CBD-E4F6-4CB5-8E7E-EC34633D75B0
keywords:
- Carga de la función HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7733ab4802037d83dbb2b4ce523ff7bb57f729
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986470"
---
# <a name="texture1dloadintintuint-function"></a><span data-ttu-id="51d58-105">Texture1D:: Load (int, int, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="51d58-105">Texture1D::Load(int,int,uint) function</span></span>

<span data-ttu-id="51d58-106">Lee los datos de textura y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="51d58-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="51d58-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51d58-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="51d58-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51d58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51d58-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="51d58-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51d58-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="51d58-110">Type: **int**</span></span>

<span data-ttu-id="51d58-111">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="51d58-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="51d58-112">*Desplazamiento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51d58-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51d58-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="51d58-113">Type: **int**</span></span>

<span data-ttu-id="51d58-114">Desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="51d58-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="51d58-115">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="51d58-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51d58-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="51d58-116">Type: **uint**</span></span>

<span data-ttu-id="51d58-117">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="51d58-117">The status of the operation.</span></span> <span data-ttu-id="51d58-118">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="51d58-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="51d58-119">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="51d58-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="51d58-120">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="51d58-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51d58-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51d58-121">Return value</span></span>

<span data-ttu-id="51d58-122">Escriba:</span><span class="sxs-lookup"><span data-stu-id="51d58-122">Type:</span></span>

<span data-ttu-id="51d58-123">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**Texture1D**](sm5-object-texture1d.md) .</span><span class="sxs-lookup"><span data-stu-id="51d58-123">The return type matches the type in the declaration for the [**Texture1D**](sm5-object-texture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="51d58-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51d58-124">Remarks</span></span>

<span data-ttu-id="51d58-125">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="51d58-125">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="51d58-126">Vértice</span><span class="sxs-lookup"><span data-stu-id="51d58-126">Vertex</span></span> | <span data-ttu-id="51d58-127">Casco</span><span class="sxs-lookup"><span data-stu-id="51d58-127">Hull</span></span> | <span data-ttu-id="51d58-128">Dominio</span><span class="sxs-lookup"><span data-stu-id="51d58-128">Domain</span></span> | <span data-ttu-id="51d58-129">Geometría</span><span class="sxs-lookup"><span data-stu-id="51d58-129">Geometry</span></span> | <span data-ttu-id="51d58-130">Píxel</span><span class="sxs-lookup"><span data-stu-id="51d58-130">Pixel</span></span> | <span data-ttu-id="51d58-131">Compute</span><span class="sxs-lookup"><span data-stu-id="51d58-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="51d58-132">x</span><span class="sxs-lookup"><span data-stu-id="51d58-132">x</span></span>      | <span data-ttu-id="51d58-133">x</span><span class="sxs-lookup"><span data-stu-id="51d58-133">x</span></span>    | <span data-ttu-id="51d58-134">x</span><span class="sxs-lookup"><span data-stu-id="51d58-134">x</span></span>      | <span data-ttu-id="51d58-135">x</span><span class="sxs-lookup"><span data-stu-id="51d58-135">x</span></span>        | <span data-ttu-id="51d58-136">x</span><span class="sxs-lookup"><span data-stu-id="51d58-136">x</span></span>     | <span data-ttu-id="51d58-137">x</span><span class="sxs-lookup"><span data-stu-id="51d58-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="51d58-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="51d58-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51d58-139">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="51d58-139">Load methods</span></span>](texture1d-load.md)
</dt> <dt>

[<span data-ttu-id="51d58-140">**Texture1D**</span><span class="sxs-lookup"><span data-stu-id="51d58-140">**Texture1D**</span></span>](sm5-object-texture1d.md)
</dt> </dl>

 

 
