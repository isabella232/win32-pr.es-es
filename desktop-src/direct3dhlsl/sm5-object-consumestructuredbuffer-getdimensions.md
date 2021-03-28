---
title: 'ConsumeStructuredBuffer:: Getdimensions ((función)'
description: 'Obtiene las dimensiones de recursos. | ConsumeStructuredBuffer:: Getdimensions ((función)'
ms.assetid: 0710a4fb-23b0-4b19-b9ed-21bbb9874d33
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
ms.openlocfilehash: a204ed44c90c60b327ceb201037c6758763b3a05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998025"
---
# <a name="consumestructuredbuffergetdimensions-function"></a><span data-ttu-id="f0ead-105">ConsumeStructuredBuffer:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="f0ead-105">ConsumeStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="f0ead-106">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="f0ead-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ead-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0ead-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="f0ead-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0ead-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0ead-109">*numStructs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f0ead-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ead-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f0ead-110">Type: **uint**</span></span>

<span data-ttu-id="f0ead-111">El número de estructuras.</span><span class="sxs-lookup"><span data-stu-id="f0ead-111">The number of structures.</span></span>

</dd> <dt>

<span data-ttu-id="f0ead-112">*STRIDE* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f0ead-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ead-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f0ead-113">Type: **uint**</span></span>

<span data-ttu-id="f0ead-114">Intervalo, en bytes, de cada elemento.</span><span class="sxs-lookup"><span data-stu-id="f0ead-114">The stride, in bytes, of each element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0ead-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0ead-115">Return value</span></span>

<span data-ttu-id="f0ead-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f0ead-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0ead-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0ead-117">Remarks</span></span>

<span data-ttu-id="f0ead-118">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="f0ead-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f0ead-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="f0ead-119">Vertex</span></span> | <span data-ttu-id="f0ead-120">Casco</span><span class="sxs-lookup"><span data-stu-id="f0ead-120">Hull</span></span> | <span data-ttu-id="f0ead-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="f0ead-121">Domain</span></span> | <span data-ttu-id="f0ead-122">Geometría</span><span class="sxs-lookup"><span data-stu-id="f0ead-122">Geometry</span></span> | <span data-ttu-id="f0ead-123">Píxel</span><span class="sxs-lookup"><span data-stu-id="f0ead-123">Pixel</span></span> | <span data-ttu-id="f0ead-124">Compute</span><span class="sxs-lookup"><span data-stu-id="f0ead-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f0ead-125">x</span><span class="sxs-lookup"><span data-stu-id="f0ead-125">x</span></span>      | <span data-ttu-id="f0ead-126">x</span><span class="sxs-lookup"><span data-stu-id="f0ead-126">x</span></span>    | <span data-ttu-id="f0ead-127">x</span><span class="sxs-lookup"><span data-stu-id="f0ead-127">x</span></span>      | <span data-ttu-id="f0ead-128">x</span><span class="sxs-lookup"><span data-stu-id="f0ead-128">x</span></span>        | <span data-ttu-id="f0ead-129">x</span><span class="sxs-lookup"><span data-stu-id="f0ead-129">x</span></span>     | <span data-ttu-id="f0ead-130">x</span><span class="sxs-lookup"><span data-stu-id="f0ead-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f0ead-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0ead-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ead-132">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="f0ead-132">ConsumeStructuredBuffer</span></span>](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="f0ead-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f0ead-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




