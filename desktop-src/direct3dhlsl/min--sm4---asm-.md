---
title: min (sm4 - asm)
description: Mínimo flotante por componente.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8791589b77edc66eeab4b48f10f4a9b16b5cb2d9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993902"
---
# <a name="min-sm4---asm"></a><span data-ttu-id="7e11e-103">min (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="7e11e-103">min (sm4 - asm)</span></span>

<span data-ttu-id="7e11e-104">Mínimo flotante por componente.</span><span class="sxs-lookup"><span data-stu-id="7e11e-104">Component-wise float minimum.</span></span>



| <span data-ttu-id="7e11e-105">min \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , \[ - \] src1 abs \[ \_ \] \[ .sw swle \] ,</span><span class="sxs-lookup"><span data-stu-id="7e11e-105">min\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="7e11e-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="7e11e-106">Item</span></span>                                                            | <span data-ttu-id="7e11e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e11e-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e11e-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="7e11e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="7e11e-109">\[en \] El resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="7e11e-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="7e11e-110">*dest*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="7e11e-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="7e11e-111">*src0:* *src1*</span><span class="sxs-lookup"><span data-stu-id="7e11e-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="7e11e-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="7e11e-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="7e11e-113">\[en \] Los componentes que se comparan con *src1*.</span><span class="sxs-lookup"><span data-stu-id="7e11e-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                  |
| <span data-ttu-id="7e11e-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="7e11e-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="7e11e-115">\[en \] Los componentes que se comparan con *src0*.</span><span class="sxs-lookup"><span data-stu-id="7e11e-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="7e11e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e11e-116">Remarks</span></span>

><span data-ttu-id="7e11e-117">= se usa en lugar > para que si min(x,y) = x, max(x,y) = y.</span><span class="sxs-lookup"><span data-stu-id="7e11e-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="7e11e-118">NaN tiene un control especial.</span><span class="sxs-lookup"><span data-stu-id="7e11e-118">NaN has special handling.</span></span> <span data-ttu-id="7e11e-119">Si un operando de origen es NaN, se devuelve el otro operando de origen y la elección se realiza por componente.</span><span class="sxs-lookup"><span data-stu-id="7e11e-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="7e11e-120">Si ambos son NaN, se devuelve cualquier representación de NaN.</span><span class="sxs-lookup"><span data-stu-id="7e11e-120">If both are NaN, any NaN representation is returned.</span></span> <span data-ttu-id="7e11e-121">Esto se ajusta a las nuevas reglas IEEE 754R.</span><span class="sxs-lookup"><span data-stu-id="7e11e-121">This conforms to new IEEE 754R rules.</span></span>

<span data-ttu-id="7e11e-122">Los desnormas se vacían, con el signo conservado, antes de la comparación.</span><span class="sxs-lookup"><span data-stu-id="7e11e-122">Denorms are flushed, with the sign preserved, before comparison.</span></span> <span data-ttu-id="7e11e-123">Sin embargo, el resultado escrito *en dest* puede o no vaciarse desnormado.</span><span class="sxs-lookup"><span data-stu-id="7e11e-123">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="7e11e-124">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzcan desbordamientos ni subdesbordes.</span><span class="sxs-lookup"><span data-stu-id="7e11e-124">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="7e11e-125">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="7e11e-125">F means finite real number.</span></span>



