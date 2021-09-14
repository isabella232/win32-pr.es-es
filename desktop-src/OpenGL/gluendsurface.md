---
title: Función gluEndSurface (Glu.h)
description: Las funciones gluBeginSurface y gluEndSurface delimitan una definición de superficie B-Spline racionalizada no uniforme (DSLBS). | Función gluEndSurface (Glu.h)
ms.assetid: beaa0340-c67d-4376-bedd-7f73c5c6d742
keywords:
- Función gluEndSurface OpenGL
topic_type:
- apiref
api_name:
- gluEndSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54631d5c4ef752cffd989f8fa02f8cb512c67da3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071477"
---
# <a name="gluendsurface-function"></a>Función gluEndSurface

Las [**funciones gluBeginSurface**](glubeginsurface.md) y **gluEndSurface** delimitan una definición de superficie B-Spline racionalizada no uniforme [(SPLINEBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluEndSurface(
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

Las [**funciones gluBeginSurface**](glubeginsurface.md) y **gluEndSurface** marcan el principio y el final de las definiciones de la superficie DE GLUBS, que se definen con llamadas a **gluNurbsSurface**.

1.  Llame **a gluBeginSurface para** marcar el principio de una definición de superficie DE LA BASE DE DATOS.
2.  Realice una o varias llamadas a **gluNurbsSurface** para definir los atributos de la superficie.

    Exactamente una de estas llamadas a **gluNurbsSurface** debe tener un tipo de superficie de GL \_ MAP2 VERTEX 3 o GL \_ \_ \_ MAP2 \_ VERTEX \_ 4.

3.  Para marcar el final de la definición de la superficie de LABS, llame **a gluEndSurface**.

Las [**funciones gluBeginTrim,**](glubegintrim.md) [**gluPwlCurve,**](glupwlcurve.md) [**gluNurbsCurve**](glunurbscurve.md)y **gluEndTrim** admiten el recorte de superficies DETRUBS.

Use evaluadores OpenGL para representar la superficie de LABS como un conjunto de polígonos. Conserve el estado del evaluador durante la representación [**con glPushAttrib**](glpushattrib.md) (GL \_ EVAL \_ BIT) y [**glPopAttrib**](glpopattrib.md).

## <a name="examples"></a>Ejemplos

Las funciones siguientes representan una superficie DE COLORYBS con textura con normales; Las coordenadas de textura y las normales también se describen como superficies DE TIPO XYZBS:

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
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
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

 

 





