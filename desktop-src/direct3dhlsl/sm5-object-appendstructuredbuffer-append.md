---
title: 'AppendStructuredBuffer:: Append (función)'
description: Anexa un valor al final del búfer.
ms.assetid: 667bc6dc-c0d0-419a-9227-99ce30b9cc73
keywords:
- Anexar la función HLSL
topic_type:
- apiref
api_name:
- Append
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79db73558cb243437560cc77ed66b64f2807fe13
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "103994791"
---
# <a name="append-function"></a><span data-ttu-id="14737-104">Append (función)</span><span class="sxs-lookup"><span data-stu-id="14737-104">Append function</span></span>

<span data-ttu-id="14737-105">Anexa un valor al final del búfer.</span><span class="sxs-lookup"><span data-stu-id="14737-105">Appends a value to the end of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="14737-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14737-106">Syntax</span></span>

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a><span data-ttu-id="14737-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14737-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14737-108">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="14737-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14737-109">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="14737-109">Type: **T**</span></span>

<span data-ttu-id="14737-110">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="14737-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14737-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14737-111">Return value</span></span>

<span data-ttu-id="14737-112">Ninguno</span><span class="sxs-lookup"><span data-stu-id="14737-112">None</span></span>

## <a name="remarks"></a><span data-ttu-id="14737-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14737-113">Remarks</span></span>

<span data-ttu-id="14737-114">T puede ser cualquier tipo de datos, incluidas las estructuras.</span><span class="sxs-lookup"><span data-stu-id="14737-114">T can be any data type including structures.</span></span>

<span data-ttu-id="14737-115">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="14737-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="14737-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="14737-116">Vertex</span></span> | <span data-ttu-id="14737-117">Casco</span><span class="sxs-lookup"><span data-stu-id="14737-117">Hull</span></span> | <span data-ttu-id="14737-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="14737-118">Domain</span></span> | <span data-ttu-id="14737-119">Geometría</span><span class="sxs-lookup"><span data-stu-id="14737-119">Geometry</span></span> | <span data-ttu-id="14737-120">Píxel</span><span class="sxs-lookup"><span data-stu-id="14737-120">Pixel</span></span> | <span data-ttu-id="14737-121">Compute</span><span class="sxs-lookup"><span data-stu-id="14737-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="14737-122">x</span><span class="sxs-lookup"><span data-stu-id="14737-122">x</span></span>      | <span data-ttu-id="14737-123">x</span><span class="sxs-lookup"><span data-stu-id="14737-123">x</span></span>    | <span data-ttu-id="14737-124">x</span><span class="sxs-lookup"><span data-stu-id="14737-124">x</span></span>      | <span data-ttu-id="14737-125">x</span><span class="sxs-lookup"><span data-stu-id="14737-125">x</span></span>        | <span data-ttu-id="14737-126">x</span><span class="sxs-lookup"><span data-stu-id="14737-126">x</span></span>     | <span data-ttu-id="14737-127">x</span><span class="sxs-lookup"><span data-stu-id="14737-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="14737-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="14737-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14737-129">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="14737-129">AppendStructuredBuffer</span></span>](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="14737-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="14737-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




