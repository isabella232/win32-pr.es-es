---
title: 'RWByteAddressBuffer:: 2 (función)'
description: Establece dos valores.
ms.assetid: 7b32c84c-9ea2-47ae-a0f3-df6d95249163
keywords:
- 2 de la función HLSL
topic_type:
- apiref
api_name:
- Store2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 574ad7fd59921767308e980e645bac966be87709
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104076992"
---
# <a name="store2-function"></a><span data-ttu-id="7d293-104">Función 2</span><span class="sxs-lookup"><span data-stu-id="7d293-104">Store2 function</span></span>

<span data-ttu-id="7d293-105">Establece dos valores.</span><span class="sxs-lookup"><span data-stu-id="7d293-105">Sets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d293-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d293-106">Syntax</span></span>

``` syntax
void Store2(
  in uint address,
  in uint2 values
);
```

## <a name="parameters"></a><span data-ttu-id="7d293-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d293-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d293-108">*Dirección* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="7d293-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d293-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7d293-109">Type: **uint**</span></span>

<span data-ttu-id="7d293-110">Dirección de entrada en bytes, que debe ser un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="7d293-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="7d293-111">*valores* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="7d293-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d293-112">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="7d293-112">Type: **uint2**</span></span>

<span data-ttu-id="7d293-113">Dos valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="7d293-113">Two input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d293-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d293-114">Return value</span></span>

<span data-ttu-id="7d293-115">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7d293-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d293-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d293-116">Remarks</span></span>

<span data-ttu-id="7d293-117">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="7d293-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7d293-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="7d293-118">Vertex</span></span> | <span data-ttu-id="7d293-119">Casco</span><span class="sxs-lookup"><span data-stu-id="7d293-119">Hull</span></span> | <span data-ttu-id="7d293-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="7d293-120">Domain</span></span> | <span data-ttu-id="7d293-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="7d293-121">Geometry</span></span> | <span data-ttu-id="7d293-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="7d293-122">Pixel</span></span> | <span data-ttu-id="7d293-123">Compute</span><span class="sxs-lookup"><span data-stu-id="7d293-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7d293-124">x</span><span class="sxs-lookup"><span data-stu-id="7d293-124">x</span></span>     | <span data-ttu-id="7d293-125">x</span><span class="sxs-lookup"><span data-stu-id="7d293-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7d293-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d293-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d293-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="7d293-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="7d293-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="7d293-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




