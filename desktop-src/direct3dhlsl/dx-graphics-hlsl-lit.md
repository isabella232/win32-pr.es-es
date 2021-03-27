---
title: encender
description: Devuelve un vector de coeficiente de iluminación.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- HLSL Lit
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dbf6f1e53218355ba1ee9ccf58dac6176007218
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904614"
---
# <a name="lit"></a><span data-ttu-id="f3741-104">encender</span><span class="sxs-lookup"><span data-stu-id="f3741-104">lit</span></span>

<span data-ttu-id="f3741-105">Devuelve un vector de coeficiente de iluminación.</span><span class="sxs-lookup"><span data-stu-id="f3741-105">Returns a lighting coefficient vector.</span></span>



| <span data-ttu-id="f3741-106">*RET* Lit (*n \_ punto \_ l*, *n \_ punto \_ h*, *m*)</span><span class="sxs-lookup"><span data-stu-id="f3741-106">*ret* lit(*n\_dot\_l*, *n\_dot\_h*, *m*)</span></span> |
|------------------------------------------|



 

<span data-ttu-id="f3741-107">Esta función devuelve un vector de coeficiente de iluminación (ambiente, difuso, especular, 1) donde:</span><span class="sxs-lookup"><span data-stu-id="f3741-107">This function returns a lighting coefficient vector (ambient, diffuse, specular, 1) where:</span></span>

-   <span data-ttu-id="f3741-108">ambiente = 1</span><span class="sxs-lookup"><span data-stu-id="f3741-108">ambient = 1</span></span>
-   <span data-ttu-id="f3741-109">difuso = n · l < 0?</span><span class="sxs-lookup"><span data-stu-id="f3741-109">diffuse = n · l < 0 ?</span></span> <span data-ttu-id="f3741-110">0: n · CG</span><span class="sxs-lookup"><span data-stu-id="f3741-110">0 : n · l</span></span>
-   <span data-ttu-id="f3741-111">especular = n · l < 0 \| \| n · h < 0?</span><span class="sxs-lookup"><span data-stu-id="f3741-111">specular = n · l < 0 \|\| n · h < 0 ?</span></span> <span data-ttu-id="f3741-112">0: (n · h) ^ m</span><span class="sxs-lookup"><span data-stu-id="f3741-112">0 : (n · h) ^ m</span></span>

<span data-ttu-id="f3741-113">Donde el vector n es el vector normal, l es la dirección que se debe aclarar y h es el vector medio.</span><span class="sxs-lookup"><span data-stu-id="f3741-113">Where the vector n is the normal vector, l is the direction to light and h is the half vector.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3741-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3741-114">Parameters</span></span>



| <span data-ttu-id="f3741-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="f3741-115">Item</span></span>                                                                       | <span data-ttu-id="f3741-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3741-116">Description</span></span>                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3741-117"><span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ punto \_ l*</span><span class="sxs-lookup"><span data-stu-id="f3741-117"><span id="n_dot_l"></span><span id="N_DOT_L"></span>*n\_dot\_l*</span></span><br/> | <span data-ttu-id="f3741-118">\[en \] el producto de punto de la superficie normalizada normal y el vector de luz.</span><span class="sxs-lookup"><span data-stu-id="f3741-118">\[in\] The dot product of the normalized surface normal and the light vector.</span></span><br/> |
| <span data-ttu-id="f3741-119"><span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ punto \_ h*</span><span class="sxs-lookup"><span data-stu-id="f3741-119"><span id="n_dot_h"></span><span id="N_DOT_H"></span>*n\_dot\_h*</span></span><br/> | <span data-ttu-id="f3741-120">\[en \] el producto de puntos del vector de medio ángulo y la superficie normal.</span><span class="sxs-lookup"><span data-stu-id="f3741-120">\[in\] The dot product of the half-angle vector and the surface normal.</span></span><br/>       |
| <span data-ttu-id="f3741-121"><span id="m"></span><span id="M"></span>*f*</span><span class="sxs-lookup"><span data-stu-id="f3741-121"><span id="m"></span><span id="M"></span>*m*</span></span><br/>                     | <span data-ttu-id="f3741-122">\[en \] un exponente especular.</span><span class="sxs-lookup"><span data-stu-id="f3741-122">\[in\] A specular exponent.</span></span><br/>                                                   |



 

## <a name="return-value"></a><span data-ttu-id="f3741-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3741-123">Return Value</span></span>

<span data-ttu-id="f3741-124">Vector de coeficiente de iluminación.</span><span class="sxs-lookup"><span data-stu-id="f3741-124">The lighting coefficient vector.</span></span>

## <a name="type-description"></a><span data-ttu-id="f3741-125">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="f3741-125">Type Description</span></span>



| <span data-ttu-id="f3741-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="f3741-126">Name</span></span>        | [<span data-ttu-id="f3741-127">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="f3741-127">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="f3741-128">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="f3741-128">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="f3741-129">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f3741-129">Size</span></span> |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="f3741-130">*n \_ punto \_ l*</span><span class="sxs-lookup"><span data-stu-id="f3741-130">*n\_dot\_l*</span></span> | [<span data-ttu-id="f3741-131">**escalar**</span><span class="sxs-lookup"><span data-stu-id="f3741-131">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f3741-132">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="f3741-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f3741-133">1</span><span class="sxs-lookup"><span data-stu-id="f3741-133">1</span></span>    |
| <span data-ttu-id="f3741-134">*n \_ punto \_ h*</span><span class="sxs-lookup"><span data-stu-id="f3741-134">*n\_dot\_h*</span></span> | [<span data-ttu-id="f3741-135">**escalar**</span><span class="sxs-lookup"><span data-stu-id="f3741-135">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f3741-136">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="f3741-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f3741-137">1</span><span class="sxs-lookup"><span data-stu-id="f3741-137">1</span></span>    |
| <span data-ttu-id="f3741-138">*m*</span><span class="sxs-lookup"><span data-stu-id="f3741-138">*m*</span></span>         | [<span data-ttu-id="f3741-139">**escalar**</span><span class="sxs-lookup"><span data-stu-id="f3741-139">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f3741-140">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="f3741-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f3741-141">1</span><span class="sxs-lookup"><span data-stu-id="f3741-141">1</span></span>    |
| <span data-ttu-id="f3741-142">*direcc*</span><span class="sxs-lookup"><span data-stu-id="f3741-142">*ret*</span></span>       | [<span data-ttu-id="f3741-143">**medios**</span><span class="sxs-lookup"><span data-stu-id="f3741-143">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f3741-144">**float**</span><span class="sxs-lookup"><span data-stu-id="f3741-144">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f3741-145">4</span><span class="sxs-lookup"><span data-stu-id="f3741-145">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f3741-146">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="f3741-146">Minimum Shader Model</span></span>

<span data-ttu-id="f3741-147">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f3741-147">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f3741-148">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="f3741-148">Shader Model</span></span>                                                                       | <span data-ttu-id="f3741-149">Compatible</span><span class="sxs-lookup"><span data-stu-id="f3741-149">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="f3741-150">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="f3741-150">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="f3741-151">sí</span><span class="sxs-lookup"><span data-stu-id="f3741-151">yes</span></span>                 |
| [<span data-ttu-id="f3741-152">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3741-152">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="f3741-153">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="f3741-153">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="f3741-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3741-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3741-155">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="f3741-155">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

