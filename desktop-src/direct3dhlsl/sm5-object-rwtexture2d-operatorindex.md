---
title: 'RWTexture2D:: Operator (función)'
description: 'Devuelve una variable de recurso. | RWTexture2D:: Operator (función)'
ms.assetid: 339dba7d-b0c6-4112-ae40-555661577a3e
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
ms.openlocfilehash: 8c1ff25cdf4a0f33d041500f6a81220261f216c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986478"
---
# <a name="rwtexture2doperator--function"></a><span data-ttu-id="6f9e6-105">RWTexture2D:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="6f9e6-105">RWTexture2D::Operator  function</span></span>

<span data-ttu-id="6f9e6-106">Devuelve una variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f9e6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f9e6-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="6f9e6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f9e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f9e6-109">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6f9e6-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9e6-110">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="6f9e6-110">Type: **uint2**</span></span>

<span data-ttu-id="6f9e6-111">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-111">The index position.</span></span> <span data-ttu-id="6f9e6-112">Contiene las coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="6f9e6-112">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f9e6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f9e6-113">Return value</span></span>

<span data-ttu-id="6f9e6-114">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="6f9e6-114">Type: **R**</span></span>

<span data-ttu-id="6f9e6-115">Variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="6f9e6-115">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f9e6-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f9e6-116">Remarks</span></span>

<span data-ttu-id="6f9e6-117">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="6f9e6-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6f9e6-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="6f9e6-118">Vertex</span></span> | <span data-ttu-id="6f9e6-119">Casco</span><span class="sxs-lookup"><span data-stu-id="6f9e6-119">Hull</span></span> | <span data-ttu-id="6f9e6-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="6f9e6-120">Domain</span></span> | <span data-ttu-id="6f9e6-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="6f9e6-121">Geometry</span></span> | <span data-ttu-id="6f9e6-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="6f9e6-122">Pixel</span></span> | <span data-ttu-id="6f9e6-123">Compute</span><span class="sxs-lookup"><span data-stu-id="6f9e6-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6f9e6-124">x</span><span class="sxs-lookup"><span data-stu-id="6f9e6-124">x</span></span>     | <span data-ttu-id="6f9e6-125">x</span><span class="sxs-lookup"><span data-stu-id="6f9e6-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6f9e6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f9e6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f9e6-127">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="6f9e6-127">RWTexture2D</span></span>](sm5-object-rwtexture2d.md)
</dt> <dt>

[<span data-ttu-id="6f9e6-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6f9e6-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




