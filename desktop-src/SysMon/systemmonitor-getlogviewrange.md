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
ms.openlocfilehash: 3233dd57327734669631fc57b31bfb85578621991f34c1b1c414a69697b82048
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882431"
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

## <a name="remarks"></a>Comentarios

SYSMON recupera los valores de contador de los archivos de registro que se encuentran dentro de las fechas de inicio y de detenerse, ambos incluidos.

El uso de este método es igual que el acceso a [**las propiedades SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) y [**SystemMonitor.LogViewStop.**](systemmonitor-logviewstop.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.SetLogViewRange**](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





