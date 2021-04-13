---
title: TriggerCollection. Remove (método)
description: En el caso de scripting, quita el desencadenador especificado de la colección de desencadenadores utilizada por la tarea.
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- desencadenadores Programador de tareas, quitar
- Quitar método Programador de tareas
- Quitar método Programador de tareas, objeto TriggerCollection
- Objeto TriggerCollection Programador de tareas, Remove (método)
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
ms.openlocfilehash: 401e84e57b28db9b08fd7e93e85fb7bc35f60647
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359720"
---
# <a name="triggercollectionremove-method"></a>TriggerCollection. Remove (método)

En el caso de scripting, quita el desencadenador especificado de la colección de desencadenadores utilizada por la tarea.

## <a name="syntax"></a>Sintaxis


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

Índice del desencadenador que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Al quitar los elementos, tenga en cuenta que el índice del primer elemento de la colección es 1 y el índice del último elemento es el valor de la propiedad [**TriggerCollection. Count**](triggercollection-count.md) .

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

 

 





