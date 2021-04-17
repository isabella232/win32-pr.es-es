---
title: Elemento Hidden (settingsType)
description: Especifica que la tarea no será visible de forma predeterminada en la interfaz de usuario.
ms.assetid: a08c270f-6d4e-4473-9538-c1e1e21b3b10
keywords:
- Programador de tareas de elementos ocultos
topic_type:
- apiref
api_name:
- Hidden
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef5ad479fe3107ed8fa79f0f86307254a9f33c4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676997"
---
# <a name="hidden-settingstype-element"></a>Elemento Hidden (settingsType)

Especifica que la tarea no será visible de forma predeterminada en la interfaz de usuario. Sin embargo, los administradores pueden invalidar esta configuración mediante el uso de un "modificador principal" que hace que todas las tareas sean visibles en la interfaz de usuario.

``` syntax
<xs:element name="Hidden"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

El elemento **Hidden** se define mediante el tipo complejo [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                    |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que usa Programador de tareas para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea [**Hidden (propiedad) de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).

Para el desarrollo de scripts, vea [**TaskSettings. Hidden**](tasksettings-hidden.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





