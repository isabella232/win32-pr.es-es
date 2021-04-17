---
title: Propiedad SystemMonitor. ManualUpdate
description: Recupera o establece un valor que indica si el contenido del monitor de sistema se actualizará manualmente o automáticamente a intervalos especificados.
ms.assetid: e068a955-ec1d-4f93-9261-25ba87773913
keywords:
- Propiedad ManualUpdate SysMon
- Propiedad ManualUpdate SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad ManualUpdate
topic_type:
- apiref
api_name:
- SystemMonitor.ManualUpdate
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1ecb426b47ba9cb7ec50b737f4f32d5ce274eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665983"
---
# <a name="systemmonitormanualupdate-property"></a>Propiedad SystemMonitor. ManualUpdate

Recupera o establece un valor que indica si el contenido del monitor de sistema se actualizará manualmente o automáticamente a intervalos especificados.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property ManualUpdate As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True indica que el gráfico se actualiza manualmente. False indica que el gráfico se actualiza automáticamente según el intervalo de actualización especificado en [**SystemMonitor. UpdateInterval**](systemmonitor-updateinterval.md).

## <a name="remarks"></a>Observaciones

De forma predeterminada, el gráfico se actualiza automáticamente.

Para actualizar el gráfico manualmente, llame al método [**SystemMonitor. CollectSample**](systemmonitor-collectsample.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.CollectSample**](systemmonitor-collectsample.md)
</dt> <dt>

[**SystemMonitor.UpdateGraph**](systemmonitor-updategraph.md)
</dt> </dl>

 

 





