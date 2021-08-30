---
title: Función glColorTableEXT (Gl.h)
description: La función glColorTableEXT especifica el formato y el tamaño de una paleta para las texturas de paleta de destino.
ms.assetid: f3d7b1a1-97a5-47ef-a0ca-5e58acb86bb4
keywords:
- Función glColorTableEXT OpenGL
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
ms.openlocfilehash: 0f42a0be9d2cd9b39a86a9f55d776c61b25fa448
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475381"
---
# <a name="glcolortableext-function"></a>Función glColorTableEXT

La **función glColorTableEXT** especifica el formato y el tamaño de una paleta para las texturas de paleta de destino.

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

Textura de destino a la que se va a cambiar la paleta. Debe ser TEXTURE \_ 1D, TEXTURE \_ 2D, PROXY \_ TEXTURE \_ 1D o PROXY \_ TEXTURE \_ 2D.

</dd> <dt>

*internalFormat* 
</dt> <dd>

Formato interno y resolución de la paleta. Este parámetro puede suponer uno de los siguientes valores simbólicos.



| Constante       | Formato base | R Bits | G Bits | B Bits | A Bits |
|----------------|-------------|--------|--------|--------|--------|
| GL \_ R3 \_ G3 \_ B2 | GL \_ RGB     | 3      | 3      | 2      |        |
| GL \_ RGB4       | GL \_ RGB     | 4      | 4      | 4      |        |
| GL \_ RGB5       | GL \_ RGB     | 5      | 5      | 5      |        |
| GL \_ RGB8       | GL \_ RGB     | 8      | 8      | 8      |        |
| GL \_ RGB10      | GL \_ RGB     | 10     | 10     | 10     |        |
| GL \_ RGB12      | GL \_ RGB     | 12     | 12     | 12     |        |
| GL \_ RGB16      | GL \_ RGB     | 16     | 16     | 16     |        |
| GL \_ RGBA2      | GL \_ RGBA    | 2      | 2      | 2      | 2      |
| GL \_ RGBA4      | GL \_ RGBA    | 4      | 4      | 4      | 4      |
| GL \_ RGB5 \_ A1   | GL \_ RGBA    | 5      | 5      | 5      | 1      |
| GL \_ RGBA8      | GL \_ RGBA    | 8      | 8      | 8      | 8      |
| GL \_ RG10 \_ A2   | GL \_ RGBA    | 10     | 10     | 10     | 2      |
| GL \_ RGB12      | GL \_ RGBA    | 12     | 12     | 12     | 12     |
| GL \_ RGBA16     | GL \_ RGBA    | 16     | 16     | 16     | 16     |



 

</dd> <dt>

*width* 
</dt> <dd>

Tamaño de la paleta. Debe ser 2n = 1 para algún entero *n*.

</dd> <dt>

*format* 
</dt> <dd>

Formato de los datos de píxeles. Se aceptan las siguientes constantes simbólicas.




