---
title: Max (SM4-ASM)
description: Valor máximo de Float de componente.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f24618897eacf250f2b924f6dde3745a32a7172
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419894"
---
# <a name="max-sm4---asm"></a><span data-ttu-id="ca8e7-103">Max (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ca8e7-103">max (sm4 - asm)</span></span>

<span data-ttu-id="ca8e7-104">Valor máximo de Float de componente.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-104">Component-wise float maximum.</span></span>



| <span data-ttu-id="ca8e7-105">Max \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="ca8e7-105">max\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="ca8e7-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="ca8e7-106">Item</span></span>                                                            | <span data-ttu-id="ca8e7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca8e7-107">Description</span></span>                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca8e7-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ca8e7-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ca8e7-109">\[en \] el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="ca8e7-110">*dest*  =  *src0*  >=  *SRC1* ?</span><span class="sxs-lookup"><span data-stu-id="ca8e7-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="ca8e7-111">*src0* : *SRC1*</span><span class="sxs-lookup"><span data-stu-id="ca8e7-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="ca8e7-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ca8e7-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ca8e7-113">\[en \] los componentes que se van a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                    |
| <span data-ttu-id="ca8e7-114"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="ca8e7-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="ca8e7-115">\[en \] los componentes que se van a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="ca8e7-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca8e7-116">Remarks</span></span>

><span data-ttu-id="ca8e7-117">= se usa en lugar de > para que, si es min (x, y) = x, entonces Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="ca8e7-118">NaN tiene un tratamiento especial.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-118">NaN has special handling.</span></span> <span data-ttu-id="ca8e7-119">Si un operando de origen es NaN, se devuelve el otro operando de origen y la elección se realiza por componente.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="ca8e7-120">Si ambos son NaN, se devuelve cualquier representación NaN.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-120">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="ca8e7-121">Las desnormaciones se vacían con el signo que se conserva antes de la comparación.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-121">Denorms are flushed with sign preserved before the comparison.</span></span> <span data-ttu-id="ca8e7-122">Sin embargo, el resultado que se escribe en *dest* puede o no ser de desnormalización.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-122">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="ca8e7-123">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-123">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="ca8e7-124">F significa un número real finito.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-124">F means finite real number.</span></span>



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="ca8e7-125">**src0 SRC1->**</span><span class="sxs-lookup"><span data-stu-id="ca8e7-125">**src0 src1->**</span></span> | <span data-ttu-id="ca8e7-126">**-INF**</span><span class="sxs-lookup"><span data-stu-id="ca8e7-126">**-inf**</span></span> | <span data-ttu-id="ca8e7-127">**F**</span><span class="sxs-lookup"><span data-stu-id="ca8e7-127">**F**</span></span>        | <span data-ttu-id="ca8e7-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="ca8e7-128">**+inf**</span></span> | <span data-ttu-id="ca8e7-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="ca8e7-129">**NaN**</span></span> |
| <span data-ttu-id="ca8e7-130">**-INF**</span><span class="sxs-lookup"><span data-stu-id="ca8e7-130">**-inf**</span></span>           | <span data-ttu-id="ca8e7-131">-inf</span><span class="sxs-lookup"><span data-stu-id="ca8e7-131">-inf</span></span>     | <span data-ttu-id="ca8e7-132">src1</span><span class="sxs-lookup"><span data-stu-id="ca8e7-132">src1</span></span>         | <span data-ttu-id="ca8e7-133">+inf</span><span class="sxs-lookup"><span data-stu-id="ca8e7-133">+inf</span></span>     | <span data-ttu-id="ca8e7-134">-inf</span><span class="sxs-lookup"><span data-stu-id="ca8e7-134">-inf</span></span>    |
| <span data-ttu-id="ca8e7-135">**F**</span><span class="sxs-lookup"><span data-stu-id="ca8e7-135">**F**</span></span>              | <span data-ttu-id="ca8e7-136">src0</span><span class="sxs-lookup"><span data-stu-id="ca8e7-136">src0</span></span>     | <span data-ttu-id="ca8e7-137">src0 o SRC1</span><span class="sxs-lookup"><span data-stu-id="ca8e7-137">src0 or src1</span></span> | <span data-ttu-id="ca8e7-138">+inf</span><span class="sxs-lookup"><span data-stu-id="ca8e7-138">+inf</span></span>     | <span data-ttu-id="ca8e7-139">src0</span><span class="sxs-lookup"><span data-stu-id="ca8e7-139">src0</span></span>    |
| <span data-ttu-id="ca8e7-140">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="ca8e7-140">**+inf**</span></span>           | <span data-ttu-id="ca8e7-141">+inf</span><span class="sxs-lookup"><span data-stu-id="ca8e7-141">+inf</span></span>     | <span data-ttu-id="ca8e7-142">+inf</span><span class="sxs-lookup"><span data-stu-id="ca8e7-142">+inf</span></span>         | <span data-ttu-id="ca8e7-143">+inf</span><span class="sxs-lookup"><span data-stu-id="ca8e7-143">+inf</span></span>     | <span data-ttu-id="ca8e7-144">+inf</span><span class="sxs-lookup"><span data-stu-id="ca8e7-144">+inf</span></span>    |
| <span data-ttu-id="ca8e7-145">**NaN**</span><span class="sxs-lookup"><span data-stu-id="ca8e7-145">**NaN**</span></span>            | <span data-ttu-id="ca8e7-146">-inf</span><span class="sxs-lookup"><span data-stu-id="ca8e7-146">-inf</span></span>     | <span data-ttu-id="ca8e7-147">src1</span><span class="sxs-lookup"><span data-stu-id="ca8e7-147">src1</span></span>         | <span data-ttu-id="ca8e7-148">+inf</span><span class="sxs-lookup"><span data-stu-id="ca8e7-148">+inf</span></span>     | <span data-ttu-id="ca8e7-149">NaN</span><span class="sxs-lookup"><span data-stu-id="ca8e7-149">NaN</span></span>     |



 

