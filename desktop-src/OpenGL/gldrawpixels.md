---
title: Función glDrawPixels (Gl.h)
description: La función glDrawPixels escribe un bloque de píxeles en el búfer de fotogramas.
ms.assetid: c4eda64f-a75e-4e6d-984d-af49414b94d8
keywords:
- Función glDrawPixels OpenGL
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
ms.openlocfilehash: 832cfadb28d80b57366084297877ffadc1a6238c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480711"
---
# <a name="gldrawpixels-function"></a>Función glDrawPixels

La **función glDrawPixels** escribe un bloque de píxeles en el búfer de fotogramas.

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

Dimensión de ancho del rectángulo de píxeles que se escribirá en el búfer de fotogramas.

</dd> <dt>

*height* 
</dt> <dd>

Dimensión de alto del rectángulo de píxeles que se escribirá en el búfer de fotogramas.

</dd> <dt>

*format* 
</dt> <dd>

Formato de los datos de píxeles. Las constantes simbólicas aceptables son las siguientes.




| Valor | Significado | 
|-------|---------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl><dt><strong>GL_COLOR_INDEX</strong></dt></dl> | Cada píxel es un valor único, un índice de color. <br /><ol><li>La <strong>función glDrawPixels</strong> convierte cada píxel en formato de punto fijo, con un número no especificado de bits a la derecha del punto binario, independientemente del tipo de datos de memoria. Los valores de punto flotante se convierten en valores de punto fijo verdaderos. La <strong>función glDrawPixels</strong> convierte datos enteros con signo y sin signo con todos los bits de fracción establecidos en cero. La función convierte los datos de mapa de bits en 0.0 o 1.0.</li><li>La <strong>función glDrawPixels</strong> desplaza cada índice de punto fijo a la izquierda GL_INDEX_SHIFT bits y lo agrega a GL_INDEX_OFFSET. Si GL_INDEX_SHIFT es negativo, el desplazamiento es a la derecha. En cualquier caso, los bits cero rellenan ubicaciones de bits no especificadas en el resultado.</li><li>En el modo RGBA, <strong>glDrawPixels</strong> convierte el índice resultante en un píxel RGBA mediante las tablas GL_PIXEL_MAP_I_TO_R, GL_PIXEL_MAP_I_TO_G, GL_PIXEL_MAP_I_TO_B y GL_PIXEL_MAP_I_TO_A. Cuando en el modo de índice de color y GL_MAP_COLOR es true, el índice se reemplaza por el valor al que <strong>glDrawPixels</strong> hace referencia en la tabla de búsqueda GL_PIXEL_MAP_I_TO_I.</li><li>Independientemente de si la sustitución de búsqueda del índice se realiza o no, la parte entera del índice es <strong>AND</strong>ed con 2<sup>b</sup> - 1, donde <em>b</em> es el número de bits de un búfer de índice de color.</li><li>A continuación, los índices resultantes o los colores RGBA se convierten en fragmentos adjuntando las coordenadas z <em>-coordinate</em>y texture de la posición de trama actual a cada píxel y, a continuación, asignando las coordenadas de ventana <em></em> <em>x</em> e <em>y</em> al n-th fragmento, como <em>x</em>? = <em>x</em><sub>r</sub>  +  <em>n</em> mod <em>width</em><br /><em>y</em>? = <em>y</em><sub>r</sub>  +  <em>n/width</em><br /> donde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) es la posición de trama actual.<br /></li><li>La <strong>función glDrawPixels</strong> trata estos fragmentos de píxeles igual que los fragmentos generados por puntos de rasterización, líneas o polígonos. Aplica la asignación de texturas, los guiones y todas las operaciones de fragmento antes de escribir los fragmentos en el búfer de fotogramas.</li></ol> | 
| <span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl><dt><strong>GL_STENCIL_INDEX</strong></dt></dl> | Cada píxel es un valor único, un índice de galería de símbolos. <br /><ol><li>La <strong>función glDrawPixels</strong> la convierte al formato de punto fijo, con un número no especificado de bits a la derecha del punto binario, independientemente del tipo de datos de memoria. Los valores de punto flotante se convierten en valores de punto fijo verdaderos. La <strong>función glDrawPixels</strong> convierte datos enteros con signo y sin signo con todos los bits de fracción establecidos en cero. Los datos de mapa de bits se convierten en 0,0 o 1,0.</li><li>La <strong>función glDrawPixels</strong> desplaza cada índice de punto fijo a la izquierda GL_INDEX_SHIFT bits y lo agrega a GL_INDEX_OFFSET. Si GL_INDEX_SHIFT es negativo, el desplazamiento es a la derecha. En cualquier caso, los bits cero rellenan ubicaciones de bits no especificadas en el resultado.</li><li>Si GL_MAP_STENCIL es true, el índice se reemplaza por el valor al que <strong>glDrawPixels</strong> hace referencia en la tabla de búsqueda GL_PIXEL_MAP_S_TO_S.</li><li>Independientemente de si la sustitución de búsqueda del índice se realiza o no, la parte entera del índice es <strong>ENTONCES AND</strong>ed con 2<sup>b</sup> - 1, donde <em>b</em> es el número de bits en el búfer de galería de símbolos. A continuación, los índices de galería de símbolos resultantes se escriben en el búfer de la galería de símbolos de forma que el índice <em>nº</em>se escribe en la ubicación <em>x</em>? = <em>x</em><sub>r</sub>  +  <em>n</em> mod <em>width</em><br /><em>y</em>? = <em>y</em><sub>r</sub>  +  <em>n/width</em><br /> donde (<em>x</em><sub>r</sub> , <em></em> y<sub>r</sub> ) es la posición de trama actual. Solo la prueba de propiedad de píxeles, la prueba de desenlazamiento y la máscara de escritura de la galería de símbolos afectan a estas escrituras.<br /></li></ol> | 
| <span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl><dt><strong>GL_DEPTH_COMPONENT</strong></dt></dl> | Cada píxel es un componente de una sola profundidad. <br /><ol><li>La <strong>función glDrawPixels</strong> convierte los datos de punto flotante directamente en un formato de punto flotante interno con precisión no especificada. Los datos enteros con signo se asignan linealmente al formato de punto flotante interno, de modo que el valor entero representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a -1,0. Los datos enteros sin signo se asignan de forma similar: el valor entero más grande se asigna a 1,0 y cero se asigna a 0,0.</li><li>La <strong>función glDrawPixels</strong> multiplica el valor de profundidad de punto flotante resultante GL_DEPTH_SCALE y lo agrega a GL_DEPTH_BIAS. El resultado se fija en el intervalo [0,1].</li><li>La función <strong>glDrawPixels</strong> convierte los componentes de profundidad resultantes en fragmentos adjuntando el color de la posición de trama <em></em> actual o el índice de color y las coordenadas de textura a cada píxel y, a continuación, asignando las coordenadas de ventana <em>x</em> e <em>y</em> al fragmento n como <em>x</em>? = <em></em>x<sub>r</sub>  +  <em>n</em> mod <em>width</em><br /><em>y</em>? = <em>y</em><sub>r</sub>  +  <em>n/width</em><br /> donde ( <em></em> x<sub>r</sub> ,<em>y</em><sub>r</sub> ) es la posición de trama actual.<br /></li><li>Estos fragmentos de píxeles se tratan como los fragmentos generados al rasterizar puntos, líneas o polígonos. La <strong>función glDrawPixels</strong> aplica la asignación de textura, la textura y todas las operaciones de fragmento antes de escribir los fragmentos en el búfer de fotogramas.</li></ol> | 
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl><dt><strong>GL_RGBA</strong></dt></dl> | Cada píxel es un grupo de cuatro componentes en este orden: rojo, verde, azul, alfa. <br /><ol><li>La <strong>función glDrawPixels</strong> convierte los valores de punto flotante directamente en un formato de punto flotante interno con precisión no especificada. Los valores enteros con signo se asignan linealmente al formato de punto flotante interno, de modo que el valor entero que se puede representar más positivo se asigna a 1,0 y el valor representable más negativo se asigna a -1,0. Los datos enteros sin signo se asignan de forma similar: el valor entero más grande se asigna a 1,0 y cero se asigna a 0,0.</li><li>La <strong>función glDrawPixels</strong> multiplica los valores de color de punto flotante resultantes por GL_c_SCALE y los agrega a GL_c_BIAS, donde <em>c</em> es RED, GREEN, BLUE y ALPHA para los componentes de color respectivos. Los resultados se fijan en el intervalo [0,1].</li><li>Si GL_MAP_COLOR es true, <strong>glDrawPixels</strong> escala cada componente de color por el tamaño de la tabla de búsqueda GL_PIXEL_MAP_c_TO_c y, a continuación, reemplaza el componente por el valor al que hace referencia en esa tabla; <em>c</em> es R, G, B o A, respectivamente.</li><li>La función <em></em> <strong>glDrawPixels</strong> convierte los colores RGBA resultantes en fragmentos mediante la asociación de las coordenadas z -coordinate y texture de la posición de trama actual a cada píxel y, a continuación, asigna las coordenadas de ventana <em>x</em> e <em>y</em> al n fragmento como <em>x</em>? <em></em> = <em>x</em><sub>r</sub>  +  <em>n</em> mod <em>width</em><br /><em>y</em>? = <em>y</em><sub>r</sub>  +  <em>n /width</em><br /> donde (<em>x</em><sub>r</sub> ,<em>y</em><sub>r</sub> ) es la posición de trama actual.<br /></li><li>Estos fragmentos de píxeles se tratan como los fragmentos generados al rasterizar puntos, líneas o polígonos. La <strong>función glDrawPixels</strong> aplica la asignación de textura, la textura y todas las operaciones de fragmento antes de escribir los fragmentos en el búfer de fotogramas.</li></ol> | 
| <span id="GL_RED"></span><span id="gl_red"></span><dl><dt><strong>GL_RED</strong></dt></dl> | Cada píxel es un único componente rojo.<br /> La función <strong>glDrawPixels</strong> convierte este componente al formato de punto flotante interno de la misma manera que el componente rojo de un píxel RGBA y, a continuación, lo convierte en un píxel RGBA con verde y azul establecido en 0,0 y alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl><dt><strong>GL_GREEN</strong></dt></dl> | Cada píxel es un único componente verde.<br /> La función <strong>glDrawPixels</strong> convierte este componente al formato de punto flotante interno de la misma manera que el componente verde de un píxel RGBA y, a continuación, lo convierte en un píxel RGBA con rojo y azul establecido en 0,0 y alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl><dt><strong>GL_BLUE</strong></dt></dl> | Cada píxel es un único componente azul.<br /> La función <strong>glDrawPixels</strong> convierte este componente al formato de punto flotante interno de la misma manera que el componente azul de un píxel RGBA y, a continuación, lo convierte en un píxel RGBA con rojo y verde establecido en 0,0 y alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl><dt><strong>GL_ALPHA</strong></dt></dl> | Cada píxel es un único componente alfa.<br /> La función <strong>glDrawPixels</strong> convierte este componente al formato de punto flotante interno de la misma manera que el componente alfa de un píxel RGBA y, a continuación, lo convierte en un píxel RGBA con rojo, verde y azul establecido en 0,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl><dt><strong>GL_RGB</strong></dt></dl> | Cada píxel es un grupo de tres componentes en este orden: rojo, verde y azul. La <strong>función glDrawPixels</strong> convierte cada componente al formato de punto flotante interno de la misma manera que los componentes rojo, verde y azul de un píxel RGBA. El triple de color se convierte en un píxel RGBA con alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl><dt><strong>GL_LUMINANCE</strong></dt></dl> | Cada píxel es un único componente de luminosidad.<br /> La <strong>función glDrawPixels</strong> convierte este componente al formato de punto flotante interno de la misma manera que el componente rojo de un píxel RGBA y, a continuación, lo convierte en un píxel RGBA con el conjunto rojo, verde y azul en el valor de luminosidad convertido y alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl><dt><strong>GL_LUMINANCE_ALPHA</strong></dt></dl> | Cada píxel es un grupo de dos componentes en este orden: luminance, alpha.<br /> La función <strong>glDrawPixels</strong> convierte los dos componentes en el formato de punto flotante interno de la misma manera que el componente rojo de un píxel RGBA y, a continuación, los convierte en un píxel RGBA con un conjunto rojo, verde y azul en el valor de luminosidad convertido y alfa establecido en el valor alfa convertido. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl><dt><strong>GL_BGR_EXT</strong></dt></dl> | Cada píxel es un grupo de tres componentes en este orden: azul, verde, rojo.<br /> GL_BGR_EXT proporciona un formato que coincide con el diseño de memoria de Windows mapas de bits independientes del dispositivo (DIB). Por lo tanto, las aplicaciones pueden usar los mismos datos con Windows llamadas de función y llamadas de función de píxel openGL.<br /> | 
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl><dt><strong>GL_BGRA_EXT</strong></dt></dl> | Cada píxel es un grupo de cuatro componentes en este orden: azul, verde, rojo, alfa.<br /> GL_BGRA_EXT proporciona un formato que coincide con el diseño de memoria de Windows mapas de bits independientes del dispositivo (DIB). Por lo tanto, las aplicaciones pueden usar los mismos datos con Windows llamadas de función y llamadas de función de píxel openGL.<br /> | 




 

