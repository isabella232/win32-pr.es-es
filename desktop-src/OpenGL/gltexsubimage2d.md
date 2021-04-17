---
title: función glTexSubImage2D (GL. h)
description: La función glTexSubImage2D especifica una parte de una imagen de textura de una dimensión existente. No se puede definir una textura nueva con glTexSubImage2D.
ms.assetid: 2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7
keywords:
- glTexSubImage2D (función) OpenGL
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
ms.openlocfilehash: a7a0a59ae9e6724386cb2f7891a14e4bf9d4c1a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665916"
---
# <a name="gltexsubimage2d-function"></a>glTexSubImage2D función)

La función **glTexSubImage2D** especifica una parte de una imagen de textura de una dimensión existente. No se puede definir una textura nueva con **glTexSubImage2D**.

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

Textura de destino. Debe ser la \_ textura de GL \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

El número de nivel de detalle. El nivel 0 es la imagen base. *El nivel* *n* es la imagen de reducción del MIP.

</dd> <dt>

*xoffset* 
</dt> <dd>

Desplazamiento textura en la dirección *x* dentro de la matriz de textura.

</dd> <dt>

*yoffset* 
</dt> <dd>

Desplazamiento textura en la dirección *y* dentro de la matriz de textura.

</dd> <dt>

*width* 
</dt> <dd>

Ancho de la subimagen de textura.

</dd> <dt>

*height* 
</dt> <dd>

Alto de la subimagen de textura.

</dd> <dt>

*format* 
</dt> <dd>

Formato de los datos de píxeles. Puede suponer uno de los siguientes valores simbólicos.



| Value                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**\_Índice de color de GL \_**</dt> </dl>             | Cada elemento es un valor único, un índice de color. Se convierte en un formato de punto fijo (con un número no especificado de 0 bits a la derecha del punto binario), desplazado a la izquierda o a la derecha, según el valor y el signo del turno del índice de contabilidad \_ \_ y se agrega al desplazamiento del índice de GL \_ \_ (vea [**glPixelTransfer**](glpixeltransfer.md)). El índice resultante se convierte en un conjunto de componentes de color mediante el uso de la asignación de píxeles de GL \_ \_ \_ i \_ a \_ R, la asignación de píxeles de GL \_ \_ \_ i \_ a \_ G, la asignación de píxeles de GL \_ \_ \_ i \_ a \_ B y \_ la asignación de píxeles de GL \_ \_ \_ a \_ una tabla, y se ha fijado en el intervalo de \[ 0 a 1 \] .<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**\_rojo GL**</dt> </dl>                                      | Cada elemento es un componente rojo único. Se convierte al formato de punto flotante y se monta en un elemento RGBA adjuntando 0,0 para verde y azul, y 1,0 para alpha. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**\_verde GL**</dt> </dl>                                | Cada elemento es un único componente verde. Se convierte al formato de punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo y azul, y 1,0 para alfa. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**\_azul GL**</dt> </dl>                                   | Cada elemento es un único componente azul. Se convierte al formato de punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo y verde, y 1,0 para alpha. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**libro \_ de contabilidad**</dt> </dl>                                | Cada elemento es un único componente alfa. Se convierte al formato de punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo, verde y azul. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**RGB de GL \_**</dt> </dl>                                      | Cada elemento es un triple RGB. Se convierte al formato de punto flotante y se monta en un elemento RGBA adjuntando 1,0 para alpha. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).<br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**el \_ RGBA de GL**</dt> </dl>                                   | Cada elemento es un elemento RGBA completo. Se convierte en punto flotante. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).<br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**luminancia del libro de contabilidad \_**</dt> </dl>                    | Cada elemento es un valor de luminancia único. Se convierte al formato de punto flotante y, a continuación, se monta en un elemento RGBA mediante la replicación del valor de luminancia tres veces para rojo, verde y azul, y la Asociación de 1,0 para alpha. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**alfa de luminancia de GL \_ \_**</dt> </dl> | Cada elemento es un par de luminancia/alfa. Se convierte al formato de punto flotante y, a continuación, se monta en un elemento RGBA mediante la replicación del valor de luminancia tres veces para rojo, verde y azul. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).<br/>                                                                                                                                                                         |



 

</dd> <dt>

*type* 
</dt> <dd>

El tipo de datos de los datos de píxeles. Se aceptan los siguientes valores simbólicos: \_ byte sin signo \_ de libro de contabilidad, \_ bytes de contabilidad, \_ mapa de bits de GL, GL \_ sin signo \_ corto, GL \_ corto, libro de contabilidad \_ sin signo de GL \_ , GL \_ int y contabilidad \_ flotante.

</dd> <dt>

*píxeles* 
</dt> <dd>

Puntero a los datos de la imagen en memoria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *destino* no era \_ \_ 2D Texture 2D.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *formato* no era una constante aceptada.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *tipo* no era una constante aceptada.<br/>                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *tipo* era un \_ mapa de bits de contabilidad y el *formato* no era un índice de color de GL \_ \_ .<br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *nivel* era menor que cero o mayor que LOG2 *Max*, donde *Max* era el valor devuelto del \_ tamaño de textura Max GL \_ \_ .<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *xoffset* era menor que-*b*; o el ancho de *xoffset*  +   era mayor que *w*  -  *b*; o *YOFFSET* era menor que-*b*; o el alto de *YOFFSET*  +   era mayor que *h*  -  *b*, donde *w* es el ancho de la textura GL \_ \_ , *h* es el \_ alto de la textura GL \_ y *b* es el ancho del borde de la textura de contabilidad \_ \_ de la imagen de textura que se está modificando. <br/> Tenga en cuenta que *w* y *h* incluyen dos veces el ancho del borde.<br/> |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *ancho* era menor que *b*, donde *b* es el ancho del borde de la matriz de textura.<br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *Border* no era cero o 1.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Una operación **glTexImage2D** anterior no definió la matriz de textura.<br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/>                                                                                                                                                                                                                                                                        |



## <a name="remarks"></a>Observaciones

La texturización bidimensional para un primitivo se habilita mediante [**glEnable**](glenable.md) y **glDisable** con el argumento GL \_ Texture \_ 2D. Durante la texturización, parte de una imagen de textura especificada se asigna a cada primitiva habilitada. La función **glTexSubImage2D** se usa para especificar una subimagen contigua de una imagen de textura bidimensional existente para la texturización.

Los textura a los que se hace referencia en *píxeles* reemplazan una región de la matriz de textura existente por índices *x* de *xoffset* y *xoffset* + (*ancho* 1) índices inclusivos *e y de* *YOFFSET* y *YOFFSET* + (*alto* 1) inclusive. Esta región no puede incluir ningún textura fuera del intervalo de la matriz de textura originalmente especificada.

Especificar una subimagen con un *ancho* de cero no tiene ningún efecto y no genera ningún error.

La texturización no tiene ningún efecto en el modo de índice de color.

En general, las imágenes de textura se pueden representar con los mismos formatos de datos que los píxeles de un comando [**glDrawPixels**](gldrawpixels.md) , excepto en que \_ no se puede usar el índice de estarcido de GL \_ y el componente de profundidad de contabilidad \_ \_ . Los modos [**glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente como afectan a **glDrawPixels**.

Las siguientes funciones recuperan información relacionada con **glTexSubImage2D**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled**](glisenabled.md) con el argumento GL \_ Texture \_ 2D

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

 

 





