---
title: 'RWByteAddressBuffer:: Store4 (función)'
description: Establece cuatro valores.
ms.assetid: 261dd270-79a7-4566-9fbd-52bd8dc3e1bf
keywords:
- Store4 de función HLSL
topic_type:
- apiref
api_name:
- Store4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 219cd04e4f68ad6f0d16d964e6685c558fed98b1
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104419791"
---
# <a name="store4-function"></a><span data-ttu-id="76148-104">Store4 función)</span><span class="sxs-lookup"><span data-stu-id="76148-104">Store4 function</span></span>

<span data-ttu-id="76148-105">Establece cuatro valores.</span><span class="sxs-lookup"><span data-stu-id="76148-105">Sets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="76148-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76148-106">Syntax</span></span>

``` syntax
void Store4(
  in uint address,
  in uint4 values
);
```

## <a name="parameters"></a><span data-ttu-id="76148-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76148-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76148-108">*Dirección* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="76148-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76148-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="76148-109">Type: **uint**</span></span>

<span data-ttu-id="76148-110">Dirección de entrada en bytes, que debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="76148-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="76148-111">*valores* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="76148-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76148-112">Tipo: **uint4**</span><span class="sxs-lookup"><span data-stu-id="76148-112">Type: **uint4**</span></span>

<span data-ttu-id="76148-113">Cuatro valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="76148-113">Four input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76148-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76148-114">Return value</span></span>

<span data-ttu-id="76148-115">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="76148-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="76148-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76148-116">Remarks</span></span>

<span data-ttu-id="76148-117">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="76148-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="76148-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="76148-118">Vertex</span></span> | <span data-ttu-id="76148-119">Casco</span><span class="sxs-lookup"><span data-stu-id="76148-119">Hull</span></span> | <span data-ttu-id="76148-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="76148-120">Domain</span></span> | <span data-ttu-id="76148-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="76148-121">Geometry</span></span> | <span data-ttu-id="76148-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="76148-122">Pixel</span></span> | <span data-ttu-id="76148-123">Compute</span><span class="sxs-lookup"><span data-stu-id="76148-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="76148-124">x</span><span class="sxs-lookup"><span data-stu-id="76148-124">x</span></span>     | <span data-ttu-id="76148-125">x</span><span class="sxs-lookup"><span data-stu-id="76148-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="76148-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="76148-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76148-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="76148-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="76148-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="76148-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




