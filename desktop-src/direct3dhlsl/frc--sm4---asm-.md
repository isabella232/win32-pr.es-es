---
title: FRC (SM4-ASM)
description: Por componentes, extraiga los componentes fraccionarios.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4abcfd56e7d6051e9c476097b3e5eef4d97563e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983875"
---
# <a name="frc-sm4---asm"></a><span data-ttu-id="dec86-103">FRC (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="dec86-103">frc (sm4 - asm)</span></span>

<span data-ttu-id="dec86-104">Por componentes, extraiga los componentes fraccionarios.</span><span class="sxs-lookup"><span data-stu-id="dec86-104">Component-wise, extract fractional component.</span></span>



| <span data-ttu-id="dec86-105">FRC \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="dec86-105">frc\[\_sat\] dest\[.mask\], \[-\] src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="dec86-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="dec86-106">Item</span></span>                                                            | <span data-ttu-id="dec86-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="dec86-107">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec86-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="dec86-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="dec86-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="dec86-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="dec86-110">*dest*  =  *src0*  -  [Round \_ ni](round-ni--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="dec86-110">*dest* = *src0* - [round\_ni](round-ni--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="dec86-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="dec86-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="dec86-112">\[en \] el componente de la operación.</span><span class="sxs-lookup"><span data-stu-id="dec86-112">\[in\] The component in the operation.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="dec86-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dec86-113">Remarks</span></span>

<span data-ttu-id="dec86-114">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.</span><span class="sxs-lookup"><span data-stu-id="dec86-114">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|          |          |            |             |        |        |             |            |          |         |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="dec86-115">**src**</span><span class="sxs-lookup"><span data-stu-id="dec86-115">**src**</span></span>  | <span data-ttu-id="dec86-116">**-INF**</span><span class="sxs-lookup"><span data-stu-id="dec86-116">**-inf**</span></span> | <span data-ttu-id="dec86-117">**-F**</span><span class="sxs-lookup"><span data-stu-id="dec86-117">**-F**</span></span>     | <span data-ttu-id="dec86-118">**-denormalización**</span><span class="sxs-lookup"><span data-stu-id="dec86-118">**-denorm**</span></span> | <span data-ttu-id="dec86-119">**-0**</span><span class="sxs-lookup"><span data-stu-id="dec86-119">**-0**</span></span> | <span data-ttu-id="dec86-120">**+0**</span><span class="sxs-lookup"><span data-stu-id="dec86-120">**+0**</span></span> | <span data-ttu-id="dec86-121">**+ denormalización**</span><span class="sxs-lookup"><span data-stu-id="dec86-121">**+denorm**</span></span> | <span data-ttu-id="dec86-122">**+ F**</span><span class="sxs-lookup"><span data-stu-id="dec86-122">**+F**</span></span>     | <span data-ttu-id="dec86-123">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="dec86-123">**+inf**</span></span> | <span data-ttu-id="dec86-124">**NaN**</span><span class="sxs-lookup"><span data-stu-id="dec86-124">**NaN**</span></span> |
| <span data-ttu-id="dec86-125">**dest**</span><span class="sxs-lookup"><span data-stu-id="dec86-125">**dest**</span></span> | <span data-ttu-id="dec86-126">NaN</span><span class="sxs-lookup"><span data-stu-id="dec86-126">NaN</span></span>      | <span data-ttu-id="dec86-127">\[+ 0 a 1)</span><span class="sxs-lookup"><span data-stu-id="dec86-127">\[+0 to 1)</span></span> | <span data-ttu-id="dec86-128">+0</span><span class="sxs-lookup"><span data-stu-id="dec86-128">+0</span></span>          | <span data-ttu-id="dec86-129">+0</span><span class="sxs-lookup"><span data-stu-id="dec86-129">+0</span></span>     | <span data-ttu-id="dec86-130">+0</span><span class="sxs-lookup"><span data-stu-id="dec86-130">+0</span></span>     | <span data-ttu-id="dec86-131">+0</span><span class="sxs-lookup"><span data-stu-id="dec86-131">+0</span></span>          | <span data-ttu-id="dec86-132">\[+ 0 a 1)</span><span class="sxs-lookup"><span data-stu-id="dec86-132">\[+0 to 1)</span></span> | <span data-ttu-id="dec86-133">NaN</span><span class="sxs-lookup"><span data-stu-id="dec86-133">NaN</span></span>      | <span data-ttu-id="dec86-134">NaN</span><span class="sxs-lookup"><span data-stu-id="dec86-134">NaN</span></span>     |



 

<span data-ttu-id="dec86-135">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="dec86-135">F means finite-real number.</span></span>

<span data-ttu-id="dec86-136">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="dec86-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dec86-137">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="dec86-137">Vertex Shader</span></span> | <span data-ttu-id="dec86-138">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="dec86-138">Geometry Shader</span></span> | <span data-ttu-id="dec86-139">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="dec86-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="dec86-140">x</span><span class="sxs-lookup"><span data-stu-id="dec86-140">x</span></span>             | <span data-ttu-id="dec86-141">x</span><span class="sxs-lookup"><span data-stu-id="dec86-141">x</span></span>               | <span data-ttu-id="dec86-142">x</span><span class="sxs-lookup"><span data-stu-id="dec86-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dec86-143">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="dec86-143">Minimum Shader Model</span></span>

<span data-ttu-id="dec86-144">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dec86-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dec86-145">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="dec86-145">Shader Model</span></span>                                              | <span data-ttu-id="dec86-146">Compatible</span><span class="sxs-lookup"><span data-stu-id="dec86-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dec86-147">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="dec86-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dec86-148">sí</span><span class="sxs-lookup"><span data-stu-id="dec86-148">yes</span></span>       |
| [<span data-ttu-id="dec86-149">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="dec86-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dec86-150">sí</span><span class="sxs-lookup"><span data-stu-id="dec86-150">yes</span></span>       |
| [<span data-ttu-id="dec86-151">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="dec86-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dec86-152">sí</span><span class="sxs-lookup"><span data-stu-id="dec86-152">yes</span></span>       |
| [<span data-ttu-id="dec86-153">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dec86-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dec86-154">no</span><span class="sxs-lookup"><span data-stu-id="dec86-154">no</span></span>        |
| [<span data-ttu-id="dec86-155">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dec86-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dec86-156">no</span><span class="sxs-lookup"><span data-stu-id="dec86-156">no</span></span>        |
| [<span data-ttu-id="dec86-157">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dec86-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dec86-158">no</span><span class="sxs-lookup"><span data-stu-id="dec86-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dec86-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dec86-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dec86-160">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dec86-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





