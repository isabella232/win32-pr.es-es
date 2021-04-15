---
title: 'AppendStructuredBuffer:: Getdimensions ((función)'
description: 'Obtiene las dimensiones de recursos. | AppendStructuredBuffer:: Getdimensions ((función)'
ms.assetid: 41ed86d5-25c0-48bd-add9-792eb89605c3
keywords:
- Getdimensions (de función HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 93db905ae40f1bec7488eca292f4ea44d87950d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986207"
---
# <a name="appendstructuredbuffergetdimensions-function"></a><span data-ttu-id="7acc7-105">AppendStructuredBuffer:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="7acc7-105">AppendStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="7acc7-106">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="7acc7-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7acc7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7acc7-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="7acc7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7acc7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7acc7-109">*numStructs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7acc7-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7acc7-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7acc7-110">Type: **uint**</span></span>

<span data-ttu-id="7acc7-111">El número de estructuras.</span><span class="sxs-lookup"><span data-stu-id="7acc7-111">The number of structures.</span></span>

</dd> <dt>

<span data-ttu-id="7acc7-112">*STRIDE* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7acc7-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7acc7-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7acc7-113">Type: **uint**</span></span>

<span data-ttu-id="7acc7-114">Número de bytes de cada elemento.</span><span class="sxs-lookup"><span data-stu-id="7acc7-114">The number of bytes in each element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7acc7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7acc7-115">Return value</span></span>

<span data-ttu-id="7acc7-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7acc7-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7acc7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7acc7-117">Remarks</span></span>

<span data-ttu-id="7acc7-118">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="7acc7-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7acc7-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="7acc7-119">Vertex</span></span> | <span data-ttu-id="7acc7-120">Casco</span><span class="sxs-lookup"><span data-stu-id="7acc7-120">Hull</span></span> | <span data-ttu-id="7acc7-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="7acc7-121">Domain</span></span> | <span data-ttu-id="7acc7-122">Geometría</span><span class="sxs-lookup"><span data-stu-id="7acc7-122">Geometry</span></span> | <span data-ttu-id="7acc7-123">Píxel</span><span class="sxs-lookup"><span data-stu-id="7acc7-123">Pixel</span></span> | <span data-ttu-id="7acc7-124">Compute</span><span class="sxs-lookup"><span data-stu-id="7acc7-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7acc7-125">x</span><span class="sxs-lookup"><span data-stu-id="7acc7-125">x</span></span>      | <span data-ttu-id="7acc7-126">x</span><span class="sxs-lookup"><span data-stu-id="7acc7-126">x</span></span>    | <span data-ttu-id="7acc7-127">x</span><span class="sxs-lookup"><span data-stu-id="7acc7-127">x</span></span>      | <span data-ttu-id="7acc7-128">x</span><span class="sxs-lookup"><span data-stu-id="7acc7-128">x</span></span>        | <span data-ttu-id="7acc7-129">x</span><span class="sxs-lookup"><span data-stu-id="7acc7-129">x</span></span>     | <span data-ttu-id="7acc7-130">x</span><span class="sxs-lookup"><span data-stu-id="7acc7-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7acc7-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7acc7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7acc7-132">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="7acc7-132">AppendStructuredBuffer</span></span>](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="7acc7-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="7acc7-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




