---
title: Formato BC7
description: El formato BC7 es un formato de compresión de textura que se usa para la compresión de alta calidad de datos RGB y RGBA.
ms.assetid: DF333106-293E-4B3E-A1EB-B0BF0ADBAC72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd48826cc0c02be6d15a837c272442c0931e9660f507a90cb491acf4d5820ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858225"
---
# <a name="bc7-format"></a>Formato BC7

El formato BC7 es un formato de compresión de textura que se usa para la compresión de alta calidad de datos RGB y RGBA.

-   [Acerca del FORMATO BC7/DXGI \_ \_ BC7](/windows)
-   [Implementación de BC7](#bc7-implementation)
-   [Decoding the BC7 Format](#decoding-the-bc7-format)
-   [Temas relacionados](#related-topics)

Para obtener información sobre los modos de bloque del formato BC7, vea [Referencia del modo de formato BC7.](bc7-format-mode-reference.md)

## <a name="about-bc7dxgi_format_bc7"></a>Acerca del FORMATO BC7/DXGI \_ \_ BC7

BC7 se especifica mediante los siguientes valores de enumeración \_ DXGI FORMAT:

-   **DXGI \_ FORMAT \_ BC7 \_ SIN TIPO.**
-   **DXGI \_ FORMAT \_ BC7 \_ UNORM**.
-   **DXGI \_ FORMAT \_ BC7 \_ UNORM \_ SRGB**.

El formato BC7 se puede usar para los recursos de textura [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluidas las matrices), Texture3D o TextureCube (incluidas las matrices). De forma similar, este formato se aplica a las superficies de mapa de MIP asociadas a estos recursos.

BC7 usa un tamaño de bloque fijo de 16 bytes (128 bits) y un tamaño de mosaico fijo de 4 x 4 elementos de textura. Al igual que con los formatos BC anteriores, las imágenes de textura mayores que el tamaño de mosaico admitido (4x4) se comprimen mediante el uso de varios bloques. Esta identidad de direccionamiento también se aplica a imágenes tridimensionales y mapas MIP, mapas de cubos y matrices de textura. Todos los iconos de imagen deben tener el mismo formato.

BC7 comprime imágenes de datos de punto fijo de tres canales (RGB) y de cuatro canales (RGBA). Normalmente, los datos de origen son de 8 bits por componente de color (canal), aunque el formato es capaz de codificar los datos de origen con bits más altos por componente de color. Todos los iconos de imagen deben tener el mismo formato.

El descodificador BC7 realiza la descompresión antes de aplicar el filtrado de textura.

El hardware de descompresión bc7 debe ser bit preciso; Es decir, el hardware debe devolver resultados idénticos a los resultados devueltos por el descodificador descrito en este documento.

## <a name="bc7-implementation"></a>Implementación de BC7

Una implementación bc7 puede especificar uno de los 8 modos, con el modo especificado en el bit menos significativo del bloque de 16 bytes (128 bits). El modo se codifica mediante cero o más bits con un valor de 0 seguido de 1.

Un bloque BC7 puede contener varios pares de punto de conexión. Para los fines de esta documentación, el conjunto de índices que corresponden a un par de puntos de conexión se puede denominar "subconjunto". Además, en algunos modos de bloque, la representación del punto de conexión se codifica en un formato que, de nuevo, para los fines de esta documentación, se denominará "RBGP", donde el bit "P" representa un bit menos significativo compartido para los componentes de color del punto de conexión. Por ejemplo, si la representación del punto de conexión para el formato es "RGB 5.5.5.1", el punto de conexión se interpreta como un valor RGB 6.6.6, donde el estado del bit P define el bit menos significativo de cada componente. Del mismo modo, para los datos de origen con un canal alfa, si la representación para el formato es "RGBAP 5.5.5.5.1", el punto de conexión se intercala como RGBA 6.6.6.6. En función del modo de bloque, puede especificar el bit menos significativo compartido para ambos puntos de conexión de un subconjunto individualmente (2 bits P por subconjunto) o compartido entre los puntos de conexión de un subconjunto (1 bit P por subconjunto).

Para los bloques BC7 que no codifican explícitamente el componente alfa, un bloque BC7 consta de bits de modo, bits de partición, puntos de conexión comprimidos, índices comprimidos y un bit P opcional. En estos bloques, los puntos de conexión tienen una representación solo RGB y el componente alfa se descodifica como 1.0 para todos los elementos de textura de los datos de origen.

Para los bloques BC7 que tienen componentes de color y alfa combinados, un bloque consta de bits de modo, puntos de conexión comprimidos, índices comprimidos y bits de partición opcionales y un bit P. En estos bloques, los colores del punto de conexión se expresan en formato RGBA y los valores de componente alfa se interpolan junto con los valores de los componentes de color.

Para los bloques BC7 que tienen componentes alfa y de color independientes, un bloque consta de bits de modo, bits de rotación, puntos de conexión comprimidos, índices comprimidos y un bit de selector de índice opcional. Estos bloques tienen un vector RGB \[ efectivo R, G, B y un canal alfa escalar A \] codificado por \[ \] separado.

En la tabla siguiente se enumeran los componentes de cada tipo de bloque.



| El bloque BC7 contiene...     | bits de modo | bits de rotación | bit del selector de índice | bits de partición | puntos de conexión comprimidos | Bit P    | índices comprimidos |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| solo componentes de color     | requerido  | N/D           | N/D                | requerido       | requerido             | opcional | requerido           |
| color + alfa combinado    | requerido  | N/D           | N/D                | opcional       | requerido             | opcional | requerido           |
| color y alfa separados | requerido  | requerido      | opcional           | N/D            | requerido             | N/D      | requerido           |



 

BC7 define una paleta de colores en una línea aproximada entre dos puntos de conexión. El valor de modo determina el número de pares de punto de conexión de interpolación por bloque. BC7 almacena un índice de paleta por elemento de textura.

Para cada subconjunto de índices que corresponde a un par de puntos de conexión, el codificador corrige el estado de un bit de los datos de índice comprimidos para ese subconjunto. Para ello, elige un orden de punto de conexión que permite que el índice para el índice de "corrección" designado establezca su bit más significativo en 0 y, a continuación, se puede descartar, lo que ahorra un bit por subconjunto. Para los modos de bloque con un solo subconjunto, el índice de corrección siempre es el índice 0.

## <a name="decoding-the-bc7-format"></a>Decoding the BC7 Format

El pseudocódigo siguiente describe los pasos para descomprimir el píxel en (x,y) dado el bloque BC7 de 16 bytes.

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

El pseudocódigo siguiente describe los pasos para descodificar completamente el color del punto de conexión y los componentes alfa para cada subconjunto dado un bloque BC7 de 16 bytes.

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

Para generar cada componente interpolado para cada subconjunto, use el siguiente algoritmo: permita que "c" sea el componente que se va a generar; permita que "e0" sea ese componente del punto de conexión 0 del subconjunto; y permiten que "e1" sea ese componente del punto de conexión 1 del subconjunto.

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

El pseudocódigo siguiente muestra cómo extraer índices y recuentos de bits para componentes alfa y de color. Los bloques con color independiente y alfa también tienen dos conjuntos de datos de índice: uno para el canal vectorial y otro para el canal escalar. En el modo 4, estos índices tienen anchos diferentes (2 o 3 bits) y hay un selector de un bit que especifica si el vector o los datos escalares usan los índices de 3 bits. (Extraer el recuento de bits alfa es similar a extraer el recuento de bits de color, pero con un comportamiento inverso basado en el bit **idxMode).**

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

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compresión de bloques de textura en Direct3D 11](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 