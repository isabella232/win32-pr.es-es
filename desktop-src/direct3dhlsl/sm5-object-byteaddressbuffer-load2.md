---
title: 'ByteAddressBuffer:: Load2 (uint) (función)'
description: 'Obtiene dos valores. | ByteAddressBuffer:: Load2 (uint) (función)'
ms.assetid: 696ce310-4d65-4382-97ec-046160197c67
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
ms.openlocfilehash: 78204fc3d41daf07a54974fbf103685e718ab79d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820511"
---
# <a name="byteaddressbufferload2uint-function"></a><span data-ttu-id="f6ccc-105">ByteAddressBuffer:: Load2 (uint) (función)</span><span class="sxs-lookup"><span data-stu-id="f6ccc-105">ByteAddressBuffer::Load2(uint) function</span></span>

<span data-ttu-id="f6ccc-106">Obtiene dos valores.</span><span class="sxs-lookup"><span data-stu-id="f6ccc-106">Gets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6ccc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6ccc-107">Syntax</span></span>

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="f6ccc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6ccc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6ccc-109">*Dirección* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f6ccc-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ccc-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f6ccc-110">Type: **uint**</span></span>

<span data-ttu-id="f6ccc-111">Dirección de entrada en bytes, que debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="f6ccc-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6ccc-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6ccc-112">Return value</span></span>

<span data-ttu-id="f6ccc-113">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="f6ccc-113">Type: **uint2**</span></span>

<span data-ttu-id="f6ccc-114">Dos valores.</span><span class="sxs-lookup"><span data-stu-id="f6ccc-114">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6ccc-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6ccc-115">Remarks</span></span>

<span data-ttu-id="f6ccc-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="f6ccc-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f6ccc-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="f6ccc-117">Vertex</span></span> | <span data-ttu-id="f6ccc-118">Casco</span><span class="sxs-lookup"><span data-stu-id="f6ccc-118">Hull</span></span> | <span data-ttu-id="f6ccc-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="f6ccc-119">Domain</span></span> | <span data-ttu-id="f6ccc-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="f6ccc-120">Geometry</span></span> | <span data-ttu-id="f6ccc-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="f6ccc-121">Pixel</span></span> | <span data-ttu-id="f6ccc-122">Compute</span><span class="sxs-lookup"><span data-stu-id="f6ccc-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f6ccc-123">x</span><span class="sxs-lookup"><span data-stu-id="f6ccc-123">x</span></span>      | <span data-ttu-id="f6ccc-124">x</span><span class="sxs-lookup"><span data-stu-id="f6ccc-124">x</span></span>    | <span data-ttu-id="f6ccc-125">x</span><span class="sxs-lookup"><span data-stu-id="f6ccc-125">x</span></span>      | <span data-ttu-id="f6ccc-126">x</span><span class="sxs-lookup"><span data-stu-id="f6ccc-126">x</span></span>        | <span data-ttu-id="f6ccc-127">x</span><span class="sxs-lookup"><span data-stu-id="f6ccc-127">x</span></span>     | <span data-ttu-id="f6ccc-128">x</span><span class="sxs-lookup"><span data-stu-id="f6ccc-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f6ccc-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6ccc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6ccc-130">Métodos Load2</span><span class="sxs-lookup"><span data-stu-id="f6ccc-130">Load2 methods</span></span>](byteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="f6ccc-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f6ccc-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




