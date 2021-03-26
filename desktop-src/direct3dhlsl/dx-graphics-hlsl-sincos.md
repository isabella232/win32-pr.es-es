---
title: sincos (
description: Devuelve el seno y el coseno de x.
ms.assetid: 2ef9e84e-4539-47f5-9966-d8e02ca15d36
keywords:
- HLSL de sincos (
topic_type:
- apiref
api_name:
- sincos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8391c2fcecc939db1d7044fe56fbd281fe3e79fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997137"
---
# <a name="sincos"></a><span data-ttu-id="ba83a-104">sincos (</span><span class="sxs-lookup"><span data-stu-id="ba83a-104">sincos</span></span>

<span data-ttu-id="ba83a-105">Devuelve el seno y el coseno de x.</span><span class="sxs-lookup"><span data-stu-id="ba83a-105">Returns the sine and cosine of x.</span></span>



| <span data-ttu-id="ba83a-106">sincos ((*x*, out *s*, out *c*)</span><span class="sxs-lookup"><span data-stu-id="ba83a-106">sincos(*x*, out *s*, out *c*)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="ba83a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba83a-107">Parameters</span></span>



| <span data-ttu-id="ba83a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ba83a-108">Item</span></span>                                                   | <span data-ttu-id="ba83a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba83a-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="ba83a-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="ba83a-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ba83a-111">\[en \] el valor especificado, en radianes.</span><span class="sxs-lookup"><span data-stu-id="ba83a-111">\[in\] The specified value, in radians.</span></span><br/> |
| <span data-ttu-id="ba83a-112"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="ba83a-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="ba83a-113">\[out \] devuelve el seno de x.</span><span class="sxs-lookup"><span data-stu-id="ba83a-113">\[out\] Returns the sine of x.</span></span><br/>          |
| <span data-ttu-id="ba83a-114"><span id="c"></span><span id="C"></span>*unidad*</span><span class="sxs-lookup"><span data-stu-id="ba83a-114"><span id="c"></span><span id="C"></span>*c*</span></span><br/> | <span data-ttu-id="ba83a-115">\[out \] devuelve el coseno de x.</span><span class="sxs-lookup"><span data-stu-id="ba83a-115">\[out\] Returns the cosine of x.</span></span><br/>        |



 

## <a name="return-value"></a><span data-ttu-id="ba83a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba83a-116">Return Value</span></span>

<span data-ttu-id="ba83a-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ba83a-117">None.</span></span>

## <a name="type-description"></a><span data-ttu-id="ba83a-118">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="ba83a-118">Type Description</span></span>



| <span data-ttu-id="ba83a-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="ba83a-119">Name</span></span> | [<span data-ttu-id="ba83a-120">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="ba83a-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ba83a-121">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="ba83a-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ba83a-122">Tamaño</span><span class="sxs-lookup"><span data-stu-id="ba83a-122">Size</span></span>                           |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ba83a-123">*x*</span><span class="sxs-lookup"><span data-stu-id="ba83a-123">*x*</span></span>  | <span data-ttu-id="ba83a-124">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="ba83a-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="ba83a-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="ba83a-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ba83a-126">cualquiera</span><span class="sxs-lookup"><span data-stu-id="ba83a-126">any</span></span>                            |
| <span data-ttu-id="ba83a-127">*s*</span><span class="sxs-lookup"><span data-stu-id="ba83a-127">*s*</span></span>  | <span data-ttu-id="ba83a-128">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="ba83a-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="ba83a-129">**flot**</span><span class="sxs-lookup"><span data-stu-id="ba83a-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ba83a-130">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="ba83a-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="ba83a-131">c</span><span class="sxs-lookup"><span data-stu-id="ba83a-131">c</span></span>    | <span data-ttu-id="ba83a-132">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="ba83a-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="ba83a-133">**flot**</span><span class="sxs-lookup"><span data-stu-id="ba83a-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ba83a-134">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="ba83a-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ba83a-135">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="ba83a-135">Minimum Shader Model</span></span>

<span data-ttu-id="ba83a-136">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ba83a-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ba83a-137">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ba83a-137">Shader Model</span></span>                                                                       | <span data-ttu-id="ba83a-138">Compatible</span><span class="sxs-lookup"><span data-stu-id="ba83a-138">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="ba83a-139">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="ba83a-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="ba83a-140">sí</span><span class="sxs-lookup"><span data-stu-id="ba83a-140">yes</span></span>                 |
| [<span data-ttu-id="ba83a-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ba83a-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ba83a-142">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="ba83a-142">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="ba83a-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba83a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba83a-144">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ba83a-144">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

