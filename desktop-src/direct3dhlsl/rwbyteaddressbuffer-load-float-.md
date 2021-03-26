---
title: 'RWByteAddressBuffer:: Load (int) (función)'
description: 'Obtiene un valor. | RWByteAddressBuffer:: Load (int) (función)'
ms.assetid: C95C865E-E44D-46DC-A076-BD2903758432
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
ms.openlocfilehash: 6efff2363f844e6940b489dd2dda48cbdc0c6b75
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986323"
---
# <a name="rwbyteaddressbufferloadint-function"></a><span data-ttu-id="0ef49-105">RWByteAddressBuffer:: Load (int) (función)</span><span class="sxs-lookup"><span data-stu-id="0ef49-105">RWByteAddressBuffer::Load(int) function</span></span>

<span data-ttu-id="0ef49-106">Obtiene un valor.</span><span class="sxs-lookup"><span data-stu-id="0ef49-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef49-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ef49-107">Syntax</span></span>


``` syntax
uint Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="0ef49-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ef49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ef49-109">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0ef49-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef49-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="0ef49-110">Type: **int**</span></span>

<span data-ttu-id="0ef49-111">Ubicación del búfer.</span><span class="sxs-lookup"><span data-stu-id="0ef49-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ef49-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ef49-112">Return value</span></span>

<span data-ttu-id="0ef49-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="0ef49-113">Type: **uint**</span></span>

<span data-ttu-id="0ef49-114">Un valor.</span><span class="sxs-lookup"><span data-stu-id="0ef49-114">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ef49-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ef49-115">Remarks</span></span>

<span data-ttu-id="0ef49-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="0ef49-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0ef49-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="0ef49-117">Vertex</span></span> | <span data-ttu-id="0ef49-118">Casco</span><span class="sxs-lookup"><span data-stu-id="0ef49-118">Hull</span></span> | <span data-ttu-id="0ef49-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="0ef49-119">Domain</span></span> | <span data-ttu-id="0ef49-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="0ef49-120">Geometry</span></span> | <span data-ttu-id="0ef49-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="0ef49-121">Pixel</span></span> | <span data-ttu-id="0ef49-122">Compute</span><span class="sxs-lookup"><span data-stu-id="0ef49-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="0ef49-123">x</span><span class="sxs-lookup"><span data-stu-id="0ef49-123">x</span></span>     | <span data-ttu-id="0ef49-124">x</span><span class="sxs-lookup"><span data-stu-id="0ef49-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0ef49-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ef49-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef49-126">Cargar métodos</span><span class="sxs-lookup"><span data-stu-id="0ef49-126">Load methods</span></span>](rwbyteaddressbuffer-load.md)
</dt> </dl>

 

 




