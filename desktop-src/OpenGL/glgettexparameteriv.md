---
title: Función glGetTexParameteriv (Gl.h)
description: Las funciones glGetTexParameterfv y glGetTexParameteriv devuelven valores de parámetro de textura. | Función glGetTexParameteriv (Gl.h)
ms.assetid: b89d10f1-5e30-4d25-8953-fbd59781fdac
keywords:
- Función glGetTexParameteriv OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameteriv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1226f4096088d20851b0eab9789acf19cb84ecfac5202ff9e992c8c07ded4bb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493675"
---
# <a name="glgettexparameteriv-function"></a>Función glGetTexParameteriv

Las [**funciones glGetTexParameterfv**](glgettexparameterfv.md) y **glGetTexParameteriv** devuelven valores de parámetro de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetTexParameteriv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Nombre simbólico de la textura de destino. Se \_ aceptan GL TEXTURE \_ 1D y GL \_ TEXTURE \_ 2D.

</dd> <dt>

*pname* 
</dt> <dd>

Nombre simbólico de un parámetro de textura. Se aceptan los valores siguientes.



| Value                                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**FILTRO GL \_ TEXTURE \_ MAG \_**</dt> </dl>       | Devuelve el filtro de ampliación de textura de un solo valor, una constante simbólica.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**FILTRO MIN \_ \_ DE TEXTURA DE \_ GL**</dt> </dl>       | Devuelve el filtro de minificación de textura con un solo valor, una constante simbólica.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ S**</dt> </dl>                   | Devuelve la función de ajuste de un solo valor para las coordenadas *de textura ,* una constante simbólica.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ T**</dt> </dl>                   | Devuelve la función de ajuste de un solo valor para la coordenada *de textura t*, una constante simbólica.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**COLOR DEL \_ BORDE \_ DE TEXTURA \_ GL**</dt> </dl> | Devuelve cuatro números enteros o de punto flotante que componen el color RGBA del borde de textura. Los valores de punto flotante se devuelven en el \[ intervalo 0,1. \] Los valores enteros se devuelven como una asignación lineal de la representación interna de punto flotante, de modo que 1,0 se asigna al entero más positivo que se puede representar y -1,0 se asigna al entero que se puede representar más negativo.<br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**PRIORIDAD \_ DE TEXTURA \_ GL**</dt> </dl>              | Devuelve la prioridad de residencia de la textura de destino (o la textura con nombre enlazada a ella). El valor inicial es 1. Vea [**glPrioritizeTextures.**](glprioritizetextures.md)<br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <dt>**GL \_ TEXTURE \_ RESIDENT**</dt> </dl>              | Devuelve el estado de residencia de la textura de destino. Si el valor devuelto en params es GL \_ TRUE, la textura se encuentra en la memoria de textura. Vea [**glAreTexturesResident.**](glaretexturesresident.md)<br/>                                                                                                                                                                           |



 

</dd> <dt>

*params* 
</dt> <dd>

Devuelve los parámetros de textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *target* o *name* no era un valor aceptado.<br/>                                                                              |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glGetTexParameter** devuelve en *parámetros* el valor o los valores del parámetro de textura especificado como *pname*. El *parámetro de* destino define la textura de destino, ya sea GL TEXTURE 1D o GL TEXTURE 2D, para especificar el texturizado \_ \_ unidimensional o \_ \_ bidimensional. El *parámetro pname* acepta los mismos símbolos que [**glTexParameter**](gltexparameter-functions.md), con las mismas interpretaciones.

Si se genera un error, no se realiza ningún cambio en el contenido de *params*.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





