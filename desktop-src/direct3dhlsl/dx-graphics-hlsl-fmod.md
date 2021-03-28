---
title: fmod (Corecrt, \_ Math. h)
description: Devuelve el resto de punto flotante de x/y.
ms.assetid: bb940548-c4c5-4109-a488-4ea7295c7213
keywords:
- HLSL de fmod
topic_type:
- apiref
api_name:
- fmod
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9dc4367e3aa80484098e88926567953fc8e9a90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362547"
---
# <a name="fmod"></a><span data-ttu-id="69ce8-104">fmod</span><span class="sxs-lookup"><span data-stu-id="69ce8-104">fmod</span></span>

<span data-ttu-id="69ce8-105">Devuelve el resto de punto flotante de x/y.</span><span class="sxs-lookup"><span data-stu-id="69ce8-105">Returns the floating-point remainder of x/y.</span></span>



| <span data-ttu-id="69ce8-106">*RET* FMOD (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="69ce8-106">*ret* fmod(*x*, *y*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="69ce8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69ce8-107">Parameters</span></span>



| <span data-ttu-id="69ce8-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="69ce8-108">Item</span></span>                                                   | <span data-ttu-id="69ce8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="69ce8-109">Description</span></span>                                    |
|--------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="69ce8-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="69ce8-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="69ce8-111">\[en \] el dividendo de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="69ce8-111">\[in\] The floating-point dividend.</span></span><br/> |
| <span data-ttu-id="69ce8-112"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="69ce8-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="69ce8-113">\[en \] el divisor de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="69ce8-113">\[in\] The floating-point divisor.</span></span><br/>  |



 

## <a name="return-value"></a><span data-ttu-id="69ce8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69ce8-114">Return Value</span></span>

<span data-ttu-id="69ce8-115">El resto de punto flotante del parámetro *x* dividido por el parámetro *y* .</span><span class="sxs-lookup"><span data-stu-id="69ce8-115">The floating-point remainder of the *x* parameter divided by the *y* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="69ce8-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69ce8-116">Remarks</span></span>

<span data-ttu-id="69ce8-117">El resto de punto flotante se calcula de forma que x = i \* y + f, donde i es un entero, f tiene el mismo signo que x y el valor absoluto de f es menor que el valor absoluto de y.</span><span class="sxs-lookup"><span data-stu-id="69ce8-117">The floating-point remainder is calculated such that x = i \* y + f, where i is an integer, f has the same sign as x, and the absolute value of f is less than the absolute value of y.</span></span>

## <a name="type-description"></a><span data-ttu-id="69ce8-118">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="69ce8-118">Type Description</span></span>



| <span data-ttu-id="69ce8-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="69ce8-119">Name</span></span>  | [<span data-ttu-id="69ce8-120">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="69ce8-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="69ce8-121">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="69ce8-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="69ce8-122">Tamaño</span><span class="sxs-lookup"><span data-stu-id="69ce8-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="69ce8-123">*x*</span><span class="sxs-lookup"><span data-stu-id="69ce8-123">*x*</span></span>   | <span data-ttu-id="69ce8-124">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="69ce8-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="69ce8-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="69ce8-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="69ce8-126">cualquiera</span><span class="sxs-lookup"><span data-stu-id="69ce8-126">any</span></span>                            |
| <span data-ttu-id="69ce8-127">*y*</span><span class="sxs-lookup"><span data-stu-id="69ce8-127">*y*</span></span>   | <span data-ttu-id="69ce8-128">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="69ce8-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="69ce8-129">**flot**</span><span class="sxs-lookup"><span data-stu-id="69ce8-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="69ce8-130">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="69ce8-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="69ce8-131">*direcc*</span><span class="sxs-lookup"><span data-stu-id="69ce8-131">*ret*</span></span> | <span data-ttu-id="69ce8-132">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="69ce8-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="69ce8-133">**flot**</span><span class="sxs-lookup"><span data-stu-id="69ce8-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="69ce8-134">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="69ce8-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="69ce8-135">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="69ce8-135">Minimum Shader Model</span></span>

<span data-ttu-id="69ce8-136">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="69ce8-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="69ce8-137">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="69ce8-137">Shader Model</span></span>                                                                       | <span data-ttu-id="69ce8-138">Compatible</span><span class="sxs-lookup"><span data-stu-id="69ce8-138">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="69ce8-139">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="69ce8-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="69ce8-140">sí</span><span class="sxs-lookup"><span data-stu-id="69ce8-140">yes</span></span>       |
| [<span data-ttu-id="69ce8-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69ce8-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="69ce8-142">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="69ce8-142">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="69ce8-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69ce8-143">Requirements</span></span>



| <span data-ttu-id="69ce8-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="69ce8-144">Requirement</span></span> | <span data-ttu-id="69ce8-145">Value</span><span class="sxs-lookup"><span data-stu-id="69ce8-145">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="69ce8-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69ce8-146">Header</span></span><br/> | <dl> <span data-ttu-id="69ce8-147"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="69ce8-147"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69ce8-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="69ce8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ce8-149">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="69ce8-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

