---
title: frc (sm4 - asm)
description: Por componente, extraiga el componente fraccionario.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f59b747f38fb970b92b5e48610873efe781d63d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993922"
---
# <a name="frc-sm4---asm"></a><span data-ttu-id="54f5a-103">frc (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="54f5a-103">frc (sm4 - asm)</span></span>

<span data-ttu-id="54f5a-104">Por componente, extraiga el componente fraccionario.</span><span class="sxs-lookup"><span data-stu-id="54f5a-104">Component-wise, extract fractional component.</span></span>



| <span data-ttu-id="54f5a-105">frc \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle\]</span><span class="sxs-lookup"><span data-stu-id="54f5a-105">frc\[\_sat\] dest\[.mask\], \[-\] src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="54f5a-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="54f5a-106">Item</span></span>                                                            | <span data-ttu-id="54f5a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="54f5a-107">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54f5a-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="54f5a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="54f5a-109">\[en \] La dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="54f5a-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="54f5a-110">*dest*  =  *src0*  -  [round \_ ni](round-ni--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="54f5a-110">*dest* = *src0* - [round\_ni](round-ni--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="54f5a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="54f5a-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="54f5a-112">\[en \] el componente de la operación.</span><span class="sxs-lookup"><span data-stu-id="54f5a-112">\[in\] The component in the operation.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="54f5a-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54f5a-113">Remarks</span></span>

<span data-ttu-id="54f5a-114">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.</span><span class="sxs-lookup"><span data-stu-id="54f5a-114">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="54f5a-115">**src**</span><span class="sxs-lookup"><span data-stu-id="54f5a-115">**src**</span></span>  | <span data-ttu-id="54f5a-116">**-inf**</span><span class="sxs-lookup"><span data-stu-id="54f5a-116">**-inf**</span></span> | <span data-ttu-id="54f5a-117">**-F**</span><span class="sxs-lookup"><span data-stu-id="54f5a-117">**-F**</span></span>     | <span data-ttu-id="54f5a-118">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="54f5a-118">**-denorm**</span></span> | <span data-ttu-id="54f5a-119">**-0**</span><span class="sxs-lookup"><span data-stu-id="54f5a-119">**-0**</span></span> | <span data-ttu-id="54f5a-120">**+0**</span><span class="sxs-lookup"><span data-stu-id="54f5a-120">**+0**</span></span> | <span data-ttu-id="54f5a-121">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="54f5a-121">**+denorm**</span></span> | <span data-ttu-id="54f5a-122">**+F**</span><span class="sxs-lookup"><span data-stu-id="54f5a-122">**+F**</span></span>     | <span data-ttu-id="54f5a-123">**+inf**</span><span class="sxs-lookup"><span data-stu-id="54f5a-123">**+inf**</span></span> | <span data-ttu-id="54f5a-124">**NaN**</span><span class="sxs-lookup"><span data-stu-id="54f5a-124">**NaN**</span></span> |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="54f5a-125">**Dest**</span><span class="sxs-lookup"><span data-stu-id="54f5a-125">**dest**</span></span> | <span data-ttu-id="54f5a-126">NaN</span><span class="sxs-lookup"><span data-stu-id="54f5a-126">NaN</span></span>      | <span data-ttu-id="54f5a-127">\[+0 a 1)</span><span class="sxs-lookup"><span data-stu-id="54f5a-127">\[+0 to 1)</span></span> | <span data-ttu-id="54f5a-128">+0</span><span class="sxs-lookup"><span data-stu-id="54f5a-128">+0</span></span>          | <span data-ttu-id="54f5a-129">+0</span><span class="sxs-lookup"><span data-stu-id="54f5a-129">+0</span></span>     | <span data-ttu-id="54f5a-130">+0</span><span class="sxs-lookup"><span data-stu-id="54f5a-130">+0</span></span>     | <span data-ttu-id="54f5a-131">+0</span><span class="sxs-lookup"><span data-stu-id="54f5a-131">+0</span></span>          | <span data-ttu-id="54f5a-132">\[+0 a 1)</span><span class="sxs-lookup"><span data-stu-id="54f5a-132">\[+0 to 1)</span></span> | <span data-ttu-id="54f5a-133">NaN</span><span class="sxs-lookup"><span data-stu-id="54f5a-133">NaN</span></span>      | <span data-ttu-id="54f5a-134">NaN</span><span class="sxs-lookup"><span data-stu-id="54f5a-134">NaN</span></span>     |



 

<span data-ttu-id="54f5a-135">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="54f5a-135">F means finite-real number.</span></span>

<span data-ttu-id="54f5a-136">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="54f5a-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="54f5a-137">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="54f5a-137">Vertex Shader</span></span> | <span data-ttu-id="54f5a-138">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="54f5a-138">Geometry Shader</span></span> | <span data-ttu-id="54f5a-139">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="54f5a-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="54f5a-140">x</span><span class="sxs-lookup"><span data-stu-id="54f5a-140">x</span></span>             | <span data-ttu-id="54f5a-141">x</span><span class="sxs-lookup"><span data-stu-id="54f5a-141">x</span></span>               | <span data-ttu-id="54f5a-142">x</span><span class="sxs-lookup"><span data-stu-id="54f5a-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="54f5a-143">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="54f5a-143">Minimum Shader Model</span></span>

<span data-ttu-id="54f5a-144">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="54f5a-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="54f5a-145">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="54f5a-145">Shader Model</span></span>                                              | <span data-ttu-id="54f5a-146">Compatible</span><span class="sxs-lookup"><span data-stu-id="54f5a-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="54f5a-147">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="54f5a-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="54f5a-148">sí</span><span class="sxs-lookup"><span data-stu-id="54f5a-148">yes</span></span>       |
| [<span data-ttu-id="54f5a-149">Modelo de sombreador 4.1</span><span class="sxs-lookup"><span data-stu-id="54f5a-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="54f5a-150">sí</span><span class="sxs-lookup"><span data-stu-id="54f5a-150">yes</span></span>       |
| [<span data-ttu-id="54f5a-151">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="54f5a-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="54f5a-152">sí</span><span class="sxs-lookup"><span data-stu-id="54f5a-152">yes</span></span>       |
| [<span data-ttu-id="54f5a-153">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54f5a-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="54f5a-154">no</span><span class="sxs-lookup"><span data-stu-id="54f5a-154">no</span></span>        |
| [<span data-ttu-id="54f5a-155">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54f5a-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="54f5a-156">no</span><span class="sxs-lookup"><span data-stu-id="54f5a-156">no</span></span>        |
| [<span data-ttu-id="54f5a-157">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54f5a-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="54f5a-158">no</span><span class="sxs-lookup"><span data-stu-id="54f5a-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="54f5a-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54f5a-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54f5a-160">Ensamblado del modelo de sombreador 4 (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="54f5a-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





