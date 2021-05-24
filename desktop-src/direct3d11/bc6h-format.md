---
title: Formato BC6H
description: El formato BC6H es un formato de compresión de textura diseñado para admitir espacios de color de alto rango dinámico (HDR) en los datos de origen.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ea15e0275bc478c0708ce08f531d8888a3c84d
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335229"
---
# <a name="bc6h-format"></a><span data-ttu-id="07cc6-105">Formato BC6H</span><span class="sxs-lookup"><span data-stu-id="07cc6-105">BC6H Format</span></span>

<span data-ttu-id="07cc6-106">El formato BC6H es un formato de compresión de textura diseñado para admitir espacios de color de alto rango dinámico (HDR) en los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="07cc6-106">The BC6H format is a texture compression format designed to support high-dynamic range (HDR) color spaces in source data.</span></span>

-   [<span data-ttu-id="07cc6-107">Acerca del FORMATO BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="07cc6-107">About BC6H/DXGI\_FORMAT\_BC6H</span></span>](/windows)
-   [<span data-ttu-id="07cc6-108">Implementación de BC6H</span><span class="sxs-lookup"><span data-stu-id="07cc6-108">BC6H Implementation</span></span>](#bc6h-implementation)
-   [<span data-ttu-id="07cc6-109">Decoding the BC6H Format</span><span class="sxs-lookup"><span data-stu-id="07cc6-109">Decoding the BC6H Format</span></span>](#decoding-the-bc6h-format)
-   [<span data-ttu-id="07cc6-110">Formato de punto de conexión comprimido bc6H</span><span class="sxs-lookup"><span data-stu-id="07cc6-110">BC6H Compressed Endpoint Format</span></span>](#bc6h-compressed-endpoint-format)
-   [<span data-ttu-id="07cc6-111">Extensión de signo para valores de punto de conexión</span><span class="sxs-lookup"><span data-stu-id="07cc6-111">Sign Extension for Endpoint Values</span></span>](#sign-extension-for-endpoint-values)
-   [<span data-ttu-id="07cc6-112">Inversión de transformación para valores de punto de conexión</span><span class="sxs-lookup"><span data-stu-id="07cc6-112">Transform Inversion for Endpoint Values</span></span>](#transform-inversion-for-endpoint-values)
-   [<span data-ttu-id="07cc6-113">Descuantización de puntos de conexión de color</span><span class="sxs-lookup"><span data-stu-id="07cc6-113">Unquantization of Color Endpoints</span></span>](#unquantization-of-color-endpoints)
-   [<span data-ttu-id="07cc6-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07cc6-114">Related topics</span></span>](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a><span data-ttu-id="07cc6-115">Acerca del FORMATO BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="07cc6-115">About BC6H/DXGI\_FORMAT\_BC6H</span></span>

<span data-ttu-id="07cc6-116">El formato BC6H proporciona compresión de alta calidad para imágenes que usan tres canales de color HDR, con un valor de 16 bits para cada canal de color del valor (16:16:16).</span><span class="sxs-lookup"><span data-stu-id="07cc6-116">The BC6H format provides high-quality compression for images that use three HDR color channels, with a 16-bit value for each color channel of the value (16:16:16).</span></span> <span data-ttu-id="07cc6-117">No hay compatibilidad con un canal alfa.</span><span class="sxs-lookup"><span data-stu-id="07cc6-117">There is no support for an alpha channel.</span></span>

<span data-ttu-id="07cc6-118">BC6H se especifica mediante los siguientes valores de enumeración DXGI \_ FORMAT:</span><span class="sxs-lookup"><span data-stu-id="07cc6-118">BC6H is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="07cc6-119">**DXGI \_ FORMAT \_ BC6H \_ TYPELESS**.</span><span class="sxs-lookup"><span data-stu-id="07cc6-119">**DXGI\_FORMAT\_BC6H\_TYPELESS**.</span></span>
-   <span data-ttu-id="07cc6-120">**DXGI \_ FORMAT \_ BC6H \_ UF16**.</span><span class="sxs-lookup"><span data-stu-id="07cc6-120">**DXGI\_FORMAT\_BC6H\_UF16**.</span></span> <span data-ttu-id="07cc6-121">Este formato BC6H no usa un bit de signo en los valores del canal de color de punto flotante de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="07cc6-121">This BC6H format does not use a sign bit in the 16-bit floating point color channel values.</span></span>
-   <span data-ttu-id="07cc6-122">**DXGI \_ FORMAT \_ BC6H \_ SF16**. Este formato BC6H usa un bit de signo en los valores del canal de color de punto flotante de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="07cc6-122">**DXGI\_FORMAT\_BC6H\_SF16**.This BC6H format uses a sign bit in the 16-bit floating point color channel values.</span></span>

> [!Note]  
> <span data-ttu-id="07cc6-123">El formato de punto flotante de 16 bits para los canales de color a menudo se conoce como formato de punto flotante "medio".</span><span class="sxs-lookup"><span data-stu-id="07cc6-123">The 16 bit floating point format for color channels is often referred to as a "half" floating point format.</span></span> <span data-ttu-id="07cc6-124">Este formato tiene el siguiente diseño de bits:</span><span class="sxs-lookup"><span data-stu-id="07cc6-124">This format has the following bit layout:</span></span>
>
> |  <span data-ttu-id="07cc6-125">Formato</span><span class="sxs-lookup"><span data-stu-id="07cc6-125">Format</span></span>                     | <span data-ttu-id="07cc6-126">Diseño de bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-126">Bit layout</span></span>                                                |
> |-----------------------|-------------------------------------------------|
> | <span data-ttu-id="07cc6-127">UF16 (flotante sin signo)</span><span class="sxs-lookup"><span data-stu-id="07cc6-127">UF16 (unsigned float)</span></span> | <span data-ttu-id="07cc6-128">5 bits de exponente + 11 bits de mantisa</span><span class="sxs-lookup"><span data-stu-id="07cc6-128">5 exponent bits + 11 mantissa bits</span></span>              |
> | <span data-ttu-id="07cc6-129">SF16 (float con firma)</span><span class="sxs-lookup"><span data-stu-id="07cc6-129">SF16 (signed float)</span></span>   | <span data-ttu-id="07cc6-130">1 bit de signo + 5 bits de exponente + 10 bits de mantisa</span><span class="sxs-lookup"><span data-stu-id="07cc6-130">1 sign bit + 5 exponent bits + 10 mantissa bits</span></span> |
>
> 
>
>  

 

<span data-ttu-id="07cc6-131">El formato BC6H se puede usar para los recursos de textura [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluidas las matrices), Texture3D o TextureCube (incluidas las matrices).</span><span class="sxs-lookup"><span data-stu-id="07cc6-131">The BC6H format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="07cc6-132">De forma similar, este formato se aplica a las superficies de mapa de MIP asociadas a estos recursos.</span><span class="sxs-lookup"><span data-stu-id="07cc6-132">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="07cc6-133">BC6H usa un tamaño de bloque fijo de 16 bytes (128 bits) y un tamaño de mosaico fijo de 4 x 4 texturas.</span><span class="sxs-lookup"><span data-stu-id="07cc6-133">BC6H uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="07cc6-134">Al igual que con los formatos BC anteriores, las imágenes de textura mayores que el tamaño de mosaico admitido (4x4) se comprimen mediante el uso de varios bloques.</span><span class="sxs-lookup"><span data-stu-id="07cc6-134">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="07cc6-135">Esta identidad de direccionamiento también se aplica a imágenes tridimensionales, mapas MIP, mapas de cubos y matrices de textura.</span><span class="sxs-lookup"><span data-stu-id="07cc6-135">This addressing identity applies also to three-dimensional images, MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="07cc6-136">Todos los iconos de imagen deben tener el mismo formato.</span><span class="sxs-lookup"><span data-stu-id="07cc6-136">All image tiles must be of the same format.</span></span>

<span data-ttu-id="07cc6-137">Algunas notas importantes sobre el formato BC6H:</span><span class="sxs-lookup"><span data-stu-id="07cc6-137">Some important notes about the BC6H format:</span></span>

-   <span data-ttu-id="07cc6-138">BC6H admite la desnormalización de punto flotante, pero no admite INF (infinito) y NaN (no un número).</span><span class="sxs-lookup"><span data-stu-id="07cc6-138">BC6H supports floating point denormalization, but does not support INF (infinity) and NaN (not a number).</span></span> <span data-ttu-id="07cc6-139">La excepción es el modo firmado de BC6H (DXGI \_ FORMAT \_ BC6H \_ SF16), que admite -INF (infinito negativo).</span><span class="sxs-lookup"><span data-stu-id="07cc6-139">The exception is the signed mode of BC6H (DXGI\_FORMAT\_BC6H\_SF16), which supports -INF (negative infinity).</span></span> <span data-ttu-id="07cc6-140">Tenga en cuenta que esta compatibilidad con -INF es simplemente un artefacto del propio formato y no es compatible específicamente con los codificadores para este formato.</span><span class="sxs-lookup"><span data-stu-id="07cc6-140">Note that this support for -INF is merely an artifact of the format itself, and is not specifically supported by encoders for this format.</span></span> <span data-ttu-id="07cc6-141">En general, cuando los codificadores encuentran datos de entrada INF (positivos o negativos) o NaN, deben convertir los datos en el valor de representación no INF máximo permitido y asignar NaN a 0 antes de la \\ compresión.</span><span class="sxs-lookup"><span data-stu-id="07cc6-141">In general, when encoders encounter INF (positive or negative) or NaN input data, they should \\ convert that data to the maximum allowable non-INF representation value, and map NaN to 0 prior to compression.</span></span>
-   <span data-ttu-id="07cc6-142">BC6H no admite un canal alfa.</span><span class="sxs-lookup"><span data-stu-id="07cc6-142">BC6H does not support an alpha channel.</span></span>
-   <span data-ttu-id="07cc6-143">El descodificador BC6H realiza la descompresión antes de realizar el filtrado de texturas.</span><span class="sxs-lookup"><span data-stu-id="07cc6-143">The BC6H decoder performs decompression before it performs texture filtering.</span></span>
-   <span data-ttu-id="07cc6-144">La descompresión de BC6H debe ser precisa en bits; Es decir, el hardware debe devolver resultados idénticos al descodificador descrito en esta documentación.</span><span class="sxs-lookup"><span data-stu-id="07cc6-144">BC6H decompression must be bit accurate; that is, the hardware must return results that are identical to the decoder described in this documentation.</span></span>

## <a name="bc6h-implementation"></a><span data-ttu-id="07cc6-145">Implementación de BC6H</span><span class="sxs-lookup"><span data-stu-id="07cc6-145">BC6H Implementation</span></span>

<span data-ttu-id="07cc6-146">Un bloque BC6H consta de bits de modo, puntos de conexión comprimidos, índices comprimidos y un índice de partición opcional.</span><span class="sxs-lookup"><span data-stu-id="07cc6-146">A BC6H block consists of mode bits, compressed endpoints, compressed indices, and an optional partition index.</span></span> <span data-ttu-id="07cc6-147">Este formato especifica 14 modos diferentes.</span><span class="sxs-lookup"><span data-stu-id="07cc6-147">This format specifies 14 different modes.</span></span>

<span data-ttu-id="07cc6-148">Un color de punto de conexión se almacena como un triplete RGB.</span><span class="sxs-lookup"><span data-stu-id="07cc6-148">An endpoint color is stored as an RGB triplet.</span></span> <span data-ttu-id="07cc6-149">BC6H define una paleta de colores en una línea aproximada a través de varios puntos de conexión de color definidos.</span><span class="sxs-lookup"><span data-stu-id="07cc6-149">BC6H defines a palette of colors on an approximate line across a number of defined color endpoints.</span></span> <span data-ttu-id="07cc6-150">Además, en función del modo, un icono se puede dividir en dos regiones o tratarse como una sola región, donde un icono de dos regiones tiene un conjunto independiente de puntos de conexión de color para cada región.</span><span class="sxs-lookup"><span data-stu-id="07cc6-150">Also, depending on the mode, a tile can be divided into two regions or treated as a single region, where a two-region tile has a separate set of color endpoints for each region.</span></span> <span data-ttu-id="07cc6-151">BC6H almacena un índice de paleta por elemento de textura.</span><span class="sxs-lookup"><span data-stu-id="07cc6-151">BC6H stores one palette index per texel.</span></span>

<span data-ttu-id="07cc6-152">En el caso de dos regiones, hay 32 particiones posibles.</span><span class="sxs-lookup"><span data-stu-id="07cc6-152">In the two-region case, there are 32 possible partitions.</span></span>

## <a name="decoding-the-bc6h-format"></a><span data-ttu-id="07cc6-153">Decoding the BC6H Format</span><span class="sxs-lookup"><span data-stu-id="07cc6-153">Decoding the BC6H Format</span></span>

<span data-ttu-id="07cc6-154">El pseudocódigo siguiente muestra los pasos para descomprimir el píxel en (x,y) dado el bloque BC6H de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="07cc6-154">The pseudocode below shows the steps to decompress the pixel at (x,y) given the 16 byte BC6H block.</span></span>

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

<span data-ttu-id="07cc6-155">La tabla siguiente contiene el número de bits y los valores de cada uno de los 14 formatos posibles para los bloques BC6H.</span><span class="sxs-lookup"><span data-stu-id="07cc6-155">The following table contains the bit count and values for each of the 14 possible formats for BC6H blocks.</span></span> 

| <span data-ttu-id="07cc6-156">Mode</span><span class="sxs-lookup"><span data-stu-id="07cc6-156">Mode</span></span> | <span data-ttu-id="07cc6-157">Índices de partición</span><span class="sxs-lookup"><span data-stu-id="07cc6-157">Partition Indices</span></span> | <span data-ttu-id="07cc6-158">Partición</span><span class="sxs-lookup"><span data-stu-id="07cc6-158">Partition</span></span> | <span data-ttu-id="07cc6-159">Puntos de conexión de color</span><span class="sxs-lookup"><span data-stu-id="07cc6-159">Color Endpoints</span></span>                  | <span data-ttu-id="07cc6-160">Bits de modo</span><span class="sxs-lookup"><span data-stu-id="07cc6-160">Mode Bits</span></span>      |
|------|-------------------|-----------|----------------------------------|----------------|
| <span data-ttu-id="07cc6-161">1</span><span class="sxs-lookup"><span data-stu-id="07cc6-161">1</span></span>    | <span data-ttu-id="07cc6-162">46 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-162">46 bits</span></span>           | <span data-ttu-id="07cc6-163">5 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-163">5 bits</span></span>    | <span data-ttu-id="07cc6-164">75 bits (10,555, 10,555, 10,555)</span><span class="sxs-lookup"><span data-stu-id="07cc6-164">75 bits (10.555, 10.555, 10.555)</span></span> | <span data-ttu-id="07cc6-165">2 bits (00)</span><span class="sxs-lookup"><span data-stu-id="07cc6-165">2 bits (00)</span></span>    |
| <span data-ttu-id="07cc6-166">2</span><span class="sxs-lookup"><span data-stu-id="07cc6-166">2</span></span>    | <span data-ttu-id="07cc6-167">46 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-167">46 bits</span></span>           | <span data-ttu-id="07cc6-168">5 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-168">5 bits</span></span>    | <span data-ttu-id="07cc6-169">75 bits (7666, 7666, 7666)</span><span class="sxs-lookup"><span data-stu-id="07cc6-169">75 bits (7666, 7666, 7666)</span></span>       | <span data-ttu-id="07cc6-170">2 bits (01)</span><span class="sxs-lookup"><span data-stu-id="07cc6-170">2 bits (01)</span></span>    |
| <span data-ttu-id="07cc6-171">3</span><span class="sxs-lookup"><span data-stu-id="07cc6-171">3</span></span>    | <span data-ttu-id="07cc6-172">46 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-172">46 bits</span></span>           | <span data-ttu-id="07cc6-173">5 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-173">5 bits</span></span>    | <span data-ttu-id="07cc6-174">72 bits (11,555, 11,444, 11,444)</span><span class="sxs-lookup"><span data-stu-id="07cc6-174">72 bits (11.555, 11.444, 11.444)</span></span> | <span data-ttu-id="07cc6-175">5 bits (00010)</span><span class="sxs-lookup"><span data-stu-id="07cc6-175">5 bits (00010)</span></span> |
| <span data-ttu-id="07cc6-176">4</span><span class="sxs-lookup"><span data-stu-id="07cc6-176">4</span></span>    | <span data-ttu-id="07cc6-177">46 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-177">46 bits</span></span>           | <span data-ttu-id="07cc6-178">5 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-178">5 bits</span></span>    | <span data-ttu-id="07cc6-179">72 bits (11,444, 11,555, 11,444)</span><span class="sxs-lookup"><span data-stu-id="07cc6-179">72 bits (11.444, 11.555, 11.444)</span></span> | <span data-ttu-id="07cc6-180">5 bits (00110)</span><span class="sxs-lookup"><span data-stu-id="07cc6-180">5 bits (00110)</span></span> |
| <span data-ttu-id="07cc6-181">5</span><span class="sxs-lookup"><span data-stu-id="07cc6-181">5</span></span>    | <span data-ttu-id="07cc6-182">46 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-182">46 bits</span></span>           | <span data-ttu-id="07cc6-183">5 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-183">5 bits</span></span>    | <span data-ttu-id="07cc6-184">72 bits (11,444, 11,444, 11,555)</span><span class="sxs-lookup"><span data-stu-id="07cc6-184">72 bits (11.444, 11.444, 11.555)</span></span> | <span data-ttu-id="07cc6-185">5 bits (01010)</span><span class="sxs-lookup"><span data-stu-id="07cc6-185">5 bits (01010)</span></span> |
| <span data-ttu-id="07cc6-186">6</span><span class="sxs-lookup"><span data-stu-id="07cc6-186">6</span></span>    | <span data-ttu-id="07cc6-187">46 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-187">46 bits</span></span>           | <span data-ttu-id="07cc6-188">5 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-188">5 bits</span></span>    | <span data-ttu-id="07cc6-189">72 bits (9555, 9555, 9555)</span><span class="sxs-lookup"><span data-stu-id="07cc6-189">72 bits (9555, 9555, 9555)</span></span>       | <span data-ttu-id="07cc6-190">5 bits (01110)</span><span class="sxs-lookup"><span data-stu-id="07cc6-190">5 bits (01110)</span></span> |
| <span data-ttu-id="07cc6-191">7</span><span class="sxs-lookup"><span data-stu-id="07cc6-191">7</span></span>    | <span data-ttu-id="07cc6-192">46 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-192">46 bits</span></span>           | <span data-ttu-id="07cc6-193">5 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-193">5 bits</span></span>    | <span data-ttu-id="07cc6-194">72 bits (8666, 8555, 8555)</span><span class="sxs-lookup"><span data-stu-id="07cc6-194">72 bits (8666, 8555, 8555)</span></span>       | <span data-ttu-id="07cc6-195">5 bits (10010)</span><span class="sxs-lookup"><span data-stu-id="07cc6-195">5 bits (10010)</span></span> |
| <span data-ttu-id="07cc6-196">8</span><span class="sxs-lookup"><span data-stu-id="07cc6-196">8</span></span>    | <span data-ttu-id="07cc6-197">46 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-197">46 bits</span></span>           | <span data-ttu-id="07cc6-198">5 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-198">5 bits</span></span>    | <span data-ttu-id="07cc6-199">72 bits (8555, 8666, 8555)</span><span class="sxs-lookup"><span data-stu-id="07cc6-199">72 bits (8555, 8666, 8555)</span></span>       | <span data-ttu-id="07cc6-200">5 bits (10110)</span><span class="sxs-lookup"><span data-stu-id="07cc6-200">5 bits (10110)</span></span> |
| <span data-ttu-id="07cc6-201">9</span><span class="sxs-lookup"><span data-stu-id="07cc6-201">9</span></span>    | <span data-ttu-id="07cc6-202">46 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-202">46 bits</span></span>           | <span data-ttu-id="07cc6-203">5 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-203">5 bits</span></span>    | <span data-ttu-id="07cc6-204">72 bits (8555, 8555, 8666)</span><span class="sxs-lookup"><span data-stu-id="07cc6-204">72 bits (8555, 8555, 8666)</span></span>       | <span data-ttu-id="07cc6-205">5 bits (11010)</span><span class="sxs-lookup"><span data-stu-id="07cc6-205">5 bits (11010)</span></span> |
| <span data-ttu-id="07cc6-206">10</span><span class="sxs-lookup"><span data-stu-id="07cc6-206">10</span></span>   | <span data-ttu-id="07cc6-207">46 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-207">46 bits</span></span>           | <span data-ttu-id="07cc6-208">5 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-208">5 bits</span></span>    | <span data-ttu-id="07cc6-209">72 bits (6666, 6666, 6666)</span><span class="sxs-lookup"><span data-stu-id="07cc6-209">72 bits (6666, 6666, 6666)</span></span>       | <span data-ttu-id="07cc6-210">5 bits (11110)</span><span class="sxs-lookup"><span data-stu-id="07cc6-210">5 bits (11110)</span></span> |
| <span data-ttu-id="07cc6-211">11</span><span class="sxs-lookup"><span data-stu-id="07cc6-211">11</span></span>   | <span data-ttu-id="07cc6-212">63 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-212">63 bits</span></span>           | <span data-ttu-id="07cc6-213">0 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-213">0 bits</span></span>    | <span data-ttu-id="07cc6-214">60 bits (10.10, 10.10, 10.10)</span><span class="sxs-lookup"><span data-stu-id="07cc6-214">60 bits (10.10, 10.10, 10.10)</span></span>    | <span data-ttu-id="07cc6-215">5 bits (00011)</span><span class="sxs-lookup"><span data-stu-id="07cc6-215">5 bits (00011)</span></span> |
| <span data-ttu-id="07cc6-216">12</span><span class="sxs-lookup"><span data-stu-id="07cc6-216">12</span></span>   | <span data-ttu-id="07cc6-217">63 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-217">63 bits</span></span>           | <span data-ttu-id="07cc6-218">0 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-218">0 bits</span></span>    | <span data-ttu-id="07cc6-219">60 bits (11.9, 11.9, 11.9)</span><span class="sxs-lookup"><span data-stu-id="07cc6-219">60 bits (11.9, 11.9, 11.9)</span></span>       | <span data-ttu-id="07cc6-220">5 bits (00111)</span><span class="sxs-lookup"><span data-stu-id="07cc6-220">5 bits (00111)</span></span> |
| <span data-ttu-id="07cc6-221">13</span><span class="sxs-lookup"><span data-stu-id="07cc6-221">13</span></span>   | <span data-ttu-id="07cc6-222">63 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-222">63 bits</span></span>           | <span data-ttu-id="07cc6-223">0 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-223">0 bits</span></span>    | <span data-ttu-id="07cc6-224">60 bits (12.8, 12.8, 12.8)</span><span class="sxs-lookup"><span data-stu-id="07cc6-224">60 bits (12.8, 12.8, 12.8)</span></span>       | <span data-ttu-id="07cc6-225">5 bits (01011)</span><span class="sxs-lookup"><span data-stu-id="07cc6-225">5 bits (01011)</span></span> |
| <span data-ttu-id="07cc6-226">14</span><span class="sxs-lookup"><span data-stu-id="07cc6-226">14</span></span>   | <span data-ttu-id="07cc6-227">63 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-227">63 bits</span></span>           | <span data-ttu-id="07cc6-228">0 bits</span><span class="sxs-lookup"><span data-stu-id="07cc6-228">0 bits</span></span>    | <span data-ttu-id="07cc6-229">60 bits (16.4, 16.4, 16.4)</span><span class="sxs-lookup"><span data-stu-id="07cc6-229">60 bits (16.4, 16.4, 16.4)</span></span>       | <span data-ttu-id="07cc6-230">5 bits (01111)</span><span class="sxs-lookup"><span data-stu-id="07cc6-230">5 bits (01111)</span></span> |



 

<span data-ttu-id="07cc6-231">Los bits de modo pueden identificar de forma única cada formato de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="07cc6-231">Each format in this table can be uniquely identified by the mode bits.</span></span> <span data-ttu-id="07cc6-232">Los diez primeros modos se usan para los iconos de dos regiones y el campo de bits de modo puede tener una longitud de dos o cinco bits.</span><span class="sxs-lookup"><span data-stu-id="07cc6-232">The first ten modes are used for two-region tiles, and the mode bit field can be either two or five bits long.</span></span> <span data-ttu-id="07cc6-233">Estos bloques también tienen campos para los puntos de conexión de color comprimidos (72 o 75 bits), la partición (5 bits) y los índices de partición (46 bits).</span><span class="sxs-lookup"><span data-stu-id="07cc6-233">These blocks also have fields for the compressed color endpoints (72 or 75 bits), the partition (5 bits), and the partition indices (46 bits).</span></span>

<span data-ttu-id="07cc6-234">Para los puntos de conexión de color comprimidos, los valores de la tabla anterior tienen en cuenta la precisión de los puntos de conexión RGB almacenados y el número de bits usados para cada valor de color.</span><span class="sxs-lookup"><span data-stu-id="07cc6-234">For the compressed color endpoints, the values in the preceding table note the precision of the stored RGB endpoints, and the number of bits used for each color value.</span></span> <span data-ttu-id="07cc6-235">Por ejemplo, el modo 3 especifica un nivel de precisión de punto de conexión de color de 11 y el número de bits usados para almacenar los valores delta de los puntos de conexión transformados para los colores rojo, azul y verde (5, 4 y 4 respectivamente).</span><span class="sxs-lookup"><span data-stu-id="07cc6-235">For example, mode 3 specifies a color endpoint precision level of 11, and the number of bits used to store the delta values of the transformed endpoints for the red, blue and green colors (5, 4, and 4 respectively).</span></span> <span data-ttu-id="07cc6-236">El modo 10 no usa la compresión diferencial y, en su lugar, almacena los cuatro puntos de conexión de color explícitamente.</span><span class="sxs-lookup"><span data-stu-id="07cc6-236">Mode 10 does not use delta compression, and instead stores all four color endpoints explicitly.</span></span>

<span data-ttu-id="07cc6-237">Los cuatro últimos modos de bloque se usan para los iconos de una región, donde el campo de modo es de 5 bits.</span><span class="sxs-lookup"><span data-stu-id="07cc6-237">The last four block modes are used for one-region tiles, where the mode field is 5 bits.</span></span> <span data-ttu-id="07cc6-238">Estos bloques tienen campos para los puntos de conexión (60 bits) y los índices comprimidos (63 bits).</span><span class="sxs-lookup"><span data-stu-id="07cc6-238">These blocks have fields for the endpoints (60 bits) and the compressed indices (63 bits).</span></span> <span data-ttu-id="07cc6-239">El modo 11 (como el modo 10) no usa la compresión diferencial y, en su lugar, almacena ambos puntos de conexión de color explícitamente.</span><span class="sxs-lookup"><span data-stu-id="07cc6-239">Mode 11 (like Mode 10) does not use delta compression, and instead stores both color endpoints explicitly.</span></span>

<span data-ttu-id="07cc6-240">Los modos 10011, 10111, 11011 y 11111 (no se muestran) están reservados.</span><span class="sxs-lookup"><span data-stu-id="07cc6-240">Modes 10011, 10111, 11011, and 11111 (not shown) are reserved.</span></span> <span data-ttu-id="07cc6-241">No los use en el codificador.</span><span class="sxs-lookup"><span data-stu-id="07cc6-241">Do not use these in your encoder.</span></span> <span data-ttu-id="07cc6-242">Si se pasan bloques de hardware con uno de estos modos especificados, el bloque descomprimido resultante debe contener todos los ceros en todos los canales, excepto el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="07cc6-242">If the hardware is passed blocks with one of these modes specified, the resulting decompressed block must contain all zeroes in all channels except for the alpha channel.</span></span>

<span data-ttu-id="07cc6-243">Para BC6H, el canal alfa siempre debe devolver 1.0 independientemente del modo.</span><span class="sxs-lookup"><span data-stu-id="07cc6-243">For BC6H, the alpha channel must always return 1.0 regardless of the mode.</span></span>

### <a name="bc6h-partition-set"></a><span data-ttu-id="07cc6-244">Conjunto de particiones BC6H</span><span class="sxs-lookup"><span data-stu-id="07cc6-244">BC6H Partition Set</span></span>

<span data-ttu-id="07cc6-245">Hay 32 posibles conjuntos de particiones para un icono de dos regiones y que se definen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="07cc6-245">There are 32 possible partition sets for a two-region tile, and which are defined in the table below.</span></span> <span data-ttu-id="07cc6-246">Cada bloque 4x4 representa una sola forma.</span><span class="sxs-lookup"><span data-stu-id="07cc6-246">Each 4x4 block represents a single shape.</span></span>

![tabla de conjuntos de particiones bc6h](images/bc6h-partition-sets.png)

<span data-ttu-id="07cc6-248">En esta tabla de conjuntos de particiones, la entrada en negrita y subrayado es la ubicación del índice de corrección para el subconjunto 1 (que se especifica con un bit menos).</span><span class="sxs-lookup"><span data-stu-id="07cc6-248">In this table of partition sets, the bolded and underlined entry is the location of the fix-up index for subset 1 (which is specified with one less bit).</span></span> <span data-ttu-id="07cc6-249">El índice de corrección del subconjunto 0 siempre es el índice 0, ya que la creación de particiones siempre se organiza de forma que el índice 0 siempre está en el subconjunto 0.</span><span class="sxs-lookup"><span data-stu-id="07cc6-249">The fix-up index for subset 0 is always index 0, as the partitioning is always arranged such that index 0 is always in subset 0.</span></span> <span data-ttu-id="07cc6-250">El orden de partición va de arriba a abajo a la derecha, se mueve de izquierda a derecha y, a continuación, de arriba abajo.</span><span class="sxs-lookup"><span data-stu-id="07cc6-250">Partition order goes from top-left to bottom-right, moving left to right and then top to bottom.</span></span>

## <a name="bc6h-compressed-endpoint-format"></a><span data-ttu-id="07cc6-251">Formato de punto de conexión comprimido bc6H</span><span class="sxs-lookup"><span data-stu-id="07cc6-251">BC6H Compressed Endpoint Format</span></span>

![campos de bits para formatos de punto de conexión comprimido bc6h](images/bc6h-headers-med.png)

<span data-ttu-id="07cc6-253">En esta tabla se muestran los campos de bits de los puntos de conexión comprimidos como una función del formato de punto de conexión, donde cada columna especifica una codificación y cada fila especifica un campo de bits.</span><span class="sxs-lookup"><span data-stu-id="07cc6-253">This table shows the bit fields for the compressed endpoints as a function of the endpoint format, with each column specifying an encoding and each row specifying a bit field.</span></span> <span data-ttu-id="07cc6-254">Este enfoque toma 82 bits para los iconos de dos regiones y 65 bits para los iconos de una región.</span><span class="sxs-lookup"><span data-stu-id="07cc6-254">This approach takes up 82 bits for two-region tiles and 65 bits for one-region tiles.</span></span> <span data-ttu-id="07cc6-255">Por ejemplo, los primeros 5 bits para la codificación one-region 16 4 anterior (específicamente la columna más a la derecha) son \[ \] bits m 4:0, los 10 bits siguientes son bits rw 9:0, y así sucesivamente con los últimos 6 bits que contienen \[ bw \] \[ \] \[ 10:15 \] .</span><span class="sxs-lookup"><span data-stu-id="07cc6-255">As an example, the first 5 bits for the one-region \[16 4\] encoding above (specifically the right-most column) are bits m\[4:0\], the next 10 bits are bits rw\[9:0\], and so on with the last 6 bits containing bw\[10:15\].</span></span>

<span data-ttu-id="07cc6-256">Los nombres de campo de la tabla anterior se definen de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="07cc6-256">The field names in the table above are defined as follows:</span></span>

| <span data-ttu-id="07cc6-257">Campo</span><span class="sxs-lookup"><span data-stu-id="07cc6-257">Field</span></span> | <span data-ttu-id="07cc6-258">Variable</span><span class="sxs-lookup"><span data-stu-id="07cc6-258">Variable</span></span>          |
|-------|-------------------|
| <span data-ttu-id="07cc6-259">m</span><span class="sxs-lookup"><span data-stu-id="07cc6-259">m</span></span>     | <span data-ttu-id="07cc6-260">mode</span><span class="sxs-lookup"><span data-stu-id="07cc6-260">mode</span></span>              |
| <span data-ttu-id="07cc6-261">d</span><span class="sxs-lookup"><span data-stu-id="07cc6-261">d</span></span>     | <span data-ttu-id="07cc6-262">índice de forma</span><span class="sxs-lookup"><span data-stu-id="07cc6-262">shape index</span></span>       |
| <span data-ttu-id="07cc6-263">Rw</span><span class="sxs-lookup"><span data-stu-id="07cc6-263">rw</span></span>    | <span data-ttu-id="07cc6-264">endpt \[ 0 \] . A \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="07cc6-264">endpt\[0\].A\[0\]</span></span> |
| <span data-ttu-id="07cc6-265">Rx</span><span class="sxs-lookup"><span data-stu-id="07cc6-265">rx</span></span>    | <span data-ttu-id="07cc6-266">endpt \[ 0 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="07cc6-266">endpt\[0\].B\[0\]</span></span> |
| <span data-ttu-id="07cc6-267">Ry</span><span class="sxs-lookup"><span data-stu-id="07cc6-267">ry</span></span>    | <span data-ttu-id="07cc6-268">endpt \[ 1 \] . A \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="07cc6-268">endpt\[1\].A\[0\]</span></span> |
| <span data-ttu-id="07cc6-269">Rz</span><span class="sxs-lookup"><span data-stu-id="07cc6-269">rz</span></span>    | <span data-ttu-id="07cc6-270">endpt \[ 1 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="07cc6-270">endpt\[1\].B\[0\]</span></span> |
| <span data-ttu-id="07cc6-271">Gw</span><span class="sxs-lookup"><span data-stu-id="07cc6-271">gw</span></span>    | <span data-ttu-id="07cc6-272">endpt \[ 0 \] . A \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="07cc6-272">endpt\[0\].A\[1\]</span></span> |
| <span data-ttu-id="07cc6-273">Gx</span><span class="sxs-lookup"><span data-stu-id="07cc6-273">gx</span></span>    | <span data-ttu-id="07cc6-274">endpt \[ 0 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="07cc6-274">endpt\[0\].B\[1\]</span></span> |
| <span data-ttu-id="07cc6-275">Gy</span><span class="sxs-lookup"><span data-stu-id="07cc6-275">gy</span></span>    | <span data-ttu-id="07cc6-276">endpt \[ 1 \] . A \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="07cc6-276">endpt\[1\].A\[1\]</span></span> |
| <span data-ttu-id="07cc6-277">gz</span><span class="sxs-lookup"><span data-stu-id="07cc6-277">gz</span></span>    | <span data-ttu-id="07cc6-278">endpt \[ 1 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="07cc6-278">endpt\[1\].B\[1\]</span></span> |
| <span data-ttu-id="07cc6-279">Bw</span><span class="sxs-lookup"><span data-stu-id="07cc6-279">bw</span></span>    | <span data-ttu-id="07cc6-280">endpt \[ 0 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="07cc6-280">endpt\[0\].A\[2\]</span></span> |
| <span data-ttu-id="07cc6-281">Bx</span><span class="sxs-lookup"><span data-stu-id="07cc6-281">bx</span></span>    | <span data-ttu-id="07cc6-282">endpt \[ 0 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="07cc6-282">endpt\[0\].B\[2\]</span></span> |
| <span data-ttu-id="07cc6-283">by</span><span class="sxs-lookup"><span data-stu-id="07cc6-283">by</span></span>    | <span data-ttu-id="07cc6-284">endpt \[ 1 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="07cc6-284">endpt\[1\].A\[2\]</span></span> |
| <span data-ttu-id="07cc6-285">Bz</span><span class="sxs-lookup"><span data-stu-id="07cc6-285">bz</span></span>    | <span data-ttu-id="07cc6-286">endpt \[ 1 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="07cc6-286">endpt\[1\].B\[2\]</span></span> |



 

<span data-ttu-id="07cc6-287">Endpt i , donde i es 0 o 1, hace referencia al \[ 0 o 1.º conjunto de puntos de \] conexión, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="07cc6-287">Endpt\[i\], where i is either 0 or 1, refers to the 0th or 1st set of endpoints respectively.</span></span>

## <a name="sign-extension-for-endpoint-values"></a><span data-ttu-id="07cc6-288">Extensión de signo para valores de punto de conexión</span><span class="sxs-lookup"><span data-stu-id="07cc6-288">Sign Extension for Endpoint Values</span></span>

<span data-ttu-id="07cc6-289">Para los iconos de dos regiones, hay cuatro valores de punto de conexión que se pueden firmar extendidos.</span><span class="sxs-lookup"><span data-stu-id="07cc6-289">For two-region tiles, there are four endpoint values that can be sign extended.</span></span> <span data-ttu-id="07cc6-290">Endpt \[ 0 \] . Un solo se firma si el formato es un formato firmado; Los demás puntos de conexión solo se firman si el punto de conexión se transformó o si el formato es un formato firmado.</span><span class="sxs-lookup"><span data-stu-id="07cc6-290">Endpt\[0\].A is signed only if the format is a signed format; the other endpoints are signed only if the endpoint was transformed, or if the format is a signed format.</span></span> <span data-ttu-id="07cc6-291">El código siguiente muestra el algoritmo para extender el signo de valores de punto de conexión de dos regiones.</span><span class="sxs-lookup"><span data-stu-id="07cc6-291">The code below demonstrates the algorithm for extending the sign of two-region endpoint values.</span></span>

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

<span data-ttu-id="07cc6-292">En el caso de los iconos de una región, el comportamiento es el mismo, solo con el punto \[ final 1 \] quitado.</span><span class="sxs-lookup"><span data-stu-id="07cc6-292">For one-region tiles, the behavior is the same, only with endpt\[1\] removed.</span></span>

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

## <a name="transform-inversion-for-endpoint-values"></a><span data-ttu-id="07cc6-293">Inversión de transformación para valores de punto de conexión</span><span class="sxs-lookup"><span data-stu-id="07cc6-293">Transform Inversion for Endpoint Values</span></span>

<span data-ttu-id="07cc6-294">En el caso de los iconos de dos regiones, la transformación aplica la codificación inversa de la diferencia, agregando el valor base en el punto \[ final \] 0. a las otras tres entradas para un total de 9 operaciones de adición.</span><span class="sxs-lookup"><span data-stu-id="07cc6-294">For two-region tiles, the transform applies the inverse of the difference encoding, adding the base value at endpt\[0\].A to the three other entries for a total of 9 add operations.</span></span> <span data-ttu-id="07cc6-295">En la imagen siguiente, el valor base se representa como "A0" y tiene la mayor precisión de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="07cc6-295">In the image below, the base value is represented as "A0" and has the highest floating point precision.</span></span> <span data-ttu-id="07cc6-296">"A1," "B0" y "B1" son deltas calculados a partir del valor delimitador y estos valores delta se representan con una precisión inferior.</span><span class="sxs-lookup"><span data-stu-id="07cc6-296">"A1," "B0," and "B1" are all deltas calculated from the anchor value, and these delta values are represented with lower precision.</span></span> <span data-ttu-id="07cc6-297">(A0 corresponde al punto final \[ \] 0. A, B0 corresponde al punto final \[ \] 0. B, A1 corresponde al punto \[ final \] 1. A y B1 corresponden al punto de conexión \[ 1 \] .B).</span><span class="sxs-lookup"><span data-stu-id="07cc6-297">(A0 corresponds to endpt\[0\].A, B0 corresponds to endpt\[0\].B, A1 corresponds to endpt\[1\].A, and B1 corresponds to endpt\[1\].B.)</span></span>

![cálculo de valores de punto de conexión de inversión de transformación](images/bc6h-transform-inverse.png)

<span data-ttu-id="07cc6-299">En el caso de los iconos de una región, solo hay un desplazamiento diferencial y, por tanto, solo 3 operaciones de adición.</span><span class="sxs-lookup"><span data-stu-id="07cc6-299">For one-region tiles there is only one delta offset, and therefore only 3 add operations.</span></span>

<span data-ttu-id="07cc6-300">El descomprimidor debe asegurarse de que los resultados de la transformación inversa no desbordarán la precisión del punto \[ final 0 \] .a.</span><span class="sxs-lookup"><span data-stu-id="07cc6-300">The decompressor must ensure that that the results of the inverse transform will not overflow the precision of endpt\[0\].a.</span></span> <span data-ttu-id="07cc6-301">En el caso de un desbordamiento, los valores resultantes de la transformación inversa deben ajustarse dentro del mismo número de bits.</span><span class="sxs-lookup"><span data-stu-id="07cc6-301">In the case of an overflow, the values resulting from the inverse transform must wrap within the same number of bits.</span></span> <span data-ttu-id="07cc6-302">Si la precisión de A0 es "p", el algoritmo de transformación es:</span><span class="sxs-lookup"><span data-stu-id="07cc6-302">If the precision of A0 is "p" bits, then the transform algorithm is:</span></span>

`B0 = (B0 + A0) & ((1 << p) - 1)`

<span data-ttu-id="07cc6-303">En el caso de los formatos firmados, los resultados del cálculo diferencial también se deben extender.</span><span class="sxs-lookup"><span data-stu-id="07cc6-303">For signed formats, the results of the delta calculation must be sign extended as well.</span></span> <span data-ttu-id="07cc6-304">Si la operación de extensión de signo considera extender ambos signos, donde 0 es positivo y 1 es negativo, la extensión de signo de 0 se encarga de la fijación anterior.</span><span class="sxs-lookup"><span data-stu-id="07cc6-304">If the sign extension operation considers extending both signs, where 0 is positive and 1 is negative, then the sign extension of 0 takes care of the clamp above.</span></span> <span data-ttu-id="07cc6-305">De forma equivalente, después de la fijación anterior, solo es necesario firmar un valor de 1 (negativo).</span><span class="sxs-lookup"><span data-stu-id="07cc6-305">Equivalently, after the clamp above, only a value of 1 (negative) needs to be sign extended.</span></span>

## <a name="unquantization-of-color-endpoints"></a><span data-ttu-id="07cc6-306">Descuantización de puntos de conexión de color</span><span class="sxs-lookup"><span data-stu-id="07cc6-306">Unquantization of Color Endpoints</span></span>

<span data-ttu-id="07cc6-307">Dados los puntos de conexión sin comprimir, el siguiente paso consiste en realizar una eliminación de la marca inicial de los puntos de conexión de color.</span><span class="sxs-lookup"><span data-stu-id="07cc6-307">Given the uncompressed endpoints, the next step is to perform an initial unquantization of the color endpoints.</span></span> <span data-ttu-id="07cc6-308">Esto implica tres pasos:</span><span class="sxs-lookup"><span data-stu-id="07cc6-308">This involves three steps:</span></span>

-   <span data-ttu-id="07cc6-309">Un descuantización de las paletas de colores</span><span class="sxs-lookup"><span data-stu-id="07cc6-309">An unquantization of the color palettes</span></span>
-   <span data-ttu-id="07cc6-310">Interpolación de las paletas</span><span class="sxs-lookup"><span data-stu-id="07cc6-310">Interpolation of the palettes</span></span>
-   <span data-ttu-id="07cc6-311">Fin de la descontización</span><span class="sxs-lookup"><span data-stu-id="07cc6-311">Unquantization finalization</span></span>

<span data-ttu-id="07cc6-312">La separación del proceso de desquantización en dos partes (descuantización de la paleta de colores antes de la interpolación y desenlazamiento final después de la interpolación) reduce el número de operaciones de multiplicación necesarias en comparación con un proceso de descesión completo antes de la interpolación de la paleta.</span><span class="sxs-lookup"><span data-stu-id="07cc6-312">Separating the unquantization process into two parts (color palette unquantization before interpolation and final unquantization after interpolation) reduces the number of multiplication operations required when compared to a full unquantization process before palette interpolation.</span></span>

<span data-ttu-id="07cc6-313">El código siguiente muestra el proceso para recuperar estimaciones de los valores de color originales de 16 bits y, a continuación, usar los valores de peso proporcionados para agregar 6 valores de color adicionales a la paleta.</span><span class="sxs-lookup"><span data-stu-id="07cc6-313">The code below illustrates the process for retrieving estimates of the original 16-bit color values, and then using the supplied weight values to add 6 additional color values to the palette.</span></span> <span data-ttu-id="07cc6-314">La misma operación se realiza en cada canal.</span><span class="sxs-lookup"><span data-stu-id="07cc6-314">The same operation is performed on each channel.</span></span>

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

<span data-ttu-id="07cc6-315">En el ejemplo de código siguiente se muestra el proceso de interpolación, con las siguientes observaciones:</span><span class="sxs-lookup"><span data-stu-id="07cc6-315">The next code sample demonstrates the interpolation process, with the following observations:</span></span>

-   <span data-ttu-id="07cc6-316">Puesto que el intervalo completo de valores de color para la función **unquantize** (a continuación) va de -32768 a 65535, el interpolador se implementa mediante aritmética con firma de 17 bits.</span><span class="sxs-lookup"><span data-stu-id="07cc6-316">Since the full range of color values for the **unquantize** function (below) are from -32768 to 65535, the interpolator is implemented using 17-bit signed arithmetic.</span></span>
-   <span data-ttu-id="07cc6-317">Después de la interpolación, los valores se pasan a la función **finish \_ unquantize** (descrita en el tercer ejemplo de esta sección), que aplica el escalado final.</span><span class="sxs-lookup"><span data-stu-id="07cc6-317">After interpolation, the values are passed to the **finish\_unquantize** function (described in the third sample in this section), which applies the final scaling.</span></span>
-   <span data-ttu-id="07cc6-318">Todos los descompresores de hardware son necesarios para devolver resultados con precisión de bits con estas funciones.</span><span class="sxs-lookup"><span data-stu-id="07cc6-318">All hardware decompressors are required to return bit-accurate results with these functions.</span></span>

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

<span data-ttu-id="07cc6-319">**Se llama a finish \_ unquantize** después de la interpolación de la paleta.</span><span class="sxs-lookup"><span data-stu-id="07cc6-319">**finish\_unquantize** is called after palette interpolation.</span></span> <span data-ttu-id="07cc6-320">La **función unquantize** pospone el escalado en 31/32 para signed, 31/64 para unsigned.</span><span class="sxs-lookup"><span data-stu-id="07cc6-320">The **unquantize** function postpones the scaling by 31/32 for signed, 31/64 for unsigned.</span></span> <span data-ttu-id="07cc6-321">Este comportamiento es necesario para obtener el valor final en un intervalo medio válido (-0x7BFF ~ 0x7BFF) una vez completada la interpolación de la paleta con el fin de reducir el número de multiplicaciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="07cc6-321">This behavior is required to get the final value into valid half range(-0x7BFF ~ 0x7BFF) after the palette interpolation is completed in order to reduce the number of necessary multiplications.</span></span> <span data-ttu-id="07cc6-322">**finish \_ unquantize** aplica el escalado final y devuelve **un** valor corto sin signo que se reinterpreta a la **mitad.**</span><span class="sxs-lookup"><span data-stu-id="07cc6-322">**finish\_unquantize** applies the final scaling and returns an **unsigned short** value that gets reinterpreted into **half**.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="07cc6-323">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07cc6-323">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07cc6-324">Compresión de bloques de textura en Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="07cc6-324">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 