---
title: Evento SystemMonitor.OnCounterDeleted
description: Le notifica antes de que se elimine un contador de la colección Counters.
ms.assetid: ab6bc1ba-20cd-4774-853e-b6adb765fae3
keywords:
- Evento OnCounterDeleted SysMon
- Evento OnCounterDeleted SysMon , clase SystemMonitor
- Clase SystemMonitor SysMon , Evento OnCounterDeleted
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterDeleted
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44c178cb0b9c19fde0814f15729ffd49a0a0dbea65023bde06673cd843aeb668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884007"
---
# <a name="systemmonitoroncounterdeleted-event"></a>Evento SystemMonitor.OnCounterDeleted

Le notifica antes de que se elimine un contador de [**la colección Counters.**](counters.md)

## <a name="syntax"></a>Sintaxis


```VB
SystemMonitor.OnCounterDeleted( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

Índice del contador que se va a eliminar del [**objeto de colección Counters.**](counters.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SystemMonitor.OnCounter Agregado**](systemmonitor-oncounteradded.md)
</dt> <dt>

[**SystemMonitor.OnCounterSelected**](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





