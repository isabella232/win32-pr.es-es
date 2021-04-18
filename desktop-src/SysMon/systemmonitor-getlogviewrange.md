---
title: SystemMonitor. GetLogViewRange, método
description: Recupera la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- Método GetLogViewRange SysMon
- Método GetLogViewRange SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método GetLogViewRange
topic_type:
- apiref
api_name:
- SystemMonitor.GetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d494a5861ff9c0d2c076abe2bdad749d21653500
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534185"
---
# <a name="systemmonitorgetlogviewrange-method"></a>SystemMonitor. GetLogViewRange, método

Recupera la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.

## <a name="syntax"></a>Sintaxis


```VB
SystemMonitor.GetLogViewRange( _
  ByRef StartTime As Date, _
  ByRef StopTime As Date _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartTime* \[ enuncia\]
</dt> <dd>

Fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.

</dd> <dt>

*StopTime* \[ enuncia\]
</dt> <dd>

Fecha de finalización utilizada para recuperar los valores de contador de los archivos de registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

SYSMON recupera los valores de los contadores de los archivos de registro que se encuentran dentro de las fechas de inicio y de finalización, en su interior.

El uso de este método es igual que el acceso a las propiedades [**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md) y [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md) .

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

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





