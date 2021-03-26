---
title: 'RWStructuredBuffer:: Getdimensions ((función)'
description: 'Obtiene las dimensiones de recursos. | RWStructuredBuffer:: Getdimensions ((función)'
ms.assetid: 842b3d21-2e2b-4906-93ee-0252b2e8cf85
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
ms.openlocfilehash: 0e3868f33e372472999c29bffdd8e12bc8ef09b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986202"
---
# <a name="rwstructuredbuffergetdimensions-function"></a><span data-ttu-id="7f52f-105">RWStructuredBuffer:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="7f52f-105">RWStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="7f52f-106">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="7f52f-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f52f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f52f-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="7f52f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f52f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f52f-109">*numStructs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7f52f-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f52f-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7f52f-110">Type: **uint**</span></span>

<span data-ttu-id="7f52f-111">El número de estructuras en el recurso.</span><span class="sxs-lookup"><span data-stu-id="7f52f-111">The number of structures in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="7f52f-112">*STRIDE* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7f52f-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f52f-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7f52f-113">Type: **uint**</span></span>

<span data-ttu-id="7f52f-114">Intervalo, en bytes, de cada elemento de la estructura.</span><span class="sxs-lookup"><span data-stu-id="7f52f-114">The stride, in bytes, of each structure element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f52f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f52f-115">Return value</span></span>

<span data-ttu-id="7f52f-116">Nada</span><span class="sxs-lookup"><span data-stu-id="7f52f-116">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="7f52f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f52f-117">Remarks</span></span>

<span data-ttu-id="7f52f-118">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="7f52f-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7f52f-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="7f52f-119">Vertex</span></span> | <span data-ttu-id="7f52f-120">Casco</span><span class="sxs-lookup"><span data-stu-id="7f52f-120">Hull</span></span> | <span data-ttu-id="7f52f-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="7f52f-121">Domain</span></span> | <span data-ttu-id="7f52f-122">Geometría</span><span class="sxs-lookup"><span data-stu-id="7f52f-122">Geometry</span></span> | <span data-ttu-id="7f52f-123">Píxel</span><span class="sxs-lookup"><span data-stu-id="7f52f-123">Pixel</span></span> | <span data-ttu-id="7f52f-124">Compute</span><span class="sxs-lookup"><span data-stu-id="7f52f-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7f52f-125">x</span><span class="sxs-lookup"><span data-stu-id="7f52f-125">x</span></span>     | <span data-ttu-id="7f52f-126">x</span><span class="sxs-lookup"><span data-stu-id="7f52f-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7f52f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f52f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f52f-128">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="7f52f-128">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="7f52f-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="7f52f-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




