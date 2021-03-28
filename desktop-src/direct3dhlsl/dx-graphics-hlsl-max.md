---
title: max
description: Selecciona el mayor de x e y.
ms.assetid: 08e17a0c-6d44-49ea-b613-bd262534522c
keywords:
- HLSL máx.
topic_type:
- apiref
api_name:
- max
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a40ccb32bb2c2fcd7ca7342b9d7d4d143688102
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421153"
---
# <a name="max"></a><span data-ttu-id="3d2c5-104">max</span><span class="sxs-lookup"><span data-stu-id="3d2c5-104">max</span></span>

<span data-ttu-id="3d2c5-105">Selecciona el mayor de x e y.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-105">Selects the greater of x and y.</span></span>



| <span data-ttu-id="3d2c5-106">RET máx. (x, y)</span><span class="sxs-lookup"><span data-stu-id="3d2c5-106">ret max(x, y)</span></span> |
|---------------|



 

## <a name="parameters"></a><span data-ttu-id="3d2c5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d2c5-107">Parameters</span></span>



| <span data-ttu-id="3d2c5-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3d2c5-108">Item</span></span>                                                   | <span data-ttu-id="3d2c5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d2c5-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="3d2c5-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="3d2c5-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="3d2c5-111">\[en \] el valor de entrada x.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-111">\[in\] The x input value.</span></span><br/> |
| <span data-ttu-id="3d2c5-112"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="3d2c5-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="3d2c5-113">\[en \] el valor de entrada y.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-113">\[in\] The y input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3d2c5-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d2c5-114">Return Value</span></span>

<span data-ttu-id="3d2c5-115">Parámetro *x* o *y* , el que sea el valor más grande.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-115">The *x* or *y* parameter, whichever is the largest value.</span></span>


## <a name="remarks"></a><span data-ttu-id="3d2c5-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d2c5-116">Remarks</span></span>

<span data-ttu-id="3d2c5-117">Las desnormalizaciones se controlan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="3d2c5-117">Denormals are handled as follows:</span></span>

| <span data-ttu-id="3d2c5-118">src0 SRC1-></span><span class="sxs-lookup"><span data-stu-id="3d2c5-118">src0 src1-></span></span> | <span data-ttu-id="3d2c5-119">-inf</span><span class="sxs-lookup"><span data-stu-id="3d2c5-119">-inf</span></span> | <span data-ttu-id="3d2c5-120">F</span><span class="sxs-lookup"><span data-stu-id="3d2c5-120">F</span></span>             | <span data-ttu-id="3d2c5-121">+inf</span><span class="sxs-lookup"><span data-stu-id="3d2c5-121">+inf</span></span> | <span data-ttu-id="3d2c5-122">NAN</span><span class="sxs-lookup"><span data-stu-id="3d2c5-122">NAN</span></span>  |
|-------------|------|---------------|------|------|
| <span data-ttu-id="3d2c5-123">-inf</span><span class="sxs-lookup"><span data-stu-id="3d2c5-123">-inf</span></span>        | <span data-ttu-id="3d2c5-124">-inf</span><span class="sxs-lookup"><span data-stu-id="3d2c5-124">-inf</span></span> | <span data-ttu-id="3d2c5-125">src1</span><span class="sxs-lookup"><span data-stu-id="3d2c5-125">src1</span></span>          | <span data-ttu-id="3d2c5-126">+inf</span><span class="sxs-lookup"><span data-stu-id="3d2c5-126">+inf</span></span> | <span data-ttu-id="3d2c5-127">-inf</span><span class="sxs-lookup"><span data-stu-id="3d2c5-127">-inf</span></span> |
| <span data-ttu-id="3d2c5-128">F</span><span class="sxs-lookup"><span data-stu-id="3d2c5-128">F</span></span>           | <span data-ttu-id="3d2c5-129">src0</span><span class="sxs-lookup"><span data-stu-id="3d2c5-129">src0</span></span> | <span data-ttu-id="3d2c5-130">src0 o SRC1</span><span class="sxs-lookup"><span data-stu-id="3d2c5-130">src0 or src1</span></span>  | <span data-ttu-id="3d2c5-131">+inf</span><span class="sxs-lookup"><span data-stu-id="3d2c5-131">+inf</span></span> | <span data-ttu-id="3d2c5-132">src0</span><span class="sxs-lookup"><span data-stu-id="3d2c5-132">src0</span></span> |
| <span data-ttu-id="3d2c5-133">+inf</span><span class="sxs-lookup"><span data-stu-id="3d2c5-133">+inf</span></span>        | <span data-ttu-id="3d2c5-134">+inf</span><span class="sxs-lookup"><span data-stu-id="3d2c5-134">+inf</span></span> | <span data-ttu-id="3d2c5-135">+inf</span><span class="sxs-lookup"><span data-stu-id="3d2c5-135">+inf</span></span>          | <span data-ttu-id="3d2c5-136">+inf</span><span class="sxs-lookup"><span data-stu-id="3d2c5-136">+inf</span></span> | <span data-ttu-id="3d2c5-137">+inf</span><span class="sxs-lookup"><span data-stu-id="3d2c5-137">+inf</span></span> |
| <span data-ttu-id="3d2c5-138">NaN</span><span class="sxs-lookup"><span data-stu-id="3d2c5-138">NaN</span></span>         | <span data-ttu-id="3d2c5-139">-inf</span><span class="sxs-lookup"><span data-stu-id="3d2c5-139">-inf</span></span> | <span data-ttu-id="3d2c5-140">src1</span><span class="sxs-lookup"><span data-stu-id="3d2c5-140">src1</span></span>          | <span data-ttu-id="3d2c5-141">+inf</span><span class="sxs-lookup"><span data-stu-id="3d2c5-141">+inf</span></span> | <span data-ttu-id="3d2c5-142">NaN</span><span class="sxs-lookup"><span data-stu-id="3d2c5-142">NaN</span></span>  |

