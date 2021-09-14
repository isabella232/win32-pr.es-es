---
title: Función gluEndTrim (Glu.h)
description: Las funciones gluBeginTrim y gluEndTrim delimitan una definición de bucle de recorte B-Spline no uniforme de rational (SPLINEBS). | Función gluEndTrim (Glu.h)
ms.assetid: e85cc60b-4492-441d-b778-31a3d52b398a
keywords:
- Función gluEndTrim OpenGL
topic_type:
- apiref
api_name:
- gluEndTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4105cc911105f0444ba17c6b57a3deb048bc96d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071474"
---
# <a name="gluendtrim-function"></a>función gluEndTrim

Las [**funciones gluBeginTrim**](glubegintrim.md) y **gluEndTrim** delimitan una definición de bucle de recorte B-Spline racionalizada no uniforme [(SPLINEBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluEndTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nobj* 
</dt> <dd>

El objeto RGBBS (creado [**con gluNewNurbsRenderer).**](glunewnurbsrenderer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use [**gluBeginTrim para**](glubegintrim.md) marcar el principio de un bucle de recorte y **gluEndTrim** para marcar el final de un bucle de recorte. Un bucle de recorte es un conjunto de segmentos de curva orientados (formando una curva cerrada) que definen los límites de una superficie DE LABS. Estos bucles de recorte se incluyen en la definición de una superficie DE ASEBS, entre llamadas a [**gluBeginSurface**](glubeginsurface.md) y [**gluEndSurface.**](gluendsurface.md)

La definición de una superficie DE LABS puede contener muchos bucles de recorte. Por ejemplo, si escribe una definición para una superficie DE TRIMBS similar a un rectángulo con un hueco recortado, la definición contendrá dos bucles de recorte. Un bucle definiría el borde exterior del rectángulo; el otro definiría el hueco de salida despedazado. Las definiciones de cada uno de estos bucles de recorte estarían entre corchetes mediante un par [**gluBeginTrim**](glubegintrim.md)  /  **gluEndTrim.**

La definición de un único bucle de recorte cerrado puede constar de varios segmentos de curva, cada uno descrito como una serie de segmentos de línea que forman una curva lineal (vea [**gluPwlCurve),**](glupwlcurve.md)como una única curva DE LANBS (vea [**gluNurbsCurve)**](glunurbscurve.md)o como una combinación de ambos en cualquier orden. Las únicas llamadas de biblioteca que pueden aparecer en una definición de bucle de recorte (entre las llamadas a [**gluBeginTrim**](glubegintrim.md) y **gluEndTrim)** son **gluPwlCurve** y **gluNurbsCurve.**

El área mostrada de la superficie de LABS es la región del dominio a la izquierda de la curva de recorte a medida que aumenta el parámetro de curva. Por lo tanto, la región retenida de la superficie de LABS está dentro de un bucle de recorte en sentido contrario a las agujas del reloj y fuera de un bucle de recorte en el sentido de las agujas del reloj. Para el rectángulo mencionado anteriormente, el bucle de recorte para el borde exterior del rectángulo se ejecuta en sentido contrario a las agujas del reloj, mientras que el bucle de recorte para el hueco recortado se ejecuta en el sentido de las agujas del reloj.

Si usa más de una curva para definir un único bucle de recorte, los segmentos de curva deben formar un bucle cerrado (es decir, el punto de conexión de cada curva debe ser el punto inicial de la curva siguiente y el punto de conexión de la curva final debe ser el punto inicial de la primera curva). Si los puntos de conexión de la curva están lo suficientemente cerca juntos, pero no exactamente coincidentes, se verán obligados a coincidir. Si los puntos de conexión no están lo suficientemente cerca, se produce un error (vea [*gluNurbsCallback*](glunurbs.md)).

Si una definición de bucle de recorte contiene varias curvas, la dirección de las curvas debe ser coherente (es decir, el interior debe estar a la izquierda de todas las curvas). Puede usar bucles de recorte anidados siempre que las orientaciones de curva se alterne correctamente. Las curvas de recorte no pueden formar intersección entre sí ni pueden formar una intersección entre sí (o resultados de un error).

Si no se proporciona ninguna información de recorte para una superficie DE TRIMBS, se dibuja toda la superficie.

## <a name="examples"></a>Ejemplos

Este fragmento de código define un bucle de recorte que consta de una curva lineal por partes y dos curvas DE LANBS:

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
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
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

 

 





