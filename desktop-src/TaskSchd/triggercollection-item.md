---
title: TriggerCollection. Item (propiedad)
description: En el caso de scripting, obtiene el desencadenador especificado de la colección.
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- Propiedad del elemento Programador de tareas
- Propiedad Item Programador de tareas, objeto TriggerCollection
- Programador de tareas de objeto TriggerCollection, propiedad Item
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
ms.openlocfilehash: d600418d43459d6c4cbfcb0746a378633d096c24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801730"
---
# <a name="triggercollectionitem-property"></a>TriggerCollection. Item (propiedad)

En el caso de scripting, obtiene el desencadenador especificado de la colección.

## <a name="syntax"></a>Sintaxis


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**desencadenador**](trigger.md) que representa el desencadenador solicitado.

## <a name="remarks"></a>Observaciones

Las colecciones se basan en 1. En otras palabras, el índice del primer elemento de la colección es 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





