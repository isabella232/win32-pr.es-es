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
ms.openlocfilehash: 8a8d93bcabd0e121c44f4a7212d11491624a08d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891532"
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



## <a name="remarks"></a>Observaciones

El valor predeterminado de este elemento es True.

Para el desarrollo de scripting, se tiene acceso a esta información a través de [**la propiedad TaskSettings.DisallowStartIfOnBatteries.**](tasksettings-disallowstartifonbatteries.md)

Para el desarrollo de C++, se tiene acceso a esta información a través de la propiedad [**ITaskSettings::D isallowStartIfOnBatteries.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries)

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





