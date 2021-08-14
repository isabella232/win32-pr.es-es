---
description: La compresión de bloques es una técnica de compresión de textura para reducir el tamaño de la textura.
ms.assetid: add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5
title: Compresión de bloques (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edf93a9d475b21b54baa59f9324a7f69b043bb0c21787c0c2892bfdbe2f6c66d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101304"
---
# <a name="block-compression-direct3d-10"></a>Compresión de bloques (Direct3D 10)

La compresión de bloques es una técnica de compresión de textura para reducir el tamaño de la textura. En comparación con una textura con 32 bits por color, una textura comprimida por bloques puede ser hasta un 75 % más pequeña. Las aplicaciones suelen ver un aumento del rendimiento al usar la compresión de bloques debido a la menor superficie de memoria.

Aunque la pérdida, la compresión de bloques funciona bien y se recomienda para todas las texturas que la canalización transforma y filtra. Las texturas que se asignan directamente a la pantalla (elementos de la interfaz de usuario como iconos y texto) no son buenas opciones para la compresión porque los artefactos son más evidentes.

Una textura comprimida en bloque debe crearse como un múltiplo de tamaño 4 en todas las dimensiones y no se puede usar como salida de la canalización.

-   [¿Cómo funciona la compresión de bloques?](#how-does-block-compression-work)
    -   [Almacenamiento de datos sin comprimir](#storing-uncompressed-data)
    -   [Almacenamiento de datos comprimidos](#storing-compressed-data)
-   [Uso de la compresión de bloques](#using-block-compression)
    -   [Tamaño virtual frente a tamaño físico](#virtual-size-versus-physical-size)
-   [Algoritmos de compresión](#compression-algorithms)
    -   [BC1](#bc1)
    -   [BC2](#bc2)
    -   [BC3](#bc3)
    -   [BC4](#bc4)
    -   [BC5](#bc5)
-   [Conversión de formato mediante Direct3D 10.1](#format-conversion-using-direct3d-101)
-   [Temas relacionados](#related-topics)

## <a name="how-does-block-compression-work"></a>¿Cómo funciona la compresión de bloques?

La compresión de bloques es una técnica para reducir la cantidad de memoria necesaria para almacenar datos de color. Al almacenar algunos colores en su tamaño original y otros colores mediante un esquema de codificación, puede reducir drásticamente la cantidad de memoria necesaria para almacenar la imagen. Puesto que el hardware descodifica automáticamente los datos comprimidos, no hay ninguna penalización de rendimiento para el uso de texturas comprimidas.

Para ver cómo funciona la compresión, consulte los dos ejemplos siguientes. En el primer ejemplo se describe la cantidad de memoria utilizada al almacenar datos sin comprimir; En el segundo ejemplo se describe la cantidad de memoria utilizada al almacenar datos comprimidos.

### <a name="storing-uncompressed-data"></a>Almacenamiento de datos sin comprimir

En la ilustración siguiente se representa una textura 4×4 sin comprimir. Suponga que cada color contiene un único componente de color (rojo por ejemplo) y se almacena en un byte de memoria.

![ilustración de una textura 4x4 sin comprimir](images/d3d10-block-compress-1.png)

Los datos sin comprimir se menten en memoria secuencialmente y requieren 16 bytes, como se muestra en la ilustración siguiente.

![ilustración de datos sin comprimir en memoria secuencial](images/d3d10-block-compress-2.png)

### <a name="storing-compressed-data"></a>Almacenamiento de datos comprimidos

Ahora que ha visto cuánta memoria usa una imagen sin comprimir, vea cuánta memoria guarda una imagen comprimida. El formato de compresión [BC4](#bc4) almacena 2 colores (1 byte cada uno) y 16 índices de 3 bits (48 bits o 6 bytes) que se usan para interpolar los colores originales de la textura, como se muestra en la ilustración siguiente.

![ilustración del formato de compresión bc4](images/d3d10-block-compress-3.png)

El espacio total necesario para almacenar los datos comprimidos es de 8 bytes, lo que significa un ahorro de memoria del 50 por ciento con respecto al ejemplo sin comprimir. El ahorro es incluso mayor cuando se usa más de un componente de color.

El ahorro sustancial de memoria que proporciona la compresión de bloques puede dar lugar a un aumento del rendimiento. Este rendimiento se produce a costa de la calidad de la imagen (debido a la interpolación de colores). sin embargo, la calidad más baja a menudo no es perceptible.

En la sección siguiente se muestra cómo Direct3D 10 facilita el uso de la compresión de bloques en la aplicación.

## <a name="using-block-compression"></a>Uso de la compresión de bloques

Cree una textura comprimida en bloque igual que una textura sin comprimir (vea Crear una textura [a](d3d10-graphics-programming-guide-resources-creating-textures.md)partir de un archivo ), salvo que especifique un formato comprimido en bloques.


```
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;
D3DX10CreateTextureFromFile(...);
```



A continuación, cree una vista para enlazar la textura a la canalización. Puesto que una textura comprimida por bloques solo se puede usar como entrada para una fase de sombreador, quiere crear una vista de recursos de sombreador mediante una llamada a [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).

Use una textura comprimida de bloque de la misma manera que usaría una textura sin comprimir. Si la aplicación obtiene un puntero de memoria a los datos comprimidos en bloques, debe tener en cuenta el relleno de memoria en un mapa mipmap que hace que el tamaño declarado se difir de su tamaño real.

### <a name="virtual-size-versus-physical-size"></a>Tamaño virtual frente a tamaño físico

Si tiene código de aplicación que usa un puntero de memoria para recorrer la memoria de una textura comprimida de bloque, hay una consideración importante que puede requerir una modificación en el código de la aplicación. Una textura comprimida por bloques debe ser un múltiplo de 4 en todas las dimensiones porque los algoritmos de compresión de bloques funcionan en bloques de texel de 4x4. Esto será un problema para un mapa mip cuyas dimensiones iniciales son divisibles por 4, pero los niveles subdivididas no lo son. En el diagrama siguiente se muestra la diferencia de área entre el tamaño virtual (declarado) y el tamaño físico (real) de cada nivel de mapa mip.

![diagrama de niveles de asignación mipmap sin comprimir y comprimidos](images/d3d10-block-compress-pad.png)

El lado izquierdo del diagrama muestra los tamaños de nivel de mapa mip que se generan para una textura de 60×40 sin comprimir. El tamaño de nivel superior se toma de la llamada API que genera la textura; cada nivel posterior es la mitad del tamaño del nivel anterior. Para una textura sin comprimir, no hay ninguna diferencia entre el tamaño virtual (declarado) y el tamaño físico (real).

El lado derecho del diagrama muestra los tamaños de nivel de mapa mip que se generan para la misma textura de 60×40 con compresión. Observe que tanto el segundo como el tercer nivel tienen relleno de memoria para que los factores de tamaño de 4 en cada nivel. Esto es necesario para que los algoritmos puedan funcionar en bloques de 4×4 texel. Esto es evidente si se tienen en cuenta los niveles de mapa mip que son menores que 4×4; El tamaño de estos niveles de mapa mip muy pequeños se redondeará al factor más cercano de 4 cuando se asigne memoria de textura.

El hardware de muestreo usa el tamaño virtual; cuando se muestrea la textura, se omite el relleno de memoria. En el caso de los niveles de mapa mip que son menores que 4×4, solo se usarán los cuatro primeros elementos de textura para un mapa de 2×2 y solo un bloque 1×1 usará el primer texel. Sin embargo, no hay ninguna estructura de API que exponga el tamaño físico (incluido el relleno de memoria).

En resumen, tenga cuidado de usar bloques de memoria alineados al copiar regiones que contienen datos comprimidos en bloques. Para ello en una aplicación que obtiene un puntero de memoria, asegúrese de que el puntero usa el paso de superficie para tener en cuenta el tamaño de la memoria física.

## <a name="compression-algorithms"></a>Algoritmos de compresión

Las técnicas de compresión de bloques de Direct3D divide los datos de textura sin comprimir en 4×4 bloques, comprime cada bloque y, a continuación, almacena los datos. Por esta razón, se espera que las texturas se comprima deben tener dimensiones de textura que sean múltiplo de 4.

![diagrama de compresión de bloques](images/d3d10-compression-1.png)

En el diagrama anterior se muestra una textura particionada en bloques de texel. El primer bloque muestra el diseño de los 16 elementos de textura etiquetados como a-p, pero cada bloque tiene la misma organización de datos.

Direct3D implementa varios esquemas de compresión, cada uno implementa un equilibrio diferente entre el número de componentes almacenados, el número de bits por componente y la cantidad de memoria consumida. Use esta tabla para ayudar a elegir el formato que mejor funcione con el tipo de datos y la resolución de datos que mejor se adapte a su aplicación.



| Datos de origen                     | Resolución de compresión de datos (en bits) | Elegir este formato de compresión |
|---------------------------------|---------------------------------------|--------------------------------|
| Color de tres componentes y alfa | Color (5:6:5), Alfa (1) o ningún alfa  | BC1                            |
| Color de tres componentes y alfa | Color (5:6:5), Alfa (4)              | [BC2](#bc2)                    |
| Color de tres componentes y alfa | Color (5:6:5), Alfa (8)              | [BC3](#bc3)                    |
| Color de un componente             | Un componente (8)                     | [BC4](#bc4)                    |
| Color de dos componentes             | Dos componentes (8:8)                  | [BC5](#bc5)                    |



 

### <a name="bc1"></a>BC1

Use el primer formato de compresión de bloque (BC1) (DXGI FORMAT BC1 TYPELESS, DXGI FORMAT BC1 UNORM o DXGI BC1 UNORM SRGB) para almacenar datos de color de tres componentes mediante un \_ \_ color de \_ \_ \_ \_ \_ \_ \_ 5:6:5 (5 bits rojo, 6 bits verde, 5 bits azul). Esto es así incluso si los datos también contienen alfa de 1 bit. Suponiendo una textura de 4×4 con el formato de datos más grande posible, el formato BC1 reduce la memoria necesaria de 48 bytes (16 colores × 3 componentes/color × 1 byte/componente) a 8 bytes de memoria.

El algoritmo funciona en bloques de 4 ×4 de elementos de textura. En lugar de almacenar 16 colores, el algoritmo guarda 2 colores de referencia (color 0 y color 1) y 16 índices de color de 2 bits \_ (bloques a–p), como se muestra en el \_ diagrama siguiente.

![diagrama del diseño para la compresión bc1](images/d3d10-compression-bc1.png)

Los índices de color (a–p) se usan para buscar los colores originales de una tabla de colores. La tabla de colores contiene 4 colores. Los dos primeros colores( color \_ 0 y color \_ 1) son los colores mínimo y máximo. Los otros dos colores, color 2 y color 3, son colores intermedios \_ \_ calculados con interpolación lineal.


```
color_2 = 2/3*color_0 + 1/3*color_1
color_3 = 1/3*color_0 + 2/3*color_1
```



A los cuatro colores se les asignan valores de índice de 2 bits que se guardarán en bloques a–p.


```
color_0 = 00
color_1 = 01
color_2 = 10
color_3 = 11
```



Por último, cada uno de los colores de los bloques a–p se compara con los cuatro colores de la tabla de colores y el índice del color más cercano se almacena en los bloques de 2 bits.

Este algoritmo se presta a los datos que también contienen alfa de 1 bit. La única diferencia es que el color 3 se establece en 0 (que representa un color transparente) y el color 2 es una mezcla lineal de color 0 y \_ \_ color \_ \_ 1.


```
color_2 = 1/2*color_0 + 1/2*color_1;
color_3 = 0;
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 10:<br/> Este formato existe tanto en Direct3D 9 como en 10.<br/>
<ul>
<li>En Direct3D 9, el formato BC1 se denomina D3DFMT_DXT1.</li>
<li>En Direct3D 10, el formato BC1 se representa mediante DXGI_FORMAT_BC1_UNORM o DXGI_FORMAT_BC1_UNORM_SRGB.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc2"></a>BC2

Use el formato BC2 (DXGI \_ FORMAT \_ BC2 \_ TYPELESS, DXGI \_ FORMAT BC2 UNORM o \_ \_ DXGI \_ BC2 \_ UNORM SRGB) \_ [](#bc3) para almacenar datos que contengan datos de color y alfa con baja coherencia (use BC3 para datos alfa altamente coherentes). El formato BC2 almacena los datos RGB como un color de 5:6:5 (5 bits rojos, 6 bits verdes, 5 bits azules) y alfa como un valor de 4 bits independiente. Suponiendo que una textura de 4×4 usa el formato de datos más grande posible, esta técnica de compresión reduce la memoria necesaria de 64 bytes (16 colores × 4 componentes/color × 1 byte/componente) a 16 bytes de memoria.

El formato BC2 almacena colores con el mismo número de bits y diseño de datos que el [formato BC1;](#bc1) sin embargo, BC2 requiere 64 bits de memoria adicionales para almacenar los datos alfa, como se muestra en el diagrama siguiente.

![diagrama del diseño para la compresión bc2](images/d3d10-compression-bc2.png)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 10:<br/> Este formato existe tanto en Direct3D 9 como en 10.<br/>
<ul>
<li>En Direct3D 9, el formato BC2 se denomina D3DFMT_DXT2 y D3DFMT_DXT3.</li>
<li>En Direct3D 10, el formato BC2 se representa mediante DXGI_FORMAT_BC2_UNORM o DXGI_FORMAT_BC2_UNORM_SRGB.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc3"></a>BC3

Use el formato BC3 (DXGI \_ FORMAT \_ BC3 \_ TYPELESS, DXGI \_ FORMAT BC3 UNORM o \_ \_ DXGI \_ BC3 \_ UNORM SRGB) \_ [](#bc2) para almacenar datos de color altamente coherentes (use BC2 con datos alfa menos coherentes). El formato BC3 almacena datos de color con datos alfa de 5:6:5 (5 bits rojos, 6 bits verdes, 5 bits azules) y alfa con un byte. Suponiendo que una textura de 4×4 usa el formato de datos más grande posible, esta técnica de compresión reduce la memoria necesaria de 64 bytes (16 colores × 4 componentes/color × 1 byte/componente) a 16 bytes de memoria.

El formato BC3 almacena colores con el mismo número de bits y diseño de datos que el [formato BC1;](#bc1) sin embargo, BC3 requiere 64 bits de memoria adicionales para almacenar los datos alfa. El formato BC3 controla el alfa almacenando dos valores de referencia e interpolando entre ellos (de forma similar a cómo BC1 almacena el color RGB).

El algoritmo funciona en bloques × 4 de elementos de textura. En lugar de almacenar 16 valores alfa, el algoritmo almacena 2 alfas de referencia (alfa 0 y alfa 1) y 16 índices de color de 3 bits (alfa a a p), como se muestra en el \_ \_ diagrama siguiente.

![diagrama del diseño para la compresión bc3](images/d3d10-compression-bc3.png)

El formato BC3 usa los índices alfa (a–p) para buscar los colores originales de una tabla de búsqueda que contiene 8 valores. Los dos primeros valores(alfa 0 y alfa 1) son los valores mínimo y máximo; los otros seis valores intermedios se \_ \_ calculan mediante interpolación lineal.

El algoritmo determina el número de valores alfa interpolados examinando los dos valores alfa de referencia. Si alpha \_ 0 es mayor que alpha 1, BC3 interpola 6 valores alfa; de lo \_ contrario, interpola 4. Cuando BC3 interpola solo 4 valores alfa, establece dos valores alfa adicionales (0 para totalmente transparente y 255 para totalmente opacos). BC3 comprime los valores alfa en el área de textura 4×4 almacenando el código de bits correspondiente a los valores alfa interpolados que más se corresponden con el alfa original para un texel determinado.


```
if( alpha_0 > alpha_1 )
{
  // 6 interpolated alpha values.
  alpha_2 = 6/7*alpha_0 + 1/7*alpha_1; // bit code 010
  alpha_3 = 5/7*alpha_0 + 2/7*alpha_1; // bit code 011
  alpha_4 = 4/7*alpha_0 + 3/7*alpha_1; // bit code 100
  alpha_5 = 3/7*alpha_0 + 4/7*alpha_1; // bit code 101
  alpha_6 = 2/7*alpha_0 + 5/7*alpha_1; // bit code 110
  alpha_7 = 1/7*alpha_0 + 6/7*alpha_1; // bit code 111
}
else
{
  // 4 interpolated alpha values.
  alpha_2 = 4/5*alpha_0 + 1/5*alpha_1; // bit code 010
  alpha_3 = 3/5*alpha_0 + 2/5*alpha_1; // bit code 011
  alpha_4 = 2/5*alpha_0 + 3/5*alpha_1; // bit code 100
  alpha_5 = 1/5*alpha_0 + 4/5*alpha_1; // bit code 101
  alpha_6 = 0;                         // bit code 110
  alpha_7 = 255;                       // bit code 111
}
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 10:<br/>
<ul>
<li>En Direct3D 9, el formato BC3 se denomina D3DFMT_DXT4 y D3DFMT_DXT5.</li>
<li>En Direct3D 10, el formato BC3 se representa mediante DXGI_FORMAT_BC3_UNORM o DXGI_FORMAT_BC3_UNORM_SRGB.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc4"></a>BC4

Use el formato BC4 para almacenar datos de color de un componente con 8 bits para cada color. Como resultado de la mayor precisión (en comparación con [BC1), BC4](#bc1)es ideal para almacenar datos de punto flotante en el intervalo de 0 a 1 mediante el formato DXGI FORMAT BC4 UNORM y -1 a +1 con el formato \[ \] \_ \_ \_ \[ \] DXGI \_ FORMAT \_ BC4 \_ SNORM. Suponiendo que una textura de 4×4 usa el formato de datos más grande posible, esta técnica de compresión reduce la memoria necesaria de 16 bytes (16 colores × 1 componentes/color × 1 byte/componente) a 8 bytes.

El algoritmo funciona en bloques × 4 de elementos de textura. En lugar de almacenar 16 colores, el algoritmo almacena 2 colores de referencia (rojo 0 y rojo 1) y 16 índices de color de 3 bits (rojo a a rojo p), como se muestra en el \_ \_ diagrama siguiente.

![diagrama del diseño para la compresión bc4](images/d3d10-compression-bc4.png)

El algoritmo usa los índices de 3 bits para buscar colores de una tabla de colores que contiene 8 colores. Los dos primeros \_ colores(rojo 0 y \_ rojo 1) son los colores mínimo y máximo. El algoritmo calcula los colores restantes mediante la interpolación lineal.

El algoritmo determina el número de valores de color interpolados examinando los dos valores de referencia. Si rojo 0 es mayor que rojo 1, BC4 interpola 6 valores de color; de lo \_ \_ contrario, interpola 4. Cuando BC4 interpola solo 4 valores de color, establece dos valores de color adicionales (0,0f para totalmente transparente y 1,0f para totalmente opacos). BC4 comprime los valores alfa del área de texel 4×4 almacenando el código de bits correspondiente a los valores alfa interpolados que más se corresponden con el alfa original para un texel determinado.

-   [BC4 \_ UNORM](/windows)
-   [BC4 \_ SNORM](/windows)

### <a name="bc4_unorm"></a>BC4 \_ UNORM

La interpolación de los datos de un solo componente se realiza como en el ejemplo de código siguiente.


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



A los colores de referencia se les asignan índices de 3 bits (de 000 a 111, ya que hay 8 valores), que se guardarán en bloques rojos a a p rojos durante la compresión.

### <a name="bc4_snorm"></a>BC4 \_ SNORM

DXGI FORMAT BC4 SNORM es exactamente igual, salvo que los datos están codificados en el intervalo SNORM y cuando \_ \_ se \_ interpolan 4 valores de color. La interpolación de los datos de un solo componente se realiza como en el ejemplo de código siguiente.


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                     // bit code 110
  red_7 =  1.0f;                     // bit code 111
}
```



A los colores de referencia se les asignan índices de 3 bits (de 000 a 111, ya que hay 8 valores), que se guardarán en bloques rojos a a p rojos durante la compresión.

### <a name="bc5"></a>BC5

Use el formato BC5 para almacenar datos de color de dos componentes con 8 bits para cada color. Como resultado de la mayor precisión (en comparación con [BC1), BC5](#bc1)es ideal para almacenar datos de punto flotante en el intervalo de 0 a 1 mediante el formato DXGI FORMAT BC5 UNORM y -1 a +1 mediante el formato \[ \] \_ \_ \_ \[ \] DXGI \_ FORMAT \_ BC5 \_ SNORM. Suponiendo que una textura de 4×4 usa el formato de datos más grande posible, esta técnica de compresión reduce la memoria necesaria de 32 bytes (16 colores × 2 componentes/color × 1 byte/componente) a 16 bytes.

El algoritmo funciona en bloques × 4 de elementos de textura. En lugar de almacenar 16 colores para ambos componentes, el algoritmo almacena 2 colores de referencia para cada componente (rojo \_ 0, rojo 1, verde 0 y verde \_ \_ 1) y 16 índices de color de 3 bits para cada componente (rojo a a p rojo y verde de a a verde p), como se muestra en el \_ diagrama siguiente.

![diagrama del diseño para la compresión bc5](images/d3d10-compression-bc5.png)

El algoritmo usa los índices de 3 bits para buscar colores de una tabla de colores que contiene 8 colores. Los dos primeros colores,rojo 0 y \_ rojo \_ 1 (o verde 0 y verde \_ 1) son los colores mínimo \_ y máximo. El algoritmo calcula los colores restantes mediante la interpolación lineal.

El algoritmo determina el número de valores de color interpolados examinando los dos valores de referencia. Si rojo 0 es mayor que rojo 1, BC5 interpola 6 valores de color; de lo \_ \_ contrario, interpola 4. Cuando BC5 interpola solo 4 valores de color, establece los dos valores de color restantes en 0,0f y 1,0f.

-   [BC5 \_ UNORM](/windows)
-   [BC5 \_ SNORM](/windows)

### <a name="bc5_unorm"></a>BC5 \_ UNORM

La interpolación de los datos de un solo componente se realiza como en el ejemplo de código siguiente. Los cálculos de los componentes verdes son similares.


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



A los colores de referencia se les asignan índices de 3 bits (de 000 a 111, ya que hay 8 valores), que se guardarán en bloques rojos a a p rojos durante la compresión.

### <a name="bc5_snorm"></a>BC5 \_ SNORM

DXGI FORMAT BC5 SNORM es exactamente igual, salvo que los datos están codificados en el intervalo SNORM y cuando se interpolan 4 valores de datos, los dos valores adicionales son \_ \_ \_ -1.0f y 1.0f. La interpolación de los datos de un solo componente se realiza como en el ejemplo de código siguiente. Los cálculos de los componentes verdes son similares.


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                    // bit code 110
  red_7 =  1.0f;                    // bit code 111
}
```



A los colores de referencia se les asignan índices de 3 bits (de 000 a 111, ya que hay 8 valores), que se guardarán en bloques rojos a a p rojos durante la compresión.

## <a name="format-conversion-using-direct3d-101"></a>Conversión de formato mediante Direct3D 10.1

Direct3D 10.1 habilita copias entre texturas con tipo estructurado previamente y texturas comprimidas en bloques de los mismos anchos de bits. Las funciones que pueden lograr esto son [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) y [**CopySubresourceRegion.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)

A partir de Direct3D 10.1, puede usar [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) y [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) para copiar entre algunos tipos de formato. Este tipo de operación de copia realiza un tipo de conversión de formato que reinterpreta los datos de recursos como un tipo de formato diferente. Considere este ejemplo que muestra la diferencia entre la reinterpretación de datos con la forma en que se comporta un tipo de conversión más típico:


```
    FLOAT32 f = 1.0f;
    UINT32 u;
```



Para reinterpretar 'f' como el tipo de 'u', use [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):


```
    memcpy( &u, &f, sizeof( f ) ); // ‘u’ becomes equal to 0x3F800000.
```



En la reinterpretación anterior, el valor subyacente de los datos no cambia; [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) reinterpreta float como un entero sin signo.

Para realizar el tipo de conversión más típico, use asignación:


```
    u = f; // ‘u’ becomes 1.
```



En la conversión anterior, cambia el valor subyacente de los datos.

En la tabla siguiente se enumeran los formatos de origen y destino permitidos que puede usar en este tipo de reinterpretación de conversión de formato. Debe codificar los valores correctamente para que la reinterpretación funcione según lo previsto.



| Ancho de bits | Recurso sin comprimir                                                                                                                                               | Block-Compressed recurso                                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 32        | DXGI \_ FORMAT \_ R32 \_ UINT<br/> DXGI \_ FORMAT \_ R32 \_ SINT<br/>                                                                                               | FORMATO DXGI \_ \_ R9G9B9E5 \_ SHAREDEXP                                                                                                                                   |
| 64        | DXGI \_ FORMAT \_ R16G16B16A16 \_ UINT<br/> DXGI \_ FORMAT \_ R16G16B16A16 \_ SINT<br/> DXGI \_ FORMAT \_ R32G32 \_ UINT<br/> DXGI \_ FORMAT \_ R32G32 \_ SINT<br/> | DXGI \_ FORMAT \_ BC1 \_ UNORM \[ \_ SRGB\]<br/> DXGI \_ FORMAT \_ BC4 \_ UNORM<br/> DXGI \_ FORMAT \_ BC4 \_ SNORM<br/>                                               |
| 128       | DXGI \_ FORMAT \_ R32G32B32A32 \_ UINT<br/> DXGI \_ FORMAT \_ R32G32B32A32 \_ SINT<br/>                                                                             | DXGI \_ FORMAT \_ BC2 \_ UNORM \[ \_ SRGB\]<br/> DXGI \_ FORMAT \_ BC3 \_ UNORM \[ \_ SRGB\]<br/> DXGI \_ FORMAT \_ BC5 \_ UNORM<br/> DXGI \_ FORMAT \_ BC5 \_ SNORM<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
