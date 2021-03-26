---
title: 'RWByteAddressBuffer:: Load (int, uint) (función)'
description: Obtiene un valor y devuelve el estado de la operación.
ms.assetid: E3FD0FFA-6A9B-4B44-A90D-47270326F9BA
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
ms.openlocfilehash: 71f142d35ae8be3800ccf85b5e8114d5e85c44ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103904924"
---
# <a name="rwbyteaddressbufferloadintuint-function"></a><span data-ttu-id="ccf11-104">RWByteAddressBuffer:: Load (int, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="ccf11-104">RWByteAddressBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="ccf11-105">Obtiene un valor y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ccf11-105">Gets one value and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf11-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ccf11-106">Syntax</span></span>


``` syntax
uint Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="ccf11-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ccf11-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccf11-108">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ccf11-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf11-109">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="ccf11-109">Type: **int**</span></span>

<span data-ttu-id="ccf11-110">Ubicación del búfer.</span><span class="sxs-lookup"><span data-stu-id="ccf11-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ccf11-111">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ccf11-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf11-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ccf11-112">Type: **uint**</span></span>

<span data-ttu-id="ccf11-113">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ccf11-113">The status of the operation.</span></span> <span data-ttu-id="ccf11-114">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="ccf11-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="ccf11-115">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="ccf11-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="ccf11-116">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="ccf11-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccf11-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ccf11-117">Return value</span></span>

<span data-ttu-id="ccf11-118">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ccf11-118">Type: **uint**</span></span>

<span data-ttu-id="ccf11-119">Un valor.</span><span class="sxs-lookup"><span data-stu-id="ccf11-119">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccf11-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ccf11-120">Remarks</span></span>

<span data-ttu-id="ccf11-121">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="ccf11-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ccf11-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="ccf11-122">Vertex</span></span> | <span data-ttu-id="ccf11-123">Casco</span><span class="sxs-lookup"><span data-stu-id="ccf11-123">Hull</span></span> | <span data-ttu-id="ccf11-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="ccf11-124">Domain</span></span> | <span data-ttu-id="ccf11-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="ccf11-125">Geometry</span></span> | <span data-ttu-id="ccf11-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="ccf11-126">Pixel</span></span> | <span data-ttu-id="ccf11-127">Compute</span><span class="sxs-lookup"><span data-stu-id="ccf11-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="ccf11-128">x</span><span class="sxs-lookup"><span data-stu-id="ccf11-128">x</span></span>     | <span data-ttu-id="ccf11-129">x</span><span class="sxs-lookup"><span data-stu-id="ccf11-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ccf11-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccf11-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf11-131">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="ccf11-131">Load methods</span></span>](rwbyteaddressbuffer-load.md)
</dt> </dl>

 

 
