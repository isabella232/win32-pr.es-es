---
description: En las secciones siguientes se describe cómo Direct3D controla las conversiones entre tipos de datos.
ms.assetid: 454d3fd0-fc0f-46a9-925e-13f8e3c39f02
title: Reglas de conversión de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b5ba37305fb7cadc229a614b883519cf6c5f45
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626301"
---
# <a name="data-conversion-rules"></a>Reglas de conversión de datos

En las secciones siguientes se describe cómo Direct3D controla las conversiones entre tipos de datos.

-   [Terminología de tipos de datos](#data-type-terminology)
-   [Conversión de punto flotante](#floating-point-conversion)
    -   [Conververso de una representación de intervalo superior a una representación de intervalo inferior](#conververting-from-a-higher-range-representation-to-a-lower-range-representation)
    -   [Conversión de una representación de intervalo inferior a una representación de intervalo superior](#converting-from-a-lower-range-representation-to-a-higher-range-representation)
-   [Conversión de enteros](#integer-conversion)
-   [Conversión de entero de punto fijo](#fixed-point-integer-conversion)
-   [Temas relacionados](#related-topics)

## <a name="data-type-terminology"></a>Terminología de tipos de datos

Posteriormente, se usa el siguiente conjunto de términos para caracterizar varias conversiones de formato.



| Término  | Definición                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNORM | Entero normalizado con signo, lo que significa que para un número de complemento de n bits 2, el valor máximo significa 1,0f (por ejemplo, el valor de 5 bits 01111 se asigna a 1,0f) y el valor mínimo significa -1,0f (por ejemplo, el valor de 5 bits 10000 se asigna a -1,0f). Además, el segundo número mínimo se asigna a -1,0f (por ejemplo, el valor de 5 bits 10001 se asigna a -1,0f). Por lo tanto, hay dos representaciones de entero para -1,0f. Hay una única representación para 0,0f y una representación única para 1,0f. Esto da como resultado un conjunto de representaciones de enteros para los valores de punto flotante espaciados uniformemente en el intervalo (-1,0f... 0,0f) y también un conjunto complementario de representaciones para los números del intervalo (0,0f... 1.0f) |
| UNORM | Entero normalizado sin signo, lo que significa que para un número de n bits, todos los 0 significan 0,0f y los 1 significan 1,0f. Se representa una secuencia de valores de punto flotante espaciados uniformemente de 0,0f a 1,0f. Por ejemplo, una UNORM de 2 bits representa 0,0f, 1/3, 2/3 y 1,0f.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SINT  | Entero con signo. Entero de complemento de 2. Por ejemplo, un SINT de 3 bits representa los valores enteros -4, -3, -2, -1, 0, 1, 2, 3.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| UINT  | Entero sin signo. Por ejemplo, un UINT de 3 bits representa los valores enteros 0, 1, 2, 3, 4, 5, 6, 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| FLOAT | Valor de punto flotante en cualquiera de las representaciones definidas por Direct3D.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| SRGB  | De forma similar a UNORM, en que para un número de n bits, los 0 significan 0,0f y los 1 significan 1,0f. Sin embargo, a diferencia de UNORM, con SRGB, la secuencia de codificaciones de enteros sin signo entre los 0 y los 1 representa una progresión no lineal en la interpretación de punto flotante de los números, entre 0,0f y 1,0f. Aproximadamente, si esta progresión no lineal, SRGB, se muestra como una secuencia de colores, aparecería como una rampa lineal de niveles de luminosidad a un observador "promedio", en condiciones de visualización "medias", en una presentación "media". Para más información, consulte el estándar de color SRGB IEC 61996-2-1 en IEC (Comisión electrotécnica internacional (CEI)).                |



 

## <a name="floating-point-conversion"></a>Conversión de punto flotante

Cada vez que se produce una conversión de punto flotante entre diferentes representaciones, incluidas las representaciones de punto flotante hacia o desde ellas, se aplican las reglas siguientes.

### <a name="conververting-from-a-higher-range-representation-to-a-lower-range-representation"></a>Conververso de una representación de intervalo superior a una representación de intervalo inferior

-   Se usa round-to-zero durante la conversión a otro formato float. Si el destino es un formato entero o de punto fijo, se usa round-to-nearest-even, a menos que la conversión se documente explícitamente como usar otro comportamiento de redondeo, como round-to-nearest para FLOAT a SNORM, FLOAT a UNORM o FLOAT a SRGB. Otras excepciones son las instrucciones del sombreador ftoi y ftou, que usan round-to-zero. Por último, las conversiones float a fixed usadas por el muestreador de textura y el rasterizador tienen una tolerancia especificada medida en Unit-Last-Place desde un ideal infinitamente preciso.
-   Para valores de origen mayores que el intervalo dinámico de un formato de destino de intervalo inferior (por ejemplo, Un valor float grande de 32 bits se escribe en un elemento RenderTarget float de 16 bits, el valor máximo que se puede representar (firmado correctamente), SIN incluir infinito con firma (debido a la ronda a cero descrita anteriormente).
-   NaN en un formato de intervalo superior se convertirá a la representación NaN en el formato de intervalo inferior si la representación naN existe en el formato de intervalo inferior. Si el formato inferior no tiene una representación NaN, el resultado será 0.
-   INF en un formato de intervalo superior se convertirá a INF en el formato de intervalo inferior si está disponible. Si el formato inferior no tiene una representación INF, se convertirá al valor máximo que se puede representar. El signo se conservará si está disponible en el formato de destino.
-   El desnormado en un formato de intervalo superior se convertirá a la representación Denorm en el formato de intervalo inferior si está disponible en el formato de intervalo inferior y la conversión es posible; de lo contrario, el resultado es 0. El bit de signo se conservará si está disponible en el formato de destino.

### <a name="converting-from-a-lower-range-representation-to-a-higher-range-representation"></a>Conversión de una representación de intervalo inferior a una representación de intervalo superior

-   NaN en un formato de intervalo inferior se convertirá a la representación NaN en el formato de intervalo superior si está disponible en el formato de intervalo superior. Si el formato de intervalo superior no tiene una representación NaN, se convertirá a 0.
-   INF en un formato de intervalo inferior se convertirá a la representación INF en el formato de intervalo superior si está disponible en el formato de intervalo superior. Si el formato superior no tiene una representación INF, se convertirá al valor máximo que se puede representar (MAX \_ FLOAT en ese formato). El signo se conservará si está disponible en el formato de destino.
-   El desnorma en un formato de intervalo inferior se convertirá en una representación normalizada en el formato de intervalo superior si es posible, o en una representación Denorm en el formato de intervalo superior si existe la representación Denorm. Si no lo hace, si el formato de intervalo superior no tiene una representación Denorm, se convertirá a 0. El signo se conservará si está disponible en el formato de destino. Tenga en cuenta que los números flotantes de 32 bits cuentan como un formato sin una representación Denorm (porque Denorms en operaciones en flotantes de 32 bits se vacían para firmar 0 conservado).

## <a name="integer-conversion"></a>Conversión de enteros

En la tabla siguiente se describen las conversiones de varias representaciones descritas anteriormente a otras representaciones. Solo se muestran las conversiones que se producen realmente en Direct3D.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de datos de origen</th>
<th>Tipo de datos de destino</th>
<th>Regla de conversión</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SNORM</td>
<td>FLOAT</td>
<td>Dado un valor entero de n bits que representa el intervalo con signo [-1.0f a 1.0f], la conversión a punto flotante es la siguiente.<br/>
<ul>
<li>El valor más negativo se asigna a -1,0f. Por ejemplo, el valor 10000 de 5 bits se asigna a -1,0f.</li>
<li>Todos los demás valores se convierten en un valor float (lo llaman c) y, a continuación, result = c * (1,0f / (2⁽ⁿ⁾-1)). Por ejemplo, el valor 10001 de 5 bits se convierte en -15.0f y, a continuación, se divide entre 15.0f, lo que produce -1.0f.</li>
</ul></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>SNORM</td>
<td>Dado un número de punto flotante, la conversión a un valor entero de n bits que representa el intervalo con signo [-1.0f a 1.0f] es la siguiente.<br/>
<ul>
<li>Deje que c represente el valor inicial.</li>
<li>Si c es NaN, el resultado es 0.</li>
<li>Si c > 1.0f, incluido INF, se fija a 1.0f.</li>
<li>Si c < -1.0f, incluido -INF, se fija a -1.0f.</li>
<li>Conversión de la escala float a la escala de enteros: c = c * (2ⁿ,¹-1).</li>
<li>Convierta en un entero como se muestra a continuación.
<ul>
<li>Si c >= 0, c = c + 0,5f; de lo contrario, c = c - 0,5f.</li>
<li>Coloque la fracción decimal y el valor de punto flotante restante (entero) se convertirá directamente en un entero.</li>
</ul></li>
</ul>
Esta conversión se permite con una tolerancia de D3D xx _FLOAT32_TO_INTEGER_TOLERANCE_IN_Unit-Last-Place Unit-Last-Place (en el lado entero).<em></em> Esto significa que, después de convertir la escala float a la escala de enteros, cualquier valor de D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place de un valor de formato de destino representable puede asignarse a ese valor. El requisito de inversión de datos adicional garantiza que la conversión no disminuya en todo el intervalo y que todos los valores de salida sean alcanzables. (En las constantes que se muestran aquí, <em>xx</em> debe reemplazarse por la versión de Direct3D, por ejemplo, 10, 11 o 12).<br/></td>
</tr>
<tr class="odd">
<td>UNORM</td>
<td>FLOAT</td>
<td>El valor inicial de n bits se convierte en float (0.0f, 1.0f, 2.0f, etc.) y, a continuación, se divide por (2ⁿ-1).<br/></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>UNORM</td>
<td>Deje que c represente el valor inicial.<br/>
<ul>
<li>Si c es NaN, el resultado es 0.</li>
<li>Si c > 1.0f, incluido INF, se fija a 1.0f.</li>
<li>Si c < 0.0f, incluido -INF, se fija a 0.0f.</li>
<li>Conversión de la escala float a la escala de enteros: c = c * (2ⁿ-1).</li>
<li>Convertir en entero.
<ul>
<li>c = c + 0,5f.</li>
<li>Se descarta la fracción decimal y el valor de punto flotante restante (entero) se convierte directamente en un entero.</li>
</ul></li>
</ul>
Esta conversión se permite con una tolerancia de D3D<em>xx _FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP</em>Unit-Last-Place (en el lado entero). Esto significa que, después de convertir la escala float a la escala de enteros, cualquier valor de D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place de un valor de formato de destino representable puede asignarse a ese valor. El requisito de inversión de datos adicional garantiza que la conversión no disminuya en todo el intervalo y que todos los valores de salida sean alcanzables.<br/></td>
</tr>
<tr class="odd">
<td>SRGB</td>
<td>FLOAT</td>
<td>A continuación se muestra la conversión ideal de SRGB a FLOAT.<br/>
<ul>
<li>Tome el valor inicial de n bits, conviéndolo en float (0.0f, 1.0f, 2.0f, etc.); llame a este c.</li>
<li>c = c * (1.0f / (2ⁿ-1))</li>
<li>Si (c < = D3D<em>xx</em>_SRGB_TO_FLOAT_THRESHOLD) entonces: result = c / D3D<em>xx</em>_SRGB_TO_FLOAT_DENOMINATOR_1, en caso contrario: result = ((c + D3D<em>xx</em>_SRGB_TO_FLOAT_OFFSET)/D3D<em>xx</em>_SRGB_TO_FLOAT_DENOMINATOR_2)D3D<em>xx</em>_SRGB_TO_FLOAT_EXPONENT</li>
</ul>
Esta conversión permite una tolerancia de D3D<em>xx _SRGB_TO_FLOAT_TOLERANCE_IN_ULP</em>Unit-Last-Place (en el lado SRGB). <br/></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>SRGB</td>
<td>A continuación se muestra la conversión float -> SRGB ideal.<br/> Suponiendo que el componente de color SRGB de destino tenga n bits:<br/>
<ul>
<li>Supongamos que el valor inicial es c.</li>
<li>Si c es NaN, el resultado es 0.</li>
<li>Si c > 1.0f, incluido INF, se fija a 1.0f.</li>
<li>Si c < 0.0f, incluido -INF, se fija a 0.0f.</li>
<li>Si (c <= D3D<em>xx</em>_FLOAT_TO_SRGB_THRESHOLD) entonces: c = D3D<em>xx</em>_FLOAT_TO_SRGB_SCALE_1 * c; de lo contrario: c = D3D<em>xx</em>_FLOAT_TO_SRGB_SCALE_2 * c(D3D<em>xx</em>_FLOAT_TO_SRGB_EXPONENT_NUMERATOR/D3D<em>xx</em>_FLOAT_TO_SRGB_EXPONENT_DENOMINATOR) - D3D<em>xx</em>_FLOAT_TO_SRGB_OFFSET</li>
<li>Conversión de la escala float a la escala de enteros: c = c * (2ⁿ-1).</li>
<li>Convertir en entero:
<ul>
<li>c = c + 0,5f.</li>
<li>Se descarta la fracción decimal y el valor de punto flotante restante (entero) se convierte directamente en un entero.</li>
</ul></li>
</ul>
Esta conversión se permite con una tolerancia de D3D<em>xx _FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP</em>Unit-Last-Place (en el lado entero). Esto significa que, después de convertir la escala float a la escala de enteros, cualquier valor de D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP Unit-Last-Place de un valor de formato de destino representable puede asignarse a ese valor. El requisito de inversión de datos adicional garantiza que la conversión no disminuya en todo el intervalo y que todos los valores de salida sean alcanzables.<br/></td>
</tr>
<tr class="odd">
<td>SINT</td>
<td>SINT con más bits</td>
<td>Para convertir de SINT a un SINT con más bits, el bit más significativo (MSB) del número inicial se extiende a los bits adicionales disponibles en el formato &quot; &quot; de destino.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>SINT con más bits</td>
<td>Para convertir de UINT a un SINT con más bits, el número se copia en los bits menos significativos (LSB) del formato de destino y los MSB adicionales se agregan con 0.<br/></td>
</tr>
<tr class="odd">
<td>SINT</td>
<td>UINT con más bits</td>
<td>Para convertir de SINT a UINT con más bits: si es negativo, el valor se fija en 0. De lo contrario, el número se copia en los LSB del formato de destino y los MSB adicionales se agregan con 0.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>UINT con más bits</td>
<td>Para convertir de UINT a UINT con más bits, el número se copia en los LSB del formato de destino y los MSB adicionales se agregan con 0.<br/></td>
</tr>
<tr class="odd">
<td>SINT o UINT</td>
<td>SINT o UINT con menos o igual bits</td>
<td>Para convertir de SINT o UINT a SINT o UINT con menos o igual bits (o cambio en la firma), el valor inicial simplemente se fija en el intervalo del formato de destino.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="fixed-point-integer-conversion"></a>Conversión de entero de punto fijo

Los enteros de punto fijo son simplemente enteros de algún tamaño de bits que tienen un separador decimal implícito en una ubicación fija.

El tipo de datos ubicuo "entero" es un caso especial de un entero de punto fijo con el decimal al final del número.

Las representaciones de número de punto fijo se caracterizan como: i.f, donde i es el número de bits enteros y f es el número de bits fraccionales. Por ejemplo, 16,8 significa un entero de 16 bits seguido de 8 bits de fracción. La parte entera se almacena en el complemento de 2, al menos como se define aquí (aunque también se puede definir por igual para enteros sin signo). La parte fraccionera se almacena en formato sin signo. La parte fraccionera siempre representa la fracción positiva entre los dos valores enteros más cercanos, empezando por el más negativo.

Las operaciones de suma y resta en números de punto fijo se realizan simplemente con aritmética de enteros estándar, sin tener en cuenta dónde se encuentra el decimal implícito. Agregar 1 a un número de punto fijo de 16,8 significa simplemente agregar 256, ya que el decimal está a 8 posiciones del final menos significativo del número. Otras operaciones, como la multiplicación, también se pueden realizar simplemente con aritmética de enteros, siempre que se tenga en cuenta el efecto en el decimal fijo. Por ejemplo, la multiplicación de dos enteros de 16,8 mediante una multiplicación de enteros genera un resultado de 32,16.

Las representaciones de entero de punto fijo se usan de dos maneras en Direct3D.

-   Las posiciones de vértice recortadas posteriormente en el rasterizador se ajustarán a un punto fijo para distribuir uniformemente la precisión en el área RenderTarget. Muchas operaciones de rasterizador, incluida la selección de caras como ejemplo, se producen en posiciones con ajuste de punto fijo, mientras que otras operaciones, como la configuración del interpolador de atributos, usan posiciones que se han convertido de nuevo en punto flotante desde las posiciones de punto fijo.
-   Las coordenadas de textura para las operaciones de muestreo se ajusta a un punto fijo (después de escalar por tamaño de textura), para distribuir uniformemente la precisión entre el espacio de textura, al elegir las ubicaciones o pesos de las pulsaciones de filtro. Los valores de peso se convierten de nuevo en punto flotante antes de que se realice la aritmética de filtrado real.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de datos de origen</th>
<th>Tipo de datos de destino</th>
<th>Regla de conversión</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FLOAT</td>
<td>Entero de punto fijo</td>
<td>El siguiente es el procedimiento general para convertir un número de punto flotante n en un entero de punto fijo i.f, donde i es el número de bits enteros (con signo) y f es el número de bits fraccionales.<br/>
<ul>
<li>Compute FixedMin = -2⁽ⁱ,¹⁾</li>
<li>Compute FixedMax = 2⁽ⁱ,¹⁾ - 2<sup>(-f)</sup></li>
<li>Si n es un NaN, result = 0; si n es +Inf, result = FixedMax*2<sup>f</sup>; si n es -Inf, result = FixedMin*2<sup>f</sup></li>
<li>Si n >= FixedMax, result = Fixedmax*2<sup>f</sup>; si n <= FixedMin, result = FixedMin*2 <sup> f</sup></li>
<li>De lo contrario, calcule n*2<sup>f</sup> y convierta en entero.</li>
</ul>
Se permiten implementaciones D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP tolerancia unit-last-place en el resultado entero, en lugar del valor infinitamente preciso n*2<sup>f</sup> después del último paso anterior.<br/></td>
</tr>
<tr class="even">
<td>Entero de punto fijo</td>
<td>FLOAT</td>
<td>Suponga que la representación de punto fijo específica que se va a convertir en float no contiene más de 24 bits de información, de los cuales no hay más de 23 bits en el componente fraccionrio. Supongamos que un número de punto fijo determinado, fxp, está en formato i.f (entero de i bits, fracción de bits f). La conversión a float es similar al pseudocódigo siguiente.<br/> float result = (float)(fxp >> f) + // extract integer<br/> <dl> ((float)(fxp & (2<sup>f</sup> - 1)) / (2<sup>f</sup>)); // extract fraction<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




