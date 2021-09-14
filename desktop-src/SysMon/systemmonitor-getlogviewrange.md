---
title: Método SystemMonitor.GetLogViewRange
description: Recupera la fecha de inicio utilizada para recuperar los valores de contador de los archivos de registro.
ms.assetid: c74c3a5b-d2ec-43d8-b715-e399f42e8ae5
keywords:
- Método GetLogViewRange SysMon
- Método GetLogViewRange SysMon , objeto SystemMonitor
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374835"
---
# <a name="systemmonitorgetlogviewrange-method"></a>Método SystemMonitor.GetLogViewRange

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

*StartTime* \[ out\]
</dt> <dd>

Fecha de inicio utilizada para recuperar valores de contador de los archivos de registro.

</dd> <dt>

*StopTime* \[ out\]
</dt> <dd>

Fecha de finalización utilizada para recuperar valores de contador de los archivos de registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

SYSMON recupera los valores de contador de los archivos de registro que se encuentran dentro de las fechas de inicio y de detenerse, ambos incluidos.

El uso de este método es igual que el acceso a [**las propiedades SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) y [**SystemMonitor.LogViewStop.**](systemmonitor-logviewstop.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





