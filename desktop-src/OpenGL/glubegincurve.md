---
title: función gluBeginCurve (GLU. h)
description: Las funciones gluBeginCurve y gluEndCurve delimitan una definición de curva B-spline racional (NURBS) no uniforme. | función gluBeginCurve (GLU. h)
ms.assetid: f7f2e765-1a07-4faa-940c-9cb957dd54d4
keywords:
- gluBeginCurve (función) OpenGL
topic_type:
- apiref
api_name:
- gluBeginCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4e17bd88cfcb49801450ead865c437843d179b5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689858"
---
# <a name="glubegincurve-function"></a>gluBeginCurve función)

Las funciones **gluBeginCurve** y [**gluEndCurve**](gluendcurve.md) delimitan una definición de curva B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)) no uniforme.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluBeginCurve(
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

Use **gluBeginCurve** para marcar el inicio de una definición de curva NURBS. Después de llamar a **gluBeginCurve**, realice una o varias llamadas a [**gluNurbsCurve**](glunurbscurve.md) para definir los atributos de la curva. Exactamente una de las llamadas a **gluNurbsCurve** debe tener un tipo de curva de GL \_ MAP1 \_ Vertex \_ 3 o GL \_ MAP1 \_ Vertex \_ 4. Para marcar el final de la definición de curva NURBS, llame a [**gluEndCurve**](gluendcurve.md).

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

 

 





