---
title: Propiedad SystemMonitor.Highlight
description: Recupera o establece un valor que indica si los valores de los contadores seleccionados están resaltados en el gráfico.
ms.assetid: 5342b81f-71bb-4564-b520-1e91d3002c5b
keywords:
- Resaltar la propiedad SysMon
- Propiedad Highlight SysMon , Clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad Highlight
topic_type:
- apiref
api_name:
- SystemMonitor.Highlight
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3009501123673175c64d88acd838f94aa7e332aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374834"
---
# <a name="systemmonitorhighlight-property"></a>Propiedad SystemMonitor.Highlight

Recupera o establece un valor que indica si los valores de los contadores seleccionados están resaltados en el gráfico.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property Highlight As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True indica que los valores de los contadores seleccionados están resaltados en el gráfico; de lo contrario, False. El valor predeterminado es False.

## <a name="remarks"></a>Observaciones

Para seleccionar uno o varios contadores, puede establecer [**CounterItem.Selected**](counteritem-selected.md) en True, o bien el usuario puede seleccionar los contadores de la lista de contadores que se muestra en leyenda.

**Antes de Windows Vista:** No se pueden seleccionar contadores mediante programación y el usuario solo puede seleccionar un contador de la lista de contadores que se muestra en la leyenda.

El resaltado puede ser blanco o negro, dependiendo del valor de la [**propiedad BackColor.**](systemmonitor-backcolor.md) El resaltado se establece automáticamente en el color que proporcionará suficiente contraste entre el color de resaltado y el color de fondo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> <dt>

[**CounterItem.Selected**](counteritem-selected.md)
</dt> </dl>

 

 





