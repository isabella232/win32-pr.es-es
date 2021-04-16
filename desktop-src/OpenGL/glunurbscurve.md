---
title: función gluNurbsCurve (GLU. h)
description: La función gluNurbsCurve define la forma de una curva no uniforme B-spline (NURBS).
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- gluNurbsCurve (función) OpenGL
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676689"
---
# <a name="glunurbscurve-function"></a>gluNurbsCurve función)

La función **gluNurbsCurve** define la forma de una curva no uniforme B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)).

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

El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*nknots* 
</dt> <dd>

Número de nudos en el *nodo*. El parámetro *nknots* es igual al número de puntos de control más el orden.

</dd> <dt>

*decremento* 
</dt> <dd>

Matriz de valores de nudos de *nknots* nondecreasing.

</dd> <dt>

*STRI* 
</dt> <dd>

Desplazamiento (como un número de valores de punto flotante de precisión sencilla) entre los puntos de control de curva sucesivos.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Puntero a una matriz de puntos de control. Las coordenadas deben coincidir con el *tipo*.

</dd> <dt>

*order* 
</dt> <dd>

El orden de la curva de NURBS. El parámetro *Order* es igual a degree + 1; por lo tanto, una curva cúbica tiene un orden de 4.

</dd> <dt>

*type* 
</dt> <dd>

Tipo de la curva. Si esta curva se define dentro de un par [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md) , el tipo puede ser cualquiera de los tipos de evaluador unidimensional válidos (como GL \_ MAP1 \_ Vertex \_ 3 o GL \_ MAP1 \_ color \_ 4). Entre un par de [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim**](gluendtrim.md) , los únicos tipos válidos son Glu \_ MAP1 \_ Trim \_ 2 y Glu \_ MAP1 \_ Trim \_ 3.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando **gluNurbsCurve** aparece entre un  / par de **gluEndCurve** gluBeginCurve, describe una curva que se va a representar. Para asociar coordenadas posicional, de textura y de color, presenta cada una de ellas como un **gluNurbsCurve** independiente entre un par de gluEndCurve de **gluBeginCurve** /  . No realice más de una llamada a **gluNurbsCurve** para los datos de color, posición y textura dentro de un solo par de  / **gluEndCurve** gluBeginCurve. Realice exactamente una llamada para describir la posición de la curva (un *tipo* de GL \_ MAP1 \_ Vertex \_ 3 o GL \_ MAP1 \_ Vertex \_ 4).

Cuando **gluNurbsCurve** aparece entre un [](glubegintrim.md) / par de [**gluEndTrim**](gluendtrim.md) gluBeginTrim, describe una curva de recorte en una superficie NURBS. Si *Type* es Glu \_ MAP1 \_ Trim \_ 2, describe una curva en el espacio de parámetros bidimensional (*u* y *v*). Si es GLU \_ MAP1 \_ Trim \_ 3, describe una curva en el espacio de parámetros homogéneos bidimensionales (*u*, *v* y *w*). Para obtener más información sobre las curvas de recorte, vea **gluBeginTrim**.

## <a name="examples"></a>Ejemplos

Las siguientes funciones representan una curva NURBS con texturas con normalidad:

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
| Encabezado<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
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

 

 





