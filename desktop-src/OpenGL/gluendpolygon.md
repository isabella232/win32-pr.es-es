---
title: Función gluEndPolygon (Glu.h)
description: Las funciones gluBeginPolygon y gluEndPolygon delimitan una descripción de polígono. | Función gluEndPolygon (Glu.h)
ms.assetid: fdb8cc73-c6c3-4377-aa5b-36a79791e7a9
keywords:
- Función gluEndPolygon OpenGL
topic_type:
- apiref
api_name:
- gluEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf69bfb16f9c83462bbe6b53c86f319b3d09623
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071479"
---
# <a name="gluendpolygon-function"></a>función gluEndPolygon

\[La **función gluEndPolygon** está obsoleta y solo se proporciona por compatibilidad con versiones anteriores. La **función gluEndPolygon** se asigna a **gluTessEndPolygon** seguido de **gluTessEndContour.**\]

Las [**funciones gluBeginPolygon**](glubeginpolygon.md) y **gluEndPolygon** delimitan una descripción de polígono.

## <a name="syntax"></a>Sintaxis


```C++
void gluEndPolygon(
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

Use [**gluBeginPolygon y**](glubeginpolygon.md) **gluEndPolygon** para delimitar la definición de un polígono no convexa.

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

 

 





