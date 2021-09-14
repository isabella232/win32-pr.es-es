---
title: Función gluBeginPolygon (Glu.h)
description: Las funciones gluBeginPolygon y gluEndPolygon delimitan una descripción de polígono. | Función gluBeginPolygon (Glu.h)
ms.assetid: e4da731c-2082-4dbc-ae3a-8d6b30d50253
keywords:
- Función gluBeginPolygon OpenGL
topic_type:
- apiref
api_name:
- gluBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60204e7d937b4686f3757b520c820886e168529e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169222"
---
# <a name="glubeginpolygon-function"></a>función gluBeginPolygon

\[La **función gluBeginPolygon** está obsoleta y solo se proporciona por compatibilidad con versiones anteriores. La **función gluBeginPolygon** se asigna a [**gluTessBeginPolygon**](glutessbeginpolygon.md) seguido de [**gluTessBeginContour.**](glutessbegincontour.md)\]

Las **funciones gluBeginPolygon** y [**gluEndPolygon**](gluendpolygon.md) delimitan una descripción de polígono.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluBeginPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tess* 
</dt> <dd>

Objeto de teselación (creado [**con gluNewTess**](glunewtess.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use **gluBeginPolygon y** **gluEndPolygon** para delimitar la definición de un polígono no convexa.

1.  Llame **a gluBeginPolygon.**
2.  Defina los contornos del polígono mediante una llamada [**a gluTessVertex**](glutessvertex.md) para cada vértice y [**gluNextContour**](glunextcontour.md) para iniciar cada nuevo contorno.
3.  Llame **a gluEndPolygon** para indicar el final de la definición.

    Una vez que se llama a **gluEndPolygon,** el polígono se tesela y los triángulos resultantes se describen mediante devoluciones de llamada. Para obtener descripciones de las funciones de devolución de llamada, [*vea gluTessCallback*](glutess.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se describe un cuadrángulo con un hueco triangular:

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4); 
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7); 
gluEndPolygon(tess);
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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluNextContour**](glunextcontour.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





