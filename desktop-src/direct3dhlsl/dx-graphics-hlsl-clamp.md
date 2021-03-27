---
title: Sujet
description: Fija el valor especificado en el intervalo mínimo y máximo especificado.
ms.assetid: bcfafcec-3f9c-4b65-950c-da34184d5cdb
keywords:
- HLSL de abrazadera
topic_type:
- apiref
api_name:
- clamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5d6b0a3e83c0b1a5e511aba96df03b828b90c11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793306"
---
# <a name="clamp"></a><span data-ttu-id="82359-104">Sujet</span><span class="sxs-lookup"><span data-stu-id="82359-104">clamp</span></span>

<span data-ttu-id="82359-105">Fija el valor especificado en el intervalo mínimo y máximo especificado.</span><span class="sxs-lookup"><span data-stu-id="82359-105">Clamps the specified value to the specified minimum and maximum range.</span></span>



| <span data-ttu-id="82359-106">abrazadera *RET* (*x*, *min*, *Max*)</span><span class="sxs-lookup"><span data-stu-id="82359-106">*ret* clamp(*x*, *min*, *max*)</span></span> |
|--------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="82359-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82359-107">Parameters</span></span>



| <span data-ttu-id="82359-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="82359-108">Item</span></span>                                                         | <span data-ttu-id="82359-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="82359-109">Description</span></span>                                    |
|--------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="82359-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="82359-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="82359-111">\[en \] un valor para la abrazadera.</span><span class="sxs-lookup"><span data-stu-id="82359-111">\[in\] A value to clamp.</span></span><br/>            |
| <span data-ttu-id="82359-112"><span id="min"></span><span id="MIN"></span>*minuto*</span><span class="sxs-lookup"><span data-stu-id="82359-112"><span id="min"></span><span id="MIN"></span>*min*</span></span><br/> | <span data-ttu-id="82359-113">\[en \] el intervalo mínimo especificado.</span><span class="sxs-lookup"><span data-stu-id="82359-113">\[in\] The specified minimum range.</span></span><br/> |
| <span data-ttu-id="82359-114"><span id="max"></span><span id="MAX"></span>*máx.*</span><span class="sxs-lookup"><span data-stu-id="82359-114"><span id="max"></span><span id="MAX"></span>*max*</span></span><br/> | <span data-ttu-id="82359-115">\[en \] el intervalo máximo especificado.</span><span class="sxs-lookup"><span data-stu-id="82359-115">\[in\] The specified maximum range.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="82359-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82359-116">Return Value</span></span>

<span data-ttu-id="82359-117">Valor de la abrazadera del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="82359-117">The clamped value for the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="82359-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82359-118">Remarks</span></span>

<span data-ttu-id="82359-119">En el caso de los valores de-INF o INF, la abrazadera se comportará de la manera esperada.</span><span class="sxs-lookup"><span data-stu-id="82359-119">For values of -INF or INF, clamp will behave as expected.</span></span> <span data-ttu-id="82359-120">Sin embargo, para los valores NaN, los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="82359-120">However for values of NaN, the results are undefined.</span></span>

## <a name="type-description"></a><span data-ttu-id="82359-121">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="82359-121">Type Description</span></span>



| <span data-ttu-id="82359-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="82359-122">Name</span></span>  | [<span data-ttu-id="82359-123">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="82359-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="82359-124">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="82359-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="82359-125">Tamaño</span><span class="sxs-lookup"><span data-stu-id="82359-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="82359-126">*x*</span><span class="sxs-lookup"><span data-stu-id="82359-126">*x*</span></span>   | <span data-ttu-id="82359-127">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="82359-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="82359-128">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="82359-128">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="82359-129">cualquiera</span><span class="sxs-lookup"><span data-stu-id="82359-129">any</span></span>                            |
| <span data-ttu-id="82359-130">*min*</span><span class="sxs-lookup"><span data-stu-id="82359-130">*min*</span></span> | <span data-ttu-id="82359-131">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="82359-131">same as input *x*</span></span>                                                                                              | <span data-ttu-id="82359-132">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="82359-132">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="82359-133">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="82359-133">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="82359-134">*max*</span><span class="sxs-lookup"><span data-stu-id="82359-134">*max*</span></span> | <span data-ttu-id="82359-135">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="82359-135">same as input *x*</span></span>                                                                                              | <span data-ttu-id="82359-136">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="82359-136">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="82359-137">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="82359-137">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="82359-138">*direcc*</span><span class="sxs-lookup"><span data-stu-id="82359-138">*ret*</span></span> | <span data-ttu-id="82359-139">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="82359-139">same as input *x*</span></span>                                                                                              | <span data-ttu-id="82359-140">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="82359-140">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="82359-141">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="82359-141">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="82359-142">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="82359-142">Minimum Shader Model</span></span>

<span data-ttu-id="82359-143">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="82359-143">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="82359-144">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="82359-144">Shader Model</span></span>                                                                       | <span data-ttu-id="82359-145">Compatible</span><span class="sxs-lookup"><span data-stu-id="82359-145">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="82359-146">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="82359-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="82359-147">sí</span><span class="sxs-lookup"><span data-stu-id="82359-147">yes</span></span>                   |
| [<span data-ttu-id="82359-148">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82359-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="82359-149">vs \_ 1 \_ 1 y PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="82359-149">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="82359-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="82359-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82359-151">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="82359-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

