---
title: Propiedad RunningTaskCollection.Item
description: Para el scripting, obtiene la tarea especificada de la colección.
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- Propiedad Item Programador de tareas
- Propiedad Item Programador de tareas , objeto RunningTaskCollection
- Objeto RunningTaskCollection Programador de tareas , propiedad Item
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886569"
---
# <a name="runningtaskcollectionitem-property"></a>Propiedad RunningTaskCollection.Item

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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





