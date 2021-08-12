---
description: Hay dos maneras de codificar mapas de textura que muestran una transparencia más compleja.
ms.assetid: cae788f6-60f1-4987-8f06-bf4256bccd9b
title: Texturas con canales alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 934660a62c0257de1549ccec09f9bb77e5c02c4c22baf1e1dc9cc8dffef03f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290535"
---
# <a name="textures-with-alpha-channels-direct3d-9"></a>Texturas con canales alfa (Direct3D 9)

Hay dos maneras de codificar mapas de textura que muestran una transparencia más compleja. En cada caso, un bloque que describe la transparencia precede al bloque de 64 bits ya descrito. La transparencia se representa como un mapa de bits de 4x4 con 4 bits por píxel (codificación explícita) o con menos bits e interpolación lineal que es análoga a lo que se usa para la codificación de color.

El bloque de transparencia y el bloque de colores se organizan como se muestra en la tabla siguiente.



| Dirección de word | Bloque de 64 bits                      |
|--------------|-----------------------------------|
| 3:0          | Bloque de transparencia                |
| 7:4          | Bloque de 64 bits descrito anteriormente |



 

## <a name="explicit-texture-encoding"></a>Codificación de textura explícita

Para la codificación de textura explícita (formatos DXT2 y DXT3), los componentes alfa de los elementos de textura que describen la transparencia se codifican en un mapa de bits de 4x4 con 4 bits por texel. Estos cuatro bits se pueden lograr a través de diversos medios, como la dithering o mediante los cuatro bits más significativos de los datos alfa. Sin embargo, se generan, se usan tal y como están, sin ninguna forma de interpolación.

En el diagrama siguiente se muestra un bloque de transparencia de 64 bits.

![diagrama de un bloque de transparencia de 64 bits](images/colors4.png)

> [!Note]  
> El método de compresión de Direct3D usa los cuatro bits más significativos.

 

En las tablas siguientes se muestra cómo se dispone la información alfa en memoria para cada palabra de 16 bits.

Esta tabla contiene el diseño de la palabra 0.



| Bits          | Alpha      |
|---------------|------------|
| 3:0 (LSB \* )   | \[0 \] \[ 0\] |
| 7:4           | \[0 \] \[ 1\] |
| 11:8          | \[0 \] \[ 2\] |
| 15:12 (MSB) \* | \[0 \] \[ 3\] |



 

\*bit menos significativo, bit más significativo (MSB)

Esta tabla contiene el diseño de la palabra 1.



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[1 \] \[ 0\] |
| 7:4         | \[1 \] \[ 1\] |
| 11:8        | \[1 \] \[ 2\] |
| 15:12 (MSB) | \[1 \] \[ 3\] |



 

Esta tabla contiene el diseño de la palabra 2.



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[2 \] \[ 0\] |
| 7:4         | \[2 \] \[ 1\] |
| 11:8        | \[2 \] \[ 2\] |
| 15:12 (MSB) | \[2 \] \[ 3\] |



 

Esta tabla contiene el diseño de la palabra 3.



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[3 \] \[ 0\] |
| 7:4         | \[3 \] \[ 1\] |
| 11:8        | \[3 \] \[ 2\] |
| 15:12 (MSB) | \[3 \] \[ 3\] |



 

La diferencia entre DXT2 y DXT3 es que, en el formato DXT2, se supone que los datos de color se han multiplicado previamente por alfa. En el formato DXT3, se supone que el color no se multiplica previamente por alfa. Estos dos formatos son necesarios porque, en la mayoría de los casos, cuando se usa una textura, simplemente examinar los datos no es suficiente para determinar si los valores de color se han multiplicado por alfa. Dado que esta información es necesaria en tiempo de ejecución, se usan los dos códigos FOURCC para diferenciar estos casos. Sin embargo, los datos y el método de interpolación usados para estos dos formatos son idénticos.

La comparación de colores usada en DXT1 para determinar si el texel es transparente no se usa en este formato. Se supone que, sin la comparación de color, los datos de color siempre se tratan como si se tratara en modo de 4 colores. En otras palabras, la instrucción if en la parte superior del código DXT1 debe ser la siguiente:


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="three-bit-linear-alpha-interpolation"></a>Three-Bit interpolación alfa lineal

