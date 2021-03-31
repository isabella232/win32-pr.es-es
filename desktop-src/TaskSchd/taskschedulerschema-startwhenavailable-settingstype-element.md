---
title: Elemento StartWhenAvailable (settingsType)
description: Especifica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- Programador de tareas del elemento StartWhenAvailable
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d86f6f6e75457d08e10ef40d728eaf3e3b00aa7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996086"
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

El elemento **StartWhenAvailable** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Esta propiedad solo se aplica a las tareas con tiempo.

Para el desarrollo de C++, consulte la [**propiedad StartWhenAvailable de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).

Para el desarrollo de scripts, vea [**TaskSettings. StartWhenAvailable**](tasksettings-startwhenavailable.md).

## <a name="examples"></a>Ejemplos

En el código XML siguiente se define un elemento de configuración que permite al Programador de tareas iniciar la tarea cuando está disponible.


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
</Settings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





