---
title: 'Texture1DArray:: Operator (función)'
description: 'Devuelve una variable de recurso de solo lectura. | Texture1DArray:: Operator (función)'
ms.assetid: 05ec9652-b5dd-41cf-8bef-730c507c5ba4
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
ms.openlocfilehash: 578d778cd1e0e064c435c19fb094feb66f651e05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986475"
---
# <a name="texture1darrayoperator--function"></a><span data-ttu-id="6c3ab-105">Texture1DArray:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="6c3ab-105">Texture1DArray::Operator  function</span></span>

<span data-ttu-id="6c3ab-106">Devuelve una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6c3ab-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c3ab-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c3ab-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="6c3ab-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c3ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c3ab-109">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6c3ab-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c3ab-110">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="6c3ab-110">Type: **uint2**</span></span>

<span data-ttu-id="6c3ab-111">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="6c3ab-111">The index position.</span></span> <span data-ttu-id="6c3ab-112">El primer componente contiene la coordenada x.</span><span class="sxs-lookup"><span data-stu-id="6c3ab-112">The first component contains the x-coordinate.</span></span> <span data-ttu-id="6c3ab-113">El segundo componente indica el segmento de matriz deseado.</span><span class="sxs-lookup"><span data-stu-id="6c3ab-113">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c3ab-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c3ab-114">Return value</span></span>

<span data-ttu-id="6c3ab-115">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="6c3ab-115">Type: **R**</span></span>

<span data-ttu-id="6c3ab-116">Variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6c3ab-116">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c3ab-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c3ab-117">Remarks</span></span>

<span data-ttu-id="6c3ab-118">Este método siempre tiene acceso al primer nivel de MIP.</span><span class="sxs-lookup"><span data-stu-id="6c3ab-118">This method always accesses the first mip level.</span></span> <span data-ttu-id="6c3ab-119">Para especificar otros niveles de MIP, utilice en su lugar el método [**MIP. Operator \[ \] \[ \]**](sm5-object-texture1darray-mipsoperatorindex.md) .</span><span class="sxs-lookup"><span data-stu-id="6c3ab-119">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="6c3ab-120">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="6c3ab-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6c3ab-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="6c3ab-121">Vertex</span></span> | <span data-ttu-id="6c3ab-122">Casco</span><span class="sxs-lookup"><span data-stu-id="6c3ab-122">Hull</span></span> | <span data-ttu-id="6c3ab-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="6c3ab-123">Domain</span></span> | <span data-ttu-id="6c3ab-124">Geometría</span><span class="sxs-lookup"><span data-stu-id="6c3ab-124">Geometry</span></span> | <span data-ttu-id="6c3ab-125">Píxel</span><span class="sxs-lookup"><span data-stu-id="6c3ab-125">Pixel</span></span> | <span data-ttu-id="6c3ab-126">Compute</span><span class="sxs-lookup"><span data-stu-id="6c3ab-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6c3ab-127">x</span><span class="sxs-lookup"><span data-stu-id="6c3ab-127">x</span></span>      | <span data-ttu-id="6c3ab-128">x</span><span class="sxs-lookup"><span data-stu-id="6c3ab-128">x</span></span>    | <span data-ttu-id="6c3ab-129">x</span><span class="sxs-lookup"><span data-stu-id="6c3ab-129">x</span></span>      | <span data-ttu-id="6c3ab-130">x</span><span class="sxs-lookup"><span data-stu-id="6c3ab-130">x</span></span>        | <span data-ttu-id="6c3ab-131">x</span><span class="sxs-lookup"><span data-stu-id="6c3ab-131">x</span></span>     | <span data-ttu-id="6c3ab-132">x</span><span class="sxs-lookup"><span data-stu-id="6c3ab-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6c3ab-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c3ab-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c3ab-134">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="6c3ab-134">Texture1DArray</span></span>](sm5-object-texture1darray.md)
</dt> <dt>

[<span data-ttu-id="6c3ab-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6c3ab-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




