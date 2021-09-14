---
title: Función glTexImage2D (Gl.h)
description: La función glTexImage2D especifica una imagen de textura bidimensional.
ms.assetid: e8b9c692-5239-47de-86eb-80c247c60e1d
keywords:
- Función glTexImage2D OpenGL
topic_type:
- apiref
api_name:
- glTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba2d5bc6f966d9b10c0dadccb221086e64de827
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169241"
---
# <a name="glteximage2d-function"></a>Función glTexImage2D

La **función glTexImage2D** especifica una imagen de textura bidimensional.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glTexImage2D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLsizei height,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Textura de destino. Debe ser GL \_ TEXTURE \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Número de nivel de detalle. El nivel 0 es el nivel de imagen base. El *nivel n* es la imagen *de* reducción de mipmap n.

</dd> <dt>

*internalformat* 
</dt> <dd>

Número de componentes de color de la textura. Debe ser 1, 2, 3 o 4, o una de las siguientes constantes simbólicas: GL \_ ALPHA, GL \_ ALPHA4, GL \_ ALPHA8, GL \_ ALPHA12, GL \_ ALPHA16, GL \_ LUMINANCE, GL \_ \_ LUMINANCE4, GL LUMINANCE8, GL \_ \_ LUMINANCE12, GL LUMINANCE16, GL \_ LUMINANCE \_ ALPHA, GL \_ LUMINANCE4 \_ ALPHA4, GL \_ LUMINANCE6 \_ ALPHA2, GL \_ LUMINANCE8 \_ ALPHA8, GL \_ LUMINANCE12 \_ ALPHA4, GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 \_ ALPHA16, GL INTENSITY, GL LUMINANCE16 ALPHA16, GL \_ INTENSITY GL \_ INTENSITY4, GL \_ INTENSITY8, GL \_ INTENSITY12, GL \_ INTENSITY16, GL \_ R3 \_ G3 \_ B2, GL \_ RGB, GL \_ RGB4, GL \_ \_ RGB5, GL RGB8, GL \_ RGB10, GL \_ RGB12, GL \_ RGB16, GL \_ RGBA, GL \_ RGBA2, GL \_ RGBA4, GL \_ RGB5 \_ A1, GL \_ RGBA8, GL \_ RGB10 \_ A2, GL \_ RGBA12 o GL \_ RGBA16.

</dd> <dt>

*width* 
</dt> <dd>

Ancho de la imagen de textura. Debe ser 2 *n* + 2(*borde*) para algún entero *n*.

</dd> <dt>

*height* 
</dt> <dd>

Alto de la imagen de textura. Debe ser 2 *<sup>m</sup>* + 2(*borde*) para algún entero *m*.

</dd> <dt>

*Frontera* 
</dt> <dd>

Ancho del borde. Debe ser 0 o 1.

</dd> <dt>

*format* 
</dt> <dd>

Formato de los datos de píxel. Puede suponer uno de los nueve valores simbólicos.