<span data-ttu-id="ca8e7-150">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="ca8e7-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ca8e7-151">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="ca8e7-151">Vertex Shader</span></span> | <span data-ttu-id="ca8e7-152">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="ca8e7-152">Geometry Shader</span></span> | <span data-ttu-id="ca8e7-153">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ca8e7-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ca8e7-154">x</span><span class="sxs-lookup"><span data-stu-id="ca8e7-154">x</span></span>             | <span data-ttu-id="ca8e7-155">x</span><span class="sxs-lookup"><span data-stu-id="ca8e7-155">x</span></span>               | <span data-ttu-id="ca8e7-156">x</span><span class="sxs-lookup"><span data-stu-id="ca8e7-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ca8e7-157">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="ca8e7-157">Minimum Shader Model</span></span>

<span data-ttu-id="ca8e7-158">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ca8e7-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ca8e7-159">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ca8e7-159">Shader Model</span></span>                                              | <span data-ttu-id="ca8e7-160">Compatible</span><span class="sxs-lookup"><span data-stu-id="ca8e7-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ca8e7-161">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ca8e7-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ca8e7-162">sí</span><span class="sxs-lookup"><span data-stu-id="ca8e7-162">yes</span></span>       |
| [<span data-ttu-id="ca8e7-163">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ca8e7-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ca8e7-164">sí</span><span class="sxs-lookup"><span data-stu-id="ca8e7-164">yes</span></span>       |
| [<span data-ttu-id="ca8e7-165">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ca8e7-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ca8e7-166">sí</span><span class="sxs-lookup"><span data-stu-id="ca8e7-166">yes</span></span>       |
| [<span data-ttu-id="ca8e7-167">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca8e7-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ca8e7-168">no</span><span class="sxs-lookup"><span data-stu-id="ca8e7-168">no</span></span>        |
| [<span data-ttu-id="ca8e7-169">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca8e7-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ca8e7-170">no</span><span class="sxs-lookup"><span data-stu-id="ca8e7-170">no</span></span>        |
| [<span data-ttu-id="ca8e7-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca8e7-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ca8e7-172">no</span><span class="sxs-lookup"><span data-stu-id="ca8e7-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ca8e7-173">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca8e7-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca8e7-174">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca8e7-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





