---
title: función gluTessBeginContour (GLU. h)
description: Las funciones gluTessBeginContour y gluTessEndContour delimitan una descripción de perfil. | función gluTessBeginContour (GLU. h)
ms.assetid: 4008ce9c-86e7-4b24-9bda-5915f469596a
keywords:
- gluTessBeginContour (función) OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd28efc96c977e5e0483b4f3d87e9ce840b985cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689788"
---
# <a name="glutessbegincontour-function"></a>gluTessBeginContour función)

Las funciones **gluTessBeginContour** y [**gluTessEndContour**](glutessendcontour.md) delimitan una descripción de perfil.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluTessBeginContour(
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

Las funciones **gluTessBeginContour** y [**gluTessEndPolygon**](glutessendpolygon.md) delimitan la definición de un contorno de polígono. Dentro de cada par de gluTessEndPolygon de **gluTessBeginContour** /  , puede haber cero o más llamadas a [**gluTessVertex**](glutessvertex.md). Los vértices especifican un perfil cerrado (el último vértice de cada contorno se vincula automáticamente al primero). Solo puede llamar a **gluTessBeginContour** entre [**gluTessBeginPolygon**](glutessbeginpolygon.md) y **gluTessEndPolygon**.

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

 

 





