---
title: 'RWByteAddressBuffer:: Load4 (uint, uint) (función)'
description: Obtiene cuatro valores y devuelve el estado de la operación.
ms.assetid: 10C21836-3CE4-4AE9-82F4-C8BBDE19CA69
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
ms.openlocfilehash: 14cb5354c21935c22833ea6f4b54b20fedc696f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793743"
---
# <a name="load4uintuint-function"></a><span data-ttu-id="095bc-104">Load4 (uint, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="095bc-104">Load4(uint,uint) function</span></span>

<span data-ttu-id="095bc-105">Obtiene cuatro valores y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="095bc-105">Gets four values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="095bc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="095bc-106">Syntax</span></span>


``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="095bc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="095bc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="095bc-108">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="095bc-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="095bc-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="095bc-109">Type: **uint**</span></span>

<span data-ttu-id="095bc-110">Ubicación del búfer.</span><span class="sxs-lookup"><span data-stu-id="095bc-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="095bc-111">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="095bc-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="095bc-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="095bc-112">Type: **uint**</span></span>

<span data-ttu-id="095bc-113">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="095bc-113">The status of the operation.</span></span> <span data-ttu-id="095bc-114">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="095bc-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="095bc-115">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="095bc-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="095bc-116">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="095bc-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="095bc-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="095bc-117">Return value</span></span>

<span data-ttu-id="095bc-118">Tipo: **uint4**</span><span class="sxs-lookup"><span data-stu-id="095bc-118">Type: **uint4**</span></span>

<span data-ttu-id="095bc-119">Cuatro valores.</span><span class="sxs-lookup"><span data-stu-id="095bc-119">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="095bc-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="095bc-120">Remarks</span></span>

<span data-ttu-id="095bc-121">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="095bc-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="095bc-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="095bc-122">Vertex</span></span> | <span data-ttu-id="095bc-123">Casco</span><span class="sxs-lookup"><span data-stu-id="095bc-123">Hull</span></span> | <span data-ttu-id="095bc-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="095bc-124">Domain</span></span> | <span data-ttu-id="095bc-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="095bc-125">Geometry</span></span> | <span data-ttu-id="095bc-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="095bc-126">Pixel</span></span> | <span data-ttu-id="095bc-127">Compute</span><span class="sxs-lookup"><span data-stu-id="095bc-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="095bc-128">x</span><span class="sxs-lookup"><span data-stu-id="095bc-128">x</span></span>     | <span data-ttu-id="095bc-129">x</span><span class="sxs-lookup"><span data-stu-id="095bc-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="095bc-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="095bc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="095bc-131">Métodos Load4</span><span class="sxs-lookup"><span data-stu-id="095bc-131">Load4 methods</span></span>](rwbyteaddressbuffer-load4.md)
</dt> </dl>

 

 