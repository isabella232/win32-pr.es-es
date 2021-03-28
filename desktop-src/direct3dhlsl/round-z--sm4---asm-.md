---
title: round_z (SM4-ASM)
description: Redondeo de punto flotante a Float entero. | round_z (SM4-ASM)
ms.assetid: 97C0E0F2-2571-4A94-BB04-B0CDBA0B5C0C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ed79a60bf122163b49411a3b3197ccdacba1311
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914341"
---
# <a name="round_z-sm4---asm"></a><span data-ttu-id="ff688-104">Round \_ z (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ff688-104">round\_z (sm4 - asm)</span></span>

<span data-ttu-id="ff688-105">Redondeo de punto flotante a Float entero.</span><span class="sxs-lookup"><span data-stu-id="ff688-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="ff688-106">Round \_ z \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ff688-106">round\_z\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------|



 



| <span data-ttu-id="ff688-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="ff688-107">Item</span></span>                                                            | <span data-ttu-id="ff688-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff688-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="ff688-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ff688-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ff688-110">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="ff688-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="ff688-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ff688-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ff688-112">\[en \] los componentes de la operación.</span><span class="sxs-lookup"><span data-stu-id="ff688-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="ff688-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff688-113">Remarks</span></span>

<span data-ttu-id="ff688-114">Esta instrucción realiza un redondeo de punto flotante de modo de componente de los valores de *src0*, escribiendo valores de punto flotante enteros en el *destino*.</span><span class="sxs-lookup"><span data-stu-id="ff688-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="ff688-115">**Round \_ z** redondea hacia cero.</span><span class="sxs-lookup"><span data-stu-id="ff688-115">**round\_z** rounds towards zero.</span></span>

<span data-ttu-id="ff688-116">En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.</span><span class="sxs-lookup"><span data-stu-id="ff688-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="ff688-117">**src**</span><span class="sxs-lookup"><span data-stu-id="ff688-117">**src**</span></span>  | <span data-ttu-id="ff688-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="ff688-118">**-inf**</span></span> | <span data-ttu-id="ff688-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="ff688-119">**-F**</span></span> | <span data-ttu-id="ff688-120">**-denormalización**</span><span class="sxs-lookup"><span data-stu-id="ff688-120">**-denorm**</span></span> | <span data-ttu-id="ff688-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="ff688-121">**-0**</span></span> | <span data-ttu-id="ff688-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="ff688-122">**+0**</span></span> | <span data-ttu-id="ff688-123">**+ denormalización**</span><span class="sxs-lookup"><span data-stu-id="ff688-123">**+denorm**</span></span> | <span data-ttu-id="ff688-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="ff688-124">**+F**</span></span> | <span data-ttu-id="ff688-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="ff688-125">**+inf**</span></span> | <span data-ttu-id="ff688-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="ff688-126">**NaN**</span></span> |
| <span data-ttu-id="ff688-127">**dest**</span><span class="sxs-lookup"><span data-stu-id="ff688-127">**dest**</span></span> | <span data-ttu-id="ff688-128">-inf</span><span class="sxs-lookup"><span data-stu-id="ff688-128">-inf</span></span>     | <span data-ttu-id="ff688-129">-F</span><span class="sxs-lookup"><span data-stu-id="ff688-129">-F</span></span>     | <span data-ttu-id="ff688-130">-0</span><span class="sxs-lookup"><span data-stu-id="ff688-130">-0</span></span>          | <span data-ttu-id="ff688-131">-0</span><span class="sxs-lookup"><span data-stu-id="ff688-131">-0</span></span>     | <span data-ttu-id="ff688-132">+0</span><span class="sxs-lookup"><span data-stu-id="ff688-132">+0</span></span>     | <span data-ttu-id="ff688-133">+0</span><span class="sxs-lookup"><span data-stu-id="ff688-133">+0</span></span>          | <span data-ttu-id="ff688-134">+F</span><span class="sxs-lookup"><span data-stu-id="ff688-134">+F</span></span>     | <span data-ttu-id="ff688-135">+inf</span><span class="sxs-lookup"><span data-stu-id="ff688-135">+inf</span></span>     | <span data-ttu-id="ff688-136">NaN</span><span class="sxs-lookup"><span data-stu-id="ff688-136">NaN</span></span>     |



 

<span data-ttu-id="ff688-137">F significa número finito-real.</span><span class="sxs-lookup"><span data-stu-id="ff688-137">F means finite-real number.</span></span>

<span data-ttu-id="ff688-138">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="ff688-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ff688-139">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="ff688-139">Vertex Shader</span></span> | <span data-ttu-id="ff688-140">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="ff688-140">Geometry Shader</span></span> | <span data-ttu-id="ff688-141">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ff688-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ff688-142">x</span><span class="sxs-lookup"><span data-stu-id="ff688-142">x</span></span>             | <span data-ttu-id="ff688-143">x</span><span class="sxs-lookup"><span data-stu-id="ff688-143">x</span></span>               | <span data-ttu-id="ff688-144">x</span><span class="sxs-lookup"><span data-stu-id="ff688-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ff688-145">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="ff688-145">Minimum Shader Model</span></span>

<span data-ttu-id="ff688-146">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ff688-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ff688-147">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ff688-147">Shader Model</span></span>                                              | <span data-ttu-id="ff688-148">Compatible</span><span class="sxs-lookup"><span data-stu-id="ff688-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ff688-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ff688-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ff688-150">sí</span><span class="sxs-lookup"><span data-stu-id="ff688-150">yes</span></span>       |
| [<span data-ttu-id="ff688-151">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ff688-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ff688-152">sí</span><span class="sxs-lookup"><span data-stu-id="ff688-152">yes</span></span>       |
| [<span data-ttu-id="ff688-153">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ff688-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ff688-154">sí</span><span class="sxs-lookup"><span data-stu-id="ff688-154">yes</span></span>       |
| [<span data-ttu-id="ff688-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff688-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ff688-156">no</span><span class="sxs-lookup"><span data-stu-id="ff688-156">no</span></span>        |
| [<span data-ttu-id="ff688-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff688-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ff688-158">no</span><span class="sxs-lookup"><span data-stu-id="ff688-158">no</span></span>        |
| [<span data-ttu-id="ff688-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff688-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ff688-160">no</span><span class="sxs-lookup"><span data-stu-id="ff688-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ff688-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff688-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff688-162">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff688-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