</dd> <dt>

*type* 
</dt> <dd>

Tipo de datos para *píxeles.* Las siguientes son las constantes simbólicas aceptadas y sus significados.



| Valor                                                                                                                                                                      | Significado                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL \_ UNSIGNED \_ BYTE**</dt> </dl>    | Entero de 8 bits sin signo<br/>                 |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ BYTE**</dt> </dl>                                | Entero de 8 bits con signo<br/>                   |
| <span id="GL_BITMAP"></span><span id="gl_bitmap"></span><dl> <dt>**MAPA DE BITS \_ DE GL**</dt> </dl>                          | Bits únicos en enteros de 8 bits sin signo<br/> |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ UNSIGNED \_ SHORT**</dt> </dl> | Entero de 16 bits sin signo<br/>                |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ SHORT**</dt> </dl>                             | Entero de 16 bits con signo<br/>                  |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ UNSIGNED \_ INT**</dt> </dl>       | Entero de 32 bits sin signo<br/>                |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ INT**</dt> </dl>                                   | Entero de 32 bits<br/>                         |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ FLOAT**</dt> </dl>                             | Punto flotante de precisión sencilla<br/>        |



 

</dd> <dt>

*píxeles* 
</dt> <dd>

Puntero a los datos de píxel.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | El *ancho o* alto *era* negativo.<br/>                                                                                                                                          |
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | El *formato* o *el tipo* no era un valor aceptado. <br/>                                                                                                                             |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | *El* formato era GL \_ RED, GL \_ GREEN, GL \_ BLUE, GL \_ ALPHA, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ EXT, GL \_ BGRA \_ EXT, GL \_ LUMINANCE o GL \_ LUMINANCE \_ ALPHA, y OpenGL estaba en modo de índice de colores.<br/> |
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *El tipo* era GL BITMAP y el formato no \_ era GL COLOR INDEX ni GL  \_ \_ \_ STENCIL \_ INDEX.<br/>                                                                                         |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | *format* era GL \_ STENCIL \_ INDEX y no había ningún búfer de galería de símbolos.<br/>                                                                                                                  |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/>                                                        |


