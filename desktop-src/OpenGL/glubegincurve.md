---
title: Función gluBeginCurve (Glu.h)
description: Las funciones gluBeginCurve y gluEndCurve delimitan una definición de curva de spline B no uniforme lógica (SPLINEBS). | Función gluBeginCurve (Glu.h)
ms.assetid: f7f2e765-1a07-4faa-940c-9cb957dd54d4
keywords:
- Función gluBeginCurve OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169229"
---
# <a name="glubegincurve-function"></a>Función gluBeginCurve

Las **funciones gluBeginCurve** y [**gluEndCurve**](gluendcurve.md) delimitan una definición de curva B-Spline racionalizada no uniforme [(SPLINEBS).](using-nurbs-curves-and-surfaces.md)

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

El objeto RGBBS (creado [**con gluNewNurbsRenderer).**](glunewnurbsrenderer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use **gluBeginCurve para** marcar el principio de una definición de curva DE ASEBS. Después de **llamar a gluBeginCurve,** realice una o varias llamadas a [**gluNurbsCurve**](glunurbscurve.md) para definir los atributos de la curva. Exactamente una de las llamadas a **gluNurbsCurve** debe tener un tipo de curva de GL \_ MAP1 VERTEX 3 o GL \_ \_ \_ MAP1 \_ VERTEX \_ 4. Para marcar el final de la definición de curva DE ASEBS, llame [**a gluEndCurve**](gluendcurve.md).

Los evaluadores de OpenGL se usan para representar la curva DE ASBS como una serie de segmentos de línea. El estado del evaluador se conserva durante la representación [**con glPushAttrib**](glpushattrib.md) (GL \_ EVAL \_ BIT) y [**glPopAttrib**](glpopattrib.md). Para obtener información sobre exactamente qué estado conservan estas llamadas, **vea glPushAttrib**.

## <a name="examples"></a>Ejemplos

Las funciones siguientes representan una curva TEXTUREBS con textura con normales; Las coordenadas de textura y las normales también se especifican como curvas DE LANBS:

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

 

 





