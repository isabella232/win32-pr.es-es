---
title: 'ByteAddressBuffer:: Load3 (uint) (función)'
description: 'Obtiene tres valores. | ByteAddressBuffer:: Load3 (uint) (función)'
ms.assetid: 79afeb36-e0e7-44a2-b252-8e3577f4c1a5
keywords:
- Load3 de función HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e3975d454fcbb8c5dfa8cdef8d7f5718143546f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986626"
---
# <a name="byteaddressbufferload3uint-function"></a><span data-ttu-id="74f3c-105">ByteAddressBuffer:: Load3 (uint) (función)</span><span class="sxs-lookup"><span data-stu-id="74f3c-105">ByteAddressBuffer::Load3(uint) function</span></span>

<span data-ttu-id="74f3c-106">Obtiene tres valores.</span><span class="sxs-lookup"><span data-stu-id="74f3c-106">Gets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="74f3c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74f3c-107">Syntax</span></span>

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="74f3c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74f3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74f3c-109">*Dirección* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="74f3c-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74f3c-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="74f3c-110">Type: **uint**</span></span>

<span data-ttu-id="74f3c-111">Dirección de entrada en bytes, que debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="74f3c-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74f3c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74f3c-112">Return value</span></span>

<span data-ttu-id="74f3c-113">Tipo: **UInt3**</span><span class="sxs-lookup"><span data-stu-id="74f3c-113">Type: **uint3**</span></span>

<span data-ttu-id="74f3c-114">Tres valores.</span><span class="sxs-lookup"><span data-stu-id="74f3c-114">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="74f3c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74f3c-115">Remarks</span></span>

<span data-ttu-id="74f3c-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="74f3c-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="74f3c-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="74f3c-117">Vertex</span></span> | <span data-ttu-id="74f3c-118">Casco</span><span class="sxs-lookup"><span data-stu-id="74f3c-118">Hull</span></span> | <span data-ttu-id="74f3c-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="74f3c-119">Domain</span></span> | <span data-ttu-id="74f3c-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="74f3c-120">Geometry</span></span> | <span data-ttu-id="74f3c-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="74f3c-121">Pixel</span></span> | <span data-ttu-id="74f3c-122">Compute</span><span class="sxs-lookup"><span data-stu-id="74f3c-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="74f3c-123">x</span><span class="sxs-lookup"><span data-stu-id="74f3c-123">x</span></span>      | <span data-ttu-id="74f3c-124">x</span><span class="sxs-lookup"><span data-stu-id="74f3c-124">x</span></span>    | <span data-ttu-id="74f3c-125">x</span><span class="sxs-lookup"><span data-stu-id="74f3c-125">x</span></span>      | <span data-ttu-id="74f3c-126">x</span><span class="sxs-lookup"><span data-stu-id="74f3c-126">x</span></span>        | <span data-ttu-id="74f3c-127">x</span><span class="sxs-lookup"><span data-stu-id="74f3c-127">x</span></span>     | <span data-ttu-id="74f3c-128">x</span><span class="sxs-lookup"><span data-stu-id="74f3c-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="74f3c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="74f3c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74f3c-130">Métodos Load3</span><span class="sxs-lookup"><span data-stu-id="74f3c-130">Load3 methods</span></span>](byteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="74f3c-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="74f3c-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




