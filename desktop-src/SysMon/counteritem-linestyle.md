---
title: CounterItem.LineStyle, propiedad
description: Recupera o establece el estilo de línea utilizado para representar el valor del contador.
ms.assetid: 5801f0f8-37e5-4b15-a13f-24c71fea550d
keywords:
- Propiedad LineStyle SysMon
- Propiedad LineStyle SysMon , clase CounterItem
- Clase CounterItem SysMon, propiedad LineStyle
topic_type:
- apiref
api_name:
- CounterItem.LineStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff1dd78c6fd65d72c28fe8f13f7bbf5603c75f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068882"
---
# <a name="counteritemlinestyle-property"></a>CounterItem.LineStyle, propiedad

Recupera o establece el estilo de línea utilizado para representar el valor del contador.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Property LineStyle As Long
```



## <a name="property-value"></a>Valor de propiedad

Estilo de línea utilizado para representar el valor del contador. Los valores corresponden a las constantes del sistema que se muestran en la tabla siguiente.



| Value                                                                                                                                                                                                                                                                                                                                                                               | Significado                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="System.Drawing.Drawing2D.DashStyle.Solid"></span><span id="system.drawing.drawing2d.dashstyle.solid"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.SOLID"></span><dl> <dt>**System.Drawing.Drawing2D.DashStyle.Solid**</dt> <dt>0</dt> </dl>                     | Línea continua. Este es el valor predeterminado.<br/>                |
| <span id="System.Drawing.Drawing2D.DashStyle.Dash"></span><span id="system.drawing.drawing2d.dashstyle.dash"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASH"></span><dl> <dt>**System.Drawing.Drawing2D.DashStyle.Dash**</dt> <dt>1</dt> </dl>                         | Línea de puntos con segmentos largos y espacios estrechos.<br/>     |
| <span id="System.Drawing.Drawing2D.DashStyle.Dot"></span><span id="system.drawing.drawing2d.dashstyle.dot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DOT"></span><dl> <dt>**System.Drawing.Drawing2D.DashStyle.Dot**</dt> <dt>2</dt> </dl>                             | Línea de puntos con segmentos y espacios uniformes.<br/>         |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOT"></span><dl> <dt>**System.Drawing.Drawing2D.DashStyle.DashDot**</dt> <dt>3</dt> </dl>             | Línea de puntos con segmentos cortos y largos alternados.<br/> |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDotDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdotdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOTDOT"></span><dl> <dt>**System.Drawing.Drawing2D.DashStyle.DashDotDot**</dt> <dt>4</dt> </dl> | Línea de puntos con guiones alternos y puntos dobles.<br/>  |



 

## <a name="exceptions"></a>Excepciones



| Tipo de excepción               | Condición                              |
|------------------------------|----------------------------------------|
| **System.ArgumentException** | El estilo de línea especificado no es válido. |



 

## <a name="remarks"></a>Observaciones

Para especificar un valor distinto de DashStyle.Solid, [**CounterItem.Width**](counteritem-width.md) debe establecerse en 1. Si el ancho es mayor que 1, SYSMON omite el estilo de línea especificado y usa DashStyle.Solid.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





