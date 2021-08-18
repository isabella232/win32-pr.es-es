---
title: Trigger.Id propiedad
description: Para el scripting, obtiene o establece el identificador del desencadenador.
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- Identificador de propiedad Programador de tareas
- Propiedad Id Programador de tareas , Trigger object
- Desencadenador de objeto Programador de tareas , propiedad Id
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c9ff851eab7b5e9cfb124bf03c83986d24b391d5ea109865ff2d59e2e33536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002163"
---
# <a name="triggerid-property"></a>Trigger.Id propiedad

Para el scripting, obtiene o establece el identificador del desencadenador.

## <a name="syntax"></a>Syntax


```VB
Trigger.Id As String
```



## <a name="property-value"></a>Valor de propiedad

Identificador del desencadenador. Este identificador lo usa el Programador de tareas con fines de registro.

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, el identificador del desencadenador se especifica en el atributo Id de los elementos de desencadenador individuales (por ejemplo, el atributo Id del [**elemento BootTrigger)**](taskschedulerschema-boottrigger-triggergroup-element.md) del esquema Programador de tareas.

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

 

 





