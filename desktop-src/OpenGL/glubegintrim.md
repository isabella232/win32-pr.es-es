---
title: función gluBeginTrim (GLU. h)
description: Las funciones gluBeginTrim y gluEndTrim delimitan una definición de bucle de recorte B-spline racional (NURBS) no uniforme. | función gluBeginTrim (GLU. h)
ms.assetid: 636402d0-8f6d-4ad8-84c6-66364025d788
keywords:
- gluBeginTrim (función) OpenGL
topic_type:
- apiref
api_name:
- gluBeginTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84cbe5c1cd0cc68ee892d42fc60db05b6ae2bea6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670131"
---
# <a name="glubegintrim-function"></a>gluBeginTrim función)

Las funciones **gluBeginTrim** y [**gluEndTrim**](gluendtrim.md) delimitan una definición de bucle de recorte B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)) no uniforme.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluBeginTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nobj* 
</dt> <dd>

El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use **gluBeginTrim** para marcar el principio de un bucle de recorte y **gluEndTrim** para marcar el final de un bucle de recorte. Un bucle de recorte es un conjunto de segmentos de curva orientado (formando una curva cerrada) que define los límites de una superficie NURBS. Estos bucles de recorte se incluyen en la definición de una superficie NURBS, entre las llamadas a [**gluBeginSurface**](glubeginsurface.md) y [**gluEndSurface**](gluendsurface.md).

La definición de una superficie NURBS puede contener muchos bucles de recorte. Por ejemplo, si escribe una definición para una superficie NURBS similar a un rectángulo con un orificio perforado, la definición contendría dos bucles de recorte. Un bucle definiría el borde exterior del rectángulo; la otra definiría el orificio perforado. Las definiciones de cada uno de estos bucles de recorte estarán entre corchetes por un par de gluEndTrim de **gluBeginTrim**  /   .

La definición de un solo bucle de recorte cerrado puede estar formada por varios segmentos de curva, cada uno de los cuales se describe como una serie de segmentos de línea que forman una curva lineal (vea [**gluPwlCurve**](glupwlcurve.md)), como una sola curva de NURBS (vea [**gluNurbsCurve**](glunurbscurve.md)) o como una combinación de ambos en cualquier orden. Las únicas llamadas de biblioteca que pueden aparecer en una definición de bucle de recorte (entre las llamadas a **gluBeginTrim** y **GluEndTrim**) son **gluPwlCurve** y **gluNurbsCurve**.

El área mostrada de la superficie de NURBS es la región del dominio a la izquierda de la curva de recorte a medida que aumenta el parámetro de curva. Por lo tanto, la región retenida de la superficie de NURBS está dentro de un bucle de recorte en sentido contrario a las agujas del reloj y fuera de un bucle de recorte. En el caso del rectángulo mencionado anteriormente, el bucle de recorte del borde exterior del rectángulo se ejecuta en sentido contrario a las agujas del reloj, mientras que el bucle de recorte del orificio perforado se ejecuta en el sentido de las agujas del reloj.

Si usa más de una curva para definir un bucle de recorte único, los segmentos de curva deben formar un bucle cerrado (es decir, el extremo de cada curva debe ser el punto inicial de la curva siguiente y el extremo de la curva final debe ser el punto inicial de la primera curva). Si los puntos de conexión de la curva están suficientemente cercanos, pero no exactamente el coincidente, se verán obligados a coincidir. Si los puntos de conexión no están suficientemente cerca, se producirá un error (vea [*gluNurbsCallback*](glunurbs.md)).

Si una definición de bucle de recorte contiene varias curvas, la dirección de las curvas debe ser coherente (es decir, el interior debe estar a la izquierda de todas las curvas). Puede utilizar bucles de recorte anidados siempre que las orientaciones de curva alternen correctamente. Las curvas de recorte no pueden intersectarse por sí mismas ni pueden intersectar entre sí (o un resultado de error).

Si no se proporciona información de recorte para una superficie NURBS, se dibuja toda la superficie.

## <a name="examples"></a>Ejemplos

Este fragmento de código define un bucle de recorte que consta de una curva lineal a trozos y dos curvas NURBS:

``` syntax
gluBeginTrim(nobj); 
    gluPwlCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_3);  
gluEndTrim(nobj);
```

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

[**gluEndSurface**](gluendsurface.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





