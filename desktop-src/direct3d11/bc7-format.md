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
# <a name="bc7-format"></a>Formato BC7

El formato BC7 es un formato de compresión de textura que se usa para la compresión de alta calidad de datos RGB y RGBA.

-   [Acerca del formato BC7/DXGI \_ \_ BC7](/windows)
-   [Implementación de BC7](#bc7-implementation)
-   [Descodificar el formato BC7](#decoding-the-bc7-format)
-   [Temas relacionados](#related-topics)

Para obtener información sobre los modos de bloqueo del formato BC7, consulte [Referencia del modo de formato BC7](bc7-format-mode-reference.md).

## <a name="about-bc7dxgi_format_bc7"></a>Acerca del formato BC7/DXGI \_ \_ BC7

BC7 se especifica mediante los siguientes \_ valores de enumeración de formato de DXGI:

-   **DXGI \_ DAR formato a \_ BC7 \_ sin tipo**.
-   **DXGI \_ DAR formato a \_ BC7 \_ UNORM**.
-   **DXGI \_ FORMATO \_ BC7 \_ UNORM \_ sRGB**.

El formato BC7 se puede usar para los recursos de textura [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluidas las matrices), Texture3D o TextureCube (incluidas las matrices). Del mismo modo, este formato se aplica a las superficies de mapa MIP asociadas a estos recursos.

BC7 usa un tamaño de bloque fijo de 16 bytes (128 bits) y un tamaño de mosaico fijo de textura 4x4. Al igual que con los formatos BC anteriores, las imágenes de textura mayores que el tamaño de mosaico compatible (4x4) se comprimen mediante varios bloques. Esta identidad de direccionamiento también se aplica a imágenes de tres dimensiones y matrices de mapas MIP, cubemaps y Texture. Todos los mosaicos de imagen deben tener el mismo formato.

BC7 comprime las imágenes de datos de punto fijo de tres canales (RGB) y de cuatro canales (RGBA). Normalmente, los datos de origen son de 8 bits por componente de color (canal), aunque el formato es capaz de codificar los datos de origen con más bits por componente de color. Todos los mosaicos de imagen deben tener el mismo formato.

El descodificador de BC7 realiza la descompresión antes de aplicar el filtrado de textura.

El hardware de descompresión de BC7 debe ser preciso. es decir, el hardware debe devolver resultados idénticos a los resultados devueltos por el descodificador descrito en este documento.

## <a name="bc7-implementation"></a>Implementación de BC7

Una implementación de BC7 puede especificar uno de los ocho modos, con el modo especificado en el bit menos significativo del bloque de 16 bytes (128 bits). El modo está codificado por cero o más bits con un valor de 0 seguido de 1.

Un bloque BC7 puede contener varios pares de extremos. Para los fines de esta documentación, el conjunto de índices que corresponden a un par de puntos de conexión se puede denominar "subconjunto". Además, en algunos modos de bloqueo, la representación del punto de conexión se codifica en un formulario que, para los fines de esta documentación, se denominará "RBGP", donde el bit "P" representa un bit menos significativo compartido para los componentes de color del punto de conexión. Por ejemplo, si la representación del punto de conexión para el formato es "RGB 5.5.5.1", el punto de conexión se interpreta como un valor de 6.6.6 RGB, en el que el estado del bit P define el bit menos significativo de cada componente. De forma similar, para los datos de origen con un canal alfa, si la representación para el formato es "RGBAP 5.5.5.5.1", el punto de conexión es interepreted como RGBA 6.6.6.6. Dependiendo del modo de bloqueo, puede especificar el bit menos significativo compartido para ambos extremos de un subconjunto individualmente (2 P bits por subconjunto) o compartirlos entre los puntos de conexión de un subconjunto (1 P bits por subconjunto).

En el caso de los bloques BC7 que no codifican explícitamente el componente alfa, un bloque BC7 está formado por bits de modo, bits de partición, puntos de conexión comprimidos, índices comprimidos y un bit P opcional. En estos bloques, los puntos de conexión tienen una representación solo de RGB y el componente alfa se descodifica como 1,0 para todos los textura de datos de origen.

En el caso de los bloques BC7 que tienen componentes de color y alfa combinados, un bloque consta de bits de modo, puntos de conexión comprimidos, índices comprimidos y bits de partición opcionales y un bit P. En estos bloques, los colores del punto de conexión se expresan en formato RGBA y los valores de los componentes alfa se interpolan junto con los valores del componente de color.

En el caso de los bloques BC7 que tienen componentes de color y alfa independientes, un bloque consta de bits de modo, bits de rotación, puntos de conexión comprimidos, índices comprimidos y un bit de selector de índice opcional. Estos bloques tienen un vector RGB efectivo \[ R, G, B \] y un canal alfa escalar \[ a una \] codificación separada.

En la tabla siguiente se enumeran los componentes de cada tipo de bloque.



| El bloque BC7 contiene...     | bits de modo | bits de rotación | bit de selector de índice | bits de partición | puntos de conexión comprimidos | Bit P    | índices comprimidos |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| solo componentes de color     | requerido  | N/D           | N/D                | requerido       | requerido             | opcional | requerido           |
| color + alfa combinado    | requerido  | N/D           | N/D                | opcional       | requerido             | opcional | requerido           |
| color y con separación alfa | requerido  | requerido      | opcional           | N/D            | requerido             | N/D      | requerido           |



 

BC7 define una paleta de colores en una línea aproximada entre dos extremos. El valor de modo determina el número de pares de puntos de conexión de interpolación por bloque. BC7 almacena un índice de paleta por textura.

Para cada subconjunto de índices que corresponde a un par de puntos de conexión, el codificador corrige el estado de un bit de los datos de índice comprimidos para ese subconjunto. Para ello, elige un orden de punto de conexión que permita que el índice del índice designado "Fix-up" establezca el bit más significativo en 0 y que se pueda descartar, lo que ahorra un bit por subconjunto. En el caso de los modos de bloqueo con un solo subconjunto, el índice de corrección siempre es el índice 0.

## <a name="decoding-the-bc7-format"></a>Descodificar el formato BC7

En el siguiente pseudocódigo se describen los pasos para descomprimir el píxel en (x, y) dado el bloque BC7 de 16 bytes.

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

El pseudocódigo al describe los pasos para descodificar completamente los componentes alfa y de color del punto de conexión para cada subconjunto dado un bloque BC7 de 16 bytes.

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

Para generar cada componente interpolado para cada subconjunto, use el siguiente algoritmo: permita que "c" sea el componente que se va a generar. permita que "E0" sea el componente del punto de conexión 0 del subconjunto; y permiten que "E1" sea el componente del punto de conexión 1 del subconjunto.

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

En el siguiente pseudocódigo se muestra cómo extraer índices y recuentos de bits para los componentes de color y alfa. Los bloques con color y alfa independientes también tienen dos conjuntos de datos de índice: uno para el canal vectorial y otro para el canal escalar. En el modo 4, estos índices son de distintos anchos (2 o 3 bits) y hay un selector de un bit que especifica si los datos de vectores o escalares usan los índices de 3 bits. (La extracción del recuento de bits alfa es similar a la extracción del recuento de bits de color, pero con un comportamiento inverso basado en el bit **idxMode** ).

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

[Compresión de bloque de textura en Direct3D 11](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 