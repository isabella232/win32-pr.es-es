---
title: Función gluTessBeginContour (Glu.h)
description: Las funciones gluTessBeginContour y gluTessEndContour delimitan una descripción de contorno. | Función gluTessBeginContour (Glu.h)
ms.assetid: 4008ce9c-86e7-4b24-9bda-5915f469596a
keywords:
- Función GluTessBeginContour OpenGL
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
ms.openlocfilehash: 2edc46eb3aa1be6b37c9276bcfd1c2b951162722689b0d0affc358a71119736f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937476"
---
# <a name="glutessbegincontour-function"></a>Función gluTessBeginContour

Las **funciones gluTessBeginContour** y [**gluTessEndContour**](glutessendcontour.md) delimitan una descripción de contorno.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluTessBeginContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tess* 
</dt> <dd>

Objeto de teselación (creado [**con gluNewTess).**](glunewtess.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Las **funciones gluTessBeginContour** y [**gluTessEndPolygon**](glutessendpolygon.md) delimitan la definición de un contorno de polígono. Dentro de cada par **gluTessBeginContour** / **gluTessEndPolygon,** puede haber cero o más llamadas a [**gluTessVertex.**](glutessvertex.md) Los vértices especifican un contorno cerrado (el último vértice de cada contorno se vincula automáticamente al primero). Solo puede llamar **a gluTessBeginContour** entre [**gluTessBeginPolygon**](glutessbeginpolygon.md) y **gluTessEndPolygon.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 





