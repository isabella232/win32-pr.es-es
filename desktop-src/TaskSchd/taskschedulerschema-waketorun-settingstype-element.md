---
title: Elemento WakeToRun (settingsType)
description: Especifica que Programador de tareas reactivará el equipo cuando llegue el momento de ejecutar la tarea.
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
ms.openlocfilehash: 12d16f9f06685a427a8f3e7c4f2356dff0bc6415e50379ba752a4bc3a3fec8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872065"
---
# <a name="waketorun-settingstype-element"></a>Elemento WakeToRun (settingsType)

Especifica que Programador de tareas reactivará el equipo cuando llegue el momento de ejecutar la tarea.

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



## <a name="remarks"></a>Comentarios

Cuando el Programador de tareas reactiva el equipo para ejecutar una tarea, la pantalla puede permanecer desactivada aunque el equipo ya no esté en modo de suspensión o hibernación. La pantalla se activará cuando Windows Vista detecte que un usuario ha vuelto a usar el equipo.

Para el desarrollo de C++, [**vea WakeToRun Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).

Para el desarrollo de scripts, [**vea TaskSettings.WakeToRun**](tasksettings-waketorun.md).

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

 

 





