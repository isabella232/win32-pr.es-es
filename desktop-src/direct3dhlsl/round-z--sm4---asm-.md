---
title: round_z (sm4 - asm)
description: Punto flotante redondeado a flotante entero. | round_z (sm4 - asm)
ms.assetid: 97C0E0F2-2571-4A94-BB04-B0CDBA0B5C0C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc874c6d0a1f26902086af300784c55950b71569
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997132"
---
# <a name="round_z-sm4---asm"></a><span data-ttu-id="ec414-104">round \_ z (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="ec414-104">round\_z (sm4 - asm)</span></span>

<span data-ttu-id="ec414-105">Punto flotante redondeado a flotante entero.</span><span class="sxs-lookup"><span data-stu-id="ec414-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="ec414-106">round \_ z \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swzzle\]</span><span class="sxs-lookup"><span data-stu-id="ec414-106">round\_z\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------|



 



| <span data-ttu-id="ec414-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="ec414-107">Item</span></span>                                                            | <span data-ttu-id="ec414-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec414-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="ec414-109"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="ec414-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ec414-110">\[en \] La dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="ec414-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="ec414-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ec414-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ec414-112">\[en \] Los componentes de la operación.</span><span class="sxs-lookup"><span data-stu-id="ec414-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="ec414-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ec414-113">Remarks</span></span>

<span data-ttu-id="ec414-114">Esta instrucción realiza una ronda de punto flotante por componente de los valores de *src0,* escribiendo valores de punto flotante enteros *en dest*.</span><span class="sxs-lookup"><span data-stu-id="ec414-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="ec414-115">**round \_ z** se redondea hacia cero.</span><span class="sxs-lookup"><span data-stu-id="ec414-115">**round\_z** rounds towards zero.</span></span>

<span data-ttu-id="ec414-116">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.</span><span class="sxs-lookup"><span data-stu-id="ec414-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="ec414-117">**src**</span><span class="sxs-lookup"><span data-stu-id="ec414-117">**src**</span></span>  | <span data-ttu-id="ec414-118">**-inf**</span><span class="sxs-lookup"><span data-stu-id="ec414-118">**-inf**</span></span> | <span data-ttu-id="ec414-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="ec414-119">**-F**</span></span> | <span data-ttu-id="ec414-120">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="ec414-120">**-denorm**</span></span> | <span data-ttu-id="ec414-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="ec414-121">**-0**</span></span> | <span data-ttu-id="ec414-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="ec414-122">**+0**</span></span> | <span data-ttu-id="ec414-123">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="ec414-123">**+denorm**</span></span> | <span data-ttu-id="ec414-124">**+F**</span><span class="sxs-lookup"><span data-stu-id="ec414-124">**+F**</span></span> | <span data-ttu-id="ec414-125">**+inf**</span><span class="sxs-lookup"><span data-stu-id="ec414-125">**+inf**</span></span> | <span data-ttu-id="ec414-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="ec414-126">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="ec414-127">**Dest**</span><span class="sxs-lookup"><span data-stu-id="ec414-127">**dest**</span></span> | <span data-ttu-id="ec414-128">-inf</span><span class="sxs-lookup"><span data-stu-id="ec414-128">-inf</span></span>     | <span data-ttu-id="ec414-129">-F</span><span class="sxs-lookup"><span data-stu-id="ec414-129">-F</span></span>     | <span data-ttu-id="ec414-130">-0</span><span class="sxs-lookup"><span data-stu-id="ec414-130">-0</span></span>          | <span data-ttu-id="ec414-131">-0</span><span class="sxs-lookup"><span data-stu-id="ec414-131">-0</span></span>     | <span data-ttu-id="ec414-132">+0</span><span class="sxs-lookup"><span data-stu-id="ec414-132">+0</span></span>     | <span data-ttu-id="ec414-133">+0</span><span class="sxs-lookup"><span data-stu-id="ec414-133">+0</span></span>          | <span data-ttu-id="ec414-134">+F</span><span class="sxs-lookup"><span data-stu-id="ec414-134">+F</span></span>     | <span data-ttu-id="ec414-135">+inf</span><span class="sxs-lookup"><span data-stu-id="ec414-135">+inf</span></span>     | <span data-ttu-id="ec414-136">NaN</span><span class="sxs-lookup"><span data-stu-id="ec414-136">NaN</span></span>     |



 

<span data-ttu-id="ec414-137">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="ec414-137">F means finite-real number.</span></span>

<span data-ttu-id="ec414-138">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="ec414-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ec414-139">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="ec414-139">Vertex Shader</span></span> | <span data-ttu-id="ec414-140">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="ec414-140">Geometry Shader</span></span> | <span data-ttu-id="ec414-141">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ec414-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ec414-142">x</span><span class="sxs-lookup"><span data-stu-id="ec414-142">x</span></span>             | <span data-ttu-id="ec414-143">x</span><span class="sxs-lookup"><span data-stu-id="ec414-143">x</span></span>               | <span data-ttu-id="ec414-144">x</span><span class="sxs-lookup"><span data-stu-id="ec414-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ec414-145">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ec414-145">Minimum Shader Model</span></span>

<span data-ttu-id="ec414-146">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ec414-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ec414-147">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ec414-147">Shader Model</span></span>                                              | <span data-ttu-id="ec414-148">Compatible</span><span class="sxs-lookup"><span data-stu-id="ec414-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ec414-149">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="ec414-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ec414-150">sí</span><span class="sxs-lookup"><span data-stu-id="ec414-150">yes</span></span>       |
| [<span data-ttu-id="ec414-151">Shader Model 4.1</span><span class="sxs-lookup"><span data-stu-id="ec414-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ec414-152">sí</span><span class="sxs-lookup"><span data-stu-id="ec414-152">yes</span></span>       |
| [<span data-ttu-id="ec414-153">Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="ec414-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ec414-154">sí</span><span class="sxs-lookup"><span data-stu-id="ec414-154">yes</span></span>       |
| [<span data-ttu-id="ec414-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ec414-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ec414-156">no</span><span class="sxs-lookup"><span data-stu-id="ec414-156">no</span></span>        |
| [<span data-ttu-id="ec414-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ec414-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ec414-158">no</span><span class="sxs-lookup"><span data-stu-id="ec414-158">no</span></span>        |
| [<span data-ttu-id="ec414-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ec414-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ec414-160">no</span><span class="sxs-lookup"><span data-stu-id="ec414-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ec414-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ec414-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec414-162">Ensamblado del modelo 4 del sombreador (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="ec414-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





