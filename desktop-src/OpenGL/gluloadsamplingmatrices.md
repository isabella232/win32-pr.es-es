---
title: Función gluLoadSamplingMatrices (Glu.h)
description: La función gluLoadSamplingMatrices carga matrices de muestreo y de selección no uniformes de B-Spline lógica (SPLINE).
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- Función GluLoadSamplingMatrices OpenGL
topic_type:
- apiref
api_name:
- gluLoadSamplingMatrices
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41b2f6b25e0cecf0d13d87760a941d5ea68baa1fdd85495c8a316e862c77aec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777535"
---
# <a name="gluloadsamplingmatrices-function"></a>Función gluLoadSamplingMatrices

La **función gluLoadSamplingMatrices** carga matrices de muestreo y de selección no uniformes de B-Spline racionalizadas [(SPLINEBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluLoadSamplingMatrices(
         GLUnurbs *nobj,
   const GLfloat  modelMatrix[16],
   const GLfloat  projMatrix[16],
   const GLint    viewport[4]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nobj* 
</dt> <dd>

El objeto RGBBS (creado [**con gluNewNurbsRenderer).**](glunewnurbsrenderer.md)

</dd> <dt>

*modelMatrix* 
</dt> <dd>

Matriz modelview (como de una [**llamada a glGetFloatv).**](glgetfloatv.md)

</dd> <dt>

*projMatrix* 
</dt> <dd>

Matriz de proyección (a partir de una **llamada a glGetFloatv).**

</dd> <dt>

*Viewport* 
</dt> <dd>

Una ventanilla (como desde una [**llamada a glGetIntegerv).**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La **función gluLoadSamplingMatrices** usa *modelMatrix*, *projMatrix* y *viewport* para volver a compilar las matrices de muestreo y de selección almacenadas *en nobj*. La matriz de muestreo determina la forma en que se debe teselar una curva o una superficie DE ASBS para satisfacer la tolerancia de muestreo (según lo determinado por la propiedad GLU \_ SAMPLING \_ TOLERANCE). La matriz de selección se usa para decidir si se debe realizar la selección de una curva o una superficie DE LABS antes de la representación (cuando se ha activado la propiedad GLU \_ CULLING).

La **función gluLoadSamplingMatrices** solo es necesaria si la propiedad GLU AUTO LOAD MATRIX está desactivada \_ \_ \_ (vea [**gluNurbsProperty**](glunurbsproperty.md)). Aunque puede ser conveniente dejar activada la propiedad GLU AUTO LOAD MATRIX, para ello es necesario realizar un recorrido de ida y vuelta al servidor OpenGL para obtener los valores actuales de la matriz modelview, la matriz de proyección y la \_ \_ \_ ventanilla).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glGetFloatv**](glgetfloatv.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluGetNurbsProperty**](glugetnurbsproperty.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





