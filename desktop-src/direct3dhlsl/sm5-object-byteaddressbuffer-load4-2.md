---
title: 'ByteAddressBuffer:: Load4 (uint, uint) (función)'
description: Obtiene cuatro valores y el estado de la operación.
ms.assetid: C814F717-9FD4-4BFC-A91B-319477B7F3DE
keywords:
- Load4 de función HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab27ed9002562643ddf4df6b33efe9d8f0454d94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077776"
---
# <a name="load4uint-uint-function"></a><span data-ttu-id="c66a9-104">Load4 (uint, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="c66a9-104">Load4(uint, uint) function</span></span>

<span data-ttu-id="c66a9-105">Obtiene cuatro valores y el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c66a9-105">Gets four values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c66a9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c66a9-106">Syntax</span></span>

``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="c66a9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c66a9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c66a9-108">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c66a9-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c66a9-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c66a9-109">Type: **uint**</span></span>

<span data-ttu-id="c66a9-110">Dirección de entrada en bytes, que debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="c66a9-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="c66a9-111">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c66a9-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c66a9-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c66a9-112">Type: **uint**</span></span>

<span data-ttu-id="c66a9-113">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c66a9-113">The status of the operation.</span></span> <span data-ttu-id="c66a9-114">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="c66a9-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c66a9-115">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="c66a9-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c66a9-116">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="c66a9-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c66a9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c66a9-117">Return value</span></span>

<span data-ttu-id="c66a9-118">Tipo: **uint4**</span><span class="sxs-lookup"><span data-stu-id="c66a9-118">Type: **uint4**</span></span>

<span data-ttu-id="c66a9-119">Cuatro valores.</span><span class="sxs-lookup"><span data-stu-id="c66a9-119">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c66a9-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c66a9-120">Remarks</span></span>

<span data-ttu-id="c66a9-121">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="c66a9-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c66a9-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="c66a9-122">Vertex</span></span> | <span data-ttu-id="c66a9-123">Casco</span><span class="sxs-lookup"><span data-stu-id="c66a9-123">Hull</span></span> | <span data-ttu-id="c66a9-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="c66a9-124">Domain</span></span> | <span data-ttu-id="c66a9-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="c66a9-125">Geometry</span></span> | <span data-ttu-id="c66a9-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="c66a9-126">Pixel</span></span> | <span data-ttu-id="c66a9-127">Compute</span><span class="sxs-lookup"><span data-stu-id="c66a9-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c66a9-128">x</span><span class="sxs-lookup"><span data-stu-id="c66a9-128">x</span></span>      | <span data-ttu-id="c66a9-129">x</span><span class="sxs-lookup"><span data-stu-id="c66a9-129">x</span></span>    | <span data-ttu-id="c66a9-130">x</span><span class="sxs-lookup"><span data-stu-id="c66a9-130">x</span></span>      | <span data-ttu-id="c66a9-131">x</span><span class="sxs-lookup"><span data-stu-id="c66a9-131">x</span></span>        | <span data-ttu-id="c66a9-132">x</span><span class="sxs-lookup"><span data-stu-id="c66a9-132">x</span></span>     | <span data-ttu-id="c66a9-133">x</span><span class="sxs-lookup"><span data-stu-id="c66a9-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c66a9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c66a9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c66a9-135">Métodos Load4</span><span class="sxs-lookup"><span data-stu-id="c66a9-135">Load4 methods</span></span>](byteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="c66a9-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="c66a9-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 