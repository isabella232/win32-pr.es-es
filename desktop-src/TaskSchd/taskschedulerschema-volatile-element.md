---
title: Elemento Volatile
description: Indica si la tarea se deshabilita automáticamente cada vez que Windows inicio.
ms.assetid: E0298876-2A96-401D-B857-69758AF980E5
keywords:
- Elemento volatile Programador de tareas
topic_type:
- apiref
api_name:
- Volatile
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 496e95fe98ecb2890d19bde0b99e171ab20b045a47bf69840dd78f501bfbc309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872105"
---
# <a name="volatile-element"></a>Elemento Volatile

Indica si la tarea se deshabilita automáticamente cada vez que Windows inicio.

``` syntax
<xs:element name="Volatile"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
    default="false"
 />
```

El **elemento Volatile** se define mediante el tipo complejo [**settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de | Descripción                                                                        |
|-------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) |              | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Para la programación de C++, esta configuración inactiva se especifica mediante la [**propiedad ITaskSettings3::Volatile.**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>           |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





