---
title: Elemento DisallowStartIfOnBatteries (settingsType)
description: Especifica que la tarea no se iniciará si el equipo se ejecuta con baterías.
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- Elemento DisallowStartIfOnBatteries Programador de tareas
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efd78b3e868c41431521b4c584a4044b9086362cf55d86466eb38ed75fcee148
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100045"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a>Elemento DisallowStartIfOnBatteries (settingsType)

Especifica que la tarea no se iniciará si el equipo se ejecuta con baterías.

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

El **elemento DisallowStartIfOnBatteries** se define mediante el [**tipo complejo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Comentarios

El valor predeterminado de este elemento es True.

Para el desarrollo de scripting, se tiene acceso a esta información a través de la [**propiedad TaskSettings.DisallowStartIfOnBatteries.**](tasksettings-disallowstartifonbatteries.md)

Para el desarrollo de C++, se accede a esta información a través de la propiedad [**ITaskSettings::D isallowStartIfOnBatteries.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries)

## <a name="examples"></a>Ejemplos

El xml siguiente define un elemento de configuración que no permite que la tarea se ejecute si el equipo se ejecuta con baterías.


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
</Settings>
        
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





