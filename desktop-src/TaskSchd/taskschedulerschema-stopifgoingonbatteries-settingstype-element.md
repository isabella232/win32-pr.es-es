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
ms.openlocfilehash: 2e7de57cde928760c15dd671010880e824c8979f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968644"
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



## <a name="remarks"></a>Observaciones

El valor predeterminado de este elemento es False. Tenga en cuenta que el valor predeterminado ha cambiado con respecto a las versiones anteriores de Programador de tareas.

Para el desarrollo de scripting, esta configuración se especifica mediante la [**propiedad TaskSettings.StopIfGoingOnBatteries.**](tasksettings-stopifgoingonbatteries.md)

Para el desarrollo de C++, esta configuración se especifica mediante la [**propiedad ITaskSettings::StopIfGoingOnBatteries.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries)

## <a name="examples"></a>Ejemplos

El xml siguiente define un elemento de configuración que permite una terminación de la tarea de forma fija.


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
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

 

 





