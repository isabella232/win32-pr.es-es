---
title: Función glColorSubTableEXT (Gl.h)
description: La función glColorSubTableEXT especifica una parte de la paleta de la textura de destino que se va a reemplazar.
ms.assetid: 21430245-f837-4c7a-944f-b44482254b12
keywords:
- Función glColorSubTableEXT OpenGL
topic_type:
- apiref
api_name:
- glColorSubTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff6f4b88a355c25df40a847912d4e3352bd87962
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475401"
---
# <a name="glcolorsubtableext-function"></a>Función glColorSubTableEXT

La **función glColorSubTableEXT** especifica una parte de la paleta de la textura de destino que se va a reemplazar.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glColorSubTableEXT(
         GLenum  target,
         GLsizei start,
         GLsizei count,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Textura de la paleta de destino a la que se va a cambiar la paleta. Debe ser TEXTURE \_ 1D o TEXTURE \_ 2D.

</dd> <dt>

*start* 
</dt> <dd>

Entrada de índice de la paleta inicial de la paleta que se va a cambiar.

</dd> <dt>

*count* 
</dt> <dd>

Número de entradas de índice de paleta de la paleta que se va a cambiar a partir de *al principio.* El *parámetro count* determina el intervalo de entradas de índice de la paleta que se cambian.

</dd> <dt>

*format* 
</dt> <dd>

Formato de los datos de píxeles. Se aceptan las siguientes constantes simbólicas.




| Valor | Significado | 
|-------|---------|
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl><dt><strong>GL_RGBA</strong></dt></dl> | Cada píxel es un grupo de cuatro componentes en el orden siguiente: rojo, verde, azul, alfa. El formato RGBA se determina de esta manera: <br /><ol><li>La <strong>función glColorSubTableEXT</strong> convierte los valores de punto flotante directamente en un formato interno con precisión no especificada. Los valores enteros con signo se asignan linealmente al formato interno, de modo que el valor entero representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a -1,0. Los datos enteros sin signo se asignan de forma similar: el valor entero más grande se asigna a 1,0 y cero se asigna a 0,0.</li><li>La <strong>función glColorSubTableEXT</strong> multiplica los valores de color resultantes por GL_c_SCALE y los agrega a GL_c_BIAS, donde <em>c</em> es RED, GREEN, BLUE y ALPHA para los componentes de color respectivos. Los resultados se fijan en el intervalo [0,1].</li><li>Si GL_MAP_COLOR es <strong>TRUE,</strong> <strong>glColorSubTableEXT</strong> escala cada componente de color por el tamaño de la tabla de búsqueda GL_PIXEL_MAP_c_TO_c y, a continuación, reemplaza el componente por el valor al que hace referencia en esa tabla; <em>c</em> es R, G, B o A, respectivamente.</li><li>La función <em></em> <strong>glColorSubTableEXT</strong> convierte los colores RGBA resultantes en fragmentos adjuntando las coordenadas de textura y coordenada <em>z</em>de posición de trama actual a cada píxel y, a continuación, asignando coordenadas de ventana <em>x</em> e <em>y</em> al n fragmento como<em>x</em>? = <em>x</em><sub>r</sub>  +  <em>n</em> mod <em>width</em><br /><em>y</em>? = <em>y</em><sub>r</sub>  + <em>n/ width</em><br /> donde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) es la posición de trama actual.<br /></li><li>Estos fragmentos de píxeles se tratan como los fragmentos generados al rasterizar puntos, líneas o polígonos. La <strong>función glColorSubTableEXT</strong> aplica la asignación de textura, la textura y todas las operaciones de fragmento antes de escribir los fragmentos en el búfer de fotogramas.</li></ol> | 
| <span id="GL_RED"></span><span id="gl_red"></span><dl><dt><strong>GL_RED</strong></dt></dl> | Cada píxel es un único componente rojo.<br /> La función <strong>glColorSubTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente rojo de un píxel RGBA, lo convierte en un píxel RGBA con verde y azul establecido en 0,0 y alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl><dt><strong>GL_GREEN</strong></dt></dl> | Cada píxel es un único componente verde.<br /> La función <strong>glColorSubTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente verde de un píxel RGBA y, a continuación, lo convierte en un píxel RGBA con rojo y azul establecido en 0,0 y alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl><dt><strong>GL_BLUE</strong></dt></dl> | Cada píxel es un único componente azul.<br /> La función <strong>glColorSubTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente azul de un píxel RGBA y, a continuación, lo convierte en un píxel RGBA con rojo y verde establecido en 0,0 y alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl><dt><strong>GL_ALPHA</strong></dt></dl> | Cada píxel es un único componente alfa.<br /> La función <strong>glColorSubTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente alfa de un píxel RGBA y, a continuación, lo convierte en un píxel RGBA con rojo, verde y azul establecido en 0,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl><dt><strong>GL_RGB</strong></dt></dl> | Cada píxel es un grupo de tres componentes en este orden: rojo, verde y azul.<br /> La <strong>función glColorSubTableEXT</strong> convierte cada componente al formato interno de la misma manera que los componentes rojo, verde y azul de un píxel RGBA. El triple de color se convierte en un píxel RGBA con alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br /> | 
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



| Nombre                                                                                              | Significado                                                                                                                               |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl> | *start* o *count* era un entero no válido.<br/>                                                                                 |
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>  | *target*, *format*,or *type* was not an accepted value.<br/>                                                                    |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glColorSubTableEXT** especifica partes de la paleta de la textura de destino actual que se va a reemplazar. A [**diferencia de glColorTableEXT,**](glcolortableext.md)no se puede especificar el parámetro *de* destino para que sea una paleta de texturas de proxy.

> [!Note]  
> La **función glColorSubTableEXT** es una función de extensión que no forma parte de la biblioteca OpenGL estándar, pero forma parte de la extensión de textura de paleta \_ GL \_ \_ EXT. Para comprobar si la implementación de OpenGL admite **glColorSubTableEXT,** llame [**a glGetString**](glgetstring.md)(GL \_ EXTENSIONS). Si devuelve la textura \_ de paleta GL \_ \_ EXT, se admite **glColorSubTableEXT.** Para obtener la dirección de función de una función de extensión, llame [**a wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

 

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

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





