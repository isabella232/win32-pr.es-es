---
title: Función glGetTexGendv (Gl.h)
description: Las funciones glGetTexGendv, glGetTexGenfv y glGetTexGeniv devuelven parámetros de generación de coordenadas de textura. | Función glGetTexGendv (Gl.h)
ms.assetid: bce26bde-071b-476e-9e33-c43a8c997cdd
keywords:
- Función glGetTexGendv OpenGL
topic_type:
- apiref
api_name:
- glGetTexGendv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f020d72ee0a9e89cbe490bed4a51e4df95096a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260180"
---
# <a name="glgettexgendv-function"></a>Función glGetTexGendv

Las **funciones glGetTexGendv**, [**glGetTexGenfv**](glgettexgenfv.md)y [**glGetTexGeniv**](glgettexgeniv.md) devuelven parámetros de generación de coordenadas de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetTexGendv(
   GLenum   coord,
   GLenum   pname,
   GLdouble *params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Coord* 
</dt> <dd>

Coordenada de textura. Debe ser GL \_ S, GL \_ T, GL \_ R o GL \_ Q.

</dd> <dt>

*pname* 
</dt> <dd>

Nombre simbólico de los valores que se devolverán. Debe ser GL TEXTURE GEN MODE o el nombre de una de las ecuaciones del plano de generación de \_ \_ \_ texturas: GL \_ OBJECT PLANE o GL EYE \_ \_ \_ PLANE. Estos valores son los siguientes.



| Value                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <dt>**MODO GEN \_ DE \_ TEXTURA \_ GL**</dt> </dl> | El *parámetro params* devuelve la función de generación de textura de un solo valor, una constante simbólica.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <dt>**PLANO \_ DE OBJETOS \_ GL**</dt> </dl>              | El *parámetro params* devuelve los coeficientes de ecuación de cuatro plano que especifican la generación de coordenadas lineales de objetos. Los valores enteros, cuando se solicitan, se asignan directamente desde la representación interna de punto flotante.<br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <dt>**GL \_ EYE \_ PLANE**</dt> </dl>                       | El *parámetro params* devuelve los coeficientes de ecuación de cuatro plano que especifican la generación de coordenadas lineales de los ojos. Los valores enteros, cuando se solicitan, se asignan directamente desde la representación interna de punto flotante. Los valores devueltos son los que se mantienen en coordenadas de los ojos. No son iguales a los valores especificados mediante [**glTexGen**](gltexgen-functions.md), a menos que se identificara la matriz modelview en el momento en que se llamó **a glTexGen.**<br/> |



 

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
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *coord o* *pname* no era un valor aceptado.<br/>                                                                              |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glGetTexGen** devuelve en *parámetros seleccionados los parámetros* de una función de generación de coordenadas de textura que especificó con **glTexGen**. El *parámetro coord* denomina una de las coordenadas de textura (*s*, *t*, *r*, *q*), mediante la constante simbólica GL \_ S, GL \_ T, GL R o GL \_ \_ Q.

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

[**glTexGen**](gltexgen-functions.md)
</dt> </dl>

 

 