| <span data-ttu-id="7e11e-126">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="7e11e-126">**src0 src1->**</span></span> | <span data-ttu-id="7e11e-127">**-inf**</span><span class="sxs-lookup"><span data-stu-id="7e11e-127">**-inf**</span></span> | <span data-ttu-id="7e11e-128">**F**</span><span class="sxs-lookup"><span data-stu-id="7e11e-128">**F**</span></span>        | <span data-ttu-id="7e11e-129">**+inf**</span><span class="sxs-lookup"><span data-stu-id="7e11e-129">**+inf**</span></span> | <span data-ttu-id="7e11e-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="7e11e-130">**NaN**</span></span> |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="7e11e-131">**-inf**</span><span class="sxs-lookup"><span data-stu-id="7e11e-131">**-inf**</span></span>           | <span data-ttu-id="7e11e-132">-inf</span><span class="sxs-lookup"><span data-stu-id="7e11e-132">-inf</span></span>     | <span data-ttu-id="7e11e-133">-inf</span><span class="sxs-lookup"><span data-stu-id="7e11e-133">-inf</span></span>         | <span data-ttu-id="7e11e-134">-inf</span><span class="sxs-lookup"><span data-stu-id="7e11e-134">-inf</span></span>     | <span data-ttu-id="7e11e-135">-inf</span><span class="sxs-lookup"><span data-stu-id="7e11e-135">-inf</span></span>    |
| <span data-ttu-id="7e11e-136">**F**</span><span class="sxs-lookup"><span data-stu-id="7e11e-136">**F**</span></span>              | <span data-ttu-id="7e11e-137">-inf</span><span class="sxs-lookup"><span data-stu-id="7e11e-137">-inf</span></span>     | <span data-ttu-id="7e11e-138">src0 o src1</span><span class="sxs-lookup"><span data-stu-id="7e11e-138">src0 or src1</span></span> | <span data-ttu-id="7e11e-139">src0</span><span class="sxs-lookup"><span data-stu-id="7e11e-139">src0</span></span>     | <span data-ttu-id="7e11e-140">src0</span><span class="sxs-lookup"><span data-stu-id="7e11e-140">src0</span></span>    |
| <span data-ttu-id="7e11e-141">**-inf**</span><span class="sxs-lookup"><span data-stu-id="7e11e-141">**-inf**</span></span>           | <span data-ttu-id="7e11e-142">-inf</span><span class="sxs-lookup"><span data-stu-id="7e11e-142">-inf</span></span>     | <span data-ttu-id="7e11e-143">src1</span><span class="sxs-lookup"><span data-stu-id="7e11e-143">src1</span></span>         | <span data-ttu-id="7e11e-144">+inf</span><span class="sxs-lookup"><span data-stu-id="7e11e-144">+inf</span></span>     | <span data-ttu-id="7e11e-145">+inf</span><span class="sxs-lookup"><span data-stu-id="7e11e-145">+inf</span></span>    |
| <span data-ttu-id="7e11e-146">**NaN**</span><span class="sxs-lookup"><span data-stu-id="7e11e-146">**NaN**</span></span>            | <span data-ttu-id="7e11e-147">-inf</span><span class="sxs-lookup"><span data-stu-id="7e11e-147">-inf</span></span>     | <span data-ttu-id="7e11e-148">src1</span><span class="sxs-lookup"><span data-stu-id="7e11e-148">src1</span></span>         | <span data-ttu-id="7e11e-149">+inf</span><span class="sxs-lookup"><span data-stu-id="7e11e-149">+inf</span></span>     | <span data-ttu-id="7e11e-150">NaN</span><span class="sxs-lookup"><span data-stu-id="7e11e-150">NaN</span></span>     |



 

<span data-ttu-id="7e11e-151">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="7e11e-151">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7e11e-152">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="7e11e-152">Vertex Shader</span></span> | <span data-ttu-id="7e11e-153">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="7e11e-153">Geometry Shader</span></span> | <span data-ttu-id="7e11e-154">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="7e11e-154">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7e11e-155">x</span><span class="sxs-lookup"><span data-stu-id="7e11e-155">x</span></span>             | <span data-ttu-id="7e11e-156">x</span><span class="sxs-lookup"><span data-stu-id="7e11e-156">x</span></span>               | <span data-ttu-id="7e11e-157">x</span><span class="sxs-lookup"><span data-stu-id="7e11e-157">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7e11e-158">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="7e11e-158">Minimum Shader Model</span></span>

<span data-ttu-id="7e11e-159">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7e11e-159">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7e11e-160">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="7e11e-160">Shader Model</span></span>                                              | <span data-ttu-id="7e11e-161">Compatible</span><span class="sxs-lookup"><span data-stu-id="7e11e-161">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7e11e-162">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="7e11e-162">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7e11e-163">sí</span><span class="sxs-lookup"><span data-stu-id="7e11e-163">yes</span></span>       |
| [<span data-ttu-id="7e11e-164">Modelo de sombreador 4.1</span><span class="sxs-lookup"><span data-stu-id="7e11e-164">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7e11e-165">sí</span><span class="sxs-lookup"><span data-stu-id="7e11e-165">yes</span></span>       |
| [<span data-ttu-id="7e11e-166">Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="7e11e-166">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7e11e-167">sí</span><span class="sxs-lookup"><span data-stu-id="7e11e-167">yes</span></span>       |
| [<span data-ttu-id="7e11e-168">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e11e-168">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7e11e-169">no</span><span class="sxs-lookup"><span data-stu-id="7e11e-169">no</span></span>        |
| [<span data-ttu-id="7e11e-170">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e11e-170">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7e11e-171">no</span><span class="sxs-lookup"><span data-stu-id="7e11e-171">no</span></span>        |
| [<span data-ttu-id="7e11e-172">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e11e-172">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7e11e-173">no</span><span class="sxs-lookup"><span data-stu-id="7e11e-173">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7e11e-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e11e-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e11e-175">Ensamblado del modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e11e-175">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





