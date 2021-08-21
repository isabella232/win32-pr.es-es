---
title: Función glTexSubImage2D (Gl.h)
description: La función glTexSubImage2D especifica una parte de una imagen de textura unidimensional existente. No se puede definir una nueva textura con glTexSubImage2D.
ms.assetid: 2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7
keywords:
- Función GlTexSubImage2D OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c568afbe63ab01bd2866f180f968ea80101fec2ff22062707f4929d662ea47ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519705"
---
# <a name="gltexsubimage2d-function"></a>Función glTexSubImage2D

La **función glTexSubImage2D** especifica una parte de una imagen de textura unidimensional existente. No se puede definir una nueva textura **con glTexSubImage2D.**

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glTexSubImage2D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLint   yoffset,
         GLsizei width,
         GLsizei height,
         GLenum  format,
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

Número de nivel de detalle. El nivel 0 es la imagen base. El *nivel n* es la imagen *de* reducción de mipmap n.

</dd> <dt>

*xoffset* 
</dt> <dd>

Desplazamiento de texel en la *dirección x* dentro de la matriz de textura.

</dd> <dt>

*yoffset* 
</dt> <dd>

Desplazamiento de textura en la dirección *y* dentro de la matriz de textura.

</dd> <dt>

*width* 
</dt> <dd>

Ancho de la sub image de textura.

</dd> <dt>

*height* 
</dt> <dd>

Alto de la sub image de textura.

</dd> <dt>

*format* 
</dt> <dd>

Formato de los datos de píxel. Puede suponer uno de los siguientes valores simbólicos.



| Valor                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**GL \_ COLOR \_ INDEX**</dt> </dl>             | Cada elemento es un valor único, un índice de color. Se convierte al formato de punto fijo (con un número no especificado de 0 bits a la derecha del punto binario), se desplaza a la izquierda o a la derecha, según el valor y el signo de GL INDEX SHIFT y se agrega a \_ \_ GL INDEX OFFSET \_ \_ (vea [**glPixelTransfer).**](glpixeltransfer.md) El índice resultante se convierte en un conjunto de componentes de color mediante las tablas GL PIXEL MAP I TO R, GL PIXEL MAP I TO G, GL PIXEL MAP I TO B y GL PIXEL MAP I TO A, y fija en el intervalo \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \[ 0,1. \]<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**GL \_ RED**</dt> </dl>                                      | Cada elemento es un único componente rojo. Se convierte al formato de punto flotante y se ensambla en un elemento RGBA adjuntando 0,0 para verde y azul, y 1,0 para alfa. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea **glPixelTransfer).**<br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**GL \_ GREEN**</dt> </dl>                                | Cada elemento es un único componente verde. Se convierte al formato de punto flotante y se ensambla en un elemento RGBA adjuntando 0,0 para rojo y azul, y 1,0 para alfa. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea [**glPixelTransfer).**](glpixeltransfer.md)<br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**GL \_ BLUE**</dt> </dl>                                   | Cada elemento es un único componente azul. Se convierte al formato de punto flotante y se ensambla en un elemento RGBA adjuntando 0,0 para rojo y verde, y 1,0 para alfa. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea **glPixelTransfer).**<br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**GL \_ ALPHA**</dt> </dl>                                | Cada elemento es un único componente alfa. Se convierte al formato de punto flotante y se ensambla en un elemento RGBA adjuntando 0,0 para rojo, verde y azul. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea [**glPixelTransfer).**](glpixeltransfer.md)<br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**GL \_ RGB**</dt> </dl>                                      | Cada elemento es un triple RGB. Se convierte al formato de punto flotante y se ensambla en un elemento RGBA adjuntando 1.0 para alfa. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea **glPixelTransfer).**<br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**GL \_ RGBA**</dt> </dl>                                   | Cada elemento es un elemento RGBA completo. Se convierte en punto flotante. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea **glPixelTransfer).**<br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**GL \_ LUMINANCE**</dt> </dl>                    | Cada elemento es un único valor de luminosidad. Se convierte al formato de punto flotante y, a continuación, se ensambla en un elemento RGBA replicando el valor de la luminosidad tres veces para rojo, verde y azul, y adjuntando 1,0 para alfa. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea [**glPixelTransfer).**](glpixeltransfer.md)<br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**GL \_ LUMINANCE \_ ALPHA**</dt> </dl> | Cada elemento es un par luminance/alpha. Se convierte al formato de punto flotante y, a continuación, se ensambla en un elemento RGBA mediante la replicación del valor de luminosidad tres veces para rojo, verde y azul. A continuación, cada componente se multiplica por el factor de escala firmado GL c SCALE, se agrega al sesgo firmado GL c BIAS y se fija al intervalo \_ \_ \_ \_ \[ 0,1 \] (vea **glPixelTransfer).**<br/>                                                                                                                                                                         |



 

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



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *el* destino no era GL \_ TEXTURE \_ 2D.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *format* no era una constante aceptada.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *Type* no era una constante aceptada.<br/>                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *El tipo* era GL \_ BITMAP y el *formato* no era GL \_ COLOR \_ INDEX.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *level* era menor que cero o mayor que log2 *max,* donde *max* era el valor devuelto de GL \_ MAX TEXTURE \_ \_ SIZE.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *xoffset* era menor que -*b*; o *xoffset* width was  +   greater than *w*  -  *b*; or *yoffset* was less than -*b*; or *yoffset*  +  *height* was greater than *h*  -  *b*, where *w* is the GL \_ TEXTURE \_ WIDTH, *h* is the GL \_ TEXTURE HEIGHT, and b is the width of the GL TEXTURE BORDER of the texture image being \_  \_ \_ modified. <br/> Tenga en cuenta *que w* y *h* incluyen dos veces el ancho del borde.<br/> |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *width* era menor que *b*, donde *b* es el ancho del borde de la matriz de textura.<br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *border* no era cero o 1.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | La matriz de texturas no se definió mediante una operación **glTexImage2D** anterior.<br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/>                                                                                                                                                                                                                                                                        |



## <a name="remarks"></a>Comentarios

El texturizado bidimensional para una primitiva se habilita mediante [**glEnable**](glenable.md) y **glDisable** con el argumento GL \_ TEXTURE \_ 2D. Durante el texto, parte de una imagen de textura especificada se asigna a cada primitiva habilitada. Use la función **glTexSubImage2D** para especificar una subimagen contigua de una imagen de textura bidimensional existente para texturizar.

Los elementos de textura  a los que hacen referencia los píxeles reemplazan una región de la matriz de texturas existente por *índices x* *de xoffset* y *xoffset* +*(ancho* 1) inclusivos e índices y *yoffset* e *yoffset* +*(alto* 1) inclusivos.  Esta región no puede incluir ningún elemento de textura fuera del intervalo de la matriz de texturas especificada originalmente.

Especificar una sub image con un *ancho de* cero no tiene ningún efecto y no genera un error.

El texto no tiene ningún efecto en el modo de índice de color.

En general, las imágenes de textura se pueden representar con los mismos formatos de datos que los píxeles de un [**comando glDrawPixels,**](gldrawpixels.md) salvo que gl STENCIL INDEX y GL DEPTH COMPONENT no se pueden \_ \_ \_ \_ usar. Los [**modos glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente de la manera en que afectan **a glDrawPixels.**

Las siguientes funciones recuperan información relacionada **con glTexSubImage2D**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ TEXTURE \_ 2D

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glCopyTexImage1D**](glcopyteximage1d.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage1D**](glcopytexsubimage1d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