| Valor | Significado | 
|-------|---------|
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl><dt><strong>GL_RGBA</strong></dt></dl> | Cada píxel es un grupo de cuatro componentes en este orden: rojo, verde, azul, alfa. El formato RGBA se determina de esta manera: <br /><ol><li>La <strong>función glColorTableEXT</strong> convierte los valores de punto flotante directamente en un formato interno con precisión no especificada. Los valores enteros con signo se asignan linealmente al formato interno, de modo que el valor entero representable más positivo se asigna a 1,0 y el valor entero representable más negativo se asigna a -1,0. Los datos enteros sin signo se asignan de forma similar: el valor entero más grande se asigna a 1,0 y cero se asigna a 0,0.</li><li>La <strong>función glColorTableEXT</strong> multiplica los valores de color resultantes por GL_c_SCALE y los agrega a GL_c_BIAS, donde <em>c</em> es RED, GREEN, BLUE y ALPHA para los componentes de color respectivos. Los resultados se fijan en el intervalo [0,1].</li><li>Si GL_MAP_COLOR es <strong>TRUE,</strong> <strong>glColorTableEXT</strong> escala cada componente de color por el tamaño de la tabla de búsqueda GL_PIXEL_MAP_c_TO_c, reemplaza el componente por el valor al que hace referencia en esa tabla; <em>c</em> es R, G, B o A, respectivamente.</li><li>La función <em></em> <strong>glColorTableEXT</strong> convierte los colores RGBA resultantes en fragmentos mediante la asociación de las coordenadas z -coordinate y texture de la posición de trama actual a cada píxel y, a continuación, asigna las coordenadas de ventana <em>x</em> e <em>y</em> al n fragmento como<em>x</em>? <em></em> = <em>x</em><sub>r</sub>  +  <em>n</em> mod <em>width</em><br /><em></em>y? = <em>y</em><sub>r</sub>  + <em>n/ width</em><br /> donde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) es la posición de trama actual.<br /></li><li>Estos fragmentos de píxeles se tratan como los fragmentos generados al rasterizar puntos, líneas o polígonos. La <strong>función glColorTableEXT</strong> aplica la asignación de texturas, la textura y todas las operaciones de fragmento antes de escribir los fragmentos en el búfer de fotogramas.</li></ol> | 
| <span id="GL_RED"></span><span id="gl_red"></span><dl><dt><strong>GL_RED</strong></dt></dl> | Cada píxel es un único componente rojo.<br /> La función <strong>glColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente rojo de un píxel RGBA y, a continuación, lo convierte en un píxel RGBA con verde y azul establecido en 0,0 y alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl><dt><strong>GL_GREEN</strong></dt></dl> | Cada píxel es un único componente verde.<br /> La función <strong>glColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente verde de un píxel RGBA y, a continuación, lo convierte en un píxel RGBA con rojo y azul establecido en 0,0 y alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl><dt><strong>GL_BLUE</strong></dt></dl> | Cada píxel es un único componente azul.<br /> La función <strong>glColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente azul de un píxel RGBA y, a continuación, lo convierte en un píxel RGBA con rojo y verde establecido en 0,0 y alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl><dt><strong>GL_ALPHA</strong></dt></dl> | Cada píxel es un único componente alfa.<br /> La función <strong>glColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente alfa de un píxel RGBA y, a continuación, lo convierte en un píxel RGBA con rojo, verde y azul establecido en 0,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl><dt><strong>GL_RGB</strong></dt></dl> | Cada píxel es un grupo de tres componentes en este orden: rojo, verde y azul.<br /> La <strong>función glColorTableEXT</strong> convierte cada componente al formato interno de la misma manera que los componentes rojo, verde y azul de un píxel RGBA. El triple de color se convierte en un píxel RGBA con alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl><dt><strong>GL_BGR_EXT</strong></dt></dl> | Cada píxel es un grupo de tres componentes en este orden: azul, verde, rojo.<br /> GL_BGR_EXT proporciona un formato que coincide con el diseño de memoria de Windows mapas de bits independientes del dispositivo (DIB). Por lo tanto, las aplicaciones pueden usar los mismos datos con las Windows de función y las llamadas de función de píxel de OpenGL.<br /> | 
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl><dt><strong>GL_BGRA_EXT</strong></dt></dl> | Cada píxel es un grupo de cuatro componentes en este orden: azul, verde, rojo y alfa.<br /> GL_BGRA_EXT proporciona un formato que coincide con el diseño de memoria de Windows mapas de bits independientes del dispositivo (DIB). Por lo tanto, las aplicaciones pueden usar los mismos datos con las Windows de función y las llamadas de función de píxel de OpenGL.<br /> | 




 

</dd> <dt>

*type* 
</dt> <dd>

Tipo de datos para *los datos*. Se aceptan las siguientes constantes simbólicas: GL \_ UNSIGNED \_ BYTE, GL \_ BYTE, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT y GL \_ FLOAT.

En la tabla siguiente se resume el significado de las constantes válidas para el *parámetro de* tipo.



