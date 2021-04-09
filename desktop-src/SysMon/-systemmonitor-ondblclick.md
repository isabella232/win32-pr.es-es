---
title: Evento SystemMonitor. OnDblClick
description: Le informa cuando un usuario hace doble clic en la línea del gráfico, en la barra de histograma o en el elemento de informe con el botón primario del mouse.
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- Evento de OnDblClick SysMon
- Evento Alhacerdobleclic SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, evento OnDblClick
topic_type:
- apiref
api_name:
- SystemMonitor.OnDblClick
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f21c6d67468ecb07bbe0fe83bec7b48a086571
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150338"
---
# <a name="systemmonitorondblclick-event"></a>Evento SystemMonitor. OnDblClick

Le informa cuando un usuario hace doble clic en la línea del gráfico, en la barra de histograma o en el elemento de informe con el botón primario del mouse.

## <a name="syntax"></a>Sintaxis


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de in, out\]
</dt> <dd>

Índice del contador seleccionado en el objeto de colección [**counters**](counters.md) . Se devuelve un valor de índice de 0 si no se ha seleccionado ningún contador; de lo contrario, se devuelve el índice del contador seleccionado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Cuando se desencadena este evento, el contador que el usuario seleccionó en el gráfico de líneas y el histograma también se selecciona en el panel leyenda. Esto hace que sea más fácil para el usuario del monitor de sistema ver qué contador está seleccionado cuando se muestran varios valores de contador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





