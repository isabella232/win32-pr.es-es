---
title: min.
description: Selecciona el menor de x e y.
ms.assetid: 4e10cfc2-d680-4d7f-81b2-fa52024f902d
keywords:
- HLSL mín.
topic_type:
- apiref
api_name:
- min
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 129c5cb641c2d69b6c1365d8221663e264060532
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488211"
---
# <a name="min"></a><span data-ttu-id="10937-104">min.</span><span class="sxs-lookup"><span data-stu-id="10937-104">min</span></span>

<span data-ttu-id="10937-105">Selecciona el menor de x e y.</span><span class="sxs-lookup"><span data-stu-id="10937-105">Selects the lesser of x and y.</span></span>



| <span data-ttu-id="10937-106">RET min (x, y)</span><span class="sxs-lookup"><span data-stu-id="10937-106">ret min(x, y)</span></span> |
|---------------|



 

## <a name="parameters"></a><span data-ttu-id="10937-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10937-107">Parameters</span></span>



| <span data-ttu-id="10937-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="10937-108">Item</span></span>                                                   | <span data-ttu-id="10937-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="10937-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="10937-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="10937-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="10937-111">\[en \] el valor de entrada x.</span><span class="sxs-lookup"><span data-stu-id="10937-111">\[in\] The x input value.</span></span><br/> |
| <span data-ttu-id="10937-112"><span id="y"></span><span id="Y"></span>*sí*</span><span class="sxs-lookup"><span data-stu-id="10937-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="10937-113">\[en \] el valor de entrada y.</span><span class="sxs-lookup"><span data-stu-id="10937-113">\[in\] The y input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="10937-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10937-114">Return Value</span></span>

<span data-ttu-id="10937-115">Parámetro *x* o *y* , el que sea el valor más pequeño.</span><span class="sxs-lookup"><span data-stu-id="10937-115">The *x* or *y* parameter, whichever is the smallest value.</span></span>


## <a name="remarks"></a><span data-ttu-id="10937-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10937-116">Remarks</span></span>

<span data-ttu-id="10937-117">Las desnormalizaciones se controlan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="10937-117">Denormals are handled as follows:</span></span>

| <span data-ttu-id="10937-118">src0 SRC1-></span><span class="sxs-lookup"><span data-stu-id="10937-118">src0 src1-></span></span> | <span data-ttu-id="10937-119">-inf</span><span class="sxs-lookup"><span data-stu-id="10937-119">-inf</span></span> | <span data-ttu-id="10937-120">F</span><span class="sxs-lookup"><span data-stu-id="10937-120">F</span></span>             | <span data-ttu-id="10937-121">+inf</span><span class="sxs-lookup"><span data-stu-id="10937-121">+inf</span></span> | <span data-ttu-id="10937-122">NAN</span><span class="sxs-lookup"><span data-stu-id="10937-122">NAN</span></span>  |
|-------------|------|---------------|------|------|
| <span data-ttu-id="10937-123">-inf</span><span class="sxs-lookup"><span data-stu-id="10937-123">-inf</span></span>        | <span data-ttu-id="10937-124">-inf</span><span class="sxs-lookup"><span data-stu-id="10937-124">-inf</span></span> | <span data-ttu-id="10937-125">-inf</span><span class="sxs-lookup"><span data-stu-id="10937-125">-inf</span></span>          | <span data-ttu-id="10937-126">-inf</span><span class="sxs-lookup"><span data-stu-id="10937-126">-inf</span></span> | <span data-ttu-id="10937-127">-inf</span><span class="sxs-lookup"><span data-stu-id="10937-127">-inf</span></span> |
| <span data-ttu-id="10937-128">F</span><span class="sxs-lookup"><span data-stu-id="10937-128">F</span></span>           | <span data-ttu-id="10937-129">-inf</span><span class="sxs-lookup"><span data-stu-id="10937-129">-inf</span></span> | <span data-ttu-id="10937-130">src0 o SRC1</span><span class="sxs-lookup"><span data-stu-id="10937-130">src0 or src1</span></span>  | <span data-ttu-id="10937-131">src0</span><span class="sxs-lookup"><span data-stu-id="10937-131">src0</span></span> | <span data-ttu-id="10937-132">src0</span><span class="sxs-lookup"><span data-stu-id="10937-132">src0</span></span> |
| <span data-ttu-id="10937-133">+inf</span><span class="sxs-lookup"><span data-stu-id="10937-133">+inf</span></span>        | <span data-ttu-id="10937-134">-inf</span><span class="sxs-lookup"><span data-stu-id="10937-134">-inf</span></span> | <span data-ttu-id="10937-135">src1</span><span class="sxs-lookup"><span data-stu-id="10937-135">src1</span></span>          | <span data-ttu-id="10937-136">+inf</span><span class="sxs-lookup"><span data-stu-id="10937-136">+inf</span></span> | <span data-ttu-id="10937-137">+inf</span><span class="sxs-lookup"><span data-stu-id="10937-137">+inf</span></span> |
| <span data-ttu-id="10937-138">NaN</span><span class="sxs-lookup"><span data-stu-id="10937-138">NaN</span></span>         | <span data-ttu-id="10937-139">-inf</span><span class="sxs-lookup"><span data-stu-id="10937-139">-inf</span></span> | <span data-ttu-id="10937-140">src1</span><span class="sxs-lookup"><span data-stu-id="10937-140">src1</span></span>          | <span data-ttu-id="10937-141">+inf</span><span class="sxs-lookup"><span data-stu-id="10937-141">+inf</span></span> | <span data-ttu-id="10937-142">NaN</span><span class="sxs-lookup"><span data-stu-id="10937-142">NaN</span></span>  |

