---
title: Elemento RestartOnFailure (settingsType)
description: Especifica que el Programador de tareas intentará reiniciar la tarea si se produce un error en la tarea por cualquier motivo.
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- Elemento RestartOnFailure Programador de tareas
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bfe29be7dd329def41e8a6726f141a850eb2daecd05e05d6b5988f543f64864c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072445"
---
# <a name="restartonfailure-settingstype-element"></a>Elemento RestartOnFailure (settingsType)

Especifica que el Programador de tareas intentará reiniciar la tarea si se produce un error en la tarea por cualquier motivo.

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

El **elemento RestartOnFailure** se define mediante el [**tipo complejo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                              | Tipo         | Descripción                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [**Count**](taskschedulerschema-count-restarttype-element.md)       | unsignedByte | Especifica el número de veces que el Programador de tareas intentará reiniciar la tarea.<br/> |
| [**Intervalo**](taskschedulerschema-interval-restarttype-element.md) | duration     | Especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.<br/>                 |



## <a name="remarks"></a>Comentarios

Cuando una aplicación especifica la configuración de tareas, se accede a esta información a través de las propiedades [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) y [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) de la [**interfaz ITaskSettings.**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) Para el scripting, se tiene acceso a esta información a través de las propiedades [**TaskSettings.RestartCount**](tasksettings-restartcount.md) [**y TaskSettings.RestartInterval.**](tasksettings-restartinterval.md)

Ambos elementos secundarios deben establecerse para especificar cómo el Programador de tareas reinicia la tarea.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





