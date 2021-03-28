---
title: registro (SM4-ASM)
description: Base de registro de componentes 2.
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf99949e278ca302543437da346188b690789604
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077102"
---
# <a name="log-sm4---asm"></a><span data-ttu-id="a944d-103">registro (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a944d-103">log (sm4 - asm)</span></span>

<span data-ttu-id="a944d-104">Base de registro de componentes 2.</span><span class="sxs-lookup"><span data-stu-id="a944d-104">Component-wise log base 2.</span></span>



| <span data-ttu-id="a944d-105">log \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle</span><span class="sxs-lookup"><span data-stu-id="a944d-105">log\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="a944d-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a944d-106">Item</span></span>                                                            | <span data-ttu-id="a944d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a944d-107">Description</span></span>                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a944d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a944d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a944d-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="a944d-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="a944d-110">dest = LOG2 (src0)</span><span class="sxs-lookup"><span data-stu-id="a944d-110">dest = log2(src0)</span></span><br/> |
| <span data-ttu-id="a944d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a944d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a944d-112">\[en \] el valor de la operación.</span><span class="sxs-lookup"><span data-stu-id="a944d-112">\[in\] The value for the operation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="a944d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a944d-113">Remarks</span></span>

### <a name="restrictions"></a><span data-ttu-id="a944d-114">Restricciones</span><span class="sxs-lookup"><span data-stu-id="a944d-114">Restrictions</span></span>

-   <span data-ttu-id="a944d-115">Sigue la teoría de límites.</span><span class="sxs-lookup"><span data-stu-id="a944d-115">Follows limit theory.</span></span>
-   <span data-ttu-id="a944d-116">Tolerancia a errores: Si *src0* es \[ 0,5.. 2 \] , el error Absolue no debe ser superior a 2-21.</span><span class="sxs-lookup"><span data-stu-id="a944d-116">Error tolerance: If *src0* is \[0.5..2\], absolue error must be no more than 2-21.</span></span> <span data-ttu-id="a944d-117">Si *src0* es (0.. 0.5) o (2.. + inf \] , el error relativo no debe ser superior a 2-21.</span><span class="sxs-lookup"><span data-stu-id="a944d-117">If *src0* is (0..0.5) or (2..+INF\], relative error must be no more than 2-21.</span></span>

<span data-ttu-id="a944d-118">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento.</span><span class="sxs-lookup"><span data-stu-id="a944d-118">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="a944d-119">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="a944d-119">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="a944d-120">**src**</span><span class="sxs-lookup"><span data-stu-id="a944d-120">**src**</span></span>  | <span data-ttu-id="a944d-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="a944d-121">**-inf**</span></span> | <span data-ttu-id="a944d-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="a944d-122">**-F**</span></span> | <span data-ttu-id="a944d-123">**-denormalización**</span><span class="sxs-lookup"><span data-stu-id="a944d-123">**-denorm**</span></span> | <span data-ttu-id="a944d-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="a944d-124">**-0**</span></span> | <span data-ttu-id="a944d-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="a944d-125">**+0**</span></span> | <span data-ttu-id="a944d-126">**+ denormalización**</span><span class="sxs-lookup"><span data-stu-id="a944d-126">**+denorm**</span></span> | <span data-ttu-id="a944d-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="a944d-127">**+F**</span></span> | <span data-ttu-id="a944d-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="a944d-128">**+inf**</span></span> | <span data-ttu-id="a944d-129">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a944d-129">**NaN**</span></span> |
| <span data-ttu-id="a944d-130">**dest**</span><span class="sxs-lookup"><span data-stu-id="a944d-130">**dest**</span></span> | <span data-ttu-id="a944d-131">NaN</span><span class="sxs-lookup"><span data-stu-id="a944d-131">NaN</span></span>      | <span data-ttu-id="a944d-132">NaN</span><span class="sxs-lookup"><span data-stu-id="a944d-132">NaN</span></span>    | <span data-ttu-id="a944d-133">-inf</span><span class="sxs-lookup"><span data-stu-id="a944d-133">-inf</span></span>        | <span data-ttu-id="a944d-134">-inf</span><span class="sxs-lookup"><span data-stu-id="a944d-134">-inf</span></span>   | <span data-ttu-id="a944d-135">-inf</span><span class="sxs-lookup"><span data-stu-id="a944d-135">-inf</span></span>   | <span data-ttu-id="a944d-136">-inf</span><span class="sxs-lookup"><span data-stu-id="a944d-136">-inf</span></span>        | <span data-ttu-id="a944d-137">F</span><span class="sxs-lookup"><span data-stu-id="a944d-137">F</span></span>      | <span data-ttu-id="a944d-138">+inf</span><span class="sxs-lookup"><span data-stu-id="a944d-138">+inf</span></span>     | <span data-ttu-id="a944d-139">NaN</span><span class="sxs-lookup"><span data-stu-id="a944d-139">NaN</span></span>     |



 

<span data-ttu-id="a944d-140">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="a944d-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a944d-141">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a944d-141">Vertex Shader</span></span> | <span data-ttu-id="a944d-142">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="a944d-142">Geometry Shader</span></span> | <span data-ttu-id="a944d-143">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="a944d-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a944d-144">x</span><span class="sxs-lookup"><span data-stu-id="a944d-144">x</span></span>             | <span data-ttu-id="a944d-145">x</span><span class="sxs-lookup"><span data-stu-id="a944d-145">x</span></span>               | <span data-ttu-id="a944d-146">x</span><span class="sxs-lookup"><span data-stu-id="a944d-146">x</span></span>            |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="a944d-147">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a944d-147">Minimum Shader Model</span></span>

<span data-ttu-id="a944d-148">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a944d-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a944d-149">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a944d-149">Shader Model</span></span>                                              | <span data-ttu-id="a944d-150">Compatible</span><span class="sxs-lookup"><span data-stu-id="a944d-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a944d-151">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a944d-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a944d-152">sí</span><span class="sxs-lookup"><span data-stu-id="a944d-152">yes</span></span>       |
| [<span data-ttu-id="a944d-153">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a944d-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a944d-154">sí</span><span class="sxs-lookup"><span data-stu-id="a944d-154">yes</span></span>       |
| [<span data-ttu-id="a944d-155">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a944d-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a944d-156">sí</span><span class="sxs-lookup"><span data-stu-id="a944d-156">yes</span></span>       |
| [<span data-ttu-id="a944d-157">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a944d-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a944d-158">no</span><span class="sxs-lookup"><span data-stu-id="a944d-158">no</span></span>        |
| [<span data-ttu-id="a944d-159">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a944d-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a944d-160">no</span><span class="sxs-lookup"><span data-stu-id="a944d-160">no</span></span>        |
| [<span data-ttu-id="a944d-161">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a944d-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a944d-162">no</span><span class="sxs-lookup"><span data-stu-id="a944d-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a944d-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a944d-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a944d-164">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a944d-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





