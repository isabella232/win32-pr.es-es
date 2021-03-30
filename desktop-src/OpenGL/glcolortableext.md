---
title: función glColorTableEXT (GL. h)
description: La función glColorTableEXT especifica el formato y el tamaño de una paleta para las texturas de paletas de destino.
ms.assetid: f3d7b1a1-97a5-47ef-a0ca-5e58acb86bb4
keywords:
- glColorTableEXT (función) OpenGL
topic_type:
- apiref
api_name:
- glColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0d5fd5c848e787f480e3e1893b9b25e4bbd3de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802809"
---
# <a name="glcolortableext-function"></a>glColorTableEXT función)

La función **glColorTableEXT** especifica el formato y el tamaño de una paleta para las texturas de paletas de destino.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glColorTableEXT(
         GLenum  target,
         GLenum  internalFormat,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Textura de destino que va a cambiar su paleta. Debe ser la textura \_ 1D, textura \_ 2D, \_ textura de proxy \_ 1D o \_ textura de proxy \_ 2D.

</dd> <dt>

*internalFormat* 
</dt> <dd>

El formato interno y la resolución de la paleta. Este parámetro puede suponer uno de los siguientes valores simbólicos.



| Constante       | Formato base | Bits R | G bits | Bits B | Un bits |
|----------------|-------------|--------|--------|--------|--------|
| GL \_ R3 \_ G3 \_ B2 | RGB de GL \_     | 3      | 3      | 2      |        |
| GL \_ RGB4       | RGB de GL \_     | 4      | 4      | 4      |        |
| GL \_ RGB5       | RGB de GL \_     | 5      | 5      | 5      |        |
| GL \_ RGB8       | RGB de GL \_     | 8      | 8      | 8      |        |
| GL \_ RGB10      | RGB de GL \_     | 10     | 10     | 10     |        |
| GL \_ RGB12      | RGB de GL \_     | 12     | 12     | 12     |        |
| GL \_ RGB16      | RGB de GL \_     | 16     | 16     | 16     |        |
| GL \_ RGBA2      | el \_ RGBA de GL    | 2      | 2      | 2      | 2      |
| GL \_ RGBA4      | el \_ RGBA de GL    | 4      | 4      | 4      | 4      |
| GL \_ RGB5 \_ a1   | el \_ RGBA de GL    | 5      | 5      | 5      | 1      |
| GL \_ RGBA8      | el \_ RGBA de GL    | 8      | 8      | 8      | 8      |
| GL \_ RG10 \_ a2   | el \_ RGBA de GL    | 10     | 10     | 10     | 2      |
| GL \_ RGB12      | el \_ RGBA de GL    | 12     | 12     | 12     | 12     |
| GL \_ RGBA16     | el \_ RGBA de GL    | 16     | 16     | 16     | 16     |



 

</dd> <dt>

*width* 
</dt> <dd>

Tamaño de la paleta. Debe ser 2N = 1 para algún entero *n*.

</dd> <dt>

*format* 
</dt> <dd>

Formato de los datos de píxeles. Se aceptan las siguientes constantes simbólicas.



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
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt><strong>GL_RGBA</strong></dt> </dl></td>
<td>Cada píxel es un grupo de cuatro componentes en este orden: rojo, verde, azul, alfa. El formato RGBA se determina de esta manera: <br/>
<ol>
<li>La función <strong>glColorTableEXT</strong> convierte los valores de punto flotante directamente a un formato interno con una precisión no especificada. Los valores enteros con signo se asignan linealmente al formato interno, de modo que el valor entero representable más positivo se asigna a 1,0 y el valor entero representable más negativo se asigna a-1,0. Los datos enteros sin signo se asignan de forma similar: el valor entero más grande se asigna a 1,0 y cero se asigna a 0,0.</li>
<li>La función <strong>glColorTableEXT</strong> multiplica los valores de color resultantes por GL_c_SCALE y los agrega a GL_c_BIAS, donde <em>c</em> es rojo, verde, azul y alfa para los componentes de color respectivos. Los resultados se fijan en el intervalo [0, 1].</li>
<li>Si GL_MAP_COLOR es <strong>true</strong>, <strong>glColorTableEXT</strong> escala cada componente de color por el tamaño de la tabla de búsqueda GL_PIXEL_MAP_c_TO_c y, a continuación, reemplaza el componente por el valor al que hace referencia en esa tabla; <em>c</em> es R, G, B o A, respectivamente.</li>
<li>La función <strong>glColorTableEXT</strong> convierte los colores RGBA resultantes en fragmentos adjuntando las coordenadas <em>z</em>y de textura de la posición de la trama actual a cada píxel y asignando las coordenadas de la ventana <em>x</em> e <em>y</em> al fragmento <em>n</em>, tal que<em>x</em>? = <em>ancho</em> <em>x</em><sub>r</sub> + <em>n</em> mod<br/> <em></em>sí? = <em></em><sub></sub> +<em>n/ancho</em> de r<br/> donde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) es la posición de la trama actual.<br/></li>
<li>Estos fragmentos de píxeles se tratan a continuación como los fragmentos generados mediante la rasterización de puntos, líneas o polígonos. La función <strong>glColorTableEXT</strong> aplica la asignación de texturas, la niebla y todas las operaciones de fragmento antes de escribir los fragmentos en el fotogramas.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Cada píxel es un único componente rojo.<br/> La función <strong>glColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente rojo de un píxel RGBA es, lo convierte en un píxel RGBA con el verde y el azul establecidos en 0,0 y el valor alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Cada píxel es un único componente verde.<br/> La función <strong>glColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente verde de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con el rojo y el azul establecidos en 0,0 y el alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Cada píxel es un único componente azul.<br/> La función <strong>glColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente azul de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con rojo y verde establecido en 0,0 y el valor alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Cada píxel es un único componente alfa.<br/> La función <strong>glColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente alfa de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con rojo, verde y azul establecido en 0,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Cada píxel es un grupo de tres componentes en este orden: rojo, verde, azul.<br/> La función <strong>glColorTableEXT</strong> convierte cada componente al formato interno de la misma manera que los componentes rojo, verde y azul de un píxel RGBA. El color triple se convierte en un píxel RGBA con el valor alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>Cada píxel es un grupo de tres componentes en este orden: azul, verde, rojo.<br/> GL_BGR_EXT proporciona un formato que coincide con el diseño de memoria de los mapas de bits independientes del dispositivo (DIB) de Windows. Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt><strong>GL_BGRA_EXT</strong></dt> </dl></td>
<td>Cada píxel es un grupo de cuatro componentes en este orden: azul, verde, rojo y alfa.<br/> GL_BGRA_EXT proporciona un formato que coincide con el diseño de memoria de los mapas de bits independientes del dispositivo (DIB) de Windows. Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*type* 
</dt> <dd>

