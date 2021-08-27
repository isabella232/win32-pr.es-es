---
title: Propiedad SystemMonitor.LogViewStop
description: Recupera o establece la fecha de finalización utilizada para recuperar valores de contador de los archivos de registro.
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- Propiedad LogViewStop SysMon
- Propiedad LogViewStop SysMon , objeto SystemMonitor
- Objeto SystemMonitor SysMon, propiedad LogViewStop
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStop
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8c30305f99e0d9bf66dd0f00dccc7674073e0f7058bca4284411c9d24426b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882079"
---
# <a name="systemmonitorlogviewstop-property"></a>Propiedad SystemMonitor.LogViewStop

Recupera o establece la fecha de finalización utilizada para recuperar valores de contador de los archivos de registro.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a>Valor de propiedad

Fecha de finalización utilizada para recuperar valores de contador de los archivos de registro.

## <a name="remarks"></a>Comentarios

SYSMON recupera los valores de contador de los archivos de registro que se encuentran dentro de [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) y las fechas de detenerse, ambos incluidos.

Si no especifica un valor de detención o establece esta propiedad en un valor de fecha posterior a la última fecha contenida en el archivo de registro, SYSMON cambia el valor al valor de fecha más reciente que se encuentra en los archivos de registro.

Si esta propiedad se establece en un valor de fecha menor que [**LogViewStart,**](systemmonitor-logviewstart.md)SYSMON cambia el valor al valor **de LogViewStart**.

Debe establecer la fecha de inicio antes de establecer la fecha de detenerse. De lo contrario, ambos valores se establecen en Date.MinValue y, si establece las fechas después de establecer [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md), solo se recupera el primer valor de contador del archivo de registro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.GetLogViewRange**](systemmonitor-getlogviewrange.md)
</dt> <dt>

[**SystemMonitor.LogSourceStopTime**](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





