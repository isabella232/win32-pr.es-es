---
title: Función glPopMatrix (Gl.h)
description: Las funciones glPushMatrix y glPopMatrix insertan y devuelven la pila de matriz actual. | Función glPopMatrix (Gl.h)
ms.assetid: 7b4fc26e-36c8-4252-aba7-2e8ec6b34f91
keywords:
- Función glPopMatrix OpenGL
topic_type:
- apiref
api_name:
- glPopMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c0f10456c1038da46d9070689713a8237f876bec7ce7da40acf3d81d89ad15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128025"
---
# <a name="glpopmatrix-function"></a>Función glPopMatrix

Las [**funciones glPushMatrix**](glpushmatrix.md) y **glPopMatrix** insertan y devuelven la pila de matriz actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPopMatrix(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Es un error insertar una pila de matriz completa o sacar una pila de matriz que contiene solo una matriz. En cualquier caso, se establece la marca de error y no se realiza ningún otro cambio en el estado OpenGL.

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ UNDERFLOW**</dt> </dl>   | Se llamó a la función mientras la pila de matriz actual solo contenía una sola matriz.<br/>                                     |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

Hay una pila de matrices para cada uno de los modos de matriz. En el \_ modo GL MODELVIEW, la profundidad de la pila es al menos 32. En los otros dos modos, GL \_ PROJECTION y GL \_ TEXTURE, la profundidad es al menos 2. La matriz actual en cualquier modo es la matriz en la parte superior de la pila para ese modo.

La [**función glPushMatrix**](glpushmatrix.md) presiona una vez la pila de matriz actual, duplicando la matriz actual. Es decir, después de una **llamada a glPushMatrix,** la matriz de la parte superior de la pila es idéntica a la que hay debajo de ella. La **función glPopMatrix** muestra la pila de matriz actual, reemplazando la matriz actual por la que está debajo de ella en la pila. Inicialmente, cada una de las pilas contiene una matriz, una matriz de identidad.

Las funciones siguientes recuperan información relacionada [**con glPushMatrix**](glpushmatrix.md) y **glPopMatrix**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MATRIX \_ MODE

**glGet con** el argumento GL \_ MODELVIEW \_ MATRIX

**glGet con** el argumento GL \_ PROJECTION \_ MATRIX

**glGet con** el argumento GL \_ TEXTURE \_ MATRIX

**glGet con** el argumento GL \_ MODELVIEW \_ STACK \_ DEPTH

**glGet con** el argumento GL \_ PROJECTION STACK \_ \_ DEPTH

**glGet con** el argumento GL \_ TEXTURE STACK \_ \_ DEPTH

**glGet con** el argumento GL \_ MAX \_ MODELVIEW STACK \_ \_ DEPTH

**glGet con** el argumento GL \_ MAX PROJECTION STACK \_ \_ \_ DEPTH

**glGet con** el argumento GL \_ MAX TEXTURE STACK \_ \_ \_ DEPTH

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





