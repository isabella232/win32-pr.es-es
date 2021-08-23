---
title: Función glLoadMatrixf (Gl.h)
description: La función glLoadMatrixf reemplaza la matriz actual por una matriz arbitraria. | Función glLoadMatrixf (Gl.h)
ms.assetid: 6e1337b0-d1e7-4002-a561-d959d7f70942
keywords:
- Función glLoadMatrixf OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3d822d784d6e24b15296a29da1c77b37b55af4211d2d9b5ce40a3c6a43c7fdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492854"
---
# <a name="glloadmatrixf-function"></a>Función glLoadMatrixf

Las [**funciones glLoadMatrixd**](glloadmatrixd.md) **y glLoadMatrixf** reemplazan la matriz actual por una matriz arbitraria.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glLoadMatrixf(
   const GLfloat *m
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*m* 
</dt> <dd>

Puntero a una matriz de 4x4 almacenada en orden de columna principal como 16 valores consecutivos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glLoadMatrix** reemplaza la matriz actual por la especificada en *m*. La matriz actual es la matriz de proyección, la matriz modelview o la matriz de textura, determinada por el modo de matriz actual (vea [**glMatrixMode**](glmatrixmode.md)).

El *parámetro m* apunta a una matriz 4x4 de valores de punto flotante de precisión sencilla o de precisión doble almacenados en orden de columna principal. Es decir, la matriz se almacena como se muestra en la siguiente imagen.

![Diagrama que muestra la matriz 4x4 a la que apunta el parámetro m.](images/load02.png)

Las siguientes funciones recuperan información relacionada **con glLoadMatrix**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MATRIX \_ MODE

**glGet** con el argumento GL \_ MODELVIEW \_ MATRIX

**glGet con** el argumento GL \_ PROJECTION \_ MATRIX

**glGet con** el argumento GL \_ TEXTURE \_ MATRIX

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





