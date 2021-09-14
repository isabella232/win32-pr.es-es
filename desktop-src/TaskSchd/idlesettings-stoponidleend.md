---
title: Propiedad IdleSettings.StopOnIdleEnd
description: Para el scripting, obtiene o establece un valor booleano que indica que el Programador de tareas finalizará la tarea si la condición de inactividad finaliza antes de que se complete la tarea.
ms.assetid: 5908bf6b-227a-4234-a741-82cf38163171
keywords:
- Propiedad StopOnIdleEnd Programador de tareas
- Propiedad StopOnIdleEnd Programador de tareas , objeto IdleSettings
- Objeto IdleSettings Programador de tareas , propiedad StopOnIdleEnd
topic_type:
- apiref
api_name:
- IdleSettings.StopOnIdleEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f475c0a05d43cf0fbdd7097c1ee083f9040b07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073444"
---
# <a name="idlesettingsstoponidleend-property"></a>Propiedad IdleSettings.StopOnIdleEnd

Para el scripting, obtiene o establece un valor booleano que indica que el Programador de tareas finalizará la tarea si la condición de inactividad finaliza antes de que se complete la tarea.

## <a name="syntax"></a>Sintaxis


```VB
IdleSettings.StopOnIdleEnd As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Valor booleano que indica que el Programador de tareas finalizará la tarea si la condición de inactividad finaliza antes de que se complete la tarea.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el [**elemento StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) del Programador de tareas esquema.

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
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





