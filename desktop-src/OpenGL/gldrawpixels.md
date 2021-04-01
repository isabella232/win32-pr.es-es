---
title: función glDrawPixels (GL. h)
description: La función glDrawPixels escribe un bloque de píxeles en el fotogramas.
ms.assetid: c4eda64f-a75e-4e6d-984d-af49414b94d8
keywords:
- glDrawPixels (función) OpenGL
topic_type:
- apiref
api_name:
- glDrawPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25adc8ad28791086020a37d3a30651e169bfd07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150053"
---
# <a name="gldrawpixels-function"></a>glDrawPixels función)

La función **glDrawPixels** escribe un bloque de píxeles en el fotogramas.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glDrawPixels(
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*width* 
</dt> <dd>

La dimensión de ancho del rectángulo de píxeles que se escribirá en el fotogramas.

</dd> <dt>

*height* 
</dt> <dd>

La dimensión de alto del rectángulo de píxeles que se escribirá en el fotogramas.

</dd> <dt>

*format* 
</dt> <dd>

Formato de los datos de píxeles. Las constantes simbólicas aceptables son las siguientes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt><strong>GL_COLOR_INDEX</strong></dt> </dl></td>
<td>Cada píxel es un valor único, un índice de color. <br/>
<ol>
<li>La función <strong>glDrawPixels</strong> convierte cada píxel en formato de punto fijo, con un número no especificado de bits a la derecha del punto binario, independientemente del tipo de datos de memoria. Los valores de punto flotante se convierten en valores de punto fijo verdaderos. La función <strong>glDrawPixels</strong> convierte los datos enteros con signo y sin signo con todos los bits de fracción establecidos en cero. La función convierte los datos de mapa de bits en 0,0 o 1,0.</li>
<li>La función <strong>glDrawPixels</strong> desplaza cada índice de punto fijo a la izquierda GL_INDEX_SHIFT bits y lo agrega a GL_INDEX_OFFSET. Si GL_INDEX_SHIFT es negativo, el desplazamiento está a la derecha. En cualquier caso, cero bits rellenan de otro modo las ubicaciones de bits no especificadas en el resultado.</li>
<li>En el modo RGBA, <strong>glDrawPixels</strong> convierte el índice resultante en un píxel RGBA mediante las tablas GL_PIXEL_MAP_I_TO_R, GL_PIXEL_MAP_I_TO_G, GL_PIXEL_MAP_I_TO_B y GL_PIXEL_MAP_I_TO_A. Cuando se encuentra en el modo de índice de color y GL_MAP_COLOR es true, el índice se reemplaza por el valor al que <strong>glDrawPixels</strong> hace referencia en la tabla de búsqueda GL_PIXEL_MAP_I_TO_I.</li>
<li>Tanto si el reemplazo de búsqueda del índice se realiza como si no, la parte entera del índice es <strong>y</strong>Ed con 2<sup>b</sup> - 1, donde <em>b</em> es el número de bits de un búfer de índice de color.</li>
<li>Los índices resultantes o los colores RGBA se convierten entonces en fragmentos al adjuntar las coordenadas <em>z</em>y de textura de la posición de la trama actual a cada píxel y, a continuación, asignar las coordenadas de la ventana <em>x</em> <em>e y al</em> fragmento <em>n</em>como <em>x</em>? = <em>ancho</em> <em>x</em><sub>r</sub> + <em>n</em> mod<br/> ¿ <em>y</em>? = <em></em><sub></sub> + <em>n/ancho</em> de r<br/> donde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) es la posición de la trama actual.<br/></li>
<li>La función <strong>glDrawPixels</strong> trata estos fragmentos de píxeles del mismo modo que los fragmentos generados mediante la rasterización de puntos, líneas o polígonos. Aplica la asignación de texturas, la niebla y todas las operaciones de fragmento antes de escribir los fragmentos en el fotogramas.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <dt><strong>GL_STENCIL_INDEX</strong></dt> </dl></td>
<td>Cada píxel es un valor único, un índice de estarcido. <br/>
<ol>
<li>La función <strong>glDrawPixels</strong> lo convierte en un formato de punto fijo, con un número no especificado de bits a la derecha del punto binario, independientemente del tipo de datos de memoria. Los valores de punto flotante se convierten en valores de punto fijo verdaderos. La función <strong>glDrawPixels</strong> convierte los datos enteros con signo y sin signo con todos los bits de fracción establecidos en cero. Los datos de mapa de bits se convierten en 0,0 o 1,0.</li>
<li>La función <strong>glDrawPixels</strong> desplaza cada índice de punto fijo a la izquierda GL_INDEX_SHIFT bits y lo agrega a GL_INDEX_OFFSET. Si GL_INDEX_SHIFT es negativo, el desplazamiento está a la derecha. En cualquier caso, cero bits rellenan de otro modo las ubicaciones de bits no especificadas en el resultado.</li>
<li>Si GL_MAP_STENCIL es true, el índice se reemplaza por el valor al que <strong>glDrawPixels</strong> hace referencia en la tabla de búsqueda GL_PIXEL_MAP_S_TO_S.</li>
<li>Tanto si el reemplazo de búsqueda del índice se realiza como si no, la parte entera del índice es entonces <strong>y</strong>Ed con 2<sup>b</sup> - 1, donde <em>b</em> es el número de bits del búfer de estarcido. Los índices de estarcido resultantes se escriben en el búfer de la galería de símbolos, de modo que el <em>n</em>índice se escribe en la ubicación <em>x</em>? = <em>ancho</em> <em>x</em><sub>r</sub> + <em>n</em> mod<br/> ¿ <em>y</em>? = <em></em><sub></sub> + <em>n/ancho</em> de r<br/> donde (<em>x</em><sub>r</sub> , <em></em> y<sub>r</sub> ) es la posición de la trama actual. Solo la prueba de propiedad del píxel, la prueba de tijera y la galería de símbolos writemask afectan a estas escrituras.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <dt><strong>GL_DEPTH_COMPONENT</strong></dt> </dl></td>
<td>Cada píxel es un componente de una sola profundidad. <br/>
<ol>
<li>La función <strong>glDrawPixels</strong> convierte los datos de punto flotante directamente en un formato de punto flotante interno con una precisión no especificada. Los datos enteros con signo se asignan linealmente al formato de punto flotante interno, de modo que el valor entero representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0. Los datos enteros sin signo se asignan de forma similar: el valor entero más grande se asigna a 1,0 y cero se asigna a 0,0.</li>
<li>La función <strong>glDrawPixels</strong> multiplica el valor de profundidad de punto flotante resultante por GL_DEPTH_SCALE y lo agrega a GL_DEPTH_BIAS. El resultado se fija en el intervalo [0, 1].</li>
<li>La función <strong>glDrawPixels</strong> convierte los componentes de profundidad resultantes en fragmentos adjuntando el color de posición de la trama actual o el índice de color y las coordenadas de textura a cada píxel y, a continuación, asignando las coordenadas de la ventana <em>x</em> <em>e y al</em> fragmento <em>n</em> tal que <em>x</em>? = <em></em><em>ancho</em> x<sub>r</sub> + <em>n</em> mod<br/> ¿ <em>y</em>? = <em></em><sub></sub> + <em>n/ancho</em> de r<br/> donde ( <em></em> x<sub>r</sub> ,<em>y</em><sub>r</sub> ) es la posición de la trama actual.<br/></li>
<li>Estos fragmentos de píxeles se tratan a continuación como los fragmentos generados mediante la rasterización de puntos, líneas o polígonos. La función <strong>glDrawPixels</strong> aplica la asignación de texturas, la niebla y todas las operaciones de fragmento antes de escribir los fragmentos en el fotogramas.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt><strong>GL_RGBA</strong></dt> </dl></td>
<td>Cada píxel es un grupo de cuatro componentes en este orden: rojo, verde, azul, alfa. <br/>
<ol>
<li>La función <strong>glDrawPixels</strong> convierte los valores de punto flotante directamente en un formato de punto flotante interno con una precisión no especificada. Los valores enteros con signo se asignan linealmente al formato de punto flotante interno, de modo que el valor entero representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0. Los datos enteros sin signo se asignan de forma similar: el valor entero más grande se asigna a 1,0 y cero se asigna a 0,0.</li>
<li>La función <strong>glDrawPixels</strong> multiplica los valores de color de punto flotante resultantes por GL_c_SCALE y los agrega a GL_c_BIAS, donde <em>c</em> es rojo, verde, azul y alfa para los componentes de color respectivos. Los resultados se fijan en el intervalo [0, 1].</li>
<li>Si GL_MAP_COLOR es true, <strong>glDrawPixels</strong> escala cada componente de color por el tamaño de la tabla de búsqueda GL_PIXEL_MAP_c_TO_c y, a continuación, reemplaza el componente por el valor al que hace referencia en esa tabla; <em>c</em> es R, G, B o A, respectivamente.</li>
<li>La función <strong>glDrawPixels</strong> convierte los colores RGBA resultantes en fragmentos adjuntando las coordenadas <em>z</em>y de textura de la posición de la trama actual a cada píxel y asignando las coordenadas de la ventana <em>x</em> e <em>y</em> al fragmento <em>n</em>, tal que <em>x</em>? = <em>ancho</em> <em>x</em><sub>r</sub> + <em>n</em> mod<br/> ¿ <em>y</em>? = <em>s</em><sub>r</sub> + <em>n/width</em><br/> donde (<em>x</em><sub>r</sub> ,<em>y</em><sub>r</sub> ) es la posición de la trama actual.<br/></li>
<li>Estos fragmentos de píxeles se tratan a continuación como los fragmentos generados mediante la rasterización de puntos, líneas o polígonos. La función <strong>glDrawPixels</strong> aplica la asignación de texturas, la niebla y todas las operaciones de fragmento antes de escribir los fragmentos en el fotogramas.</li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Cada píxel es un único componente rojo.<br/> La función <strong>glDrawPixels</strong> convierte este componente en el formato de punto flotante interno de la misma manera que el componente rojo de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con el verde y el azul establecidos en 0,0 y el valor alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Cada píxel es un único componente verde.<br/> La función <strong>glDrawPixels</strong> convierte este componente al formato de punto flotante interno de la misma manera que el componente verde de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con el rojo y el azul establecidos en 0,0 y el valor alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Cada píxel es un único componente azul.<br/> La función <strong>glDrawPixels</strong> convierte este componente en el formato de punto flotante interno de la misma manera que el componente azul de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con rojo y verde establecido en 0,0 y el valor alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Cada píxel es un único componente alfa.<br/> La función <strong>glDrawPixels</strong> convierte este componente al formato de punto flotante interno de la misma manera que el componente alfa de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con rojo, verde y azul establecido en 0,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Cada píxel es un grupo de tres componentes en este orden: rojo, verde, azul. La función <strong>glDrawPixels</strong> convierte cada componente en el formato de punto flotante interno de la misma manera que los componentes rojo, verde y azul de un píxel RGBA. El color triple se convierte en un píxel RGBA con el valor alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt><strong>GL_LUMINANCE</strong></dt> </dl></td>
<td>Cada píxel es un único componente de luminancia.<br/> La función <strong>glDrawPixels</strong> convierte este componente en el formato de punto flotante interno de la misma manera que el componente rojo de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con el rojo, verde y azul establecido en el valor de luminancia convertido y alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt><strong>GL_LUMINANCE_ALPHA</strong></dt> </dl></td>
<td>Cada píxel es un grupo de dos componentes en este orden: luminancia, alfa.<br/> La función <strong>glDrawPixels</strong> convierte los dos componentes en el formato de punto flotante interno de la misma manera que el componente rojo de un píxel RGBA es y, a continuación, los convierte en un píxel RGBA con el color rojo, verde y azul establecido en el valor de luminancia convertido y el alfa establecido en el valor alfa convertido. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>Cada píxel es un grupo de tres componentes en este orden: azul, verde, rojo.<br/> GL_BGR_EXT proporciona un formato que coincide con el diseño de memoria de los mapas de bits independientes del dispositivo (DIB) de Windows. Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt><strong>GL_BGRA_EXT</strong></dt> </dl></td>
<td>Cada píxel es un grupo de cuatro componentes en este orden: azul, verde, rojo y alfa.<br/> GL_BGRA_EXT proporciona un formato que coincide con el diseño de memoria de los mapas de bits independientes del dispositivo (DIB) de Windows. Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*type* 
</dt> <dd>

