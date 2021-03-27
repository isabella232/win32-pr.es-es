---
title: paso
description: Compara dos valores, devolviendo 0 o 1 según el valor que sea mayor.
ms.assetid: 1c1c4ec4-ae97-42ce-99af-71903e0b5edf
keywords:
- paso HLSL
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9c800e8d8c6f78386139f822f118163f3b431f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793294"
---
# <a name="step"></a><span data-ttu-id="b963f-104">paso</span><span class="sxs-lookup"><span data-stu-id="b963f-104">step</span></span>

<span data-ttu-id="b963f-105">Compara dos valores, devolviendo 0 o 1 según el valor que sea mayor.</span><span class="sxs-lookup"><span data-stu-id="b963f-105">Compares two values, returning 0 or 1 based on which value is greater.</span></span>



| <span data-ttu-id="b963f-106">paso *RET* (*y*, *x*)</span><span class="sxs-lookup"><span data-stu-id="b963f-106">*ret* step(*y*, *x*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="b963f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b963f-107">Parameters</span></span>



| <span data-ttu-id="b963f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b963f-108">Item</span></span>                                                   | <span data-ttu-id="b963f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b963f-109">Description</span></span>                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b963f-110"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="b963f-110"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="b963f-111">\[en \] el primer valor de punto flotante que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="b963f-111">\[in\] The first floating-point value to compare.</span></span><br/>  |
| <span data-ttu-id="b963f-112"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="b963f-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b963f-113">\[en \] el segundo valor de punto flotante que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="b963f-113">\[in\] The second floating-point value to compare.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b963f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b963f-114">Return Value</span></span>

<span data-ttu-id="b963f-115">1 si el parámetro *x* es mayor o igual que el parámetro *y* ; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="b963f-115">1 if the *x* parameter is greater than or equal to the *y* parameter; otherwise, 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="b963f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b963f-116">Remarks</span></span>

<span data-ttu-id="b963f-117">Esta función usa la siguiente fórmula: (*x*  >=  *y*)?</span><span class="sxs-lookup"><span data-stu-id="b963f-117">This function uses the following formula: (*x* >= *y*) ?</span></span> <span data-ttu-id="b963f-118">1:0.</span><span class="sxs-lookup"><span data-stu-id="b963f-118">1 : 0.</span></span> <span data-ttu-id="b963f-119">La función devuelve 0 o 1, dependiendo de si el parámetro *x* es mayor que el parámetro *y* .</span><span class="sxs-lookup"><span data-stu-id="b963f-119">The function returns either 0 or 1 depending on whether the *x* parameter is greater than the *y* parameter.</span></span> <span data-ttu-id="b963f-120">Para calcular una interpolación suave entre 0 y 1, use la función intrínseca de HLSL [**smoothstep (**](dx-graphics-hlsl-smoothstep.md) .</span><span class="sxs-lookup"><span data-stu-id="b963f-120">To compute a smooth interpolation between 0 and 1, use the [**smoothstep**](dx-graphics-hlsl-smoothstep.md) HLSL intrinsic function.</span></span>

## <a name="type-description"></a><span data-ttu-id="b963f-121">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="b963f-121">Type Description</span></span>



| <span data-ttu-id="b963f-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="b963f-122">Name</span></span>  | [<span data-ttu-id="b963f-123">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="b963f-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b963f-124">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="b963f-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b963f-125">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b963f-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b963f-126">*y*</span><span class="sxs-lookup"><span data-stu-id="b963f-126">*y*</span></span>   | <span data-ttu-id="b963f-127">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="b963f-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="b963f-128">**flot**</span><span class="sxs-lookup"><span data-stu-id="b963f-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b963f-129">cualquiera</span><span class="sxs-lookup"><span data-stu-id="b963f-129">any</span></span>                            |
| <span data-ttu-id="b963f-130">*x*</span><span class="sxs-lookup"><span data-stu-id="b963f-130">*x*</span></span>   | <span data-ttu-id="b963f-131">igual que la entrada *y*</span><span class="sxs-lookup"><span data-stu-id="b963f-131">same as input *y*</span></span>                                                                                              | [<span data-ttu-id="b963f-132">**flot**</span><span class="sxs-lookup"><span data-stu-id="b963f-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b963f-133">mismas dimensiones como entrada *y*</span><span class="sxs-lookup"><span data-stu-id="b963f-133">same dimension(s) as input *y*</span></span> |
| <span data-ttu-id="b963f-134">*direcc*</span><span class="sxs-lookup"><span data-stu-id="b963f-134">*ret*</span></span> | <span data-ttu-id="b963f-135">igual que la entrada *y*</span><span class="sxs-lookup"><span data-stu-id="b963f-135">same as input *y*</span></span>                                                                                              | [<span data-ttu-id="b963f-136">**flot**</span><span class="sxs-lookup"><span data-stu-id="b963f-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b963f-137">mismas dimensiones como entrada *y*</span><span class="sxs-lookup"><span data-stu-id="b963f-137">same dimension(s) as input *y*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b963f-138">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="b963f-138">Minimum Shader Model</span></span>

<span data-ttu-id="b963f-139">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b963f-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b963f-140">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="b963f-140">Shader Model</span></span>                                                                       | <span data-ttu-id="b963f-141">Compatible</span><span class="sxs-lookup"><span data-stu-id="b963f-141">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="b963f-142">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="b963f-142">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b963f-143">sí</span><span class="sxs-lookup"><span data-stu-id="b963f-143">yes</span></span>                         |
| [<span data-ttu-id="b963f-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b963f-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b963f-145">sí (vs \_ 1 \_ 1 y PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="b963f-145">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="b963f-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="b963f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b963f-147">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b963f-147">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

