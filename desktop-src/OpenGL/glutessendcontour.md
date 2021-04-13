---
title: función gluTessEndContour (GLU. h)
description: Las funciones gluTessBeginContour y gluTessEndContour delimitan una descripción de perfil. | función gluTessEndContour (GLU. h)
ms.assetid: 115db079-cbcb-48e1-8bab-0eb4814afb82
keywords:
- gluTessEndContour (función) OpenGL
topic_type:
- apiref
api_name:
- gluTessEndContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac53f3920476489a1453bb6b5dc1e01d650d4fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362107"
---
# <a name="glutessendcontour-function"></a>gluTessEndContour función)

Las funciones [**gluTessBeginContour**](glutessbegincontour.md) y **gluTessEndContour** delimitan una descripción de perfil.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluTessEndContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tess* 
</dt> <dd>

Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las funciones [**gluTessBeginContour**](glutessbegincontour.md) y **gluTessEndContour** delimitan la definición de un contorno de polígono. Dentro de cada par de gluTessEndContour de **gluTessBeginContour** /  , puede haber cero o más llamadas a [**gluTessVertex**](glutessvertex.md). Los vértices especifican un perfil cerrado (el último vértice de cada contorno se vincula automáticamente al primero). Solo puede llamar a **gluTessBeginContour** entre [**gluTessBeginPolygon**](glutessbeginpolygon.md) y [**gluTessEndPolygon**](glutessendpolygon.md).

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

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





