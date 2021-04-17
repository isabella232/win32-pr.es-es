---
title: función glGetTexEnvfv (GL. h)
description: Las funciones glGetTexEnvfv y glGetTexEnviv devuelven parámetros de entorno de textura. | función glGetTexEnvfv (GL. h)
ms.assetid: aa037494-e227-48f1-8d5e-9f82073dc2ea
keywords:
- glGetTexEnvfv (función) OpenGL
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
ms.openlocfilehash: 36d542461b05a824c78bbad82d843735289f2fb4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670144"
---
# <a name="glgettexenvfv-function"></a>glGetTexEnvfv función)

Las funciones **glGetTexEnvfv** y [**glGetTexEnviv**](glgettexenviv.md) devuelven parámetros de entorno de textura.

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

Entorno de textura. Debe ser un \_ \_ env Texture.

</dd> <dt>

*PName* 
</dt> <dd>

Nombre simbólico de un parámetro de entorno de textura. Se aceptan los siguientes valores.



| Value                                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <dt>**\_modo de textura del libro de contabilidad \_ \_**</dt> </dl>    | El parámetro *params* devuelve el modo de entorno de textura de un solo valor, una constante simbólica.<br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <dt>**\_color de textura de libro de contabilidad \_ \_**</dt> </dl> | El parámetro *params* devuelve cuatro valores enteros o de punto flotante que son el color del entorno de textura. Los valores enteros, cuando se solicitan, se asignan linealmente a partir de la representación de punto flotante interna, de modo que 1,0 se asigna al entero representable más positivo y-1,0 se asigna al entero representable más negativo.<br/> |



 

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
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glGetTexEnv** devuelve en *params* valores seleccionados de un entorno de textura que se especificó con [**glTexEnv**](gltexenv-functions.md). El parámetro de *destino* especifica un entorno de textura. Actualmente, solo se define y admite un entorno de textura: GL \_ Texture \_ env.

El parámetro *PName* nombra un parámetro de entorno de textura específico.

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

[**glTexEnv**](gltexenv-functions.md)
</dt> </dl>

 

 





