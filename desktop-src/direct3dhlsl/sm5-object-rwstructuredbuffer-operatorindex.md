---
title: 'RWStructuredBuffer:: Operator (función)'
description: 'Devuelve una variable de recurso. | RWStructuredBuffer:: Operator (función)'
ms.assetid: e821b60e-38db-463f-b0c6-47f2a4c9ccee
keywords:
- Función de operador HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e915d7862f7994d3b438bf3255ee836ede4b3d7d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547534"
---
# <a name="rwstructuredbufferoperator--function"></a><span data-ttu-id="b0986-105">RWStructuredBuffer:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="b0986-105">RWStructuredBuffer::Operator  function</span></span>

<span data-ttu-id="b0986-106">Devuelve una variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="b0986-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0986-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0986-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="b0986-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0986-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0986-109">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b0986-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0986-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b0986-110">Type: **uint**</span></span>

<span data-ttu-id="b0986-111">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="b0986-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0986-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0986-112">Return value</span></span>

<span data-ttu-id="b0986-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="b0986-113">Type: **R**</span></span>

<span data-ttu-id="b0986-114">Variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="b0986-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0986-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0986-115">Remarks</span></span>

<span data-ttu-id="b0986-116">Un recurso estructurado se puede indexar más en función de los nombres de componente de las estructuras.</span><span class="sxs-lookup"><span data-stu-id="b0986-116">A structured resource can be further indexed based on the component names of the structures.</span></span>

<span data-ttu-id="b0986-117">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b0986-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b0986-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="b0986-118">Vertex</span></span> | <span data-ttu-id="b0986-119">Casco</span><span class="sxs-lookup"><span data-stu-id="b0986-119">Hull</span></span> | <span data-ttu-id="b0986-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="b0986-120">Domain</span></span> | <span data-ttu-id="b0986-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="b0986-121">Geometry</span></span> | <span data-ttu-id="b0986-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="b0986-122">Pixel</span></span> | <span data-ttu-id="b0986-123">Compute</span><span class="sxs-lookup"><span data-stu-id="b0986-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b0986-124">x</span><span class="sxs-lookup"><span data-stu-id="b0986-124">x</span></span>     | <span data-ttu-id="b0986-125">x</span><span class="sxs-lookup"><span data-stu-id="b0986-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b0986-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0986-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0986-127">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="b0986-127">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="b0986-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b0986-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




