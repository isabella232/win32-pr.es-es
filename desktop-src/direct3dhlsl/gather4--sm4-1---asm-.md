---
title: gather4 (SM 4.1-ASM)
description: Recopila las cuatro textura que se utilizarían en una operación de filtrado bilineal y las empaqueta en un solo registro. | gather4 (SM 4.1-ASM)
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84387bfe027e30b338b4701ec941a9d4e1b5e242
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986439"
---
# <a name="gather4-sm41---asm"></a><span data-ttu-id="2fe25-104">gather4 (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="2fe25-104">gather4 (sm4.1 - asm)</span></span>

<span data-ttu-id="2fe25-105">Recopila las cuatro textura que se utilizarían en una operación de filtrado bilineal y las empaqueta en un solo registro.</span><span class="sxs-lookup"><span data-stu-id="2fe25-105">Gathers the four texels that would be used in a bi-linear filtering operation and packs them into a single register.</span></span>



| <span data-ttu-id="2fe25-106">gather4 \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] srcSampler. r</span><span class="sxs-lookup"><span data-stu-id="2fe25-106">gather4\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\] srcSampler.r</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2fe25-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="2fe25-107">Item</span></span>                                                                                                               | <span data-ttu-id="2fe25-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fe25-108">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fe25-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2fe25-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="2fe25-110">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="2fe25-110">\[in\] The address of the result of the operation.</span></span><br/>                                                                                                       |
| <span data-ttu-id="2fe25-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="2fe25-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="2fe25-112">\[en \] contiene las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="2fe25-112">\[in\] Contains the texture coordinates.</span></span> <br/>                                                                                                                |
| <span data-ttu-id="2fe25-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="2fe25-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="2fe25-114">\[en \] un registro de recursos.</span><span class="sxs-lookup"><span data-stu-id="2fe25-114">\[in\] A resource register.</span></span> <br/> <span data-ttu-id="2fe25-115">Swizzle permite que los valores devueltos se swizzled arbitrariamente antes de que se escriban en el *destino*.</span><span class="sxs-lookup"><span data-stu-id="2fe25-115">The swizzle allows the returned values to be swizzled arbitrarily before they are written to *dest*.</span></span> <br/>            |
| <span data-ttu-id="2fe25-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="2fe25-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="2fe25-117">\[en \] un registro de muestra.</span><span class="sxs-lookup"><span data-stu-id="2fe25-117">\[in\] A sampler register.</span></span><br/> <span data-ttu-id="2fe25-118">Este parámetro debe tener un swizzle. r (rojo), que indica que el valor del canal de R se copia en el *destino*.</span><span class="sxs-lookup"><span data-stu-id="2fe25-118">This parameter must have a .r (red) swizzle, which indicates that the value of the R channel is copied to *dest*.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="2fe25-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fe25-119">Remarks</span></span>

<span data-ttu-id="2fe25-120">Esta operación solo funciona con texturas 2D o mapa de canal único.</span><span class="sxs-lookup"><span data-stu-id="2fe25-120">This operation only works with single channel 2D or CubeMap textures.</span></span> <span data-ttu-id="2fe25-121">Para las texturas 2D solo se usan los modos de direccionamiento de la muestra y se usa el nivel superior de cualquier pirámide MIP.</span><span class="sxs-lookup"><span data-stu-id="2fe25-121">For 2D textures only the addressing modes of the sampler are used and the top level of any mip pyramid is used.</span></span>

<span data-ttu-id="2fe25-122">Esta instrucción se comporta como la instrucción de [ejemplo](sample--sm4---asm-.md) , pero no se genera un ejemplo filtrado.</span><span class="sxs-lookup"><span data-stu-id="2fe25-122">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="2fe25-123">Las cuatro muestras que contribuirían al filtrado se colocan en xyzw en el orden en el sentido contrario a las agujas del reloj, empezando por el ejemplo situado en la parte inferior izquierda de la ubicación consultada.</span><span class="sxs-lookup"><span data-stu-id="2fe25-123">The four samples that would contribute to filtering are placed into xyzw in counter clockwise order starting with the sample to the lower left of the queried location.</span></span> <span data-ttu-id="2fe25-124">Esto es lo mismo que el muestreo de puntos con diferencias de coordenadas de textura (u, v) en las siguientes ubicaciones: (-, +), (+, +), (+,-), (-,-), donde la magnitud de los deltas siempre es la mitad de un textura.</span><span class="sxs-lookup"><span data-stu-id="2fe25-124">This is the same as point sampling with (u,v) texture coordinate deltas at the following locations: (-,+),(+,+),(+,-),(-,-), where the magnitude of the deltas are always half a texel.</span></span>

