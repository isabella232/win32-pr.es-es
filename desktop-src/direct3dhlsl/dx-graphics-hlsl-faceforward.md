---
title: faceforward
description: Voltea la superficie normal (si es necesario) para cara en una dirección opuesta a i; Devuelve el resultado en n.
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- HLSL de faceforward
topic_type:
- apiref
api_name:
- faceforward
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6a3f035ed4f0d16b500864f941bc4fe5413ff54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149365"
---
# <a name="faceforward"></a><span data-ttu-id="37981-104">faceforward</span><span class="sxs-lookup"><span data-stu-id="37981-104">faceforward</span></span>

<span data-ttu-id="37981-105">Voltea la superficie normal (si es necesario) para cara en una dirección opuesta a i; Devuelve el resultado en n.</span><span class="sxs-lookup"><span data-stu-id="37981-105">Flips the surface-normal (if needed) to face in a direction opposite to i; returns the result in n.</span></span>



| <span data-ttu-id="37981-106">*RET* faceforward (*n*, *i*, *ng*)</span><span class="sxs-lookup"><span data-stu-id="37981-106">*ret* faceforward(*n*, *i*, *ng*)</span></span> |
|-----------------------------------|



 

<span data-ttu-id="37981-107">Esta función usa la siguiente fórmula:-*n*  signo (punto (*i*, *ng*)).</span><span class="sxs-lookup"><span data-stu-id="37981-107">This function uses the following formula: -*n*  sign(dot(*i*, *ng*)).</span></span>

## <a name="parameters"></a><span data-ttu-id="37981-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37981-108">Parameters</span></span>



| <span data-ttu-id="37981-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="37981-109">Item</span></span>                                                      | <span data-ttu-id="37981-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="37981-110">Description</span></span>                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37981-111"><span id="n"></span><span id="N"></span>*n*</span><span class="sxs-lookup"><span data-stu-id="37981-111"><span id="n"></span><span id="N"></span>*n*</span></span><br/>    | <span data-ttu-id="37981-112">\[en \] el vector de la superficie de punto flotante normal.</span><span class="sxs-lookup"><span data-stu-id="37981-112">\[in\] The resulting floating-point surface-normal vector.</span></span><br/>                                           |
| <span data-ttu-id="37981-113"><span id="i"></span><span id="I"></span>*Configur*</span><span class="sxs-lookup"><span data-stu-id="37981-113"><span id="i"></span><span id="I"></span>*i*</span></span><br/>    | <span data-ttu-id="37981-114">\[en \] un vector de incidente de punto flotante que apunta de la posición de la vista a la posición del sombreado.</span><span class="sxs-lookup"><span data-stu-id="37981-114">\[in\] A floating-point, incident vector that points from the view position to the shading position.</span></span><br/> |
| <span data-ttu-id="37981-115"><span id="ng"></span><span id="NG"></span>*natural*</span><span class="sxs-lookup"><span data-stu-id="37981-115"><span id="ng"></span><span id="NG"></span>*ng*</span></span><br/> | <span data-ttu-id="37981-116">\[en \] un vector normal de superficie de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="37981-116">\[in\] A floating-point surface-normal vector.</span></span><br/>                                                       |



 

## <a name="return-value"></a><span data-ttu-id="37981-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37981-117">Return Value</span></span>

<span data-ttu-id="37981-118">Vector normal de superficie de punto flotante que está orientado A la dirección de la vista.</span><span class="sxs-lookup"><span data-stu-id="37981-118">A floating-point, surface normal vector that is facing the view direction.</span></span>

## <a name="type-description"></a><span data-ttu-id="37981-119">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="37981-119">Type Description</span></span>



| <span data-ttu-id="37981-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="37981-120">Name</span></span>  | [<span data-ttu-id="37981-121">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="37981-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="37981-122">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="37981-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="37981-123">Tamaño</span><span class="sxs-lookup"><span data-stu-id="37981-123">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="37981-124">*n*</span><span class="sxs-lookup"><span data-stu-id="37981-124">*n*</span></span>   | [<span data-ttu-id="37981-125">**medios**</span><span class="sxs-lookup"><span data-stu-id="37981-125">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="37981-126">**flot**</span><span class="sxs-lookup"><span data-stu-id="37981-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="37981-127">cualquiera</span><span class="sxs-lookup"><span data-stu-id="37981-127">any</span></span>                            |
| <span data-ttu-id="37981-128">*i*</span><span class="sxs-lookup"><span data-stu-id="37981-128">*i*</span></span>   | [<span data-ttu-id="37981-129">**medios**</span><span class="sxs-lookup"><span data-stu-id="37981-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="37981-130">**flot**</span><span class="sxs-lookup"><span data-stu-id="37981-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="37981-131">mismas dimensiones que la entrada *n*</span><span class="sxs-lookup"><span data-stu-id="37981-131">same dimension(s) as input *n*</span></span> |
| <span data-ttu-id="37981-132">*natural*</span><span class="sxs-lookup"><span data-stu-id="37981-132">*ng*</span></span>  | [<span data-ttu-id="37981-133">**medios**</span><span class="sxs-lookup"><span data-stu-id="37981-133">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="37981-134">**flot**</span><span class="sxs-lookup"><span data-stu-id="37981-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="37981-135">mismas dimensiones que la entrada *n*</span><span class="sxs-lookup"><span data-stu-id="37981-135">same dimensions as input *n*</span></span>   |
| <span data-ttu-id="37981-136">*direcc*</span><span class="sxs-lookup"><span data-stu-id="37981-136">*ret*</span></span> | [<span data-ttu-id="37981-137">**medios**</span><span class="sxs-lookup"><span data-stu-id="37981-137">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="37981-138">**flot**</span><span class="sxs-lookup"><span data-stu-id="37981-138">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="37981-139">mismas dimensiones que la entrada *n*</span><span class="sxs-lookup"><span data-stu-id="37981-139">same dimensions as input *n*</span></span>   |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="37981-140">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="37981-140">Minimum Shader Model</span></span>

<span data-ttu-id="37981-141">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="37981-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="37981-142">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="37981-142">Shader Model</span></span>                                                                       | <span data-ttu-id="37981-143">Compatible</span><span class="sxs-lookup"><span data-stu-id="37981-143">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="37981-144">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="37981-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="37981-145">sí</span><span class="sxs-lookup"><span data-stu-id="37981-145">yes</span></span>                   |
| [<span data-ttu-id="37981-146">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="37981-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="37981-147">vs \_ 1 \_ 1 y PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="37981-147">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="37981-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="37981-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37981-149">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="37981-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

