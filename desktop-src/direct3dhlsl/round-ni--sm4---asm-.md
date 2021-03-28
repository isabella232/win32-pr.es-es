---
title: round_ni (SM4-ASM)
description: Redondeo de punto flotante a Float entero. | round_ni (SM4-ASM)
ms.assetid: 6DEF818B-AFF9-4B44-950E-320EACE1CAC4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3daafd64e76bd8c04acf7812b096f7374befef6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083658"
---
# <a name="round_ni-sm4---asm"></a><span data-ttu-id="f35e3-104">Round \_ ni (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f35e3-104">round\_ni (sm4 - asm)</span></span>

<span data-ttu-id="f35e3-105">Redondeo de punto flotante a Float entero.</span><span class="sxs-lookup"><span data-stu-id="f35e3-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="f35e3-106">Round \_ ni \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f35e3-106">round\_ni\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="f35e3-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f35e3-107">Item</span></span>                                                            | <span data-ttu-id="f35e3-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="f35e3-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f35e3-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f35e3-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f35e3-110">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="f35e3-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="f35e3-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f35e3-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f35e3-112">\[en \] los componentes de la operación.</span><span class="sxs-lookup"><span data-stu-id="f35e3-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="f35e3-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f35e3-113">Remarks</span></span>

<span data-ttu-id="f35e3-114">Esta instrucción realiza un redondeo de punto flotante de modo de componente de los valores de *src0*, escribiendo valores de punto flotante enteros en el *destino*.</span><span class="sxs-lookup"><span data-stu-id="f35e3-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span> <span data-ttu-id="f35e3-115">**Round \_** no redondea hacia el infinito, lo que se conoce comúnmente como Floor ().</span><span class="sxs-lookup"><span data-stu-id="f35e3-115">**round\_ni** rounds toward -infinity, commonly known as floor().</span></span>

<span data-ttu-id="f35e3-116">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.</span><span class="sxs-lookup"><span data-stu-id="f35e3-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="f35e3-117">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="f35e3-117">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="f35e3-118">**src**</span><span class="sxs-lookup"><span data-stu-id="f35e3-118">**src**</span></span>  | <span data-ttu-id="f35e3-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="f35e3-119">**-inf**</span></span> | <span data-ttu-id="f35e3-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="f35e3-120">**-F**</span></span> | <span data-ttu-id="f35e3-121">**-denormalización**</span><span class="sxs-lookup"><span data-stu-id="f35e3-121">**-denorm**</span></span> | <span data-ttu-id="f35e3-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="f35e3-122">**-0**</span></span> | <span data-ttu-id="f35e3-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="f35e3-123">**+0**</span></span> | <span data-ttu-id="f35e3-124">**+ denormalización**</span><span class="sxs-lookup"><span data-stu-id="f35e3-124">**+denorm**</span></span> | <span data-ttu-id="f35e3-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="f35e3-125">**+F**</span></span> | <span data-ttu-id="f35e3-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="f35e3-126">**+inf**</span></span> | <span data-ttu-id="f35e3-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="f35e3-127">**NaN**</span></span> |
| <span data-ttu-id="f35e3-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="f35e3-128">**dest**</span></span> | <span data-ttu-id="f35e3-129">-inf</span><span class="sxs-lookup"><span data-stu-id="f35e3-129">-inf</span></span>     | <span data-ttu-id="f35e3-130">-F</span><span class="sxs-lookup"><span data-stu-id="f35e3-130">-F</span></span>     | <span data-ttu-id="f35e3-131">-0</span><span class="sxs-lookup"><span data-stu-id="f35e3-131">-0</span></span>          | <span data-ttu-id="f35e3-132">-0</span><span class="sxs-lookup"><span data-stu-id="f35e3-132">-0</span></span>     | <span data-ttu-id="f35e3-133">+0</span><span class="sxs-lookup"><span data-stu-id="f35e3-133">+0</span></span>     | <span data-ttu-id="f35e3-134">+0</span><span class="sxs-lookup"><span data-stu-id="f35e3-134">+0</span></span>          | <span data-ttu-id="f35e3-135">+F</span><span class="sxs-lookup"><span data-stu-id="f35e3-135">+F</span></span>     | <span data-ttu-id="f35e3-136">+inf</span><span class="sxs-lookup"><span data-stu-id="f35e3-136">+inf</span></span>     | <span data-ttu-id="f35e3-137">NaN</span><span class="sxs-lookup"><span data-stu-id="f35e3-137">NaN</span></span>     |



 

<span data-ttu-id="f35e3-138">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="f35e3-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f35e3-139">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="f35e3-139">Vertex Shader</span></span> | <span data-ttu-id="f35e3-140">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="f35e3-140">Geometry Shader</span></span> | <span data-ttu-id="f35e3-141">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="f35e3-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f35e3-142">x</span><span class="sxs-lookup"><span data-stu-id="f35e3-142">x</span></span>             | <span data-ttu-id="f35e3-143">x</span><span class="sxs-lookup"><span data-stu-id="f35e3-143">x</span></span>               | <span data-ttu-id="f35e3-144">x</span><span class="sxs-lookup"><span data-stu-id="f35e3-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f35e3-145">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="f35e3-145">Minimum Shader Model</span></span>

<span data-ttu-id="f35e3-146">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f35e3-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f35e3-147">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="f35e3-147">Shader Model</span></span>                                              | <span data-ttu-id="f35e3-148">Compatible</span><span class="sxs-lookup"><span data-stu-id="f35e3-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f35e3-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f35e3-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f35e3-150">sí</span><span class="sxs-lookup"><span data-stu-id="f35e3-150">yes</span></span>       |
| [<span data-ttu-id="f35e3-151">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f35e3-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f35e3-152">sí</span><span class="sxs-lookup"><span data-stu-id="f35e3-152">yes</span></span>       |
| [<span data-ttu-id="f35e3-153">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f35e3-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f35e3-154">sí</span><span class="sxs-lookup"><span data-stu-id="f35e3-154">yes</span></span>       |
| [<span data-ttu-id="f35e3-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f35e3-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f35e3-156">no</span><span class="sxs-lookup"><span data-stu-id="f35e3-156">no</span></span>        |
| [<span data-ttu-id="f35e3-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f35e3-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f35e3-158">no</span><span class="sxs-lookup"><span data-stu-id="f35e3-158">no</span></span>        |
| [<span data-ttu-id="f35e3-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f35e3-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f35e3-160">no</span><span class="sxs-lookup"><span data-stu-id="f35e3-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f35e3-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f35e3-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f35e3-162">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f35e3-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