| Value                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**GL \_ COLOR \_ INDEX**</dt> </dl>             | Cada elemento es un valor único, un índice de color. Se convierte en punto fijo (con un número no especificado de 0 bits a la derecha del punto binario), se desplaza a la izquierda o a la derecha según el valor y el signo de GL INDEX SHIFT y se agrega a \_ \_ GL INDEX OFFSET \_ \_ (vea [**glPixelTransfer).**](glpixeltransfer.md) El índice resultante se convierte en un conjunto de componentes de color mediante las tablas GL PIXEL MAP I TO R, GL PIXEL MAP I TO G, GL PIXEL MAP I TO B y GL PIXEL MAP I TO A, y se fija en el \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ intervalo \_ \_ \_ \_ \_ \_ \_ \_ \[ 0,1. \]<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**GL \_ RED**</dt> </dl>                                      | Cada elemento es un único componente rojo. Se convierte en punto flotante y se ensambla en un elemento RGBA adjuntando 0,0 para verde y azul, y 1,0 para alfa. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea **glPixelTransfer).**<br/>                                                                                                                                                                                               |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**GL \_ GREEN**</dt> </dl>                                | Cada elemento es un único componente verde. Se convierte en punto flotante y se ensambla en un elemento RGBA adjuntando 0,0 para rojo y azul, y 1,0 para alfa. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea [**glPixelTransfer).**](glpixeltransfer.md)<br/>                                                                                                                                                                        |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**GL \_ BLUE**</dt> </dl>                                   | Cada elemento es un único componente azul. Se convierte en punto flotante y se ensambla en un elemento RGBA adjuntando 0,0 para rojo y verde, y 1,0 para alfa. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea **glPixelTransfer).**<br/>                                                                                                                                                                                               |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**GL \_ ALPHA**</dt> </dl>                                | Cada elemento es un único componente rojo. Se convierte en punto flotante y se ensambla en un elemento RGBA adjuntando 0,0 para rojo, verde y azul. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea [**glPixelTransfer).**](glpixeltransfer.md)<br/>                                                                                                                                                                                     |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**GL \_ RGB**</dt> </dl>                                      | Cada elemento es un triple RGB. Se convierte en punto flotante y se ensambla en un elemento RGBA adjuntando 1.0 para alfa. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea **glPixelTransfer).**<br/>                                                                                                                                                                                                                                    |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**GL \_ RGBA**</dt> </dl>                                   | Cada elemento es un elemento RGBA completo. Se convierte en punto flotante. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea [**glPixelTransfer).**](glpixeltransfer.md)<br/>                                                                                                                                                                                                                                                                 |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt>**GL \_ BGR \_ EXT**</dt> </dl>                         | Cada píxel es un grupo de tres componentes en este orden: azul, verde, rojo.<br/> GL BGR EXT proporciona un formato que coincide con el diseño de memoria de Windows mapas de bits independientes \_ \_ del dispositivo (DIB). Por lo tanto, las aplicaciones pueden usar los mismos datos con Windows llamadas de función y llamadas de función de píxel openGL.<br/>                                                                                                                                                                                                                                     |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt>**GL \_ BGRA \_ EXT**</dt> </dl>                      | Cada píxel es un grupo de cuatro componentes en este orden: azul, verde, rojo, alfa. GL BGRA EXT proporciona un formato que coincide con el diseño de memoria Windows mapas de bits independientes \_ \_ del dispositivo (DIB). Por lo tanto, las aplicaciones pueden usar los mismos datos con Windows llamadas de función y llamadas de función de píxel openGL.<br/>                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**GL \_ LUMINANCE**</dt> </dl>                    | Cada elemento es un único valor de luminosidad. Se convierte en punto flotante y, a continuación, se ensambla en un elemento RGBA replicando el valor de luminosidad tres veces para rojo, verde y azul, y adjuntando 1,0 para alfa. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea **glPixelTransfer).**<br/>                                                                                                                                         |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**GL \_ LUMINANCE \_ ALPHA**</dt> </dl> | Cada elemento es un par luminance/alpha. Se convierte en punto flotante y, a continuación, se ensambla en un elemento RGBA mediante la replicación del valor de luminosidad tres veces para rojo, verde y azul. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea [**glPixelTransfer).**](glpixeltransfer.md)<br/>                                                                                                                                                 |



 

</dd> <dt>

*type* 
</dt> <dd>

Tipo de datos de los datos de píxel. Se aceptan los siguientes valores simbólicos: GL \_ \_ UNSIGNED BYTE, GL \_ BYTE, GL \_ BITMAP, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT \_ y GL FLOAT.

</dd> <dt>

*píxeles* 
</dt> <dd>