<span data-ttu-id="3d2c5-143">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-143">F means finite-real number.</span></span>


## <a name="type-description"></a><span data-ttu-id="3d2c5-144">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="3d2c5-144">Type Description</span></span>

| <span data-ttu-id="3d2c5-145">Nombre</span><span class="sxs-lookup"><span data-stu-id="3d2c5-145">Name</span></span> | <span data-ttu-id="3d2c5-146">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="3d2c5-146">In/Out</span></span>      | [<span data-ttu-id="3d2c5-147">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="3d2c5-147">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="3d2c5-148">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="3d2c5-148">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="3d2c5-149">Tamaño</span><span class="sxs-lookup"><span data-stu-id="3d2c5-149">Size</span></span>                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="3d2c5-150">x</span><span class="sxs-lookup"><span data-stu-id="3d2c5-150">x</span></span>    | <span data-ttu-id="3d2c5-151">in</span><span class="sxs-lookup"><span data-stu-id="3d2c5-151">in</span></span>          | <span data-ttu-id="3d2c5-152">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="3d2c5-152">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="3d2c5-153">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="3d2c5-153">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="3d2c5-154">cualquiera</span><span class="sxs-lookup"><span data-stu-id="3d2c5-154">any</span></span>                          |
| <span data-ttu-id="3d2c5-155">y</span><span class="sxs-lookup"><span data-stu-id="3d2c5-155">y</span></span>    | <span data-ttu-id="3d2c5-156">in</span><span class="sxs-lookup"><span data-stu-id="3d2c5-156">in</span></span>          | <span data-ttu-id="3d2c5-157">igual que la entrada x</span><span class="sxs-lookup"><span data-stu-id="3d2c5-157">same as input x</span></span>                                                                                                | <span data-ttu-id="3d2c5-158">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="3d2c5-158">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="3d2c5-159">mismas dimensiones que la entrada x</span><span class="sxs-lookup"><span data-stu-id="3d2c5-159">same dimension(s) as input x</span></span> |
| <span data-ttu-id="3d2c5-160">direcc</span><span class="sxs-lookup"><span data-stu-id="3d2c5-160">ret</span></span>  | <span data-ttu-id="3d2c5-161">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d2c5-161">return type</span></span> | <span data-ttu-id="3d2c5-162">igual que la entrada x</span><span class="sxs-lookup"><span data-stu-id="3d2c5-162">same as input x</span></span>                                                                                                | <span data-ttu-id="3d2c5-163">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="3d2c5-163">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="3d2c5-164">mismas dimensiones que la entrada x</span><span class="sxs-lookup"><span data-stu-id="3d2c5-164">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3d2c5-165">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="3d2c5-165">Minimum Shader Model</span></span>

<span data-ttu-id="3d2c5-166">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3d2c5-166">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3d2c5-167">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="3d2c5-167">Shader Model</span></span>                                                                       | <span data-ttu-id="3d2c5-168">Compatible</span><span class="sxs-lookup"><span data-stu-id="3d2c5-168">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="3d2c5-169">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="3d2c5-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="3d2c5-170">sí</span><span class="sxs-lookup"><span data-stu-id="3d2c5-170">yes</span></span>                         |
| [<span data-ttu-id="3d2c5-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d2c5-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="3d2c5-172">sí (vs \_ 1 \_ 1 y PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="3d2c5-172">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="3d2c5-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d2c5-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d2c5-174">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="3d2c5-174">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[<span data-ttu-id="3d2c5-175">**Especificación funcional de DirectX**</span><span class="sxs-lookup"><span data-stu-id="3d2c5-175">**DirectX Functional Specification**</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MAX) 
</dt> </dl>
 
