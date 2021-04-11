---
title: Elemento RestartOnFailure (settingsType)
description: Especifica que el Programador de tareas intentará reiniciar la tarea si se produce un error en la tarea por cualquier motivo.
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- Programador de tareas del elemento RestartOnFailure
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4239d21362d589cae84252c728387b2a2b6159e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274554"
---
# <a name="restartonfailure-settingstype-element"></a>Elemento RestartOnFailure (settingsType)

Especifica que el Programador de tareas intentará reiniciar la tarea si se produce un error en la tarea por cualquier motivo.

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

El elemento **RestartOnFailure** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                              | Tipo         | Descripción                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [**Contabiliza**](taskschedulerschema-count-restarttype-element.md)       | unsignedByte | Especifica el número de veces que el Programador de tareas intentará reiniciar la tarea.<br/> |
| [**Interval**](taskschedulerschema-interval-restarttype-element.md) | duration     | Especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.<br/>                 |



## <a name="remarks"></a>Observaciones

Cuando una aplicación especifica la configuración de la tarea, se obtiene acceso a esta información a través de las propiedades [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) y [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) de la interfaz [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) . En el caso de scripting, se obtiene acceso a esta información a través de las propiedades [**TaskSettings. RestartCount**](tasksettings-restartcount.md) y [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md) .

Ambos elementos secundarios se deben establecer para especificar cómo el Programador de tareas reinicia la tarea.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





