---
title: 'ByteAddressBuffer:: Load (int, uint) (función)'
description: Obtiene un valor y el estado de la operación.
ms.assetid: 8F90671B-CEEB-4F8C-9469-D85940568872
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
ms.openlocfilehash: 319daad35da0256a4d36ef4580df62fd4d295854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149777"
---
# <a name="byteaddressbufferloadint-uint-function"></a><span data-ttu-id="607bf-104">ByteAddressBuffer:: Load (int, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="607bf-104">ByteAddressBuffer::Load(int, uint) function</span></span>

<span data-ttu-id="607bf-105">Obtiene un valor y el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="607bf-105">Gets one value and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="607bf-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="607bf-106">Syntax</span></span>

``` syntax
uint Load(
  in  int Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="607bf-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="607bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="607bf-108">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="607bf-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="607bf-109">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="607bf-109">Type: **int**</span></span>

<span data-ttu-id="607bf-110">Dirección de entrada en bytes, que debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="607bf-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="607bf-111">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="607bf-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="607bf-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="607bf-112">Type: **uint**</span></span>

<span data-ttu-id="607bf-113">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="607bf-113">The status of the operation.</span></span> <span data-ttu-id="607bf-114">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="607bf-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="607bf-115">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="607bf-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="607bf-116">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="607bf-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="607bf-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="607bf-117">Return value</span></span>

<span data-ttu-id="607bf-118">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="607bf-118">Type: **uint**</span></span>

<span data-ttu-id="607bf-119">Un valor.</span><span class="sxs-lookup"><span data-stu-id="607bf-119">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="607bf-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="607bf-120">Remarks</span></span>

<span data-ttu-id="607bf-121">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="607bf-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="607bf-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="607bf-122">Vertex</span></span> | <span data-ttu-id="607bf-123">Casco</span><span class="sxs-lookup"><span data-stu-id="607bf-123">Hull</span></span> | <span data-ttu-id="607bf-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="607bf-124">Domain</span></span> | <span data-ttu-id="607bf-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="607bf-125">Geometry</span></span> | <span data-ttu-id="607bf-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="607bf-126">Pixel</span></span> | <span data-ttu-id="607bf-127">Compute</span><span class="sxs-lookup"><span data-stu-id="607bf-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="607bf-128">x</span><span class="sxs-lookup"><span data-stu-id="607bf-128">x</span></span>      | <span data-ttu-id="607bf-129">x</span><span class="sxs-lookup"><span data-stu-id="607bf-129">x</span></span>    | <span data-ttu-id="607bf-130">x</span><span class="sxs-lookup"><span data-stu-id="607bf-130">x</span></span>      | <span data-ttu-id="607bf-131">x</span><span class="sxs-lookup"><span data-stu-id="607bf-131">x</span></span>        | <span data-ttu-id="607bf-132">x</span><span class="sxs-lookup"><span data-stu-id="607bf-132">x</span></span>     | <span data-ttu-id="607bf-133">x</span><span class="sxs-lookup"><span data-stu-id="607bf-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="607bf-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="607bf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="607bf-135">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="607bf-135">Load methods</span></span>](byteaddressbuffer-load.md)
</dt> <dt>

[<span data-ttu-id="607bf-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="607bf-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 
