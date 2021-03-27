---
title: ldexp (Corecrt, \_ Math. h)
description: Devuelve el resultado de multiplicar el valor especificado por dos, elevado a la potencia del exponente especificado.
ms.assetid: 6d6fee96-f952-4058-a1ac-3abb98dbd540
keywords:
- HLSL de ldexp
topic_type:
- apiref
api_name:
- ldexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731cb5cbf933ea3f8754a7d70b9ef0b7a54e783b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914757"
---
# <a name="ldexp"></a><span data-ttu-id="a39fe-104">ldexp</span><span class="sxs-lookup"><span data-stu-id="a39fe-104">ldexp</span></span>

<span data-ttu-id="a39fe-105">Devuelve el resultado de multiplicar el valor especificado por dos, elevado a la potencia del exponente especificado.</span><span class="sxs-lookup"><span data-stu-id="a39fe-105">Returns the result of multiplying the specified value by two, raised to the power of the specified exponent.</span></span>



| <span data-ttu-id="a39fe-106">*RET* ldexp (*x*, *exp*)</span><span class="sxs-lookup"><span data-stu-id="a39fe-106">*ret* ldexp(*x*, *exp*)</span></span> |
|-------------------------|



 

<span data-ttu-id="a39fe-107">Esta función usa la siguiente fórmula: *x* \* 2 <sup>exp</sup></span><span class="sxs-lookup"><span data-stu-id="a39fe-107">This function uses the following formula: *x* \* 2<sup>exp</sup></span></span>

## <a name="parameters"></a><span data-ttu-id="a39fe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a39fe-108">Parameters</span></span>



| <span data-ttu-id="a39fe-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="a39fe-109">Item</span></span>                                                         | <span data-ttu-id="a39fe-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a39fe-110">Description</span></span>                               |
|--------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="a39fe-111"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="a39fe-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="a39fe-112">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="a39fe-112">\[in\] The specified value.</span></span><br/>    |
| <span data-ttu-id="a39fe-113"><span id="exp"></span><span id="EXP"></span>*consumo*</span><span class="sxs-lookup"><span data-stu-id="a39fe-113"><span id="exp"></span><span id="EXP"></span>*exp*</span></span><br/> | <span data-ttu-id="a39fe-114">\[en \] el exponente especificado.</span><span class="sxs-lookup"><span data-stu-id="a39fe-114">\[in\] The specified exponent.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a39fe-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a39fe-115">Return Value</span></span>

<span data-ttu-id="a39fe-116">Resultado de multiplicar el parámetro *x* por dos, elevado a la potencia del parámetro *exp* .</span><span class="sxs-lookup"><span data-stu-id="a39fe-116">The result of multiplying the *x* parameter by two, raised to the power of the *exp* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="a39fe-117">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="a39fe-117">Type Description</span></span>



| <span data-ttu-id="a39fe-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="a39fe-118">Name</span></span>  | [<span data-ttu-id="a39fe-119">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="a39fe-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="a39fe-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="a39fe-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="a39fe-121">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a39fe-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="a39fe-122">*x*</span><span class="sxs-lookup"><span data-stu-id="a39fe-122">*x*</span></span>   | <span data-ttu-id="a39fe-123">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="a39fe-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="a39fe-124">**flot**</span><span class="sxs-lookup"><span data-stu-id="a39fe-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a39fe-125">cualquiera</span><span class="sxs-lookup"><span data-stu-id="a39fe-125">any</span></span>                            |
| <span data-ttu-id="a39fe-126">*exp*</span><span class="sxs-lookup"><span data-stu-id="a39fe-126">*exp*</span></span> | <span data-ttu-id="a39fe-127">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="a39fe-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="a39fe-128">**flot**</span><span class="sxs-lookup"><span data-stu-id="a39fe-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a39fe-129">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="a39fe-129">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="a39fe-130">*direcc*</span><span class="sxs-lookup"><span data-stu-id="a39fe-130">*ret*</span></span> | <span data-ttu-id="a39fe-131">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="a39fe-131">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="a39fe-132">**flot**</span><span class="sxs-lookup"><span data-stu-id="a39fe-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a39fe-133">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="a39fe-133">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a39fe-134">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a39fe-134">Minimum Shader Model</span></span>

<span data-ttu-id="a39fe-135">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a39fe-135">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a39fe-136">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a39fe-136">Shader Model</span></span>                                                                       | <span data-ttu-id="a39fe-137">Compatible</span><span class="sxs-lookup"><span data-stu-id="a39fe-137">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="a39fe-138">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="a39fe-138">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="a39fe-139">sí</span><span class="sxs-lookup"><span data-stu-id="a39fe-139">yes</span></span>                 |
| [<span data-ttu-id="a39fe-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a39fe-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="a39fe-141">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="a39fe-141">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a39fe-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a39fe-142">Requirements</span></span>



| <span data-ttu-id="a39fe-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="a39fe-143">Requirement</span></span> | <span data-ttu-id="a39fe-144">Value</span><span class="sxs-lookup"><span data-stu-id="a39fe-144">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a39fe-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a39fe-145">Header</span></span><br/> | <dl> <span data-ttu-id="a39fe-146"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a39fe-146"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a39fe-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="a39fe-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a39fe-148">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a39fe-148">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

