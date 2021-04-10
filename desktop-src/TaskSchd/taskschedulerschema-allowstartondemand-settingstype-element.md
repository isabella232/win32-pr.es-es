---
title: Elemento AllowStartOnDemand (settingsType)
description: Especifica que la tarea se puede iniciar con el comando ejecutar o el menú contextual.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- Programador de tareas del elemento AllowStartOnDemand
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec396bf10efbd11024fe39e57bdf05025db0e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996089"
---
# <a name="allowstartondemand-settingstype-element"></a>Elemento AllowStartOnDemand (settingsType)

Especifica que la tarea se puede iniciar con el comando ejecutar o el menú contextual.

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

El elemento **AllowStartOnDemand** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Cuando este elemento se establece en true, la tarea se puede iniciar independientemente de cuando cualquier desencadenador inicie la tarea.

Para el desarrollo de C++, vea la [**propiedad AllowDemandStart de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).

Para el desarrollo de scripts, vea [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md).

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que permite el inicio de la demanda, vea [ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





