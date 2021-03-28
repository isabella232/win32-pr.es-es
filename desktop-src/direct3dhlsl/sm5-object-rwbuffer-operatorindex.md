---
title: 'RWBuffer:: Operator (función)'
description: 'Devuelve una variable de recurso. | RWBuffer:: Operator (función)'
ms.assetid: 59e5e4ec-ff0d-43aa-805a-04b79f5ab57f
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
ms.openlocfilehash: 40336c8ad6ee9e8008b82c172f1a5b863e967c0d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998021"
---
# <a name="rwbufferoperator--function"></a><span data-ttu-id="69b61-105">RWBuffer:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="69b61-105">RWBuffer::Operator  function</span></span>

<span data-ttu-id="69b61-106">Devuelve una variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="69b61-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b61-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69b61-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="69b61-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69b61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b61-109">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="69b61-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b61-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="69b61-110">Type: **uint**</span></span>

<span data-ttu-id="69b61-111">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="69b61-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b61-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69b61-112">Return value</span></span>

<span data-ttu-id="69b61-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="69b61-113">Type: **R**</span></span>

<span data-ttu-id="69b61-114">Variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="69b61-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="69b61-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69b61-115">Remarks</span></span>

<span data-ttu-id="69b61-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="69b61-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="69b61-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="69b61-117">Vertex</span></span> | <span data-ttu-id="69b61-118">Casco</span><span class="sxs-lookup"><span data-stu-id="69b61-118">Hull</span></span> | <span data-ttu-id="69b61-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="69b61-119">Domain</span></span> | <span data-ttu-id="69b61-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="69b61-120">Geometry</span></span> | <span data-ttu-id="69b61-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="69b61-121">Pixel</span></span> | <span data-ttu-id="69b61-122">Compute</span><span class="sxs-lookup"><span data-stu-id="69b61-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="69b61-123">x</span><span class="sxs-lookup"><span data-stu-id="69b61-123">x</span></span>      | <span data-ttu-id="69b61-124">x</span><span class="sxs-lookup"><span data-stu-id="69b61-124">x</span></span>    | <span data-ttu-id="69b61-125">x</span><span class="sxs-lookup"><span data-stu-id="69b61-125">x</span></span>      | <span data-ttu-id="69b61-126">x</span><span class="sxs-lookup"><span data-stu-id="69b61-126">x</span></span>        | <span data-ttu-id="69b61-127">x</span><span class="sxs-lookup"><span data-stu-id="69b61-127">x</span></span>     | <span data-ttu-id="69b61-128">x</span><span class="sxs-lookup"><span data-stu-id="69b61-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="69b61-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="69b61-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b61-130">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="69b61-130">RWBuffer</span></span>](sm5-object-rwbuffer.md)
</dt> <dt>

[<span data-ttu-id="69b61-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="69b61-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




