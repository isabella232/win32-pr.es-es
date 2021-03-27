---
title: 'ByteAddressBuffer:: Load4 (uint) (función)'
description: 'Obtiene cuatro valores. | ByteAddressBuffer:: Load4 (uint) (función)'
ms.assetid: bc74bf29-1c22-4e47-bafc-ecef194f54b8
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
ms.openlocfilehash: 18ce27e7d02a414165aab169e40a6ab14cdd8c4c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986623"
---
# <a name="byteaddressbufferload4uint-function"></a><span data-ttu-id="c61cd-105">ByteAddressBuffer:: Load4 (uint) (función)</span><span class="sxs-lookup"><span data-stu-id="c61cd-105">ByteAddressBuffer::Load4(uint) function</span></span>

<span data-ttu-id="c61cd-106">Obtiene cuatro valores.</span><span class="sxs-lookup"><span data-stu-id="c61cd-106">Gets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c61cd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c61cd-107">Syntax</span></span>

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="c61cd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c61cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c61cd-109">*Dirección* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c61cd-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c61cd-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c61cd-110">Type: **uint**</span></span>

<span data-ttu-id="c61cd-111">Dirección de entrada en bytes, que debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="c61cd-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c61cd-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c61cd-112">Return value</span></span>

<span data-ttu-id="c61cd-113">Tipo: **uint4**</span><span class="sxs-lookup"><span data-stu-id="c61cd-113">Type: **uint4**</span></span>

<span data-ttu-id="c61cd-114">Cuatro valores.</span><span class="sxs-lookup"><span data-stu-id="c61cd-114">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c61cd-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c61cd-115">Remarks</span></span>

<span data-ttu-id="c61cd-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="c61cd-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c61cd-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="c61cd-117">Vertex</span></span> | <span data-ttu-id="c61cd-118">Casco</span><span class="sxs-lookup"><span data-stu-id="c61cd-118">Hull</span></span> | <span data-ttu-id="c61cd-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="c61cd-119">Domain</span></span> | <span data-ttu-id="c61cd-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="c61cd-120">Geometry</span></span> | <span data-ttu-id="c61cd-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="c61cd-121">Pixel</span></span> | <span data-ttu-id="c61cd-122">Compute</span><span class="sxs-lookup"><span data-stu-id="c61cd-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c61cd-123">x</span><span class="sxs-lookup"><span data-stu-id="c61cd-123">x</span></span>      | <span data-ttu-id="c61cd-124">x</span><span class="sxs-lookup"><span data-stu-id="c61cd-124">x</span></span>    | <span data-ttu-id="c61cd-125">x</span><span class="sxs-lookup"><span data-stu-id="c61cd-125">x</span></span>      | <span data-ttu-id="c61cd-126">x</span><span class="sxs-lookup"><span data-stu-id="c61cd-126">x</span></span>        | <span data-ttu-id="c61cd-127">x</span><span class="sxs-lookup"><span data-stu-id="c61cd-127">x</span></span>     | <span data-ttu-id="c61cd-128">x</span><span class="sxs-lookup"><span data-stu-id="c61cd-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c61cd-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c61cd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c61cd-130">Métodos Load4</span><span class="sxs-lookup"><span data-stu-id="c61cd-130">Load4 methods</span></span>](byteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="c61cd-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c61cd-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




