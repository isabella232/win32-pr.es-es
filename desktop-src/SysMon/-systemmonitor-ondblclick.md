---
title: Evento SystemMonitor.OnDblClick
description: Le notifica cuando un usuario hace doble clic en la línea del gráfico, la barra del histograma o el elemento de informe con el botón izquierdo del mouse.
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- SysMon, evento OnDblClick
- Evento OnDblClick SysMon , clase SystemMonitor
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
ms.openlocfilehash: 37ef829fad368e7d8cf3b65ab70db4600f6d635b1d36bcc5e3f50fcdbaf429a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883968"
---
# <a name="systemmonitorondblclick-event"></a>Evento SystemMonitor.OnDblClick

Le notifica cuando un usuario hace doble clic en la línea del gráfico, la barra del histograma o el elemento de informe con el botón izquierdo del mouse.

## <a name="syntax"></a>Sintaxis


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ in, out\]
</dt> <dd>

Índice del contador seleccionado en el [**objeto de colección Counters.**](counters.md) Se devuelve un valor de índice de 0 si no se ha seleccionado ningún contador; De lo contrario, se devuelve el índice del contador seleccionado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Cuando se desencadena este evento, el contador que el usuario seleccionó en el gráfico de líneas y el histograma también se selecciona en el panel Leyenda. Esto facilita al usuario del Monitor de sistema ver qué contador se selecciona cuando se muestran varios valores de contador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





