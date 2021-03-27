---
title: min (SM4-ASM)
description: Valor Float mínimo de componente.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584aee077735b717bf76d148d4d0db4357a7d95
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104149005"
---
# <a name="min-sm4---asm"></a><span data-ttu-id="d8092-103">min (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d8092-103">min (sm4 - asm)</span></span>

<span data-ttu-id="d8092-104">Valor Float mínimo de componente.</span><span class="sxs-lookup"><span data-stu-id="d8092-104">Component-wise float minimum.</span></span>



| <span data-ttu-id="d8092-105">min \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="d8092-105">min\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d8092-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="d8092-106">Item</span></span>                                                            | <span data-ttu-id="d8092-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8092-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8092-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d8092-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d8092-109">\[en \] el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d8092-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="d8092-110">*dest*  =  *src0*  <  *SRC1* ?</span><span class="sxs-lookup"><span data-stu-id="d8092-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="d8092-111">*src0* : *SRC1*</span><span class="sxs-lookup"><span data-stu-id="d8092-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="d8092-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d8092-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d8092-113">\[en \] los componentes que se van a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="d8092-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                  |
| <span data-ttu-id="d8092-114"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="d8092-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="d8092-115">\[en \] los componentes que se van a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="d8092-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="d8092-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8092-116">Remarks</span></span>

><span data-ttu-id="d8092-117">= se usa en lugar de > para que, si es min (x, y) = x, entonces Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="d8092-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="d8092-118">NaN tiene un tratamiento especial.</span><span class="sxs-lookup"><span data-stu-id="d8092-118">NaN has special handling.</span></span> <span data-ttu-id="d8092-119">Si un operando de origen es NaN, se devuelve el otro operando de origen y la elección se realiza por componente.</span><span class="sxs-lookup"><span data-stu-id="d8092-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="d8092-120">Si ambos son NaN, se devuelve cualquier representación NaN.</span><span class="sxs-lookup"><span data-stu-id="d8092-120">If both are NaN, any NaN representation is returned.</span></span> <span data-ttu-id="d8092-121">Esto se ajusta a las nuevas reglas de IEEE 754R.</span><span class="sxs-lookup"><span data-stu-id="d8092-121">This conforms to new IEEE 754R rules.</span></span>

