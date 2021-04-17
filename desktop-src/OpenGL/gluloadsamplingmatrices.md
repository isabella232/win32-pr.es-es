---
title: función gluLoadSamplingMatrices (GLU. h)
description: La función gluLoadSamplingMatrices carga las matrices de muestreo y selección de la spline B-spline racional (NURBS) no uniformes.
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- gluLoadSamplingMatrices (función) OpenGL
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
ms.openlocfilehash: 293b8bace0dff7d89bfcffa2af33738e0e59de7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665953"
---
# <a name="gluloadsamplingmatrices-function"></a>gluLoadSamplingMatrices función)

La función **gluLoadSamplingMatrices** carga las matrices de muestreo y selección de la spline B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)) no uniformes.

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

El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*modelMatrix* 
</dt> <dd>

Matriz MODELVIEW (a partir de una llamada a [**glGetFloatv**](glgetfloatv.md) ).

</dd> <dt>

*projMatrix* 
</dt> <dd>

Matriz de proyección (a partir de una llamada a **glGetFloatv** ).

</dd> <dt>

*encuadre* 
</dt> <dd>

Una ventanilla (a partir de una llamada a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluLoadSamplingMatrices** usa *modelMatrix*, *projMatrix* y *viewport* para volver a calcular las matrices de muestreo y selección almacenadas en *nobj*. La matriz de muestreo determina la precisión con que una curva o superficie de NURBS debe ser teselada para satisfacer la tolerancia de muestreo (según lo determinado por la propiedad de tolerancia de muestreo de GLU \_ \_ ). La matriz de selección se usa para decidir si se debe seleccionar una curva o superficie de NURBS antes de la representación (cuando la \_ propiedad de selección de Glu está activada).

La función **gluLoadSamplingMatrices** solo es necesaria si la propiedad de la matriz de carga automática Glu está desactivada \_ \_ \_ (consulte [**gluNurbsProperty**](glunurbsproperty.md)). Aunque puede ser conveniente dejar \_ \_ activada la \_ propiedad de matriz de carga automática de Glu, al hacerlo se requiere un recorrido de ida y vuelta al servidor de OpenGL para obtener los valores actuales de la matriz de MODELVIEW, la matriz de proyección y la ventanilla).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
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

 

 





