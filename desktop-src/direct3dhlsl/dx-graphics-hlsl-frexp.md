---
title: frexp ((Corecrt, \_ Math. h)
description: Devuelve la mantisa y el exponente del valor de punto flotante especificado.
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- HLSL de frexp (
topic_type:
- apiref
api_name:
- frexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bddbcbbf9e97aff739bb06a0f0d0ddac12134463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003810"
---
# <a name="frexp"></a><span data-ttu-id="22b31-104">frexp</span><span class="sxs-lookup"><span data-stu-id="22b31-104">frexp</span></span>

<span data-ttu-id="22b31-105">Devuelve la mantisa y el exponente del valor de punto flotante especificado.</span><span class="sxs-lookup"><span data-stu-id="22b31-105">Returns the mantissa and exponent of the specified floating-point value.</span></span>



| <span data-ttu-id="22b31-106">*RET* frexp ((*x*, *exp*)</span><span class="sxs-lookup"><span data-stu-id="22b31-106">*ret* frexp(*x*, *exp*)</span></span> |
|-------------------------|



 

<span data-ttu-id="22b31-107">El valor devuelto es la mantisa y el valor devuelto por el parámetro *exp* es el exponente.</span><span class="sxs-lookup"><span data-stu-id="22b31-107">The return value is the mantissa, and the value returned by *exp* parameter is the exponent.</span></span>

## <a name="parameters"></a><span data-ttu-id="22b31-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22b31-108">Parameters</span></span>



| <span data-ttu-id="22b31-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="22b31-109">Item</span></span>                                                         | <span data-ttu-id="22b31-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="22b31-110">Description</span></span>                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22b31-111"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="22b31-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="22b31-112">\[en \] el valor de punto flotante especificado.</span><span class="sxs-lookup"><span data-stu-id="22b31-112">\[in\] The specified floating-point value.</span></span> <span data-ttu-id="22b31-113">Si el parámetro *x* es 0, esta función devuelve 0 para la mantisa y el exponente.</span><span class="sxs-lookup"><span data-stu-id="22b31-113">If the *x* parameter is 0, this function returns 0 for both the mantissa and the exponent.</span></span><br/> |
| <span data-ttu-id="22b31-114"><span id="exp"></span><span id="EXP"></span>*consumo*</span><span class="sxs-lookup"><span data-stu-id="22b31-114"><span id="exp"></span><span id="EXP"></span>*exp*</span></span><br/> | <span data-ttu-id="22b31-115">\[\]el exponente devuelto del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="22b31-115">\[out\] The returned exponent of the *x* parameter.</span></span><br/>                                                                                   |



 

## <a name="return-value"></a><span data-ttu-id="22b31-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22b31-116">Return Value</span></span>

<span data-ttu-id="22b31-117">La mantisa del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="22b31-117">The mantissa of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="22b31-118">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="22b31-118">Type Description</span></span>



| <span data-ttu-id="22b31-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="22b31-119">Name</span></span>  | [<span data-ttu-id="22b31-120">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="22b31-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="22b31-121">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="22b31-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="22b31-122">Tamaño</span><span class="sxs-lookup"><span data-stu-id="22b31-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="22b31-123">*x*</span><span class="sxs-lookup"><span data-stu-id="22b31-123">*x*</span></span>   | <span data-ttu-id="22b31-124">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="22b31-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="22b31-125">**flot**</span><span class="sxs-lookup"><span data-stu-id="22b31-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="22b31-126">cualquiera</span><span class="sxs-lookup"><span data-stu-id="22b31-126">any</span></span>                            |
| <span data-ttu-id="22b31-127">*exp*</span><span class="sxs-lookup"><span data-stu-id="22b31-127">*exp*</span></span> | <span data-ttu-id="22b31-128">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="22b31-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="22b31-129">**flot**</span><span class="sxs-lookup"><span data-stu-id="22b31-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="22b31-130">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="22b31-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="22b31-131">*direcc*</span><span class="sxs-lookup"><span data-stu-id="22b31-131">*ret*</span></span> | <span data-ttu-id="22b31-132">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="22b31-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="22b31-133">**flot**</span><span class="sxs-lookup"><span data-stu-id="22b31-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="22b31-134">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="22b31-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="22b31-135">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="22b31-135">Minimum Shader Model</span></span>

<span data-ttu-id="22b31-136">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="22b31-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="22b31-137">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="22b31-137">Shader Model</span></span>                                                                       | <span data-ttu-id="22b31-138">Compatible</span><span class="sxs-lookup"><span data-stu-id="22b31-138">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="22b31-139">Modelador [modelo 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="22b31-139">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="22b31-140">sí</span><span class="sxs-lookup"><span data-stu-id="22b31-140">yes</span></span>                 |
| [<span data-ttu-id="22b31-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="22b31-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="22b31-142">sí ( \_ solo PS 2 \_ x)</span><span class="sxs-lookup"><span data-stu-id="22b31-142">yes (ps\_2\_x only)</span></span> |
| [<span data-ttu-id="22b31-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="22b31-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="22b31-144">no</span><span class="sxs-lookup"><span data-stu-id="22b31-144">no</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="22b31-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22b31-145">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="22b31-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22b31-146">Requirements</span></span>



| <span data-ttu-id="22b31-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="22b31-147">Requirement</span></span> | <span data-ttu-id="22b31-148">Value</span><span class="sxs-lookup"><span data-stu-id="22b31-148">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="22b31-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22b31-149">Header</span></span><br/> | <dl> <span data-ttu-id="22b31-150"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="22b31-150"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22b31-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="22b31-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22b31-152">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="22b31-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

