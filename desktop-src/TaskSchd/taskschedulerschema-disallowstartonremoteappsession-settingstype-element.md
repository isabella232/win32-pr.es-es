---
title: Elemento DisallowStartOnRemoteAppSession (settingsType)
description: Especifica que la tarea no se iniciará si se desencadena para ejecutarse en una sesión de Aplicaciones remotas integradas localmente (RAIL).
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- Elemento DisallowStartOnRemoteAppSession Programador de tareas
topic_type:
- apiref
api_name:
- DisallowStartOnRemoteAppSession
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11e3d0a367f2385e78cf1ec56231bbf7632fe05b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891524"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a>Elemento DisallowStartOnRemoteAppSession (settingsType)

Especifica que la tarea no se iniciará si se desencadena para ejecutarse en una sesión de Aplicaciones remotas integradas localmente (RAIL).

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

El **elemento DisallowStartOnRemoteAppSession** se define mediante el [**tipo complejo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

El valor predeterminado de este elemento es False.

Para el desarrollo de C++, se tiene acceso a esta información a través de la propiedad [**ITaskSettings2::D isallowStartOnRemoteAppSession.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession)

## <a name="examples"></a>Ejemplos

El xml siguiente define un elemento de configuración que no permite que la tarea se inicie si la tarea se desencadena para ejecutarse en una sesión RAIL.


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
</Settings>
        
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





