---
title: 'RWByteAddressBuffer:: Store (función)'
description: Establece un valor.
ms.assetid: edfda955-602c-44f4-adc3-77b61c9dcd05
keywords:
- Almacenar la función HLSL
topic_type:
- apiref
api_name:
- Store
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e161e4fb64d09e41c6529954e63b2ace55207e9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104983774"
---
# <a name="store-function"></a><span data-ttu-id="552f2-104">Función de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="552f2-104">Store function</span></span>

<span data-ttu-id="552f2-105">Establece un valor.</span><span class="sxs-lookup"><span data-stu-id="552f2-105">Sets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="552f2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="552f2-106">Syntax</span></span>

``` syntax
void Store(
  in uint address,
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="552f2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="552f2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="552f2-108">*Dirección* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="552f2-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="552f2-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="552f2-109">Type: **uint**</span></span>

<span data-ttu-id="552f2-110">Dirección de entrada en bytes, que debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="552f2-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="552f2-111">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="552f2-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="552f2-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="552f2-112">Type: **uint**</span></span>

<span data-ttu-id="552f2-113">Un valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="552f2-113">One input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="552f2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="552f2-114">Return value</span></span>

<span data-ttu-id="552f2-115">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="552f2-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="552f2-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="552f2-116">Remarks</span></span>

<span data-ttu-id="552f2-117">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="552f2-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="552f2-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="552f2-118">Vertex</span></span> | <span data-ttu-id="552f2-119">Casco</span><span class="sxs-lookup"><span data-stu-id="552f2-119">Hull</span></span> | <span data-ttu-id="552f2-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="552f2-120">Domain</span></span> | <span data-ttu-id="552f2-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="552f2-121">Geometry</span></span> | <span data-ttu-id="552f2-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="552f2-122">Pixel</span></span> | <span data-ttu-id="552f2-123">Compute</span><span class="sxs-lookup"><span data-stu-id="552f2-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="552f2-124">x</span><span class="sxs-lookup"><span data-stu-id="552f2-124">x</span></span>     | <span data-ttu-id="552f2-125">x</span><span class="sxs-lookup"><span data-stu-id="552f2-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="552f2-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="552f2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="552f2-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="552f2-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="552f2-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="552f2-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




