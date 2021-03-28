---
title: 'StructuredBuffer:: Operator (función)'
description: Devuelve una variable de recurso de solo lectura de un StructuredBuffer.
ms.assetid: e2a1b0f7-f374-44a3-b567-8a2318e8b2b8
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
ms.openlocfilehash: 1f0d75bdfbcd3bfc560e896416f241f1291120d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149812"
---
# <a name="structuredbufferoperator--function"></a><span data-ttu-id="e3931-104">StructuredBuffer:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="e3931-104">StructuredBuffer::Operator  function</span></span>

<span data-ttu-id="e3931-105">Devuelve una variable de recurso de solo lectura de un [**StructuredBuffer**](sm5-object-structuredbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="e3931-105">Returns a read-only resource variable of a [**StructuredBuffer**](sm5-object-structuredbuffer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3931-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3931-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="e3931-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3931-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3931-108">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e3931-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3931-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e3931-109">Type: **uint**</span></span>

<span data-ttu-id="e3931-110">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="e3931-110">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3931-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3931-111">Return value</span></span>

<span data-ttu-id="e3931-112">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="e3931-112">Type: **R**</span></span>

<span data-ttu-id="e3931-113">Variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e3931-113">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3931-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3931-114">Remarks</span></span>

<span data-ttu-id="e3931-115">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="e3931-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e3931-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="e3931-116">Vertex</span></span> | <span data-ttu-id="e3931-117">Casco</span><span class="sxs-lookup"><span data-stu-id="e3931-117">Hull</span></span> | <span data-ttu-id="e3931-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="e3931-118">Domain</span></span> | <span data-ttu-id="e3931-119">Geometría</span><span class="sxs-lookup"><span data-stu-id="e3931-119">Geometry</span></span> | <span data-ttu-id="e3931-120">Píxel</span><span class="sxs-lookup"><span data-stu-id="e3931-120">Pixel</span></span> | <span data-ttu-id="e3931-121">Compute</span><span class="sxs-lookup"><span data-stu-id="e3931-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e3931-122">x</span><span class="sxs-lookup"><span data-stu-id="e3931-122">x</span></span>      | <span data-ttu-id="e3931-123">x</span><span class="sxs-lookup"><span data-stu-id="e3931-123">x</span></span>    | <span data-ttu-id="e3931-124">x</span><span class="sxs-lookup"><span data-stu-id="e3931-124">x</span></span>      | <span data-ttu-id="e3931-125">x</span><span class="sxs-lookup"><span data-stu-id="e3931-125">x</span></span>        | <span data-ttu-id="e3931-126">x</span><span class="sxs-lookup"><span data-stu-id="e3931-126">x</span></span>     | <span data-ttu-id="e3931-127">x</span><span class="sxs-lookup"><span data-stu-id="e3931-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e3931-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3931-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3931-129">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="e3931-129">StructuredBuffer</span></span>](sm5-object-structuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="e3931-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e3931-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




