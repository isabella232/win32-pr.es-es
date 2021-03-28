---
title: smoothstep (
description: Devuelve una interpolación Smooth Hermite entre 0 y 1, si x está en el intervalo \ min, Max \.
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- HLSL de smoothstep (
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64e828b52a4d4517e53ba1f1aaf0f687255ad02b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104983995"
---
# <a name="smoothstep"></a><span data-ttu-id="362c2-104">smoothstep (</span><span class="sxs-lookup"><span data-stu-id="362c2-104">smoothstep</span></span>

<span data-ttu-id="362c2-105">Devuelve una interpolación Smooth Hermite entre 0 y 1, si *x* está en el intervalo \[ *min*, *Max* \] .</span><span class="sxs-lookup"><span data-stu-id="362c2-105">Returns a smooth Hermite interpolation between 0 and 1, if *x* is in the range \[*min*, *max*\].</span></span>



| <span data-ttu-id="362c2-106">*RET* smoothstep ((*min*, *Max*, *x*)</span><span class="sxs-lookup"><span data-stu-id="362c2-106">*ret* smoothstep(*min*, *max*, *x*)</span></span> |
|-------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="362c2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="362c2-107">Parameters</span></span>



| <span data-ttu-id="362c2-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="362c2-108">Item</span></span>                                                         | <span data-ttu-id="362c2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="362c2-109">Description</span></span>                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="362c2-110"><span id="min"></span><span id="MIN"></span>*minuto*</span><span class="sxs-lookup"><span data-stu-id="362c2-110"><span id="min"></span><span id="MIN"></span>*min*</span></span><br/> | <span data-ttu-id="362c2-111">\[en \] el intervalo mínimo del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="362c2-111">\[in\] The minimum range of the *x* parameter.</span></span><br/> |
| <span data-ttu-id="362c2-112"><span id="max"></span><span id="MAX"></span>*máx.*</span><span class="sxs-lookup"><span data-stu-id="362c2-112"><span id="max"></span><span id="MAX"></span>*max*</span></span><br/> | <span data-ttu-id="362c2-113">\[en \] el intervalo máximo del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="362c2-113">\[in\] The maximum range of the *x* parameter.</span></span><br/> |
| <span data-ttu-id="362c2-114"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="362c2-114"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="362c2-115">\[en \] el valor especificado que se va a interpolar.</span><span class="sxs-lookup"><span data-stu-id="362c2-115">\[in\] The specified value to be interpolated.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="362c2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="362c2-116">Return Value</span></span>

<span data-ttu-id="362c2-117">Devuelve 0 si *x* es menor que *min*; 1 si *x* es mayor que el *máximo*; de lo contrario, un valor comprendido entre 0 y 1 si *x* está en el intervalo \[ *min*, *Max* \] .</span><span class="sxs-lookup"><span data-stu-id="362c2-117">Returns 0 if *x* is less than *min*; 1 if *x* is greater than *max*; otherwise, a value between 0 and 1 if *x* is in the range \[*min*, *max*\].</span></span>

## <a name="remarks"></a><span data-ttu-id="362c2-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="362c2-118">Remarks</span></span>

<span data-ttu-id="362c2-119">Use la función intrínseca **smoothstep (** HLSL para crear una transición fluida entre dos valores.</span><span class="sxs-lookup"><span data-stu-id="362c2-119">Use the **smoothstep** HLSL intrinsic function to create a smooth transition between two values.</span></span> <span data-ttu-id="362c2-120">Por ejemplo, puede usar esta función para mezclar dos colores sin problemas.</span><span class="sxs-lookup"><span data-stu-id="362c2-120">For example, you can use this function to blend two colors smoothly.</span></span>

## <a name="type-description"></a><span data-ttu-id="362c2-121">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="362c2-121">Type Description</span></span>



| <span data-ttu-id="362c2-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="362c2-122">Name</span></span>  | [<span data-ttu-id="362c2-123">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="362c2-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="362c2-124">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="362c2-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="362c2-125">Tamaño</span><span class="sxs-lookup"><span data-stu-id="362c2-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="362c2-126">*x*</span><span class="sxs-lookup"><span data-stu-id="362c2-126">*x*</span></span>   | <span data-ttu-id="362c2-127">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="362c2-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="362c2-128">**flot**</span><span class="sxs-lookup"><span data-stu-id="362c2-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="362c2-129">cualquiera</span><span class="sxs-lookup"><span data-stu-id="362c2-129">any</span></span>                            |
| <span data-ttu-id="362c2-130">*min*</span><span class="sxs-lookup"><span data-stu-id="362c2-130">*min*</span></span> | <span data-ttu-id="362c2-131">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="362c2-131">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="362c2-132">**flot**</span><span class="sxs-lookup"><span data-stu-id="362c2-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="362c2-133">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="362c2-133">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="362c2-134">*max*</span><span class="sxs-lookup"><span data-stu-id="362c2-134">*max*</span></span> | <span data-ttu-id="362c2-135">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="362c2-135">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="362c2-136">**flot**</span><span class="sxs-lookup"><span data-stu-id="362c2-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="362c2-137">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="362c2-137">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="362c2-138">*direcc*</span><span class="sxs-lookup"><span data-stu-id="362c2-138">*ret*</span></span> | <span data-ttu-id="362c2-139">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="362c2-139">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="362c2-140">**flot**</span><span class="sxs-lookup"><span data-stu-id="362c2-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="362c2-141">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="362c2-141">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="362c2-142">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="362c2-142">Minimum Shader Model</span></span>

<span data-ttu-id="362c2-143">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="362c2-143">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="362c2-144">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="362c2-144">Shader Model</span></span>                                                                       | <span data-ttu-id="362c2-145">Compatible</span><span class="sxs-lookup"><span data-stu-id="362c2-145">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="362c2-146">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="362c2-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="362c2-147">sí</span><span class="sxs-lookup"><span data-stu-id="362c2-147">yes</span></span>                 |
| [<span data-ttu-id="362c2-148">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="362c2-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="362c2-149">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="362c2-149">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="362c2-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="362c2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="362c2-151">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="362c2-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