Puntero a los datos de imagen en memoria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *el* destino no era UNA \_ TEXTURA \_ 2D de GL.<br/>                                                                                                                                                                                |
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *format* no era una constante *de formato* aceptado. Solo se aceptan constantes de formato que no sean GL \_ STENCIL \_ INDEX y GL DEPTH \_ \_ COMPONENT. Consulte la descripción del parámetro *de formato* para obtener una lista de valores posibles.<br/> |
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *type* no era una *constante de* tipo.<br/>                                                                                                                                                                                   |
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *El tipo* era GL \_ BITMAP y el *formato* no era GL \_ COLOR \_ INDEX.<br/>                                                                                                                                                        |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *level* era menor que cero o mayor que log2 *max,* donde *max* era el valor devuelto de GL \_ MAX TEXTURE \_ \_ SIZE.<br/>                                                                                                |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *internalformat* no era 1, 2, 3 o 4.<br/>                                                                                                                                                                         |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *width* o height era menor que cero o mayor que 2 + GL MAX TEXTURE SIZE, o no se pudo representar como \_ \_ \_ 2 *n* + 2 (borde) para algún valor entero de n .<br/>                                                  |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *border* no era 0 o 1.<br/>                                                                                                                                                                                            |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/>                                                                                          |



## <a name="remarks"></a>Observaciones

La **función glTexImage2D** especifica una imagen de textura bidimensional. Texturing asigna una parte de una imagen de *textura especificada* a cada primitiva gráfica para la que está habilitada la texturing. El texturing bidimensional está habilitado y deshabilitado mediante [**glEnable**](glenable.md) y **glDisable** con el argumento GL \_ TEXTURE \_ 2D.

Las imágenes de textura se definen **con glTexImage2D.** Los argumentos describen los parámetros de la imagen de textura, como el alto, el ancho, el ancho del borde, el número de nivel de detalle (vea [**glTexParameter)**](gltexparameter-functions.md)y el número de componentes de color proporcionados. Los tres últimos argumentos describen la forma en que la imagen se representa en memoria. Estos argumentos son idénticos a los formatos de píxel usados para [**glDrawPixels.**](gldrawpixels.md)

Los datos  se leen desde píxeles como una secuencia de bytes con signo o sin signo, shorts o longs, o valores de punto flotante de precisión sencilla, según el *tipo*. Estos valores se agrupan en conjuntos de uno, dos, tres o cuatro valores, según el *formato*, para formar elementos. Si *type* es GL BITMAP, los datos se consideran una cadena de bytes sin signo (y el formato \_ debe ser GL COLOR  \_ \_ INDEX). Cada byte de datos se trata como ocho elementos de 1 bit, con ordenación de bits determinada por GL \_ UNPACK \_ LSB \_ FIRST (vea [**glPixelStore**](glpixelstore-functions.md)). Consulte [**glDrawPixels para**](gldrawpixels.md) obtener una descripción de los valores aceptables para el *parámetro de* tipo.

Una imagen de textura puede tener hasta cuatro componentes por elemento de textura, dependiendo de *los componentes*. Una imagen de textura de un componente solo usa el componente rojo del color RGBA extraído de *píxeles.* Una imagen de dos componentes usa los valores R y A. Una imagen de tres componentes usa los valores R, G y B. Una imagen de cuatro componentes usa todos los componentes RGBA.

El texturing no tiene ningún efecto en el modo de índice de color.

La imagen de textura se puede representar con los mismos formatos de datos que los píxeles de un **comando glDrawPixels,** salvo que gl STENCIL INDEX y GL DEPTH COMPONENT no se pueden \_ \_ \_ \_ usar. Los [**modos glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente de la manera en que afectan **a glDrawPixels.**

Una imagen de textura con un alto o ancho cero indica la textura nula. Si se especifica la textura null para el nivel de detalle 0, es como si se deshabilitara el texturing.

Las siguientes funciones recuperan información relacionada con **glTexImage2D**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ TEXTURE \_ 2D

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





