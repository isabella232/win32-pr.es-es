---
title: sqrt (SM4-ASM)
description: Raíz cuadrada de un componente.
ms.assetid: B860D656-7F01-484F-909F-A5C9A61C52C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a12afaf5b2366dac15c953d509a6814b48a6b9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419935"
---
# <a name="sqrt-sm4---asm"></a><span data-ttu-id="8a877-103">sqrt (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8a877-103">sqrt (sm4 - asm)</span></span>

<span data-ttu-id="8a877-104">Raíz cuadrada de un componente.</span><span class="sxs-lookup"><span data-stu-id="8a877-104">Component-wise square root.</span></span>



| <span data-ttu-id="8a877-105">sqrt \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="8a877-105">sqrt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="8a877-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="8a877-106">Item</span></span>                                                            | <span data-ttu-id="8a877-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a877-107">Description</span></span>                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8a877-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="8a877-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="8a877-109">\[en \] el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="8a877-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="8a877-110">*dest* = sqrt (*src0*)</span><span class="sxs-lookup"><span data-stu-id="8a877-110">*dest* = sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="8a877-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8a877-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="8a877-112">\[en \] los componentes para los que se va a tomar la raíz cuadrada.</span><span class="sxs-lookup"><span data-stu-id="8a877-112">\[in\] The components for which to take the square root.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="8a877-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a877-113">Remarks</span></span>

<span data-ttu-id="8a877-114">La precisión es 1 ULP.</span><span class="sxs-lookup"><span data-stu-id="8a877-114">Precision is 1 ulp.</span></span>

<span data-ttu-id="8a877-115">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento.</span><span class="sxs-lookup"><span data-stu-id="8a877-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="8a877-116">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="8a877-116">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
|          | <span data-ttu-id="8a877-117">**-INF**</span><span class="sxs-lookup"><span data-stu-id="8a877-117">**-inf**</span></span> | <span data-ttu-id="8a877-118">**-F**</span><span class="sxs-lookup"><span data-stu-id="8a877-118">**-F**</span></span> | <span data-ttu-id="8a877-119">**-denormalización**</span><span class="sxs-lookup"><span data-stu-id="8a877-119">**-denorm**</span></span> | <span data-ttu-id="8a877-120">**-0**</span><span class="sxs-lookup"><span data-stu-id="8a877-120">**-0**</span></span> | <span data-ttu-id="8a877-121">**+0**</span><span class="sxs-lookup"><span data-stu-id="8a877-121">**+0**</span></span> | <span data-ttu-id="8a877-122">**+ denormalización**</span><span class="sxs-lookup"><span data-stu-id="8a877-122">**+denorm**</span></span> | <span data-ttu-id="8a877-123">**+ F**</span><span class="sxs-lookup"><span data-stu-id="8a877-123">**+F**</span></span> | <span data-ttu-id="8a877-124">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="8a877-124">**+inf**</span></span> | <span data-ttu-id="8a877-125">**NaN**</span><span class="sxs-lookup"><span data-stu-id="8a877-125">**NaN**</span></span> |
| <span data-ttu-id="8a877-126">**dest**</span><span class="sxs-lookup"><span data-stu-id="8a877-126">**dest**</span></span> | <span data-ttu-id="8a877-127">NaN</span><span class="sxs-lookup"><span data-stu-id="8a877-127">NaN</span></span>      | <span data-ttu-id="8a877-128">NaN</span><span class="sxs-lookup"><span data-stu-id="8a877-128">NaN</span></span>    | <span data-ttu-id="8a877-129">-0</span><span class="sxs-lookup"><span data-stu-id="8a877-129">-0</span></span>          | <span data-ttu-id="8a877-130">-0</span><span class="sxs-lookup"><span data-stu-id="8a877-130">-0</span></span>     | <span data-ttu-id="8a877-131">+0</span><span class="sxs-lookup"><span data-stu-id="8a877-131">+0</span></span>     | <span data-ttu-id="8a877-132">+0</span><span class="sxs-lookup"><span data-stu-id="8a877-132">+0</span></span>          | <span data-ttu-id="8a877-133">+F</span><span class="sxs-lookup"><span data-stu-id="8a877-133">+F</span></span>     | <span data-ttu-id="8a877-134">+inf</span><span class="sxs-lookup"><span data-stu-id="8a877-134">+inf</span></span>     | <span data-ttu-id="8a877-135">NaN</span><span class="sxs-lookup"><span data-stu-id="8a877-135">NaN</span></span>     |



 

<span data-ttu-id="8a877-136">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="8a877-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8a877-137">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="8a877-137">Vertex Shader</span></span> | <span data-ttu-id="8a877-138">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="8a877-138">Geometry Shader</span></span> | <span data-ttu-id="8a877-139">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="8a877-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8a877-140">x</span><span class="sxs-lookup"><span data-stu-id="8a877-140">x</span></span>             | <span data-ttu-id="8a877-141">x</span><span class="sxs-lookup"><span data-stu-id="8a877-141">x</span></span>               | <span data-ttu-id="8a877-142">x</span><span class="sxs-lookup"><span data-stu-id="8a877-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8a877-143">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="8a877-143">Minimum Shader Model</span></span>

<span data-ttu-id="8a877-144">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8a877-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8a877-145">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="8a877-145">Shader Model</span></span>                                              | <span data-ttu-id="8a877-146">Compatible</span><span class="sxs-lookup"><span data-stu-id="8a877-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8a877-147">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8a877-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8a877-148">sí</span><span class="sxs-lookup"><span data-stu-id="8a877-148">yes</span></span>       |
| [<span data-ttu-id="8a877-149">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8a877-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8a877-150">sí</span><span class="sxs-lookup"><span data-stu-id="8a877-150">yes</span></span>       |
| [<span data-ttu-id="8a877-151">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8a877-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8a877-152">sí</span><span class="sxs-lookup"><span data-stu-id="8a877-152">yes</span></span>       |
| [<span data-ttu-id="8a877-153">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a877-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8a877-154">no</span><span class="sxs-lookup"><span data-stu-id="8a877-154">no</span></span>        |
| [<span data-ttu-id="8a877-155">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a877-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8a877-156">no</span><span class="sxs-lookup"><span data-stu-id="8a877-156">no</span></span>        |
| [<span data-ttu-id="8a877-157">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a877-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8a877-158">no</span><span class="sxs-lookup"><span data-stu-id="8a877-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8a877-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a877-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a877-160">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a877-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





