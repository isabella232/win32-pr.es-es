---
title: Elemento RunOnlyIfNetworkAvailable (settingsType)
description: Especifica que el Programador de tareas ejecutará la tarea solo cuando haya una red disponible.
ms.assetid: b7b804d3-b31a-4d70-9ba5-805a285e278e
keywords:
- Elemento RunOnlyIfNetworkAvailable Programador de tareas
topic_type:
- apiref
api_name:
- RunOnlyIfNetworkAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ff1e7c838c142e30b75eb4abb935c0de352d9f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891481"
---
# <a name="runonlyifnetworkavailable-settingstype-element"></a>Elemento RunOnlyIfNetworkAvailable (settingsType)

Especifica que el Programador de tareas ejecutará la tarea solo cuando haya una red disponible.

``` syntax
<xs:element name="RunOnlyIfNetworkAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

El **elemento RunOnlyIfNetworkAvailable** se define mediante el [**tipo complejo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, [**vea Propiedad RunOnlyIfNetworkAvailable de ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable)

Para el desarrollo de scripts, [**vea TaskSettings.RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md).

## <a name="examples"></a>Ejemplos

El xml siguiente define un elemento de configuración que permite que la tarea se inicie solo si hay una red disponible.


```XML
<Settings>
    <RunOnlyIfNetworkAvailable>true</RunOnlyIfNetworkAvailable>
</Settings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





