---
title: Función gluTessBeginPolygon (Glu.h)
description: Las funciones gluTessBeginPolygon y gluTessEndPolygon delimitan una descripción de polígono. | Función gluTessBeginPolygon (Glu.h)
ms.assetid: 3a04363a-c492-4fa5-b312-f2fa2a805782
keywords:
- Función GluTessBeginPolygon OpenGL
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
ms.openlocfilehash: 42566cf8a0674086883e6333a67ac2df03329f6a9bd3bb903ef558af3c430b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777395"
---
# <a name="glutessbeginpolygon-function"></a>Función gluTessBeginPolygon

Las **funciones gluTessBeginPolygon** y [**gluTessEndPolygon**](glutessendpolygon.md) delimitan una descripción de polígono.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluTessBeginPolygon(
   GLUtesselator *tess,
   void          *polygon_data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tess* 
</dt> <dd>

Objeto de teselación (creado [**con gluNewTess**](glunewtess.md)).

</dd> <dt>

*datos de \_ polígono* 
</dt> <dd>

Puntero a una estructura de datos de polígono definida por el programador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Las **funciones gluTessBeginPolygon** y [**gluTessEndPolygon**](glutessendpolygon.md) delimitan la definición de un polígono no convexa. Dentro de cada par **gluTessBeginPolygon**  /  **gluTessEndPolygon,** incluya una o varias llamadas a [**gluTessBeginContour.**](glutessbegincontour.md) Dentro de cada contorno, hay cero o más llamadas [**a gluTessVertex.**](glutessvertex.md) Los vértices especifican un contorno cerrado (el último vértice de cada contorno se vincula automáticamente al primero).

El *parámetro \_ de datos* polygon es un puntero a una estructura de datos definida por el programador. Si se especifican las devoluciones de llamada adecuadas (vea [*gluTessCallback),*](glutess.md)este puntero se devuelve a la función o funciones de devolución de llamada, lo que lo hace una manera cómoda de almacenar información por polígono.

Cuando se llama [**a gluTessEndPolygon,**](glutessendpolygon.md)el polígono se tesela y los triángulos resultantes se describen a través de devoluciones de llamada. Para obtener descripciones de las funciones de devolución de llamada, [*vea gluTessCallback*](glutess.md).

## <a name="examples"></a>Ejemplos

A continuación se describe un cuadrángulo con un hueco triangular:

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



| Requisito | Valor |
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

 

 