<span data-ttu-id="2fe25-125">En el caso de las texturas de mapa cuando se usa una superficie bilineal, se utiliza un textura de borde de la superficie adyacente.</span><span class="sxs-lookup"><span data-stu-id="2fe25-125">For CubeMap textures when a bi-linear footprint spans an edge texels from the neighboring face are used.</span></span> <span data-ttu-id="2fe25-126">Las esquinas usan las mismas reglas que la instrucción de **ejemplo** ; es decir, la esquina desconocida se considera el promedio de las tres esquinas de la esfera en la que se está haciendo ping.</span><span class="sxs-lookup"><span data-stu-id="2fe25-126">Corners use the same rules as the **sample** instruction; that is the unkown corner is considered the average of the three impinging face corners.</span></span>

<span data-ttu-id="2fe25-127">Las restricciones de formato de textura que se aplican a las instrucciones de **ejemplo** también se aplican a la instrucción **gather4** .</span><span class="sxs-lookup"><span data-stu-id="2fe25-127">The texture format restrictions that apply to the **sample** instructions also apply to the **gather4** instruction.</span></span>

<span data-ttu-id="2fe25-128">En el caso de las implementaciones de hardware, las optimizaciones en el filtrado bilineal tradicional que detectan muestras directamente en textura y omiten la lectura de textura que tendrían el peso 0 no se pueden aprovechar con **gather4**.</span><span class="sxs-lookup"><span data-stu-id="2fe25-128">For hardware implementations, optimizations in traditional bilinear filtering that detect samples directly on texels and skip reading of texels that would have weight 0 cannot be leveraged with **gather4**.</span></span> <span data-ttu-id="2fe25-129">**gather4** siempre devuelve todos los textura solicitados.</span><span class="sxs-lookup"><span data-stu-id="2fe25-129">**gather4** always returns all requested texels.</span></span>

<span data-ttu-id="2fe25-130">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="2fe25-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2fe25-131">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="2fe25-131">Vertex Shader</span></span> | <span data-ttu-id="2fe25-132">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="2fe25-132">Geometry Shader</span></span> | <span data-ttu-id="2fe25-133">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="2fe25-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2fe25-134">x</span><span class="sxs-lookup"><span data-stu-id="2fe25-134">x</span></span>             | <span data-ttu-id="2fe25-135">x</span><span class="sxs-lookup"><span data-stu-id="2fe25-135">x</span></span>               | <span data-ttu-id="2fe25-136">x</span><span class="sxs-lookup"><span data-stu-id="2fe25-136">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2fe25-137">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2fe25-137">Minimum Shader Model</span></span>

<span data-ttu-id="2fe25-138">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2fe25-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2fe25-139">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2fe25-139">Shader Model</span></span>                                              | <span data-ttu-id="2fe25-140">Compatible</span><span class="sxs-lookup"><span data-stu-id="2fe25-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2fe25-141">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2fe25-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2fe25-142">sí</span><span class="sxs-lookup"><span data-stu-id="2fe25-142">yes</span></span>       |
| [<span data-ttu-id="2fe25-143">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2fe25-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2fe25-144">sí</span><span class="sxs-lookup"><span data-stu-id="2fe25-144">yes</span></span>       |
| [<span data-ttu-id="2fe25-145">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2fe25-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2fe25-146">no</span><span class="sxs-lookup"><span data-stu-id="2fe25-146">no</span></span>        |
| [<span data-ttu-id="2fe25-147">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fe25-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2fe25-148">no</span><span class="sxs-lookup"><span data-stu-id="2fe25-148">no</span></span>        |
| [<span data-ttu-id="2fe25-149">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fe25-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2fe25-150">no</span><span class="sxs-lookup"><span data-stu-id="2fe25-150">no</span></span>        |
| [<span data-ttu-id="2fe25-151">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fe25-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2fe25-152">no</span><span class="sxs-lookup"><span data-stu-id="2fe25-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2fe25-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2fe25-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fe25-154">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2fe25-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





