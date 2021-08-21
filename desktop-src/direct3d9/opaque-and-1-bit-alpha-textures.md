---
description: El formato de textura DXT1 es para texturas opacas o con un único color transparente.
ms.assetid: a890ed0a-1f68-45b8-93cb-b621d1908d9f
title: Texturas opacas y alfa de 1 bit (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda620810e48cba519322f3f2426555443fb696f524f4fbe7752a8c7aaedba73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728182"
---
# <a name="opaque-and-1-bit-alpha-textures-direct3d-9"></a>Texturas opacas y alfa de 1 bit (Direct3D 9)

El formato de textura DXT1 es para texturas opacas o con un único color transparente.

Para cada bloque alfa opaco o de 1 bit, se almacenan dos valores de 16 bits (formato RGB 5:6:5) y un mapa de bits de 4x4 con 2 bits por píxel. Esto suma 64 bits para 16 elementos de textura o cuatro bits por texel. En el mapa de bits del bloque, hay 2 bits por texel para seleccionar entre los cuatro colores, dos de los cuales se almacenan en los datos codificados. Los otros dos colores se derivan de estos colores almacenados mediante interpolación lineal. Este diseño se muestra en el diagrama siguiente.

![diagrama del diseño de mapa de bits](images/colors1.png)

El formato alfa de 1 bit se distingue del formato opaco comparando los dos valores de color de 16 bits almacenados en el bloque. Se tratan como enteros sin signo. Si el primer color es mayor que el segundo, implica que solo se definen los elementos texel opacos. Esto significa que se usan cuatro colores para representar los elementos de textura. En la codificación de cuatro colores, hay dos colores derivados y los cuatro colores se distribuyen por igual en el espacio de colores RGB. Este formato es análogo al formato RGB 5:6:5. De lo contrario, para la transparencia alfa de 1 bit, se usan tres colores y el cuarto se reserva para representar los texturas transparentes.

En la codificación de tres colores, hay un color derivado y el cuarto código de 2 bits está reservado para indicar un texel transparente (información alfa). Este formato es análogo a RGBA 5:5:5:1, donde el bit final se usa para codificar la máscara alfa.

En el ejemplo de código siguiente se muestra el algoritmo para decidir si está seleccionada la codificación de tres o cuatro colores:


```
if (color_0 > color_1) 
{
    // Four-color block: derive the other two colors.    
    // 00 = color_0, 01 = color_1, 10 = color_2, 11 = color_3
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block.
    color_2 = (2 * color_0 + color_1 + 1) / 3;
    color_3 = (color_0 + 2 * color_1 + 1) / 3;
}    
else
{ 
    // Three-color block: derive the other color.
    // 00 = color_0,  01 = color_1,  10 = color_2,  
    // 11 = transparent.
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block. 
    color_2 = (color_0 + color_1) / 2;    
    color_3 = transparent;    

}
```



Se recomienda establecer los componentes RGBA del píxel de transparencia en cero antes de combinar.

En las tablas siguientes se muestra el diseño de memoria para el bloque de 8 bytes. Se supone que el primer índice corresponde a la coordenada Y y que el segundo corresponde a la coordenada x. Por ejemplo, Texel 1 2 hace referencia al píxel del mapa de \[ \] \[ textura en \] (x,y) = (2,1).

Esta tabla contiene el diseño de memoria para el bloque de 8 bytes (64 bits).



| Dirección de Word | Palabra de 16 bits    |
|--------------|----------------|
| 0            | Color \_ 0       |
| 1            | Color \_ 1       |
| 2            | Palabra de mapa \_ de bits 0 |
| 3            | Palabra de mapa \_ de bits 1 |



 

Color 0 y Color 1, los colores de los dos \_ \_ extremos, se establecen de la siguiente manera:



| Bits        | Color                 |
|-------------|-----------------------|
| 4:0 (LSB \* ) | Componente de color azul  |
| 10:5        | Componente de color verde |
| 15:11       | Componente de color rojo   |



 

\*bit menos significativo

Palabra de \_ mapa de bits 0 se ha diseñado de la siguiente manera:



| Bits          | Texel           |
|---------------|-----------------|
| 1:0 (LSB)     | Texel \[ 0 \] \[ 0\] |
| 3:2           | Texel \[ 0 \] \[ 1\] |
| 5:4           | Texel \[ 0 \] \[ 2\] |
| 7:6           | Texel \[ 0 \] \[ 3\] |
| 9:8           | Texel \[ 1 \] \[ 0\] |
| 11:10         | Texel \[ 1 \] \[ 1\] |
| 13:12         | Texel \[ 1 \] \[ 2\] |
| 15:14 (MSB \* ) | Texel \[ 1 \] \[ 3\] |



 

\*bit más significativo (MSB)

Palabra de \_ mapa de bits 1 se ha diseñado de la siguiente manera:



| Bits        | Texel           |
|-------------|-----------------|
| 1:0 (LSB)   | Texel \[ 2 \] \[ 0\] |
| 3:2         | Texel \[ 2 \] \[ 1\] |
| 5:4         | Texel \[ 2 \] \[ 2\] |
| 7:6         | Texel \[ 2 \] \[ 3\] |
| 9:8         | Texel \[ 3 \] \[ 0\] |
| 11:10       | Texel \[ 3 \] \[ 1\] |
| 13:12       | Texel \[ 3 \] \[ 2\] |
| 15:14 (MSB) | Texel \[ 3 \] \[ 3\] |



 

## <a name="example-of-opaque-color-encoding"></a>Ejemplo de codificación de color opaco

Como ejemplo de codificación opaca, suponga que los colores rojo y negro están en los extremos. El rojo es el \_ color 0 y el negro el \_ color 1. Hay cuatro colores interpolados que forman el degradado distribuido uniformemente entre ellos. Para determinar los valores del mapa de bits 4x4, se usan los cálculos siguientes:


```
00 ? color_0
01 ? color_1
10 ? 2/3 color_0 + 1/3 color_1
11 ? 1/3 color_0 + 2/3 color_1
```



A continuación, el mapa de bits se parece al diagrama siguiente.

![Diagrama que muestra el diseño de mapa de bits expandido.](images/colors2.png)

Este aspecto es similar a la siguiente serie ilustrada de colores.

> [!Note]  
> En una imagen, aparece un píxel (0,0) en la parte superior izquierda.

 

![ilustración de un degradado codificado opaco](images/redsquares.png)

## <a name="example-of-1-bit-alpha-encoding"></a>Ejemplo de codificación alfa de 1 bit

Este formato se selecciona cuando el entero de 16 bits sin signo, color 0, es menor que el entero de 16 bits sin \_ signo, color \_ 1. Un ejemplo de dónde se puede usar este formato son las hojas de un árbol, que se muestran en un cielo azul. Algunos elementos de textura se pueden marcar como transparentes, mientras que hay tres tonos de verde disponibles para las hojas. Dos colores corrigen los extremos y el tercero es un color interpolado.

La siguiente ilustración es un ejemplo de este tipo de imagen.

![ilustración de la codificación alfa de 1 bit](images/greenthing.png)

Tenga en cuenta que, cuando la imagen se muestra como blanca, el elemento texel se codificaría como transparente. Tenga en cuenta también que los componentes RGBA de los elementos de textura transparente deben establecerse en cero antes de combinar.

La codificación de mapa de bits para los colores y la transparencia se determina mediante los cálculos siguientes.


```
00 ? color_0
01 ? color_1
10 ? 1/2 color_0 + 1/2 color_1
11   ?   Transparent
```



A continuación, el mapa de bits se parece al diagrama siguiente.

![diagrama del diseño de mapa de bits expandido](images/colors3.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de textura comprimidos](compressed-texture-resources.md)
</dt> </dl>

 

 



