---
title: Propiedad EventTrigger.Subscription
description: Para el scripting, obtiene o establece una cadena de consulta que identifica el evento que activa el desencadenador.
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- Propiedad de suscripción Programador de tareas
- Propiedad subscription Programador de tareas , objeto EventTrigger
- Objeto EventTrigger Programador de tareas , propiedad Subscription
topic_type:
- apiref
api_name:
- EventTrigger.Subscription
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ad05576e248d3ad6c2551a8654a9198ca3c0f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068662"
---
# <a name="eventtriggersubscription-property"></a>Propiedad EventTrigger.Subscription

Para el scripting, obtiene o establece una cadena de consulta que identifica el evento que activa el desencadenador.

## <a name="syntax"></a>Sintaxis


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a>Valor de propiedad

Cadena de consulta que identifica el evento que activa el desencadenador.

## <a name="remarks"></a>Observaciones

Al leer o escribir su propio XML para una tarea, la suscripción de eventos se especifica mediante el elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) del Programador de tareas esquema.

Para obtener más información sobre cómo escribir una cadena de consulta para determinados eventos, vea [Selección de](/previous-versions//aa385231(v=vs.85)) eventos y Suscripción [a eventos](../wes/subscribing-to-events.md).

## <a name="examples"></a>Ejemplos

La siguiente cadena de consulta define una suscripción a todos los eventos de nivel 2 en el canal del sistema:


```XML
"<QueryList>
    <Query Id='1'>
        <Select Path='System'>*[System/Level=2]</Select>
    </Query>
</QueryList>" 
```



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
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

