---
title: dot
description: Devuelve el producto escalar de dos vectores.
ms.assetid: ad24c06c-0b40-4dc5-a2b9-1d5438635ed8
keywords:
- HLSL de punto
topic_type:
- apiref
api_name:
- dot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6d05abf0d67628d1d77b362b028107e07b83457
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995511"
---
# <a name="dot"></a><span data-ttu-id="47f5f-104">dot</span><span class="sxs-lookup"><span data-stu-id="47f5f-104">dot</span></span>

<span data-ttu-id="47f5f-105">Devuelve el producto escalar de dos vectores.</span><span class="sxs-lookup"><span data-stu-id="47f5f-105">Returns the dot product of two vectors.</span></span>



| <span data-ttu-id="47f5f-106">*RET* (punto *x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="47f5f-106">*ret* dot(*x*, *y*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="47f5f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47f5f-107">Parameters</span></span>



| <span data-ttu-id="47f5f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="47f5f-108">Item</span></span>                                                   | <span data-ttu-id="47f5f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="47f5f-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="47f5f-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="47f5f-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="47f5f-111">\[en \] el primer vector.</span><span class="sxs-lookup"><span data-stu-id="47f5f-111">\[in\] The first vector.</span></span><br/>  |
| <span data-ttu-id="47f5f-112"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="47f5f-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="47f5f-113">\[en \] el segundo vector.</span><span class="sxs-lookup"><span data-stu-id="47f5f-113">\[in\] The second vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="47f5f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47f5f-114">Return Value</span></span>

<span data-ttu-id="47f5f-115">El producto DOT del parámetro *x* y del parámetro *y* .</span><span class="sxs-lookup"><span data-stu-id="47f5f-115">The dot product of the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="47f5f-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="47f5f-116">Type Description</span></span>



| <span data-ttu-id="47f5f-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="47f5f-117">Name</span></span>  | [<span data-ttu-id="47f5f-118">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="47f5f-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="47f5f-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="47f5f-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="47f5f-120">Tamaño</span><span class="sxs-lookup"><span data-stu-id="47f5f-120">Size</span></span>                            |
|-------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="47f5f-121">*x*</span><span class="sxs-lookup"><span data-stu-id="47f5f-121">*x*</span></span>   | [<span data-ttu-id="47f5f-122">**medios**</span><span class="sxs-lookup"><span data-stu-id="47f5f-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="47f5f-123">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="47f5f-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="47f5f-124">cualquiera</span><span class="sxs-lookup"><span data-stu-id="47f5f-124">any</span></span>                             |
| <span data-ttu-id="47f5f-125">*y*</span><span class="sxs-lookup"><span data-stu-id="47f5f-125">*y*</span></span>   | [<span data-ttu-id="47f5f-126">**medios**</span><span class="sxs-lookup"><span data-stu-id="47f5f-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="47f5f-127">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="47f5f-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="47f5f-128">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="47f5f-128">same dimensions(s) as input *x*</span></span> |
| <span data-ttu-id="47f5f-129">*direcc*</span><span class="sxs-lookup"><span data-stu-id="47f5f-129">*ret*</span></span> | [<span data-ttu-id="47f5f-130">**escalar**</span><span class="sxs-lookup"><span data-stu-id="47f5f-130">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="47f5f-131">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="47f5f-131">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="47f5f-132">1</span><span class="sxs-lookup"><span data-stu-id="47f5f-132">1</span></span>                               |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="47f5f-133">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="47f5f-133">Minimum Shader Model</span></span>

<span data-ttu-id="47f5f-134">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="47f5f-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="47f5f-135">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="47f5f-135">Shader Model</span></span>                                                                       | <span data-ttu-id="47f5f-136">Compatible</span><span class="sxs-lookup"><span data-stu-id="47f5f-136">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="47f5f-137">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="47f5f-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="47f5f-138">sí</span><span class="sxs-lookup"><span data-stu-id="47f5f-138">yes</span></span>       |
| [<span data-ttu-id="47f5f-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47f5f-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="47f5f-140">sí</span><span class="sxs-lookup"><span data-stu-id="47f5f-140">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="47f5f-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="47f5f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47f5f-142">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="47f5f-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

