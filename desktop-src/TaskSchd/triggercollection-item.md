---
title: Propiedad TriggerCollection.Item
description: Para el scripting, obtiene el desencadenador especificado de la colección.
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- Propiedad Item Programador de tareas
- Propiedad Item Programador de tareas , objeto TriggerCollection
- Objeto TriggerCollection Programador de tareas , propiedad Item
topic_type:
- apiref
api_name:
- TriggerCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee0460d79ef239c8dacbf7fbd45573dac8ba03ad9b53e6e9881dded1bf01030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001963"
---
# <a name="triggercollectionitem-property"></a>Propiedad TriggerCollection.Item

Para el scripting, obtiene el desencadenador especificado de la colección.

## <a name="syntax"></a>Syntax


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**Trigger**](trigger.md) que representa el desencadenador solicitado.

## <a name="remarks"></a>Comentarios

Las colecciones se basan en 1. En otras palabras, el índice del primer elemento de la colección es 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





