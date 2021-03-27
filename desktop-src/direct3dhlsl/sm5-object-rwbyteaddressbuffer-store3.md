---
title: 'RWByteAddressBuffer:: Store3 (función)'
description: Establece tres valores.
ms.assetid: eaf12b5a-c9c6-413a-9646-3d14e7825460
keywords:
- Store3 de función HLSL
topic_type:
- apiref
api_name:
- Store3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd27684c3adf506e086fb17f789272c6b263ab20
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104358375"
---
# <a name="store3-function"></a><span data-ttu-id="2f5fd-104">Store3 función)</span><span class="sxs-lookup"><span data-stu-id="2f5fd-104">Store3 function</span></span>

<span data-ttu-id="2f5fd-105">Establece tres valores.</span><span class="sxs-lookup"><span data-stu-id="2f5fd-105">Sets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f5fd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f5fd-106">Syntax</span></span>

``` syntax
void Store3(
  in uint address,
  in uint3 values
);
```

## <a name="parameters"></a><span data-ttu-id="2f5fd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f5fd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f5fd-108">*Dirección* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2f5fd-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5fd-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2f5fd-109">Type: **uint**</span></span>

<span data-ttu-id="2f5fd-110">Dirección de entrada en bytes, que debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="2f5fd-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="2f5fd-111">*valores* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2f5fd-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5fd-112">Tipo: **UInt3**</span><span class="sxs-lookup"><span data-stu-id="2f5fd-112">Type: **uint3**</span></span>

<span data-ttu-id="2f5fd-113">Tres valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="2f5fd-113">Three input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f5fd-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f5fd-114">Return value</span></span>

<span data-ttu-id="2f5fd-115">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2f5fd-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f5fd-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f5fd-116">Remarks</span></span>

<span data-ttu-id="2f5fd-117">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2f5fd-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2f5fd-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="2f5fd-118">Vertex</span></span> | <span data-ttu-id="2f5fd-119">Casco</span><span class="sxs-lookup"><span data-stu-id="2f5fd-119">Hull</span></span> | <span data-ttu-id="2f5fd-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="2f5fd-120">Domain</span></span> | <span data-ttu-id="2f5fd-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="2f5fd-121">Geometry</span></span> | <span data-ttu-id="2f5fd-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="2f5fd-122">Pixel</span></span> | <span data-ttu-id="2f5fd-123">Compute</span><span class="sxs-lookup"><span data-stu-id="2f5fd-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="2f5fd-124">x</span><span class="sxs-lookup"><span data-stu-id="2f5fd-124">x</span></span>     | <span data-ttu-id="2f5fd-125">x</span><span class="sxs-lookup"><span data-stu-id="2f5fd-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2f5fd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f5fd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f5fd-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="2f5fd-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="2f5fd-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2f5fd-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