| Valor                                                                                                                                                                      | Significado                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL \_ UNSIGNED \_ BYTE**</dt> </dl>    | Entero de 8 bits sin signo<br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ BYTE**</dt> </dl>                                | Entero de 8 bits con signo<br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL \_ UNSIGNED \_ SHORT**</dt> </dl> | Entero de 16 bits sin signo<br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ SHORT**</dt> </dl>                             | Entero de 16 bits con signo<br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL \_ UNSIGNED \_ INT**</dt> </dl>       | Entero de 32 bits sin signo<br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ INT**</dt> </dl>                                   | Entero de 32 bits<br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ FLOAT**</dt> </dl>                             | Valor de punto flotante de precisión sencilla<br/> |



 

</dd> <dt>

*data* 
</dt> <dd>

Puntero a los datos de textura paleta. Los datos se tratan como píxeles individuales de una entrada de paleta de textura 1D para una entrada de paleta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *width* era un entero no válido.<br/>                                                                                            |
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *target*, *internalFormat*, *format* o *type* no era un valor aceptado.<br/>                                                 |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

Las texturas de paleta se definen con una paleta de colores y un conjunto de datos de imagen que se compone de índices para las entradas de color de una paleta (una tabla de colores).

La **función glColorTableEXT** especifica la paleta de texturas de una textura de destino. Toma los datos *de la* memoria y convierte los datos como si cada entrada de la paleta fuera un solo píxel de una textura 1D. La **función glColorTableEXT** desempaqueta y convierte los datos y los  convierte en un formato interno que coincida con el formato especificado lo más cerca posible.

Si el ancho de *una* paleta es mayor que el intervalo de los índices de color de los datos de textura, algunas de las entradas de la paleta no se usan. Si el ancho  de una paleta es menor que el intervalo de los índices de color de los datos de textura, se omiten los bits más significativos de los datos de textura y solo se usa el número adecuado de bits del índice al acceder a la paleta. Cuando se especifica un destino *de* proxy mediante PROXY \_ TEXTURE 1D o PROXY TEXTURE \_ \_ 2D, se cambia el tamaño de la paleta de la textura del proxy y se establecen sus parámetros, pero no se transfiere ni se accede a ningún \_ dato.

Cuando  el parámetro de destino es GL PROXY TEXTURE 1D o GL PROXY TEXTURE 2D y la implementación no admite los valores especificados para formato o \_ \_ \_ \_ \_ \_ ancho, **glColorTableEXT**  puede no crear la tabla de colores solicitada. En este caso, la tabla de colores está vacía y todos los parámetros recuperados serán cero. Puede determinar si OpenGL admite un formato y un tamaño de tabla de colores determinados llamando a **glColorTableEXT** con un destino de proxy y, a continuación, llamando a [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) o [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) para determinar si el parámetro width coincide con el establecido por **glColorTableEXT**. Si el ancho recuperado es cero, error en la solicitud de tabla de colores **de glColorTable.** Si el ancho recuperado no es cero, puede llamar a **glColorTable** con el destino real con TEXTURE 1D o TEXTURE 2D para establecer \_ \_ la tabla de colores.

> [!Note]  
> La **función glColorTableEXT** es una función de extensión que no forma parte de la biblioteca OpenGL estándar, pero forma parte de la extensión de textura de paleta \_ GL \_ \_ EXT. Para comprobar si la implementación de OpenGL admite **glColorTableEXT,** llame [**a glGetString**](glgetstring.md)(GL \_ EXTENSIONS). Si devuelve la textura \_ de paleta GL \_ \_ EXT, se admite **glColorTableEXT.** Para obtener la dirección de función de una función de extensión, llame [**a wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

 

Para recuperar los datos reales de la tabla de colores especificados por la **función glColorTableEXT,** llame [**a glGetColorTableEXT**](glgetcolortableext.md). Para recuperar los parámetros, como *el* ancho y el *formato,* de la tabla de colores especificada por la función **glColorTableEXT,** llame a la función **glGetColorTableParameterivEXT** o **glGetColorTableParameterfvEXT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 