## <a name="remarks"></a>Comentarios

La **función glDrawPixels** lee datos de píxeles de la memoria y los escribe en el búfer de fotogramas con respecto a la posición de trama actual. Use [**glRasterPos para**](glrasterpos-functions.md) establecer la posición de trama actual y [**use glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ CURRENT RASTER POSITION para consultar la posición del \_ \_ trama.

Varios parámetros definen la codificación de datos de píxeles en memoria y controlan el procesamiento de los datos de píxel antes de colocarse en el búfer de fotogramas. Estos parámetros se establecen con cuatro funciones: [**glPixelStore,**](glpixelstore-functions.md) [**glPixelTransfer,**](glpixeltransfer.md) [**glPixelMap**](glpixelmap.md)y [**glPixelZoom.**](glpixelzoom.md) En este tema se describen los efectos en **glDrawPixels** de muchos, pero no todos, de los parámetros especificados por estas cuatro funciones.

Los datos  se leen desde píxeles como una secuencia de bytes con o sin signo, shorts con o sin signo, enteros con o sin signo, o valores de punto flotante de precisión sencilla, según el tipo *.* Cada uno de estos bytes, shorts, enteros o valores de punto flotante se interpreta como un componente de color o profundidad, o un índice, según el *formato*. Los índices siempre se tratan individualmente. Los componentes de color se tratan como grupos de uno, dos, tres o cuatro valores, de nuevo en función del *formato*. Tanto los índices individuales como los grupos de componentes se conocen como píxeles. Si *type* es GL BITMAP, los datos deben ser bytes sin signo y el formato debe ser \_ GL COLOR INDEX o GL  \_ \_ \_ STENCIL \_ INDEX. Cada byte sin signo se trata como ocho píxeles de 1 bit, con ordenación de bits determinada por GL \_ UNPACK \_ LSB \_ FIRST (vea [**glPixelStore).**](glpixelstore-functions.md)

El *ancho por* *píxeles de alto* se lee de la memoria, empezando por los píxeles de *ubicación.* De forma predeterminada, estos píxeles se toman  de ubicaciones de memoria adyacentes, salvo que, una vez leídos todos los píxeles de ancho, el puntero de lectura avanza al siguiente límite de 4 bytes. La **función glPixelStore** especifica la alineación de filas de 4 bytes con el argumento GL UNPACK ALIGNMENT y se puede establecer en \_ \_ 1, 2, 4 u 8 bytes. Otros parámetros de almacén de píxeles especifican diferentes avances de  puntero de lectura, tanto antes de leer el primer píxel como después de leer todos los píxeles de ancho. La **función glPixelStore** funciona en  cada uno de los píxeles ancho por alto que lee de la memoria de la misma manera, en función de los valores de varios parámetros especificados por [**glPixelTransfer**](glpixeltransfer.md) y [**glPixelMap.**](glpixelmap.md) Los detalles de estas operaciones, así como el búfer de destino en el que se dibujan los píxeles, son específicos del formato de los píxeles, como se especifica mediante *el formato*.

La rasterización descrita hasta ahora supone factores de zoom de píxeles de 1,0. Si usa [**glPixelZoom**](glpixelzoom.md) para  cambiar los factores de zoom de píxel x e *y,* los píxeles se convierten en fragmentos como se muestra a continuación. Si (*xr, yr*) es la posición de trama actual y un píxel determinado está en la n columna y la fila *mth* del rectángulo de píxeles, se generan fragmentos para píxeles cuyos centros están en el rectángulo con esquinas en

(*x*<sub>r</sub>  +  *zoom*? *n*, *y*<sub>r</sub>  +  *zoom*<sub>y</sub> *m*)

(*x*<sub>r</sub>  +  *zoom*? (*n* + 1), *y*<sub>r</sub>  +  *zoom*<sub>y</sub> (*m* + 1))

where *zoom*? es el valor de GL \_ ZOOM X y \_ *zoom*<sub>y</sub> es el valor de GL \_ ZOOM \_ Y.

Las siguientes funciones recuperan información relacionada **con glDrawPixels**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ CURRENT RASTER \_ \_ POSITION

**glGet con** el argumento GL \_ CURRENT RASTER POSITION \_ \_ \_ VALID

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 





