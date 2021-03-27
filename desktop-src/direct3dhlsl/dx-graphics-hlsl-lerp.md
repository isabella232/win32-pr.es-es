---
title: lerp
description: Realiza una interpolación lineal.
ms.assetid: e369f182-b5bd-4b7f-aa77-9cfe11033bc4
keywords:
- HLSL de lerp
topic_type:
- apiref
api_name:
- lerp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c7a5251aaf410d7224b87b9ee9a8f0e8a0c947e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997084"
---
# <a name="lerp"></a><span data-ttu-id="01444-104">lerp</span><span class="sxs-lookup"><span data-stu-id="01444-104">lerp</span></span>

<span data-ttu-id="01444-105">Realiza una interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="01444-105">Performs a linear interpolation.</span></span>



| <span data-ttu-id="01444-106">*RET* lerp (*x*, *y*, *s*)</span><span class="sxs-lookup"><span data-stu-id="01444-106">*ret* lerp(*x*, *y*, *s*)</span></span> |
|---------------------------|



 

## <a name="parameters"></a><span data-ttu-id="01444-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01444-107">Parameters</span></span>



| <span data-ttu-id="01444-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="01444-108">Item</span></span>                                                   | <span data-ttu-id="01444-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="01444-109">Description</span></span>                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01444-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="01444-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="01444-111">\[en \] el primer valor de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="01444-111">\[in\] The first-floating point value.</span></span><br/>                                                     |
| <span data-ttu-id="01444-112"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="01444-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="01444-113">\[en \] el segundo valor de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="01444-113">\[in\] The second-floating point value.</span></span><br/>                                                    |
| <span data-ttu-id="01444-114"><span id="s"></span><span id="S"></span>*seg*</span><span class="sxs-lookup"><span data-stu-id="01444-114"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="01444-115">\[en \] un valor que se interpola linealmente entre el parámetro *x* y el parámetro *y* .</span><span class="sxs-lookup"><span data-stu-id="01444-115">\[in\] A value that linearly interpolates between the *x* parameter and the *y* parameter.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="01444-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01444-116">Return Value</span></span>

<span data-ttu-id="01444-117">Resultado de la interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="01444-117">The result of the linear interpolation.</span></span>

## <a name="type-description"></a><span data-ttu-id="01444-118">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="01444-118">Type Description</span></span>



| <span data-ttu-id="01444-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="01444-119">Name</span></span>  | [<span data-ttu-id="01444-120">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="01444-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="01444-121">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="01444-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="01444-122">Tamaño</span><span class="sxs-lookup"><span data-stu-id="01444-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="01444-123">*x*</span><span class="sxs-lookup"><span data-stu-id="01444-123">*x*</span></span>   | <span data-ttu-id="01444-124">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="01444-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="01444-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="01444-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="01444-126">cualquiera</span><span class="sxs-lookup"><span data-stu-id="01444-126">any</span></span>                            |
| <span data-ttu-id="01444-127">*y*</span><span class="sxs-lookup"><span data-stu-id="01444-127">*y*</span></span>   | <span data-ttu-id="01444-128">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="01444-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="01444-129">**flot**</span><span class="sxs-lookup"><span data-stu-id="01444-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="01444-130">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="01444-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="01444-131">*s*</span><span class="sxs-lookup"><span data-stu-id="01444-131">*s*</span></span>   | <span data-ttu-id="01444-132">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="01444-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="01444-133">**flot**</span><span class="sxs-lookup"><span data-stu-id="01444-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="01444-134">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="01444-134">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="01444-135">*direcc*</span><span class="sxs-lookup"><span data-stu-id="01444-135">*ret*</span></span> | <span data-ttu-id="01444-136">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="01444-136">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="01444-137">**flot**</span><span class="sxs-lookup"><span data-stu-id="01444-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="01444-138">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="01444-138">same dimension(s) as input *x*</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="01444-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01444-139">Remarks</span></span>

<span data-ttu-id="01444-140">La interpolación lineal se basa en la fórmula siguiente: x \* (1-s) + y, \* que se puede escribir de forma equivalente como x + s (y-x).</span><span class="sxs-lookup"><span data-stu-id="01444-140">Linear interpolation is based on the following formula: x\*(1-s) + y\*s which can equivalently be written as x + s(y-x).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="01444-141">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="01444-141">Minimum Shader Model</span></span>

<span data-ttu-id="01444-142">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="01444-142">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="01444-143">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="01444-143">Shader Model</span></span>                                                                       | <span data-ttu-id="01444-144">Compatible</span><span class="sxs-lookup"><span data-stu-id="01444-144">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="01444-145">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="01444-145">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="01444-146">sí</span><span class="sxs-lookup"><span data-stu-id="01444-146">yes</span></span>                         |
| [<span data-ttu-id="01444-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01444-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="01444-148">sí (vs \_ 1 1 \_ y PS \_ 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="01444-148">yes (vs\_1\_1 and ps\_1\_1)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="01444-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="01444-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01444-150">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="01444-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

