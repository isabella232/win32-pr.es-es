---
title: Propiedad TaskSettings. StartWhenAvailable
description: En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- Programador de tareas de la propiedad StartWhenAvailable
- Programador de tareas de la propiedad StartWhenAvailable, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad StartWhenAvailable
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63325fbf7aa9186e5748294c2ef57302efa0c79b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492256"
---
# <a name="tasksettingsstartwhenavailable-property"></a>Propiedad TaskSettings. StartWhenAvailable

En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es true, la propiedad indica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada. El valor predeterminado es False.

## <a name="remarks"></a>Observaciones

Esta propiedad solo se aplica a las tareas basadas en tiempo con un límite final o tareas basadas en el tiempo que se establecen para repetirse infinitamente.

Las tareas que se inician después de que transcurra la hora programada (debido a que la propiedad [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) se establece en true) se ponen en cola en la cola del servicio Programador de tareas de las tareas y se inician después de un retraso. El retraso predeterminado es de 10 minutos.

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) del esquema de programador de tareas.

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

 

 





