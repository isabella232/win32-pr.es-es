---
title: Elemento WakeToRun (settingsType)
description: Especifica que Programador de tareas reactivará el equipo cuando sea el momento de ejecutar la tarea.
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- Programador de tareas del elemento WakeToRun
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686188"
---
# <a name="waketorun-settingstype-element"></a>Elemento WakeToRun (settingsType)

Especifica que Programador de tareas reactivará el equipo cuando sea el momento de ejecutar la tarea.

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

El elemento **WakeToRun** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Cuando el servicio de Programador de tareas reactiva el equipo para ejecutar una tarea, es posible que la pantalla permanezca desactivada aunque el equipo ya no esté en modo de suspensión o hibernación. La pantalla se activará cuando Windows Vista detecte que un usuario ha vuelto a usar el equipo.

Para el desarrollo de C++, consulte la [**propiedad WakeToRun de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).

Para el desarrollo de scripts, vea [**TaskSettings. WakeToRun**](tasksettings-waketorun.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





