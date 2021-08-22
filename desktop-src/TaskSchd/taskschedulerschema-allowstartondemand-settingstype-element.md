---
title: Elemento AllowStartOnDemand (settingsType)
description: Especifica que la tarea se puede iniciar mediante el comando Ejecutar o el menú Contextual.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- Elemento AllowStartOnDemand Programador de tareas
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be89197c4ae88188fc1d2a746c40d69e385edc7ba08aaf2d3bf29067ee5f4a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516995"
---
# <a name="allowstartondemand-settingstype-element"></a>Elemento AllowStartOnDemand (settingsType)

Especifica que la tarea se puede iniciar mediante el comando Ejecutar o el menú Contextual.

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

El **elemento AllowStartOnDemand** se define mediante el [**tipo complejo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Cuando este elemento se establece en True, la tarea se puede iniciar independientemente de cuando cualquier desencadenador inicia la tarea.

Para el desarrollo de C++, vea [**la propiedad AllowDemandStart de ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart)

Para el desarrollo de scripts, [**vea TaskSettings.AllowDemandStart.**](tasksettings-allowdemandstart.md)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que permite el inicio de la demanda, vea [Ejemplo de desencadenador de tiempo (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





