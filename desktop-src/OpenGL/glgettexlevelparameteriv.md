---
title: función glGetTexLevelParameteriv (GL. h)
description: Las funciones glGetTexLevelParameterfv y glGetTexLevelParameteriv devuelven los valores de los parámetros de textura para un nivel de detalle específico. | función glGetTexLevelParameteriv (GL. h)
ms.assetid: 536d7bc9-1599-47ff-8559-374f96f1d5f3
keywords:
- glGetTexLevelParameteriv (función) OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameteriv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc0fa167eae842784e967538ff1539e0b43a6a2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003544"
---
# <a name="glgettexlevelparameteriv-function"></a>glGetTexLevelParameteriv función)

Las funciones [**glGetTexLevelParameterfv**](glgettexlevelparameterfv.md) y **glGetTexLevelParameteriv** devuelven los valores de los parámetros de textura para un nivel de detalle específico.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetTexLevelParameteriv(
   GLenum target,
   GLint  level,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

El nombre simbólico de la textura de destino: libro \_ \_ de contabilidad 1D, textura de contabilidad \_ 2D, textura de \_ \_ proxy de contabilidad \_ \_ 1D o textura de proxy de GL \_ \_ \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

El número de nivel de detalle de la imagen deseada. El nivel 0 es el nivel de la imagen base. *El nivel* *n* es la imagen de reducción del MIP.

</dd> <dt>

*PName* 
</dt> <dd>

Nombre simbólico de un parámetro de textura. Se aceptan los siguientes nombres de parámetro.



| Value                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <dt>**\_ancho de textura de GL \_**</dt> </dl>                                | El parámetro *params* devuelve un valor único que contiene el ancho de la imagen de textura. Este valor incluye el borde de la imagen de textura.<br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <dt>**\_alto de textura de GL \_**</dt> </dl>                             | El parámetro *params* devuelve un valor único que contiene el alto de la imagen de textura. Este valor incluye el borde de la imagen de textura.<br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <dt>**\_ \_ formato interno de textura GL \_**</dt> </dl> | El parámetro *params* devuelve un valor único que describe el formato textura de la textura.<br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <dt>**\_borde de textura GL \_**</dt> </dl>                             | El parámetro *params* devuelve un valor único: el ancho, en píxeles, del borde de la imagen de textura.<br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <dt>**\_ \_ tamaño rojo de textura de GL \_**</dt> </dl>                      | La resolución de almacenamiento interna del componente rojo de un textura. La resolución elegida por OpenGL será una coincidencia cercana para la resolución solicitada por el usuario con el argumento de componente de [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).<br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <dt>**\_ \_ tamaño verde de textura GL \_**</dt> </dl>                | La resolución de almacenamiento interna del componente verde de un textura. La resolución elegida por OpenGL será una coincidencia cercana para la resolución solicitada por el usuario con el argumento de componente de [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).<br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <dt>**\_ \_ tamaño azul de textura de GL \_**</dt> </dl>                   | La resolución de almacenamiento interna del componente azul de un textura. La resolución elegida por OpenGL será una coincidencia cercana para la resolución solicitada por el usuario con el argumento de componente de [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).<br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <dt>**\_ \_ tamaño alfa de textura de GL \_**</dt> </dl>                | La resolución de almacenamiento interna del componente alfa de un textura. La resolución elegida por OpenGL será una coincidencia cercana para la resolución solicitada por el usuario con el argumento de componente de [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).<br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <dt>**\_tamaño de \_ luminancia de textura de GL \_**</dt> </dl>    | La resolución de almacenamiento interna del componente de luminancia de un textura. La resolución elegida por OpenGL será una coincidencia cercana para la resolución solicitada por el usuario con el argumento de componente de [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).<br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <dt>**\_tamaño de \_ intensidad de textura de GL \_**</dt> </dl>    | La resolución de almacenamiento interna del componente de intensidad de un textura. La resolución elegida por OpenGL será una coincidencia cercana para la resolución solicitada por el usuario con el argumento de componente de [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).<br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <dt>**\_componentes de textura de GL \_**</dt> </dl>                 | El parámetro *params* devuelve un valor único: el número de componentes de la imagen de textura.<br/>                                                                                                                                                                                          |



 

</dd> <dt>

*params* 
</dt> <dd>

Devuelve los datos solicitados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *destino* o *PName* no era un valor aceptado.<br/>                                                                             |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | el *nivel* es menor que cero o mayor que el *registro* 2 *(Max)*, donde *Max* es el valor devuelto del \_ tamaño de textura Max GL \_ \_ .<br/>      |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glGetTexLevelParameter** devuelve los valores de *parámetro Texture de los parámetros para* un valor de nivel de detalle específico, especificado como *nivel*. El parámetro de *destino* define la textura de destino, ya sea GL \_ Texture \_ 1D, GL \_ Texture \_ 2D, GL \_ proxy \_ Texture \_ 1D o la \_ \_ textura de proxy GL \_ 2D para especificar una texturización unidimensional o bidimensional. El parámetro *PName* especifica el parámetro de textura cuyo valor o valores se devolverán.

Si se genera un error, no se realiza ningún cambio en el contenido de los *parámetros*.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





