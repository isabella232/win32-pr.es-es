---
title: 'RWTexture2DArray:: Operator (función)'
description: 'Devuelve una variable de recurso. | RWTexture2DArray:: Operator (función)'
ms.assetid: ae3d0697-ea0a-450d-bdfe-7bc5d8faf11a
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
ms.openlocfilehash: faf49c48fbf5042ce2765005cd8daea4d1227255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083619"
---
# <a name="rwtexture2darrayoperator--function"></a><span data-ttu-id="0d42c-105">RWTexture2DArray:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="0d42c-105">RWTexture2DArray::Operator  function</span></span>

<span data-ttu-id="0d42c-106">Devuelve una variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="0d42c-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d42c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d42c-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="0d42c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d42c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d42c-109">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0d42c-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d42c-110">Tipo: **UInt3**</span><span class="sxs-lookup"><span data-stu-id="0d42c-110">Type: **uint3**</span></span>

<span data-ttu-id="0d42c-111">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="0d42c-111">The index position.</span></span> <span data-ttu-id="0d42c-112">Los componentes primero y segundo contienen las coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="0d42c-112">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="0d42c-113">El tercer componente indica el segmento de matriz deseado.</span><span class="sxs-lookup"><span data-stu-id="0d42c-113">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d42c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d42c-114">Return value</span></span>

<span data-ttu-id="0d42c-115">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="0d42c-115">Type: **R**</span></span>

<span data-ttu-id="0d42c-116">Variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="0d42c-116">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d42c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d42c-117">Remarks</span></span>

<span data-ttu-id="0d42c-118">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="0d42c-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0d42c-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="0d42c-119">Vertex</span></span> | <span data-ttu-id="0d42c-120">Casco</span><span class="sxs-lookup"><span data-stu-id="0d42c-120">Hull</span></span> | <span data-ttu-id="0d42c-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="0d42c-121">Domain</span></span> | <span data-ttu-id="0d42c-122">Geometría</span><span class="sxs-lookup"><span data-stu-id="0d42c-122">Geometry</span></span> | <span data-ttu-id="0d42c-123">Píxel</span><span class="sxs-lookup"><span data-stu-id="0d42c-123">Pixel</span></span> | <span data-ttu-id="0d42c-124">Compute</span><span class="sxs-lookup"><span data-stu-id="0d42c-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="0d42c-125">x</span><span class="sxs-lookup"><span data-stu-id="0d42c-125">x</span></span>     | <span data-ttu-id="0d42c-126">x</span><span class="sxs-lookup"><span data-stu-id="0d42c-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0d42c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d42c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d42c-128">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="0d42c-128">RWTexture2DArray</span></span>](sm5-object-rwtexture2darray.md)
</dt> <dt>

[<span data-ttu-id="0d42c-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0d42c-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




