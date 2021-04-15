---
title: función gluBeginSurface (GLU. h)
description: Las funciones gluBeginSurface y gluEndSurface delimitan una definición de superficie de la spline B-spline racional (NURBS) no uniforme. | función gluBeginSurface (GLU. h)
ms.assetid: 7189f05e-0c4d-4f82-8a82-a51fcc51b202
keywords:
- gluBeginSurface (función) OpenGL
topic_type:
- apiref
api_name:
- gluBeginSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd09030290f78fac987a52cddd977a502dda06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689742"
---
# <a name="glubeginsurface-function"></a>gluBeginSurface función)

Las funciones **gluBeginSurface** y [**gluEndSurface**](gluendsurface.md) delimitan una definición de superficie de la spline B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)) no uniforme.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluBeginSurface(
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

Las funciones **gluBeginSurface** y **gluEndSurface** marcan el principio y el final de las definiciones de la superficie de NURBS, que se definen con llamadas a **gluNurbsSurface**.

1.  Llame a **gluBeginSurface** para marcar el inicio de una definición de superficie de NURBS.
2.  Realice una o varias llamadas a **gluNurbsSurface** para definir los atributos de la superficie.

    Exactamente una de estas llamadas a **gluNurbsSurface** debe tener un tipo de superficie de GL \_ MAP2 ( \_ Vertex \_ 3 o GL \_ MAP2 ( \_ Vertex \_ 4.

3.  Para marcar el final de la definición de la superficie de NURBS, llame a **gluEndSurface**.

Las funciones [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md)y [**gluEndTrim**](gluendtrim.md) admiten el recorte de superficies NURBS.

Utilice los evaluadores de OpenGL para representar la superficie de NURBS como un conjunto de polígonos. Conservar el estado del evaluador durante la representación con [**glPushAttrib**](glpushattrib.md)(el bit de evaluación de GL \_ \_ ) y [**glPopAttrib**](glpopattrib.md).

## <a name="examples"></a>Ejemplos

Las siguientes funciones representan una superficie NURBS con texturas con normalidad; las coordenadas de textura y las normales también se describen como superficies NURBS:

``` syntax
gluBeginSurface(nobj); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_TEXTURE_COORD_2); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_NORMAL); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_VERTEX_4); 
gluEndSurface(nobj);
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

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluNurbsSurface**](glunurbssurface.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