<span data-ttu-id="10937-143">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="10937-143">F means finite-real number.</span></span>


## <a name="type-description"></a><span data-ttu-id="10937-144">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="10937-144">Type Description</span></span>

| <span data-ttu-id="10937-145">Nombre</span><span class="sxs-lookup"><span data-stu-id="10937-145">Name</span></span> | <span data-ttu-id="10937-146">Entrada o salida</span><span class="sxs-lookup"><span data-stu-id="10937-146">In/Out</span></span>      | [<span data-ttu-id="10937-147">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="10937-147">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="10937-148">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="10937-148">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="10937-149">Tamaño</span><span class="sxs-lookup"><span data-stu-id="10937-149">Size</span></span>                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="10937-150">x</span><span class="sxs-lookup"><span data-stu-id="10937-150">x</span></span>    | <span data-ttu-id="10937-151">in</span><span class="sxs-lookup"><span data-stu-id="10937-151">in</span></span>          | <span data-ttu-id="10937-152">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="10937-152">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="10937-153">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="10937-153">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="10937-154">cualquiera</span><span class="sxs-lookup"><span data-stu-id="10937-154">any</span></span>                          |
| <span data-ttu-id="10937-155">y</span><span class="sxs-lookup"><span data-stu-id="10937-155">y</span></span>    | <span data-ttu-id="10937-156">in</span><span class="sxs-lookup"><span data-stu-id="10937-156">in</span></span>          | <span data-ttu-id="10937-157">igual que la entrada x</span><span class="sxs-lookup"><span data-stu-id="10937-157">same as input x</span></span>                                                                                                | <span data-ttu-id="10937-158">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="10937-158">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="10937-159">mismas dimensiones que la entrada x</span><span class="sxs-lookup"><span data-stu-id="10937-159">same dimension(s) as input x</span></span> |
| <span data-ttu-id="10937-160">direcc</span><span class="sxs-lookup"><span data-stu-id="10937-160">ret</span></span>  | <span data-ttu-id="10937-161">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10937-161">return type</span></span> | <span data-ttu-id="10937-162">igual que la entrada x</span><span class="sxs-lookup"><span data-stu-id="10937-162">same as input x</span></span>                                                                                                | <span data-ttu-id="10937-163">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="10937-163">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="10937-164">mismas dimensiones que la entrada x</span><span class="sxs-lookup"><span data-stu-id="10937-164">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="10937-165">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="10937-165">Minimum Shader Model</span></span>

<span data-ttu-id="10937-166">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="10937-166">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="10937-167">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="10937-167">Shader Model</span></span>                                                                       | <span data-ttu-id="10937-168">Compatible</span><span class="sxs-lookup"><span data-stu-id="10937-168">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="10937-169">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="10937-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="10937-170">sí</span><span class="sxs-lookup"><span data-stu-id="10937-170">yes</span></span>                         |
| [<span data-ttu-id="10937-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="10937-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="10937-172">sí (vs \_ 1 \_ 1 y PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="10937-172">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="10937-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="10937-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10937-174">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="10937-174">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[<span data-ttu-id="10937-175">**Especificación funcional de DirectX**</span><span class="sxs-lookup"><span data-stu-id="10937-175">**DirectX Functional Specification**</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MIN)