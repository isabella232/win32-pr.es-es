---
title: 'Texture2DArray:: Operator (función)'
description: 'Devuelve una variable de recurso de solo lectura. | Texture2DArray:: Operator (función)'
ms.assetid: eb6ff496-c46f-405f-a172-ab747415a2f9
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
ms.openlocfilehash: 1b86aad839fbf28a4fc666b3a5fe5c5788b7b3ae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083618"
---
# <a name="texture2darrayoperator--function"></a><span data-ttu-id="aa2b4-105">Texture2DArray:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="aa2b4-105">Texture2DArray::Operator  function</span></span>

<span data-ttu-id="aa2b4-106">Devuelve una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="aa2b4-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa2b4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa2b4-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="aa2b4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa2b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa2b4-109">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="aa2b4-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa2b4-110">Tipo: **UInt3**</span><span class="sxs-lookup"><span data-stu-id="aa2b4-110">Type: **uint3**</span></span>

<span data-ttu-id="aa2b4-111">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="aa2b4-111">The index position.</span></span> <span data-ttu-id="aa2b4-112">Los componentes primero y segundo contienen las coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="aa2b4-112">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="aa2b4-113">El tercer componente indica el segmento de matriz deseado.</span><span class="sxs-lookup"><span data-stu-id="aa2b4-113">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa2b4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa2b4-114">Return value</span></span>

<span data-ttu-id="aa2b4-115">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="aa2b4-115">Type: **R**</span></span>

<span data-ttu-id="aa2b4-116">Variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="aa2b4-116">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa2b4-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa2b4-117">Remarks</span></span>

<span data-ttu-id="aa2b4-118">Este método siempre tiene acceso al primer nivel de MIP.</span><span class="sxs-lookup"><span data-stu-id="aa2b4-118">This method always accesses the first mip level.</span></span> <span data-ttu-id="aa2b4-119">Para especificar otros niveles de MIP, utilice en su lugar el método [**MIP. Operator \[ \] \[ \]**](sm5-object-texture2darray-mipsoperatorindex.md) .</span><span class="sxs-lookup"><span data-stu-id="aa2b4-119">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) method instead.</span></span>

<span data-ttu-id="aa2b4-120">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="aa2b4-120">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="aa2b4-121">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="aa2b4-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="aa2b4-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="aa2b4-122">Vertex</span></span> | <span data-ttu-id="aa2b4-123">Casco</span><span class="sxs-lookup"><span data-stu-id="aa2b4-123">Hull</span></span> | <span data-ttu-id="aa2b4-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="aa2b4-124">Domain</span></span> | <span data-ttu-id="aa2b4-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="aa2b4-125">Geometry</span></span> | <span data-ttu-id="aa2b4-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="aa2b4-126">Pixel</span></span> | <span data-ttu-id="aa2b4-127">Compute</span><span class="sxs-lookup"><span data-stu-id="aa2b4-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="aa2b4-128">x</span><span class="sxs-lookup"><span data-stu-id="aa2b4-128">x</span></span>      | <span data-ttu-id="aa2b4-129">x</span><span class="sxs-lookup"><span data-stu-id="aa2b4-129">x</span></span>    | <span data-ttu-id="aa2b4-130">x</span><span class="sxs-lookup"><span data-stu-id="aa2b4-130">x</span></span>      | <span data-ttu-id="aa2b4-131">x</span><span class="sxs-lookup"><span data-stu-id="aa2b4-131">x</span></span>        | <span data-ttu-id="aa2b4-132">x</span><span class="sxs-lookup"><span data-stu-id="aa2b4-132">x</span></span>     | <span data-ttu-id="aa2b4-133">x</span><span class="sxs-lookup"><span data-stu-id="aa2b4-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="aa2b4-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa2b4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa2b4-135">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="aa2b4-135">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> <dt>

[<span data-ttu-id="aa2b4-136">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="aa2b4-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




