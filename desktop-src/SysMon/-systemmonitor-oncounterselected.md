---
title: Evento SystemMonitor. OnCounterSelected
description: Le notifica cuando se selecciona un contador.
ms.assetid: 788a95a7-47ec-41f9-bf46-324ad3cc8a4e
keywords:
- Evento OnCounterSelected SysMon
- Evento OnCounterSelected SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, evento OnCounterSelected
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterSelected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0174ab2f896a27e44df592ec28b7cb12a03198f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666006"
---
# <a name="systemmonitoroncounterselected-event"></a>Evento SystemMonitor. OnCounterSelected

Le notifica cuando se selecciona un contador.

## <a name="syntax"></a>Sintaxis


```VB
SystemMonitor.OnCounterSelected( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

Índice del contador seleccionado en el objeto de colección [**counters**](counters.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Puede recibir este evento cuando

-   El valor de el elemento se establece en true [**.**](counteritem-selected.md)
-   El usuario selecciona un contador en la leyenda
-   El usuario hace doble clic en un contador de la leyenda

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor.OnCounterAdded**](systemmonitor-oncounteradded.md)
</dt> <dt>

[**SystemMonitor.OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)
</dt> </dl>

 

 