La codificación de transparencia para los formatos DXT4 y DXT5 se basa en un concepto similar a la codificación lineal usada para el color. Dos valores alfa de 8 bits y un mapa de bits de 4x4 con tres bits por píxel se almacenan en los primeros ocho bytes del bloque. Los valores alfa representativos se usan para interpolar valores alfa intermedios. Hay información adicional disponible en la forma en que se almacenan los dos valores alfa. Si alpha 0 es mayor que alpha 1, la interpolación crea seis valores \_ \_ alfa intermedios. De lo contrario, se interpolan cuatro valores alfa intermedios entre los extremos alfa especificados. Los dos valores alfa implícitos adicionales son 0 (totalmente transparente) y 255 (totalmente opacos).

En el ejemplo de código siguiente se muestra este algoritmo.


```
// 8-alpha or 6-alpha block?    
if (alpha_0 > alpha_1) {    
    // 8-alpha block:  derive the other six alphas.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (6 * alpha_0 + 1 * alpha_1 + 3) / 7;    // bit code 010
    alpha_3 = (5 * alpha_0 + 2 * alpha_1 + 3) / 7;    // bit code 011
    alpha_4 = (4 * alpha_0 + 3 * alpha_1 + 3) / 7;    // bit code 100
    alpha_5 = (3 * alpha_0 + 4 * alpha_1 + 3) / 7;    // bit code 101
    alpha_6 = (2 * alpha_0 + 5 * alpha_1 + 3) / 7;    // bit code 110
    alpha_7 = (1 * alpha_0 + 6 * alpha_1 + 3) / 7;    // bit code 111  
}    
else {  
    // 6-alpha block.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (4 * alpha_0 + 1 * alpha_1 + 2) / 5;    // Bit code 010
    alpha_3 = (3 * alpha_0 + 2 * alpha_1 + 2) / 5;    // Bit code 011
    alpha_4 = (2 * alpha_0 + 3 * alpha_1 + 2) / 5;    // Bit code 100
    alpha_5 = (1 * alpha_0 + 4 * alpha_1 + 2) / 5;    // Bit code 101
    alpha_6 = 0;                                      // Bit code 110
    alpha_7 = 255;                                    // Bit code 111
}
```



El diseño de memoria del bloque alfa es el siguiente:



| Byte | Alpha                                                          |
|------|----------------------------------------------------------------|
| 0    | Alfa \_ 0                                                       |
| 1    | Alfa \_ 1                                                       |
| 2    | \[0 \] \[ 2 \] (2 MSB), \[ 0 \] \[ 1 \] , \[ 0 \] \[ 0\]                    |
| 3    | \[1 \] \[ 1 \] (1 MSB), \[ 1 \] \[ \] 0, \[ 0 \] \[ \] 3, \[ 0 \] \[ 2 \] (1 LSB) |
| 4    | \[1 \] \[ \] 3, \[ 1 \] \[ \] 2, \[ 1 \] \[ 1 \] (2 LSB)                    |
| 5    | \[2 \] \[ 2 \] (2 MSB), \[ 2 \] \[ 1 \] , \[ 2 \] \[ 0\]                    |
| 6    | \[3 \] \[ 1 \] (1 MSB), \[ 3 \] \[ \] 0, \[ 2 \] \[ \] 3, \[ 2 \] \[ 2 \] (1 LSB) |
| 7    | \[3 \] \[ \] 3, \[ 3 \] \[ \] 2, \[ 3 \] \[ 1 \] (2 LSB)                    |



 

La diferencia entre DXT4 y DXT5 es que, en el formato DXT4, se supone que los datos de color se han multiplicado previamente por alfa. En el formato DXT5, se supone que el color no se multiplica previamente por alfa. Estos dos formatos son necesarios porque, en la mayoría de los casos, cuando se usa una textura, simplemente examinar los datos no es suficiente para determinar si los valores de color se han multiplicado por alfa. Dado que esta información es necesaria en tiempo de ejecución, se usan los dos códigos FOURCC para diferenciar estos casos. Sin embargo, los datos y el método de interpolación usados para estos dos formatos son idénticos.

La comparación de colores usada en DXT1 para determinar si el elemento texel es transparente no se usa con estos formatos. Se supone que, sin la comparación de colores, los datos de color siempre se tratan como si se tratara en modo de 4 colores. En otras palabras, la instrucción if en la parte superior del código DXT1 debe ser:


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de textura comprimidos](compressed-texture-resources.md)
</dt> </dl>

 

 



