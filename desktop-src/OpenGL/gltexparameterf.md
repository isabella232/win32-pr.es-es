---
title: Función glTexParameterf (Gl.h)
description: Establece los parámetros de textura. | Función glTexParameterf (Gl.h)
ms.assetid: 20b9f2d5-66e1-41cd-9571-8caa38ef033d
keywords:
- Función glTexParameterf OpenGL
topic_type:
- apiref
api_name:
- glTexParameterf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f749513757ee32f6fe468dadbe968b8657a06f3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265711"
---
# <a name="gltexparameterf-function"></a>Función glTexParameterf

Establece los parámetros de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glTexParameterf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

La textura de destino, que debe ser GL \_ TEXTURE \_ 1D o GL \_ TEXTURE \_ 2D.

</dd> <dt>

*pname* 
</dt> <dd>

Nombre simbólico de un parámetro de textura con un solo valor. Los símbolos siguientes se aceptan en *pname*.



| Value                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**FILTRO \_ DE TEXTURA MÍNIMA DE \_ \_ GL**</dt> </dl> | La función de compresión de textura se usa siempre que el píxel con textura se asigna a un área mayor que un elemento de textura. Hay seis funciones de compresión definidas. Dos de ellos usan los cuatro elementos de textura más cercanos o más cercanos para calcular el valor de textura. Los otros cuatro usan mapas MIP.<br/> Un mapa mip es un conjunto ordenado de matrices que representan la misma imagen con resoluciones progresivamente inferiores. Si la textura tiene dimensiones de 2nx2<sup>m,</sup> hay max(n, m) + 1 mipmaps. El primer mapa mip es la textura original, con dimensiones de 2nx2<sup>m.</sup> Cada mapa mipmap subsiguiente tiene dimensiones de 2<sup>k</sup>1x2<sup>l</sup>1, donde 2<sup>k</sup>x2<sup>l</sup> son las dimensiones del mapa mipmap anterior, hasta k = 0 o l = 0. En ese momento, los mapas MIP posteriores tienen la dimensión 1x2<sup>l</sup>1 o 2<sup>k</sup>1x1 hasta el mapa mip final, que tiene la dimensión 1x1. Los mapas Mip se definen mediante [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md) con el argumento de nivel de detalle que indica el orden de los mapas mip. El nivel 0 es la textura original; level bold max(n, m) es el mapa mipmap 1x1 final.<br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**FILTRO GL \_ TEXTURE \_ MAG \_**</dt> </dl> | La función de ampliación de textura se usa cuando el píxel con textura se asigna a un área menor o igual que un elemento de textura. Establece la función de ampliación de textura en GL \_ NEAREST o GL \_ LINEAR.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ S**</dt> </dl>             | Establece el parámetro wrap para las coordenadas de textura en \_ GL CLAMP o GL \_ REPEAT. GL CLAMP hace que las coordenadas se fijan en el intervalo \_ 0,1 y es útil para evitar el ajuste de artefactos al asignar una sola imagen \[ \] a un objeto. GL REPEAT hace que se ignore la parte entera de la \_ coordenada de la ; OpenGL usa solo la parte fraccionera, lo que crea un patrón repetido. Solo se tiene acceso a los elementos de textura de borde si el ajuste se establece en \_ GL CLAMP. Inicialmente, GL \_ TEXTURE WRAP S se establece en GL \_ \_ \_ REPEAT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ T**</dt> </dl>             | Establece el parámetro wrap para la coordenada de textura t \_ en GL CLAMP o GL \_ REPEAT. Consulte la explicación en GL \_ TEXTURE \_ WRAP \_ S. Inicialmente, GL \_ TEXTURE WRAP T se establece en GL \_ \_ \_ REPEAT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*param* 
</dt> <dd>

Valor de *pname*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ENUMERACIÓN \_ NO VÁLIDA**</dt> </dl>     | *target* o *pname* no era uno de los valores definidos aceptados, o cuando *param* debería haber tenido un valor constante definido (basado en el valor de *pname)* y no lo hizo.<br/> |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/>                                            |



## <a name="remarks"></a>Observaciones

La asignación de textura es una técnica que aplica una imagen a la superficie de un objeto como si la imagen fuera un ajuste reducción decal o cellophane. La imagen se crea en el espacio de textura, con un sistema de coordenadas (*s*, *t*). Una textura es una imagen unidimensional o bidimensional y un conjunto de parámetros que determinan cómo se derivan las muestras de la imagen.

La **función glTexParameter** asigna el valor o los valores de los parámetros al parámetro de textura especificado como pname. El parámetro de destino define la textura de destino, ya sea GL \_ TEXTURE \_ 1D o GL \_ TEXTURE \_ 2D.

A medida que se muestree más elementos de textura en el proceso de minificación, serán evidentes menos artefactos de alias. Aunque las funciones de minificación GL NEAREST y GL LINEAR pueden ser más rápidas que las otras cuatro, solo muestrean uno o cuatro elementos de textura para determinar el valor de textura del píxel que se representa y pueden generar patrones de moire o \_ \_ transiciones desiguales. El valor predeterminado de GL \_ TEXTURE MIN FILTER es GL NEAREST \_ \_ \_ \_ MIPMAP \_ LINEAR.

Supongamos que texturing está habilitado (mediante una llamada a [**glEnable**](glenable.md) con el argumento GL TEXTURE 1D o GL TEXTURE 2D) y GL TEXTURE MIN FILTER se establece en una de las funciones que requiere \_ \_ un mapa \_ \_ \_ \_ \_ mipmap. Si las dimensiones de las imágenes de textura definidas actualmente (con llamadas anteriores a [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D)**](glteximage2d.md)no siguen la secuencia adecuada para los mapas mip, o hay menos imágenes de textura definidas de las necesarias, o si el conjunto de imágenes de textura tiene distintos números de componentes de textura, es como si se deshabilitara la asignación de textura. El filtrado lineal tiene acceso a los cuatro elementos de textura más cercanos solo en texturas 2D. En texturas 1D, el filtrado lineal accede a los dos elementos de textura más cercanos. La función siguiente recupera información relacionada con **glTexParameterf,** **glTexParameteri,** **glTexParameterfv** y **glTexParameteriv.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexImage1D**](glcopyteximage1d.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
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

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





