---
title: 'OutputPatch:: Operator (función)'
description: 'Devuelve el n punto de control de la revisión. | OutputPatch:: Operator (función)'
ms.assetid: 3ac15fe8-8bab-46a2-8826-61ade927c99e
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
ms.openlocfilehash: 8194713dc4967151991fab95000fa70c40122f26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362141"
---
# <a name="outputpatchoperator--function"></a><span data-ttu-id="21a1d-105">OutputPatch:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="21a1d-105">OutputPatch::Operator  function</span></span>

<span data-ttu-id="21a1d-106">Devuelve el punto <sup>de control</sup> *n* de la revisión.</span><span class="sxs-lookup"><span data-stu-id="21a1d-106">Returns the *n*<sup>th</sup> control point in the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="21a1d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21a1d-107">Syntax</span></span>

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a><span data-ttu-id="21a1d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21a1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21a1d-109">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21a1d-109">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21a1d-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="21a1d-110">Type: **uint**</span></span>

<span data-ttu-id="21a1d-111">Índice de entrada.</span><span class="sxs-lookup"><span data-stu-id="21a1d-111">The input index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21a1d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21a1d-112">Return value</span></span>

<span data-ttu-id="21a1d-113">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="21a1d-113">Type: **T**</span></span>

<span data-ttu-id="21a1d-114">Punto <sup>de control</sup> n.</span><span class="sxs-lookup"><span data-stu-id="21a1d-114">The *n*<sup>th</sup> control point.</span></span>

## <a name="remarks"></a><span data-ttu-id="21a1d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21a1d-115">Remarks</span></span>

<span data-ttu-id="21a1d-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="21a1d-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="21a1d-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="21a1d-117">Vertex</span></span> | <span data-ttu-id="21a1d-118">Casco</span><span class="sxs-lookup"><span data-stu-id="21a1d-118">Hull</span></span> | <span data-ttu-id="21a1d-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="21a1d-119">Domain</span></span> | <span data-ttu-id="21a1d-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="21a1d-120">Geometry</span></span> | <span data-ttu-id="21a1d-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="21a1d-121">Pixel</span></span> | <span data-ttu-id="21a1d-122">Compute</span><span class="sxs-lookup"><span data-stu-id="21a1d-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="21a1d-123">x</span><span class="sxs-lookup"><span data-stu-id="21a1d-123">x</span></span>    | <span data-ttu-id="21a1d-124">x</span><span class="sxs-lookup"><span data-stu-id="21a1d-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="21a1d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="21a1d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21a1d-126">OutputPatch</span><span class="sxs-lookup"><span data-stu-id="21a1d-126">OutputPatch</span></span>](sm5-object-outputpatch.md)
</dt> <dt>

[<span data-ttu-id="21a1d-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="21a1d-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




