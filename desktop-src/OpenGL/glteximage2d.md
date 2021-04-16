---
title: función glTexImage2D (GL. h)
description: La función glTexImage2D especifica una imagen de textura bidimensional.
ms.assetid: e8b9c692-5239-47de-86eb-80c247c60e1d
keywords:
- glTexImage2D (función) OpenGL
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666089"
---
# <a name="glteximage2d-function"></a>glTexImage2D función)

La función **glTexImage2D** especifica una imagen de textura bidimensional.

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

Textura de destino. Debe ser la \_ textura de GL \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

El número de nivel de detalle. El nivel 0 es el nivel de la imagen base. *El nivel* *n* es la imagen de reducción del MIP.

</dd> <dt>

*internalformat* 
</dt> <dd>

El número de componentes de color de la textura. Debe ser 1, 2, 3 o 4, o una de las siguientes constantes simbólicas: GL \_ Alpha, GL \_ ALPHA4, GL \_ ALPHA8, GL \_ ALPHA12, GL \_ ALPHA16, GL \_ luminancia, GL \_ LUMINANCE4, GL \_ LUMINANCE8, GL \_ LUMINANCE12, GL \_ LUMINANCE16, GL \_ luminancia \_ Alpha, GL LUMINANCE4 ALPHA4, GL LUMINANCE6 ALPHA2, GL \_ \_ \_ \_ \_ LUMINANCE8 \_ ALPHA8, GL LUMINANCE12 \_ \_ ALPHA4, GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 \_ ALPHA16, GL \_ Intensity, GL \_ INTENSITY4, GL \_ INTENSITY8, GL \_ INTENSITY12, GL \_ INTENSITY16, GL \_ R3 \_ G3 \_ B2, GL \_ RGB, GL \_ RGB4, GL \_ RGB5, GL \_ RGB8, GL \_ RGB10, GL \_ RGB12, GL RGB16, cont. \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ RGBA2, GL RGBA4, GL RGB5, GL RGBA8, GL RGB10, GL RGBA12, GL RGBA16 o GL.

</dd> <dt>

*width* 
</dt> <dd>

Ancho de la imagen de textura. Debe ser 2 *n* + 2 (*borde*) para algún entero *n*.

</dd> <dt>

*height* 
</dt> <dd>

Alto de la imagen de textura. Debe ser 2 *<sup>m</sup>* + 2 (*borde*) para algún entero *m*.

</dd> <dt>

*PDA* 
</dt> <dd>

Ancho del borde. Debe ser 0 o 1.

</dd> <dt>

*format* 
</dt> <dd>

Formato de los datos de píxeles. Puede suponer uno de los nueve valores simbólicos.



