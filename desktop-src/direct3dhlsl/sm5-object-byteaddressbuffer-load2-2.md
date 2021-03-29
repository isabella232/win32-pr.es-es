---
title: 'ByteAddressBuffer:: Load2 (uint, uint) (función)'
description: Obtiene dos valores y el estado de la operación.
ms.assetid: EE6FA09D-0C86-499D-86F9-EAA56125EB91
keywords:
- Load2 de función HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 662e40789f59b75e53111fbab6d24288f27c8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078138"
---
# <a name="load2uint-uint-function"></a><span data-ttu-id="b5746-104">Load2 (uint, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="b5746-104">Load2(uint, uint) function</span></span>

<span data-ttu-id="b5746-105">Obtiene dos valores y el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="b5746-105">Gets two values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5746-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5746-106">Syntax</span></span>

``` syntax
uint2 Load2(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="b5746-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5746-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5746-108">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b5746-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5746-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b5746-109">Type: **uint**</span></span>

<span data-ttu-id="b5746-110">Dirección de entrada en bytes, que debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="b5746-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="b5746-111">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b5746-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5746-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b5746-112">Type: **uint**</span></span>

<span data-ttu-id="b5746-113">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="b5746-113">The status of the operation.</span></span> <span data-ttu-id="b5746-114">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="b5746-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b5746-115">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="b5746-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b5746-116">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="b5746-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5746-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5746-117">Return value</span></span>

<span data-ttu-id="b5746-118">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="b5746-118">Type: **uint2**</span></span>

<span data-ttu-id="b5746-119">Dos valores.</span><span class="sxs-lookup"><span data-stu-id="b5746-119">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5746-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5746-120">Remarks</span></span>

<span data-ttu-id="b5746-121">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b5746-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b5746-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="b5746-122">Vertex</span></span> | <span data-ttu-id="b5746-123">Casco</span><span class="sxs-lookup"><span data-stu-id="b5746-123">Hull</span></span> | <span data-ttu-id="b5746-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="b5746-124">Domain</span></span> | <span data-ttu-id="b5746-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="b5746-125">Geometry</span></span> | <span data-ttu-id="b5746-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="b5746-126">Pixel</span></span> | <span data-ttu-id="b5746-127">Compute</span><span class="sxs-lookup"><span data-stu-id="b5746-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b5746-128">x</span><span class="sxs-lookup"><span data-stu-id="b5746-128">x</span></span>      | <span data-ttu-id="b5746-129">x</span><span class="sxs-lookup"><span data-stu-id="b5746-129">x</span></span>    | <span data-ttu-id="b5746-130">x</span><span class="sxs-lookup"><span data-stu-id="b5746-130">x</span></span>      | <span data-ttu-id="b5746-131">x</span><span class="sxs-lookup"><span data-stu-id="b5746-131">x</span></span>        | <span data-ttu-id="b5746-132">x</span><span class="sxs-lookup"><span data-stu-id="b5746-132">x</span></span>     | <span data-ttu-id="b5746-133">x</span><span class="sxs-lookup"><span data-stu-id="b5746-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b5746-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5746-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5746-135">Métodos Load2</span><span class="sxs-lookup"><span data-stu-id="b5746-135">Load2 methods</span></span>](byteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="b5746-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="b5746-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 