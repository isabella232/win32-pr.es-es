---
title: Función glMapGrid2f (Gl.h)
description: Define una malla unidimensional. | Función glMapGrid2f (Gl.h)
ms.assetid: f9bc2b0c-dec5-4762-8c99-46546a81893e
keywords:
- Función glMapGrid2f OpenGL
topic_type:
- apiref
api_name:
- glMapGrid2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37975e7ca88f829286872b5352ff3e59d84fd4d123d457defb01b6d14003dad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358943"
---
# <a name="glmapgrid2f-function"></a>Función glMapGrid2f

Define una malla unidimensional.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glMapGrid2f(
   GLint   un,
   GLfloat u1,
   GLfloat u2,
   GLint   vn,
   GLfloat v1,
   GLfloat v2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*un* 
</dt> <dd>

Número de particiones en el intervalo de intervalo de cuadrícula \[ u1, u2 \] . Este valor debe ser positivo.

</dd> <dt>

*u1* 
</dt> <dd>

Valor que se usa como asignación para el valor de dominio de cuadrícula de enteros i = 0.

</dd> <dt>

*u2* 
</dt> <dd>

Valor que se usa como asignación para el valor de dominio de cuadrícula de enteros i = un.

</dd> <dt>

*Vn* 
</dt> <dd>

Número de particiones en el intervalo de intervalo de cuadrícula \[ v1, v2 \] .

</dd> <dt>

*v1* 
</dt> <dd>

Valor utilizado como asignación para el valor de dominio de cuadrícula de enteros j = 0.

</dd> <dt>

*v2* 
</dt> <dd>

Valor que se usa como asignación para el valor de dominio de cuadrícula de enteros j = vn.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | Un *o* *vn no* fueron positivos.<br/>                                                                                      |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

Las **funciones glMapGrid** y [glEvalMesh](glevalmesh-functions.md) se usan conjuntamente para generar y evaluar eficazmente una serie de valores de dominio de mapa espaciados uniformemente. La función glEvalMesh atraviesa el dominio entero de una cuadrícula unidimensional, cuyo intervalo es el dominio de los mapas de evaluación especificados por [**glMap1**](glmap1.md) y [**glMap2.**](glmap2.md)

Las [**funciones glMapGrid1**](glmapgrid1d.md) y [**glMapGrid2**](glmapgrid2d.md) especifican las asignaciones de cuadrícula lineal entre las coordenadas de cuadrícula de enteros i (o i y j), a las coordenadas del mapa de evaluación de punto flotante u (o usted y v). Consulte [**glMap1**](glmap1.md) y [**glMap2 para**](glmap2.md) obtener más información sobre cómo se evalúan las coordenadas v y usted.

La [**función glMapGrid1**](glmapgrid1d.md) especifica una asignación lineal única, de modo que la  coordenada de cuadrícula de enteros 0 se asigna exactamente a u1 y la coordenada de cuadrícula de enteros se asigna exactamente a *u2.* Todas las demás coordenadas de cuadrícula de *enteros i* están asignadas de forma que:

*u = i(u2 u1)/un + u1*

La [**función glMapGrid2**](glmapgrid2d.md) especifica dos de estas asignaciones lineales. Una asigna la coordenada de cuadrícula *de enteros i = 0* exactamente *a u1* y la coordenada de cuadrícula de *enteros i = un* exactamente a *u2*. El otro asigna la coordenada de cuadrícula de *enteros j = 0* exactamente *a v1* y la coordenada de cuadrícula de *enteros j = vn* exactamente a *v2.* Otras coordenadas de cuadrícula de enteros i y j se asignan de forma que

*u = i(u2 u1)/un + u1*

*v = j (v2 v1)/vn + v1*

[GlEvalMesh](glevalmesh-functions.md) y [**glEvalPoint**](glevalpoint.md)usan de forma idéntica las asignaciones especificadas por [**glMapGrid.**](glmapgrid1d.md)

Las siguientes funciones recuperan información relacionada con [**glMapGrid**](glmapgrid1d.md):

<dl>

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAP1 \_ GRID \_ DOMAIN  
[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAP2 \_ GRID \_ DOMAIN  
[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAP1 \_ GRID \_ SEGMENTS  
[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAP2 \_ GRID \_ SEGMENTS  
</dl>

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

 

 





