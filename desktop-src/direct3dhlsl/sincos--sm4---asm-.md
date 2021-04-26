---
title: sincos (sm4 - asm)
description: Sin(theta) por componente y cos(theta) para theta en radianes.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c03118ff9a1fc2d958eaa6eb1a550a6dbf672a2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997022"
---
# <a name="sincos-sm4---asm"></a><span data-ttu-id="4a914-103">sincos (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="4a914-103">sincos (sm4 - asm)</span></span>

<span data-ttu-id="4a914-104">Sin(theta) por componente y cos(theta) para theta en radianes.</span><span class="sxs-lookup"><span data-stu-id="4a914-104">Component-wise sin(theta) and cos(theta) for theta in radians.</span></span>



| <span data-ttu-id="4a914-105">sincos \[ \_ sat \] destSIN \[ .mask \] , destCOS \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swzzle\]</span><span class="sxs-lookup"><span data-stu-id="4a914-105">sincos\[\_sat\] destSIN\[.mask\], destCOS\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------------|



 



| <span data-ttu-id="4a914-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="4a914-106">Item</span></span>                                                                                               | <span data-ttu-id="4a914-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a914-107">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="4a914-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span><span class="sxs-lookup"><span data-stu-id="4a914-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span></span><br/> | <span data-ttu-id="4a914-109">\[en \] La dirección de sin(*src0*), calculada por componente.</span><span class="sxs-lookup"><span data-stu-id="4a914-109">\[in\] The address of sin(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="4a914-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span><span class="sxs-lookup"><span data-stu-id="4a914-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span></span><br/> | <span data-ttu-id="4a914-111">\[en \] La dirección de cos(*src0*), calculada por componente.</span><span class="sxs-lookup"><span data-stu-id="4a914-111">\[in\] The address of cos(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="4a914-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4a914-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                    | <span data-ttu-id="4a914-113">\[en \] Los componentes para los que se va a calcular sin y cos.</span><span class="sxs-lookup"><span data-stu-id="4a914-113">\[in\] The components for which to compute sin and cos.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="4a914-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a914-114">Remarks</span></span>

<span data-ttu-id="4a914-115">Si el resultado no es necesario, puede especificar *destSIN* y *destCOS* como NULL en lugar de especificar un registro.</span><span class="sxs-lookup"><span data-stu-id="4a914-115">If the result is not needed, you can specify *destSIN* and *destCOS* as NULL instead of specifying a register.</span></span>

<span data-ttu-id="4a914-116">Los valores de Theta pueden ser cualquier valor de punto flotante ieee de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4a914-116">Theta values can be any IEEE 32-bit floating point values.</span></span>

<span data-ttu-id="4a914-117">El error absoluto máximo es 0,0008 en el intervalo de -100 \* Pi a +100 \* Pi.</span><span class="sxs-lookup"><span data-stu-id="4a914-117">The maximum absolute error is 0.0008 in the interval from -100\*Pi to +100\*Pi.</span></span>

<span data-ttu-id="4a914-118">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.</span><span class="sxs-lookup"><span data-stu-id="4a914-118">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="4a914-119">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="4a914-119">F means finite-real number.</span></span>



