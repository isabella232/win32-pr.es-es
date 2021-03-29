---
title: función gluEndCurve (GLU. h)
description: Las funciones gluBeginCurve y gluEndCurve delimitan una definición de curva B-spline racional (NURBS) no uniforme. | función gluEndCurve (GLU. h)
ms.assetid: b00ec687-6127-4585-b7b7-06e8dca78cfc
keywords:
- gluEndCurve (función) OpenGL
topic_type:
- apiref
api_name:
- gluEndCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49f6c0c08bf31135ca82e87d2093ef3b57197955
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678727"
---
# <a name="gluendcurve-function"></a>gluEndCurve función)

Las funciones [**gluBeginCurve**](glubegincurve.md) y **gluEndCurve** delimitan una definición de curva B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)) no uniforme.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluEndCurve(
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

Use [**gluBeginCurve**](glubegincurve.md) para marcar el inicio de una definición de curva NURBS. Después de llamar a **gluBeginCurve**, realice una o varias llamadas a [**gluNurbsCurve**](glunurbscurve.md) para definir los atributos de la curva. Exactamente una de las llamadas a **gluNurbsCurve** debe tener un tipo de curva de GL \_ MAP1 \_ Vertex \_ 3 o GL \_ MAP1 \_ Vertex \_ 4. Para marcar el final de la definición de curva NURBS, llame a **gluEndCurve**.

Los evaluadores de OpenGL se utilizan para representar la curva NURBS como una serie de segmentos de línea. El estado del evaluador se conserva durante la representación con [**glPushAttrib**](glpushattrib.md) (el bit de evaluación de GL \_ \_ ) y [**glPopAttrib**](glpopattrib.md). Para obtener información sobre exactamente el estado que estas llamadas conservan, vea **glPushAttrib**.

## <a name="examples"></a>Ejemplos

Las siguientes funciones representan una curva NURBS con texturas con normalidad; las coordenadas de textura y las normales también se especifican como curvas NURBS:

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
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

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> </dl>

 

 





