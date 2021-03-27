---
title: Formato BC6H
description: El formato BC6H es un formato de compresión de textura diseñado para admitir los espacios de colores de intervalos dinámicos (HDR) en los datos de origen.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed4b934df742a4d2c99e20b52b7172b64e598dc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078109"
---
# <a name="bc6h-format"></a><span data-ttu-id="5af66-105">Formato BC6H</span><span class="sxs-lookup"><span data-stu-id="5af66-105">BC6H Format</span></span>

<span data-ttu-id="5af66-106">El formato BC6H es un formato de compresión de textura diseñado para admitir los espacios de colores de intervalos dinámicos (HDR) en los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="5af66-106">The BC6H format is a texture compression format designed to support high-dynamic range (HDR) color spaces in source data.</span></span>

-   [<span data-ttu-id="5af66-107">Acerca del formato BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="5af66-107">About BC6H/DXGI\_FORMAT\_BC6H</span></span>](/windows)
-   [<span data-ttu-id="5af66-108">Implementación de BC6H</span><span class="sxs-lookup"><span data-stu-id="5af66-108">BC6H Implementation</span></span>](#bc6h-implementation)
-   [<span data-ttu-id="5af66-109">Descodificar el formato BC6H</span><span class="sxs-lookup"><span data-stu-id="5af66-109">Decoding the BC6H Format</span></span>](#decoding-the-bc6h-format)
-   [<span data-ttu-id="5af66-110">Formato de punto de conexión comprimido BC6H</span><span class="sxs-lookup"><span data-stu-id="5af66-110">BC6H Compressed Endpoint Format</span></span>](#bc6h-compressed-endpoint-format)
-   [<span data-ttu-id="5af66-111">Extensión de signo para los valores de punto de conexión</span><span class="sxs-lookup"><span data-stu-id="5af66-111">Sign Extension for Endpoint Values</span></span>](#sign-extension-for-endpoint-values)
-   [<span data-ttu-id="5af66-112">Transformación de la inversión para los valores de punto de conexión</span><span class="sxs-lookup"><span data-stu-id="5af66-112">Transform Inversion for Endpoint Values</span></span>](#transform-inversion-for-endpoint-values)
-   [<span data-ttu-id="5af66-113">Descuantificación de los extremos de color</span><span class="sxs-lookup"><span data-stu-id="5af66-113">Unquantization of Color Endpoints</span></span>](#unquantization-of-color-endpoints)
-   [<span data-ttu-id="5af66-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5af66-114">Related topics</span></span>](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a><span data-ttu-id="5af66-115">Acerca del formato BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="5af66-115">About BC6H/DXGI\_FORMAT\_BC6H</span></span>

<span data-ttu-id="5af66-116">El formato BC6H proporciona compresión de alta calidad para las imágenes que usan tres canales de color HDR, con un valor de 16 bits para cada canal de color del valor (16:16:16).</span><span class="sxs-lookup"><span data-stu-id="5af66-116">The BC6H format provides high-quality compression for images that use three HDR color channels, with a 16-bit value for each color channel of the value (16:16:16).</span></span> <span data-ttu-id="5af66-117">No se admiten canales alfa.</span><span class="sxs-lookup"><span data-stu-id="5af66-117">There is no support for an alpha channel.</span></span>

<span data-ttu-id="5af66-118">BC6H se especifica mediante los siguientes \_ valores de enumeración de formato de DXGI:</span><span class="sxs-lookup"><span data-stu-id="5af66-118">BC6H is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="5af66-119">**DXGI \_ DAR formato a \_ BC6H \_ sin tipo**.</span><span class="sxs-lookup"><span data-stu-id="5af66-119">**DXGI\_FORMAT\_BC6H\_TYPELESS**.</span></span>
-   <span data-ttu-id="5af66-120">**DXGI \_ DAR formato a \_ BC6H \_ UF16**.</span><span class="sxs-lookup"><span data-stu-id="5af66-120">**DXGI\_FORMAT\_BC6H\_UF16**.</span></span> <span data-ttu-id="5af66-121">Este formato BC6H no usa un bit de signo en los valores de canal de color de punto flotante de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5af66-121">This BC6H format does not use a sign bit in the 16-bit floating point color channel values.</span></span>
-   <span data-ttu-id="5af66-122">**DXGI \_ DAR formato a \_ BC6H \_ SF16**. Este formato BC6H usa un bit de signo en los valores de canal de color de punto flotante de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5af66-122">**DXGI\_FORMAT\_BC6H\_SF16**.This BC6H format uses a sign bit in the 16-bit floating point color channel values.</span></span>

> [!Note]  
> <span data-ttu-id="5af66-123">El formato de punto flotante de 16 bits para los canales de color a menudo se conoce como formato de punto flotante "medio".</span><span class="sxs-lookup"><span data-stu-id="5af66-123">The 16 bit floating point format for color channels is often referred to as a "half" floating point format.</span></span> <span data-ttu-id="5af66-124">Este formato tiene el siguiente diseño de bits:</span><span class="sxs-lookup"><span data-stu-id="5af66-124">This format has the following bit layout:</span></span>
>
> |                       |                                                 |
> |-----------------------|-------------------------------------------------|
> | <span data-ttu-id="5af66-125">UF16 (unsigned float)</span><span class="sxs-lookup"><span data-stu-id="5af66-125">UF16 (unsigned float)</span></span> | <span data-ttu-id="5af66-126">5 bits de exponente + 11 bits de mantisa</span><span class="sxs-lookup"><span data-stu-id="5af66-126">5 exponent bits + 11 mantissa bits</span></span>              |
> | <span data-ttu-id="5af66-127">SF16 (valor Float con signo)</span><span class="sxs-lookup"><span data-stu-id="5af66-127">SF16 (signed float)</span></span>   | <span data-ttu-id="5af66-128">1 bit de signo + 5 bits de exponente + 10 bits de mantisa</span><span class="sxs-lookup"><span data-stu-id="5af66-128">1 sign bit + 5 exponent bits + 10 mantissa bits</span></span> |
>
> 
>
>  

 

<span data-ttu-id="5af66-129">El formato BC6H se puede usar para los recursos de textura [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluidas las matrices), Texture3D o TextureCube (incluidas las matrices).</span><span class="sxs-lookup"><span data-stu-id="5af66-129">The BC6H format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="5af66-130">Del mismo modo, este formato se aplica a las superficies de mapa MIP asociadas a estos recursos.</span><span class="sxs-lookup"><span data-stu-id="5af66-130">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="5af66-131">BC6H usa un tamaño de bloque fijo de 16 bytes (128 bits) y un tamaño de mosaico fijo de textura 4x4.</span><span class="sxs-lookup"><span data-stu-id="5af66-131">BC6H uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="5af66-132">Al igual que con los formatos BC anteriores, las imágenes de textura mayores que el tamaño de mosaico compatible (4x4) se comprimen mediante varios bloques.</span><span class="sxs-lookup"><span data-stu-id="5af66-132">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="5af66-133">Esta identidad de direccionamiento se aplica también a imágenes tridimensionales, mapas MIP, cubemaps y matrices de texturas.</span><span class="sxs-lookup"><span data-stu-id="5af66-133">This addressing identity applies also to three-dimensional images, MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="5af66-134">Todos los mosaicos de imagen deben tener el mismo formato.</span><span class="sxs-lookup"><span data-stu-id="5af66-134">All image tiles must be of the same format.</span></span>

<span data-ttu-id="5af66-135">Algunas notas importantes sobre el formato BC6H:</span><span class="sxs-lookup"><span data-stu-id="5af66-135">Some important notes about the BC6H format:</span></span>

-   <span data-ttu-id="5af66-136">BC6H admite la desnormalización de punto flotante, pero no admite INF (infinito) y NaN (no un número).</span><span class="sxs-lookup"><span data-stu-id="5af66-136">BC6H supports floating point denormalization, but does not support INF (infinity) and NaN (not a number).</span></span> <span data-ttu-id="5af66-137">La excepción es el modo con signo de BC6H (DXGI \_ format \_ BC6H \_ SF16), que admite-INF (infinito negativo).</span><span class="sxs-lookup"><span data-stu-id="5af66-137">The exception is the signed mode of BC6H (DXGI\_FORMAT\_BC6H\_SF16), which supports -INF (negative infinity).</span></span> <span data-ttu-id="5af66-138">Tenga en cuenta que esta compatibilidad con-INF es simplemente un artefacto del mismo formato y no es compatible específicamente con los codificadores para este formato.</span><span class="sxs-lookup"><span data-stu-id="5af66-138">Note that this support for -INF is merely an artifact of the format itself, and is not specifically supported by encoders for this format.</span></span> <span data-ttu-id="5af66-139">En general, cuando los codificadores encuentran datos de entrada INF (positivos o negativos) o NaN, deben \\ convertir los datos en el valor de representación de no INF máximo permitido y asignar Nan a 0 antes de la compresión.</span><span class="sxs-lookup"><span data-stu-id="5af66-139">In general, when encoders encounter INF (positive or negative) or NaN input data, they should \\ convert that data to the maximum allowable non-INF representation value, and map NaN to 0 prior to compression.</span></span>
-   <span data-ttu-id="5af66-140">BC6H no es compatible con un canal alfa.</span><span class="sxs-lookup"><span data-stu-id="5af66-140">BC6H does not support an alpha channel.</span></span>
-   <span data-ttu-id="5af66-141">El descodificador de BC6H realiza la descompresión antes de realizar el filtrado de textura.</span><span class="sxs-lookup"><span data-stu-id="5af66-141">The BC6H decoder performs decompression before it performs texture filtering.</span></span>
-   <span data-ttu-id="5af66-142">La descompresión de BC6H debe ser precisa de bits; es decir, el hardware debe devolver resultados idénticos al descodificador descrito en esta documentación.</span><span class="sxs-lookup"><span data-stu-id="5af66-142">BC6H decompression must be bit accurate; that is, the hardware must return results that are identical to the decoder described in this documentation.</span></span>

## <a name="bc6h-implementation"></a><span data-ttu-id="5af66-143">Implementación de BC6H</span><span class="sxs-lookup"><span data-stu-id="5af66-143">BC6H Implementation</span></span>

<span data-ttu-id="5af66-144">Un bloque BC6H consta de bits de modo, puntos de conexión comprimidos, índices comprimidos y un índice de partición opcional.</span><span class="sxs-lookup"><span data-stu-id="5af66-144">A BC6H block consists of mode bits, compressed endpoints, compressed indices, and an optional partition index.</span></span> <span data-ttu-id="5af66-145">Este formato especifica 14 modos diferentes.</span><span class="sxs-lookup"><span data-stu-id="5af66-145">This format specifies 14 different modes.</span></span>

<span data-ttu-id="5af66-146">Un color de punto de conexión se almacena como un tripledo RGB.</span><span class="sxs-lookup"><span data-stu-id="5af66-146">An endpoint color is stored as an RGB triplet.</span></span> <span data-ttu-id="5af66-147">BC6H define una paleta de colores en una línea aproximada en varios extremos de color definidos.</span><span class="sxs-lookup"><span data-stu-id="5af66-147">BC6H defines a palette of colors on an approximate line across a number of defined color endpoints.</span></span> <span data-ttu-id="5af66-148">Además, en función del modo, un icono se puede dividir en dos regiones o tratarse como una sola región, en la que un mosaico de dos regiones tiene un conjunto independiente de extremos de color para cada región.</span><span class="sxs-lookup"><span data-stu-id="5af66-148">Also, depending on the mode, a tile can be divided into two regions or treated as a single region, where a two-region tile has a separate set of color endpoints for each region.</span></span> <span data-ttu-id="5af66-149">BC6H almacena un índice de paleta por textura.</span><span class="sxs-lookup"><span data-stu-id="5af66-149">BC6H stores one palette index per texel.</span></span>

<span data-ttu-id="5af66-150">En el caso de dos regiones, hay 32 particiones posibles.</span><span class="sxs-lookup"><span data-stu-id="5af66-150">In the two-region case, there are 32 possible partitions.</span></span>

## <a name="decoding-the-bc6h-format"></a><span data-ttu-id="5af66-151">Descodificar el formato BC6H</span><span class="sxs-lookup"><span data-stu-id="5af66-151">Decoding the BC6H Format</span></span>

<span data-ttu-id="5af66-152">En el siguiente pseudocódigo se muestran los pasos para descomprimir el píxel en (x, y) dado el bloque BC6H de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="5af66-152">The pseudocode below shows the steps to decompress the pixel at (x,y) given the 16 byte BC6H block.</span></span>

``` syntax
decompress_bc6h(x, y, block)
{
    mode = extract_mode(block);
    endpoints;
    index;
    
    if(mode.type == ONE)
    {
        endpoints = extract_compressed_endpoints(mode, block);
        index = extract_index_ONE(x, y, block);
    }
    else //mode.type == TWO
    {
        partition = extract_partition(block);
        region = get_region(partition, x, y);
        endpoints = extract_compressed_endpoints(mode, region, block);
        index = extract_index_TWO(x, y, partition, block);
    }
    
    unquantize(endpoints);
    color = interpolate(index, endpoints);
    finish_unquantize(color);
}
```

<span data-ttu-id="5af66-153">La tabla siguiente contiene el recuento de bits y los valores para cada uno de los 14 formatos posibles para los bloques BC6H.</span><span class="sxs-lookup"><span data-stu-id="5af66-153">The following table contains the bit count and values for each of the 14 possible formats for BC6H blocks.</span></span> 

| <span data-ttu-id="5af66-154">Mode</span><span class="sxs-lookup"><span data-stu-id="5af66-154">Mode</span></span> | <span data-ttu-id="5af66-155">Índices de partición</span><span class="sxs-lookup"><span data-stu-id="5af66-155">Partition Indices</span></span> | <span data-ttu-id="5af66-156">Partición</span><span class="sxs-lookup"><span data-stu-id="5af66-156">Partition</span></span> | <span data-ttu-id="5af66-157">Extremos de color</span><span class="sxs-lookup"><span data-stu-id="5af66-157">Color Endpoints</span></span>                  | <span data-ttu-id="5af66-158">Bits de modo</span><span class="sxs-lookup"><span data-stu-id="5af66-158">Mode Bits</span></span>      |
|------|-------------------|-----------|----------------------------------|----------------|
| <span data-ttu-id="5af66-159">1</span><span class="sxs-lookup"><span data-stu-id="5af66-159">1</span></span>    | <span data-ttu-id="5af66-160">46 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-160">46 bits</span></span>           | <span data-ttu-id="5af66-161">5 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-161">5 bits</span></span>    | <span data-ttu-id="5af66-162">75 bits (10,555, 10,555, 10,555)</span><span class="sxs-lookup"><span data-stu-id="5af66-162">75 bits (10.555, 10.555, 10.555)</span></span> | <span data-ttu-id="5af66-163">2 bits (00)</span><span class="sxs-lookup"><span data-stu-id="5af66-163">2 bits (00)</span></span>    |
| <span data-ttu-id="5af66-164">2</span><span class="sxs-lookup"><span data-stu-id="5af66-164">2</span></span>    | <span data-ttu-id="5af66-165">46 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-165">46 bits</span></span>           | <span data-ttu-id="5af66-166">5 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-166">5 bits</span></span>    | <span data-ttu-id="5af66-167">75 bits (7666, 7666, 7666)</span><span class="sxs-lookup"><span data-stu-id="5af66-167">75 bits (7666, 7666, 7666)</span></span>       | <span data-ttu-id="5af66-168">2 bits (01)</span><span class="sxs-lookup"><span data-stu-id="5af66-168">2 bits (01)</span></span>    |
| <span data-ttu-id="5af66-169">3</span><span class="sxs-lookup"><span data-stu-id="5af66-169">3</span></span>    | <span data-ttu-id="5af66-170">46 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-170">46 bits</span></span>           | <span data-ttu-id="5af66-171">5 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-171">5 bits</span></span>    | <span data-ttu-id="5af66-172">72 bits (11,555, 11,444, 11,444)</span><span class="sxs-lookup"><span data-stu-id="5af66-172">72 bits (11.555, 11.444, 11.444)</span></span> | <span data-ttu-id="5af66-173">5 bits (00010)</span><span class="sxs-lookup"><span data-stu-id="5af66-173">5 bits (00010)</span></span> |
| <span data-ttu-id="5af66-174">4</span><span class="sxs-lookup"><span data-stu-id="5af66-174">4</span></span>    | <span data-ttu-id="5af66-175">46 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-175">46 bits</span></span>           | <span data-ttu-id="5af66-176">5 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-176">5 bits</span></span>    | <span data-ttu-id="5af66-177">72 bits (11,444, 11,555, 11,444)</span><span class="sxs-lookup"><span data-stu-id="5af66-177">72 bits (11.444, 11.555, 11.444)</span></span> | <span data-ttu-id="5af66-178">5 bits (00110)</span><span class="sxs-lookup"><span data-stu-id="5af66-178">5 bits (00110)</span></span> |
| <span data-ttu-id="5af66-179">5</span><span class="sxs-lookup"><span data-stu-id="5af66-179">5</span></span>    | <span data-ttu-id="5af66-180">46 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-180">46 bits</span></span>           | <span data-ttu-id="5af66-181">5 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-181">5 bits</span></span>    | <span data-ttu-id="5af66-182">72 bits (11,444, 11,444, 11,555)</span><span class="sxs-lookup"><span data-stu-id="5af66-182">72 bits (11.444, 11.444, 11.555)</span></span> | <span data-ttu-id="5af66-183">5 bits (01010)</span><span class="sxs-lookup"><span data-stu-id="5af66-183">5 bits (01010)</span></span> |
| <span data-ttu-id="5af66-184">6</span><span class="sxs-lookup"><span data-stu-id="5af66-184">6</span></span>    | <span data-ttu-id="5af66-185">46 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-185">46 bits</span></span>           | <span data-ttu-id="5af66-186">5 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-186">5 bits</span></span>    | <span data-ttu-id="5af66-187">72 bits (9555, 9555, 9555)</span><span class="sxs-lookup"><span data-stu-id="5af66-187">72 bits (9555, 9555, 9555)</span></span>       | <span data-ttu-id="5af66-188">5 bits (01110)</span><span class="sxs-lookup"><span data-stu-id="5af66-188">5 bits (01110)</span></span> |
| <span data-ttu-id="5af66-189">7</span><span class="sxs-lookup"><span data-stu-id="5af66-189">7</span></span>    | <span data-ttu-id="5af66-190">46 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-190">46 bits</span></span>           | <span data-ttu-id="5af66-191">5 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-191">5 bits</span></span>    | <span data-ttu-id="5af66-192">72 bits (8666, 8555, 8555)</span><span class="sxs-lookup"><span data-stu-id="5af66-192">72 bits (8666, 8555, 8555)</span></span>       | <span data-ttu-id="5af66-193">5 bits (10010)</span><span class="sxs-lookup"><span data-stu-id="5af66-193">5 bits (10010)</span></span> |
| <span data-ttu-id="5af66-194">8</span><span class="sxs-lookup"><span data-stu-id="5af66-194">8</span></span>    | <span data-ttu-id="5af66-195">46 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-195">46 bits</span></span>           | <span data-ttu-id="5af66-196">5 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-196">5 bits</span></span>    | <span data-ttu-id="5af66-197">72 bits (8555, 8666, 8555)</span><span class="sxs-lookup"><span data-stu-id="5af66-197">72 bits (8555, 8666, 8555)</span></span>       | <span data-ttu-id="5af66-198">5 bits (10110)</span><span class="sxs-lookup"><span data-stu-id="5af66-198">5 bits (10110)</span></span> |
| <span data-ttu-id="5af66-199">9</span><span class="sxs-lookup"><span data-stu-id="5af66-199">9</span></span>    | <span data-ttu-id="5af66-200">46 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-200">46 bits</span></span>           | <span data-ttu-id="5af66-201">5 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-201">5 bits</span></span>    | <span data-ttu-id="5af66-202">72 bits (8555, 8555, 8666)</span><span class="sxs-lookup"><span data-stu-id="5af66-202">72 bits (8555, 8555, 8666)</span></span>       | <span data-ttu-id="5af66-203">5 bits (11010)</span><span class="sxs-lookup"><span data-stu-id="5af66-203">5 bits (11010)</span></span> |
| <span data-ttu-id="5af66-204">10</span><span class="sxs-lookup"><span data-stu-id="5af66-204">10</span></span>   | <span data-ttu-id="5af66-205">46 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-205">46 bits</span></span>           | <span data-ttu-id="5af66-206">5 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-206">5 bits</span></span>    | <span data-ttu-id="5af66-207">72 bits (6666, 6666, 6666)</span><span class="sxs-lookup"><span data-stu-id="5af66-207">72 bits (6666, 6666, 6666)</span></span>       | <span data-ttu-id="5af66-208">5 bits (11110)</span><span class="sxs-lookup"><span data-stu-id="5af66-208">5 bits (11110)</span></span> |
| <span data-ttu-id="5af66-209">11</span><span class="sxs-lookup"><span data-stu-id="5af66-209">11</span></span>   | <span data-ttu-id="5af66-210">63 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-210">63 bits</span></span>           | <span data-ttu-id="5af66-211">0 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-211">0 bits</span></span>    | <span data-ttu-id="5af66-212">60 bits (10,10, 10,10, 10,10)</span><span class="sxs-lookup"><span data-stu-id="5af66-212">60 bits (10.10, 10.10, 10.10)</span></span>    | <span data-ttu-id="5af66-213">5 bits (00011)</span><span class="sxs-lookup"><span data-stu-id="5af66-213">5 bits (00011)</span></span> |
| <span data-ttu-id="5af66-214">12</span><span class="sxs-lookup"><span data-stu-id="5af66-214">12</span></span>   | <span data-ttu-id="5af66-215">63 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-215">63 bits</span></span>           | <span data-ttu-id="5af66-216">0 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-216">0 bits</span></span>    | <span data-ttu-id="5af66-217">60 bits (11,9, 11,9, 11,9)</span><span class="sxs-lookup"><span data-stu-id="5af66-217">60 bits (11.9, 11.9, 11.9)</span></span>       | <span data-ttu-id="5af66-218">5 bits (00111)</span><span class="sxs-lookup"><span data-stu-id="5af66-218">5 bits (00111)</span></span> |
| <span data-ttu-id="5af66-219">13</span><span class="sxs-lookup"><span data-stu-id="5af66-219">13</span></span>   | <span data-ttu-id="5af66-220">63 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-220">63 bits</span></span>           | <span data-ttu-id="5af66-221">0 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-221">0 bits</span></span>    | <span data-ttu-id="5af66-222">60 bits (12,8, 12,8, 12,8)</span><span class="sxs-lookup"><span data-stu-id="5af66-222">60 bits (12.8, 12.8, 12.8)</span></span>       | <span data-ttu-id="5af66-223">5 bits (01011)</span><span class="sxs-lookup"><span data-stu-id="5af66-223">5 bits (01011)</span></span> |
| <span data-ttu-id="5af66-224">14</span><span class="sxs-lookup"><span data-stu-id="5af66-224">14</span></span>   | <span data-ttu-id="5af66-225">63 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-225">63 bits</span></span>           | <span data-ttu-id="5af66-226">0 bits</span><span class="sxs-lookup"><span data-stu-id="5af66-226">0 bits</span></span>    | <span data-ttu-id="5af66-227">60 bits (16,4, 16,4, 16,4)</span><span class="sxs-lookup"><span data-stu-id="5af66-227">60 bits (16.4, 16.4, 16.4)</span></span>       | <span data-ttu-id="5af66-228">5 bits (01111)</span><span class="sxs-lookup"><span data-stu-id="5af66-228">5 bits (01111)</span></span> |



 

<span data-ttu-id="5af66-229">Los bits de modo pueden identificar de forma única cada formato de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="5af66-229">Each format in this table can be uniquely identified by the mode bits.</span></span> <span data-ttu-id="5af66-230">Los primeros diez modos se usan para los mosaicos de dos regiones y el campo de bits de modo puede tener dos o cinco bits de longitud.</span><span class="sxs-lookup"><span data-stu-id="5af66-230">The first ten modes are used for two-region tiles, and the mode bit field can be either two or five bits long.</span></span> <span data-ttu-id="5af66-231">Estos bloques también tienen campos para los puntos de conexión de color comprimidos (bits 72 o 75), la partición (5 bits) y los índices de partición (46 bits).</span><span class="sxs-lookup"><span data-stu-id="5af66-231">These blocks also have fields for the compressed color endpoints (72 or 75 bits), the partition (5 bits), and the partition indices (46 bits).</span></span>

<span data-ttu-id="5af66-232">En el caso de los extremos de color comprimido, los valores de la tabla anterior tienen en cuenta la precisión de los puntos de conexión RGB almacenados y el número de bits usados para cada valor de color.</span><span class="sxs-lookup"><span data-stu-id="5af66-232">For the compressed color endpoints, the values in the preceding table note the precision of the stored RGB endpoints, and the number of bits used for each color value.</span></span> <span data-ttu-id="5af66-233">Por ejemplo, el modo 3 especifica un nivel de precisión de punto de conexión de color de 11, y el número de bits que se usa para almacenar los valores Delta de los puntos de conexión transformados para los colores rojo, azul y verde (5, 4 y 4, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="5af66-233">For example, mode 3 specifies a color endpoint precision level of 11, and the number of bits used to store the delta values of the transformed endpoints for the red, blue and green colors (5, 4, and 4 respectively).</span></span> <span data-ttu-id="5af66-234">El modo 10 no utiliza la compresión Delta y, en su lugar, almacena explícitamente los cuatro extremos de color.</span><span class="sxs-lookup"><span data-stu-id="5af66-234">Mode 10 does not use delta compression, and instead stores all four color endpoints explicitly.</span></span>

<span data-ttu-id="5af66-235">Los cuatro últimos modos de bloqueo se usan para los mosaicos de una región, donde el campo de modo es 5 bits.</span><span class="sxs-lookup"><span data-stu-id="5af66-235">The last four block modes are used for one-region tiles, where the mode field is 5 bits.</span></span> <span data-ttu-id="5af66-236">Estos bloques tienen campos para los puntos de conexión (60 bits) y los índices comprimidos (63 bits).</span><span class="sxs-lookup"><span data-stu-id="5af66-236">These blocks have fields for the endpoints (60 bits) and the compressed indices (63 bits).</span></span> <span data-ttu-id="5af66-237">El modo 11 (como el modo 10) no utiliza la compresión Delta y, en su lugar, almacena explícitamente ambos extremos de color.</span><span class="sxs-lookup"><span data-stu-id="5af66-237">Mode 11 (like Mode 10) does not use delta compression, and instead stores both color endpoints explicitly.</span></span>

<span data-ttu-id="5af66-238">Los modos 10011, 10111, 11011 y 11111 (no mostrados) están reservados.</span><span class="sxs-lookup"><span data-stu-id="5af66-238">Modes 10011, 10111, 11011, and 11111 (not shown) are reserved.</span></span> <span data-ttu-id="5af66-239">No los use en el codificador.</span><span class="sxs-lookup"><span data-stu-id="5af66-239">Do not use these in your encoder.</span></span> <span data-ttu-id="5af66-240">Si el hardware pasa bloques con uno de estos modos especificados, el bloque descomprimido resultante debe contener todos los ceros en todos los canales excepto el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="5af66-240">If the hardware is passed blocks with one of these modes specified, the resulting decompressed block must contain all zeroes in all channels except for the alpha channel.</span></span>

<span data-ttu-id="5af66-241">En el caso de BC6H, el canal alfa siempre debe devolver 1,0 independientemente del modo.</span><span class="sxs-lookup"><span data-stu-id="5af66-241">For BC6H, the alpha channel must always return 1.0 regardless of the mode.</span></span>

### <a name="bc6h-partition-set"></a><span data-ttu-id="5af66-242">Conjunto de particiones BC6H</span><span class="sxs-lookup"><span data-stu-id="5af66-242">BC6H Partition Set</span></span>

<span data-ttu-id="5af66-243">Hay 32 posibles conjuntos de particiones para un mosaico de dos regiones y que se definen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5af66-243">There are 32 possible partition sets for a two-region tile, and which are defined in the table below.</span></span> <span data-ttu-id="5af66-244">Cada bloque 4x4 representa una sola forma.</span><span class="sxs-lookup"><span data-stu-id="5af66-244">Each 4x4 block represents a single shape.</span></span>

![tabla de conjuntos de particiones de bc6h](images/bc6h-partition-sets.png)

<span data-ttu-id="5af66-246">En esta tabla de conjuntos de particiones, la entrada en negrita y en subrayado es la ubicación del índice de corrección del subconjunto 1 (que se especifica con un bit menos).</span><span class="sxs-lookup"><span data-stu-id="5af66-246">In this table of partition sets, the bolded and underlined entry is the location of the fix-up index for subset 1 (which is specified with one less bit).</span></span> <span data-ttu-id="5af66-247">El índice de corrección del subconjunto 0 siempre es el índice 0, ya que las particiones siempre están organizadas de forma que el índice 0 siempre está en el subconjunto 0.</span><span class="sxs-lookup"><span data-stu-id="5af66-247">The fix-up index for subset 0 is always index 0, as the partitioning is always arranged such that index 0 is always in subset 0.</span></span> <span data-ttu-id="5af66-248">El orden de las particiones va de arriba a izquierda a la derecha, de izquierda a derecha y de arriba abajo.</span><span class="sxs-lookup"><span data-stu-id="5af66-248">Partition order goes from top-left to bottom-right, moving left to right and then top to bottom.</span></span>

## <a name="bc6h-compressed-endpoint-format"></a><span data-ttu-id="5af66-249">Formato de punto de conexión comprimido BC6H</span><span class="sxs-lookup"><span data-stu-id="5af66-249">BC6H Compressed Endpoint Format</span></span>

![campos de bits para formatos de punto de conexión comprimidos de bc6h](images/bc6h-headers-med.png)

<span data-ttu-id="5af66-251">En esta tabla se muestran los campos de bits de los puntos de conexión comprimidos como una función del formato del extremo, donde cada columna especifica una codificación y cada fila especifica un campo de bits.</span><span class="sxs-lookup"><span data-stu-id="5af66-251">This table shows the bit fields for the compressed endpoints as a function of the endpoint format, with each column specifying an encoding and each row specifying a bit field.</span></span> <span data-ttu-id="5af66-252">Este enfoque ocupa 82 bits para los mosaicos de dos regiones y 65 bits para los mosaicos de una región.</span><span class="sxs-lookup"><span data-stu-id="5af66-252">This approach takes up 82 bits for two-region tiles and 65 bits for one-region tiles.</span></span> <span data-ttu-id="5af66-253">Por ejemplo, los primeros cinco bits para la codificación de una región \[ 16 4 \] anterior (en concreto, la columna situada más a la derecha) son \[ los bits m 4:0 \] , los 10 bits siguientes son bits RW \[ 9:0 \] y así sucesivamente con los 6 últimos bits que contienen BW \[ 10:15 \] .</span><span class="sxs-lookup"><span data-stu-id="5af66-253">As an example, the first 5 bits for the one-region \[16 4\] encoding above (specifically the right-most column) are bits m\[4:0\], the next 10 bits are bits rw\[9:0\], and so on with the last 6 bits containing bw\[10:15\].</span></span>

<span data-ttu-id="5af66-254">Los nombres de campo de la tabla anterior se definen de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="5af66-254">The field names in the table above are defined as follows:</span></span>

| <span data-ttu-id="5af66-255">Campo</span><span class="sxs-lookup"><span data-stu-id="5af66-255">Field</span></span> | <span data-ttu-id="5af66-256">Variable</span><span class="sxs-lookup"><span data-stu-id="5af66-256">Variable</span></span>          |
|-------|-------------------|
| <span data-ttu-id="5af66-257">m</span><span class="sxs-lookup"><span data-stu-id="5af66-257">m</span></span>     | <span data-ttu-id="5af66-258">mode</span><span class="sxs-lookup"><span data-stu-id="5af66-258">mode</span></span>              |
| <span data-ttu-id="5af66-259">d</span><span class="sxs-lookup"><span data-stu-id="5af66-259">d</span></span>     | <span data-ttu-id="5af66-260">Índice de la forma</span><span class="sxs-lookup"><span data-stu-id="5af66-260">shape index</span></span>       |
| <span data-ttu-id="5af66-261">RW</span><span class="sxs-lookup"><span data-stu-id="5af66-261">rw</span></span>    | <span data-ttu-id="5af66-262">endpt \[ 0 \] . Un \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="5af66-262">endpt\[0\].A\[0\]</span></span> |
| <span data-ttu-id="5af66-263">CSO</span><span class="sxs-lookup"><span data-stu-id="5af66-263">rx</span></span>    | <span data-ttu-id="5af66-264">endpt \[ 0 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="5af66-264">endpt\[0\].B\[0\]</span></span> |
| <span data-ttu-id="5af66-265">r</span><span class="sxs-lookup"><span data-stu-id="5af66-265">ry</span></span>    | <span data-ttu-id="5af66-266">endpt \[ 1 \] . Un \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="5af66-266">endpt\[1\].A\[0\]</span></span> |
| <span data-ttu-id="5af66-267">RZ</span><span class="sxs-lookup"><span data-stu-id="5af66-267">rz</span></span>    | <span data-ttu-id="5af66-268">endpt \[ 1 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="5af66-268">endpt\[1\].B\[0\]</span></span> |
| <span data-ttu-id="5af66-269">GW</span><span class="sxs-lookup"><span data-stu-id="5af66-269">gw</span></span>    | <span data-ttu-id="5af66-270">endpt \[ 0 \] . \[1\]</span><span class="sxs-lookup"><span data-stu-id="5af66-270">endpt\[0\].A\[1\]</span></span> |
| <span data-ttu-id="5af66-271">GX</span><span class="sxs-lookup"><span data-stu-id="5af66-271">gx</span></span>    | <span data-ttu-id="5af66-272">endpt \[ 0 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="5af66-272">endpt\[0\].B\[1\]</span></span> |
| <span data-ttu-id="5af66-273">GY (</span><span class="sxs-lookup"><span data-stu-id="5af66-273">gy</span></span>    | <span data-ttu-id="5af66-274">endpt \[ 1 \] . \[1\]</span><span class="sxs-lookup"><span data-stu-id="5af66-274">endpt\[1\].A\[1\]</span></span> |
| <span data-ttu-id="5af66-275">gz</span><span class="sxs-lookup"><span data-stu-id="5af66-275">gz</span></span>    | <span data-ttu-id="5af66-276">endpt \[ 1 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="5af66-276">endpt\[1\].B\[1\]</span></span> |
| <span data-ttu-id="5af66-277">ancho</span><span class="sxs-lookup"><span data-stu-id="5af66-277">bw</span></span>    | <span data-ttu-id="5af66-278">endpt \[ 0 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="5af66-278">endpt\[0\].A\[2\]</span></span> |
| <span data-ttu-id="5af66-279">BX</span><span class="sxs-lookup"><span data-stu-id="5af66-279">bx</span></span>    | <span data-ttu-id="5af66-280">endpt \[ 0 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="5af66-280">endpt\[0\].B\[2\]</span></span> |
| <span data-ttu-id="5af66-281">by</span><span class="sxs-lookup"><span data-stu-id="5af66-281">by</span></span>    | <span data-ttu-id="5af66-282">endpt \[ 1 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="5af66-282">endpt\[1\].A\[2\]</span></span> |
| <span data-ttu-id="5af66-283">BZ</span><span class="sxs-lookup"><span data-stu-id="5af66-283">bz</span></span>    | <span data-ttu-id="5af66-284">endpt \[ 1 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="5af66-284">endpt\[1\].B\[2\]</span></span> |



 

<span data-ttu-id="5af66-285">Endpt \[ i \] , donde i es 0 o 1, hace referencia al conjunto de extremos 0 o 1, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5af66-285">Endpt\[i\], where i is either 0 or 1, refers to the 0th or 1st set of endpoints respectively.</span></span>

## <a name="sign-extension-for-endpoint-values"></a><span data-ttu-id="5af66-286">Extensión de signo para los valores de punto de conexión</span><span class="sxs-lookup"><span data-stu-id="5af66-286">Sign Extension for Endpoint Values</span></span>

<span data-ttu-id="5af66-287">En el caso de los mosaicos de dos regiones, hay cuatro valores de punto de conexión que se pueden firmar.</span><span class="sxs-lookup"><span data-stu-id="5af66-287">For two-region tiles, there are four endpoint values that can be sign extended.</span></span> <span data-ttu-id="5af66-288">Endpt \[ 0 \] . Un solo está firmado si el formato es un formato con signo; los otros puntos de conexión solo se firman si se transformó el punto de conexión, o si el formato es un formato con signo.</span><span class="sxs-lookup"><span data-stu-id="5af66-288">Endpt\[0\].A is signed only if the format is a signed format; the other endpoints are signed only if the endpoint was transformed, or if the format is a signed format.</span></span> <span data-ttu-id="5af66-289">En el código siguiente se muestra el algoritmo para extender el signo de los valores de punto de conexión de dos regiones.</span><span class="sxs-lookup"><span data-stu-id="5af66-289">The code below demonstrates the algorithm for extending the sign of two-region endpoint values.</span></span>

``` syntax
static void sign_extend_two_region(Pattern &p, IntEndpts endpts[NREGIONS_TWO])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
      if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
      if (p.transformed || BC6H::FORMAT == SIGNED_F16)
      {
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
        endpts[1].A[i] = SIGN_EXTEND(endpts[1].A[i], p.chan[i].delta[1]);
        endpts[1].B[i] = SIGN_EXTEND(endpts[1].B[i], p.chan[i].delta[2]);
      }
    }
}
```

<span data-ttu-id="5af66-290">En el caso de los mosaicos de una región, el comportamiento es el mismo, solo con endpt \[ 1 \] quitado.</span><span class="sxs-lookup"><span data-stu-id="5af66-290">For one-region tiles, the behavior is the same, only with endpt\[1\] removed.</span></span>

``` syntax
static void sign_extend_one_region(Pattern &p, IntEndpts endpts[NREGIONS_ONE])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
    if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
    if (p.transformed || BC6H::FORMAT == SIGNED_F16) 
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
    }
}
```

## <a name="transform-inversion-for-endpoint-values"></a><span data-ttu-id="5af66-291">Transformación de la inversión para los valores de punto de conexión</span><span class="sxs-lookup"><span data-stu-id="5af66-291">Transform Inversion for Endpoint Values</span></span>

<span data-ttu-id="5af66-292">En el caso de los mosaicos de dos regiones, la transformación aplica el inverso de la codificación de diferencia, agregando el valor base en endpt \[ 0 \] . A las otras tres entradas para un total de 9 operaciones de adición.</span><span class="sxs-lookup"><span data-stu-id="5af66-292">For two-region tiles, the transform applies the inverse of the difference encoding, adding the base value at endpt\[0\].A to the three other entries for a total of 9 add operations.</span></span> <span data-ttu-id="5af66-293">En la imagen siguiente, el valor base se representa como "a0" y tiene la precisión de punto flotante más alta.</span><span class="sxs-lookup"><span data-stu-id="5af66-293">In the image below, the base value is represented as "A0" and has the highest floating point precision.</span></span> <span data-ttu-id="5af66-294">"A1", "B0" y "B1" son deltas calculados a partir del valor de delimitador y estos valores Delta se representan con una precisión inferior.</span><span class="sxs-lookup"><span data-stu-id="5af66-294">"A1," "B0," and "B1" are all deltas calculated from the anchor value, and these delta values are represented with lower precision.</span></span> <span data-ttu-id="5af66-295">(A0 corresponde a endpt \[ 0 \] . A, B0 corresponde a endpt \[ 0 \] . B, a1 corresponde a endpt \[ 1 \] . Y B1 corresponde a endpt \[ 1 \] . B).</span><span class="sxs-lookup"><span data-stu-id="5af66-295">(A0 corresponds to endpt\[0\].A, B0 corresponds to endpt\[0\].B, A1 corresponds to endpt\[1\].A, and B1 corresponds to endpt\[1\].B.)</span></span>

![cálculo de valores de punto de conexión de inversión de transformación](images/bc6h-transform-inverse.png)

<span data-ttu-id="5af66-297">En el caso de los mosaicos de una región solo hay un desplazamiento Delta y, por lo tanto, solo 3 operaciones de adición.</span><span class="sxs-lookup"><span data-stu-id="5af66-297">For one-region tiles there is only one delta offset, and therefore only 3 add operations.</span></span>

<span data-ttu-id="5af66-298">El descompresor debe asegurarse de que los resultados de la transformación inversa no desbordarán la precisión de endpt \[ 0 \] . a.</span><span class="sxs-lookup"><span data-stu-id="5af66-298">The decompressor must ensure that that the results of the inverse transform will not overflow the precision of endpt\[0\].a.</span></span> <span data-ttu-id="5af66-299">En el caso de un desbordamiento, los valores resultantes de la transformación inversa deben ajustarse en el mismo número de bits.</span><span class="sxs-lookup"><span data-stu-id="5af66-299">In the case of an overflow, the values resulting from the inverse transform must wrap within the same number of bits.</span></span> <span data-ttu-id="5af66-300">Si la precisión de a0 es "p" bits, el algoritmo de transformación es:</span><span class="sxs-lookup"><span data-stu-id="5af66-300">If the precision of A0 is "p" bits, then the transform algorithm is:</span></span>

`B0 = (B0 + A0) & ((1 << p) - 1)`

<span data-ttu-id="5af66-301">En el caso de los formatos con signo, los resultados del cálculo Delta también se deben firmar.</span><span class="sxs-lookup"><span data-stu-id="5af66-301">For signed formats, the results of the delta calculation must be sign extended as well.</span></span> <span data-ttu-id="5af66-302">Si la operación de extensión de signo considera la ampliación de ambos signos, donde 0 es positivo y 1 es negativo, la extensión de signo de 0 se encarga de la abrazadera anterior.</span><span class="sxs-lookup"><span data-stu-id="5af66-302">If the sign extension operation considers extending both signs, where 0 is positive and 1 is negative, then the sign extension of 0 takes care of the clamp above.</span></span> <span data-ttu-id="5af66-303">De igual forma, después de la abrazadera anterior, solo es necesario firmar el valor 1 (negativo).</span><span class="sxs-lookup"><span data-stu-id="5af66-303">Equivalently, after the clamp above, only a value of 1 (negative) needs to be sign extended.</span></span>

## <a name="unquantization-of-color-endpoints"></a><span data-ttu-id="5af66-304">Descuantificación de los extremos de color</span><span class="sxs-lookup"><span data-stu-id="5af66-304">Unquantization of Color Endpoints</span></span>

<span data-ttu-id="5af66-305">Dados los puntos de conexión sin comprimir, el paso siguiente consiste en realizar una descuantificación inicial de los extremos de color.</span><span class="sxs-lookup"><span data-stu-id="5af66-305">Given the uncompressed endpoints, the next step is to perform an initial unquantization of the color endpoints.</span></span> <span data-ttu-id="5af66-306">Esto implica tres pasos:</span><span class="sxs-lookup"><span data-stu-id="5af66-306">This involves three steps:</span></span>

-   <span data-ttu-id="5af66-307">Una descuantificación de las paletas de colores</span><span class="sxs-lookup"><span data-stu-id="5af66-307">An unquantization of the color palettes</span></span>
-   <span data-ttu-id="5af66-308">Interpolación de las paletas</span><span class="sxs-lookup"><span data-stu-id="5af66-308">Interpolation of the palettes</span></span>
-   <span data-ttu-id="5af66-309">Finalización de la descuantificación</span><span class="sxs-lookup"><span data-stu-id="5af66-309">Unquantization finalization</span></span>

<span data-ttu-id="5af66-310">La separación del proceso de descuantificación en dos partes (descuantificación de la paleta de colores antes de la interpolación y la descuantificación final después de la interpolación) reduce el número de operaciones de multiplicación necesarias cuando se compara con un proceso de descuantificación completo antes de la interpolación de la paleta.</span><span class="sxs-lookup"><span data-stu-id="5af66-310">Separating the unquantization process into two parts (color palette unquantization before interpolation and final unquantization after interpolation) reduces the number of multiplication operations required when compared to a full unquantization process before palette interpolation.</span></span>

<span data-ttu-id="5af66-311">En el código siguiente se muestra el proceso para recuperar las estimaciones de los valores de color de 16 bits originales y, a continuación, usar los valores de peso proporcionados para agregar 6 valores de color adicionales a la paleta.</span><span class="sxs-lookup"><span data-stu-id="5af66-311">The code below illustrates the process for retrieving estimates of the original 16-bit color values, and then using the supplied weight values to add 6 additional color values to the palette.</span></span> <span data-ttu-id="5af66-312">La misma operación se realiza en cada canal.</span><span class="sxs-lookup"><span data-stu-id="5af66-312">The same operation is performed on each channel.</span></span>

``` syntax
int aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
int aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

// c1, c2: endpoints of a component
void generate_palette_unquantized(UINT8 uNumIndices, int c1, int c2, int prec, UINT16 palette[NINDICES])
{
    int* aWeights;
    if(uNumIndices == 8)
        aWeights = aWeight3;
    else  // uNumIndices == 16
        aWeights = aWeight4;

    int a = unquantize(c1, prec); 
    int b = unquantize(c2, prec);

    // interpolate
    for(int i = 0; i < uNumIndices; ++i)
        palette[i] = finish_unquantize((a * (64 - aWeights[i]) + b * aWeights[i] + 32) >> 6);
}
```

<span data-ttu-id="5af66-313">En el siguiente ejemplo de código se muestra el proceso de interpolación, con las siguientes observaciones:</span><span class="sxs-lookup"><span data-stu-id="5af66-313">The next code sample demonstrates the interpolation process, with the following observations:</span></span>

-   <span data-ttu-id="5af66-314">Puesto que el intervalo completo de valores de color para la función de **descuantificación** (a continuación) está comprendido entre-32768 y 65535, el interpolador se implementa mediante la aritmética con signo de 17 bits.</span><span class="sxs-lookup"><span data-stu-id="5af66-314">Since the full range of color values for the **unquantize** function (below) are from -32768 to 65535, the interpolator is implemented using 17-bit signed arithmetic.</span></span>
-   <span data-ttu-id="5af66-315">Después de la interpolación, los valores se pasan a la función **Finish \_ uncuantificate** (descrita en el tercer ejemplo de esta sección), que aplica el ajuste de escala final.</span><span class="sxs-lookup"><span data-stu-id="5af66-315">After interpolation, the values are passed to the **finish\_unquantize** function (described in the third sample in this section), which applies the final scaling.</span></span>
-   <span data-ttu-id="5af66-316">Todos los descompresores de hardware son necesarios para devolver resultados de bits precisos con estas funciones.</span><span class="sxs-lookup"><span data-stu-id="5af66-316">All hardware decompressors are required to return bit-accurate results with these functions.</span></span>

``` syntax
int unquantize(int comp, int uBitsPerComp)
{
    int unq, s = 0;
    switch(BC6H::FORMAT)
    {
    case UNSIGNED_F16:
        if(uBitsPerComp >= 15)
            unq = comp;
        else if(comp == 0)
            unq = 0;
        else if(comp == ((1 << uBitsPerComp) - 1))
            unq = 0xFFFF;
        else
            unq = ((comp << 16) + 0x8000) >> uBitsPerComp;
        break;

    case SIGNED_F16:
        if(uBitsPerComp >= 16)
            unq = comp;
        else
        {
            if(comp < 0)
            {
                s = 1;
                comp = -comp;
            }

            if(comp == 0)
                unq = 0;
            else if(comp >= ((1 << (uBitsPerComp - 1)) - 1))
                unq = 0x7FFF;
            else
                unq = ((comp << 15) + 0x4000) >> (uBitsPerComp-1);

            if(s)
                unq = -unq;
        }
        break;
    }
    return unq;
}
```

<span data-ttu-id="5af66-317">**la \_ descuantificación finalizar** se llama después de la interpolación de la paleta.</span><span class="sxs-lookup"><span data-stu-id="5af66-317">**finish\_unquantize** is called after palette interpolation.</span></span> <span data-ttu-id="5af66-318">La función **uncuantificate** pospone el ajuste de escala en 31/32 para signed, 31/64 para sin signo.</span><span class="sxs-lookup"><span data-stu-id="5af66-318">The **unquantize** function postpones the scaling by 31/32 for signed, 31/64 for unsigned.</span></span> <span data-ttu-id="5af66-319">Este comportamiento es necesario para obtener el valor final en el intervalo medio válido (-0x7BFF ~ 0x7BFF) después de que se complete la interpolación de la paleta con el fin de reducir el número de multiplicaciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="5af66-319">This behavior is required to get the final value into valid half range(-0x7BFF ~ 0x7BFF) after the palette interpolation is completed in order to reduce the number of necessary multiplications.</span></span> <span data-ttu-id="5af66-320">**finalizar \_ descuantificar** aplica el ajuste de escala final y devuelve un valor **Short sin signo** que se reinterpreta en la **mitad**.</span><span class="sxs-lookup"><span data-stu-id="5af66-320">**finish\_unquantize** applies the final scaling and returns an **unsigned short** value that gets reinterpreted into **half**.</span></span>

``` syntax
unsigned short finish_unquantize(int comp)
{
    if(BC6H::FORMAT == UNSIGNED_F16)
    {
        comp = (comp * 31) >> 6;                                         // scale the magnitude by 31/64
        return (unsigned short) comp;
    }
    else // (BC6H::FORMAT == SIGNED_F16)
    {
        comp = (comp < 0) ? -(((-comp) * 31) >> 5) : (comp * 31) >> 5;   // scale the magnitude by 31/32
        int s = 0;
        if(comp < 0)
        {
            s = 0x8000;
            comp = -comp;
        }
        return (unsigned short) (s | comp);
    }
}
```

## <a name="related-topics"></a><span data-ttu-id="5af66-321">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5af66-321">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5af66-322">Compresión de bloque de textura en Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="5af66-322">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 