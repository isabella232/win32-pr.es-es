---
title: Función gluBeginTrim (Glu.h)
description: Las funciones gluBeginTrim y gluEndTrim delimitan una definición de bucle de recorte B-Spline racionalizado no uniforme (TRIMBS). | Función gluBeginTrim (Glu.h)
ms.assetid: 636402d0-8f6d-4ad8-84c6-66364025d788
keywords:
- Función gluBeginTrim OpenGL
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
ms.openlocfilehash: bebf103a2476aa856b55319e0eca42b8708da169fcedb34e48362062689727ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937888"
---
# <a name="glubegintrim-function"></a>Función gluBeginTrim

Las **funciones gluBeginTrim** y [**gluEndTrim**](gluendtrim.md) delimitan una definición de bucle de recorte B-Spline no uniforme racionalizada [(SPLINEBS).](using-nurbs-curves-and-surfaces.md)

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

El objeto RGBBS (creado [**con gluNewNurbsRenderer).**](glunewnurbsrenderer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Use **gluBeginTrim para** marcar el principio de un bucle de recorte y **gluEndTrim** para marcar el final de un bucle de recorte. Un bucle de recorte es un conjunto de segmentos de curva orientados (que forman una curva cerrada) que definen los límites de una superficie DE LA BASE DE DATOS DE OBJETOS . Estos bucles de recorte se incluyen en la definición de una superficie DE TRIMBS, entre llamadas a [**gluBeginSurface**](glubeginsurface.md) y [**gluEndSurface.**](gluendsurface.md)

La definición de una superficie DE TRIMBS puede contener muchos bucles de recorte. Por ejemplo, si escribe una definición para una superficie DE TRIMBS similar a un rectángulo con un hueco recortado, la definición contendrá dos bucles de recorte. Un bucle definiría el borde exterior del rectángulo; el otro definiría el hueco de salida. Las definiciones de cada uno de estos bucles de recorte estarían entre corchetes mediante un par **gluBeginTrim**  /  **gluEndTrim.**

La definición de un único bucle de recorte cerrado puede constar de varios segmentos de curva, cada uno de los que se describe como una serie de segmentos de línea que forman una curva lineal (vea [**gluPwlCurve),**](glupwlcurve.md)como una única curva DE TRIMBS (vea [**gluNurbsCurve)**](glunurbscurve.md)o como una combinación de ambos en cualquier orden. Las únicas llamadas de biblioteca que pueden aparecer en una definición de bucle de recorte (entre las llamadas a **gluBeginTrim** y **gluEndTrim)** son **gluPwlCurve** y **gluNurbsCurve.**

El área mostrada de la superficie de TRIMBS es la región del dominio a la izquierda de la curva de recorte a medida que aumenta el parámetro de curva. Por lo tanto, la región retenida de la superficie de LABS está dentro de un bucle de recorte en sentido contrario a las agujas del reloj y fuera de un bucle de recorte en el sentido de las agujas del reloj. Para el rectángulo mencionado anteriormente, el bucle de recorte del borde exterior del rectángulo se ejecuta en sentido contrario a las agujas del reloj, mientras que el bucle de recorte para el hueco recortado se ejecuta en el sentido de las agujas del reloj.

Si usa más de una curva para definir un único bucle de recorte, los segmentos de curva deben formar un bucle cerrado (es decir, el punto de conexión de cada curva debe ser el punto inicial de la siguiente curva y el punto de conexión de la curva final debe ser el punto inicial de la primera curva). Si los puntos de conexión de la curva están suficientemente cerca, pero no coinciden exactamente, se verán obligados a coincidir. Si los puntos de conexión no están lo suficientemente cerca, se produce un error (vea [*gluNurbsCallback*](glunurbs.md)).

Si una definición de bucle de recorte contiene varias curvas, la dirección de las curvas debe ser coherente (es decir, el interior debe estar a la izquierda de todas las curvas). Puede usar bucles de recorte anidados siempre que las orientaciones de curva se alterne correctamente. Las curvas de recorte no pueden formar una intersección entre sí, ni pueden formar una intersección entre sí (o resultados de un error).

Si no se proporciona información de recorte para una superficie DE TRIMBS, se dibuja toda la superficie.

## <a name="examples"></a>Ejemplos

Este fragmento de código define un bucle de recorte que consta de una curva lineal por partes y dos curvas DE COLOR DE ÁREA:

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

 

 





