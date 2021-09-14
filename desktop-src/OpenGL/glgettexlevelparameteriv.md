---
title: Función glGetTexLevelParameteriv (Gl.h)
description: Las funciones glGetTexLevelParameterfv y glGetTexLevelParameteriv devuelven valores de parámetro de textura para un nivel de detalle específico. | Función glGetTexLevelParameteriv (Gl.h)
ms.assetid: 536d7bc9-1599-47ff-8559-374f96f1d5f3
keywords:
- Función GlGetTexLevelParameteriv OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260148"
---
# <a name="glgettexlevelparameteriv-function"></a>Función glGetTexLevelParameteriv

Las [**funciones glGetTexLevelParameterfv**](glgettexlevelparameterfv.md) y **glGetTexLevelParameteriv** devuelven valores de parámetro de textura para un nivel de detalle específico.

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

Nombre simbólico de la textura de destino: GL \_ TEXTURE \_ 1D, GL \_ TEXTURE \_ 2D, GL \_ PROXY TEXTURE 1D o GL PROXY TEXTURE \_ \_ \_ \_ \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Número de nivel de detalle de la imagen deseada. El nivel 0 es el nivel de imagen base. El *nivel n* es la imagen *de* reducción de mipmap n.

</dd> <dt>

*pname* 
</dt> <dd>

Nombre simbólico de un parámetro de textura. Se aceptan los siguientes nombres de parámetro.



| Value                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <dt>**ANCHO DE \_ TEXTURA \_ GL**</dt> </dl>                                | El *parámetro params* devuelve un valor único que contiene el ancho de la imagen de textura. Este valor incluye el borde de la imagen de textura.<br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <dt>**ALTO \_ DE TEXTURA \_ GL**</dt> </dl>                             | El *parámetro params* devuelve un valor único que contiene el alto de la imagen de textura. Este valor incluye el borde de la imagen de textura.<br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <dt>**FORMATO \_ INTERNO DE TEXTURA \_ \_ GL**</dt> </dl> | El *parámetro params* devuelve un valor único que describe el formato de textura.<br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <dt>**BORDE DE \_ TEXTURA \_ GL**</dt> </dl>                             | El *parámetro params* devuelve un solo valor: el ancho en píxeles del borde de la imagen de textura.<br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <dt>**TAMAÑO ROJO \_ DE \_ TEXTURA \_ GL**</dt> </dl>                      | Resolución de almacenamiento interno del componente rojo de un texel. La resolución elegida por OpenGL será una coincidencia estrecha para la resolución solicitada por el usuario con el argumento de componente [**de glTexImage1D**](glteximage1d.md) o [**glTexImage2D.**](glteximage2d.md)<br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <dt>**TAMAÑO \_ VERDE DE TEXTURA \_ \_ GL**</dt> </dl>                | Resolución de almacenamiento interno del componente verde de un texel. La resolución elegida por OpenGL será una coincidencia estrecha para la resolución solicitada por el usuario con el argumento de componente [**de glTexImage1D**](glteximage1d.md) o [**glTexImage2D.**](glteximage2d.md)<br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <dt>**TAMAÑO AZUL \_ \_ DE TEXTURA \_ GL**</dt> </dl>                   | Resolución de almacenamiento interno del componente azul de un texel. La resolución elegida por OpenGL será una coincidencia estrecha para la resolución solicitada por el usuario con el argumento de componente [**de glTexImage1D**](glteximage1d.md) o [**glTexImage2D.**](glteximage2d.md)<br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <dt>**TAMAÑO ALFA \_ DE \_ TEXTURA \_ GL**</dt> </dl>                | Resolución de almacenamiento interno del componente alfa de un texel. La resolución elegida por OpenGL será una coincidencia estrecha para la resolución solicitada por el usuario con el argumento de componente [**de glTexImage1D**](glteximage1d.md) o [**glTexImage2D.**](glteximage2d.md)<br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <dt>**TAMAÑO DE \_ LA LUMINOSIDAD DE TEXTURA \_ \_ GL**</dt> </dl>    | Resolución de almacenamiento interno del componente de luminosidad de un texel. La resolución elegida por OpenGL será una coincidencia estrecha para la resolución solicitada por el usuario con el argumento de componente [**de glTexImage1D**](glteximage1d.md) o [**glTexImage2D.**](glteximage2d.md)<br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <dt>**TAMAÑO DE \_ INTENSIDAD \_ DE TEXTURA \_ GL**</dt> </dl>    | Resolución de almacenamiento interno del componente de intensidad de un texel. La resolución elegida por OpenGL será una coincidencia estrecha para la resolución solicitada por el usuario con el argumento de componente [**de glTexImage1D**](glteximage1d.md) o [**glTexImage2D.**](glteximage2d.md)<br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <dt>**COMPONENTES DE \_ TEXTURA \_ GL**</dt> </dl>                 | El *parámetro params* devuelve un valor único: el número de componentes de la imagen de textura.<br/>                                                                                                                                                                                          |



 

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
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *target* o *pname* no era un valor aceptado.<br/>                                                                             |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *level* es menor que cero o mayor que *el registro* 2 *(max)*, donde *max* es el valor devuelto de GL MAX \_ TEXTURE \_ \_ SIZE.<br/>      |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glGetTexLevelParameter** devuelve en los valores de parámetro de textura *params* para un valor de nivel de detalle específico, especificado como *nivel*. El  parámetro de destino define la textura de destino, ya sea GL \_ TEXTURE \_ 1D, GL \_ TEXTURE \_ 2D, GL PROXY TEXTURE 1D o GL PROXY TEXTURE 2D para especificar el texturizado unidimensional o \_ \_ \_ \_ \_ \_ bidimensional. El *parámetro pname* especifica el parámetro de textura cuyo valor o valores se devolverán.

Si se genera un error, no se realiza ningún cambio en el contenido de *params*.

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

 

 





