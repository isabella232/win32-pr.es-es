---
title: RunningTaskCollection. Item (propiedad)
description: Para el scripting, obtiene la tarea especificada de la colección.
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- Propiedad del elemento Programador de tareas
- Propiedad Item Programador de tareas, objeto RunningTaskCollection
- Programador de tareas de objeto RunningTaskCollection, propiedad Item
topic_type:
- apiref
api_name:
- RunningTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d28da7a3f5348ff9f5d6171a1a698d95b646f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150609"
---
# <a name="runningtaskcollectionitem-property"></a>RunningTaskCollection. Item (propiedad)

Para el scripting, obtiene la tarea especificada de la colección.

## <a name="syntax"></a>Sintaxis


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**RunningTask**](runningtask.md) que contiene el contexto solicitado.

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

 

 





