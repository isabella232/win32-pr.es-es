---
title: función gluTessVertex (GLU. h)
description: La función gluTessVertex especifica un vértice en un polígono.
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- gluTessVertex (función) OpenGL
topic_type:
- apiref
api_name:
- gluTessVertex
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546bbad2be1205f62c7889fbb18f23d5b0e38b8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535242"
---
# <a name="glutessvertex-function"></a>gluTessVertex función)

La función **gluTessVertex** especifica un vértice en un polígono.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluTessVertex(
   GLUtesselator *tess,
   GLdouble      coords[3],
   void          *data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tess* 
</dt> <dd>

Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*coords* 
</dt> <dd>

Ubicación del vértice.

</dd> <dt>

*data* 
</dt> <dd>

Un puntero devuelto al programa con la devolución de llamada del vértice (tal y como se especifica en [*gluTessCallback*](glutess.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluTessVertex** describe un vértice de un polígono que el usuario está definiendo. Las llamadas sucesivas a **gluTessVertex** describen un contorno cerrado. Por ejemplo, para describir un cuadrangular, llame a **gluTessVertex** cuatro veces. Solo se puede llamar a **gluTessVertex** entre [**gluTessBeginContour**](glutessbegincontour.md) y [**gluTessEndContour**](glutessendcontour.md).

Normalmente, el parámetro *Data* apunta a una estructura que contiene la ubicación del vértice, así como a otros atributos por vértice como color y normal. Este puntero se devuelve al programa a través de la devolución de llamada del vértice de GLU después de la \_ teselación (vea [*gluTessCallback*](glutess.md)).

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

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





