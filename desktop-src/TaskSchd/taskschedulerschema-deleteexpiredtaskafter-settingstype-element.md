---
title: Elemento DeleteExpiredTaskAfter (settingsType)
description: Especifica la cantidad de tiempo que el Programador de tareas esperará antes de eliminar la tarea después de que expire.
ms.assetid: 947a2fec-ceda-4726-aa1a-26fd1b258c1f
keywords:
- Elemento DeleteExpiredTaskAfter Programador de tareas
topic_type:
- apiref
api_name:
- DeleteExpiredTaskAfter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cee7cfc48f62b58caf63125404fb07209b399fc1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073405"
---
# <a name="deleteexpiredtaskafter-settingstype-element"></a>Elemento DeleteExpiredTaskAfter (settingsType)

Especifica la cantidad de tiempo que el Programador de tareas esperará antes de eliminar la tarea después de que expire. Si no se especifica ningún valor para este elemento, el Programador de tareas no eliminará la tarea. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos). Para obtener más información sobre el tipo de duración, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="DeleteExpiredTaskAfter"
    type="duration"
    minOccurs="0"
    default="PT0S"
 />
```

El **elemento DeleteExpiredTaskAfter** se define mediante el [**tipo complejo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, [**vea DeleteExpiredTaskAfter Property of ITaskSettings ( Propiedad DeleteExpiredTaskAfter de ITaskSettings).**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter)

Para el desarrollo de scripts, [**vea TaskSettings.DeleteExpiredTaskAfter.**](tasksettings-deleteexpiredtaskafter.md)

## <a name="examples"></a>Ejemplos

El siguiente XML define un elemento de configuración que elimina una tarea expirada después de una semana.


```XML
<Settings>
    <DeleteExpiredTaskAfter>PT7D</DeleteExpiredTaskAfter>
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

 

 





