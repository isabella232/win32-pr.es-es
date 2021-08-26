---
title: Método TriggerCollection.Remove
description: Para el scripting, quita el desencadenador especificado de la colección de desencadenadores usados por la tarea.
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- desencadenadores Programador de tareas , quitando
- Quitar método Programador de tareas
- Remove method Programador de tareas , TriggerCollection object
- TriggerCollection object Programador de tareas , Remove (método)
topic_type:
- apiref
api_name:
- TriggerCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ff3fda5119f4b487ba7f04546ea94e0a601a4749e1aa6aad7a9120907cd6cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099664"
---
# <a name="triggercollectionremove-method"></a>Método TriggerCollection.Remove

Para el scripting, quita el desencadenador especificado de la colección de desencadenadores usados por la tarea.

## <a name="syntax"></a>Sintaxis


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

Índice del desencadenador que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Al quitar elementos, tenga en cuenta que el índice del primer elemento de la colección es 1 y el índice del último elemento es el valor de la [**propiedad TriggerCollection.Count.**](triggercollection-count.md)

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

 

 