El tipo de datos de los *píxeles*. A continuación se indican las constantes simbólicas aceptadas y su significado.



| Value                                                                                                                                                                      | Significado                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**\_byte sin signo de \_ GL**</dt> </dl>    | Entero de 8 bits sin signo<br/>                 |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**BYTE de GL \_**</dt> </dl>                                | Entero de 8 bits con signo<br/>                   |
| <span id="GL_BITMAP"></span><span id="gl_bitmap"></span><dl> <dt>**mapa de bits de GL \_**</dt> </dl>                          | Bits únicos en enteros de 8 bits sin signo<br/> |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**libro de contabilidad \_ corto sin signo \_**</dt> </dl> | Entero de 16 bits sin signo<br/>                |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**CONTABILIDAD \_ breve**</dt> </dl>                             | Entero de 16 bits con signo<br/>                  |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**libro de contabilidad \_ sin signo \_**</dt> </dl>       | Entero de 32 bits sin signo<br/>                |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ int**</dt> </dl>                                   | Entero de 32 bits<br/>                         |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**valor \_ float de GL**</dt> </dl>                             | Punto flotante de precisión sencilla<br/>        |



 

</dd> <dt>

*píxeles* 
</dt> <dd>

Puntero a los datos de píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | El *ancho* o el *alto* era negativo.<br/>                                                                                                                                          |
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | Cualquier *formato* o *tipo* no era un valor aceptado. <br/>                                                                                                                             |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | el *formato* era GL \_ rojo, GL \_ verde, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL BGRA ext, GL GL \_ \_ \_ o \_ luminancia de GL \_ alfa y OpenGL estaba en modo de índice de color.<br/> |
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *tipo* era \_ un mapa de bits de contabilidad y el *formato* no es un índice \_ \_ de color de GL o un índice de estarcido de contabilidad \_ \_ .<br/>                                                                                         |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | el *formato* del \_ Índice de estarcido es GL \_ y no hay ningún búfer de estarcido.<br/>                                                                                                                  |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/>                                                        |


