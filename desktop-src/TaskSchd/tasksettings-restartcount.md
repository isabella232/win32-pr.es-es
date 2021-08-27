---
title: Propiedad TaskSettings.RestartCount
description: Para el scripting, obtiene o establece el número de veces que el Programador de tareas intentará reiniciar la tarea.
ms.assetid: 7d92c2c6-e846-4664-b22a-b2a6ca46c225
keywords:
- Propiedad RestartCount Programador de tareas
- Propiedad RestartCount Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas , propiedad RestartCount
topic_type:
- apiref
api_name:
- TaskSettings.RestartCount
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a34e8eef84575548998e39ab47bc5492baca368f7012d5fa096c831539ceb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072415"
---
# <a name="tasksettingsrestartcount-property"></a>Propiedad TaskSettings.RestartCount

Para el scripting, obtiene o establece el número de veces que el Programador de tareas intentará reiniciar la tarea.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RestartCount As Integer
```



## <a name="property-value"></a>Valor de propiedad

Número de veces que el Programador de tareas intentará reiniciar la tarea.

## <a name="remarks"></a>Comentarios

Al leer o escribir XML para una tarea, esta configuración se especifica en el [**elemento Count**](taskschedulerschema-count-restarttype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





