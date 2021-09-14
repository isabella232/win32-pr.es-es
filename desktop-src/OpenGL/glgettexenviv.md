---
title: Función glGetTexEnviv (Gl.h)
description: Las funciones glGetTexEnvfv y glGetTexEnviv devuelven parámetros de entorno de textura. | Función glGetTexEnviv (Gl.h)
ms.assetid: c1429cb9-4392-41ef-a978-a51db66445f2
keywords:
- Función glGetTexEnviv OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnviv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ff222b7de0bfcd5fa50e9fa5f260e329c60c69d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260188"
---
# <a name="glgettexenviv-function"></a>Función glGetTexEnviv

Las [**funciones glGetTexEnvfv**](glgettexenvfv.md) y **glGetTexEnviv** devuelven parámetros de entorno de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetTexEnviv(
   GLenum target,
   GLenum pname,
   GLint  *params
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



## <a name="remarks"></a>Observaciones

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> </dl>

 

 





