---
description: En las secciones siguientes se describe cómo Direct3D controla las conversiones entre los tipos de datos.
ms.assetid: 454d3fd0-fc0f-46a9-925e-13f8e3c39f02
title: Reglas de conversión de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61abdc58811af9155c67d7b32bcd47e9d4b71ea5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807351"
---
# <a name="data-conversion-rules"></a>Reglas de conversión de datos

En las secciones siguientes se describe cómo Direct3D controla las conversiones entre los tipos de datos.

-   [Terminología de tipos de datos](#data-type-terminology)
-   [Conversión de punto flotante](#floating-point-conversion)
    -   [Conververting de una representación de rango superior a una representación de rango inferior](#conververting-from-a-higher-range-representation-to-a-lower-range-representation)
    -   [Convertir una representación de rango inferior en una representación de rango superior](#converting-from-a-lower-range-representation-to-a-higher-range-representation)
-   [Conversión de enteros](#integer-conversion)
-   [Conversión de enteros de punto fijo](#fixed-point-integer-conversion)
-   [Temas relacionados](#related-topics)

## <a name="data-type-terminology"></a>Terminología de tipos de datos

El siguiente conjunto de términos se utiliza posteriormente para caracterizar varias conversiones de formato.



| Término  | Definición                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNORM | Entero normalizado con signo, lo que significa que para un número de complemento de n bits 2, el valor máximo significa 1,0 f (por ejemplo, el valor de 5 bits 01111 se asigna a 1,0 f) y el valor mínimo significa-1,0 f (por ejemplo, el valor de 5 bits 10000 se asigna a-1,0 f). Además, el segundo número mínimo se asigna a-1,0 f (por ejemplo, el valor de 5 bits 10001 se asigna a-1,0 f). Por tanto, hay dos representaciones enteras para-1,0 f. Hay una única representación para 0.0 f y una única representación para 1,0 f. Esto da como resultado un conjunto de representaciones enteras para los valores de punto flotante con espaciado uniforme en el intervalo (-1,0 f... 0.0 f) y también un conjunto complementario de representaciones para números en el intervalo (0,0 f... 1,0 f) |
| UNORM | Entero normalizado sin signo, lo que significa que para un número de n bits, el valor de 0 significa 0,0 f y el de los 1 significa 1,0 f. Se representa una secuencia de valores de punto flotante de espaciado uniforme entre 0,0 y 1,0 f. por ejemplo, un UNORM de 2 bits representa 0,0 f, 1/3, 2/3 y 1,0 f.                                                                                                                                                                                                                                                                                                                                                                                                                                |
| San  | Entero con signo. número entero del complemento 2. por ejemplo, un SINT de 3 bits representa los valores enteros-4,-3,-2,-1, 0, 1, 2, 3.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| UINT  | Entero sin signo. por ejemplo, un UINT de 3 bits representa los valores enteros 0, 1, 2, 3, 4, 5, 6, 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| FLOAT | Un valor de punto flotante en cualquiera de las representaciones definidas por Direct3D.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| SRGB  | Similar a UNORM, en que para un número de n bits, todo el valor de 0 significa 0,0 f y el de 1 significa 1,0 f. Sin embargo, a diferencia de UNORM, con SRGB, la secuencia de codificaciones de enteros sin signo entre 0 a todos los 1 representa una progresión no lineal en la interpretación de punto flotante de los números, entre 0,0 f y 1,0 f. Aproximadamente, si esta progresión no lineal, SRGB, se muestra como una secuencia de colores, aparecería como una rampa lineal de niveles de luminosidad a un observador "promedio", en "Average" condiciones de visualización, en una pantalla de "promedio". Para obtener detalles completos, consulte el estándar de color SRGB, IEC 61996-2-1, en IEC (Comisión electrotécnica internacional (CEI)).                |



 

## <a name="floating-point-conversion"></a>Conversión de punto flotante

Siempre que se produce una conversión de punto flotante entre distintas representaciones, incluidas las representaciones de punto no flotante o desde ellas, se aplican las reglas siguientes.

### <a name="conververting-from-a-higher-range-representation-to-a-lower-range-representation"></a>Conververting de una representación de rango superior a una representación de rango inferior

-   El redondeo a cero se usa durante la conversión a otro formato de punto flotante. Si el destino es un formato de número entero o de punto fijo, se usa la operación de redondeo a la más cercana, a menos que la conversión esté documentada explícitamente como si se usara otro comportamiento de redondeo, por ejemplo, de redondeo a SNORM, FLOAT a UNORM o FLOAT a SRGB. Otras excepciones son las instrucciones del sombreador ftoi y ftou, que usan un redondeo a cero. Por último, las conversiones de punto flotante a fijo usadas por el muestreador y el rasterizador de texturas tienen una tolerancia especificada que se mide en el último lugar de una versión ideal infinitamente.
-   Para los valores de origen mayores que el intervalo dinámico de un formato de destino de rango inferior (por ejemplo, un valor Float de 32 bits grande se escribe en un RenderTarget Float de 16 bits, el valor máximo que se pueda representar (con la firma adecuada), sin incluir el infinito con signo (debido al redondeo a cero descrito anteriormente).
-   Los NaN con un formato de intervalo más alto se convertirán en una representación de NaN en el formato de intervalo inferior si la representación NaN existe en el formato de intervalo inferior. Si el formato inferior no tiene una representación NaN, el resultado será 0.
-   INF en un formato de intervalo superior se convertirá a INF en el formato de intervalo inferior, si está disponible. Si el formato inferior no tiene una representación de INF, se convertirá en el valor máximo que se puede representar. El signo se conservará si está disponible en el formato de destino.
-   La desnormada en un formato de intervalo superior se convertirá a la representación de desnormativa en el formato de intervalo inferior si está disponible en el formato de intervalo inferior y la conversión es posible; de lo contrario, el resultado es 0. El bit de signo se conservará si está disponible en el formato de destino.

### <a name="converting-from-a-lower-range-representation-to-a-higher-range-representation"></a>Convertir una representación de rango inferior en una representación de rango superior

-   Los NaN en un formato de intervalo inferior se convertirán en la representación NaN en el formato de intervalo superior si están disponibles en el formato de rango superior. Si el formato de rango superior no tiene una representación NaN, se convertirá en 0.
-   INF en un formato de intervalo inferior se convertirá a la representación de INF en el formato de intervalo superior si está disponible en el formato de rango superior. Si el formato más alto no tiene una representación de INF, se convertirá en el valor máximo que se puede representar (MAX \_ float en ese formato). El signo se conservará si está disponible en el formato de destino.
-   La desnormada en un formato de intervalo inferior se convertirá a una representación normalizada en el formato de intervalo más alto si es posible, o bien a una representación de desnormativa en el formato de intervalo superior si existe la representación de desnormativa. Con errores, si el formato de rango superior no tiene una representación de desnormativa, se convertirá en 0. El signo se conservará si está disponible en el formato de destino. Tenga en cuenta que los números Float de 32 bits cuentan como un formato sin una representación de desnormativa (dado que las desnormativas en operaciones en los flotantes de 32 bits se vacían para firmar con el valor 0).

## <a name="integer-conversion"></a>Conversión de enteros

En la tabla siguiente se describen las conversiones de diversas representaciones descritas anteriormente a otras representaciones. Solo se muestran las conversiones que realmente se producen en Direct3D.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td>Dado un valor entero de n bits que representa el intervalo con signo [-1,0 f a 1.0 f], la conversión a punto flotante es como se indica a continuación.<br/>
<ul>
<li>El valor más negativo se asigna a-1,0 f. por ejemplo, el valor de 5 bits 10000 se asigna a-1,0 f.</li>
<li>Cada otro valor se convierte en un valor Float (lo llama c) y, a continuación, result = c * (1.0 f/(2 ⁽ ⁿ ⁻ ¹ ⁾-1)). Por ejemplo, el valor de 5 bits 10001 se convierte en-15.0 f y, a continuación, se divide entre 15 f, produciendo-1.0 f.</li>
</ul></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>SNORM</td>
<td>Dado un número de punto flotante, la conversión a un valor entero de n bits que representa el intervalo con signo [-1,0 f a 1.0 f] es como sigue.<br/>
<ul>
<li>Permita que c represente el valor de inicio.</li>
<li>Si c es NaN, el resultado es 0.</li>
<li>Si c > 1.0 f, incluido el INF, se fija en 1,0 f.</li>
<li>Si c <-1.0 f, incluido-INF, se fija en-1,0 f.</li>
<li>Convertir de escala flotante a escala de entero: c = c * (2 ⁿ ⁻ ¹-1).</li>
<li>Convertir en un entero como se indica a continuación.
<ul>
<li>Si c >= 0, c = c + 0.5 f; de lo contrario, c = c-0.5 f.</li>
<li>Quite la fracción decimal y el valor de punto flotante (entero) restante se convierte directamente en un entero.</li>
</ul></li>
</ul>
A esta conversión se le permite una tolerancia de D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_Unit de la última posición (en el lado entero). Esto significa que, después de realizar la conversión de la escala de punto flotante a entero, se permite que cualquier valor dentro de D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP unidad en el último lugar de un valor de formato de destino que se puede representar se asigne a ese valor. El requisito adicional de inversión de datos garantiza que la conversión se nondecreasing en el intervalo y todos los valores de salida se pueden alcanzar. (En las constantes que se muestran aquí, <em>XX</em> debe reemplazarse por la versión de Direct3D, por ejemplo, 10, 11 o 12).<br/></td>
</tr>
<tr class="odd">
<td>UNORM</td>
<td>FLOAT</td>
<td>El valor de n bits de inicio se convierte en Float (0,0 f, 1,0 f, 2.0 f, etc.) y, a continuación, se divide entre (2 ⁿ-1).<br/></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>UNORM</td>
<td>Permita que c represente el valor de inicio.<br/>
<ul>
<li>Si c es NaN, el resultado es 0.</li>
<li>Si c > 1.0 f, incluido el INF, se fija en 1,0 f.</li>
<li>Si c < 0.0 f, incluido-INF, se fija en 0,0 f.</li>
<li>Convertir de escala flotante a escala de entero: c = c * (2 ⁿ-1).</li>
<li>Convertir en entero.
<ul>
<li>c = c + 0.5 f.</li>
<li>Se quita la fracción decimal y el valor de punto flotante (entero) restante se convierte directamente en un entero.</li>
</ul></li>
</ul>
A esta conversión se le permite una tolerancia de D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP unidad (en el lado entero). Esto significa que, después de realizar la conversión de la escala de punto flotante a entero, se permite que cualquier valor dentro de D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP unidad en el último lugar de un valor de formato de destino que se puede representar se asigne a ese valor. El requisito adicional de inversión de datos garantiza que la conversión se nondecreasing en el intervalo y todos los valores de salida se pueden alcanzar.<br/></td>
</tr>
<tr class="odd">
<td>SRGB</td>
<td>FLOAT</td>
<td>A continuación se encuentra la conversión ideal de SRGB a FLOAT.<br/>
<ul>
<li>Tome el valor de n bits inicial, conviértalo en Float (0,0 f, 1,0 f, 2.0 f, etc.); Llame a este c.</li>
<li>c = c * (1,0 f/(2 ⁿ-1))</li>
<li>Si (c < = D3D<em>xx</em>_SRGB_TO_FLOAT_THRESHOLD): result = c/D3D<em>XX</em>_SRGB_TO_FLOAT_DENOMINATOR_1, Else: result = ((c + D3D<em>xx</em>_SRGB_TO_FLOAT_OFFSET)/D3D<em>XX</em>_SRGB_TO_FLOAT_DENOMINATOR_2) D3D<em>XX</em>_SRGB_TO_FLOAT_EXPONENT</li>
</ul>
A esta conversión se le permite una tolerancia de D3D<em>xx</em>_SRGB_TO_FLOAT_TOLERANCE_IN_ULP unidad-último lugar (en el lado de sRGB). <br/></td>
</tr>
<tr class="even">
<td>FLOAT</td>
<td>SRGB</td>
<td>A continuación se encuentra la conversión de tipo "FLOAT-> SRGB" ideal.<br/> Suponiendo que el componente de color SRGB de destino tiene n bits:<br/>
<ul>
<li>Supongamos que el valor inicial es c.</li>
<li>Si c es NaN, el resultado es 0.</li>
<li>Si c > 1.0 f, incluido el archivo INF, se fija en 1,0 f.</li>
<li>Si c < 0.0 f, incluido-INF, se fija en 0,0 f.</li>
<li>Si (c <= D3D<em>xx</em>_FLOAT_TO_SRGB_THRESHOLD): c = d3d<em>XX</em>_FLOAT_TO_SRGB_SCALE_1 * c, Else: c = D3D<em>XX</em>_FLOAT_TO_SRGB_SCALE_2 * c (D3D<em>XX</em>_FLOAT_TO_SRGB_EXPONENT_NUMERATOR/D3D<em>XX</em>_FLOAT_TO_SRGB_EXPONENT_DENOMINATOR)-D3D<em>XX</em>_FLOAT_TO_SRGB_OFFSET</li>
<li>Convertir de escala flotante a escala de entero: c = c * (2 ⁿ-1).</li>
<li>Convertir en entero:
<ul>
<li>c = c + 0.5 f.</li>
<li>Se quita la fracción decimal y el valor de punto flotante (entero) restante se convierte directamente en un entero.</li>
</ul></li>
</ul>
A esta conversión se le permite una tolerancia de D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP unidad (en el lado entero). Esto significa que, después de realizar la conversión de la escala de punto flotante a entero, se permite que cualquier valor dentro de D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP unidad en el último lugar de un valor de formato de destino que se puede representar se asigne a ese valor. El requisito adicional de inversión de datos garantiza que la conversión se nondecreasing en el intervalo y todos los valores de salida se pueden alcanzar.<br/></td>
</tr>
<tr class="odd">
<td>San</td>
<td>SINT con más bits</td>
<td>Para convertir de SINT a un San con más bits, el bit más significativo (MSB) del número de inicio se &quot; extiende con signo &quot; a los bits adicionales disponibles en el formato de destino.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>SINT con más bits</td>
<td>Para convertir de UINT a un SINT con más bits, el número se copia en los bits menos significativos del formato de destino (LSBs) y los MSBs adicionales se rellenan con 0.<br/></td>
</tr>
<tr class="odd">
<td>San</td>
<td>UINT con más bits</td>
<td>Para convertir de SINT a UINT con más bits: si es negativo, el valor se fija en 0. En caso contrario, el número se copia en el LSBs del formato de destino y los MSB adicionales se rellenan con 0.<br/></td>
</tr>
<tr class="even">
<td>UINT</td>
<td>UINT con más bits</td>
<td>Para convertir de UINT a UINT con más bits, el número se copia en el LSBs del formato de destino y los MSB adicionales se rellenan con 0.<br/></td>
</tr>
<tr class="odd">
<td>SINT o UINT</td>
<td>SINT o UINT con menos o igual bits</td>
<td>Para convertir de un SINT o UINT a SINT o UINT con menos o igual bits (y/o cambiar en la firma), el valor inicial se fija simplemente en el intervalo del formato de destino.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="fixed-point-integer-conversion"></a>Conversión de enteros de punto fijo

Los enteros de punto fijo son simplemente enteros de algún tamaño de bit que tienen un punto decimal implícito en una ubicación fija.

El tipo de datos omnipresente "integer" es un caso especial de un entero de punto fijo con el decimal al final del número.

Las representaciones de números de punto fijo se caracterizan como: i. f, donde i es el número de bits enteros y f es el número de bits fraccionarios. por ejemplo, 16,8 significa un entero de 16 bits seguido de 8 bits de fracción. La parte entera se almacena en el complemento de 2, al menos como se define aquí (aunque también se puede definir igualmente para enteros sin signo). La parte fraccionaria se almacena en formato sin signo. La parte fraccionaria siempre representa la fracción positiva entre los dos valores enteros más cercanos, empezando por el más negativo.

Las operaciones de suma y resta en números de punto fijo se realizan simplemente mediante la aritmética de enteros estándar, sin tener en cuenta el lugar en el que se encuentra el decimal implícito. Agregar 1 a un número de punto fijo 16,8 significa agregar 256, ya que el decimal es 8 lugares en el extremo menos significativo del número. Otras operaciones, como la multiplicación, se pueden realizar simplemente usando aritmética de enteros, siempre que se tenga en cuenta el efecto en el decimal fijo. Por ejemplo, si se multiplican dos enteros 16,8 mediante una multiplicación de enteros, se genera un resultado de 32,16.

Las representaciones de enteros de punto fijo se usan de dos maneras en Direct3D.

-   Las posiciones de vértices recortadas en el rasterizador se ajustan a un punto fijo para distribuir uniformemente la precisión en el área de RenderTarget. Muchas operaciones de rasterizador, incluida la selección de caras como un ejemplo, se producen en posiciones ajustadas de punto fijo, mientras que otras operaciones, como la configuración del interpolador de atributos, usan posiciones que se han convertido de nuevo en punto flotante desde las posiciones ajustadas de punto fijo.
-   Las coordenadas de textura de las operaciones de muestreo se ajustan a un punto fijo (después de que se escalen por tamaño de textura), para distribuir uniformemente la precisión a través del espacio de textura, en elegir el filtro puntee en ubicaciones/pesos. Los valores de peso se convierten de nuevo en el punto flotante antes de que se realice la aritmética de filtrado real.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td>A continuación se presenta el procedimiento general para convertir un número de punto flotante n en un entero de punto fijo i. f, donde i es el número de bits enteros (con signo) y f es el número de bits fraccionarios.<br/>
<ul>
<li>Compute FixedMin =-2 ⁽ ⁱ ⁻ ¹ ⁾</li>
<li>Compute FixedMax = 2 ⁽ ⁱ ⁻ ¹ ⁾-2<sup>(-f)</sup></li>
<li>Si n es un NaN, el resultado es 0; Si n es + inf, result = FixedMax * 2<sup>f</sup>; Si n es-inf, result = FixedMin * 2<sup>f</sup></li>
<li>Si n >= FixedMax, result = Fixedmax * 2<sup>f</sup>; Si n <= FixedMin, result = FixedMin * 2 <sup> f</sup></li>
<li>En caso contrario, Compute n * 2<sup>f</sup> y conviértalo en Integer.</li>
</ul>
Las implementaciones tienen permitidos D3D<em>xx</em>_FLOAT32_TO_INTEGER_TOLERANCE_IN_ULP tolerancia de última vez en el resultado entero, en lugar del valor Infinitely preciso n * 2<sup>f</sup> después del último paso anterior.<br/></td>
</tr>
<tr class="even">
<td>Entero de punto fijo</td>
<td>FLOAT</td>
<td>Supongamos que la representación de punto fijo específica que se está convirtiendo en Float no contiene más de un total de 24 bits de información, y no más de 23 bits de que se encuentra en el componente fraccionario. Supongamos que un número de punto fijo determinado, fxp, se encuentra en formato i. f (i bits entero, fracción de f bits). La conversión a Float es similar al siguiente pseudocódigo.<br/> Float Result = (float) (fxp >> f) +//Extract Integer<br/> <dl> ((float) (fxp & (2<sup>f</sup> - 1))/(2<sup>f</sup>));//extraer fracción<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




