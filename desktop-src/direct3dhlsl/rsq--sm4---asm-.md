---
title: rsq (sm4 - asm)
description: Raíz cuadrada mutua por componente.
ms.assetid: CDA3C2DF-2793-4CE3-87CE-4E0AA945A1BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1528e9f187ff7d4fb6074d42a1c574686f3b22f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998172"
---
# <a name="rsq-sm4---asm"></a><span data-ttu-id="f4b57-103">rsq (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="f4b57-103">rsq (sm4 - asm)</span></span>

<span data-ttu-id="f4b57-104">Raíz cuadrada mutua por componente.</span><span class="sxs-lookup"><span data-stu-id="f4b57-104">Component-wise reciprocal square root.</span></span>



| <span data-ttu-id="f4b57-105">rsq \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle\]</span><span class="sxs-lookup"><span data-stu-id="f4b57-105">rsq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="f4b57-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="f4b57-106">Item</span></span>                                                            | <span data-ttu-id="f4b57-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4b57-107">Description</span></span>                                                                                      |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4b57-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="f4b57-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f4b57-109">\[en \] Contiene los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="f4b57-109">\[in\] Contains the results of the operation.</span></span><br/> <span data-ttu-id="f4b57-110">*dest* = 1.0f / sqrt(*src0*)</span><span class="sxs-lookup"><span data-stu-id="f4b57-110">*dest* = 1.0f / sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="f4b57-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f4b57-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f4b57-112">\[en \] Los componentes de la operación.</span><span class="sxs-lookup"><span data-stu-id="f4b57-112">\[in\] The components for the operation.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="f4b57-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4b57-113">Remarks</span></span>

<span data-ttu-id="f4b57-114">El error relativo máximo es 2-21.</span><span class="sxs-lookup"><span data-stu-id="f4b57-114">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="f4b57-115">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzca ningún desbordamiento o subdesbordmiento.</span><span class="sxs-lookup"><span data-stu-id="f4b57-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="f4b57-116">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="f4b57-116">F means finite-real number.</span></span>



| <span data-ttu-id="f4b57-117">**src**</span><span class="sxs-lookup"><span data-stu-id="f4b57-117">**src**</span></span>  | <span data-ttu-id="f4b57-118">**-inf**</span><span class="sxs-lookup"><span data-stu-id="f4b57-118">**-inf**</span></span> | <span data-ttu-id="f4b57-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="f4b57-119">**-F**</span></span> | <span data-ttu-id="f4b57-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="f4b57-120">**-denorm**</span></span> | <span data-ttu-id="f4b57-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="f4b57-121">**-0**</span></span> | <span data-ttu-id="f4b57-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="f4b57-122">**+0**</span></span> | <span data-ttu-id="f4b57-123">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="f4b57-123">**+denorm**</span></span> | <span data-ttu-id="f4b57-124">**+F**</span><span class="sxs-lookup"><span data-stu-id="f4b57-124">**+F**</span></span> | <span data-ttu-id="f4b57-125">**+inf**</span><span class="sxs-lookup"><span data-stu-id="f4b57-125">**+inf**</span></span> | <span data-ttu-id="f4b57-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="f4b57-126">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="f4b57-127">**Dest**</span><span class="sxs-lookup"><span data-stu-id="f4b57-127">**dest**</span></span> | <span data-ttu-id="f4b57-128">NaN</span><span class="sxs-lookup"><span data-stu-id="f4b57-128">NaN</span></span>      | <span data-ttu-id="f4b57-129">NaN</span><span class="sxs-lookup"><span data-stu-id="f4b57-129">NaN</span></span>    | <span data-ttu-id="f4b57-130">-inf</span><span class="sxs-lookup"><span data-stu-id="f4b57-130">-inf</span></span>        | <span data-ttu-id="f4b57-131">-inf</span><span class="sxs-lookup"><span data-stu-id="f4b57-131">-inf</span></span>   | <span data-ttu-id="f4b57-132">+inf</span><span class="sxs-lookup"><span data-stu-id="f4b57-132">+inf</span></span>   | <span data-ttu-id="f4b57-133">+inf</span><span class="sxs-lookup"><span data-stu-id="f4b57-133">+inf</span></span>        | <span data-ttu-id="f4b57-134">+F</span><span class="sxs-lookup"><span data-stu-id="f4b57-134">+F</span></span>     | <span data-ttu-id="f4b57-135">+0</span><span class="sxs-lookup"><span data-stu-id="f4b57-135">+0</span></span>       | <span data-ttu-id="f4b57-136">NaN</span><span class="sxs-lookup"><span data-stu-id="f4b57-136">NaN</span></span>     |



 

<span data-ttu-id="f4b57-137">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="f4b57-137">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f4b57-138">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="f4b57-138">Vertex Shader</span></span> | <span data-ttu-id="f4b57-139">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="f4b57-139">Geometry Shader</span></span> | <span data-ttu-id="f4b57-140">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="f4b57-140">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f4b57-141">x</span><span class="sxs-lookup"><span data-stu-id="f4b57-141">x</span></span>             | <span data-ttu-id="f4b57-142">x</span><span class="sxs-lookup"><span data-stu-id="f4b57-142">x</span></span>               | <span data-ttu-id="f4b57-143">x</span><span class="sxs-lookup"><span data-stu-id="f4b57-143">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f4b57-144">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="f4b57-144">Minimum Shader Model</span></span>

<span data-ttu-id="f4b57-145">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f4b57-145">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f4b57-146">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="f4b57-146">Shader Model</span></span>                                              | <span data-ttu-id="f4b57-147">Compatible</span><span class="sxs-lookup"><span data-stu-id="f4b57-147">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f4b57-148">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="f4b57-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f4b57-149">sí</span><span class="sxs-lookup"><span data-stu-id="f4b57-149">yes</span></span>       |
| [<span data-ttu-id="f4b57-150">Modelo de sombreador 4.1</span><span class="sxs-lookup"><span data-stu-id="f4b57-150">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f4b57-151">sí</span><span class="sxs-lookup"><span data-stu-id="f4b57-151">yes</span></span>       |
| [<span data-ttu-id="f4b57-152">Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="f4b57-152">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f4b57-153">sí</span><span class="sxs-lookup"><span data-stu-id="f4b57-153">yes</span></span>       |
| [<span data-ttu-id="f4b57-154">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4b57-154">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f4b57-155">no</span><span class="sxs-lookup"><span data-stu-id="f4b57-155">no</span></span>        |
| [<span data-ttu-id="f4b57-156">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4b57-156">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f4b57-157">no</span><span class="sxs-lookup"><span data-stu-id="f4b57-157">no</span></span>        |
| [<span data-ttu-id="f4b57-158">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4b57-158">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f4b57-159">no</span><span class="sxs-lookup"><span data-stu-id="f4b57-159">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f4b57-160">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4b57-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4b57-161">Ensamblado del modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4b57-161">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





