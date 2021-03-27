---
title: 'RWByteAddressBuffer:: Load2 (uint) (función)'
description: 'Obtiene dos valores. | RWByteAddressBuffer:: Load2 (uint) (función)'
ms.assetid: a00396cb-e68d-479e-ab3f-4c52f2cfc3bc
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
ms.openlocfilehash: 7595477448deb087b94664100710690a6f386a94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986701"
---
# <a name="rwbyteaddressbufferload2uint-function"></a><span data-ttu-id="11241-105">RWByteAddressBuffer:: Load2 (uint) (función)</span><span class="sxs-lookup"><span data-stu-id="11241-105">RWByteAddressBuffer::Load2(uint) function</span></span>

<span data-ttu-id="11241-106">Obtiene dos valores.</span><span class="sxs-lookup"><span data-stu-id="11241-106">Gets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="11241-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11241-107">Syntax</span></span>

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="11241-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11241-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11241-109">*Dirección* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="11241-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11241-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="11241-110">Type: **uint**</span></span>

<span data-ttu-id="11241-111">Dirección de entrada en bytes, que debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="11241-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11241-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11241-112">Return value</span></span>

<span data-ttu-id="11241-113">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="11241-113">Type: **uint2**</span></span>

<span data-ttu-id="11241-114">Dos valores.</span><span class="sxs-lookup"><span data-stu-id="11241-114">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="11241-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11241-115">Remarks</span></span>

<span data-ttu-id="11241-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="11241-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="11241-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="11241-117">Vertex</span></span> | <span data-ttu-id="11241-118">Casco</span><span class="sxs-lookup"><span data-stu-id="11241-118">Hull</span></span> | <span data-ttu-id="11241-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="11241-119">Domain</span></span> | <span data-ttu-id="11241-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="11241-120">Geometry</span></span> | <span data-ttu-id="11241-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="11241-121">Pixel</span></span> | <span data-ttu-id="11241-122">Compute</span><span class="sxs-lookup"><span data-stu-id="11241-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="11241-123">x</span><span class="sxs-lookup"><span data-stu-id="11241-123">x</span></span>     | <span data-ttu-id="11241-124">x</span><span class="sxs-lookup"><span data-stu-id="11241-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="11241-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="11241-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11241-126">Métodos Load2</span><span class="sxs-lookup"><span data-stu-id="11241-126">Load2 methods</span></span>](rwbyteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="11241-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="11241-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




