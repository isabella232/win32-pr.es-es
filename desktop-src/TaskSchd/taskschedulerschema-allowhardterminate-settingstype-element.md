---
title: Elemento AllowHardTerminate (settingsType)
description: Especifica que la tarea se puede finalizar mediante TerminateProcess.
ms.assetid: 093a3cc6-d3e1-48e3-bc9e-0b15df2a54de
keywords:
- Elemento AllowHardTerminate (settingsType) Programador de tareas
- Elemento AllowHardTerminate Programador de tareas
topic_type:
- apiref
api_name:
- AllowHardTerminate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d7a143dfb0024cced8a67595e17b12fba9d037b335b425272e1ad2a7999e0b11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010925"
---
# <a name="allowhardterminate-settingstype-element"></a>Elemento AllowHardTerminate (settingsType)

Especifica que la tarea se puede finalizar mediante TerminateProcess.

``` syntax
<xs:element name="AllowHardTerminate"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

El **elemento AllowHardTerminate** se define mediante el [**tipo complejo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                 | Descripción                                                                        |
|-------------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, vea [**la propiedad AllowHardTerminate de ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate)

Para el desarrollo de scripts, [**vea TaskSettings.AllowHardTerminate.**](tasksettings-allowhardterminate.md)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que permite la terminación de forma automática, vea Ejemplo de desencadenador [de tiempo (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





