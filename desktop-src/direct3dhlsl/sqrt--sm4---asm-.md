---
title: sqrt (sm4 - asm)
description: Raíz cuadrada por componente.
ms.assetid: B860D656-7F01-484F-909F-A5C9A61C52C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 628601e0a3a78784a5fd1a089ef7608a0cf9ca05
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996612"
---
# <a name="sqrt-sm4---asm"></a><span data-ttu-id="04db2-103">sqrt (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="04db2-103">sqrt (sm4 - asm)</span></span>

<span data-ttu-id="04db2-104">Raíz cuadrada por componente.</span><span class="sxs-lookup"><span data-stu-id="04db2-104">Component-wise square root.</span></span>



| <span data-ttu-id="04db2-105">sqrt \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle\]</span><span class="sxs-lookup"><span data-stu-id="04db2-105">sqrt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="04db2-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="04db2-106">Item</span></span>                                                            | <span data-ttu-id="04db2-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="04db2-107">Description</span></span>                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="04db2-108"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="04db2-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="04db2-109">\[en \] El resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="04db2-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="04db2-110">*dest* = sqrt(*src0*)</span><span class="sxs-lookup"><span data-stu-id="04db2-110">*dest* = sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="04db2-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="04db2-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="04db2-112">\[en \] Componentes para los que se va a tomar la raíz cuadrada.</span><span class="sxs-lookup"><span data-stu-id="04db2-112">\[in\] The components for which to take the square root.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="04db2-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04db2-113">Remarks</span></span>

<span data-ttu-id="04db2-114">La precisión es de 1 ulp.</span><span class="sxs-lookup"><span data-stu-id="04db2-114">Precision is 1 ulp.</span></span>

<span data-ttu-id="04db2-115">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzca ningún desbordamiento o subdesbordmiento.</span><span class="sxs-lookup"><span data-stu-id="04db2-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="04db2-116">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="04db2-116">F means finite-real number.</span></span>



|          | <span data-ttu-id="04db2-117">**-inf**</span><span class="sxs-lookup"><span data-stu-id="04db2-117">**-inf**</span></span> | <span data-ttu-id="04db2-118">**-F**</span><span class="sxs-lookup"><span data-stu-id="04db2-118">**-F**</span></span> | <span data-ttu-id="04db2-119">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="04db2-119">**-denorm**</span></span> | <span data-ttu-id="04db2-120">**-0**</span><span class="sxs-lookup"><span data-stu-id="04db2-120">**-0**</span></span> | <span data-ttu-id="04db2-121">**+0**</span><span class="sxs-lookup"><span data-stu-id="04db2-121">**+0**</span></span> | <span data-ttu-id="04db2-122">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="04db2-122">**+denorm**</span></span> | <span data-ttu-id="04db2-123">**+F**</span><span class="sxs-lookup"><span data-stu-id="04db2-123">**+F**</span></span> | <span data-ttu-id="04db2-124">**+inf**</span><span class="sxs-lookup"><span data-stu-id="04db2-124">**+inf**</span></span> | <span data-ttu-id="04db2-125">**NaN**</span><span class="sxs-lookup"><span data-stu-id="04db2-125">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="04db2-126">**Dest**</span><span class="sxs-lookup"><span data-stu-id="04db2-126">**dest**</span></span> | <span data-ttu-id="04db2-127">NaN</span><span class="sxs-lookup"><span data-stu-id="04db2-127">NaN</span></span>      | <span data-ttu-id="04db2-128">NaN</span><span class="sxs-lookup"><span data-stu-id="04db2-128">NaN</span></span>    | <span data-ttu-id="04db2-129">-0</span><span class="sxs-lookup"><span data-stu-id="04db2-129">-0</span></span>          | <span data-ttu-id="04db2-130">-0</span><span class="sxs-lookup"><span data-stu-id="04db2-130">-0</span></span>     | <span data-ttu-id="04db2-131">+0</span><span class="sxs-lookup"><span data-stu-id="04db2-131">+0</span></span>     | <span data-ttu-id="04db2-132">+0</span><span class="sxs-lookup"><span data-stu-id="04db2-132">+0</span></span>          | <span data-ttu-id="04db2-133">+F</span><span class="sxs-lookup"><span data-stu-id="04db2-133">+F</span></span>     | <span data-ttu-id="04db2-134">+inf</span><span class="sxs-lookup"><span data-stu-id="04db2-134">+inf</span></span>     | <span data-ttu-id="04db2-135">NaN</span><span class="sxs-lookup"><span data-stu-id="04db2-135">NaN</span></span>     |



 

<span data-ttu-id="04db2-136">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="04db2-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="04db2-137">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="04db2-137">Vertex Shader</span></span> | <span data-ttu-id="04db2-138">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="04db2-138">Geometry Shader</span></span> | <span data-ttu-id="04db2-139">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="04db2-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="04db2-140">x</span><span class="sxs-lookup"><span data-stu-id="04db2-140">x</span></span>             | <span data-ttu-id="04db2-141">x</span><span class="sxs-lookup"><span data-stu-id="04db2-141">x</span></span>               | <span data-ttu-id="04db2-142">x</span><span class="sxs-lookup"><span data-stu-id="04db2-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="04db2-143">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="04db2-143">Minimum Shader Model</span></span>

<span data-ttu-id="04db2-144">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="04db2-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="04db2-145">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="04db2-145">Shader Model</span></span>                                              | <span data-ttu-id="04db2-146">Compatible</span><span class="sxs-lookup"><span data-stu-id="04db2-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="04db2-147">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="04db2-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="04db2-148">sí</span><span class="sxs-lookup"><span data-stu-id="04db2-148">yes</span></span>       |
| [<span data-ttu-id="04db2-149">Modelo de sombreador 4.1</span><span class="sxs-lookup"><span data-stu-id="04db2-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="04db2-150">sí</span><span class="sxs-lookup"><span data-stu-id="04db2-150">yes</span></span>       |
| [<span data-ttu-id="04db2-151">Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="04db2-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="04db2-152">sí</span><span class="sxs-lookup"><span data-stu-id="04db2-152">yes</span></span>       |
| [<span data-ttu-id="04db2-153">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04db2-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="04db2-154">no</span><span class="sxs-lookup"><span data-stu-id="04db2-154">no</span></span>        |
| [<span data-ttu-id="04db2-155">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04db2-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="04db2-156">no</span><span class="sxs-lookup"><span data-stu-id="04db2-156">no</span></span>        |
| [<span data-ttu-id="04db2-157">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04db2-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="04db2-158">no</span><span class="sxs-lookup"><span data-stu-id="04db2-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="04db2-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04db2-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04db2-160">Ensamblado del modelo 4 del sombreador (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="04db2-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





