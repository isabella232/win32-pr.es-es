---
title: función glPopMatrix (GL. h)
description: Las funciones glPushMatrix y glPopMatrix envían y extraen la pila de matriz actual. | función glPopMatrix (GL. h)
ms.assetid: 7b4fc26e-36c8-4252-aba7-2e8ec6b34f91
keywords:
- glPopMatrix (función) OpenGL
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
ms.openlocfilehash: 41424a8af3ca6599edc7a66f9e498632640022c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670141"
---
# <a name="glpopmatrix-function"></a>glPopMatrix función)

Las funciones [**glPushMatrix**](glpushmatrix.md) y **glPopMatrix** envían y extraen la pila de matriz actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPopMatrix(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Es un error insertar una pila de matriz completa o extraer una pila de matriz que contenga una sola matriz. En cualquier caso, se establece la marca de error y no se realiza ningún otro cambio en el estado de OpenGL.

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**subdesbordamiento de la pila de GL \_ \_**</dt> </dl>   | Se llamó a la función mientras que la pila de matriz actual contenía solo una matriz única.<br/>                                     |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Hay una pila de matrices para cada uno de los modos de matriz. En \_ el modo GL MODELVIEW, la profundidad de la pila es al menos 32. En los otros dos modos, \_ proyección GL y \_ textura GL, la profundidad es al menos 2. La matriz actual en cualquier modo es la matriz de la parte superior de la pila para ese modo.

La función [**glPushMatrix**](glpushmatrix.md) empuja hacia abajo la pila de la matriz actual, duplicando la matriz actual. Es decir, después de una llamada a **glPushMatrix** , la matriz de la parte superior de la pila es idéntica a la que se encuentra debajo de ella. La función **glPopMatrix** extrae la pila de matriz actual, reemplazando la matriz actual por la que se encuentra debajo en la pila. Inicialmente, cada una de las pilas contiene una matriz, una matriz de identidad.

Las siguientes funciones recuperan información relacionada con [**glPushMatrix**](glpushmatrix.md) y **glPopMatrix**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_

**glGet** con el argumento \_ MODELVIEW \_ matriz de contabilidad

**glGet** con el argumento \_ matriz de proyección de contabilidad \_

**glGet** con el argumento \_ matriz de textura de GL \_

**glGet** con el argumento GL MODELVIEW de la \_ \_ pila \_

**glGet** con el argumento \_ profundidad de la pila de proyección GL \_ \_

**glGet** con el argumento \_ profundidad de la pila de textura de contabilidad \_ \_

**glGet** con el argumento GL \_ Max MODELVIEW de la \_ \_ pila \_

**glGet** con el argumento \_ profundidad de la \_ pila de proyección Max \_ \_

**glGet** con el argumento \_ profundidad máxima de la \_ pila de textura de \_ GL \_

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

 

 





