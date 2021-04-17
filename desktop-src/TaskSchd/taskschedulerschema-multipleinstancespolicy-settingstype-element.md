---
title: Elemento MultipleInstancesPolicy (settingsType)
description: Especifica la Directiva que define el modo en que el Programador de tareas se encarga de varias instancias de la tarea.
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- Programador de tareas del elemento MultipleInstancesPolicy
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5bcbbd26880f1ccced3e71b44dc93993d20f4a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676827"
---
# <a name="multipleinstancespolicy-settingstype-element"></a>Elemento MultipleInstancesPolicy (settingsType)

Especifica la Directiva que define el modo en que el Programador de tareas se encarga de varias instancias de la tarea.

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

El elemento **MultipleInstancesPolicy** se define mediante el tipo simple [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, consulte la [**propiedad MultipleInstances de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).

Para el desarrollo de scripts, vea [**TaskSettings. MultipleInstances**](tasksettings-multipleinstances.md).

### <a name="restricted-values"></a>Valores restringidos

Este elemento está restringido a los valores siguientes.

-   Parallel: inicia una nueva instancia mientras se está ejecutando una instancia existente.
-   Queue: inicia una nueva instancia de Task una vez completadas todas las demás instancias de la tarea.
-   IgnoreNew: valor predeterminado. No inicia una nueva instancia de si se está ejecutando una instancia existente de la tarea.
-   StopExisting: detiene una instancia existente de la tarea antes de iniciar una nueva instancia.

## <a name="examples"></a>Ejemplos

En el código XML siguiente se define un elemento de configuración que permite que varias instancias de la tarea se ejecuten en paralelo.


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
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

 

 





