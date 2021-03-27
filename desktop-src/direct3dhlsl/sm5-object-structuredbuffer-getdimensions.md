---
title: 'StructuredBuffer:: Getdimensions ((función)'
description: 'Obtiene las dimensiones de recursos. | StructuredBuffer:: Getdimensions ((función)'
ms.assetid: 423ea79c-4440-4837-b637-95180a1d5019
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
ms.openlocfilehash: 2b3d7c879c77386ddee80a63053711b8ae34ee8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362191"
---
# <a name="structuredbuffergetdimensions-function"></a><span data-ttu-id="4c38d-105">StructuredBuffer:: Getdimensions ((función)</span><span class="sxs-lookup"><span data-stu-id="4c38d-105">StructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="4c38d-106">Obtiene las dimensiones de recursos.</span><span class="sxs-lookup"><span data-stu-id="4c38d-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c38d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c38d-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="4c38d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c38d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c38d-109">*numStructs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4c38d-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c38d-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4c38d-110">Type: **uint**</span></span>

<span data-ttu-id="4c38d-111">El número de estructuras en el recurso.</span><span class="sxs-lookup"><span data-stu-id="4c38d-111">The number of structures in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="4c38d-112">*STRIDE* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4c38d-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c38d-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4c38d-113">Type: **uint**</span></span>

<span data-ttu-id="4c38d-114">Intervalo, en bytes, de cada elemento de la estructura.</span><span class="sxs-lookup"><span data-stu-id="4c38d-114">The stride, in bytes, of each structure element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c38d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c38d-115">Return value</span></span>

<span data-ttu-id="4c38d-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4c38d-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c38d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c38d-117">Remarks</span></span>

<span data-ttu-id="4c38d-118">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4c38d-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4c38d-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="4c38d-119">Vertex</span></span> | <span data-ttu-id="4c38d-120">Casco</span><span class="sxs-lookup"><span data-stu-id="4c38d-120">Hull</span></span> | <span data-ttu-id="4c38d-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="4c38d-121">Domain</span></span> | <span data-ttu-id="4c38d-122">Geometría</span><span class="sxs-lookup"><span data-stu-id="4c38d-122">Geometry</span></span> | <span data-ttu-id="4c38d-123">Píxel</span><span class="sxs-lookup"><span data-stu-id="4c38d-123">Pixel</span></span> | <span data-ttu-id="4c38d-124">Compute</span><span class="sxs-lookup"><span data-stu-id="4c38d-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4c38d-125">x</span><span class="sxs-lookup"><span data-stu-id="4c38d-125">x</span></span>      | <span data-ttu-id="4c38d-126">x</span><span class="sxs-lookup"><span data-stu-id="4c38d-126">x</span></span>    | <span data-ttu-id="4c38d-127">x</span><span class="sxs-lookup"><span data-stu-id="4c38d-127">x</span></span>      | <span data-ttu-id="4c38d-128">x</span><span class="sxs-lookup"><span data-stu-id="4c38d-128">x</span></span>        | <span data-ttu-id="4c38d-129">x</span><span class="sxs-lookup"><span data-stu-id="4c38d-129">x</span></span>     | <span data-ttu-id="4c38d-130">x</span><span class="sxs-lookup"><span data-stu-id="4c38d-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4c38d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c38d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c38d-132">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="4c38d-132">StructuredBuffer</span></span>](sm5-object-structuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="4c38d-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4c38d-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




