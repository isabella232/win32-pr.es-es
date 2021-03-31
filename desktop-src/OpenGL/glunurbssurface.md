---
title: función gluNurbsSurface (GLU. h)
description: La función gluNurbsSurface define la forma de una superficie no uniforme B-spline racional (NURBS).
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- gluNurbsSurface (función) OpenGL
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
ms.openlocfilehash: c784741eded406a49bba90f67544a406ab024a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995906"
---
# <a name="glunurbssurface-function"></a>gluNurbsSurface función)

La función **gluNurbsSurface** define la forma de una superficie no uniforme B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)).

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

El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*recuento de sknot \_* 
</dt> <dd>

Número de nudos en la dirección de *u* paramétrica.

</dd> <dt>

*sknot* 
</dt> <dd>

Una matriz de valores de *sknot de \_ recuento* de nondecreasing en la dirección *u* paramétrica.

</dd> <dt>

*recuento de tknot \_* 
</dt> <dd>

Número de nudos en la dirección de *v* paramétrica.

</dd> <dt>

*tknot* 
</dt> <dd>

Una matriz de valores de *tknot de \_ recuento* de nondecreasing en la dirección *v* paramétrica.

</dd> <dt>

*\_intervalo s* 
</dt> <dd>

Desplazamiento (como número de valores únicos de precisionfloating) entre los puntos de control sucesivos de la dirección *u* paramétrica de *ctlarray*.

</dd> <dt>

*\_intervalo t* 
</dt> <dd>

Desplazamiento (en valores únicos de punto precisionfloating) entre los puntos de control sucesivos de la dirección *v* paramétrica en *ctlarray*.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Una matriz que contiene los puntos de control para la superficie de NURBS. Los desplazamientos entre los puntos de control sucesivos de las direcciones de *u* y *v* paramétricas se proporcionan mediante el *\_ STRIDE* y el *\_ paso t*.

</dd> <dt>

*sorder* 
</dt> <dd>

El orden de la superficie NURBS en la dirección *u* paramétrica. El orden es uno más que el grado; por lo tanto, una superficie cúbica en *u* tiene un orden *u* de 4.

</dd> <dt>

*torder* 
</dt> <dd>

El orden de la superficie NURBS en la dirección *v* paramétrica. El orden es uno más que el grado; por lo tanto, una superficie cúbica en *v* tiene un orden *v* de 4.

</dd> <dt>

*type* 
</dt> <dd>

Tipo de la superficie. El parámetro de *tipo* puede ser cualquiera de los tipos de evaluador bidimensionales válidos (como GL \_ MAP2 ( \_ Vertex \_ 3 o GL \_ MAP2 ( \_ color \_ 4).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use **gluNurbsSurface** en una definición de superficie de NURBS para describir la forma de una superficie NURBS (antes de cualquier recorte). Para marcar el inicio de una definición de superficie de NURBS, utilice la función [**gluBeginSurface**](glubeginsurface.md) . Para marcar el final de una definición de superficie de NURBS, utilice la función [**gluEndSurface**](gluendsurface.md) . Llame a **gluNurbsSurface** solo en una definición de Surface de NURBS.

Las coordenadas de posición, textura y color se asocian con una superficie presentando cada una de ellas como un **gluNurbsSurface** independiente entre un par de gluEndSurface de **gluBeginSurface** /  . Dentro de un solo par de gluEndSurface de **gluBeginSurface** /  , solo puede hacer una llamada a **gluNurbsSurface** para los datos de color, posición y textura. Realice exactamente una llamada para describir la posición de la superficie (un *tipo* de GL \_ MAP2 ( \_ Vertex \_ 3 o GL \_ MAP2 ( \_ Vertex \_ 4).

Puede recortar una superficie NURBS mediante las funciones [**gluNurbsCurve**](glunurbscurve.md) y [**gluPwlCurve**](glupwlcurve.md) entre las llamadas a [**gluBeginTrim**](glubegintrim.md) y [**gluEndTrim**](gluendtrim.md).

Un **gluNurbsSurface** con *sknotr \_* nudos en los nudos de la dirección *u* y *tknot \_ Count* en la dirección *v* con los pedidos *sorder* y *torder* debe tener (*sknot \_ Count*  - *sorder*) multipied por (*tknot \_ Count*  - *torder*) puntos de control.

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

 

 





