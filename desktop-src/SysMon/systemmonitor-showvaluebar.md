---
title: Propiedad SystemMonitor. ShowValueBar
description: Recupera o establece un valor que determina si la barra de valores (el conjunto de valores estadísticos por debajo del gráfico) se muestra en el control.
ms.assetid: 320fbbbb-c4ea-4772-9b10-1e123849c255
keywords:
- Propiedad ShowValueBar SysMon
- Propiedad ShowValueBar SysMon, clase SystemMonitor
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
ms.openlocfilehash: f393b36162fae6aed996d2afaccd4749f22598f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801616"
---
# <a name="systemmonitorshowvaluebar-property"></a>Propiedad SystemMonitor. ShowValueBar

Recupera o establece un valor que determina si la barra de valores (el conjunto de valores estadísticos por debajo del gráfico) se muestra en el control.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property ShowValueBar As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True indica que la barra de valores se muestra en el control; en caso contrario, false. El valor predeterminado de esta propiedad es true.

## <a name="remarks"></a>Observaciones

Las estadísticas mostradas incluyen el último valor, el valor medio y los valores mínimo y máximo del contador seleccionado actualmente en el intervalo de tiempo mostrado. Para seleccionar los valores del contador que se van a mostrar, el usuario debe seleccionar el contador en el panel leyenda del control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





