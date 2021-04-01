---
title: Propiedad SystemMonitor. LogViewStart
description: Recupera o establece la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.
ms.assetid: f9fdef17-e8b1-4efb-86db-40ca0c499194
keywords:
- Propiedad LogViewStart SysMon
- Propiedad LogViewStart SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad LogViewStart
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStart
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967c44940b195c4d8ddd3028e1d4f307827bbbfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996260"
---
# <a name="systemmonitorlogviewstart-property"></a>Propiedad SystemMonitor. LogViewStart

Recupera o establece la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Property LogViewStart As Date
```



## <a name="property-value"></a>Valor de propiedad

Fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.

## <a name="remarks"></a>Observaciones

SYSMON recupera los valores de contador de los archivos de registro que se encuentran dentro de las fechas de inicio y [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) , ambos inclusive.

Si no especifica una fecha de inicio o establece esta propiedad en un valor de fecha que está fuera del intervalo de valores de fecha que se encuentra en los archivos de registro, SYSMON cambia el valor al valor de fecha más antiguo que se encuentra en los archivos de registro.

Si esta propiedad se establece en un valor de fecha mayor que [**LogViewStop**](systemmonitor-logviewstop.md), SYSMON cambia el valor al valor de **LogViewStop**.

Si especifica una fecha de inicio y de finalización, debe especificar las fechas antes de establecer [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md).

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

[**SystemMonitor. logfiles**](systemmonitor-logfiles.md)
</dt> <dt>

[**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md)
</dt> <dt>

[**SystemMonitor.LogSourceStartTime**](systemmonitor-logsourcestarttime.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





