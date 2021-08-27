---
title: Elemento MultipleInstancesPolicy (settingsType)
description: Especifica la directiva que define cómo el Programador de tareas trata con varias instancias de la tarea.
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- Elemento MultipleInstancesPolicy Programador de tareas
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d7728d2b39fbcbed060fce409f4d721b59ef5ca324cd141d7777a5ffed110a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072455"
---
# <a name="multipleinstancespolicy-settingstype-element"></a>Elemento MultipleInstancesPolicy (settingsType)

Especifica la directiva que define cómo el Programador de tareas trata con varias instancias de la tarea.

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

El **elemento MultipleInstancesPolicy** se define mediante el [**tipo simple multipleInstancesPolicyType.**](taskschedulerschema-multipleinstancespolicytype-simpletype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, [**vea Propiedad MultipleInstances de ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances)

Para el desarrollo de scripts, [**vea TaskSettings.MultipleInstances.**](tasksettings-multipleinstances.md)

### <a name="restricted-values"></a>Valores restringidos

Este elemento está restringido a los valores siguientes.

-   Paralelo: inicia una nueva instancia mientras se ejecuta una instancia existente.
-   Cola: inicia una nueva instancia de tarea una vez completadas todas las demás instancias de la tarea.
-   IgnoreNew: valor predeterminado. No inicia una nueva instancia si se está ejecutando una instancia existente de la tarea.
-   StopExisting: detiene una instancia existente de la tarea antes de iniciar una nueva instancia.

## <a name="examples"></a>Ejemplos

El siguiente XML define un elemento de configuración que permite que varias instancias de la tarea se ejecuten en paralelo.


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
</Settings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





