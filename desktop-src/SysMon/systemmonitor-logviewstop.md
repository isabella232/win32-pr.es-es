---
title: Propiedad SystemMonitor. LogViewStop
description: Recupera o establece la fecha de finalización utilizada para recuperar los valores de contador de los archivos de registro.
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- Propiedad LogViewStop SysMon
- Propiedad LogViewStop SysMon, objeto SystemMonitor
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
ms.openlocfilehash: 4b725ee2efba22453d44f1e15fb9ce231b07cdb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996352"
---
# <a name="systemmonitorlogviewstop-property"></a>Propiedad SystemMonitor. LogViewStop

Recupera o establece la fecha de finalización utilizada para recuperar los valores de contador de los archivos de registro.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a>Valor de propiedad

Fecha de finalización utilizada para recuperar los valores de contador de los archivos de registro.

## <a name="remarks"></a>Observaciones

SYSMON recupera los valores de contador de los archivos de registro que se encuentran dentro de [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) y las fechas de detención, ambos inclusive.

Si no especifica un valor de detención o establece esta propiedad en un valor de fecha posterior a la última fecha incluida en el archivo de registro, SYSMON cambia el valor al valor de fecha más reciente que se encuentra en los archivos de registro.

Si esta propiedad se establece en un valor de fecha menor que [**LogViewStart**](systemmonitor-logviewstart.md), SYSMON cambia el valor al valor de **LogViewStart**.

Debe establecer la fecha de inicio antes de establecer la fecha de detención; de lo contrario, ambos valores se establecen en Date. MinValue y, si establece las fechas después de establecer [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md), solo se recupera el primer valor de contador del archivo de registro.

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

[**SystemMonitor.GetLogViewRange**](systemmonitor-getlogviewrange.md)
</dt> <dt>

[**SystemMonitor.LogSourceStopTime**](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





