---
title: 'Texture2D:: Operator (función)'
description: 'Devuelve una variable de recurso de solo lectura. | Texture2D:: Operator (función)'
ms.assetid: 72ba3fc8-04c3-479a-b307-525020898bac
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
ms.openlocfilehash: 2c397b1b80836f48cb856d03ccdf52ad2c95ce48
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986511"
---
# <a name="texture2doperator--function"></a><span data-ttu-id="83b46-105">Texture2D:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="83b46-105">Texture2D::Operator  function</span></span>

<span data-ttu-id="83b46-106">Devuelve una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="83b46-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="83b46-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83b46-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="83b46-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83b46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83b46-109">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="83b46-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83b46-110">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="83b46-110">Type: **uint2**</span></span>

<span data-ttu-id="83b46-111">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="83b46-111">The index position.</span></span> <span data-ttu-id="83b46-112">Contiene las coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="83b46-112">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83b46-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83b46-113">Return value</span></span>

<span data-ttu-id="83b46-114">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="83b46-114">Type: **R**</span></span>

<span data-ttu-id="83b46-115">Variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="83b46-115">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="83b46-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83b46-116">Remarks</span></span>

<span data-ttu-id="83b46-117">Este método siempre tiene acceso al primer nivel de MIP.</span><span class="sxs-lookup"><span data-stu-id="83b46-117">This method always accesses the first mip level.</span></span> <span data-ttu-id="83b46-118">Para especificar otros niveles de MIP, utilice en su lugar el método [**MIP. Operator \[ \] \[ \]**](sm5-object-texture2d-mipsoperatorindex.md) .</span><span class="sxs-lookup"><span data-stu-id="83b46-118">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="83b46-119">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="83b46-119">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="83b46-120">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="83b46-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="83b46-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="83b46-121">Vertex</span></span> | <span data-ttu-id="83b46-122">Casco</span><span class="sxs-lookup"><span data-stu-id="83b46-122">Hull</span></span> | <span data-ttu-id="83b46-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="83b46-123">Domain</span></span> | <span data-ttu-id="83b46-124">Geometría</span><span class="sxs-lookup"><span data-stu-id="83b46-124">Geometry</span></span> | <span data-ttu-id="83b46-125">Píxel</span><span class="sxs-lookup"><span data-stu-id="83b46-125">Pixel</span></span> | <span data-ttu-id="83b46-126">Compute</span><span class="sxs-lookup"><span data-stu-id="83b46-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="83b46-127">x</span><span class="sxs-lookup"><span data-stu-id="83b46-127">x</span></span>      | <span data-ttu-id="83b46-128">x</span><span class="sxs-lookup"><span data-stu-id="83b46-128">x</span></span>    | <span data-ttu-id="83b46-129">x</span><span class="sxs-lookup"><span data-stu-id="83b46-129">x</span></span>      | <span data-ttu-id="83b46-130">x</span><span class="sxs-lookup"><span data-stu-id="83b46-130">x</span></span>        | <span data-ttu-id="83b46-131">x</span><span class="sxs-lookup"><span data-stu-id="83b46-131">x</span></span>     | <span data-ttu-id="83b46-132">x</span><span class="sxs-lookup"><span data-stu-id="83b46-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="83b46-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="83b46-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b46-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="83b46-134">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="83b46-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="83b46-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




