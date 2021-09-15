---
title: Elemento WakeToRun (settingsType)
description: Especifica que Programador de tareas reactivará el equipo cuando sea el momento de ejecutar la tarea.
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- WakeToRun, elemento Programador de tareas
topic_type:
- apiref
api_name:
- WakeToRun
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23eeaa06073fa9259c1a48137cf3676baa402d39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474660"
---
# <a name="waketorun-settingstype-element"></a>Elemento WakeToRun (settingsType)

Especifica que Programador de tareas reactivará el equipo cuando sea el momento de ejecutar la tarea.

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

El **elemento WakeToRun** se define mediante el [**tipo complejo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Cuando el Programador de tareas reactiva el equipo para ejecutar una tarea, la pantalla puede permanecer desactivada aunque el equipo ya no esté en modo de suspensión o hibernación. La pantalla se activará cuando Windows Vista detecte que un usuario ha vuelto a usar el equipo.

Para el desarrollo de C++, [**vea WakeToRun Property of ITaskSettings ( Propiedad WakeToRun de ITaskSettings).**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun)

Para el desarrollo de scripts, [**vea TaskSettings.WakeToRun.**](tasksettings-waketorun.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





