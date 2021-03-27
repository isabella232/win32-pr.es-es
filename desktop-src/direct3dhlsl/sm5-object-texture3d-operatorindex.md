---
title: 'Texture3D:: Operator (función)'
description: 'Devuelve una variable de recurso de solo lectura. | Texture3D:: Operator (función)'
ms.assetid: d7e27778-6a96-47f8-a58a-1966452adf04
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
ms.openlocfilehash: 5c3bb3718094ee859d1e33a046fde7016973a0aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820655"
---
# <a name="texture3doperator--function"></a><span data-ttu-id="ee67d-105">Texture3D:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="ee67d-105">Texture3D::Operator  function</span></span>

<span data-ttu-id="ee67d-106">Devuelve una variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ee67d-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee67d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee67d-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="ee67d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee67d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee67d-109">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ee67d-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee67d-110">Tipo: **UInt3**</span><span class="sxs-lookup"><span data-stu-id="ee67d-110">Type: **uint3**</span></span>

<span data-ttu-id="ee67d-111">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="ee67d-111">The index position.</span></span> <span data-ttu-id="ee67d-112">Contiene las coordenadas (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="ee67d-112">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee67d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee67d-113">Return value</span></span>

<span data-ttu-id="ee67d-114">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="ee67d-114">Type: **R**</span></span>

<span data-ttu-id="ee67d-115">Variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ee67d-115">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee67d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee67d-116">Remarks</span></span>

<span data-ttu-id="ee67d-117">Este método siempre tiene acceso al primer nivel de MIP.</span><span class="sxs-lookup"><span data-stu-id="ee67d-117">This method always accesses the first mip level.</span></span> <span data-ttu-id="ee67d-118">Para especificar otros niveles de MIP, use el [**operador \[ \] \[ \] MIP.**](sm5-object-texture3d-mipsoperatorindex.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="ee67d-118">To specify other mip levels use the [**mip.operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) instead.</span></span>

<span data-ttu-id="ee67d-119">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="ee67d-119">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ee67d-120">Vértice</span><span class="sxs-lookup"><span data-stu-id="ee67d-120">Vertex</span></span> | <span data-ttu-id="ee67d-121">Casco</span><span class="sxs-lookup"><span data-stu-id="ee67d-121">Hull</span></span> | <span data-ttu-id="ee67d-122">Dominio</span><span class="sxs-lookup"><span data-stu-id="ee67d-122">Domain</span></span> | <span data-ttu-id="ee67d-123">Geometría</span><span class="sxs-lookup"><span data-stu-id="ee67d-123">Geometry</span></span> | <span data-ttu-id="ee67d-124">Píxel</span><span class="sxs-lookup"><span data-stu-id="ee67d-124">Pixel</span></span> | <span data-ttu-id="ee67d-125">Compute</span><span class="sxs-lookup"><span data-stu-id="ee67d-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ee67d-126">x</span><span class="sxs-lookup"><span data-stu-id="ee67d-126">x</span></span>      | <span data-ttu-id="ee67d-127">x</span><span class="sxs-lookup"><span data-stu-id="ee67d-127">x</span></span>    | <span data-ttu-id="ee67d-128">x</span><span class="sxs-lookup"><span data-stu-id="ee67d-128">x</span></span>      | <span data-ttu-id="ee67d-129">x</span><span class="sxs-lookup"><span data-stu-id="ee67d-129">x</span></span>        | <span data-ttu-id="ee67d-130">x</span><span class="sxs-lookup"><span data-stu-id="ee67d-130">x</span></span>     | <span data-ttu-id="ee67d-131">x</span><span class="sxs-lookup"><span data-stu-id="ee67d-131">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ee67d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee67d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee67d-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ee67d-133">Texture3D</span></span>](sm5-object-texture3d.md)
</dt> <dt>

[<span data-ttu-id="ee67d-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ee67d-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




