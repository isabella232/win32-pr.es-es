---
title: Función glEvalPoint2 (Gl.h)
description: Las funciones glEvalPoint1 y glEvalPoint2 generan y evalúan un único punto en una malla. | Función glEvalPoint2 (Gl.h)
ms.assetid: babae9c7-84a8-4a7e-b6f9-97c4e8bd42fe
keywords:
- Función GlEvalPoint2 OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f0c188ec5f3e8171b8035e58b235bc0c5942e221d6d85a6dd4e5a8ff1786c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675571"
---
# <a name="glevalpoint2-function"></a>Función glEvalPoint2

Las [**funciones glEvalPoint1**](glevalpoint.md) y **glEvalPoint2** generan y evalúan un único punto en una malla.

## <a name="syntax"></a>Sintaxis


```C++
void glEvalPoint2(
   GLint i,
   GLint j
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*i* 
</dt> <dd>

Valor entero de la variable de dominio de cuadrícula *i*.

</dd> <dt>

*J* 
</dt> <dd>

Valor entero de la variable de dominio de cuadrícula *j* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Las [**funciones glMapGrid**](glmapgrid-functions.md) y [**glEvalMesh**](glevalmesh-functions.md) se usan conjuntamente para generar y evaluar eficazmente una serie de valores de dominio de mapa espaciados uniformemente. Puede usar **glEvalPoint para** evaluar un único punto de cuadrícula en el mismo espacio de cuadrícula que **atraviesa glEvalMesh.** Llamar [**a glEvalPoint1**](glevalpoint.md) equivale a llamar a

**glEvalCoord1** (*i* ?*u*  + *u* 1 );

where

? *u* = (*u* 2 *u* 1 )/*n*

y *n*, *u* 1 y *u* 2 son los argumentos de la función **glMapGrid1 más** reciente. El único requisito numérico absoluto es que si *i*  =  *n*, el valor calculado a partir de (*i* ?*u* + u1 ) es exactamente *u* 2 .

En el caso bidimensional, **glEvalPoint2**, let

? *u* = (*u* 2 *u* 1 )/*n*

? *v* = (*v* 2 *v* 1 )/*m*

donde *n*, *u* 1, *u* 2 , *m*, *v* 1 y *v* 2 son los argumentos de la función **glMapGrid2** más reciente. A **continuación, la función glEvalPoint2** equivale a llamar a

**glEvalCoord2** (*i* ?*u*  +  *u u* 1 , *j* ?*v*  +  *v* 1 );

Los únicos requisitos numéricos absolutos son que si *i* = *n*, el valor calculado a partir de (*i* ?*u*  +  *u* 1 ) es exactamente u2 y, si *j*  =  *m*, el valor calculado a partir de (*j* ?*v*  +  *v* 1 ) es exactamente *v2.*

Las funciones siguientes recuperan información relacionada [**con glEvalPoint1**](glevalpoint.md) y **glEvalPoint2**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ MAP1 \_ GRID \_ DOMAIN

**glGet con** el argumento GL \_ MAP2 \_ GRID \_ DOMAIN

**glGet con** el argumento GL \_ MAP1 \_ GRID \_ SEGMENTS

**glGet con** el argumento GL \_ MAP2 \_ GRID \_ SEGMENTS

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

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> </dl>

 

 