El tipo de datos para los *datos*. Se aceptan las constantes simbólicas siguientes: \_ byte sin signo de GL \_ , GL \_ byte, GL \_ sin signo \_ Short, GL \_ Short, GL \_ unsigned \_ int, GL \_ int y GL \_ float.

En la tabla siguiente se resume el significado de las constantes válidas para el parámetro de *tipo* .



| Value                                                                                                                                                                      | Significado                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**\_byte sin signo de \_ GL**</dt> </dl>    | Entero de 8 bits sin signo<br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**BYTE de GL \_**</dt> </dl>                                | Entero de 8 bits con signo<br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**libro de contabilidad \_ corto sin signo \_**</dt> </dl> | Entero de 16 bits sin signo<br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**CONTABILIDAD \_ breve**</dt> </dl>                             | Entero de 16 bits con signo<br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**libro de contabilidad \_ sin signo \_**</dt> </dl>       | Entero de 32 bits sin signo<br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ int**</dt> </dl>                                   | Entero de 32 bits<br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**valor \_ float de GL**</dt> </dl>                             | Valor de punto flotante de precisión sencilla<br/> |



 

</dd> <dt>

*data* 
</dt> <dd>

Puntero a los datos de textura de la paleta. Los datos se tratan como píxeles individuales de una entrada de la paleta de texturas 1D para una entrada de la paleta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *ancho* era un entero no válido.<br/>                                                                                            |
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *destino*, *internalFormat*, *formato* o *tipo* no era un valor aceptado.<br/>                                                 |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Las texturas de paleta se definen con una paleta de colores y un conjunto de datos de imagen compuesto por índices para las entradas de color de una paleta (una tabla de colores).

La función **glColorTableEXT** especifica la paleta de textura de una textura de destino. Toma los *datos* de la memoria y convierte los datos como si cada entrada de la paleta es un píxel individual de una textura 1D. La función **glColorTableEXT** desempaqueta y convierte los datos y los convierte en un formato interno que coincida lo más posible con el *formato* especificado.

Si el *ancho* de una paleta es mayor que el intervalo de los índices de color de los datos de textura, algunas de las entradas de la paleta no se usan. Si el *ancho* de una paleta es menor que el intervalo de los índices de color de los datos de textura, se omiten los bits más significativos de los datos de textura y solo se usa el número adecuado de bits del índice al obtener acceso a la paleta. Cuando se especifica un *destino* de proxy mediante la \_ textura \_ 1D de proxy o \_ \_ la textura de proxy 2D, se cambia el tamaño de la paleta de la textura del proxy y se establecen sus parámetros, pero no se transfiere ni se obtiene acceso a los datos.

Cuando el parámetro de *destino* es \_ GL \_ proxy Texture \_ 1D o GL \_ proxy \_ Texture \_ 2D, y la implementación no admite los valores especificados para el *formato* o el *ancho*, **glColorTableEXT** puede generar un error al crear la tabla de colores solicitada. En este caso, la tabla de colores está vacía y todos los parámetros recuperados serán cero. Puede determinar si OpenGL admite un formato y un tamaño de tabla de colores determinados mediante una llamada a **glColorTableEXT** con un destino de proxy y, a continuación, llamar a [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) o [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) para determinar si el parámetro de ancho coincide con el establecido por **glColorTableEXT**. Si el ancho recuperado es cero, se produce un error en la solicitud de tabla de colores por **glColorTable** . Si el ancho recuperado no es cero, puede llamar a **glColorTable** con el destino real con la textura \_ 1D o textura \_ 2D para establecer la tabla de colores.

> [!Note]  
> La función **glColorTableEXT** es una función de extensión que no forma parte de la biblioteca estándar de OpenGL, pero que forma parte de la extensión de textura de la paleta de GL \_ ext \_ \_ . Para comprobar si la implementación de OpenGL es compatible con **glColorTableEXT**, llame a [**glGetString**](glgetstring.md)(extensiones de GL \_ ). Si devuelve la \_ \_ textura de paleta ext \_ de GL, se admite **glColorTableEXT** . Para obtener la dirección de la función de una función de extensión, llame a [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

 

Para recuperar los datos de la tabla de colores reales especificados por la función **glColorTableEXT** , llame a [**glGetColorTableEXT**](glgetcolortableext.md). Para recuperar los parámetros, como el *ancho* y el *formato*, de la tabla de colores especificada por la función **glColorTableEXT** , llame a la función **glGetColorTableParameterivEXT** o **glGetColorTableParameterfvEXT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                            |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





