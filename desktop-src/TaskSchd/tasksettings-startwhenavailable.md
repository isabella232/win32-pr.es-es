---
title: Propiedad TaskSettings.StartWhenAvailable
description: Para el scripting, obtiene o establece un valor booleano que indica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- Propiedad StartWhenAvailable Programador de tareas
- Propiedad StartWhenAvailable Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas , propiedad StartWhenAvailable
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160603"
---
# <a name="tasksettingsstartwhenavailable-property"></a>Propiedad TaskSettings.StartWhenAvailable

Para el scripting, obtiene o establece un valor booleano que indica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es True, la propiedad indica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada. El valor predeterminado es False.

## <a name="remarks"></a>Observaciones

Esta propiedad solo se aplica a las tareas basadas en tiempo con un límite final o tareas basadas en tiempo que se establecen para repetirse infinitamente.

Las tareas que se inician una vez transcurrido el tiempo programado (debido a que la propiedad [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) se establece en True) se ponen en cola en la cola de tareas del servicio Programador de tareas y se inician después de un retraso. El retraso predeterminado es de 10 minutos.

Al leer o escribir XML para una tarea, esta configuración se especifica en el [**elemento StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) del Programador de tareas esquema.

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

 

 





