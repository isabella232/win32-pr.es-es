---
title: round_ni (sm4 - asm)
description: Punto flotante redondeado a float entero. | round_ni (sm4 - asm)
ms.assetid: 6DEF818B-AFF9-4B44-950E-320EACE1CAC4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2487715bbb2596653b1ca985a2e0390457feecbf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998582"
---
# <a name="round_ni-sm4---asm"></a><span data-ttu-id="5cdeb-104">round \_ ni (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="5cdeb-104">round\_ni (sm4 - asm)</span></span>

<span data-ttu-id="5cdeb-105">Punto flotante redondeado a float entero.</span><span class="sxs-lookup"><span data-stu-id="5cdeb-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="5cdeb-106">round \_ ni \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swzzle\]</span><span class="sxs-lookup"><span data-stu-id="5cdeb-106">round\_ni\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="5cdeb-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="5cdeb-107">Item</span></span>                                                            | <span data-ttu-id="5cdeb-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cdeb-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="5cdeb-109"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="5cdeb-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5cdeb-110">\[en \] La dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="5cdeb-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="5cdeb-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5cdeb-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5cdeb-112">\[en \] Los componentes de la operación.</span><span class="sxs-lookup"><span data-stu-id="5cdeb-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="5cdeb-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5cdeb-113">Remarks</span></span>

<span data-ttu-id="5cdeb-114">Esta instrucción realiza una ronda de punto flotante por componente de los valores de *src0,* escribiendo valores enteros de punto flotante *en dest*.</span><span class="sxs-lookup"><span data-stu-id="5cdeb-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span> <span data-ttu-id="5cdeb-115">**round \_ ni** se redondea hacia -infinity, comúnmente conocido como floor().</span><span class="sxs-lookup"><span data-stu-id="5cdeb-115">**round\_ni** rounds toward -infinity, commonly known as floor().</span></span>

<span data-ttu-id="5cdeb-116">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.</span><span class="sxs-lookup"><span data-stu-id="5cdeb-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="5cdeb-117">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="5cdeb-117">F means finite-real number.</span></span>



| <span data-ttu-id="5cdeb-118">**src**</span><span class="sxs-lookup"><span data-stu-id="5cdeb-118">**src**</span></span>  | <span data-ttu-id="5cdeb-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="5cdeb-119">**-inf**</span></span> | <span data-ttu-id="5cdeb-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="5cdeb-120">**-F**</span></span> | <span data-ttu-id="5cdeb-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="5cdeb-121">**-denorm**</span></span> | <span data-ttu-id="5cdeb-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="5cdeb-122">**-0**</span></span> | <span data-ttu-id="5cdeb-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="5cdeb-123">**+0**</span></span> | <span data-ttu-id="5cdeb-124">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="5cdeb-124">**+denorm**</span></span> | <span data-ttu-id="5cdeb-125">**+F**</span><span class="sxs-lookup"><span data-stu-id="5cdeb-125">**+F**</span></span> | <span data-ttu-id="5cdeb-126">**+inf**</span><span class="sxs-lookup"><span data-stu-id="5cdeb-126">**+inf**</span></span> | <span data-ttu-id="5cdeb-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="5cdeb-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="5cdeb-128">**Dest**</span><span class="sxs-lookup"><span data-stu-id="5cdeb-128">**dest**</span></span> | <span data-ttu-id="5cdeb-129">-inf</span><span class="sxs-lookup"><span data-stu-id="5cdeb-129">-inf</span></span>     | <span data-ttu-id="5cdeb-130">-F</span><span class="sxs-lookup"><span data-stu-id="5cdeb-130">-F</span></span>     | <span data-ttu-id="5cdeb-131">-0</span><span class="sxs-lookup"><span data-stu-id="5cdeb-131">-0</span></span>          | <span data-ttu-id="5cdeb-132">-0</span><span class="sxs-lookup"><span data-stu-id="5cdeb-132">-0</span></span>     | <span data-ttu-id="5cdeb-133">+0</span><span class="sxs-lookup"><span data-stu-id="5cdeb-133">+0</span></span>     | <span data-ttu-id="5cdeb-134">+0</span><span class="sxs-lookup"><span data-stu-id="5cdeb-134">+0</span></span>          | <span data-ttu-id="5cdeb-135">+F</span><span class="sxs-lookup"><span data-stu-id="5cdeb-135">+F</span></span>     | <span data-ttu-id="5cdeb-136">+inf</span><span class="sxs-lookup"><span data-stu-id="5cdeb-136">+inf</span></span>     | <span data-ttu-id="5cdeb-137">NaN</span><span class="sxs-lookup"><span data-stu-id="5cdeb-137">NaN</span></span>     |



 

<span data-ttu-id="5cdeb-138">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="5cdeb-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5cdeb-139">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5cdeb-139">Vertex Shader</span></span> | <span data-ttu-id="5cdeb-140">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="5cdeb-140">Geometry Shader</span></span> | <span data-ttu-id="5cdeb-141">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="5cdeb-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5cdeb-142">x</span><span class="sxs-lookup"><span data-stu-id="5cdeb-142">x</span></span>             | <span data-ttu-id="5cdeb-143">x</span><span class="sxs-lookup"><span data-stu-id="5cdeb-143">x</span></span>               | <span data-ttu-id="5cdeb-144">x</span><span class="sxs-lookup"><span data-stu-id="5cdeb-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5cdeb-145">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="5cdeb-145">Minimum Shader Model</span></span>

<span data-ttu-id="5cdeb-146">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="5cdeb-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5cdeb-147">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="5cdeb-147">Shader Model</span></span>                                              | <span data-ttu-id="5cdeb-148">Compatible</span><span class="sxs-lookup"><span data-stu-id="5cdeb-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5cdeb-149">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="5cdeb-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5cdeb-150">sí</span><span class="sxs-lookup"><span data-stu-id="5cdeb-150">yes</span></span>       |
| [<span data-ttu-id="5cdeb-151">Shader Model 4.1</span><span class="sxs-lookup"><span data-stu-id="5cdeb-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5cdeb-152">sí</span><span class="sxs-lookup"><span data-stu-id="5cdeb-152">yes</span></span>       |
| [<span data-ttu-id="5cdeb-153">Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="5cdeb-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5cdeb-154">sí</span><span class="sxs-lookup"><span data-stu-id="5cdeb-154">yes</span></span>       |
| [<span data-ttu-id="5cdeb-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5cdeb-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5cdeb-156">no</span><span class="sxs-lookup"><span data-stu-id="5cdeb-156">no</span></span>        |
| [<span data-ttu-id="5cdeb-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5cdeb-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5cdeb-158">no</span><span class="sxs-lookup"><span data-stu-id="5cdeb-158">no</span></span>        |
| [<span data-ttu-id="5cdeb-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5cdeb-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5cdeb-160">no</span><span class="sxs-lookup"><span data-stu-id="5cdeb-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5cdeb-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5cdeb-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cdeb-162">Ensamblado del modelo 4 del sombreador (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="5cdeb-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





