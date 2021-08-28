---
title: Elemento StartWhenAvailable (settingsType)
description: Especifica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- Elemento StartWhenAvailable Programador de tareas
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aa87fe438cb2916757e5ad9ecf88e08ce944eb6c71749c116afc75b253da6f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401765"
---
# <a name="startwhenavailable-settingstype-element"></a>Elemento StartWhenAvailable (settingsType)

Especifica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.

``` syntax
<xs:element name="StartWhenAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

El **elemento StartWhenAvailable** se define mediante el [**tipo complejo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Esta propiedad solo se aplica a las tareas con tiempo.

Para el desarrollo de C++, [**vea Propiedad StartWhenAvailable de ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable)

Para el desarrollo de scripts, [**vea TaskSettings.StartWhenAvailable.**](tasksettings-startwhenavailable.md)

## <a name="examples"></a>Ejemplos

El xml siguiente define un elemento de configuración que permite al Programador de tareas iniciar la tarea cuando está disponible.


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
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

 

 





