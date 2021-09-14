---
title: Función gluNurbsCurve (Glu.h)
description: La función gluNurbsCurve define la forma de una curva B-Spline racionalizada no uniforme (SPLINEBS).
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- Función GluNurbsCurve OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e3d5fe35e994afa4b5d8b91c4244573132c5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244959"
---
# <a name="glunurbscurve-function"></a>Función gluNurbsCurve

La **función gluNurbsCurve** define la forma de una curva B-Spline racionalizada no uniforme [(SPLINEBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluNurbsCurve(
   GLUnurbs *nobj,
   GLint    nknots,
   GLfloat  *knot,
   GLint    stride,
   GLfloat  *ctlarray,
   GLint    order,
   GLenum   type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nobj* 
</dt> <dd>

El objeto RGBBS (creado [**con gluNewNurbsRenderer).**](glunewnurbsrenderer.md)

</dd> <dt>

*ynots* 
</dt> <dd>

El número de reses en *la zona .* El *parámetro nknots* es igual al número de puntos de control más el orden.

</dd> <dt>

*Nudo* 
</dt> <dd>

Una matriz de ninos no disminuye los valores de los valores de los *métodos.*

</dd> <dt>

*Paso* 
</dt> <dd>

Desplazamiento (como un número de valores de punto flotante de precisión sencilla) entre los puntos de control de curva sucesivos.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Puntero a una matriz de puntos de control. Las coordenadas deben coincidir con el *tipo*.

</dd> <dt>

*order* 
</dt> <dd>

El orden de la curva DE ASEBS. El *parámetro order* es igual a degree + 1; por lo tanto, una curva cúbica tiene un orden de 4.

</dd> <dt>

*type* 
</dt> <dd>

Tipo de la curva. Si esta curva se define dentro de un par [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve,**](gluendcurve.md) el tipo puede ser cualquiera de los tipos de evaluadores unidimensionales válidos (como GL \_ MAP1 VERTEX 3 o GL \_ \_ \_ MAP1 COLOR \_ \_ 4). Entre un [**par gluBeginTrim**](glubegintrim.md) / [**gluEndTrim,**](gluendtrim.md) los únicos tipos válidos son GLU \_ MAP1 TRIM 2 y GLU \_ \_ \_ MAP1 TRIM \_ \_ 3.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando **gluNurbsCurve aparece** entre un par **gluBeginCurve** / **gluEndCurve,** describe una curva que se va a representar. Asocie las coordenadas de posición, textura y color mediante la presentación de cada una como un **gluNurbsCurve** independiente entre un par **gluBeginCurve** / **gluEndCurve.** No realice más de una llamada a **gluNurbsCurve** para obtener datos de color, posición y textura dentro de un único par **gluBeginCurve** / **gluEndCurve.** Realice exactamente una llamada para describir la  posición de la curva (un tipo de GL \_ MAP1 VERTEX 3 o GL \_ \_ \_ MAP1 \_ VERTEX \_ 4).

Cuando **gluNurbsCurve** aparece entre un par [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim,**](gluendtrim.md) describe una curva de recorte en una superficie DETRUBS. Si *type* es GLU MAP1 TRIM 2, describe una curva en un espacio de parámetros \_ \_ \_ bidimensional *(u* y *v).* Si es GLU MAP1 TRIM 3, describe una curva en un espacio de parámetros \_ \_ \_ homogéneo bidimensional *(u,* *v* y *w).* Para obtener más información sobre el recorte de curvas, **vea gluBeginTrim**.

## <a name="examples"></a>Ejemplos

Las funciones siguientes representan una curva TEXTUREBS con textura con normales:

``` syntax
gluBeginCurve(nobj); 
    gluNurbsCurve(nobj, ..., GL_MAP1_TEXTURE_COORD_2); 
    gluNurbsCurve(nobj, ..., GL_MAP1_NORMAL); 
    gluNurbsCurve(nobj, ..., GL_MAP1_VERTEX_4);  
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

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluEndCurve**](gluendcurve.md)
</dt> <dt>

[**gluEndTrim**](gluendtrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





