---
title: SystemMonitor.Batmétodo chingLock
description: Bloquea el monitor de sistema para impedir que muestre los datos de contador del contador o el archivo de registro recién agregados.
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- Método BatchingLock SysMon
- Método BatchingLock SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método BatchingLock
topic_type:
- apiref
api_name:
- SystemMonitor.BatchingLock
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858a6920b039d911ae571d81744eb99dea4ef4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666021"
---
# <a name="systemmonitorbatchinglock-method"></a>SystemMonitor.Batmétodo chingLock

Bloquea el monitor de sistema para impedir que muestre los datos de contador del contador o el archivo de registro recién agregados.

## <a name="syntax"></a>Sintaxis


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bloquear* \[ de\]
</dt> <dd>

Establézcalo en true para bloquear el monitor de sistema y evitar que muestre los datos de contador del contador o el archivo de registro recién agregados. Establézcalo en false para quitar el bloqueo.

</dd> <dt>

*batchReason* \[ de\]
</dt> <dd>

Identifica el origen de los datos que está bloqueando. Use el mismo valor de razón al bloquear y desbloquear el recurso. Para ver los valores posibles, consulte la enumeración [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Debe llamar a este método dos veces, una vez para bloquear el origen (true) y otra para desbloquear el origen (false).

Solo puede colocar un bloqueo. Por ejemplo, si establece el bloqueo de SysmonBatchAddFiles y, a continuación, realiza una segunda llamada con SysmonBatchAddCounters como motivo, la segunda llamada quita el bloqueo colocado por la primera llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





