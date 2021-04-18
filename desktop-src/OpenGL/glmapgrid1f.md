---
title: función glMapGrid1f (GL. h)
description: Define una malla unidimensional. | función glMapGrid1f (GL. h)
ms.assetid: 242c0197-2fa6-4356-b536-627660ebd3a7
keywords:
- glMapGrid1f (función) OpenGL
topic_type:
- apiref
api_name:
- glMapGrid1f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75479e8e25098fbfc5b906ba1785913cba9f2e30
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689718"
---
# <a name="glmapgrid1f-function"></a>glMapGrid1f función)

Define una malla unidimensional.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glMapGrid1f(
   GLint   un,
   GLfloat u1,
   GLfloat u2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*un* 
</dt> <dd>

El número de particiones en el intervalo de intervalo de la cuadrícula \[ U1, U2 \] . Este valor debe ser positivo.

</dd> <dt>

*U1* 
</dt> <dd>

Valor que se usa como asignación para el valor de dominio de la cuadrícula de enteros i = 0.

</dd> <dt>

*U2* 
</dt> <dd>

Un valor que se usa como asignación para el valor de dominio de la cuadrícula de enteros i = un.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | *Un* o *vn* no era positivo.<br/>                                                                                      |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Las funciones **glMapGrid** y [glEvalMesh](glevalmesh-functions.md) se usan en conjunto para generar y evaluar eficazmente una serie de valores de dominio de mapa con espaciado uniforme. La función glEvalMesh se recorre a través del dominio entero de una cuadrícula de una o dos dimensiones, cuyo intervalo es el dominio de las asignaciones de evaluación especificadas por [**glMap1**](glmap1.md) y [**glMap2**](glmap2.md).

Las funciones [**glMapGrid1**](glmapgrid1d.md) y [**glMapGrid2**](glmapgrid2d.md) especifican las asignaciones de cuadrícula lineal entre las coordenadas de la cuadrícula de los enteros i (o i y j), a las coordenadas de mapa de evaluación de punto flotante u (o y v). Vea [**glMap1**](glmap1.md) y [**glMap2**](glmap2.md) para obtener información detallada sobre cómo se evalúan las coordenadas de y v.

La función [**glMapGrid1**](glmapgrid1d.md) especifica una asignación lineal única, de modo que la *coordenada de* la cuadrícula entera 0 se asigna exactamente a U1, y la coordenada de la cuadrícula de enteros es una asignada exactamente a *U2*. Todas las *demás coordenadas de* la cuadrícula de enteros se asignan de manera que:

*u = i (U2 U1)/un + U1*

La función [**glMapGrid2**](glmapgrid2d.md) especifica dos asignaciones lineales de este tipo. Una cuadrícula de enteros de asignación coordina *i = 0* exactamente a *U1* y las coordenadas de la cuadrícula de enteros *i =* out exactamente a *U2*. La otra coordenada de la cuadrícula de enteros de Maps *j = 0* exactamente a *v1* y la coordenada de la cuadrícula de enteros *j = vn* exactamente a *V2*. Las coordenadas i y j de otras cuadrículas de enteros se asignan de forma que

*u = i (U2 U1)/un + U1*

*v = j (V2 V1)/VN + v1*

Las asignaciones especificadas por [**glMapGrid**](glmapgrid1d.md) se usan de forma idéntica en [glEvalMesh](glevalmesh-functions.md) y [**glEvalPoint**](glevalpoint.md).

Las siguientes funciones recuperan información relacionada con [**glMapGrid**](glmapgrid1d.md):

<dl>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAP1 \_ Grid \_ Domain  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAP2 ( \_ Grid \_ Domain  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MAP1 \_ segmentos de cuadrícula de GL \_  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ MAP2 ( \_ segmentos de cuadrícula de GL \_  
</dl>

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

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[glEvalMesh](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





