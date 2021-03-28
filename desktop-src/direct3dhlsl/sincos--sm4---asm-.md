---
title: sincos ((SM4-ASM)
description: Sin componentes (Theta) y cos (Theta) para Theta en radianes.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2dd8fc3b011758f071cdcd273e34eb8a7f6421f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996864"
---
# <a name="sincos-sm4---asm"></a><span data-ttu-id="f95ea-103">sincos ((SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f95ea-103">sincos (sm4 - asm)</span></span>

<span data-ttu-id="f95ea-104">Sin componentes (Theta) y cos (Theta) para Theta en radianes.</span><span class="sxs-lookup"><span data-stu-id="f95ea-104">Component-wise sin(theta) and cos(theta) for theta in radians.</span></span>



| <span data-ttu-id="f95ea-105">sincos ( \[ \_ SAT \] destSIN \[ . Mask \] , destCOS \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f95ea-105">sincos\[\_sat\] destSIN\[.mask\], destCOS\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f95ea-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="f95ea-106">Item</span></span>                                                                                               | <span data-ttu-id="f95ea-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f95ea-107">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="f95ea-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span><span class="sxs-lookup"><span data-stu-id="f95ea-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span></span><br/> | <span data-ttu-id="f95ea-109">\[en \] la dirección de sin (*src0*), se calcula por componente.</span><span class="sxs-lookup"><span data-stu-id="f95ea-109">\[in\] The address of sin(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="f95ea-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span><span class="sxs-lookup"><span data-stu-id="f95ea-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span></span><br/> | <span data-ttu-id="f95ea-111">\[en \] la dirección de cos (*src0*), calculada por componente.</span><span class="sxs-lookup"><span data-stu-id="f95ea-111">\[in\] The address of cos(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="f95ea-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f95ea-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                    | <span data-ttu-id="f95ea-113">\[en \] los componentes para los que se van a calcular Sen y cos.</span><span class="sxs-lookup"><span data-stu-id="f95ea-113">\[in\] The components for which to compute sin and cos.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="f95ea-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f95ea-114">Remarks</span></span>

<span data-ttu-id="f95ea-115">Si el resultado no es necesario, puede especificar *destSIN* y *destCOS* como null en lugar de especificar un registro.</span><span class="sxs-lookup"><span data-stu-id="f95ea-115">If the result is not needed, you can specify *destSIN* and *destCOS* as NULL instead of specifying a register.</span></span>

<span data-ttu-id="f95ea-116">Los valores de Theta pueden ser cualquier valor de punto flotante de IEEE 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f95ea-116">Theta values can be any IEEE 32-bit floating point values.</span></span>

<span data-ttu-id="f95ea-117">El error absoluto máximo es 0,0008 en el intervalo de-100 \* PI a + 100 \* PI.</span><span class="sxs-lookup"><span data-stu-id="f95ea-117">The maximum absolute error is 0.0008 in the interval from -100\*Pi to +100\*Pi.</span></span>

<span data-ttu-id="f95ea-118">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.</span><span class="sxs-lookup"><span data-stu-id="f95ea-118">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="f95ea-119">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="f95ea-119">F means finite-real number.</span></span>



|             |          |              |             |        |        |             |              |          |         |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| <span data-ttu-id="f95ea-120">**src**</span><span class="sxs-lookup"><span data-stu-id="f95ea-120">**src**</span></span>     | <span data-ttu-id="f95ea-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="f95ea-121">**-inf**</span></span> | <span data-ttu-id="f95ea-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="f95ea-122">**-F**</span></span>       | <span data-ttu-id="f95ea-123">**-denormalización**</span><span class="sxs-lookup"><span data-stu-id="f95ea-123">**-denorm**</span></span> | <span data-ttu-id="f95ea-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="f95ea-124">**-0**</span></span> | <span data-ttu-id="f95ea-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="f95ea-125">**+0**</span></span> | <span data-ttu-id="f95ea-126">**+ denormalización**</span><span class="sxs-lookup"><span data-stu-id="f95ea-126">**+denorm**</span></span> | <span data-ttu-id="f95ea-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="f95ea-127">**+F**</span></span>       | <span data-ttu-id="f95ea-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="f95ea-128">**+inf**</span></span> | <span data-ttu-id="f95ea-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="f95ea-129">**NaN**</span></span> |
| <span data-ttu-id="f95ea-130">**destSIN**</span><span class="sxs-lookup"><span data-stu-id="f95ea-130">**destSIN**</span></span> | <span data-ttu-id="f95ea-131">NaN</span><span class="sxs-lookup"><span data-stu-id="f95ea-131">NaN</span></span>      | <span data-ttu-id="f95ea-132">\[de-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="f95ea-132">\[-1 to +1\]</span></span> | <span data-ttu-id="f95ea-133">-0</span><span class="sxs-lookup"><span data-stu-id="f95ea-133">-0</span></span>          | <span data-ttu-id="f95ea-134">-0</span><span class="sxs-lookup"><span data-stu-id="f95ea-134">-0</span></span>     | <span data-ttu-id="f95ea-135">+0</span><span class="sxs-lookup"><span data-stu-id="f95ea-135">+0</span></span>     | <span data-ttu-id="f95ea-136">+0</span><span class="sxs-lookup"><span data-stu-id="f95ea-136">+0</span></span>          | <span data-ttu-id="f95ea-137">\[de-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="f95ea-137">\[-1 to +1\]</span></span> | <span data-ttu-id="f95ea-138">NaN</span><span class="sxs-lookup"><span data-stu-id="f95ea-138">NaN</span></span>      | <span data-ttu-id="f95ea-139">NaN</span><span class="sxs-lookup"><span data-stu-id="f95ea-139">NaN</span></span>     |
| <span data-ttu-id="f95ea-140">**destCOS**</span><span class="sxs-lookup"><span data-stu-id="f95ea-140">**destCOS**</span></span> | <span data-ttu-id="f95ea-141">NaN</span><span class="sxs-lookup"><span data-stu-id="f95ea-141">NaN</span></span>      | <span data-ttu-id="f95ea-142">\[de-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="f95ea-142">\[-1 to +1\]</span></span> | <span data-ttu-id="f95ea-143">+1</span><span class="sxs-lookup"><span data-stu-id="f95ea-143">+1</span></span>          | <span data-ttu-id="f95ea-144">+1</span><span class="sxs-lookup"><span data-stu-id="f95ea-144">+1</span></span>     | <span data-ttu-id="f95ea-145">+1</span><span class="sxs-lookup"><span data-stu-id="f95ea-145">+1</span></span>     | <span data-ttu-id="f95ea-146">+1</span><span class="sxs-lookup"><span data-stu-id="f95ea-146">+1</span></span>          | <span data-ttu-id="f95ea-147">\[de-1 a + 1\]</span><span class="sxs-lookup"><span data-stu-id="f95ea-147">\[-1 to +1\]</span></span> | <span data-ttu-id="f95ea-148">NaN</span><span class="sxs-lookup"><span data-stu-id="f95ea-148">NaN</span></span>      | <span data-ttu-id="f95ea-149">NaN</span><span class="sxs-lookup"><span data-stu-id="f95ea-149">NaN</span></span>     |



 

<span data-ttu-id="f95ea-150">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="f95ea-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f95ea-151">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="f95ea-151">Vertex Shader</span></span> | <span data-ttu-id="f95ea-152">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="f95ea-152">Geometry Shader</span></span> | <span data-ttu-id="f95ea-153">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="f95ea-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f95ea-154">x</span><span class="sxs-lookup"><span data-stu-id="f95ea-154">x</span></span>             | <span data-ttu-id="f95ea-155">x</span><span class="sxs-lookup"><span data-stu-id="f95ea-155">x</span></span>               | <span data-ttu-id="f95ea-156">x</span><span class="sxs-lookup"><span data-stu-id="f95ea-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f95ea-157">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="f95ea-157">Minimum Shader Model</span></span>

<span data-ttu-id="f95ea-158">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f95ea-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f95ea-159">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="f95ea-159">Shader Model</span></span>                                              | <span data-ttu-id="f95ea-160">Compatible</span><span class="sxs-lookup"><span data-stu-id="f95ea-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f95ea-161">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f95ea-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f95ea-162">sí</span><span class="sxs-lookup"><span data-stu-id="f95ea-162">yes</span></span>       |
| [<span data-ttu-id="f95ea-163">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f95ea-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f95ea-164">sí</span><span class="sxs-lookup"><span data-stu-id="f95ea-164">yes</span></span>       |
| [<span data-ttu-id="f95ea-165">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f95ea-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f95ea-166">sí</span><span class="sxs-lookup"><span data-stu-id="f95ea-166">yes</span></span>       |
| [<span data-ttu-id="f95ea-167">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f95ea-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f95ea-168">no</span><span class="sxs-lookup"><span data-stu-id="f95ea-168">no</span></span>        |
| [<span data-ttu-id="f95ea-169">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f95ea-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f95ea-170">no</span><span class="sxs-lookup"><span data-stu-id="f95ea-170">no</span></span>        |
| [<span data-ttu-id="f95ea-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f95ea-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f95ea-172">no</span><span class="sxs-lookup"><span data-stu-id="f95ea-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f95ea-173">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f95ea-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f95ea-174">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f95ea-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