| <span data-ttu-id="4a914-120">**src**</span><span class="sxs-lookup"><span data-stu-id="4a914-120">**src**</span></span>     | <span data-ttu-id="4a914-121">**-inf**</span><span class="sxs-lookup"><span data-stu-id="4a914-121">**-inf**</span></span> | <span data-ttu-id="4a914-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="4a914-122">**-F**</span></span>       | <span data-ttu-id="4a914-123">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="4a914-123">**-denorm**</span></span> | <span data-ttu-id="4a914-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="4a914-124">**-0**</span></span> | <span data-ttu-id="4a914-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="4a914-125">**+0**</span></span> | <span data-ttu-id="4a914-126">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="4a914-126">**+denorm**</span></span> | <span data-ttu-id="4a914-127">**+F**</span><span class="sxs-lookup"><span data-stu-id="4a914-127">**+F**</span></span>       | <span data-ttu-id="4a914-128">**+inf**</span><span class="sxs-lookup"><span data-stu-id="4a914-128">**+inf**</span></span> | <span data-ttu-id="4a914-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="4a914-129">**NaN**</span></span> |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| <span data-ttu-id="4a914-130">**destSIN**</span><span class="sxs-lookup"><span data-stu-id="4a914-130">**destSIN**</span></span> | <span data-ttu-id="4a914-131">NaN</span><span class="sxs-lookup"><span data-stu-id="4a914-131">NaN</span></span>      | <span data-ttu-id="4a914-132">\[-1 a +1\]</span><span class="sxs-lookup"><span data-stu-id="4a914-132">\[-1 to +1\]</span></span> | <span data-ttu-id="4a914-133">-0</span><span class="sxs-lookup"><span data-stu-id="4a914-133">-0</span></span>          | <span data-ttu-id="4a914-134">-0</span><span class="sxs-lookup"><span data-stu-id="4a914-134">-0</span></span>     | <span data-ttu-id="4a914-135">+0</span><span class="sxs-lookup"><span data-stu-id="4a914-135">+0</span></span>     | <span data-ttu-id="4a914-136">+0</span><span class="sxs-lookup"><span data-stu-id="4a914-136">+0</span></span>          | <span data-ttu-id="4a914-137">\[-1 a +1\]</span><span class="sxs-lookup"><span data-stu-id="4a914-137">\[-1 to +1\]</span></span> | <span data-ttu-id="4a914-138">NaN</span><span class="sxs-lookup"><span data-stu-id="4a914-138">NaN</span></span>      | <span data-ttu-id="4a914-139">NaN</span><span class="sxs-lookup"><span data-stu-id="4a914-139">NaN</span></span>     |
| <span data-ttu-id="4a914-140">**destCOS**</span><span class="sxs-lookup"><span data-stu-id="4a914-140">**destCOS**</span></span> | <span data-ttu-id="4a914-141">NaN</span><span class="sxs-lookup"><span data-stu-id="4a914-141">NaN</span></span>      | <span data-ttu-id="4a914-142">\[-1 a +1\]</span><span class="sxs-lookup"><span data-stu-id="4a914-142">\[-1 to +1\]</span></span> | <span data-ttu-id="4a914-143">+1</span><span class="sxs-lookup"><span data-stu-id="4a914-143">+1</span></span>          | <span data-ttu-id="4a914-144">+1</span><span class="sxs-lookup"><span data-stu-id="4a914-144">+1</span></span>     | <span data-ttu-id="4a914-145">+1</span><span class="sxs-lookup"><span data-stu-id="4a914-145">+1</span></span>     | <span data-ttu-id="4a914-146">+1</span><span class="sxs-lookup"><span data-stu-id="4a914-146">+1</span></span>          | <span data-ttu-id="4a914-147">\[-1 a +1\]</span><span class="sxs-lookup"><span data-stu-id="4a914-147">\[-1 to +1\]</span></span> | <span data-ttu-id="4a914-148">NaN</span><span class="sxs-lookup"><span data-stu-id="4a914-148">NaN</span></span>      | <span data-ttu-id="4a914-149">NaN</span><span class="sxs-lookup"><span data-stu-id="4a914-149">NaN</span></span>     |



 

<span data-ttu-id="4a914-150">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="4a914-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4a914-151">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="4a914-151">Vertex Shader</span></span> | <span data-ttu-id="4a914-152">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="4a914-152">Geometry Shader</span></span> | <span data-ttu-id="4a914-153">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="4a914-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4a914-154">x</span><span class="sxs-lookup"><span data-stu-id="4a914-154">x</span></span>             | <span data-ttu-id="4a914-155">x</span><span class="sxs-lookup"><span data-stu-id="4a914-155">x</span></span>               | <span data-ttu-id="4a914-156">x</span><span class="sxs-lookup"><span data-stu-id="4a914-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4a914-157">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="4a914-157">Minimum Shader Model</span></span>

<span data-ttu-id="4a914-158">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4a914-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4a914-159">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="4a914-159">Shader Model</span></span>                                              | <span data-ttu-id="4a914-160">Compatible</span><span class="sxs-lookup"><span data-stu-id="4a914-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4a914-161">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4a914-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4a914-162">sí</span><span class="sxs-lookup"><span data-stu-id="4a914-162">yes</span></span>       |
| [<span data-ttu-id="4a914-163">Modelo de sombreador 4.1</span><span class="sxs-lookup"><span data-stu-id="4a914-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4a914-164">sí</span><span class="sxs-lookup"><span data-stu-id="4a914-164">yes</span></span>       |
| [<span data-ttu-id="4a914-165">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="4a914-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4a914-166">sí</span><span class="sxs-lookup"><span data-stu-id="4a914-166">yes</span></span>       |
| [<span data-ttu-id="4a914-167">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a914-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4a914-168">no</span><span class="sxs-lookup"><span data-stu-id="4a914-168">no</span></span>        |
| [<span data-ttu-id="4a914-169">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a914-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4a914-170">no</span><span class="sxs-lookup"><span data-stu-id="4a914-170">no</span></span>        |
| [<span data-ttu-id="4a914-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a914-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4a914-172">no</span><span class="sxs-lookup"><span data-stu-id="4a914-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4a914-173">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4a914-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a914-174">Ensamblado del modelo de sombreador 4 (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="4a914-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





