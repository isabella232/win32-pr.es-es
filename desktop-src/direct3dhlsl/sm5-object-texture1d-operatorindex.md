---
title: 'Texture1D:: Operator (función)'
description: Devuelve una variable de recurso de solo lectura para un Texture1D.
ms.assetid: df54097d-4d1b-496a-a17d-6e9a10cfb996
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
ms.openlocfilehash: 44e5b502c7ae8b766363956920d7922858b4d771
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149811"
---
# <a name="texture1doperator--function"></a><span data-ttu-id="5aad3-104">Texture1D:: Operator (función)</span><span class="sxs-lookup"><span data-stu-id="5aad3-104">Texture1D::Operator  function</span></span>

<span data-ttu-id="5aad3-105">Devuelve una variable de recurso de solo lectura para un [**Texture1D**](sm5-object-texture1d.md).</span><span class="sxs-lookup"><span data-stu-id="5aad3-105">Returns a read-only resource variable for a [**Texture1D**](sm5-object-texture1d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5aad3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5aad3-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="5aad3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5aad3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aad3-108">*PDV* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5aad3-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aad3-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="5aad3-109">Type: **uint**</span></span>

<span data-ttu-id="5aad3-110">Posición de índice.</span><span class="sxs-lookup"><span data-stu-id="5aad3-110">The index position.</span></span> <span data-ttu-id="5aad3-111">Contiene la coordenada x.</span><span class="sxs-lookup"><span data-stu-id="5aad3-111">Contains the x-coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aad3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5aad3-112">Return value</span></span>

<span data-ttu-id="5aad3-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="5aad3-113">Type: **R**</span></span>

<span data-ttu-id="5aad3-114">Variable de recurso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5aad3-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="5aad3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5aad3-115">Remarks</span></span>

<span data-ttu-id="5aad3-116">Este método siempre tiene acceso al primer nivel de MIP.</span><span class="sxs-lookup"><span data-stu-id="5aad3-116">This method always accesses the first mip level.</span></span> <span data-ttu-id="5aad3-117">Para especificar otros niveles de MIP, utilice en su lugar el [**\[ \] \[ \] operador MIP.**](sm5-object-texture1d-mipsoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="5aad3-117">To specify other mip levels, use the [**mip.operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) instead.</span></span>

<span data-ttu-id="5aad3-118">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="5aad3-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5aad3-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="5aad3-119">Vertex</span></span> | <span data-ttu-id="5aad3-120">Casco</span><span class="sxs-lookup"><span data-stu-id="5aad3-120">Hull</span></span> | <span data-ttu-id="5aad3-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="5aad3-121">Domain</span></span> | <span data-ttu-id="5aad3-122">Geometría</span><span class="sxs-lookup"><span data-stu-id="5aad3-122">Geometry</span></span> | <span data-ttu-id="5aad3-123">Píxel</span><span class="sxs-lookup"><span data-stu-id="5aad3-123">Pixel</span></span> | <span data-ttu-id="5aad3-124">Compute</span><span class="sxs-lookup"><span data-stu-id="5aad3-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5aad3-125">x</span><span class="sxs-lookup"><span data-stu-id="5aad3-125">x</span></span>      | <span data-ttu-id="5aad3-126">x</span><span class="sxs-lookup"><span data-stu-id="5aad3-126">x</span></span>    | <span data-ttu-id="5aad3-127">x</span><span class="sxs-lookup"><span data-stu-id="5aad3-127">x</span></span>      | <span data-ttu-id="5aad3-128">x</span><span class="sxs-lookup"><span data-stu-id="5aad3-128">x</span></span>        | <span data-ttu-id="5aad3-129">x</span><span class="sxs-lookup"><span data-stu-id="5aad3-129">x</span></span>     | <span data-ttu-id="5aad3-130">x</span><span class="sxs-lookup"><span data-stu-id="5aad3-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5aad3-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aad3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aad3-132">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5aad3-132">Texture1D</span></span>](sm5-object-texture1d.md)
</dt> <dt>

[<span data-ttu-id="5aad3-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="5aad3-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




