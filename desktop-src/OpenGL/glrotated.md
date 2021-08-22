---
title: Función glRotated (Gl.h)
description: La función glRotated multiplica la matriz actual por una matriz de rotación.
ms.assetid: 9adfeb5b-8c2a-4acf-a251-6ba23cc4c3a6
keywords:
- función glRotated OpenGL
topic_type:
- apiref
api_name:
- glRotated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32216eab9a7c7613f082470360d3f938bbdeaf8ae38cd875d84cd0338dfa78c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491775"
---
# <a name="glrotated-function"></a>función glRotated

La **función glRotated** multiplica la matriz actual por una matriz de rotación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glRotated(
   GLdouble angle,
   GLdouble x,
   GLdouble y,
   GLdouble z
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

*Coordenada x* de un vector.

</dd> <dt>

*y* 
</dt> <dd>

*Coordenada y* de un vector.

</dd> <dt>

*Z* 
</dt> <dd>

*Coordenada z* de un vector.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glRotated** calcula una matriz que realiza  una rotación en sentido contrario a las agujas del reloj de grados angulares sobre el vector desde el origen hasta el punto (*x*, *y*, *z*).

La matriz actual [**(vea glMatrixMode**](glmatrixmode.md)) se multiplica por esta matriz de rotación, con el producto reemplazando la matriz actual. Es decir, si M es la matriz actual y R es la matriz de traducción, M se reemplaza por M R.

Si el modo de matriz es GL MODELVIEW o GL PROJECTION, se giran todos los objetos dibujados después de llamar a \_ \_ **glRotated.** Use [**glPushMatrix**](glpushmatrix.md) y [**glPopMatrix para**](glpopmatrix.md) guardar y restaurar el sistema de coordenadas sin cargar.

Las siguientes funciones recuperan información relacionada **con glRotated**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ RENDER \_ MODE

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MATRIX \_ MODE

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MODELVIEW \_ MATRIX

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ PROJECTION \_ MATRIX

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ TEXTURE \_ MATRIX

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

 

 





