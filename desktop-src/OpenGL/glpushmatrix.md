---
title: Función glPushMatrix (Gl.h)
description: Las funciones glPushMatrix y glPopMatrix insertan y devuelven la pila de matriz actual. | Función glPushMatrix (Gl.h)
ms.assetid: 97d8e644-50bb-4130-b6b7-d87df4468e73
keywords:
- Función glPushMatrix OpenGL
topic_type:
- apiref
api_name:
- glPushMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0d6af41bb02c82a28b667a2b5ad62d942c036c7f744a68fa9bb79188e26ae8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795140"
---
# <a name="glpushmatrix-function"></a>Función glPushMatrix

Las **funciones glPushMatrix** y [**glPopMatrix**](glpopmatrix.md) insertan y devuelven la pila de matriz actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPushMatrix(void);
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
| <dl> <dt>**GL \_ STACK \_ OVERFLOW**</dt> </dl>    | Se llamó a la función mientras la pila de matriz actual estaba llena.<br/>                                                           |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

Hay una pila de matrices para cada uno de los modos de matriz. En el \_ modo GL MODELVIEW, la profundidad de la pila es al menos 32. En los otros dos modos, GL \_ PROJECTION y GL \_ TEXTURE, la profundidad es al menos 2. La matriz actual en cualquier modo es la matriz en la parte superior de la pila para ese modo.

La **función glPushMatrix** presiona una vez la pila de matriz actual, duplicando la matriz actual. Es decir, después de una **llamada a glPushMatrix,** la matriz de la parte superior de la pila es idéntica a la que hay debajo de ella. La **función glPopMatrix** muestra la pila de matriz actual, reemplazando la matriz actual por la que está debajo de ella en la pila. Inicialmente, cada una de las pilas contiene una matriz, una matriz de identidad.

Las funciones siguientes recuperan información relacionada **con glPushMatrix** y **glPopMatrix**:

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

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





