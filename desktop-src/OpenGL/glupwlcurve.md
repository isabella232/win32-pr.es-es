---
title: función gluPwlCurve (GLU. h)
description: La función gluPwlCurve describe una curva de recorte B-spline racional no uniforme (NURBS) a trozos lineal.
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- gluPwlCurve (función) OpenGL
topic_type:
- apiref
api_name:
- gluPwlCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15c532659811c7e499369e7798c4b1ceaf842bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666041"
---
# <a name="glupwlcurve-function"></a>gluPwlCurve función)

La función **gluPwlCurve** describe una curva de recorte B-spline racional no uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)) a trozos lineal.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluPwlCurve(
   GLUnurbs *nobj,
   GLint    count,
   GLfloat  *array,
   GLint    stride,
   GLenum   type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nobj* 
</dt> <dd>

El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*count* 
</dt> <dd>

Número de puntos de la curva.

</dd> <dt>

*array* 
</dt> <dd>

Una matriz que contiene los puntos de curva.

</dd> <dt>

*STRI* 
</dt> <dd>

Desplazamiento (un número de valores de punto flotante de precisión sencilla) entre los puntos de la curva.

</dd> <dt>

*type* 
</dt> <dd>

Tipo de curva. Debe ser GLU \_ MAP1 \_ Trim \_ 2 o Glu \_ MAP1 \_ Trim \_ 3.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluPwlCurve** describe una curva de recorte lineal a trozos para una superficie NURBS. Una curva lineal a trozos consta de una lista de coordenadas de puntos en el espacio de parámetros para que se recorte la superficie NURBS. Estos puntos están conectados con segmentos de línea para formar una curva. Si la curva es una aproximación a una curva real, los puntos deben ser lo suficientemente cercanos para que el trazado resultante aparezca curvado en la resolución usada en la aplicación.

Si *Type* es Glu \_ MAP1 \_ Trim \_ 2, describe una curva en el espacio de parámetros bidimensional (*u* y *v*). Si es GLU \_ MAP1 \_ Trim \_ 3, describe una curva en el espacio de parámetros homogéneos bidimensionales (*u*, *v* y *w*). Para obtener más información sobre las curvas de recorte, vea [**gluBeginTrim**](glubegintrim.md).

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

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> </dl>

 

 





