---
title: ATAN2 (Corecrt \_ Math. h)
description: Devuelve el arcotangente de dos valores (x, y).
ms.assetid: e7b53751-f321-4390-8f8f-ec1fa3aaa798
keywords:
- HLSL de ATAN2
topic_type:
- apiref
api_name:
- atan2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fbc6574d0fc0d53a165ae7da87c2627a295be4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280310"
---
# <a name="atan2"></a><span data-ttu-id="6357c-104">atan2</span><span class="sxs-lookup"><span data-stu-id="6357c-104">atan2</span></span>

<span data-ttu-id="6357c-105">Devuelve el arcotangente de dos valores (x, y).</span><span class="sxs-lookup"><span data-stu-id="6357c-105">Returns the arctangent of two values (x,y).</span></span>



| <span data-ttu-id="6357c-106">*RET* ATAN2 (*y*, *x*)</span><span class="sxs-lookup"><span data-stu-id="6357c-106">*ret* atan2(*y*, *x*)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="6357c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6357c-107">Parameters</span></span>



| <span data-ttu-id="6357c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6357c-108">Item</span></span>                                                   | <span data-ttu-id="6357c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6357c-109">Description</span></span>                    |
|--------------------------------------------------------|--------------------------------|
| <span data-ttu-id="6357c-110"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="6357c-110"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="6357c-111">\[en \] el valor y.</span><span class="sxs-lookup"><span data-stu-id="6357c-111">\[in\] The y value.</span></span><br/> |
| <span data-ttu-id="6357c-112"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="6357c-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="6357c-113">\[en \] el valor x.</span><span class="sxs-lookup"><span data-stu-id="6357c-113">\[in\] The x value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="6357c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6357c-114">Return Value</span></span>

<span data-ttu-id="6357c-115">Arco tangente de (y, x).</span><span class="sxs-lookup"><span data-stu-id="6357c-115">The arctangent of (y,x).</span></span>

## <a name="remarks"></a><span data-ttu-id="6357c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6357c-116">Remarks</span></span>

<span data-ttu-id="6357c-117">Los signos de los  parámetros x *e y se* usan para determinar el cuadrante de los valores devueltos en el intervalo de-π a π.</span><span class="sxs-lookup"><span data-stu-id="6357c-117">The signs of the *x* and *y* parameters are used to determine the quadrant of the return values within the range of -π to π.</span></span> <span data-ttu-id="6357c-118">La función intrínseca de HLSL **ATAN2** está bien definida para cada punto que no sea el origen, aunque *y* sea igual a 0 y *x* no sea igual a 0.</span><span class="sxs-lookup"><span data-stu-id="6357c-118">The **atan2** HLSL intrinsic function is well-defined for every point other than the origin, even if *y* equals 0 and *x* does not equal 0.</span></span>

## <a name="type-description"></a><span data-ttu-id="6357c-119">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="6357c-119">Type Description</span></span>



| <span data-ttu-id="6357c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="6357c-120">Name</span></span>  | [<span data-ttu-id="6357c-121">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="6357c-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="6357c-122">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="6357c-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="6357c-123">Tamaño</span><span class="sxs-lookup"><span data-stu-id="6357c-123">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="6357c-124">*y*</span><span class="sxs-lookup"><span data-stu-id="6357c-124">*y*</span></span>   | <span data-ttu-id="6357c-125">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="6357c-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="6357c-126">**flot**</span><span class="sxs-lookup"><span data-stu-id="6357c-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6357c-127">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="6357c-127">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="6357c-128">*x*</span><span class="sxs-lookup"><span data-stu-id="6357c-128">*x*</span></span>   | <span data-ttu-id="6357c-129">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="6357c-129">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="6357c-130">**flot**</span><span class="sxs-lookup"><span data-stu-id="6357c-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6357c-131">cualquiera</span><span class="sxs-lookup"><span data-stu-id="6357c-131">any</span></span>                            |
| <span data-ttu-id="6357c-132">*direcc*</span><span class="sxs-lookup"><span data-stu-id="6357c-132">*ret*</span></span> | <span data-ttu-id="6357c-133">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="6357c-133">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="6357c-134">**flot**</span><span class="sxs-lookup"><span data-stu-id="6357c-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6357c-135">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="6357c-135">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6357c-136">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="6357c-136">Minimum Shader Model</span></span>

<span data-ttu-id="6357c-137">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6357c-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6357c-138">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="6357c-138">Shader Model</span></span>                                                                       | <span data-ttu-id="6357c-139">Compatible</span><span class="sxs-lookup"><span data-stu-id="6357c-139">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6357c-140">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="6357c-140">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="6357c-141">sí</span><span class="sxs-lookup"><span data-stu-id="6357c-141">yes</span></span>       |
| [<span data-ttu-id="6357c-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6357c-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="6357c-143">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="6357c-143">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="6357c-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6357c-144">Requirements</span></span>



| <span data-ttu-id="6357c-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="6357c-145">Requirement</span></span> | <span data-ttu-id="6357c-146">Value</span><span class="sxs-lookup"><span data-stu-id="6357c-146">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6357c-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6357c-147">Header</span></span><br/> | <dl> <span data-ttu-id="6357c-148"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6357c-148"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6357c-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="6357c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6357c-150">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="6357c-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

