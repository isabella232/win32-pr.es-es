---
title: 'RWByteAddressBuffer:: Load3 (uint, uint) (función)'
description: Obtiene tres valores y devuelve el estado de la operación.
ms.assetid: EBCCDAF3-69B9-4132-85EC-82759F292811
keywords:
- Load3 de función HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8451abe17c3ff74a1906828b3570dc6ee98782f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359253"
---
# <a name="load3uintuint-function"></a><span data-ttu-id="daf37-104">Load3 (uint, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="daf37-104">Load3(uint,uint) function</span></span>

<span data-ttu-id="daf37-105">Obtiene tres valores y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="daf37-105">Gets three values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="daf37-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="daf37-106">Syntax</span></span>


``` syntax
uint3 Load3(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="daf37-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="daf37-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daf37-108">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="daf37-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daf37-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="daf37-109">Type: **uint**</span></span>

<span data-ttu-id="daf37-110">Ubicación del búfer.</span><span class="sxs-lookup"><span data-stu-id="daf37-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="daf37-111">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="daf37-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="daf37-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="daf37-112">Type: **uint**</span></span>

<span data-ttu-id="daf37-113">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="daf37-113">The status of the operation.</span></span> <span data-ttu-id="daf37-114">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="daf37-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="daf37-115">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="daf37-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="daf37-116">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="daf37-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daf37-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="daf37-117">Return value</span></span>

<span data-ttu-id="daf37-118">Tipo: **UInt3**</span><span class="sxs-lookup"><span data-stu-id="daf37-118">Type: **uint3**</span></span>

<span data-ttu-id="daf37-119">Tres valores.</span><span class="sxs-lookup"><span data-stu-id="daf37-119">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="daf37-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="daf37-120">Remarks</span></span>

<span data-ttu-id="daf37-121">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="daf37-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="daf37-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="daf37-122">Vertex</span></span> | <span data-ttu-id="daf37-123">Casco</span><span class="sxs-lookup"><span data-stu-id="daf37-123">Hull</span></span> | <span data-ttu-id="daf37-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="daf37-124">Domain</span></span> | <span data-ttu-id="daf37-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="daf37-125">Geometry</span></span> | <span data-ttu-id="daf37-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="daf37-126">Pixel</span></span> | <span data-ttu-id="daf37-127">Compute</span><span class="sxs-lookup"><span data-stu-id="daf37-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="daf37-128">x</span><span class="sxs-lookup"><span data-stu-id="daf37-128">x</span></span>     | <span data-ttu-id="daf37-129">x</span><span class="sxs-lookup"><span data-stu-id="daf37-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="daf37-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="daf37-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daf37-131">Métodos Load3</span><span class="sxs-lookup"><span data-stu-id="daf37-131">Load3 methods</span></span>](rwbyteaddressbuffer-load3.md)
</dt> </dl>

 

 