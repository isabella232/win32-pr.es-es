---
title: refract
description: Devuelve un vector de refracción mediante un rayo de entrada, una normal de superficie y un índice de refracción.
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- HLSL de refract
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e499d078a020ade1ff9ff2566c3fd15b2a820d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997152"
---
# <a name="refract"></a><span data-ttu-id="7147b-104">refract</span><span class="sxs-lookup"><span data-stu-id="7147b-104">refract</span></span>

<span data-ttu-id="7147b-105">Devuelve un vector de refracción mediante un rayo de entrada, una normal de superficie y un índice de refracción.</span><span class="sxs-lookup"><span data-stu-id="7147b-105">Returns a refraction vector using an entering ray, a surface normal, and a refraction index.</span></span>



| <span data-ttu-id="7147b-106">*RET* refract (*i*, *n*,?)</span><span class="sxs-lookup"><span data-stu-id="7147b-106">*ret* refract(*i*, *n*, ?)</span></span> |
|----------------------------|



 

## <a name="parameters"></a><span data-ttu-id="7147b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7147b-107">Parameters</span></span>



| <span data-ttu-id="7147b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="7147b-108">Item</span></span>                                                   | <span data-ttu-id="7147b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7147b-109">Description</span></span>                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7147b-110"><span id="i"></span><span id="I"></span>*Configur*</span><span class="sxs-lookup"><span data-stu-id="7147b-110"><span id="i"></span><span id="I"></span>*i*</span></span><br/> | <span data-ttu-id="7147b-111">\[en \] un vector de dirección de rayo de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="7147b-111">\[in\] A floating-point, ray direction vector.</span></span><br/>    |
| <span data-ttu-id="7147b-112"><span id="n"></span><span id="N"></span>*n*</span><span class="sxs-lookup"><span data-stu-id="7147b-112"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="7147b-113">\[en \] un vector normal de superficie de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="7147b-113">\[in\] A floating-point, surface normal vector.</span></span><br/>   |
| <span data-ttu-id="7147b-114">*?*</span><span class="sxs-lookup"><span data-stu-id="7147b-114">*?*</span></span><br/>                                         | <span data-ttu-id="7147b-115">\[en \] un punto flotante, el índice de refracción es escalar.</span><span class="sxs-lookup"><span data-stu-id="7147b-115">\[in\] A floating-point, refraction index scalar.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="7147b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7147b-116">Return Value</span></span>

<span data-ttu-id="7147b-117">Un vector de refracción de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="7147b-117">A floating-point, refraction vector.</span></span> <span data-ttu-id="7147b-118">Si el ángulo entre la entrada del rayo i y la superficie normal n es demasiado grande para un índice de refracción determinado, el valor devuelto es (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="7147b-118">If the angle between the entering ray i and the surface normal n is too great for a given refraction index ?, the return value is (0,0,0).</span></span>

## <a name="type-description"></a><span data-ttu-id="7147b-119">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="7147b-119">Type Description</span></span>



| <span data-ttu-id="7147b-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="7147b-120">Name</span></span>              | [<span data-ttu-id="7147b-121">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="7147b-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="7147b-122">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="7147b-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="7147b-123">Tamaño</span><span class="sxs-lookup"><span data-stu-id="7147b-123">Size</span></span>                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="7147b-124">*i*</span><span class="sxs-lookup"><span data-stu-id="7147b-124">*i*</span></span>               | [<span data-ttu-id="7147b-125">**medios**</span><span class="sxs-lookup"><span data-stu-id="7147b-125">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="7147b-126">**flot**</span><span class="sxs-lookup"><span data-stu-id="7147b-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7147b-127">cualquiera</span><span class="sxs-lookup"><span data-stu-id="7147b-127">any</span></span>                            |
| <span data-ttu-id="7147b-128">*n*</span><span class="sxs-lookup"><span data-stu-id="7147b-128">*n*</span></span>               | [<span data-ttu-id="7147b-129">**medios**</span><span class="sxs-lookup"><span data-stu-id="7147b-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="7147b-130">**flot**</span><span class="sxs-lookup"><span data-stu-id="7147b-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7147b-131">mismas dimensiones que la entrada *i*</span><span class="sxs-lookup"><span data-stu-id="7147b-131">same dimension(s) as input *i*</span></span> |
| <span data-ttu-id="7147b-132">?</span><span class="sxs-lookup"><span data-stu-id="7147b-132">?</span></span>                 | [<span data-ttu-id="7147b-133">**escalar**</span><span class="sxs-lookup"><span data-stu-id="7147b-133">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="7147b-134">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="7147b-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7147b-135">1</span><span class="sxs-lookup"><span data-stu-id="7147b-135">1</span></span>                              |
| <span data-ttu-id="7147b-136">Vector de refracción</span><span class="sxs-lookup"><span data-stu-id="7147b-136">refraction vector</span></span> | [<span data-ttu-id="7147b-137">**medios**</span><span class="sxs-lookup"><span data-stu-id="7147b-137">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="7147b-138">**flot**</span><span class="sxs-lookup"><span data-stu-id="7147b-138">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7147b-139">mismas dimensiones que la entrada *i*</span><span class="sxs-lookup"><span data-stu-id="7147b-139">same dimension(s) as input *i*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7147b-140">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="7147b-140">Minimum Shader Model</span></span>

<span data-ttu-id="7147b-141">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7147b-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7147b-142">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="7147b-142">Shader Model</span></span>                                                                       | <span data-ttu-id="7147b-143">Compatible</span><span class="sxs-lookup"><span data-stu-id="7147b-143">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="7147b-144">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="7147b-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="7147b-145">sí</span><span class="sxs-lookup"><span data-stu-id="7147b-145">yes</span></span>                 |
| [<span data-ttu-id="7147b-146">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7147b-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="7147b-147">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="7147b-147">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="7147b-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="7147b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7147b-149">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7147b-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

