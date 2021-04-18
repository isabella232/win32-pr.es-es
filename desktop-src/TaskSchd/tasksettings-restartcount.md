---
title: Propiedad TaskSettings. RestartCount
description: En el caso de scripting, obtiene o establece el número de veces que el Programador de tareas intentará reiniciar la tarea.
ms.assetid: 7d92c2c6-e846-4664-b22a-b2a6ca46c225
keywords:
- Programador de tareas de la propiedad RestartCount
- Programador de tareas de la propiedad RestartCount, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad RestartCount
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
ms.openlocfilehash: bee033eebde7b085d6df40f1e5e20d6dcf640a93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422156"
---
# <a name="tasksettingsrestartcount-property"></a>Propiedad TaskSettings. RestartCount

En el caso de scripting, obtiene o establece el número de veces que el Programador de tareas intentará reiniciar la tarea.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.RestartCount As Integer
```



## <a name="property-value"></a>Valor de propiedad

Número de veces que el Programador de tareas intentará reiniciar la tarea.

## <a name="remarks"></a>Observaciones

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**Count**](taskschedulerschema-count-restarttype-element.md) del esquema programador de tareas.

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

 

 





