---
title: función glTexParameteri (GL. h)
description: Establece los parámetros de textura. | función glTexParameteri (GL. h)
ms.assetid: 67705f63-7f86-47c1-81f7-deecc0cd2e16
keywords:
- glTexParameteri (función) OpenGL
topic_type:
- apiref
api_name:
- glTexParameteri
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 207ac902047c5a2b6a5266d08e71f8e47f7ccb97
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362143"
---
# <a name="gltexparameteri-function"></a>glTexParameteri función)

Establece los parámetros de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glTexParameteri(
   GLenum target,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Textura de destino, que debe ser la textura de GL \_ \_ 1D o la textura de GL \_ \_ 2D.

</dd> <dt>

*PName* 
</dt> <dd>

Nombre simbólico de un parámetro de textura de valor único. Los siguientes símbolos se aceptan en *PName*.



| Value                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**\_ \_ filtro mínimo de textura de GL \_**</dt> </dl> | La función Texture minificar se usa siempre que el píxel al que se aplica la textura se asigna a un área mayor que un elemento de textura. Hay seis funciones minificar definidas. Dos de ellos usan la más cercana, o los cuatro elementos de textura más cercanos, para calcular el valor de textura. Los otros cuatro mapas de uso. <br/> Un mipmap es un conjunto ordenado de matrices que representa la misma imagen con una resolución progresivamente inferior. Si la textura tiene dimensiones 2nx2<sup>m</sup> , hay un número máximo de mapas de caracteres (n, m) + 1. El primer mipmap es la textura original, con las dimensiones 2nx2<sup>m</sup>. Cada MIP subsiguiente tiene dimensiones 2<sup>k</sup>1x2<sup>l</sup>1, donde 2<sup>k</sup>x2<sup>l</sup> son las dimensiones del mipmap anterior, hasta que k = 0 o l = 0. En ese momento, los mapas de operaciones posteriores tienen la dimensión 1x2<sup>l</sup>1 o 2<sup>k</sup>1x1 hasta el mipmap final, que tiene una dimensión 1x1. Los mapas MIP se definen mediante [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md) con el argumento de nivel de detalle que indica el orden de los mapas de bits. El nivel 0 es la textura original; el nivel de negrita máximo (n, m) es el mipmap de 1x1 final.<br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**\_filtro de textura de GL \_ \_**</dt> </dl> | La función de aumento de textura se usa cuando el píxel al que se aplica la textura se asigna a un área menor o igual que un elemento de textura. Establece la función de aumento de la textura en GL \_ más próximo o en GL \_ lineal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**\_ajuste de textura de GL \_ \_**</dt> </dl>             | Establece el parámetro Wrap para las coordenadas de textura s en la \_ abrazadera de GL o en la repetición de contabilidad \_ . \_La abrazadera GL hace que las coordenadas s se detengan en el intervalo \[ 0, 1 \] y es útil para evitar los artefactos de ajuste al asignar una sola imagen a un objeto. \_La repetición de GL hace que se omita la parte entera de la coordenada s; OpenGL solo usa la parte fraccionaria, con lo que se crea un patrón de repetición. Solo se tiene acceso a los elementos de textura de borde si el ajuste está establecido en abrazadera de contabilidad \_ . Inicialmente, el \_ ajuste de textura de GL \_ \_ se establece en libro de \_ repetición.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**ajuste de textura de GL \_ \_ \_ T**</dt> </dl>             | Establece el parámetro Wrap para la coordenada de textura t en la \_ abrazadera de GL o en la repetición de contabilidad \_ . Vea la explicación de la sección sobre el ajuste de textura de GL \_ \_ \_ . Inicialmente, el \_ \_ ajuste \_ de textura de GL T se establece en GL \_ REPEAT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

*param* 
</dt> <dd>

El valor de *PName*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Libro de contabilidad \_ \_enumeración no válida**</dt> </dl>     | el *destino* o *PName* no era uno de los valores definidos aceptados o cuando el *parámetro* debe tener un valor constante definido (basado en el valor de *PName*) y no lo hizo.<br/> |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/>                                            |



## <a name="remarks"></a>Observaciones

La asignación de texturas es una técnica que aplica una imagen a la superficie de un objeto como si la imagen fuera una Decal o Cellophane shrink-wrap. La imagen se crea en el espacio de textura, con un sistema de coordenadas (*s*, *t*). Una textura es una imagen de una o dos dimensiones y un conjunto de parámetros que determinan cómo se derivan los ejemplos de la imagen.

La función **glTexParameter** asigna el valor o los valores de los parámetros al parámetro Texture especificado como PName. El parámetro de destino define la textura de destino, ya sea \_ \_ 1D Texture o textura de GL \_ \_ 2D.

A medida que se muestren más elementos de textura en el proceso minificación, se mostrarán menos artefactos de alias. Aunque las \_ funciones de minificación lineal de GL más próximas y de GL \_ pueden ser más rápidas que las otras cuatro, solo muestrean uno o cuatro elementos de textura para determinar el valor de textura del píxel que se representa y pueden generar patrones Moire o transiciones desiguales. El valor predeterminado de \_ filtro de textura mín. de la contabilidad \_ \_ es GL \_ más cercano \_ \_ lineal.

Supongamos que la texturización está habilitada (mediante una llamada a [**glEnable**](glenable.md) con el argumento GL de \_ la textura 1D o la textura de GL \_ \_ \_ 2D) y el \_ \_ \_ filtro mínimo de textura de GL está establecido en una de las funciones que requieren un mipmap. Si las dimensiones de las imágenes de textura definidas actualmente (con llamadas anteriores a [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md)) no siguen la secuencia adecuada para los mapas MIP, o hay menos imágenes de textura definidas que son necesarias, o el conjunto de imágenes de textura tiene un número diferente de componentes de textura, es como si se hubiera deshabilitado la asignación de textura. El filtrado lineal accede a los cuatro elementos de textura más cercanos solo en texturas 2D. En las texturas 1D, el filtrado lineal tiene acceso a los dos elementos de textura más cercanos. La siguiente función recupera información relacionada con **glTexParameterf**, **glTexParameteri**, **glTexParameterfv** y **glTexParameteriv**:

[**glGetTexParameter**](glgettexparameter.md)

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

[glTexEnv](gltexenv-functions.md)
</dt> <dt>

[glTexGen](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





