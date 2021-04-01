---
title: función glEvalPoint1 (GL. h)
description: Las funciones glEvalPoint1 y glEvalPoint2 generan y evalúan un solo punto en una malla. | función glEvalPoint1 (GL. h)
ms.assetid: 5ef1d2f0-d77b-4bb8-a0d4-45c1a6a91c18
keywords:
- glEvalPoint1 (función) OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b9c3b8e17f5a0554c1864a401ecf49343806c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914622"
---
# <a name="glevalpoint1-function"></a>glEvalPoint1 función)

Las funciones [**glEvalPoint1**](glevalpoint.md) y **glEvalPoint2** generan y evalúan un solo punto en una malla.

## <a name="syntax"></a>Sintaxis


```C++
void glEvalPoint1(
   GLint i
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*i* 
</dt> <dd>

Valor entero para la variable de dominio de la cuadrícula *i*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las funciones [**glMapGrid**](glmapgrid-functions.md) y [**glEvalMesh**](glevalmesh-functions.md) se usan en conjunto para generar y evaluar eficazmente una serie de valores de dominio de mapa con espaciado uniforme. Puede usar **glEvalPoint** para evaluar un solo punto de la cuadrícula en el mismo gridspace que atraviesa **glEvalMesh**. Llamar a [**glEvalPoint1**](glevalpoint.md) es equivalente a llamar a

**glEvalCoord1** (*i* ?*u*  + *u* 1);

where

? *u* = (*u* 2 *u* 1)/*n*

y *n*, *u* 1 y *u* 2 son los argumentos de la función **glMapGrid1** más reciente. El único requisito absoluto es que *, si*  =  *n*, el valor calculado de (*i* ?*u* + U1) es exactamente *u* 2.

En el caso bidimensional, **glEvalPoint2**, Let

? *u* = (*u* 2 *u* 1)/*n*

? *v* = (*v* 2 *v* 1)/*m*

donde *n*, *u* 1, *u* 2, *m*, *v* 1 y *v* 2 son los argumentos de la función **glMapGrid2** más reciente. A continuación, la función **glEvalPoint2** es equivalente a llamar a

**glEvalCoord2** (*i* ?*u*  +  *u* 1, *j* ?*v*  +  1);

Los únicos requisitos numéricos absolutos son que *, si* = *n*, el valor calculado de (*i* ?*u*  +  *u* 1) es exactamente U2 y, si es *j*  =  *m*, el valor calculado desde (*j* ?*v*  +  1) es exactamente *v* 2.

Las siguientes funciones recuperan información relacionada con [**glEvalPoint1**](glevalpoint.md) y **glEvalPoint2**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAP1 \_ Grid \_ Domain

**glGet** con el argumento GL \_ MAP2 ( \_ Grid \_ Domain

**glGet** con el argumento \_ MAP1 \_ segmentos de cuadrícula de GL \_

**glGet** con el argumento \_ MAP2 ( \_ segmentos de cuadrícula de GL \_

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

 

 





