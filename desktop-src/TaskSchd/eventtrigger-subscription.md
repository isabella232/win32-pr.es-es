---
title: Propiedad EventTrigger. subscription
description: En el caso de scripting, obtiene o establece una cadena de consulta que identifica el evento que activa el desencadenador.
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- Programador de tareas de propiedad de suscripción
- Propiedad subscription Programador de tareas, objeto EventTrigger
- Objeto EventTrigger Programador de tareas, propiedad subscription
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686128"
---
# <a name="eventtriggersubscription-property"></a>Propiedad EventTrigger. subscription

En el caso de scripting, obtiene o establece una cadena de consulta que identifica el evento que activa el desencadenador.

## <a name="syntax"></a>Sintaxis


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a>Valor de propiedad

Cadena de consulta que identifica el evento que activa el desencadenador.

## <a name="remarks"></a>Observaciones

Al leer o escribir su propio XML para una tarea, la suscripción de eventos se especifica mediante el elemento de [**suscripción**](taskschedulerschema-subscription-eventtriggertype-element.md) del esquema de programador de tareas.

Para obtener más información sobre cómo escribir una cadena de consulta para determinados eventos, vea [selección de eventos](/previous-versions//aa385231(v=vs.85)) y [suscripción a eventos](../wes/subscribing-to-events.md).

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

