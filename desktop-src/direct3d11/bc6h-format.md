---
title: Formato BC6H
description: El formato BC6H es un formato de compresión de textura diseñado para admitir espacios de color de alto rango dinámico (HDR) en los datos de origen.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27422e177e98ecdc53b4152ba0514866f5ad75216e9ef789145d1af882a645d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633825"
---
# <a name="bc6h-format"></a>Formato BC6H

El formato BC6H es un formato de compresión de textura diseñado para admitir espacios de color de alto rango dinámico (HDR) en los datos de origen.

-   [Acerca del FORMATO BC6H/DXGI \_ \_ BC6H](/windows)
-   [Implementación de BC6H](#bc6h-implementation)
-   [Decoding the BC6H Format](#decoding-the-bc6h-format)
-   [Formato de punto de conexión comprimido bc6H](#bc6h-compressed-endpoint-format)
-   [Extensión de signo para valores de punto de conexión](#sign-extension-for-endpoint-values)
-   [Inversión de transformación para valores de punto de conexión](#transform-inversion-for-endpoint-values)
-   [Descuantización de puntos de conexión de color](#unquantization-of-color-endpoints)
-   [Temas relacionados](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a>Acerca del FORMATO BC6H/DXGI \_ \_ BC6H

El formato BC6H proporciona compresión de alta calidad para imágenes que usan tres canales de color HDR, con un valor de 16 bits para cada canal de color del valor (16:16:16). No hay compatibilidad con un canal alfa.

BC6H se especifica mediante los siguientes valores de enumeración DXGI \_ FORMAT:

-   **DXGI \_ FORMAT \_ BC6H \_ TYPELESS**.
-   **DXGI \_ FORMAT \_ BC6H \_ UF16**. Este formato BC6H no usa un bit de signo en los valores del canal de color de punto flotante de 16 bits.
-   **DXGI \_ FORMAT \_ BC6H \_ SF16**. Este formato BC6H usa un bit de signo en los valores del canal de color de punto flotante de 16 bits.

> [!Note]  
> El formato de punto flotante de 16 bits para los canales de color a menudo se conoce como formato de punto flotante "medio". Este formato tiene el siguiente diseño de bits:
>
> |  Formato                     | Diseño de bits                                                |
> |-----------------------|-------------------------------------------------|
> | UF16 (flotante sin signo) | 5 bits de exponente + 11 bits de mantisa              |
> | SF16 (float con firma)   | 1 bit de signo + 5 bits de exponente + 10 bits de mantisa |
>
> 
>
>  

 

El formato BC6H se puede usar para los recursos de textura [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluidas las matrices), Texture3D o TextureCube (incluidas las matrices). De forma similar, este formato se aplica a las superficies de mapa de MIP asociadas a estos recursos.

BC6H usa un tamaño de bloque fijo de 16 bytes (128 bits) y un tamaño de mosaico fijo de 4x4 texels. Al igual que con los formatos bc anteriores, las imágenes de textura mayores que el tamaño de mosaico admitido (4x4) se comprimen mediante varios bloques. Esta identidad de direccionamiento también se aplica a imágenes tridimensionales, mapas MIP, mapas de cubo y matrices de textura. Todos los iconos de imagen deben tener el mismo formato.

Algunas notas importantes sobre el formato BC6H:

-   BC6H admite la desnormalización de punto flotante, pero no admite INF (infinito) ni NaN (no un número). La excepción es el modo firmado de BC6H (DXGI \_ FORMAT \_ BC6H \_ SF16), que admite -INF (infinito negativo). Tenga en cuenta que esta compatibilidad con -INF es simplemente un artefacto del propio formato y no es específicamente compatible con los codificadores para este formato. En general, cuando los codificadores encuentran datos de entrada INF (positivos o negativos) o NaN, deben convertir los datos al valor máximo permitido de representación no INF y asignar NaN a 0 antes de la \\ compresión.
-   BC6H no admite un canal alfa.
-   El descodificador BC6H realiza la descompresión antes de realizar el filtrado de texturas.
-   La descompresión de BC6H debe ser precisa en bits; Es decir, el hardware debe devolver resultados idénticos al descodificador descrito en esta documentación.

## <a name="bc6h-implementation"></a>Implementación de BC6H

Un bloque BC6H consta de bits de modo, puntos de conexión comprimidos, índices comprimidos y un índice de partición opcional. Este formato especifica 14 modos diferentes.

Un color de punto de conexión se almacena como un triplete RGB. BC6H define una paleta de colores en una línea aproximada a través de varios puntos de conexión de color definidos. Además, en función del modo, un icono se puede dividir en dos regiones o tratarse como una sola región, donde un icono de dos regiones tiene un conjunto independiente de puntos de conexión de color para cada región. BC6H almacena un índice de paleta por elemento de textura.

En el caso de dos regiones, hay 32 particiones posibles.

## <a name="decoding-the-bc6h-format"></a>Decoding the BC6H Format

El pseudocódigo siguiente muestra los pasos para descomprimir el píxel en (x,y) dado el bloque BC6H de 16 bytes.

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

La tabla siguiente contiene el número de bits y los valores de cada uno de los 14 formatos posibles para los bloques BC6H. 

| Modo | Índices de partición | Partition | Puntos de conexión de color                  | Bits de modo      |
|------|-------------------|-----------|----------------------------------|----------------|
| 1    | 46 bits           | 5 bits    | 75 bits (10,555, 10,555, 10,555) | 2 bits (00)    |
| 2    | 46 bits           | 5 bits    | 75 bits (7666, 7666, 7666)       | 2 bits (01)    |
| 3    | 46 bits           | 5 bits    | 72 bits (11,555, 11,444, 11,444) | 5 bits (00010) |
| 4    | 46 bits           | 5 bits    | 72 bits (11.444, 11.555, 11.444) | 5 bits (00110) |
| 5    | 46 bits           | 5 bits    | 72 bits (11.444, 11.444, 11.555) | 5 bits (01010) |
| 6    | 46 bits           | 5 bits    | 72 bits (9555, 9555, 9555)       | 5 bits (01110) |
| 7    | 46 bits           | 5 bits    | 72 bits (8666, 8555, 8555)       | 5 bits (10010) |
| 8    | 46 bits           | 5 bits    | 72 bits (8555, 8666, 8555)       | 5 bits (10110) |
| 9    | 46 bits           | 5 bits    | 72 bits (8555, 8555, 8666)       | 5 bits (11010) |
| 10   | 46 bits           | 5 bits    | 72 bits (6666, 6666, 6666)       | 5 bits (11110) |
| 11   | 63 bits           | 0 bits    | 60 bits (10.10, 10.10, 10.10)    | 5 bits (00011) |
| 12   | 63 bits           | 0 bits    | 60 bits (11.9, 11.9, 11.9)       | 5 bits (00111) |
| 13   | 63 bits           | 0 bits    | 60 bits (12.8, 12.8, 12.8)       | 5 bits (01011) |
| 14   | 63 bits           | 0 bits    | 60 bits (16.4, 16.4, 16.4)       | 5 bits (01111) |



 

Cada formato de esta tabla se puede identificar de forma única mediante los bits de modo. Los diez primeros modos se usan para iconos de dos regiones y el campo de bits de modo puede tener dos o cinco bits de longitud. Estos bloques también tienen campos para los puntos de conexión de color comprimidos (72 o 75 bits), la partición (5 bits) y los índices de partición (46 bits).

Para los puntos de conexión de color comprimidos, los valores de la tabla anterior tienen en cuenta la precisión de los puntos de conexión RGB almacenados y el número de bits usados para cada valor de color. Por ejemplo, el modo 3 especifica un nivel de precisión de punto de conexión de color de 11 y el número de bits usados para almacenar los valores delta de los puntos de conexión transformados para los colores rojo, azul y verde (5, 4 y 4 respectivamente). El modo 10 no usa la compresión diferencial y, en su lugar, almacena los cuatro puntos de conexión de color explícitamente.

Los cuatro últimos modos de bloque se usan para los iconos de una región, donde el campo de modo es de 5 bits. Estos bloques tienen campos para los puntos de conexión (60 bits) y los índices comprimidos (63 bits). El modo 11 (como el modo 10) no usa la compresión diferencial y, en su lugar, almacena ambos puntos de conexión de color explícitamente.

Los modos 10011, 10111, 11011 y 11111 (no se muestran) están reservados. No los use en el codificador. Si se pasan bloques de hardware con uno de estos modos especificados, el bloque descomprimido resultante debe contener todos los ceros en todos los canales, excepto el canal alfa.

Para BC6H, el canal alfa siempre debe devolver 1.0 independientemente del modo.

### <a name="bc6h-partition-set"></a>Conjunto de particiones BC6H

Hay 32 posibles conjuntos de particiones para un icono de dos regiones y que se definen en la tabla siguiente. Cada bloque 4x4 representa una sola forma.

![tabla de conjuntos de particiones bc6h](images/bc6h-partition-sets.png)

En esta tabla de conjuntos de particiones, la entrada en negrita y subrayado es la ubicación del índice de corrección para el subconjunto 1 (que se especifica con un bit menos). El índice de corrección del subconjunto 0 siempre es el índice 0, ya que la creación de particiones siempre se organiza de forma que el índice 0 siempre está en el subconjunto 0. El orden de partición va de arriba a abajo a la derecha, se mueve de izquierda a derecha y, a continuación, de arriba abajo.

## <a name="bc6h-compressed-endpoint-format"></a>Formato de punto de conexión comprimido bc6H

![campos de bits para formatos de punto de conexión comprimido bc6h](images/bc6h-headers-med.png)

En esta tabla se muestran los campos de bits de los puntos de conexión comprimidos como una función del formato de punto de conexión, donde cada columna especifica una codificación y cada fila especifica un campo de bits. Este enfoque ocupa 82 bits para los iconos de dos regiones y 65 bits para los iconos de una región. Por ejemplo, los primeros 5 bits para la codificación one-region 16 4 anterior (específicamente la columna más a la derecha) son \[ \] bits m 4:0, los 10 bits siguientes son bits rw 9:0, y así sucesivamente con los últimos 6 bits que contienen \[ bw \] \[ \] \[ 10:15 \] .

Los nombres de campo de la tabla anterior se definen de la siguiente manera:

| Campo | Variable          |
|-------|-------------------|
| m     | mode              |
| d     | índice de forma       |
| Rw    | endpt \[ 0 \] . A \[ 0\] |
| Rx    | endpt \[ 0 \] . B \[ 0\] |
| Ry    | endpt \[ 1 \] . A \[ 0\] |
| Rz    | endpt \[ 1 \] . B \[ 0\] |
| Gw    | endpt \[ 0 \] . A \[ 1\] |
| Gx    | endpt \[ 0 \] . B \[ 1\] |
| Gy    | endpt \[ 1 \] . A \[ 1\] |
| gz    | endpt \[ 1 \] . B \[ 1\] |
| Bw    | endpt \[ 0 \] . A \[ 2\] |
| Bx    | endpt \[ 0 \] . B \[ 2\] |
| by    | endpt \[ 1 \] . A \[ 2\] |
| Bz    | endpt \[ 1 \] . B \[ 2\] |



 

Endpt i , donde i es 0 o 1, hace referencia al \[ 0 o 1.º conjunto de puntos de \] conexión, respectivamente.

## <a name="sign-extension-for-endpoint-values"></a>Extensión de signo para valores de punto de conexión

Para los iconos de dos regiones, hay cuatro valores de punto de conexión que se pueden firmar extendidos. Endpt \[ 0 \] . Un solo se firma si el formato es un formato firmado; Los demás puntos de conexión solo se firman si el punto de conexión se transformó o si el formato es un formato firmado. El código siguiente muestra el algoritmo para extender el signo de valores de punto de conexión de dos regiones.

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

En el caso de los iconos de una región, el comportamiento es el mismo, solo con el punto \[ 1 \] eliminado.

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

## <a name="transform-inversion-for-endpoint-values"></a>Inversión de transformación para valores de punto de conexión

En el caso de los iconos de dos regiones, la transformación aplica la codificación inversa de la diferencia, agregando el valor base en el punto \[ final \] 0. a las otras tres entradas para un total de 9 operaciones de adición. En la imagen siguiente, el valor base se representa como "A0" y tiene la mayor precisión de punto flotante. "A1," "B0" y "B1" son deltas calculados a partir del valor delimitador y estos valores delta se representan con una precisión inferior. (A0 corresponde al punto final \[ \] 0. A, B0 corresponde al punto final \[ \] 0. B, A1 corresponde al punto \[ final \] 1. A y B1 corresponden al punto de conexión \[ 1 \] .B).

![cálculo de valores de punto de conexión de inversión de transformación](images/bc6h-transform-inverse.png)

En el caso de los iconos de una región, solo hay un desplazamiento diferencial y, por tanto, solo 3 operaciones de adición.

El descomprimidor debe asegurarse de que los resultados de la transformación inversa no desbordarán la precisión del punto \[ final 0 \] .a. En el caso de un desbordamiento, los valores resultantes de la transformación inversa deben ajustarse dentro del mismo número de bits. Si la precisión de A0 es "p", el algoritmo de transformación es:

`B0 = (B0 + A0) & ((1 << p) - 1)`

En el caso de los formatos firmados, los resultados del cálculo diferencial también deben ampliarse. Si la operación de extensión de signo considera extender ambos signos, donde 0 es positivo y 1 es negativo, la extensión de signo de 0 se encarga de la fijación anterior. De forma equivalente, después de la fijación anterior, solo es necesario extender un valor de 1 (negativo).

## <a name="unquantization-of-color-endpoints"></a>Descuantización de puntos de conexión de color

Dados los puntos de conexión sin comprimir, el siguiente paso consiste en realizar una eliminación de marca inicial de los puntos de conexión de color. Esto implica tres pasos:

-   Un descuantización de las paletas de colores
-   Interpolación de las paletas
-   Fin de la descontización

La separación del proceso de desquantización en dos partes (la desquantización de la paleta de colores antes de la interpolación y la desanquilación final después de la interpolación) reduce el número de operaciones de multiplicación necesarias en comparación con un proceso de desquantización completo antes de la interpolación de la paleta.

El código siguiente muestra el proceso para recuperar estimaciones de los valores de color originales de 16 bits y, a continuación, usar los valores de peso proporcionados para agregar 6 valores de color adicionales a la paleta. La misma operación se realiza en cada canal.

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

En el ejemplo de código siguiente se muestra el proceso de interpolación, con las siguientes observaciones:

-   Puesto que el intervalo completo de valores de color para la función **unquantize** (a continuación) va de -32768 a 65535, el interpolador se implementa mediante aritmética con firma de 17 bits.
-   Después de la interpolación, los valores se pasan a la función **finish \_ unquantize** (descrita en el tercer ejemplo de esta sección), que aplica el escalado final.
-   Todos los descompresores de hardware son necesarios para devolver resultados con precisión de bits con estas funciones.

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

**Se llama a finish \_ unquantize** después de la interpolación de la paleta. La **función unquantize** pospone el escalado en 31/32 para signed, 31/64 para unsigned. Este comportamiento es necesario para obtener el valor final en un intervalo medio válido (-0x7BFF ~ 0x7BFF) una vez completada la interpolación de la paleta con el fin de reducir el número de multiplicaciones necesarias. **finish \_ unquantize** aplica el escalado final y devuelve **un** valor corto sin signo que se reinterpreta a la **mitad.**

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

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compresión de bloques de textura en Direct3D 11](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 