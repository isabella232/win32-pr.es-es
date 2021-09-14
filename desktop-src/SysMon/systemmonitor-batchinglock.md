---
title: Método SystemMonitor.BatchingLock
description: Bloquea el Monitor de sistema para evitar que muestree los datos del contador o archivo de registro recién agregados.
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- Método SysMon de BatchingLock
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068832"
---
# <a name="systemmonitorbatchinglock-method"></a>Método SystemMonitor.BatchingLock

Bloquea el Monitor de sistema para evitar que muestree los datos del contador o archivo de registro recién agregados.

## <a name="syntax"></a>Sintaxis


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lock* \[ En\]
</dt> <dd>

Establezca en True para bloquear el Monitor de sistema para evitar que muestree los datos del contador o archivo de registro recién agregados. Establezca en False para quitar el bloqueo.

</dd> <dt>

*batchReason* \[ En\]
</dt> <dd>

Identifica el origen de los datos que está bloqueando. Use el mismo valor de motivo al bloquear y desbloquear el recurso. Para ver los valores posibles, consulte la [**enumeración SysmonBatchReason.**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Debe llamar a este método dos veces, una vez para bloquear el origen (True) y otra para desbloquear el origen (False).

Solo puede colocar un bloqueo. Por ejemplo, si establece el bloqueo para SysmonBatchAddFiles y, a continuación, realiza una segunda llamada mediante SysmonBatchAddCounters como motivo, la segunda llamada quita el bloqueo colocado por la primera llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> </dl>

 

 





