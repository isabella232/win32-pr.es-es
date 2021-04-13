---
title: función glScalef (GL. h)
description: Las funciones glScaled y glScalef multiplican la matriz actual por una matriz de escala general. | función glScalef (GL. h)
ms.assetid: bf039bbc-7669-4282-b629-71440b798cb1
keywords:
- glScalef (función) OpenGL
topic_type:
- apiref
api_name:
- glScalef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eda183b763f22736370dd5c9ea13ca8793243e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104568856"
---
# <a name="glscalef-function"></a>glScalef función)

Las funciones [**glScaled**](glscaled.md) y **glScalef** multiplican la matriz actual por una matriz de escala general.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glScalef(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x* 
</dt> <dd>

Factores de escala a lo largo del eje *x* .

</dd> <dt>

*y* 
</dt> <dd>

Factores de escala a lo largo del eje *y* .

</dd> <dt>

*z* 
</dt> <dd>

Factores de escala a lo largo del eje *z* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glScalef** genera una escala general a lo largo de los ejes *x*, *y* y *z* . Los tres argumentos indican los factores de escala deseados a lo largo de cada uno de los tres ejes. La matriz resultante aparece en la siguiente imagen.

![Diagrama que muestra la matriz de factores de escala a lo largo de los ejes x, y y z.](images/scale01.png)

La matriz actual (vea [**glMatrixMode**](glmatrixmode.md)) se multiplica por esta matriz de escala, con el producto que reemplaza la matriz actual. Es decir, si M es la matriz actual y S es la matriz de escala, M se reemplaza por M S.

Si el modo de matriz es \_ MODELVIEW de GL o \_ proyección de contabilidad, se escalan todos los objetos dibujados después de **glScalef** . Use [**glPushMatrix**](glpushmatrix.md) y [**glPopMatrix**](glpopmatrix.md) para guardar y restaurar el sistema de coordenadas sin escala.

Si se aplican factores de escala distintos de 1,0 a la matriz de MODELVIEW y la iluminación está habilitada, la normalización automática de las normales también debe estar habilitada ([**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento normalizar libro de contabilidad \_ ).

Las siguientes funciones recuperan información relacionada con **glScalef**:

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

[**glRotated**](glrotated.md)
</dt> <dt>

[**glRotatef**](glrotatef.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> </dl>

 

 





