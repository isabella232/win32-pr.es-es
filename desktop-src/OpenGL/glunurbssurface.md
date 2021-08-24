---
title: Función gluNurbsSurface (Glu.h)
description: La función gluNurbsSurface define la forma de una superficie de spline B racionalizada no uniforme (SPLINEBS).
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- Función gluNurbsSurface OpenGL
topic_type:
- apiref
api_name:
- gluNurbsSurface
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50f56232ac891cbdfba18195741d875ecc5436112772ed4fa665903374e96602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554195"
---
# <a name="glunurbssurface-function"></a>función gluNurbsSurface

La **función gluNurbsSurface** define la forma de una superficie de spline B no uniforme de tipo rational [(SPLINEBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluNurbsSurface(
   GLUnurbs *nobj,
   GLint    sknot_count,
   float    *sknot,
   GLint    tknot_count,
   GLfloat  *tknot,
   GLint    s_stride,
   GLint    t_stride,
   GLfloat  *ctlarray,
   GLint    sorder,
   GLint    torder,
   GLenum   type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nobj* 
</dt> <dd>

El objeto RGBBS (creado [**con gluNewNurbsRenderer).**](glunewnurbsrenderer.md)

</dd> <dt>

*sknot \_ count* 
</dt> <dd>

Número de sincronos en la dirección U *paramétrica.*

</dd> <dt>

*sknot* 
</dt> <dd>

Matriz de valores *sknot \_ count* no decrecientes en la dirección *u* paramétrica.

</dd> <dt>

*tknot \_ count* 
</dt> <dd>

Número de grados en la dirección v *paramétrica.*

</dd> <dt>

*tknot* 
</dt> <dd>

Matriz de valores de reducción no decrecientes de *tknot \_ count* en la dirección *v* paramétrica.

</dd> <dt>

*s \_ stride* 
</dt> <dd>

Desplazamiento (como un número de valores de punto de precisión única)  entre los puntos de control sucesivos en la dirección u paramétrica en *ctlarray*.

</dd> <dt>

*t \_ stride* 
</dt> <dd>

Desplazamiento (en valores de punto de precisión única) entre los  puntos de control sucesivos en la dirección v paramétrica en *ctlarray*.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Matriz que contiene puntos de control para la superficie DE LABS. Los desplazamientos entre los puntos de control sucesivos en *\_* las direcciones *u* y *v* paramétricas se dan por un intervalo y un intervalo *\_ de t.*

</dd> <dt>

*sorder* 
</dt> <dd>

El orden de la superficie de LABS en la *dirección* u paramétrica. El orden es uno más que el grado, por lo que una superficie que es cúbica en *u* tiene *un orden u* de 4.

</dd> <dt>

*torder* 
</dt> <dd>

El orden de la superficie de LABS en la dirección v *paramétrica.* El orden es uno más que el grado, por lo que una superficie que es cúbica en *v* tiene un *orden v* de 4.

</dd> <dt>

*type* 
</dt> <dd>

Tipo de la superficie. El *parámetro* de tipo puede ser cualquiera de los tipos válidos de evaluador bidimensional (como GL \_ MAP2 VERTEX 3 o GL \_ \_ \_ MAP2 COLOR \_ \_ 4).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Use **gluNurbsSurface dentro** de una definición de superficie DE DSLBS para describir la forma de una superficie DE LABS (antes de cualquier recorte). Para marcar el principio de una definición de superficie DE LABS, use la [**función gluBeginSurface.**](glubeginsurface.md) Para marcar el final de una definición de superficie DE LABS, use la [**función gluEndSurface.**](gluendsurface.md) Llame **a gluNurbsSurface solo** dentro de una definición de superficie DE DSLBS.

Las coordenadas de posición, textura y color se asocian a una superficie mediante la presentación de cada una como un **gluNurbsSurface** independiente entre un par **gluBeginSurface** / **gluEndSurface.** Dentro de un único par **gluBeginSurface** gluEndSurface, solo puede realizar una llamada a /  **gluNurbsSurface** para obtener datos de color, posición y textura. Realice exactamente una llamada para describir la  posición de la superficie (un tipo de GL \_ MAP2 VERTEX 3 o GL \_ \_ \_ MAP2 \_ VERTEX \_ 4).

Puede recortar una superficie DETRUBS mediante las funciones [**gluNurbsCurve**](glunurbscurve.md) y [**gluPwlCurve**](glupwlcurve.md) entre las llamadas a [**gluBeginTrim**](glubegintrim.md) y [**gluEndTrim**](gluendtrim.md).

Un **gluNurbsSurface** con recuento de *sknot \_* en la dirección *u* y *tknot \_ count* en la *dirección v* con orders *sorder* y *torder* deben tener (*sknot \_ count*  - *sorder*) multipied por (*tknot \_ count*  - *torder*) puntos de control.

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

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluEndSurface**](gluendsurface.md)
</dt> <dt>

[**gluEndTrim**](gluendtrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





