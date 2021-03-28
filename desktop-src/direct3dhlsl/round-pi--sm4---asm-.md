---
title: round_pi (SM4-ASM)
description: Redondeo de punto flotante a Float entero. | round_pi (SM4-ASM)
ms.assetid: AA4E4C2E-A4B0-4892-8660-1EF57767F4C4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6016cc03f28852c938b1be62d3aaca39dae5dcfb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998188"
---
# <a name="round_pi-sm4---asm"></a><span data-ttu-id="07afe-104">Round \_ PI (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="07afe-104">round\_pi (sm4 - asm)</span></span>

<span data-ttu-id="07afe-105">Redondeo de punto flotante a Float entero.</span><span class="sxs-lookup"><span data-stu-id="07afe-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="07afe-106">Round \_ PI \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="07afe-106">round\_pi\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="07afe-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="07afe-107">Item</span></span>                                                            | <span data-ttu-id="07afe-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="07afe-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="07afe-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="07afe-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="07afe-110">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="07afe-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="07afe-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="07afe-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="07afe-112">\[en \] los componentes de la operación.</span><span class="sxs-lookup"><span data-stu-id="07afe-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="07afe-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07afe-113">Remarks</span></span>

<span data-ttu-id="07afe-114">Esta instrucción realiza un redondeo de punto flotante de modo de componente de los valores de *src0*, escribiendo valores de punto flotante enteros en el *destino*.</span><span class="sxs-lookup"><span data-stu-id="07afe-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="07afe-115">**Round \_ PI** redondea hacia + infinito, comúnmente conocido como Ceil (().</span><span class="sxs-lookup"><span data-stu-id="07afe-115">**round\_pi** rounds towards +infinity, commonly known as ceil().</span></span>

<span data-ttu-id="07afe-116">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.</span><span class="sxs-lookup"><span data-stu-id="07afe-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="07afe-117">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="07afe-117">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="07afe-118">**src**</span><span class="sxs-lookup"><span data-stu-id="07afe-118">**src**</span></span>  | <span data-ttu-id="07afe-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="07afe-119">**-inf**</span></span> | <span data-ttu-id="07afe-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="07afe-120">**-F**</span></span> | <span data-ttu-id="07afe-121">**-denormalización**</span><span class="sxs-lookup"><span data-stu-id="07afe-121">**-denorm**</span></span> | <span data-ttu-id="07afe-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="07afe-122">**-0**</span></span> | <span data-ttu-id="07afe-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="07afe-123">**+0**</span></span> | <span data-ttu-id="07afe-124">**+ denormalización**</span><span class="sxs-lookup"><span data-stu-id="07afe-124">**+denorm**</span></span> | <span data-ttu-id="07afe-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="07afe-125">**+F**</span></span> | <span data-ttu-id="07afe-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="07afe-126">**+inf**</span></span> | <span data-ttu-id="07afe-127">**NaN**</span><span class="sxs-lookup"><span data-stu-id="07afe-127">**NaN**</span></span> |
| <span data-ttu-id="07afe-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="07afe-128">**dest**</span></span> | <span data-ttu-id="07afe-129">-inf</span><span class="sxs-lookup"><span data-stu-id="07afe-129">-inf</span></span>     | <span data-ttu-id="07afe-130">-F</span><span class="sxs-lookup"><span data-stu-id="07afe-130">-F</span></span>     | <span data-ttu-id="07afe-131">-0</span><span class="sxs-lookup"><span data-stu-id="07afe-131">-0</span></span>          | <span data-ttu-id="07afe-132">-0</span><span class="sxs-lookup"><span data-stu-id="07afe-132">-0</span></span>     | <span data-ttu-id="07afe-133">+0</span><span class="sxs-lookup"><span data-stu-id="07afe-133">+0</span></span>     | <span data-ttu-id="07afe-134">+0</span><span class="sxs-lookup"><span data-stu-id="07afe-134">+0</span></span>          | <span data-ttu-id="07afe-135">+F</span><span class="sxs-lookup"><span data-stu-id="07afe-135">+F</span></span>     | <span data-ttu-id="07afe-136">+inf</span><span class="sxs-lookup"><span data-stu-id="07afe-136">+inf</span></span>     | <span data-ttu-id="07afe-137">NaN</span><span class="sxs-lookup"><span data-stu-id="07afe-137">NaN</span></span>     |



 

<span data-ttu-id="07afe-138">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="07afe-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="07afe-139">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="07afe-139">Vertex Shader</span></span> | <span data-ttu-id="07afe-140">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="07afe-140">Geometry Shader</span></span> | <span data-ttu-id="07afe-141">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="07afe-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="07afe-142">x</span><span class="sxs-lookup"><span data-stu-id="07afe-142">x</span></span>             | <span data-ttu-id="07afe-143">x</span><span class="sxs-lookup"><span data-stu-id="07afe-143">x</span></span>               | <span data-ttu-id="07afe-144">x</span><span class="sxs-lookup"><span data-stu-id="07afe-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="07afe-145">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="07afe-145">Minimum Shader Model</span></span>

<span data-ttu-id="07afe-146">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="07afe-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="07afe-147">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="07afe-147">Shader Model</span></span>                                              | <span data-ttu-id="07afe-148">Compatible</span><span class="sxs-lookup"><span data-stu-id="07afe-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="07afe-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="07afe-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="07afe-150">sí</span><span class="sxs-lookup"><span data-stu-id="07afe-150">yes</span></span>       |
| [<span data-ttu-id="07afe-151">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="07afe-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="07afe-152">sí</span><span class="sxs-lookup"><span data-stu-id="07afe-152">yes</span></span>       |
| [<span data-ttu-id="07afe-153">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="07afe-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="07afe-154">sí</span><span class="sxs-lookup"><span data-stu-id="07afe-154">yes</span></span>       |
| [<span data-ttu-id="07afe-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07afe-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="07afe-156">no</span><span class="sxs-lookup"><span data-stu-id="07afe-156">no</span></span>        |
| [<span data-ttu-id="07afe-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07afe-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="07afe-158">no</span><span class="sxs-lookup"><span data-stu-id="07afe-158">no</span></span>        |
| [<span data-ttu-id="07afe-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07afe-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="07afe-160">no</span><span class="sxs-lookup"><span data-stu-id="07afe-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="07afe-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07afe-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07afe-162">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="07afe-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





