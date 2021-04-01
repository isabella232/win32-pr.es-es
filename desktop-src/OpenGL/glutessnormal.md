---
title: función gluTessNormal (GLU. h)
description: La función gluTessNormal especifica una normal para un polígono.
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- gluTessNormal (función) OpenGL
topic_type:
- apiref
api_name:
- gluTessNormal
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af04ab2364fafcea709ca36cab2f10a8bea1a96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996999"
---
# <a name="glutessnormal-function"></a>gluTessNormal función)

La función **gluTessNormal** especifica una normal para un polígono.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluTessNormal(
   GLUtesselator *tess,
   GLdouble      x,
   GLdouble      y,
   GLdouble      z
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tess* 
</dt> <dd>

Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*x* 
</dt> <dd>

Componente de la coordenada x de un normal.

</dd> <dt>

*y* 
</dt> <dd>

Componente de la coordenada y de un normal.

</dd> <dt>

*z* 
</dt> <dd>

Componente de la coordenada z de un normal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluTessNormal** describe una normal para un polígono que defina. Todos los datos de entrada se proyectan en un plano perpendicular a uno de los tres ejes de coordenadas antes de la teselación, y todos los triángulos de salida se orientan en sentido contrario a las agujas del reloj con respecto al normal. (Para obtener orientación en el sentido de las agujas del reloj, invierta el signo del normal proporcionado). Por ejemplo, si sabe que todos los polígonos se encuentran en el plano x-y, llame a **gluTessNormal**(tess, 0,0, 0,0, 1,0) antes de representar los polígonos.

Si la normal proporcionada es (0,0, 0,0, 0,0) (el valor predeterminado), la normal se determina de la manera siguiente:

1.  La dirección del normal, hasta su signo, se encuentra al ajustar un plano a los vértices, sin tener en cuenta cómo se conectan los vértices. Se espera que los datos de entrada se encuentren aproximadamente en el plano; de lo contrario, la proyección perpendicular a uno de los tres ejes de coordenadas puede cambiar la geometría de forma sustancial.
2.  El signo de la normal se elige de modo que la suma de las áreas con signo de todos los contornos de entrada no sea negativa (cuando un contorno en sentido contrario tenga un área positiva).

La normal proporcionada se conserva hasta que otra llamada a **gluTessNormal** lo cambia.

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

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> </dl>

 

 





