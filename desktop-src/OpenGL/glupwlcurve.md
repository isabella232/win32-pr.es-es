---
title: Función gluPwlCurve (Glu.h)
description: La función gluPwlCurve describe una curva de recorte lineal lineal no uniforme de B-Spline lógica (DSLBS).
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- Función GluPwlCurve OpenGL
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
ms.openlocfilehash: 9911619e54247c633d4b3cecc69327f92da6a7f27c3cebf9231ec86ad0f0a20d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061573"
---
# <a name="glupwlcurve-function"></a>Función gluPwlCurve

La **función gluPwlCurve** describe una curva de recorte lineal lineal no uniforme de B-Spline lógica [(SPLINEBS).](using-nurbs-curves-and-surfaces.md)

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

El objeto RGBBS (creado [**con gluNewNurbsRenderer).**](glunewnurbsrenderer.md)

</dd> <dt>

*count* 
</dt> <dd>

Número de puntos de la curva.

</dd> <dt>

*array* 
</dt> <dd>

Matriz que contiene los puntos de curva.

</dd> <dt>

*Paso* 
</dt> <dd>

Desplazamiento (un número de valores de punto flotante de precisión sencilla) entre los puntos de la curva.

</dd> <dt>

*type* 
</dt> <dd>

Tipo de curva. Debe ser GLU \_ MAP1 \_ TRIM \_ 2 o GLU \_ MAP1 \_ TRIM \_ 3.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La **función gluPwlCurve** describe una curva de recorte lineal por fragmentos para una superficie DE ASEBS. Una curva lineal por fragmentos consta de una lista de coordenadas de puntos en el espacio de parámetros para la superficie DE LA BASE DE DATOS QUE se va a recortar. Estos puntos están conectados con segmentos de línea para formar una curva. Si la curva es una aproximación a una curva real, los puntos deben estar lo suficientemente cerca como para que la ruta de acceso resultante aparezca curvada en la resolución utilizada en la aplicación.

Si *type* es GLU MAP1 TRIM 2, describe una curva en un espacio de parámetros \_ \_ \_ bidimensional *(u* y *v).* Si es GLU MAP1 TRIM 3, describe una curva en un espacio de parámetros \_ \_ \_ homogéneo bidimensional *(u,* *v* y *w).* Para obtener más información sobre el recorte de curvas, [**vea gluBeginTrim**](glubegintrim.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> </dl>

 

 





