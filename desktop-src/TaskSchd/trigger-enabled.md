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
ms.openlocfilehash: 2b9fe5439576322807abea6e10089460eaed4440496ed6a9e0f989dd44bc7e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099705"
---
# <a name="triggerenabled-property"></a>Propiedad Trigger.Enabled

Para el scripting, obtiene o establece un valor booleano que indica si el desencadenador está habilitado.

## <a name="syntax"></a>Syntax


```VB
Trigger.Enabled As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True si el desencadenador está habilitado; de lo contrario, false. El valor predeterminado es true.

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, la propiedad enabled se especifica mediante el [**elemento Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) del Programador de tareas esquema.

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

 

 





