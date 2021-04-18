---
title: 'RWTexture1DArray:: Operator (función)'
description: 'Devuelve una variable de recurso. | RWTexture1DArray:: Operator (función)'
ms.assetid: 7047e670-dd78-4b73-8d80-5575e458f27c
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
ms.openlocfilehash: 6f8623ab25b42f6865e401c5b263a1774206c752
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986515"
---
# <a name="rwtexture1darrayoperator--function"></a><span data-ttu-id="0fe1f-105">RWTexture1DArray:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="0fe1f-105">RWTexture1DArray::Operator  function</span></span>

<span data-ttu-id="0fe1f-106">Devuelve una variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="0fe1f-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fe1f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0fe1f-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="0fe1f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fe1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fe1f-109">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0fe1f-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fe1f-110">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="0fe1f-110">Type: **uint2**</span></span>

<span data-ttu-id="0fe1f-111">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="0fe1f-111">The index position.</span></span> <span data-ttu-id="0fe1f-112">El primer componente contiene la coordenada x.</span><span class="sxs-lookup"><span data-stu-id="0fe1f-112">The first component contains the x coordinate.</span></span> <span data-ttu-id="0fe1f-113">El segundo componente indica el segmento de matriz deseado.</span><span class="sxs-lookup"><span data-stu-id="0fe1f-113">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fe1f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0fe1f-114">Return value</span></span>

<span data-ttu-id="0fe1f-115">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="0fe1f-115">Type: **R**</span></span>

<span data-ttu-id="0fe1f-116">Variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="0fe1f-116">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fe1f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fe1f-117">Remarks</span></span>

<span data-ttu-id="0fe1f-118">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="0fe1f-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0fe1f-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="0fe1f-119">Vertex</span></span> | <span data-ttu-id="0fe1f-120">Casco</span><span class="sxs-lookup"><span data-stu-id="0fe1f-120">Hull</span></span> | <span data-ttu-id="0fe1f-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="0fe1f-121">Domain</span></span> | <span data-ttu-id="0fe1f-122">Geometría</span><span class="sxs-lookup"><span data-stu-id="0fe1f-122">Geometry</span></span> | <span data-ttu-id="0fe1f-123">Píxel</span><span class="sxs-lookup"><span data-stu-id="0fe1f-123">Pixel</span></span> | <span data-ttu-id="0fe1f-124">Compute</span><span class="sxs-lookup"><span data-stu-id="0fe1f-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="0fe1f-125">x</span><span class="sxs-lookup"><span data-stu-id="0fe1f-125">x</span></span>     | <span data-ttu-id="0fe1f-126">x</span><span class="sxs-lookup"><span data-stu-id="0fe1f-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0fe1f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fe1f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fe1f-128">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="0fe1f-128">RWTexture1DArray</span></span>](sm5-object-rwtexture1darray.md)
</dt> <dt>

[<span data-ttu-id="0fe1f-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0fe1f-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




