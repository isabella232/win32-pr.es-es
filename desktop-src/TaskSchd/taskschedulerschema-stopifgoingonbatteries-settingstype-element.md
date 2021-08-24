---
title: Elemento StopIfGoingOnBatteries (settingsType)
description: Especifica que la tarea se detendrán si el equipo va a usar baterías.
ms.assetid: 0d772dbb-a552-45ed-9dc0-7159f6ef12ed
keywords:
- Elemento StopIfGoingOnBatteries Programador de tareas
topic_type:
- apiref
api_name:
- StopIfGoingOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b92be11400d1dbb223115f11334e2a596e94e9df1fd018ce16e4a646c84825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516105"
---
# <a name="stopifgoingonbatteries-settingstype-element"></a>Elemento StopIfGoingOnBatteries (settingsType)

Especifica que la tarea se detendrán si el equipo va a usar baterías.

``` syntax
<xs:element name="StopIfGoingOnBatteries"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

El **elemento StopIfGoingOnBatteries** se define mediante el [**tipo complejo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Comentarios

El valor predeterminado para este elemento es False. Tenga en cuenta que el valor predeterminado ha cambiado con respecto a las versiones anteriores de Programador de tareas.

Para el desarrollo de scripting, esta configuración se especifica mediante la [**propiedad TaskSettings.StopIfGoingOnBatteries.**](tasksettings-stopifgoingonbatteries.md)

Para el desarrollo de C++, esta configuración se especifica mediante la [**propiedad ITaskSettings::StopIfGoingOnBatteries.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries)

## <a name="examples"></a>Ejemplos

El xml siguiente define un elemento de configuración que permite una terminación de la tarea.


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
</Settings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





