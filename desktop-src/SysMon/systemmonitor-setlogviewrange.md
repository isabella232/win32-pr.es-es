---
title: SystemMonitor. SetLogViewRange, método
description: Establece la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.
ms.assetid: ced641d0-cf71-4826-8ff0-c05f20a71aaa
keywords:
- Método SetLogViewRange SysMon
- Método SetLogViewRange SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método SetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.SetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534a7dc3bf711832ec99e4202f4f56cc347f336b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422104"
---
# <a name="systemmonitorsetlogviewrange-method"></a>SystemMonitor. SetLogViewRange, método

Establece la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.

## <a name="syntax"></a>Sintaxis


```VB
SystemMonitor.SetLogViewRange( _
  ByVal StartTime As Date, _
  ByVal StopTime As Date _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartTime* \[ de\]
</dt> <dd>

Fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.

</dd> <dt>

*StopTime* \[ de\]
</dt> <dd>

Fecha de finalización utilizada para recuperar los valores de contador de los archivos de registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

SYSMON recupera los valores de los contadores de los archivos de registro que se encuentran dentro de las fechas de inicio y de finalización, en su interior.

Si no especifica una fecha de inicio o establece la fecha de inicio en un valor de fecha que está fuera del intervalo de valores de fecha que se encuentra en los archivos de registro, SYSMON cambia el valor al valor de fecha más antiguo que se encuentra en los archivos de registro. Si el valor inicial es mayor que el valor de detención, SYSMON cambia el valor inicial para que tenga el mismo valor que el valor de detención.

Si no especifica un valor de detención o establece el valor de detención en un valor de fecha posterior a la última fecha incluida en el archivo de registro, SYSMON cambia el valor al valor de fecha más reciente que se encuentra en los archivos de registro. Si el valor de detención es menor que el valor de detención, SYSMON cambia el valor de detención para que tenga el mismo valor que el valor de inicio.

Si especifica una fecha de inicio y de finalización, debe especificar las fechas antes de establecer [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md). Si establece las fechas después de establecer **SystemMonitor. DataSourceType**, solo el primer valor de contador se recupera del archivo de registro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.GetLogViewRange**](systemmonitor-getlogviewrange.md)
</dt> </dl>

 

 





