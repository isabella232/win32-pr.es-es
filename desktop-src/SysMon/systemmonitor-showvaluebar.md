---
title: Propiedad SystemMonitor.ShowValueBar
description: Recupera o establece un valor que determina si la barra de valores (el conjunto de valores estadísticos debajo del gráfico) se muestra en el control .
ms.assetid: 320fbbbb-c4ea-4772-9b10-1e123849c255
keywords:
- SysMon, propiedad ShowValueBar
- Propiedad ShowValueBar SysMon , clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad ShowValueBar
topic_type:
- apiref
api_name:
- SystemMonitor.ShowValueBar
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4ca65a3083a9c46b900d1791f79973fc61de2b7cfc552a3314ca8444e813602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954868"
---
# <a name="systemmonitorshowvaluebar-property"></a>Propiedad SystemMonitor.ShowValueBar

Recupera o establece un valor que determina si la barra de valores (el conjunto de valores estadísticos debajo del gráfico) se muestra en el control .

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property ShowValueBar As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True indica que la barra de valores se muestra en el control; de lo contrario, false. El valor predeterminado de esta propiedad es true.

## <a name="remarks"></a>Comentarios

Las estadísticas mostradas incluyen el último valor, el valor medio y los valores mínimo y máximo del contador seleccionado actualmente durante el intervalo de tiempo mostrado. Para seleccionar los valores de contador que se mostrarán, el usuario debe seleccionar el contador en el panel Leyenda del control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> </dl>

 

 





