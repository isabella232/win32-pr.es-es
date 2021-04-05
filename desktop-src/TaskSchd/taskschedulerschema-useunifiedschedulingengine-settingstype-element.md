---
title: Elemento UseUnifiedSchedulingEngine (settingsType)
description: Especifica que se usará el motor de programación unificado para ejecutar esta tarea.
ms.assetid: 93436f14-1caf-4ec8-bf74-a198b7dcb27c
keywords:
- Programador de tareas del elemento UseUnifiedSchedulingEngine
topic_type:
- apiref
api_name:
- UseUnifiedSchedulingEngine
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a00798a46df3dfbb351dd8705b264192c38daff6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079156"
---
# <a name="useunifiedschedulingengine-settingstype-element"></a>Elemento UseUnifiedSchedulingEngine (settingsType)

Especifica que se usará el motor de programación unificado para ejecutar esta tarea.

``` syntax
<xs:element name="UseUnifiedSchedulingEngine"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

El elemento **UseUnifiedSchedulingEngine** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

La configuración predeterminada de este elemento es false.

En el desarrollo de C++, se tiene acceso a esta información a través de la propiedad [**ITaskSettings2:: UseUnifiedSchedulingEngine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) .

## <a name="examples"></a>Ejemplos

En el código XML siguiente se define un elemento de configuración que especifica que se usará el motor de programación unificado para ejecutar esta tarea.


```XML
<Settings>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
</Settings>
        
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