## <a name="remarks"></a>Observaciones

La función **glDrawPixels** lee datos de píxeles de la memoria y los escribe en el fotogramas en relación con la posición de la trama actual. Use [**glRasterPos**](glrasterpos-functions.md) para establecer la posición de la trama actual y use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con \_ \_ la posición de rasterización actual del argumento GL \_ para consultar la posición de la trama.

Varios parámetros definen la codificación de los datos de píxeles en la memoria y controlan el procesamiento de los datos de píxeles antes de colocarlos en el fotogramas. Estos parámetros se establecen con cuatro funciones: [**glPixelStore**](glpixelstore-functions.md), [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md)y [**glPixelZoom**](glpixelzoom.md). En este tema se describen los efectos en **glDrawPixels** de muchos de los parámetros especificados por estas cuatro funciones, pero no todos.

Los datos se leen desde *píxeles* como una secuencia de bytes con signo o sin signo, números cortos con signo o sin signo, enteros con signo o sin signo o valores de punto flotante de precisión sencilla, dependiendo del *tipo*. Cada uno de estos bytes, cortos, enteros o valores de punto flotante se interpreta como un componente de color o de profundidad, o un índice, dependiendo del *formato*. Los índices siempre se tratan individualmente. Los componentes de color se tratan como grupos de uno, dos, tres o cuatro valores, de nuevo en función del *formato*. Tanto los índices individuales como los grupos de componentes se conocen como píxeles. Si el *tipo* es un mapa de bits de contabilidad \_ , los datos deben ser bytes sin signo y el *formato* debe ser índice de \_ color de GL \_ o índice de estarcido de libro de contabilidad \_ \_ . Cada byte sin signo se trata como píxeles de 8 1 bits, con una ordenación de bits determinada por GL \_ unpack \_ LSB \_ primero (vea [**glPixelStore**](glpixelstore-functions.md)).

