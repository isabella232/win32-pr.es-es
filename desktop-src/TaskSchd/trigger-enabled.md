---
title: Propiedad Trigger.Enabled
description: Para el scripting, obtiene o establece un valor booleano que indica si el desencadenador está habilitado.
ms.assetid: 8fb5a0cc-ddd4-430d-9593-95a4cb311f18
keywords:
- Propiedades habilitadas Programador de tareas
- Propiedad Enabled Programador de tareas , Trigger object
- Desencadenador de objeto Programador de tareas propiedad , Enabled
topic_type:
- apiref
api_name:
- Trigger.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411bc36dcf03933e2b4cee2f575aaec3b8133846
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264916"
---
# <a name="triggerenabled-property"></a>Propiedad Trigger.Enabled

Para el scripting, obtiene o establece un valor booleano que indica si el desencadenador está habilitado.

## <a name="syntax"></a>Sintaxis


```VB
Trigger.Enabled As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True si el desencadenador está habilitado; de lo contrario, false. El valor predeterminado es true.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, la propiedad enabled se especifica mediante el [**elemento Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) del Programador de tareas esquema.

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

 

 





