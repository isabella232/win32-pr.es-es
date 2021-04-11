---
title: Elemento RunOnlyIfIdle (settingsType)
description: Especifica que la tarea se ejecuta solo cuando el equipo está en un estado de inactividad.
ms.assetid: 2ef3dd19-4d5c-4399-89b8-d737be4ef85e
keywords:
- Programador de tareas del elemento RunOnlyIfIdle
topic_type:
- apiref
api_name:
- RunOnlyIfIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c57663d763926d68e5a552ebaf66edff2172e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079633"
---
# <a name="runonlyifidle-settingstype-element"></a>Elemento RunOnlyIfIdle (settingsType)

Especifica que la tarea se ejecuta solo cuando el equipo está en un estado de inactividad.

``` syntax
<xs:element name="RunOnlyIfIdle"
    type="boolean"
 />
```

El elemento **RunOnlyIfIdle** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, consulte la [**propiedad RunOnlyIfIdle de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).

Para el desarrollo de scripts, vea [**TaskSettings. RunOnlyIfIdle**](tasksettings-runonlyifidle.md).

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

 

 





