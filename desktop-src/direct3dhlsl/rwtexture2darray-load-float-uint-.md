---
title: 'RWTexture2DArray:: Load (int, uint) (función)'
description: 'Lee los datos de textura y devuelve el estado de la operación. | RWTexture2DArray:: Load (int, uint) (función)'
ms.assetid: 97D6E36A-1613-43BA-92C1-3034E0F344F0
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
ms.openlocfilehash: 969aa0a4efa62f7072c759a1f2188e4d210d8649
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986482"
---
# <a name="rwtexture2darrayloadintuint-function"></a><span data-ttu-id="dda4e-105">RWTexture2DArray:: Load (int, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="dda4e-105">RWTexture2DArray::Load(int,uint) function</span></span>

<span data-ttu-id="dda4e-106">Lee los datos de textura y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="dda4e-106">Reads texture data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="dda4e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dda4e-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="dda4e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dda4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dda4e-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="dda4e-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dda4e-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="dda4e-110">Type: **int**</span></span>

<span data-ttu-id="dda4e-111">Ubicación de la textura.</span><span class="sxs-lookup"><span data-stu-id="dda4e-111">The location of the texture.</span></span>

</dd> <dt>

<span data-ttu-id="dda4e-112">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="dda4e-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dda4e-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="dda4e-113">Type: **uint**</span></span>

<span data-ttu-id="dda4e-114">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="dda4e-114">The status of the operation.</span></span> <span data-ttu-id="dda4e-115">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="dda4e-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="dda4e-116">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="dda4e-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="dda4e-117">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="dda4e-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dda4e-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dda4e-118">Return value</span></span>

<span data-ttu-id="dda4e-119">Escriba:</span><span class="sxs-lookup"><span data-stu-id="dda4e-119">Type:</span></span>

<span data-ttu-id="dda4e-120">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) .</span><span class="sxs-lookup"><span data-stu-id="dda4e-120">The return type matches the type in the declaration for the [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dda4e-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dda4e-121">Remarks</span></span>

<span data-ttu-id="dda4e-122">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="dda4e-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="dda4e-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="dda4e-123">Vertex</span></span> | <span data-ttu-id="dda4e-124">Casco</span><span class="sxs-lookup"><span data-stu-id="dda4e-124">Hull</span></span> | <span data-ttu-id="dda4e-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="dda4e-125">Domain</span></span> | <span data-ttu-id="dda4e-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="dda4e-126">Geometry</span></span> | <span data-ttu-id="dda4e-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="dda4e-127">Pixel</span></span> | <span data-ttu-id="dda4e-128">Compute</span><span class="sxs-lookup"><span data-stu-id="dda4e-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="dda4e-129">x</span><span class="sxs-lookup"><span data-stu-id="dda4e-129">x</span></span>     | <span data-ttu-id="dda4e-130">x</span><span class="sxs-lookup"><span data-stu-id="dda4e-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="dda4e-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="dda4e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dda4e-132">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="dda4e-132">Load methods</span></span>](rwtexture2darray-load.md)
</dt> </dl>

 

 
