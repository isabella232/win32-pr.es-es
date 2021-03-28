---
title: rcp
description: Calcula un recíproco rápido, aproximado y por componente.
ms.assetid: c8d451e4-717e-45b3-a0fe-da55feb8f443
keywords:
- HLSL de RCP
topic_type:
- apiref
api_name:
- rcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a857c897def08f31e18ef19466daa2b4584740a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792297"
---
# <a name="rcp"></a><span data-ttu-id="be971-104">rcp</span><span class="sxs-lookup"><span data-stu-id="be971-104">rcp</span></span>

<span data-ttu-id="be971-105">Calcula un recíproco rápido, aproximado y por componente.</span><span class="sxs-lookup"><span data-stu-id="be971-105">Calculates a fast, approximate, per-component reciprocal.</span></span>



| <span data-ttu-id="be971-106">*RET* RCP (*x*)</span><span class="sxs-lookup"><span data-stu-id="be971-106">*ret* rcp(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="be971-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be971-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be971-108"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="be971-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="be971-109">\[en \] el valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="be971-109">\[in\] The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be971-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be971-110">Return Value</span></span>

<span data-ttu-id="be971-111">Recíproco del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="be971-111">The reciprocal of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="be971-112">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="be971-112">Type Description</span></span>



| <span data-ttu-id="be971-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="be971-113">Name</span></span>  | [<span data-ttu-id="be971-114">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="be971-114">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="be971-115">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="be971-115">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                      | <span data-ttu-id="be971-116">Tamaño</span><span class="sxs-lookup"><span data-stu-id="be971-116">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="be971-117">*x*</span><span class="sxs-lookup"><span data-stu-id="be971-117">*x*</span></span>   | <span data-ttu-id="be971-118">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="be971-118">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="be971-119">[**float**](/windows/desktop/WinProg/windows-data-types) o [ **Double**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="be971-119">[**float**](/windows/desktop/WinProg/windows-data-types) or [**double**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="be971-120">cualquiera</span><span class="sxs-lookup"><span data-stu-id="be971-120">any</span></span>                            |
| <span data-ttu-id="be971-121">*direcc*</span><span class="sxs-lookup"><span data-stu-id="be971-121">*ret*</span></span> | <span data-ttu-id="be971-122">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="be971-122">same as input *x*</span></span>                                                                                              | <span data-ttu-id="be971-123">[**float**](/windows/desktop/WinProg/windows-data-types) o [ **Double**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="be971-123">[**float**](/windows/desktop/WinProg/windows-data-types) or [**double**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="be971-124">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="be971-124">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="be971-125">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="be971-125">Minimum Shader Model</span></span>

<span data-ttu-id="be971-126">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="be971-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="be971-127">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="be971-127">Shader Model</span></span>                                                                | <span data-ttu-id="be971-128">Compatible</span><span class="sxs-lookup"><span data-stu-id="be971-128">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="be971-129">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="be971-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="be971-130">sí</span><span class="sxs-lookup"><span data-stu-id="be971-130">yes</span></span>       |



 

<span data-ttu-id="be971-131">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="be971-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="be971-132">Vértice</span><span class="sxs-lookup"><span data-stu-id="be971-132">Vertex</span></span> | <span data-ttu-id="be971-133">Casco</span><span class="sxs-lookup"><span data-stu-id="be971-133">Hull</span></span> | <span data-ttu-id="be971-134">Dominio</span><span class="sxs-lookup"><span data-stu-id="be971-134">Domain</span></span> | <span data-ttu-id="be971-135">Geometría</span><span class="sxs-lookup"><span data-stu-id="be971-135">Geometry</span></span> | <span data-ttu-id="be971-136">Píxel</span><span class="sxs-lookup"><span data-stu-id="be971-136">Pixel</span></span> | <span data-ttu-id="be971-137">Compute</span><span class="sxs-lookup"><span data-stu-id="be971-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="be971-138">x</span><span class="sxs-lookup"><span data-stu-id="be971-138">x</span></span>      | <span data-ttu-id="be971-139">x</span><span class="sxs-lookup"><span data-stu-id="be971-139">x</span></span>    | <span data-ttu-id="be971-140">x</span><span class="sxs-lookup"><span data-stu-id="be971-140">x</span></span>      | <span data-ttu-id="be971-141">x</span><span class="sxs-lookup"><span data-stu-id="be971-141">x</span></span>        | <span data-ttu-id="be971-142">x</span><span class="sxs-lookup"><span data-stu-id="be971-142">x</span></span>     | <span data-ttu-id="be971-143">x</span><span class="sxs-lookup"><span data-stu-id="be971-143">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="be971-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="be971-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be971-145">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="be971-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="be971-146">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="be971-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 