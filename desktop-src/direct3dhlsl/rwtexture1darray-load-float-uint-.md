---
title: 'RWTexture1DArray:: Load (int, uint) (función)'
description: 'Lee los datos de textura y devuelve el estado de la operación. | RWTexture1DArray:: Load (int, uint) (función)'
ms.assetid: EF1D51CC-E037-4E04-9DD6-6A9C5950E5B5
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
ms.openlocfilehash: 5a46dde9b75d3194cc081409fe2b450c5453d7c1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986279"
---
# <a name="rwtexture1darrayloadintuint-function"></a><span data-ttu-id="d5791-105">RWTexture1DArray:: Load (int, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="d5791-105">RWTexture1DArray::Load(int,uint) function</span></span>

<span data-ttu-id="d5791-106">Lee los datos de textura y devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d5791-106">Reads texture data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5791-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5791-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="d5791-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5791-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5791-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d5791-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5791-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="d5791-110">Type: **int**</span></span>

<span data-ttu-id="d5791-111">Ubicación de la textura.</span><span class="sxs-lookup"><span data-stu-id="d5791-111">The location of the texture.</span></span>

</dd> <dt>

<span data-ttu-id="d5791-112">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d5791-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5791-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d5791-113">Type: **uint**</span></span>

<span data-ttu-id="d5791-114">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d5791-114">The status of the operation.</span></span> <span data-ttu-id="d5791-115">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="d5791-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="d5791-116">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="d5791-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="d5791-117">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="d5791-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5791-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5791-118">Return value</span></span>

<span data-ttu-id="d5791-119">Escriba:</span><span class="sxs-lookup"><span data-stu-id="d5791-119">Type:</span></span>

<span data-ttu-id="d5791-120">El tipo de valor devuelto coincide con el tipo en la declaración del objeto [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) .</span><span class="sxs-lookup"><span data-stu-id="d5791-120">The return type matches the type in the declaration for the [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5791-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5791-121">Remarks</span></span>

<span data-ttu-id="d5791-122">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="d5791-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d5791-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="d5791-123">Vertex</span></span> | <span data-ttu-id="d5791-124">Casco</span><span class="sxs-lookup"><span data-stu-id="d5791-124">Hull</span></span> | <span data-ttu-id="d5791-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="d5791-125">Domain</span></span> | <span data-ttu-id="d5791-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="d5791-126">Geometry</span></span> | <span data-ttu-id="d5791-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="d5791-127">Pixel</span></span> | <span data-ttu-id="d5791-128">Compute</span><span class="sxs-lookup"><span data-stu-id="d5791-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d5791-129">x</span><span class="sxs-lookup"><span data-stu-id="d5791-129">x</span></span>     | <span data-ttu-id="d5791-130">x</span><span class="sxs-lookup"><span data-stu-id="d5791-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d5791-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5791-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5791-132">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="d5791-132">Load methods</span></span>](rwtexture1darray-load.md)
</dt> </dl>

 

 
