---
title: Función glGetTexEnvfv (Gl.h)
description: Las funciones glGetTexEnvfv y glGetTexEnviv devuelven parámetros de entorno de textura. | Función glGetTexEnvfv (Gl.h)
ms.assetid: aa037494-e227-48f1-8d5e-9f82073dc2ea
keywords:
- Función glGetTexEnvfv OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnvfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14b9b294879711662c67f9ab581e89eaadfa620363e1d19e93f7ea686ba7453a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493875"
---
# <a name="glgettexenvfv-function"></a>Función glGetTexEnvfv

Las **funciones glGetTexEnvfv** y [**glGetTexEnviv**](glgettexenviv.md) devuelven parámetros de entorno de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetTexEnvfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Un entorno de textura. Debe ser GL \_ TEXTURE \_ ENV.

</dd> <dt>

*pname* 
</dt> <dd>

Nombre simbólico de un parámetro de entorno de textura. Se aceptan los valores siguientes.



| Value                                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <dt>**MODO DE \_ ENV DE \_ TEXTURA \_ GL**</dt> </dl>    | El *parámetro params* devuelve el modo de entorno de textura de un solo valor, una constante simbólica.<br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <dt>**COLOR DE \_ \_ ENV DE TEXTURA \_ GL**</dt> </dl> | El *parámetro params* devuelve cuatro valores enteros o de punto flotante que son el color del entorno de textura. Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación interna de punto flotante, de modo que 1,0 se asigna al entero representable más positivo y -1,0 se asigna al entero que se puede representar más negativo.<br/> |



 

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
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *target* o *pname* no era un valor aceptado.<br/>                                                                             |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glGetTexEnv** devuelve en *parámetros* los valores seleccionados de un entorno de textura que se especificó [**con glTexEnv**](gltexenv-functions.md). El *parámetro de* destino especifica un entorno de textura. Actualmente, solo se define y se admite un entorno de textura: GL \_ TEXTURE \_ ENV.

El *parámetro pname nombra* un parámetro de entorno de textura específico.

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

[**glTexEnv**](gltexenv-functions.md)
</dt> </dl>

 

 





