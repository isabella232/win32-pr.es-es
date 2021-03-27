---
title: pow
description: Devuelve el valor especificado elevado a la potencia especificada.
ms.assetid: 1d64452c-81c7-4ef5-a332-13e0263c2cd1
keywords:
- HLSL de Pow
topic_type:
- apiref
api_name:
- pow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f190c374b6c0ac42d41862eb918f0c0482b6d785
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488210"
---
# <a name="pow"></a><span data-ttu-id="87ac4-104">pow</span><span class="sxs-lookup"><span data-stu-id="87ac4-104">pow</span></span>

<span data-ttu-id="87ac4-105">Devuelve el valor especificado elevado a la potencia especificada.</span><span class="sxs-lookup"><span data-stu-id="87ac4-105">Returns the specified value raised to the specified power.</span></span>



| <span data-ttu-id="87ac4-106">*RET* Pow (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="87ac4-106">*ret* pow(*x*, *y*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="87ac4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87ac4-107">Parameters</span></span>



| <span data-ttu-id="87ac4-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="87ac4-108">Item</span></span>                                                   | <span data-ttu-id="87ac4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="87ac4-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="87ac4-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="87ac4-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="87ac4-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="87ac4-111">\[in\] The specified value.</span></span><br/> |
| <span data-ttu-id="87ac4-112"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="87ac4-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="87ac4-113">\[con \] la potencia especificada.</span><span class="sxs-lookup"><span data-stu-id="87ac4-113">\[in\] The specified power.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="87ac4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87ac4-114">Return Value</span></span>

<span data-ttu-id="87ac4-115">Parámetro *x* elevado a la potencia del parámetro *y* .</span><span class="sxs-lookup"><span data-stu-id="87ac4-115">The *x* parameter raised to the power of the *y* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="87ac4-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87ac4-116">Remarks</span></span>

<span data-ttu-id="87ac4-117">La función intrínseca de el HLSL de **Pow** calcula *x*<sup>y</sup>.</span><span class="sxs-lookup"><span data-stu-id="87ac4-117">The **pow** HLSL intrinsic function calculates *x*<sup>y</sup>.</span></span>



| <span data-ttu-id="87ac4-118">X</span><span class="sxs-lookup"><span data-stu-id="87ac4-118">X</span></span>      | <span data-ttu-id="87ac4-119">Y</span><span class="sxs-lookup"><span data-stu-id="87ac4-119">Y</span></span>      | <span data-ttu-id="87ac4-120">Resultado</span><span class="sxs-lookup"><span data-stu-id="87ac4-120">Result</span></span>                                                                      |
|--------|--------|-----------------------------------------------------------------------------|
| <span data-ttu-id="87ac4-121">< 0</span><span class="sxs-lookup"><span data-stu-id="87ac4-121">< 0</span></span> | <span data-ttu-id="87ac4-122">cualquiera</span><span class="sxs-lookup"><span data-stu-id="87ac4-122">any</span></span>    | <span data-ttu-id="87ac4-123">NAN</span><span class="sxs-lookup"><span data-stu-id="87ac4-123">NAN</span></span>                                                                         |
| <span data-ttu-id="87ac4-124">>0</span><span class="sxs-lookup"><span data-stu-id="87ac4-124">> 0</span></span> | <span data-ttu-id="87ac4-125">= = 0</span><span class="sxs-lookup"><span data-stu-id="87ac4-125">== 0</span></span>   | <span data-ttu-id="87ac4-126">1</span><span class="sxs-lookup"><span data-stu-id="87ac4-126">1</span></span>                                                                           |
| <span data-ttu-id="87ac4-127">= = 0</span><span class="sxs-lookup"><span data-stu-id="87ac4-127">== 0</span></span>   | <span data-ttu-id="87ac4-128">>0</span><span class="sxs-lookup"><span data-stu-id="87ac4-128">> 0</span></span> | <span data-ttu-id="87ac4-129">0</span><span class="sxs-lookup"><span data-stu-id="87ac4-129">0</span></span>                                                                           |
| <span data-ttu-id="87ac4-130">= = 0</span><span class="sxs-lookup"><span data-stu-id="87ac4-130">== 0</span></span>   | <span data-ttu-id="87ac4-131">< 0</span><span class="sxs-lookup"><span data-stu-id="87ac4-131">< 0</span></span> | <span data-ttu-id="87ac4-132">inf</span><span class="sxs-lookup"><span data-stu-id="87ac4-132">inf</span></span>                                                                         |
| <span data-ttu-id="87ac4-133">>0</span><span class="sxs-lookup"><span data-stu-id="87ac4-133">> 0</span></span> | <span data-ttu-id="87ac4-134">< 0</span><span class="sxs-lookup"><span data-stu-id="87ac4-134">< 0</span></span> | <span data-ttu-id="87ac4-135">1/X<sup>-y</sup></span><span class="sxs-lookup"><span data-stu-id="87ac4-135">1/X<sup>-Y</sup></span></span>                                                            |
| <span data-ttu-id="87ac4-136">= = 0</span><span class="sxs-lookup"><span data-stu-id="87ac4-136">== 0</span></span>   | <span data-ttu-id="87ac4-137">= = 0</span><span class="sxs-lookup"><span data-stu-id="87ac4-137">== 0</span></span>   | <span data-ttu-id="87ac4-138">Depende del procesador de gráficos concreto</span><span class="sxs-lookup"><span data-stu-id="87ac4-138">Depends on the particular graphics processor</span></span><br/> <span data-ttu-id="87ac4-139">0, 1 o NAN</span><span class="sxs-lookup"><span data-stu-id="87ac4-139">0, or 1, or NAN</span></span><br/> |



 

## <a name="type-description"></a><span data-ttu-id="87ac4-140">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="87ac4-140">Type Description</span></span>



| <span data-ttu-id="87ac4-141">Nombre</span><span class="sxs-lookup"><span data-stu-id="87ac4-141">Name</span></span>  | [<span data-ttu-id="87ac4-142">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="87ac4-142">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="87ac4-143">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="87ac4-143">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="87ac4-144">Tamaño</span><span class="sxs-lookup"><span data-stu-id="87ac4-144">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="87ac4-145">*x*</span><span class="sxs-lookup"><span data-stu-id="87ac4-145">*x*</span></span>   | <span data-ttu-id="87ac4-146">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="87ac4-146">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="87ac4-147">**flot**</span><span class="sxs-lookup"><span data-stu-id="87ac4-147">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="87ac4-148">cualquiera</span><span class="sxs-lookup"><span data-stu-id="87ac4-148">any</span></span>                            |
| <span data-ttu-id="87ac4-149">*y*</span><span class="sxs-lookup"><span data-stu-id="87ac4-149">*y*</span></span>   | <span data-ttu-id="87ac4-150">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="87ac4-150">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="87ac4-151">**flot**</span><span class="sxs-lookup"><span data-stu-id="87ac4-151">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="87ac4-152">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="87ac4-152">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="87ac4-153">*direcc*</span><span class="sxs-lookup"><span data-stu-id="87ac4-153">*ret*</span></span> | <span data-ttu-id="87ac4-154">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="87ac4-154">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="87ac4-155">**flot**</span><span class="sxs-lookup"><span data-stu-id="87ac4-155">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="87ac4-156">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="87ac4-156">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="87ac4-157">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="87ac4-157">Minimum Shader Model</span></span>

<span data-ttu-id="87ac4-158">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="87ac4-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="87ac4-159">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="87ac4-159">Shader Model</span></span>                                                                       | <span data-ttu-id="87ac4-160">Compatible</span><span class="sxs-lookup"><span data-stu-id="87ac4-160">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="87ac4-161">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="87ac4-161">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="87ac4-162">sí</span><span class="sxs-lookup"><span data-stu-id="87ac4-162">yes</span></span>                 |
| [<span data-ttu-id="87ac4-163">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="87ac4-163">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="87ac4-164">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="87ac4-164">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="87ac4-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="87ac4-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ac4-166">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="87ac4-166">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

