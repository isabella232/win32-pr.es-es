---
title: round_pi (sm4 - asm)
description: Punto flotante redondeado a flotante entero. | round_pi (sm4 - asm)
ms.assetid: AA4E4C2E-A4B0-4892-8660-1EF57767F4C4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61282078b3639681eed756e2899d06744f0369e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997112"
---
# <a name="round_pi-sm4---asm"></a><span data-ttu-id="8a06c-104">round \_ pi (sm4 - asm)</span><span class="sxs-lookup"><span data-stu-id="8a06c-104">round\_pi (sm4 - asm)</span></span>

<span data-ttu-id="8a06c-105">Punto flotante redondeado a flotante entero.</span><span class="sxs-lookup"><span data-stu-id="8a06c-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="8a06c-106">round \_ pi \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swzzle\]</span><span class="sxs-lookup"><span data-stu-id="8a06c-106">round\_pi\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="8a06c-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="8a06c-107">Item</span></span>                                                            | <span data-ttu-id="8a06c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a06c-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="8a06c-109"><span id="dest"></span><span id="DEST"></span>*Dest*</span><span class="sxs-lookup"><span data-stu-id="8a06c-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="8a06c-110">\[en \] La dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="8a06c-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="8a06c-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8a06c-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="8a06c-112">\[en \] Los componentes de la operación.</span><span class="sxs-lookup"><span data-stu-id="8a06c-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="8a06c-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8a06c-113">Remarks</span></span>

<span data-ttu-id="8a06c-114">Esta instrucción realiza una ronda de punto flotante por componente de los valores de *src0,* escribiendo valores de punto flotante enteros *en dest*.</span><span class="sxs-lookup"><span data-stu-id="8a06c-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="8a06c-115">**round \_ pi** se redondea hacia +infinito, normalmente conocido como ceil().</span><span class="sxs-lookup"><span data-stu-id="8a06c-115">**round\_pi** rounds towards +infinity, commonly known as ceil().</span></span>

<span data-ttu-id="8a06c-116">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.</span><span class="sxs-lookup"><span data-stu-id="8a06c-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="8a06c-117">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="8a06c-117">F means finite-real number.</span></span>



| <span data-ttu-id="8a06c-118">**src**</span><span class="sxs-lookup"><span data-stu-id="8a06c-118">**src**</span></span>  | <span data-ttu-id="8a06c-119">**-inf**</span><span class="sxs-lookup"><span data-stu-id="8a06c-119">**-inf**</span></span> | <span data-ttu-id="8a06c-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="8a06c-120">**-F**</span></span> | <span data-ttu-id="8a06c-121">**-denorm**</span><span class="sxs-lookup"><span data-stu-id="8a06c-121">**-denorm**</span></span> | <span data-ttu-id="8a06c-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="8a06c-122">**-0**</span></span> | <span data-ttu-id="8a06c-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="8a06c-123">**+0**</span></span> | <span data-ttu-id="8a06c-124">**+denorm**</span><span class="sxs-lookup"><span data-stu-id="8a06c-124">**+denorm**</span></span> | <span data-ttu-id="8a06c-125">**+F**</span><span class="sxs-lookup"><span data-stu-id="8a06c-125">**+F**</span></span> | <span data-ttu-id="8a06c-126">**+inf**</span><span class="sxs-lookup"><span data-stu-id="8a06c-126">**+inf**</span></span> | <span data-ttu-id="8a06c-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="8a06c-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="8a06c-128">**Dest**</span><span class="sxs-lookup"><span data-stu-id="8a06c-128">**dest**</span></span> | <span data-ttu-id="8a06c-129">-inf</span><span class="sxs-lookup"><span data-stu-id="8a06c-129">-inf</span></span>     | <span data-ttu-id="8a06c-130">-F</span><span class="sxs-lookup"><span data-stu-id="8a06c-130">-F</span></span>     | <span data-ttu-id="8a06c-131">-0</span><span class="sxs-lookup"><span data-stu-id="8a06c-131">-0</span></span>          | <span data-ttu-id="8a06c-132">-0</span><span class="sxs-lookup"><span data-stu-id="8a06c-132">-0</span></span>     | <span data-ttu-id="8a06c-133">+0</span><span class="sxs-lookup"><span data-stu-id="8a06c-133">+0</span></span>     | <span data-ttu-id="8a06c-134">+0</span><span class="sxs-lookup"><span data-stu-id="8a06c-134">+0</span></span>          | <span data-ttu-id="8a06c-135">+F</span><span class="sxs-lookup"><span data-stu-id="8a06c-135">+F</span></span>     | <span data-ttu-id="8a06c-136">+inf</span><span class="sxs-lookup"><span data-stu-id="8a06c-136">+inf</span></span>     | <span data-ttu-id="8a06c-137">NaN</span><span class="sxs-lookup"><span data-stu-id="8a06c-137">NaN</span></span>     |



 

<span data-ttu-id="8a06c-138">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="8a06c-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8a06c-139">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="8a06c-139">Vertex Shader</span></span> | <span data-ttu-id="8a06c-140">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="8a06c-140">Geometry Shader</span></span> | <span data-ttu-id="8a06c-141">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="8a06c-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8a06c-142">x</span><span class="sxs-lookup"><span data-stu-id="8a06c-142">x</span></span>             | <span data-ttu-id="8a06c-143">x</span><span class="sxs-lookup"><span data-stu-id="8a06c-143">x</span></span>               | <span data-ttu-id="8a06c-144">x</span><span class="sxs-lookup"><span data-stu-id="8a06c-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8a06c-145">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="8a06c-145">Minimum Shader Model</span></span>

<span data-ttu-id="8a06c-146">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8a06c-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8a06c-147">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="8a06c-147">Shader Model</span></span>                                              | <span data-ttu-id="8a06c-148">Compatible</span><span class="sxs-lookup"><span data-stu-id="8a06c-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8a06c-149">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="8a06c-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8a06c-150">sí</span><span class="sxs-lookup"><span data-stu-id="8a06c-150">yes</span></span>       |
| [<span data-ttu-id="8a06c-151">Shader Model 4.1</span><span class="sxs-lookup"><span data-stu-id="8a06c-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8a06c-152">sí</span><span class="sxs-lookup"><span data-stu-id="8a06c-152">yes</span></span>       |
| [<span data-ttu-id="8a06c-153">Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="8a06c-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8a06c-154">sí</span><span class="sxs-lookup"><span data-stu-id="8a06c-154">yes</span></span>       |
| [<span data-ttu-id="8a06c-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a06c-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8a06c-156">no</span><span class="sxs-lookup"><span data-stu-id="8a06c-156">no</span></span>        |
| [<span data-ttu-id="8a06c-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a06c-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8a06c-158">no</span><span class="sxs-lookup"><span data-stu-id="8a06c-158">no</span></span>        |
| [<span data-ttu-id="8a06c-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a06c-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8a06c-160">no</span><span class="sxs-lookup"><span data-stu-id="8a06c-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8a06c-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a06c-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a06c-162">Ensamblado del modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8a06c-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





