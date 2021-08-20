---
title: Evento SystemMonitor.OnCounterSelected
description: Le notifica cuando se selecciona un contador.
ms.assetid: 788a95a7-47ec-41f9-bf46-324ad3cc8a4e
keywords:
- OnCounterSelected, evento SysMon
- Evento OnCounterSelected SysMon , clase SystemMonitor
- Clase SystemMonitor SysMon , Evento OnCounterSelected
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
ms.openlocfilehash: 9e5e5402eb123c5edd44a5616b6973940ba065e2b0c8c2bfa63e7d151ae30124
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957253"
---
# <a name="systemmonitoroncounterselected-event"></a>Evento SystemMonitor.OnCounterSelected

Le notifica cuando se selecciona un contador.

## <a name="syntax"></a>Sintaxis


```VB
SystemMonitor.OnCounterSelected( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

Índice del contador seleccionado en el [**objeto de colección Counters.**](counters.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Puede recibir este evento cuando

-   Establezca [**CounterItem.Selected en**](counteritem-selected.md) True.
-   El usuario selecciona un contador en la leyenda.
-   El usuario hace doble clic en un contador de la leyenda.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor.OnCounter Agregado**](systemmonitor-oncounteradded.md)
</dt> <dt>

[**SystemMonitor.OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)
</dt> </dl>

 

 