| Value                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**\_Índice de color de GL \_**</dt> </dl>             | Cada elemento es un valor único, un índice de color. Se convierte en un punto fijo (con un número sin especificar de 0 bits a la derecha del punto binario), desplazado a la izquierda o a la derecha en función del valor y el signo del turno del índice de contabilidad \_ \_ y se agrega al desplazamiento del índice de contabilidad \_ \_ (vea [**glPixelTransfer**](glpixeltransfer.md)). El índice resultante se convierte en un conjunto de componentes de color mediante el uso de la asignación de píxeles de GL \_ \_ \_ i \_ a \_ R, la asignación de píxeles de GL \_ \_ \_ i \_ a \_ G, la asignación de píxeles de GL \_ \_ \_ i \_ a \_ B y \_ la asignación de píxeles de GL \_ \_ \_ a \_ una tabla, y se ha fijado en el intervalo de \[ 0 a 1 \] .<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**\_rojo GL**</dt> </dl>                                      | Cada elemento es un componente rojo único. Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 0,0 para verde y azul, y 1,0 para alfa. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).<br/>                                                                                                                                                                                               |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**\_verde GL**</dt> </dl>                                | Cada elemento es un único componente verde. Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo y azul, y 1,0 para alfa. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                        |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**\_azul GL**</dt> </dl>                                   | Cada elemento es un único componente azul. Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo y verde, y 1,0 para alfa. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).<br/>                                                                                                                                                                                               |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**libro \_ de contabilidad**</dt> </dl>                                | Cada elemento es un componente rojo único. Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 0,0 para rojo, verde y azul. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                     |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**RGB de GL \_**</dt> </dl>                                      | Cada elemento es un triple RGB. Se convierte en punto flotante y se monta en un elemento RGBA adjuntando 1,0 para alpha. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).<br/>                                                                                                                                                                                                                                    |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**el \_ RGBA de GL**</dt> </dl>                                   | Cada elemento es un elemento RGBA completo. Se convierte en punto flotante. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                                                                                                 |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt>**GL \_ BGR \_ ext**</dt> </dl>                         | Cada píxel es un grupo de tres componentes en este orden: azul, verde, rojo.<br/> GL \_ BGR \_ ext proporciona un formato que coincide con el diseño de memoria de los mapas de bits independientes del dispositivo (DIB) de Windows. Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.<br/>                                                                                                                                                                                                                                     |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt>**\_ext BGRA \_**</dt> </dl>                      | Cada píxel es un grupo de cuatro componentes en este orden: azul, verde, rojo y alfa. GL \_ BGRA \_ ext proporciona un formato que coincide con el diseño de memoria de mapas de bits independientes del dispositivo (DIB) de Windows. Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.<br/>                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**luminancia del libro de contabilidad \_**</dt> </dl>                    | Cada elemento es un valor de luminancia único. Se convierte en punto flotante y, a continuación, se monta en un elemento RGBA replicando el valor de luminancia tres veces para rojo, verde y azul, y adjuntando 1,0 para alpha. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea **glPixelTransfer**).<br/>                                                                                                                                         |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**alfa de luminancia de GL \_ \_**</dt> </dl> | Cada elemento es un par de luminancia/alfa. Se convierte en punto flotante y, a continuación, se monta en un elemento RGBA mediante la replicación del valor de luminancia tres veces para rojo, verde y azul. Después, cada componente se multiplica por el factor de escala con signo de la escala de contabilidad general \_ \_ , que se agrega a la diferencia de contabilidad c de sesgo con signo \_ \_ y se fija en el intervalo de \[ 0 a 1 \] (vea [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                 |



 

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



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *destino* no era \_ 2D Texture \_ .<br/>                                                                                                                                                                                |
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *formato* no era una constante de *formato* aceptada. Solo se aceptan constantes de formato que no sean el \_ componente de índice de estarcido \_ de GL y de profundidad de contabilidad \_ \_ . Vea la descripción del parámetro *Format* para obtener una lista de valores posibles.<br/> |
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *tipo* no era una constante de *tipo* .<br/>                                                                                                                                                                                   |
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *tipo* era un \_ mapa de bits de contabilidad y el *formato* no era un índice de color de GL \_ \_ .<br/>                                                                                                                                                        |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *nivel* era menor que cero o mayor que LOG2 *Max*, donde *Max* era el valor devuelto del \_ tamaño de textura Max GL \_ \_ .<br/>                                                                                                |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *internalformat* no era 1, 2, 3 o 4.<br/>                                                                                                                                                                         |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *ancho* o alto era menor que cero o mayor que 2 + \_ tamaño máximo de textura de GL \_ \_ , o no se pudo representar como 2 *n* + 2 (borde) para algún valor entero de *n*.<br/>                                                  |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *borde* no era 0 ni 1.<br/>                                                                                                                                                                                            |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/>                                                                                          |



## <a name="remarks"></a>Observaciones

La función **glTexImage2D** especifica una imagen de textura bidimensional. La texturización asigna una parte de una *imagen de textura* especificada en cada primitiva gráfica para la que está habilitada la texturización. La texturización bidimensional está habilitada y deshabilitada mediante [**glEnable**](glenable.md) y **glDisable** con la textura de GL de argumento \_ \_ 2D.

Las imágenes de textura se definen con **glTexImage2D**. Los argumentos describen los parámetros de la imagen de textura, como el alto, el ancho, el ancho del borde, el número de nivel de detalle (vea [**glTexParameter**](gltexparameter-functions.md)) y el número de componentes de color proporcionados. Los tres últimos argumentos describen el modo en que se representa la imagen en la memoria. Estos argumentos son idénticos a los formatos de píxel usados para [**glDrawPixels**](gldrawpixels.md).

Los datos se leen desde *píxeles* como una secuencia de bytes con signo o sin signo, breves o largos o valores de punto flotante de precisión sencilla, dependiendo del *tipo*. Estos valores se agrupan en conjuntos de uno, dos, tres o cuatro valores, según el *formato*, para formar elementos. Si el *tipo* es \_ un mapa de bits de contabilidad, los datos se consideran una cadena de bytes sin signo (y el *formato* debe ser índice de color de GL \_ \_ ). Cada byte de datos se trata como elementos de 8 1 bits, con una ordenación de bits determinada por GL \_ unpack \_ LSB \_ primero (consulte [**glPixelStore**](glpixelstore-functions.md)). Consulte [**glDrawPixels**](gldrawpixels.md) para obtener una descripción de los valores aceptables para el parámetro de *tipo* .

Una imagen de textura puede tener hasta cuatro componentes por elemento de textura, dependiendo de *los componentes*. Una imagen de textura de un componente usa solo el componente rojo del color RGBA extraído de los *píxeles*. Una imagen de dos componentes utiliza los valores R y A. Una imagen de tres componentes utiliza los valores R, G y B. Una imagen de cuatro componentes usa todos los componentes RGBA.

La texturización no tiene ningún efecto en el modo de índice de color.

La imagen de textura se puede representar con los mismos formatos de datos que los píxeles de un comando **glDrawPixels** , excepto en que \_ no se puede usar el índice de estarcido de GL \_ y el componente de profundidad de libro de contabilidad \_ \_ . Los modos [**glPixelStore**](glpixelstore-functions.md) y [**glPixelTransfer**](glpixeltransfer.md) afectan a las imágenes de textura exactamente como afectan a **glDrawPixels**.

Una imagen de textura con alto o ancho cero indica la textura nula. Si se especifica la textura null para el nivel de detalle 0, es como si se hubiera deshabilitado la texturización.

Las siguientes funciones recuperan información relacionada con **glTexImage2D**:

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

 

 