<span data-ttu-id="d8092-122">Las desnormaciones se vacían, con el signo conservado, antes de la comparación.</span><span class="sxs-lookup"><span data-stu-id="d8092-122">Denorms are flushed, with the sign preserved, before comparison.</span></span> <span data-ttu-id="d8092-123">Sin embargo, el resultado que se escribe en *dest* puede o no ser de desnormalización.</span><span class="sxs-lookup"><span data-stu-id="d8092-123">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="d8092-124">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento.</span><span class="sxs-lookup"><span data-stu-id="d8092-124">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="d8092-125">F significa un número real finito.</span><span class="sxs-lookup"><span data-stu-id="d8092-125">F means finite real number.</span></span>



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="d8092-126">**src0 SRC1->**</span><span class="sxs-lookup"><span data-stu-id="d8092-126">**src0 src1->**</span></span> | <span data-ttu-id="d8092-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="d8092-127">**-inf**</span></span> | <span data-ttu-id="d8092-128">**F**</span><span class="sxs-lookup"><span data-stu-id="d8092-128">**F**</span></span>        | <span data-ttu-id="d8092-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="d8092-129">**+inf**</span></span> | <span data-ttu-id="d8092-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="d8092-130">**NaN**</span></span> |
| <span data-ttu-id="d8092-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="d8092-131">**-inf**</span></span>           | <span data-ttu-id="d8092-132">-inf</span><span class="sxs-lookup"><span data-stu-id="d8092-132">-inf</span></span>     | <span data-ttu-id="d8092-133">-inf</span><span class="sxs-lookup"><span data-stu-id="d8092-133">-inf</span></span>         | <span data-ttu-id="d8092-134">-inf</span><span class="sxs-lookup"><span data-stu-id="d8092-134">-inf</span></span>     | <span data-ttu-id="d8092-135">-inf</span><span class="sxs-lookup"><span data-stu-id="d8092-135">-inf</span></span>    |
| <span data-ttu-id="d8092-136">**F**</span><span class="sxs-lookup"><span data-stu-id="d8092-136">**F**</span></span>              | <span data-ttu-id="d8092-137">-inf</span><span class="sxs-lookup"><span data-stu-id="d8092-137">-inf</span></span>     | <span data-ttu-id="d8092-138">src0 o SRC1</span><span class="sxs-lookup"><span data-stu-id="d8092-138">src0 or src1</span></span> | <span data-ttu-id="d8092-139">src0</span><span class="sxs-lookup"><span data-stu-id="d8092-139">src0</span></span>     | <span data-ttu-id="d8092-140">src0</span><span class="sxs-lookup"><span data-stu-id="d8092-140">src0</span></span>    |
| <span data-ttu-id="d8092-141">**-INF**</span><span class="sxs-lookup"><span data-stu-id="d8092-141">**-inf**</span></span>           | <span data-ttu-id="d8092-142">-inf</span><span class="sxs-lookup"><span data-stu-id="d8092-142">-inf</span></span>     | <span data-ttu-id="d8092-143">src1</span><span class="sxs-lookup"><span data-stu-id="d8092-143">src1</span></span>         | <span data-ttu-id="d8092-144">+inf</span><span class="sxs-lookup"><span data-stu-id="d8092-144">+inf</span></span>     | <span data-ttu-id="d8092-145">+inf</span><span class="sxs-lookup"><span data-stu-id="d8092-145">+inf</span></span>    |
| <span data-ttu-id="d8092-146">**NaN**</span><span class="sxs-lookup"><span data-stu-id="d8092-146">**NaN**</span></span>            | <span data-ttu-id="d8092-147">-inf</span><span class="sxs-lookup"><span data-stu-id="d8092-147">-inf</span></span>     | <span data-ttu-id="d8092-148">src1</span><span class="sxs-lookup"><span data-stu-id="d8092-148">src1</span></span>         | <span data-ttu-id="d8092-149">+inf</span><span class="sxs-lookup"><span data-stu-id="d8092-149">+inf</span></span>     | <span data-ttu-id="d8092-150">NaN</span><span class="sxs-lookup"><span data-stu-id="d8092-150">NaN</span></span>     |



 

<span data-ttu-id="d8092-151">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="d8092-151">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d8092-152">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="d8092-152">Vertex Shader</span></span> | <span data-ttu-id="d8092-153">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="d8092-153">Geometry Shader</span></span> | <span data-ttu-id="d8092-154">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d8092-154">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d8092-155">x</span><span class="sxs-lookup"><span data-stu-id="d8092-155">x</span></span>             | <span data-ttu-id="d8092-156">x</span><span class="sxs-lookup"><span data-stu-id="d8092-156">x</span></span>               | <span data-ttu-id="d8092-157">x</span><span class="sxs-lookup"><span data-stu-id="d8092-157">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d8092-158">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="d8092-158">Minimum Shader Model</span></span>

<span data-ttu-id="d8092-159">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d8092-159">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d8092-160">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d8092-160">Shader Model</span></span>                                              | <span data-ttu-id="d8092-161">Compatible</span><span class="sxs-lookup"><span data-stu-id="d8092-161">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d8092-162">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d8092-162">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d8092-163">sí</span><span class="sxs-lookup"><span data-stu-id="d8092-163">yes</span></span>       |
| [<span data-ttu-id="d8092-164">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="d8092-164">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d8092-165">sí</span><span class="sxs-lookup"><span data-stu-id="d8092-165">yes</span></span>       |
| [<span data-ttu-id="d8092-166">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="d8092-166">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d8092-167">sí</span><span class="sxs-lookup"><span data-stu-id="d8092-167">yes</span></span>       |
| [<span data-ttu-id="d8092-168">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8092-168">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d8092-169">no</span><span class="sxs-lookup"><span data-stu-id="d8092-169">no</span></span>        |
| [<span data-ttu-id="d8092-170">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8092-170">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d8092-171">no</span><span class="sxs-lookup"><span data-stu-id="d8092-171">no</span></span>        |
| [<span data-ttu-id="d8092-172">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8092-172">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d8092-173">no</span><span class="sxs-lookup"><span data-stu-id="d8092-173">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d8092-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8092-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8092-175">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d8092-175">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





