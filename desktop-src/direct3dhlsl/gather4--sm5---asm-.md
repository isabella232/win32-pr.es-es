---
title: gather4 (SM5-ASM)
description: Recopila las cuatro textura que se utilizarían en una operación de filtrado bilineal y las empaqueta en un solo registro. | gather4 (SM5-ASM)
ms.assetid: 5F93BB70-7696-48E4-BCD3-91D5D42FF63E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5657265738f12331afc7596286f02170de2a635
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280012"
---
# <a name="gather4-sm5---asm"></a><span data-ttu-id="a8512-104">gather4 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a8512-104">gather4 (sm5 - asm)</span></span>

<span data-ttu-id="a8512-105">Recopila las cuatro textura que se utilizarían en una operación de filtrado bilineal y las empaqueta en un solo registro.</span><span class="sxs-lookup"><span data-stu-id="a8512-105">Gathers the four texels that would be used in a bi-linear filtering operation and packs them into a single register.</span></span> <span data-ttu-id="a8512-106">Esta instrucción solo funciona con texturas 2D o mapa, incluidas las matrices.</span><span class="sxs-lookup"><span data-stu-id="a8512-106">This instruction only works with 2D or CubeMap textures, including arrays.</span></span> <span data-ttu-id="a8512-107">Solo se usan los modos de direccionamiento de la muestra y se usa el nivel superior de cualquier pirámide de MIP.</span><span class="sxs-lookup"><span data-stu-id="a8512-107">Only the addressing modes of the sampler are used and the top level of any mip pyramid is used.</span></span>



| <span data-ttu-id="a8512-108">gather4 \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . Select ( \_ componente)\]</span><span class="sxs-lookup"><span data-stu-id="a8512-108">gather4\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.select\_component\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a8512-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8512-109">Item</span></span>                                                                                                               | <span data-ttu-id="a8512-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8512-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="a8512-111"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a8512-111"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="a8512-112">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="a8512-112">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="a8512-113"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="a8512-113"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="a8512-114">\[en \] un conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="a8512-114">\[in\] A set of texture coordinates.</span></span><br/>                |
| <span data-ttu-id="a8512-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="a8512-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="a8512-116">\[en \] un registro de textura.</span><span class="sxs-lookup"><span data-stu-id="a8512-116">\[in\] A texture register.</span></span><br/>                          |
| <span data-ttu-id="a8512-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="a8512-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="a8512-118">\[en \] un registro de muestra.</span><span class="sxs-lookup"><span data-stu-id="a8512-118">\[in\] A sampler register.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="a8512-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8512-119">Remarks</span></span>

