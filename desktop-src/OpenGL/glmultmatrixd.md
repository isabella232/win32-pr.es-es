---
title: Función glMultMatrixd (Gl.h)
description: La función glMultMatrixd multiplica la matriz actual por una matriz arbitraria. | Función glMultMatrixd (Gl.h)
ms.assetid: 1f6cf4e4-e7bd-470c-b1f4-b9ccc1fb756e
keywords:
- Función glMultMatrixd OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd31b3f84bbc8c75a3622b7b87f7a7577a33927bd489a06b8691377badaf0b56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358808"
---
# <a name="glmultmatrixd-function"></a>Función glMultMatrixd

Las **funciones glMultMatrixd** y [**glMultMatrixf**](glmultmatrixf.md) multiplican la matriz actual por una matriz arbitraria.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glMultMatrixd(
   const GLdouble *m
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

La **función glMultMatrix** multiplica la matriz actual por la especificada en *m*. Es decir, si M es la matriz actual y T es la matriz que se pasa **a glMultMatrix,** M se reemplaza por M T.

La matriz actual es la matriz de proyección, la matriz modelview o la matriz de textura, determinada por el modo de matriz actual (vea [**glMatrixMode**](glmatrixmode.md)).

El *parámetro m* apunta a una matriz 4x4 de valores de punto flotante de precisión sencilla o de precisión doble almacenados en orden de columna principal. Es decir, la matriz se almacena como se muestra en la siguiente imagen.

![! [Diagrama que muestra la matriz 4x4 a la que apunta el parámetro m].](images/multi01.png)

Las siguientes funciones recuperan información relacionada **con glMultMatrix**:

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





