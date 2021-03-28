---
title: 'RWByteAddressBuffer:: Load2 (uint, uint) (función)'
description: Obtiene dos valores y devuelve el estado de la operación.
ms.assetid: E6BBA8A7-D53F-4718-B007-EBDE50FADB06
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
ms.openlocfilehash: 92fc492fddb6ad024a4507829e81dab4886af590
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149281"
---
# <a name="load2uintuint-function"></a><span data-ttu-id="031f8-104">Load2 (uint, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="031f8-104">Load2(uint,uint) function</span></span>

<span data-ttu-id="031f8-105">Obtiene dos valores y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="031f8-105">Gets two values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="031f8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="031f8-106">Syntax</span></span>


``` syntax
uint2 Load2(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="031f8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="031f8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="031f8-108">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="031f8-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="031f8-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="031f8-109">Type: **uint**</span></span>

<span data-ttu-id="031f8-110">Ubicación del búfer.</span><span class="sxs-lookup"><span data-stu-id="031f8-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="031f8-111">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="031f8-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="031f8-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="031f8-112">Type: **uint**</span></span>

<span data-ttu-id="031f8-113">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="031f8-113">The status of the operation.</span></span> <span data-ttu-id="031f8-114">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="031f8-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="031f8-115">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="031f8-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="031f8-116">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="031f8-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="031f8-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="031f8-117">Return value</span></span>

<span data-ttu-id="031f8-118">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="031f8-118">Type: **uint2**</span></span>

<span data-ttu-id="031f8-119">Dos valores.</span><span class="sxs-lookup"><span data-stu-id="031f8-119">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="031f8-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="031f8-120">Remarks</span></span>

<span data-ttu-id="031f8-121">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="031f8-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="031f8-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="031f8-122">Vertex</span></span> | <span data-ttu-id="031f8-123">Casco</span><span class="sxs-lookup"><span data-stu-id="031f8-123">Hull</span></span> | <span data-ttu-id="031f8-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="031f8-124">Domain</span></span> | <span data-ttu-id="031f8-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="031f8-125">Geometry</span></span> | <span data-ttu-id="031f8-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="031f8-126">Pixel</span></span> | <span data-ttu-id="031f8-127">Compute</span><span class="sxs-lookup"><span data-stu-id="031f8-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="031f8-128">x</span><span class="sxs-lookup"><span data-stu-id="031f8-128">x</span></span>     | <span data-ttu-id="031f8-129">x</span><span class="sxs-lookup"><span data-stu-id="031f8-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="031f8-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="031f8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="031f8-131">Métodos Load2</span><span class="sxs-lookup"><span data-stu-id="031f8-131">Load2 methods</span></span>](rwbyteaddressbuffer-load2.md)
</dt> </dl>

 

 