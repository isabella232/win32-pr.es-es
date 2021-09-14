---
title: Función gluEndCurve (Glu.h)
description: Las funciones gluBeginCurve y gluEndCurve delimitan una definición de curva B-Spline racionalizada no uniforme (DSLBS). | Función gluEndCurve (Glu.h)
ms.assetid: b00ec687-6127-4585-b7b7-06e8dca78cfc
keywords:
- Función gluEndCurve OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071485"
---
# <a name="gluendcurve-function"></a>Función gluEndCurve

Las [**funciones gluBeginCurve**](glubegincurve.md) y **gluEndCurve** delimitan una definición de curva B-Spline racionalizada no uniforme [(SPLINEBS).](using-nurbs-curves-and-surfaces.md)

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

El objeto RGBBS (creado [**con gluNewNurbsRenderer).**](glunewnurbsrenderer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use [**gluBeginCurve para**](glubegincurve.md) marcar el principio de una definición de curva DE DSLBS. Después de **llamar a gluBeginCurve,** realice una o varias llamadas a [**gluNurbsCurve**](glunurbscurve.md) para definir los atributos de la curva. Exactamente una de las llamadas a **gluNurbsCurve** debe tener un tipo de curva de GL \_ MAP1 VERTEX 3 o GL \_ \_ \_ MAP1 \_ VERTEX \_ 4. Para marcar el final de la definición de curva DE ASEBS, llame **a gluEndCurve**.

Los evaluadores OpenGL se usan para representar la curva DE ASEBS como una serie de segmentos de línea. El estado del evaluador se conserva durante la representación [**con glPushAttrib**](glpushattrib.md) (GL \_ EVAL \_ BIT ) y [**glPopAttrib**](glpopattrib.md). Para obtener información sobre exactamente qué estado conservan estas llamadas, **vea glPushAttrib**.

## <a name="examples"></a>Ejemplos

Las funciones siguientes representan una curva TEXTUREBS con textura con normales; Las coordenadas de textura y las normales también se especifican como curvas DE TIPO XYZBS:

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
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
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

 

 





