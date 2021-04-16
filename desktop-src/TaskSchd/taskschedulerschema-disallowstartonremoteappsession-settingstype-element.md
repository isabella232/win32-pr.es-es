---
title: Elemento DisallowStartOnRemoteAppSession (settingsType)
description: Especifica que la tarea no se iniciará si se desencadena para ejecutarse en una sesión local de aplicaciones remotas integrada (raíl).
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- Programador de tareas del elemento DisallowStartOnRemoteAppSession
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685945"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a>Elemento DisallowStartOnRemoteAppSession (settingsType)

Especifica que la tarea no se iniciará si se desencadena para ejecutarse en una sesión local de aplicaciones remotas integrada (raíl).

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

El elemento **DisallowStartOnRemoteAppSession** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

La configuración predeterminada de este elemento es false.

En el desarrollo de C++, se obtiene acceso a esta información a través de la propiedad [**ITaskSettings2::D isallowstartonremoteappsession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) .

## <a name="examples"></a>Ejemplos

En el código XML siguiente se define un elemento de configuración que no permite que la tarea se inicie si la tarea se desencadena para ejecutarse en una sesión de raíl.


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
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

 

 





