---
title: función glGetTexGeniv (GL. h)
description: Las funciones glGetTexGendv, glGetTexGenfv y glGetTexGeniv devuelven parámetros de generación de coordenadas de textura. | función glGetTexGeniv (GL. h)
ms.assetid: 62c481d1-4862-43bb-9319-5a282c4e47d3
keywords:
- glGetTexGeniv (función) OpenGL
topic_type:
- apiref
api_name:
- glGetTexGeniv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29569c84d21dbb2cd69579c78747e844cfd23ba4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689733"
---
# <a name="glgettexgeniv-function"></a>glGetTexGeniv función)

Las funciones [**glGetTexGendv**](glgettexgendv.md), [**glGetTexGenfv**](glgettexgenfv.md)y **glGetTexGeniv** devuelven parámetros de generación de coordenadas de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetTexGeniv(
   GLenum coord,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*coords* 
</dt> <dd>

Coordenada de textura. Debe ser GL \_ S, GL \_ T, GL \_ R o GL \_ Q.

</dd> <dt>

*PName* 
</dt> <dd>

Nombre simbólico de los valores que se van a devolver. Debe ser el modo de generación de \_ textura GL \_ \_ o el nombre de una de las ecuaciones del plano de generación de textura: plano de \_ objeto GL \_ o plano de ojo de contabilidad \_ \_ . Estos valores son los siguientes.



| Value                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <dt>**\_modo de generación de texturas GL \_ \_**</dt> </dl> | El parámetro *params* devuelve la función de generación de textura de un solo valor, una constante simbólica.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <dt>**\_plano del objeto GL \_**</dt> </dl>              | El parámetro *params* devuelve los cuatro coeficientes de ecuaciones de plano que especifican la generación de coordenada lineal del objeto. Los valores enteros, cuando se solicitan, se asignan directamente desde la representación interna de punto flotante.<br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <dt>**\_plano de ojo de contabilidad \_**</dt> </dl>                       | El parámetro *params* devuelve los cuatro coeficientes de ecuaciones de plano que especifican la generación de coordenada lineal. Los valores enteros, cuando se solicitan, se asignan directamente desde la representación interna de punto flotante. Los valores devueltos son los que se mantienen en coordenadas oculares. No son iguales a los valores especificados mediante [**glTexGen**](gltexgen-functions.md), a menos que se haya identificado la matriz MODELVIEW en el momento en que se llamó a **glTexGen** .<br/> |



 

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
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | la expresión de *coordenadas* o *PName* no era un valor aceptado.<br/>                                                                              |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glGetTexGen** devuelve en *params* parámetros seleccionados de una función de generación de coordenadas de textura que especificó con **glTexGen**. El parámetro *coords* asigna un nombre a una de las coordenadas de textura (*s*, *t*, *r*, *q*), mediante la constante simbólica GL \_ s, GL \_ t, GL \_ r o GL \_ q.

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

[**glTexGen**](gltexgen-functions.md)
</dt> </dl>

 

 





