---
title: 'InputPatch:: Operator (función)'
description: 'Devuelve el n punto de control de la revisión. | InputPatch:: Operator (función)'
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
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
ms.openlocfilehash: 5d95cb8adae6e7a91629614e0ae10b4161dbac3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280024"
---
# <a name="inputpatchoperator--function"></a><span data-ttu-id="20ad3-105">InputPatch:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="20ad3-105">InputPatch::Operator  function</span></span>

<span data-ttu-id="20ad3-106">Devuelve el punto <sup>de control</sup> *n* de la revisión.</span><span class="sxs-lookup"><span data-stu-id="20ad3-106">Returns the *n*<sup>th</sup> control point in the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="20ad3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20ad3-107">Syntax</span></span>

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a><span data-ttu-id="20ad3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20ad3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20ad3-109">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20ad3-109">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ad3-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="20ad3-110">Type: **uint**</span></span>

<span data-ttu-id="20ad3-111">Índice de entrada.</span><span class="sxs-lookup"><span data-stu-id="20ad3-111">The input index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20ad3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20ad3-112">Return value</span></span>

<span data-ttu-id="20ad3-113">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="20ad3-113">Type: **T**</span></span>

<span data-ttu-id="20ad3-114">Punto <sup>de control</sup> n.</span><span class="sxs-lookup"><span data-stu-id="20ad3-114">The *n*<sup>th</sup> control point.</span></span>

## <a name="remarks"></a><span data-ttu-id="20ad3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20ad3-115">Remarks</span></span>

<span data-ttu-id="20ad3-116">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="20ad3-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="20ad3-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="20ad3-117">Vertex</span></span> | <span data-ttu-id="20ad3-118">Casco</span><span class="sxs-lookup"><span data-stu-id="20ad3-118">Hull</span></span> | <span data-ttu-id="20ad3-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="20ad3-119">Domain</span></span> | <span data-ttu-id="20ad3-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="20ad3-120">Geometry</span></span> | <span data-ttu-id="20ad3-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="20ad3-121">Pixel</span></span> | <span data-ttu-id="20ad3-122">Compute</span><span class="sxs-lookup"><span data-stu-id="20ad3-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="20ad3-123">x</span><span class="sxs-lookup"><span data-stu-id="20ad3-123">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="20ad3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="20ad3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ad3-125">InputPatch</span><span class="sxs-lookup"><span data-stu-id="20ad3-125">InputPatch</span></span>](sm5-object-inputpatch.md)
</dt> <dt>

[<span data-ttu-id="20ad3-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="20ad3-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




