---
title: Método TriggerCollection.Remove
description: Para el scripting, quita el desencadenador especificado de la colección de desencadenadores usados por la tarea.
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- desencadenadores Programador de tareas , quitar
- Quitar método Programador de tareas
- Quitar método Programador de tareas , objeto TriggerCollection
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
ms.openlocfilehash: 401e84e57b28db9b08fd7e93e85fb7bc35f60647
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891369"
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

## <a name="remarks"></a>Observaciones

Al quitar elementos, tenga en cuenta que el índice del primer elemento de la colección es 1 y el índice del último elemento es el valor de la [**propiedad TriggerCollection.Count.**](triggercollection-count.md)

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

 

 





