---
title: Desencadenador. Enabled (propiedad)
description: En el caso de scripting, obtiene o establece un valor booleano que indica si el desencadenador está habilitado.
ms.assetid: 8fb5a0cc-ddd4-430d-9593-95a4cb311f18
keywords:
- Propiedad Enabled Programador de tareas
- Propiedad habilitada Programador de tareas, objeto desencadenador
- Objeto desencadenador Programador de tareas, propiedad Enabled
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996152"
---
# <a name="triggerenabled-property"></a>Desencadenador. Enabled (propiedad)

En el caso de scripting, obtiene o establece un valor booleano que indica si el desencadenador está habilitado.

## <a name="syntax"></a>Sintaxis


```VB
Trigger.Enabled As Boolean
```



## <a name="property-value"></a>Valor de propiedad

True si el desencadenador está habilitado; en caso contrario, false. El valor predeterminado es true.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, se especifica la propiedad Enabled mediante el elemento [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) del esquema de programador de tareas.

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

 

 





