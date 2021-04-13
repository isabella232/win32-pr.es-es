---
title: Formato BC7
description: El formato BC7 es un formato de compresión de textura que se usa para la compresión de alta calidad de datos RGB y RGBA.
ms.assetid: DF333106-293E-4B3E-A1EB-B0BF0ADBAC72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9b64c3d4a8b5e960077a9f33de82ff08cd4bbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421211"
---
# <a name="bc7-format"></a><span data-ttu-id="00f4f-103">Formato BC7</span><span class="sxs-lookup"><span data-stu-id="00f4f-103">BC7 Format</span></span>

<span data-ttu-id="00f4f-104">El formato BC7 es un formato de compresión de textura que se usa para la compresión de alta calidad de datos RGB y RGBA.</span><span class="sxs-lookup"><span data-stu-id="00f4f-104">The BC7 format is a texture compression format used for high-quality compression of RGB and RGBA data.</span></span>

-   [<span data-ttu-id="00f4f-105">Acerca del formato BC7/DXGI \_ \_ BC7</span><span class="sxs-lookup"><span data-stu-id="00f4f-105">About BC7/DXGI\_FORMAT\_BC7</span></span>](/windows)
-   [<span data-ttu-id="00f4f-106">Implementación de BC7</span><span class="sxs-lookup"><span data-stu-id="00f4f-106">BC7 Implementation</span></span>](#bc7-implementation)
-   [<span data-ttu-id="00f4f-107">Descodificar el formato BC7</span><span class="sxs-lookup"><span data-stu-id="00f4f-107">Decoding the BC7 Format</span></span>](#decoding-the-bc7-format)
-   [<span data-ttu-id="00f4f-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00f4f-108">Related topics</span></span>](#related-topics)

<span data-ttu-id="00f4f-109">Para obtener información sobre los modos de bloqueo del formato BC7, consulte [Referencia del modo de formato BC7](bc7-format-mode-reference.md).</span><span class="sxs-lookup"><span data-stu-id="00f4f-109">For info about the block modes of the BC7 format, see [BC7 Format Mode Reference](bc7-format-mode-reference.md).</span></span>

## <a name="about-bc7dxgi_format_bc7"></a><span data-ttu-id="00f4f-110">Acerca del formato BC7/DXGI \_ \_ BC7</span><span class="sxs-lookup"><span data-stu-id="00f4f-110">About BC7/DXGI\_FORMAT\_BC7</span></span>

<span data-ttu-id="00f4f-111">BC7 se especifica mediante los siguientes \_ valores de enumeración de formato de DXGI:</span><span class="sxs-lookup"><span data-stu-id="00f4f-111">BC7 is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="00f4f-112">**DXGI \_ DAR formato a \_ BC7 \_ sin tipo**.</span><span class="sxs-lookup"><span data-stu-id="00f4f-112">**DXGI\_FORMAT\_BC7\_TYPELESS**.</span></span>
-   <span data-ttu-id="00f4f-113">**DXGI \_ DAR formato a \_ BC7 \_ UNORM**.</span><span class="sxs-lookup"><span data-stu-id="00f4f-113">**DXGI\_FORMAT\_BC7\_UNORM**.</span></span>
-   <span data-ttu-id="00f4f-114">**DXGI \_ FORMATO \_ BC7 \_ UNORM \_ sRGB**.</span><span class="sxs-lookup"><span data-stu-id="00f4f-114">**DXGI\_FORMAT\_BC7\_UNORM\_SRGB**.</span></span>

<span data-ttu-id="00f4f-115">El formato BC7 se puede usar para los recursos de textura [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluidas las matrices), Texture3D o TextureCube (incluidas las matrices).</span><span class="sxs-lookup"><span data-stu-id="00f4f-115">The BC7 format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="00f4f-116">Del mismo modo, este formato se aplica a las superficies de mapa MIP asociadas a estos recursos.</span><span class="sxs-lookup"><span data-stu-id="00f4f-116">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="00f4f-117">BC7 usa un tamaño de bloque fijo de 16 bytes (128 bits) y un tamaño de mosaico fijo de textura 4x4.</span><span class="sxs-lookup"><span data-stu-id="00f4f-117">BC7 uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="00f4f-118">Al igual que con los formatos BC anteriores, las imágenes de textura mayores que el tamaño de mosaico compatible (4x4) se comprimen mediante varios bloques.</span><span class="sxs-lookup"><span data-stu-id="00f4f-118">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="00f4f-119">Esta identidad de direccionamiento también se aplica a imágenes de tres dimensiones y matrices de mapas MIP, cubemaps y Texture.</span><span class="sxs-lookup"><span data-stu-id="00f4f-119">This addressing identity also applies to three-dimensional images and MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="00f4f-120">Todos los mosaicos de imagen deben tener el mismo formato.</span><span class="sxs-lookup"><span data-stu-id="00f4f-120">All image tiles must be of the same format.</span></span>

<span data-ttu-id="00f4f-121">BC7 comprime las imágenes de datos de punto fijo de tres canales (RGB) y de cuatro canales (RGBA).</span><span class="sxs-lookup"><span data-stu-id="00f4f-121">BC7 compresses both three-channel (RGB) and four-channel (RGBA) fixed-point data images.</span></span> <span data-ttu-id="00f4f-122">Normalmente, los datos de origen son de 8 bits por componente de color (canal), aunque el formato es capaz de codificar los datos de origen con más bits por componente de color.</span><span class="sxs-lookup"><span data-stu-id="00f4f-122">Typically, source data is 8 bits per color component (channel), although the format is capable of encoding source data with higher bits per color component.</span></span> <span data-ttu-id="00f4f-123">Todos los mosaicos de imagen deben tener el mismo formato.</span><span class="sxs-lookup"><span data-stu-id="00f4f-123">All image tiles must be of the same format.</span></span>

<span data-ttu-id="00f4f-124">El descodificador de BC7 realiza la descompresión antes de aplicar el filtrado de textura.</span><span class="sxs-lookup"><span data-stu-id="00f4f-124">The BC7 decoder performs decompression before texture filtering is applied.</span></span>

<span data-ttu-id="00f4f-125">El hardware de descompresión de BC7 debe ser preciso. es decir, el hardware debe devolver resultados idénticos a los resultados devueltos por el descodificador descrito en este documento.</span><span class="sxs-lookup"><span data-stu-id="00f4f-125">BC7 decompression hardware must be bit accurate; that is, the hardware must return results that are identical to the results returned by the decoder described in this document.</span></span>

## <a name="bc7-implementation"></a><span data-ttu-id="00f4f-126">Implementación de BC7</span><span class="sxs-lookup"><span data-stu-id="00f4f-126">BC7 Implementation</span></span>

<span data-ttu-id="00f4f-127">Una implementación de BC7 puede especificar uno de los ocho modos, con el modo especificado en el bit menos significativo del bloque de 16 bytes (128 bits).</span><span class="sxs-lookup"><span data-stu-id="00f4f-127">A BC7 implementation can specify one of 8 modes, with the mode specified in the least significant bit of the 16 byte (128 bit) block.</span></span> <span data-ttu-id="00f4f-128">El modo está codificado por cero o más bits con un valor de 0 seguido de 1.</span><span class="sxs-lookup"><span data-stu-id="00f4f-128">The mode is encoded by zero or more bits with a value of 0 followed by a 1.</span></span>

<span data-ttu-id="00f4f-129">Un bloque BC7 puede contener varios pares de extremos.</span><span class="sxs-lookup"><span data-stu-id="00f4f-129">A BC7 block can contain multiple endpoint pairs.</span></span> <span data-ttu-id="00f4f-130">Para los fines de esta documentación, el conjunto de índices que corresponden a un par de puntos de conexión se puede denominar "subconjunto".</span><span class="sxs-lookup"><span data-stu-id="00f4f-130">For the purposes of this documentation, the set of indices that correspond to an endpoint pair may be referred to as a "subset."</span></span> <span data-ttu-id="00f4f-131">Además, en algunos modos de bloqueo, la representación del punto de conexión se codifica en un formulario que, para los fines de esta documentación, se denominará "RBGP", donde el bit "P" representa un bit menos significativo compartido para los componentes de color del punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="00f4f-131">Also, in some block modes, the endpoint representation is encoded in a form that -- again, for the purposes of this documentation -- shall be referred to as "RBGP," where the "P" bit represents a shared least significant bit for the color components of the endpoint.</span></span> <span data-ttu-id="00f4f-132">Por ejemplo, si la representación del punto de conexión para el formato es "RGB 5.5.5.1", el punto de conexión se interpreta como un valor de 6.6.6 RGB, en el que el estado del bit P define el bit menos significativo de cada componente.</span><span class="sxs-lookup"><span data-stu-id="00f4f-132">For example, if the endpoint representation for the format is "RGB 5.5.5.1," then the endpoint is interpreted as an RGB 6.6.6 value, where the state of the P-bit defines the least significant bit of each component.</span></span> <span data-ttu-id="00f4f-133">De forma similar, para los datos de origen con un canal alfa, si la representación para el formato es "RGBAP 5.5.5.5.1", el punto de conexión es interepreted como RGBA 6.6.6.6.</span><span class="sxs-lookup"><span data-stu-id="00f4f-133">Similarly, for source data with an alpha channel, if the representation for the format is "RGBAP 5.5.5.5.1," then the endpoint is interepreted as RGBA 6.6.6.6.</span></span> <span data-ttu-id="00f4f-134">Dependiendo del modo de bloqueo, puede especificar el bit menos significativo compartido para ambos extremos de un subconjunto individualmente (2 P bits por subconjunto) o compartirlos entre los puntos de conexión de un subconjunto (1 P bits por subconjunto).</span><span class="sxs-lookup"><span data-stu-id="00f4f-134">Depending on the block mode, you can specify the shared least significant bit for either both endpoints of a subset individually (2 P-bits per subset), or shared between endpoints of a subset (1 P-bit per subset).</span></span>

<span data-ttu-id="00f4f-135">En el caso de los bloques BC7 que no codifican explícitamente el componente alfa, un bloque BC7 está formado por bits de modo, bits de partición, puntos de conexión comprimidos, índices comprimidos y un bit P opcional.</span><span class="sxs-lookup"><span data-stu-id="00f4f-135">For BC7 blocks that don't explicitly encode the alpha component, a BC7 block consists of mode bits, partition bits, compressed endpoints, compressed indices, and an optional P-bit.</span></span> <span data-ttu-id="00f4f-136">En estos bloques, los puntos de conexión tienen una representación solo de RGB y el componente alfa se descodifica como 1,0 para todos los textura de datos de origen.</span><span class="sxs-lookup"><span data-stu-id="00f4f-136">In these blocks the endpoints have an RGB-only representation and the alpha component is decoded as 1.0 for all texels in the source data.</span></span>

<span data-ttu-id="00f4f-137">En el caso de los bloques BC7 que tienen componentes de color y alfa combinados, un bloque consta de bits de modo, puntos de conexión comprimidos, índices comprimidos y bits de partición opcionales y un bit P.</span><span class="sxs-lookup"><span data-stu-id="00f4f-137">For BC7 blocks that have combined color and alpha components, a block consists of mode bits, compressed endpoints, compressed indices, and optional partition bits and a P-bit.</span></span> <span data-ttu-id="00f4f-138">En estos bloques, los colores del punto de conexión se expresan en formato RGBA y los valores de los componentes alfa se interpolan junto con los valores del componente de color.</span><span class="sxs-lookup"><span data-stu-id="00f4f-138">In these blocks, the endpoint colors are expressed in RGBA format, and alpha component values are interpolated alongside the color component values.</span></span>

<span data-ttu-id="00f4f-139">En el caso de los bloques BC7 que tienen componentes de color y alfa independientes, un bloque consta de bits de modo, bits de rotación, puntos de conexión comprimidos, índices comprimidos y un bit de selector de índice opcional.</span><span class="sxs-lookup"><span data-stu-id="00f4f-139">For BC7 blocks that have separate color and alpha components, a block consists of mode bits, rotation bits, compressed endpoints, compressed indices, and an optional index selector bit.</span></span> <span data-ttu-id="00f4f-140">Estos bloques tienen un vector RGB efectivo \[ R, G, B \] y un canal alfa escalar \[ a una \] codificación separada.</span><span class="sxs-lookup"><span data-stu-id="00f4f-140">These blocks have an effective RGB vector \[R, G, B\] and a scalar alpha channel \[A\] separately encoded.</span></span>

<span data-ttu-id="00f4f-141">En la tabla siguiente se enumeran los componentes de cada tipo de bloque.</span><span class="sxs-lookup"><span data-stu-id="00f4f-141">The following table lists the components of each block type.</span></span>



| <span data-ttu-id="00f4f-142">El bloque BC7 contiene...</span><span class="sxs-lookup"><span data-stu-id="00f4f-142">BC7 block contains...</span></span>     | <span data-ttu-id="00f4f-143">bits de modo</span><span class="sxs-lookup"><span data-stu-id="00f4f-143">mode bits</span></span> | <span data-ttu-id="00f4f-144">bits de rotación</span><span class="sxs-lookup"><span data-stu-id="00f4f-144">rotation bits</span></span> | <span data-ttu-id="00f4f-145">bit de selector de índice</span><span class="sxs-lookup"><span data-stu-id="00f4f-145">index selector bit</span></span> | <span data-ttu-id="00f4f-146">bits de partición</span><span class="sxs-lookup"><span data-stu-id="00f4f-146">partition bits</span></span> | <span data-ttu-id="00f4f-147">puntos de conexión comprimidos</span><span class="sxs-lookup"><span data-stu-id="00f4f-147">compressed endpoints</span></span> | <span data-ttu-id="00f4f-148">Bit P</span><span class="sxs-lookup"><span data-stu-id="00f4f-148">P-bit</span></span>    | <span data-ttu-id="00f4f-149">índices comprimidos</span><span class="sxs-lookup"><span data-stu-id="00f4f-149">compressed indices</span></span> |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| <span data-ttu-id="00f4f-150">solo componentes de color</span><span class="sxs-lookup"><span data-stu-id="00f4f-150">color components only</span></span>     | <span data-ttu-id="00f4f-151">requerido</span><span class="sxs-lookup"><span data-stu-id="00f4f-151">required</span></span>  | <span data-ttu-id="00f4f-152">N/D</span><span class="sxs-lookup"><span data-stu-id="00f4f-152">N/A</span></span>           | <span data-ttu-id="00f4f-153">N/D</span><span class="sxs-lookup"><span data-stu-id="00f4f-153">N/A</span></span>                | <span data-ttu-id="00f4f-154">requerido</span><span class="sxs-lookup"><span data-stu-id="00f4f-154">required</span></span>       | <span data-ttu-id="00f4f-155">requerido</span><span class="sxs-lookup"><span data-stu-id="00f4f-155">required</span></span>             | <span data-ttu-id="00f4f-156">opcional</span><span class="sxs-lookup"><span data-stu-id="00f4f-156">optional</span></span> | <span data-ttu-id="00f4f-157">requerido</span><span class="sxs-lookup"><span data-stu-id="00f4f-157">required</span></span>           |
| <span data-ttu-id="00f4f-158">color + alfa combinado</span><span class="sxs-lookup"><span data-stu-id="00f4f-158">color + alpha combined</span></span>    | <span data-ttu-id="00f4f-159">requerido</span><span class="sxs-lookup"><span data-stu-id="00f4f-159">required</span></span>  | <span data-ttu-id="00f4f-160">N/D</span><span class="sxs-lookup"><span data-stu-id="00f4f-160">N/A</span></span>           | <span data-ttu-id="00f4f-161">N/D</span><span class="sxs-lookup"><span data-stu-id="00f4f-161">N/A</span></span>                | <span data-ttu-id="00f4f-162">opcional</span><span class="sxs-lookup"><span data-stu-id="00f4f-162">optional</span></span>       | <span data-ttu-id="00f4f-163">requerido</span><span class="sxs-lookup"><span data-stu-id="00f4f-163">required</span></span>             | <span data-ttu-id="00f4f-164">opcional</span><span class="sxs-lookup"><span data-stu-id="00f4f-164">optional</span></span> | <span data-ttu-id="00f4f-165">requerido</span><span class="sxs-lookup"><span data-stu-id="00f4f-165">required</span></span>           |
| <span data-ttu-id="00f4f-166">color y con separación alfa</span><span class="sxs-lookup"><span data-stu-id="00f4f-166">color and alpha separated</span></span> | <span data-ttu-id="00f4f-167">requerido</span><span class="sxs-lookup"><span data-stu-id="00f4f-167">required</span></span>  | <span data-ttu-id="00f4f-168">requerido</span><span class="sxs-lookup"><span data-stu-id="00f4f-168">required</span></span>      | <span data-ttu-id="00f4f-169">opcional</span><span class="sxs-lookup"><span data-stu-id="00f4f-169">optional</span></span>           | <span data-ttu-id="00f4f-170">N/D</span><span class="sxs-lookup"><span data-stu-id="00f4f-170">N/A</span></span>            | <span data-ttu-id="00f4f-171">requerido</span><span class="sxs-lookup"><span data-stu-id="00f4f-171">required</span></span>             | <span data-ttu-id="00f4f-172">N/D</span><span class="sxs-lookup"><span data-stu-id="00f4f-172">N/A</span></span>      | <span data-ttu-id="00f4f-173">requerido</span><span class="sxs-lookup"><span data-stu-id="00f4f-173">required</span></span>           |



 

<span data-ttu-id="00f4f-174">BC7 define una paleta de colores en una línea aproximada entre dos extremos.</span><span class="sxs-lookup"><span data-stu-id="00f4f-174">BC7 defines a palette of colors on an approximate line between two endpoints.</span></span> <span data-ttu-id="00f4f-175">El valor de modo determina el número de pares de puntos de conexión de interpolación por bloque.</span><span class="sxs-lookup"><span data-stu-id="00f4f-175">The mode value determines the number of interpolating endpoint pairs per block.</span></span> <span data-ttu-id="00f4f-176">BC7 almacena un índice de paleta por textura.</span><span class="sxs-lookup"><span data-stu-id="00f4f-176">BC7 stores one palette index per texel.</span></span>

<span data-ttu-id="00f4f-177">Para cada subconjunto de índices que corresponde a un par de puntos de conexión, el codificador corrige el estado de un bit de los datos de índice comprimidos para ese subconjunto.</span><span class="sxs-lookup"><span data-stu-id="00f4f-177">For each subset of indices that corresponds to a pair of endpoints, the encoder fixes the state of one bit of the compressed index data for that subset.</span></span> <span data-ttu-id="00f4f-178">Para ello, elige un orden de punto de conexión que permita que el índice del índice designado "Fix-up" establezca el bit más significativo en 0 y que se pueda descartar, lo que ahorra un bit por subconjunto.</span><span class="sxs-lookup"><span data-stu-id="00f4f-178">It does so by choosing an endpoint order that allows the index for the designated "fix-up" index to set its most significant bit to 0, and which can then be discarded, saving one bit per subset.</span></span> <span data-ttu-id="00f4f-179">En el caso de los modos de bloqueo con un solo subconjunto, el índice de corrección siempre es el índice 0.</span><span class="sxs-lookup"><span data-stu-id="00f4f-179">For block modes with only a single subset, the fix-up index is always index 0.</span></span>

## <a name="decoding-the-bc7-format"></a><span data-ttu-id="00f4f-180">Descodificar el formato BC7</span><span class="sxs-lookup"><span data-stu-id="00f4f-180">Decoding the BC7 Format</span></span>

<span data-ttu-id="00f4f-181">En el siguiente pseudocódigo se describen los pasos para descomprimir el píxel en (x, y) dado el bloque BC7 de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="00f4f-181">The following pseudocode outlines the steps to decompress the pixel at (x,y) given the 16 byte BC7 block.</span></span>

``` syntax
decompress_bc7(x, y, block)
{
    mode = extract_mode(block);
    
    //decode partition data from explicit partition bits
    subset_index = 0;
    num_subsets = 1;
    
    if (mode.type == 0 OR == 1 OR == 2 OR == 3 OR == 7)
    {
        num_subsets = get_num_subsets(mode.type);
        partition_set_id = extract_partition_set_id(mode, block);
        subset_index = get_partition_index(num_subsets, partition_set_id, x, y);
    }
    
    //extract raw, compressed endpoint bits
    UINT8 endpoint_array[num_subsets][4] = extract_endpoints(mode, block);
    
    //decode endpoint color and alpha for each subset
    fully_decode_endpoints(endpoint_array, mode, block);
    
    //endpoints are now complete.
    UINT8 endpoint_start[4] = endpoint_array[2 * subset_index];
    UINT8 endpoint_end[4]   = endpoint_array[2 * subset_index + 1];
        
    //Determine the palette index for this pixel
    alpha_index     = get_alpha_index(block, mode, x, y);
    alpha_bitcount  = get_alpha_bitcount(block, mode);
    color_index     = get_color_index(block, mode, x, y);
    color_bitcount  = get_color_bitcount(block, mode);

    //determine output
    UINT8 output[4];
    output.rgb = interpolate(endpoint_start.rgb, endpoint_end.rgb, color_index, color_bitcount);
    output.a   = interpolate(endpoint_start.a,   endpoint_end.a,   alpha_index, alpha_bitcount);
    
    if (mode.type == 4 OR == 5)
    {
        //Decode the 2 color rotation bits as follows:
        // 00 – Block format is Scalar(A) Vector(RGB) - no swapping
        // 01 – Block format is Scalar(R) Vector(AGB) - swap A and R
        // 10 – Block format is Scalar(G) Vector(RAB) - swap A and G
        // 11 - Block format is Scalar(B) Vector(RGA) - swap A and B
        rotation = extract_rot_bits(mode, block);
        output = swap_channels(output, rotation);
    }
    
}
```

<span data-ttu-id="00f4f-182">El pseudocódigo al describe los pasos para descodificar completamente los componentes alfa y de color del punto de conexión para cada subconjunto dado un bloque BC7 de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="00f4f-182">The followoing pseudocode outlines the steps to fully decode endpoint color and alpha components for each subset given a 16-byte BC7 block.</span></span>

``` syntax
fully_decode_endpoints(endpoint_array, mode, block)
{
    //first handle modes that have P-bits
    if (mode.type == 0 OR == 1 OR == 3 OR == 6 OR == 7)
    {
        for each endpoint i
        {
            //component-wise left-shift
            endpoint_array[i].rgba = endpoint_array[i].rgba << 1;
        }
        
        //if P-bit is shared
        if (mode.type == 1) 
        {
            pbit_zero = extract_pbit_zero(mode, block);
            pbit_one = extract_pbit_one(mode, block);
            
            //rgb component-wise insert pbits
            endpoint_array[0].rgb |= pbit_zero;
            endpoint_array[1].rgb |= pbit_zero;
            endpoint_array[2].rgb |= pbit_one;
            endpoint_array[3].rgb |= pbit_one;  
        }
        else //unique P-bit per endpoint
        {  
            pbit_array = extract_pbit_array(mode, block);
            for each endpoint i
            {
                endpoint_array[i].rgba |= pbit_array[i];
            }
        }
    }

    for each endpoint i
    {
        // Color_component_precision & alpha_component_precision includes pbit
        // left shift endpoint components so that their MSB lies in bit 7
        endpoint_array[i].rgb = endpoint_array[i].rgb << (8 - color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a << (8 - alpha_component_precision(mode));

        // Replicate each component's MSB into the LSBs revealed by the left-shift operation above
        endpoint_array[i].rgb = endpoint_array[i].rgb | (endpoint_array[i].rgb >> color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a | (endpoint_array[i].a >> alpha_component_precision(mode));
    }
        
    //If this mode does not explicitly define the alpha component
    //set alpha equal to 1.0
    if (mode.type == 0 OR == 1 OR == 2 OR == 3)
    {
        for each endpoint i
        {
            endpoint_array[i].a = 255; //i.e. alpha = 1.0f
        }
    }
}
```

<span data-ttu-id="00f4f-183">Para generar cada componente interpolado para cada subconjunto, use el siguiente algoritmo: permita que "c" sea el componente que se va a generar. permita que "E0" sea el componente del punto de conexión 0 del subconjunto; y permiten que "E1" sea el componente del punto de conexión 1 del subconjunto.</span><span class="sxs-lookup"><span data-stu-id="00f4f-183">To generate each interpolated component for each subset, use the following algorithm: let "c" be the component to generate; let "e0" be that component of endpoint 0 of the subset; and let "e1" be that component of endpoint 1 of the subset.</span></span>

``` syntax
UINT16 aWeight2[] = {0, 21, 43, 64};
UINT16 aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
UINT16 aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

UINT8 interpolate(UINT8 e0, UINT8 e1, UINT8 index, UINT8 indexprecision)
{
    if(indexprecision == 2)
        return (UINT8) (((64 - aWeights2[index])*UINT16(e0) + aWeights2[index]*UINT16(e1) + 32) >> 6);
    else if(indexprecision == 3)
        return (UINT8) (((64 - aWeights3[index])*UINT16(e0) + aWeights3[index]*UINT16(e1) + 32) >> 6);
    else // indexprecision == 4
        return (UINT8) (((64 - aWeights4[index])*UINT16(e0) + aWeights4[index]*UINT16(e1) + 32) >> 6);
}
```

<span data-ttu-id="00f4f-184">En el siguiente pseudocódigo se muestra cómo extraer índices y recuentos de bits para los componentes de color y alfa.</span><span class="sxs-lookup"><span data-stu-id="00f4f-184">The following pseudocode illustrates how to extract indices and bit counts for color and alpha components.</span></span> <span data-ttu-id="00f4f-185">Los bloques con color y alfa independientes también tienen dos conjuntos de datos de índice: uno para el canal vectorial y otro para el canal escalar.</span><span class="sxs-lookup"><span data-stu-id="00f4f-185">Blocks with separate color and alpha also have two sets of index data: one for the vector channel, and one for the scalar channel.</span></span> <span data-ttu-id="00f4f-186">En el modo 4, estos índices son de distintos anchos (2 o 3 bits) y hay un selector de un bit que especifica si los datos de vectores o escalares usan los índices de 3 bits.</span><span class="sxs-lookup"><span data-stu-id="00f4f-186">For Mode 4, these indices are of differing widths (2 or 3 bits), and there is a one-bit selector which specifies whether the vector or scalar data uses the 3-bit indices.</span></span> <span data-ttu-id="00f4f-187">(La extracción del recuento de bits alfa es similar a la extracción del recuento de bits de color, pero con un comportamiento inverso basado en el bit **idxMode** ).</span><span class="sxs-lookup"><span data-stu-id="00f4f-187">(Extracting the alpha bit count is similar to extracting color bit count but with inverse behavior based on the **idxMode** bit.)</span></span>

``` syntax
bitcount get_color_bitcount(block, mode)
{
    if (mode.type == 0 OR == 1)
        return 3;
    
    if (mode.type == 2 OR == 3 OR == 5 OR == 7)
        return 2;
    
    if (mode.type == 6)
        return 4;
        
    //The only remaining case is Mode 4 with 1-bit index selector
    idxMode = extract_idxMode(block);
    if (idxMode == 0)
        return 2;
    else
        return 3;
}
```

## <a name="related-topics"></a><span data-ttu-id="00f4f-188">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00f4f-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00f4f-189">Compresión de bloque de textura en Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="00f4f-189">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 