<span data-ttu-id="a8512-120">Esta instrucción se comporta como la instrucción de [**ejemplo**](sample--sm4---asm-.md) , pero no se genera un ejemplo filtrado.</span><span class="sxs-lookup"><span data-stu-id="a8512-120">This instruction behaves like the [**sample**](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="a8512-121">Las cuatro muestras que contribuirían al filtrado se colocan en xyzw en el orden en el sentido contrario a las agujas del reloj, empezando por el ejemplo situado en la parte inferior izquierda de la ubicación consultada.</span><span class="sxs-lookup"><span data-stu-id="a8512-121">The four samples that would contribute to filtering are placed into xyzw in counter clockwise order starting with the sample to the lower left of the queried location.</span></span> <span data-ttu-id="a8512-122">Esto es lo mismo que el muestreo de puntos con diferencias de coordenadas de textura (u, v) en las siguientes ubicaciones: (-, +), (+, +), (+,-), (-,-), donde la magnitud de los deltas siempre es la mitad de un textura.</span><span class="sxs-lookup"><span data-stu-id="a8512-122">This is the same as point sampling with (u,v) texture coordinate deltas at the following locations: (-,+),(+,+),(+,-),(-,-), where the magnitude of the deltas are always half a texel.</span></span>

<span data-ttu-id="a8512-123">En el caso de las texturas de mapa, cuando una superficie bilineal abarca un borde, se usan textura desde la superficie adyacente.</span><span class="sxs-lookup"><span data-stu-id="a8512-123">For CubeMap textures, when a bi-linear footprint spans an edge, texels from the neighboring face are used.</span></span> <span data-ttu-id="a8512-124">Las esquinas usan las mismas reglas que la instrucción de [**ejemplo**](sample--sm4---asm-.md) ; es decir, la esquina desconocida se considera el promedio de las tres esquinas de la esfera en la que se está haciendo ping.</span><span class="sxs-lookup"><span data-stu-id="a8512-124">Corners use the same rules as the [**sample**](sample--sm4---asm-.md) instruction; that is, the unknown corner is considered the average of the three impinging face corners.</span></span>

<span data-ttu-id="a8512-125">Hay restricciones de formato de textura que se aplican a **gather4** , que se expresan en la lista de formatos.</span><span class="sxs-lookup"><span data-stu-id="a8512-125">There are texture format restrictions that apply to **gather4** which are expressed in the format list.</span></span>

<span data-ttu-id="a8512-126">Swizzle en *srcResource* permite que los valores devueltos se swizzled arbitrariamente antes de que se escriban en el destino.</span><span class="sxs-lookup"><span data-stu-id="a8512-126">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="a8512-127">El componente. Select \_ de *srcSampler* elige qué componente de la textura de origen (r/g/b/a) se leerá 4 textura.</span><span class="sxs-lookup"><span data-stu-id="a8512-127">The .select\_component on *srcSampler* chooses which component of the source texture (r/g/b/a) to read 4 texels from.</span></span>

<span data-ttu-id="a8512-128">En el caso de los formatos con componentes float32, si el valor que se va a capturar es normalizado, desnormalizado, +-0 o +-INF, se devuelve al sombreador sin modificar.</span><span class="sxs-lookup"><span data-stu-id="a8512-128">For formats with float32 components, if the value being fetched is normalized, denormalized, +-0 or +-INF, it is returned to the shader unaltered.</span></span> <span data-ttu-id="a8512-129">NaN se devuelve como NaN, pero se puede cambiar la representación de bits exacta del NaN.</span><span class="sxs-lookup"><span data-stu-id="a8512-129">NaN is returned as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="a8512-130">En el caso de TextureCubes, algunas síntesis de la cuarta textura que faltan deben aparecer en las esquinas, por lo que no se aplican los bits que no han cambiado para la textura sintetizada, y se pueden vaciar las denormalidades.</span><span class="sxs-lookup"><span data-stu-id="a8512-130">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so returning bits unchanged for the synthesized texel does not apply, and denorms could be flushed.</span></span>

<span data-ttu-id="a8512-131">En el caso de las implementaciones de hardware, las optimizaciones en el filtrado bilineal tradicional que detectan los ejemplos directamente en textura y omiten la lectura de textura que tendrían el peso 0 no se pueden aprovechar con esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="a8512-131">For hardware implementations, optimizations in traditional bilinear filtering that detect samples directly on texels and skip reading of texels that would have weight 0 cannot be leveraged with this instruction.</span></span> <span data-ttu-id="a8512-132">*gather4* siempre devuelve todos los textura solicitados.</span><span class="sxs-lookup"><span data-stu-id="a8512-132">*gather4* always returns all requested texels.</span></span>

<span data-ttu-id="a8512-133">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="a8512-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a8512-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="a8512-134">Vertex</span></span> | <span data-ttu-id="a8512-135">Casco</span><span class="sxs-lookup"><span data-stu-id="a8512-135">Hull</span></span> | <span data-ttu-id="a8512-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="a8512-136">Domain</span></span> | <span data-ttu-id="a8512-137">Geometría</span><span class="sxs-lookup"><span data-stu-id="a8512-137">Geometry</span></span> | <span data-ttu-id="a8512-138">Píxel</span><span class="sxs-lookup"><span data-stu-id="a8512-138">Pixel</span></span> | <span data-ttu-id="a8512-139">Compute</span><span class="sxs-lookup"><span data-stu-id="a8512-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a8512-140">X</span><span class="sxs-lookup"><span data-stu-id="a8512-140">X</span></span>      | <span data-ttu-id="a8512-141">X</span><span class="sxs-lookup"><span data-stu-id="a8512-141">X</span></span>    | <span data-ttu-id="a8512-142">X</span><span class="sxs-lookup"><span data-stu-id="a8512-142">X</span></span>      | <span data-ttu-id="a8512-143">X</span><span class="sxs-lookup"><span data-stu-id="a8512-143">X</span></span>        | <span data-ttu-id="a8512-144">X</span><span class="sxs-lookup"><span data-stu-id="a8512-144">X</span></span>     | <span data-ttu-id="a8512-145">X</span><span class="sxs-lookup"><span data-stu-id="a8512-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a8512-146">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a8512-146">Minimum Shader Model</span></span>

<span data-ttu-id="a8512-147">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a8512-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a8512-148">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a8512-148">Shader Model</span></span>                                              | <span data-ttu-id="a8512-149">Compatible</span><span class="sxs-lookup"><span data-stu-id="a8512-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a8512-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a8512-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a8512-151">sí</span><span class="sxs-lookup"><span data-stu-id="a8512-151">yes</span></span>       |
| [<span data-ttu-id="a8512-152">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a8512-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a8512-153">no</span><span class="sxs-lookup"><span data-stu-id="a8512-153">no</span></span>        |
| [<span data-ttu-id="a8512-154">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a8512-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a8512-155">no</span><span class="sxs-lookup"><span data-stu-id="a8512-155">no</span></span>        |
| [<span data-ttu-id="a8512-156">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8512-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a8512-157">no</span><span class="sxs-lookup"><span data-stu-id="a8512-157">no</span></span>        |
| [<span data-ttu-id="a8512-158">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8512-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a8512-159">no</span><span class="sxs-lookup"><span data-stu-id="a8512-159">no</span></span>        |
| [<span data-ttu-id="a8512-160">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8512-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a8512-161">no</span><span class="sxs-lookup"><span data-stu-id="a8512-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a8512-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8512-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8512-163">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8512-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





