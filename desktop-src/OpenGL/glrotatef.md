---
title: función glRotatef (GL. h)
description: La función glRotatef multiplica la matriz actual por una matriz de rotación.
ms.assetid: 8216a125-de8c-44e5-afb3-3d4e5ffc600d
keywords:
- glRotatef (función) OpenGL
topic_type:
- apiref
api_name:
- glRotatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 953b8ffc5f89e5a4cf9901e4cb5fb5afb4c8dfdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493222"
---
# <a name="glrotatef-function"></a>glRotatef función)

La función **glRotatef** multiplica la matriz actual por una matriz de rotación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glRotatef(
   GLfloat angle,
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*angle* 
</dt> <dd>

Ángulo de rotación, en grados.

</dd> <dt>

*x* 
</dt> <dd>

Coordenada *x* de un vector.

</dd> <dt>

*y* 
</dt> <dd>

Coordenada *y* de un vector.

</dd> <dt>

*z* 
</dt> <dd>

Coordenada *z* de un vector.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glRotatef** calcula una matriz que realiza un giro en sentido contrario de los grados *angulares* del vector desde el origen hasta el punto (*x*, *y*, *z*).

La matriz actual (vea [**glMatrixMode**](glmatrixmode.md)) se multiplica por esta matriz de rotación, donde el producto reemplaza la matriz actual. Es decir, si M es la matriz actual y R es la matriz de traslación, M se reemplaza por M R.

Si el modo de matriz es \_ MODELVIEW de GL o \_ proyección de contabilidad, se giran todos los objetos dibujados después de **glRotatef** . Use [**glPushMatrix**](glpushmatrix.md) y [**glPopMatrix**](glpopmatrix.md) para guardar y restaurar el sistema de coordenadas sin girar.

Las siguientes funciones recuperan información relacionada con **glRotatef**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de representación de contabilidad de argumentos \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MODELVIEW \_ matriz de contabilidad

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ matriz de proyección de contabilidad \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ matriz de textura de GL \_

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

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> </dl>

 

 