Los píxeles de *ancho* por *alto* se leen de la memoria, empezando en los *píxeles* de la ubicación. De forma predeterminada, estos píxeles se toman de las ubicaciones de memoria adyacentes, salvo que, una vez leídos todos los píxeles de *ancho* , el puntero de lectura está avanzado hasta el siguiente límite de 4 bytes. La función **glPixelStore** especifica la alineación de filas de 4 bytes con la alineación del desempaquetador de contabilidad de argumentos \_ \_ , y puede establecerla en 1, 2, 4 u 8 bytes. Otros parámetros de almacén de píxeles especifican distintos avances de puntero de lectura, antes de que se lea el primer píxel y después de que se lean todos los píxeles de *ancho* . La función **glPixelStore** funciona en cada uno de los píxeles de *ancho por alto* que lee de la memoria de la misma manera, en función de los valores de varios parámetros especificados por [**glPixelTransfer**](glpixeltransfer.md) y [**glPixelMap**](glpixelmap.md). Los detalles de estas operaciones, así como el búfer de destino en el que se dibujan los píxeles, son específicos del formato de los píxeles, tal y como se especifica en *Format*.

La rasterización descrita hasta ahora supone un factor de zoom de píxeles de 1,0. Si usa [**glPixelZoom**](glpixelzoom.md) para cambiar los factores de zoom de píxeles *x* *e y, los píxeles se* convierten en fragmentos como se indica a continuación. Si (*XR, yr*) es la posición de la trama actual y un píxel determinado se encuentra en la columna *n* y en la fila *m* del rectángulo de píxeles, se generan fragmentos para los píxeles cuyos centros están en el rectángulo con esquinas en

(*x*<sub>r</sub>  +  ¿ *zoom*? *n*, *y*<sub>r</sub>  +  *zoom*<sub>y</sub> *m*

(*x*<sub>r</sub>  +  ¿ *zoom*? (*n* + 1), *y*<sub>r</sub>  +  *zoom*<sub>y</sub> (*m* + 1))

¿Dónde *hacer zoom*? es el valor de zoom de GL \_ \_ X y *zoom*<sub>y</sub> es el valor de zoom de GL \_ \_ y.

Las siguientes funciones recuperan información relacionada con **glDrawPixels**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ posición de RASTERIZAción actual de GL \_

**glGet** con argumento de \_ posición de rasterizado actual de GL \_ \_ \_ válido

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





