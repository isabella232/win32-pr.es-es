---
title: fwidth
description: Devuelve el valor absoluto de los derivados parciales del valor especificado.
ms.assetid: 7184c3b4-1720-4176-a494-7f73322a918e
keywords:
- HLSL de fwidth
topic_type:
- apiref
api_name:
- fwidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf2d5a34e1f387aadb3b044ddd1264616a61109b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149476"
---
# <a name="fwidth"></a><span data-ttu-id="4eaee-104">fwidth</span><span class="sxs-lookup"><span data-stu-id="4eaee-104">fwidth</span></span>

<span data-ttu-id="4eaee-105">Devuelve el valor absoluto de los derivados parciales del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="4eaee-105">Returns the absolute value of the partial derivatives of the specified value.</span></span>



| <span data-ttu-id="4eaee-106">*RET* fwidth (*x*)</span><span class="sxs-lookup"><span data-stu-id="4eaee-106">*ret* fwidth(*x*)</span></span> |
|-------------------|



 

<span data-ttu-id="4eaee-107">Esta función calcula lo siguiente: [**ABS**](dx-graphics-hlsl-abs.md)([**DDX**](dx-graphics-hlsl-ddx.md)(*x*)) + [**ABS**](dx-graphics-hlsl-abs.md)([**DDY**](dx-graphics-hlsl-ddy.md)(*x*)).</span><span class="sxs-lookup"><span data-stu-id="4eaee-107">This function computes the following: [**abs**](dx-graphics-hlsl-abs.md)([**ddx**](dx-graphics-hlsl-ddx.md)(*x*)) + [**abs**](dx-graphics-hlsl-abs.md)([**ddy**](dx-graphics-hlsl-ddy.md)(*x*)).</span></span>

<span data-ttu-id="4eaee-108">Esta función solo se admite en sombreadores de píxeles.</span><span class="sxs-lookup"><span data-stu-id="4eaee-108">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="4eaee-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4eaee-109">Parameters</span></span>



| <span data-ttu-id="4eaee-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="4eaee-110">Item</span></span>                                                   | <span data-ttu-id="4eaee-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4eaee-111">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="4eaee-112"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="4eaee-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="4eaee-113">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="4eaee-113">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4eaee-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4eaee-114">Return Value</span></span>

<span data-ttu-id="4eaee-115">Valor absoluto de los derivados parciales del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="4eaee-115">The absolute value of the partial derivatives of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="4eaee-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="4eaee-116">Type Description</span></span>



| <span data-ttu-id="4eaee-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="4eaee-117">Name</span></span>  | [<span data-ttu-id="4eaee-118">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="4eaee-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="4eaee-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="4eaee-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="4eaee-120">Tamaño</span><span class="sxs-lookup"><span data-stu-id="4eaee-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="4eaee-121">*x*</span><span class="sxs-lookup"><span data-stu-id="4eaee-121">*x*</span></span>   | <span data-ttu-id="4eaee-122">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="4eaee-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="4eaee-123">**flot**</span><span class="sxs-lookup"><span data-stu-id="4eaee-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4eaee-124">cualquiera</span><span class="sxs-lookup"><span data-stu-id="4eaee-124">any</span></span>                            |
| <span data-ttu-id="4eaee-125">*direcc*</span><span class="sxs-lookup"><span data-stu-id="4eaee-125">*ret*</span></span> | <span data-ttu-id="4eaee-126">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="4eaee-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="4eaee-127">**flot**</span><span class="sxs-lookup"><span data-stu-id="4eaee-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4eaee-128">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="4eaee-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4eaee-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="4eaee-129">Minimum Shader Model</span></span>

<span data-ttu-id="4eaee-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4eaee-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4eaee-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="4eaee-131">Shader Model</span></span>                                                                       | <span data-ttu-id="4eaee-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="4eaee-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="4eaee-133">Modelador [modelo 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="4eaee-133">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="4eaee-134">sí</span><span class="sxs-lookup"><span data-stu-id="4eaee-134">yes</span></span>                 |
| [<span data-ttu-id="4eaee-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4eaee-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="4eaee-136">sí ( \_ solo PS 2 \_ x)</span><span class="sxs-lookup"><span data-stu-id="4eaee-136">yes (ps\_2\_x only)</span></span> |
| [<span data-ttu-id="4eaee-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4eaee-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="4eaee-138">No</span><span class="sxs-lookup"><span data-stu-id="4eaee-138">no</span></span>                  |



 

## <a name="see-also"></a><span data-ttu-id="4eaee-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="4eaee-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eaee-140">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="4eaee-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

