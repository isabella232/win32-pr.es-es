---
title: 'StructuredBuffer:: Load (int, uint) (función)'
description: 'Lee los datos de búfer y devuelve el estado de la operación. | StructuredBuffer:: Load (int, uint) (función)'
ms.assetid: d71c6057-6651-4b70-91cf-892fde6d0188
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
ms.openlocfilehash: 957b85631bbd19742cb7afe52f6bf061de323614
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280032"
---
# <a name="structuredbufferloadintuint-function"></a><span data-ttu-id="4fd0a-105">StructuredBuffer:: Load (int, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="4fd0a-105">StructuredBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="4fd0a-106">Lee los datos de búfer y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="4fd0a-106">Reads buffer data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fd0a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4fd0a-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="4fd0a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4fd0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fd0a-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4fd0a-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fd0a-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="4fd0a-110">Type: **int**</span></span>

<span data-ttu-id="4fd0a-111">Ubicación del búfer.</span><span class="sxs-lookup"><span data-stu-id="4fd0a-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="4fd0a-112">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4fd0a-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fd0a-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4fd0a-113">Type: **uint**</span></span>

<span data-ttu-id="4fd0a-114">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="4fd0a-114">The status of the operation.</span></span> <span data-ttu-id="4fd0a-115">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="4fd0a-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="4fd0a-116">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="4fd0a-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="4fd0a-117">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="4fd0a-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fd0a-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4fd0a-118">Return value</span></span>

<span data-ttu-id="4fd0a-119">Escriba:</span><span class="sxs-lookup"><span data-stu-id="4fd0a-119">Type:</span></span>

<span data-ttu-id="4fd0a-120">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**StructuredBuffer**](sm5-object-structuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="4fd0a-120">The return type matches the type in the declaration for the [**StructuredBuffer**](sm5-object-structuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fd0a-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fd0a-121">Remarks</span></span>

<span data-ttu-id="4fd0a-122">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4fd0a-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4fd0a-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="4fd0a-123">Vertex</span></span> | <span data-ttu-id="4fd0a-124">Casco</span><span class="sxs-lookup"><span data-stu-id="4fd0a-124">Hull</span></span> | <span data-ttu-id="4fd0a-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="4fd0a-125">Domain</span></span> | <span data-ttu-id="4fd0a-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="4fd0a-126">Geometry</span></span> | <span data-ttu-id="4fd0a-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="4fd0a-127">Pixel</span></span> | <span data-ttu-id="4fd0a-128">Compute</span><span class="sxs-lookup"><span data-stu-id="4fd0a-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4fd0a-129">x</span><span class="sxs-lookup"><span data-stu-id="4fd0a-129">x</span></span>     | <span data-ttu-id="4fd0a-130">x</span><span class="sxs-lookup"><span data-stu-id="4fd0a-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4fd0a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fd0a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fd0a-132">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="4fd0a-132">Load methods</span></span>](structuredbuffer-load.md)
</dt> </dl>

 

 
