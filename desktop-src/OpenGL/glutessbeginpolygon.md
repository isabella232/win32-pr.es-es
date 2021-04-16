---
title: función gluTessBeginPolygon (GLU. h)
description: Las funciones gluTessBeginPolygon y gluTessEndPolygon delimitan una descripción de polígono. | función gluTessBeginPolygon (GLU. h)
ms.assetid: 3a04363a-c492-4fa5-b312-f2fa2a805782
keywords:
- gluTessBeginPolygon (función) OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34fad4c620890df109449b9a222d3355041ac77f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670185"
---
# <a name="glutessbeginpolygon-function"></a>gluTessBeginPolygon función)

Las funciones **gluTessBeginPolygon** y [**gluTessEndPolygon**](glutessendpolygon.md) delimitan una descripción de polígono.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluTessBeginPolygon(
   GLUtesselator *tess,
   void          *polygon_data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tess* 
</dt> <dd>

Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*datos de polígono \_* 
</dt> <dd>

Puntero a una estructura de datos de polígono definida por el programador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las funciones **gluTessBeginPolygon** y [**gluTessEndPolygon**](glutessendpolygon.md) delimitan la definición de un polígono no convexo. Dentro de cada par de gluTessEndPolygon de **gluTessBeginPolygon**  /   , incluya una o más llamadas a [**gluTessBeginContour**](glutessbegincontour.md). Dentro de cada perfil, hay cero o más llamadas a [**gluTessVertex**](glutessvertex.md). Los vértices especifican un perfil cerrado (el último vértice de cada contorno se vincula automáticamente al primero).

El parámetro de *\_ datos Polygon* es un puntero a una estructura de datos definida por el programador. Si se especifican las devoluciones de llamada adecuadas (vea [*gluTessCallback*](glutess.md)), este puntero se devuelve a la función o funciones de devolución de llamada, lo que lo convierte en una manera cómoda de almacenar la información por polígono.

Cuando se llama a [**gluTessEndPolygon**](glutessendpolygon.md), el polígono es teselando y los triángulos resultantes se describen a través de las devoluciones de llamada. Para obtener descripciones de las funciones de devolución de llamada, vea [*gluTessCallback*](glutess.md).

## <a name="examples"></a>Ejemplos

A continuación se describe un cuadrangular con un orificio triangular:

``` syntax
gluTessBeginPolygon(tobj, NULL); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v1, v1); 
    gluTessVertex(tobj, v2, v2); 
    gluTessVertex(tobj, v3, v3); 
    gluTessVertex(tobj, v4, v4); 
  gluTessEndContour(tobj); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v5, v5); 
    gluTessVertex(tobj, v6, v6); 
    gluTessVertex(tobj, v7, v7); 
  gluTessEndContour(tobj); 
gluTessEndPolygon(tobj);
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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





