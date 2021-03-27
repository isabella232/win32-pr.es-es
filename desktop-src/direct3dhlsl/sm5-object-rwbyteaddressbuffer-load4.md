---
title: 'RWByteAddressBuffer:: Load4 (uint) (función)'
description: 'Obtiene cuatro valores. | RWByteAddressBuffer:: Load4 (uint) (función)'
ms.assetid: b46cd119-75be-4c2d-82f9-5dcabd7e4400
keywords:
- Load4 de función HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2bdc5adf3b3d95c68871a14c9382891a59ad52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986724"
---
# <a name="rwbyteaddressbufferload4uint-function"></a><span data-ttu-id="36240-105">RWByteAddressBuffer:: Load4 (uint) (función)</span><span class="sxs-lookup"><span data-stu-id="36240-105">RWByteAddressBuffer::Load4(uint) function</span></span>

<span data-ttu-id="36240-106">Obtiene cuatro valores.</span><span class="sxs-lookup"><span data-stu-id="36240-106">Gets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="36240-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36240-107">Syntax</span></span>

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="36240-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36240-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36240-109">*Dirección* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="36240-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36240-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="36240-110">Type: **uint**</span></span>

<span data-ttu-id="36240-111">Dirección de entrada en bytes, que debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="36240-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36240-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36240-112">Return value</span></span>

<span data-ttu-id="36240-113">Tipo: **uint4**</span><span class="sxs-lookup"><span data-stu-id="36240-113">Type: **uint4**</span></span>

<span data-ttu-id="36240-114">Cuatro valores.</span><span class="sxs-lookup"><span data-stu-id="36240-114">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="36240-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36240-115">Remarks</span></span>

<span data-ttu-id="36240-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="36240-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="36240-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="36240-117">Vertex</span></span> | <span data-ttu-id="36240-118">Casco</span><span class="sxs-lookup"><span data-stu-id="36240-118">Hull</span></span> | <span data-ttu-id="36240-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="36240-119">Domain</span></span> | <span data-ttu-id="36240-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="36240-120">Geometry</span></span> | <span data-ttu-id="36240-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="36240-121">Pixel</span></span> | <span data-ttu-id="36240-122">Compute</span><span class="sxs-lookup"><span data-stu-id="36240-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="36240-123">x</span><span class="sxs-lookup"><span data-stu-id="36240-123">x</span></span>     | <span data-ttu-id="36240-124">x</span><span class="sxs-lookup"><span data-stu-id="36240-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="36240-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="36240-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36240-126">Métodos Load4</span><span class="sxs-lookup"><span data-stu-id="36240-126">Load4 methods</span></span>](rwbyteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="36240-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="36240-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




