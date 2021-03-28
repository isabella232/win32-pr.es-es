---
title: distancia
description: Devuelve un escalar de distancia entre dos vectores.
ms.assetid: dda8dc39-fd72-4e92-bf9d-e700db0ede9e
keywords:
- HLSL de distancia
topic_type:
- apiref
api_name:
- distance
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0f3a64778666ac8f7de16b91eed202e36e90ed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359124"
---
# <a name="distance"></a><span data-ttu-id="6013d-104">distancia</span><span class="sxs-lookup"><span data-stu-id="6013d-104">distance</span></span>

<span data-ttu-id="6013d-105">Devuelve un escalar de distancia entre dos vectores.</span><span class="sxs-lookup"><span data-stu-id="6013d-105">Returns a distance scalar between two vectors.</span></span>



| <span data-ttu-id="6013d-106">distancia *RET* (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="6013d-106">*ret* distance(*x*, *y*)</span></span> |
|--------------------------|



 

## <a name="parameters"></a><span data-ttu-id="6013d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6013d-107">Parameters</span></span>



| <span data-ttu-id="6013d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6013d-108">Item</span></span>                                                   | <span data-ttu-id="6013d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6013d-109">Description</span></span>                                                    |
|--------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="6013d-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="6013d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="6013d-111">\[en \] el primer vector de punto flotante que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="6013d-111">\[in\] The first floating-point vector to compare.</span></span><br/>  |
| <span data-ttu-id="6013d-112"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="6013d-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="6013d-113">\[en \] el segundo vector de punto flotante que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="6013d-113">\[in\] The second floating-point vector to compare.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="6013d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6013d-114">Return Value</span></span>

<span data-ttu-id="6013d-115">Un valor escalar y de punto flotante que representa la distancia entre el parámetro *x* y el parámetro *y* .</span><span class="sxs-lookup"><span data-stu-id="6013d-115">A floating-point, scalar value that represents the distance between the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="6013d-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="6013d-116">Type Description</span></span>



| <span data-ttu-id="6013d-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="6013d-117">Name</span></span>  | [<span data-ttu-id="6013d-118">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="6013d-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="6013d-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="6013d-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="6013d-120">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6013d-120">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="6013d-121">*x*</span><span class="sxs-lookup"><span data-stu-id="6013d-121">*x*</span></span>   | [<span data-ttu-id="6013d-122">**medios**</span><span class="sxs-lookup"><span data-stu-id="6013d-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6013d-123">**flot**</span><span class="sxs-lookup"><span data-stu-id="6013d-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6013d-124">cualquiera</span><span class="sxs-lookup"><span data-stu-id="6013d-124">any</span></span>                            |
| <span data-ttu-id="6013d-125">*y*</span><span class="sxs-lookup"><span data-stu-id="6013d-125">*y*</span></span>   | [<span data-ttu-id="6013d-126">**medios**</span><span class="sxs-lookup"><span data-stu-id="6013d-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6013d-127">**flot**</span><span class="sxs-lookup"><span data-stu-id="6013d-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6013d-128">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="6013d-128">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="6013d-129">*direcc*</span><span class="sxs-lookup"><span data-stu-id="6013d-129">*ret*</span></span> | [<span data-ttu-id="6013d-130">**escalar**</span><span class="sxs-lookup"><span data-stu-id="6013d-130">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6013d-131">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="6013d-131">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6013d-132">1</span><span class="sxs-lookup"><span data-stu-id="6013d-132">1</span></span>                              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6013d-133">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="6013d-133">Minimum Shader Model</span></span>

<span data-ttu-id="6013d-134">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6013d-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6013d-135">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="6013d-135">Shader Model</span></span>                                                                       | <span data-ttu-id="6013d-136">Compatible</span><span class="sxs-lookup"><span data-stu-id="6013d-136">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6013d-137">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="6013d-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="6013d-138">sí</span><span class="sxs-lookup"><span data-stu-id="6013d-138">yes</span></span>       |
| [<span data-ttu-id="6013d-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6013d-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="6013d-140">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="6013d-140">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="6013d-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="6013d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6013d-142">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="6013d-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

