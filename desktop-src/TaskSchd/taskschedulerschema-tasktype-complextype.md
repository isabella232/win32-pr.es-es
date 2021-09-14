---
title: Tipo complejo taskType (Programador de tareas)
description: Define los elementos secundarios y la información de secuenciación para el elemento Task.
ms.assetid: 622b2bf4-c7e0-403c-bd6c-99b687c1d439
keywords:
- tipo complejo taskType Programador de tareas
topic_type:
- apiref
api_name:
- taskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e86174920c28614f6c871e3f0bb0bc322243009
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968612"
---
# <a name="tasktype-complex-type"></a>tipo complejo taskType

Define los elementos secundarios y la información de secuenciación para el [**elemento Task.**](taskschedulerschema-task-element.md)

``` syntax
<xs:complexType name="taskType">
    <xs:all>
        <xs:element name="RegistrationInfo"
            type="registrationInfoType"
            minOccurs="0"
         />
        <xs:element name="Triggers"
            type="triggersType"
            minOccurs="0"
         />
        <xs:element name="Settings"
            type="settingsType"
            minOccurs="0"
         />
        <xs:element name="Data"
            type="dataType"
            minOccurs="0"
         />
        <xs:element name="Principals"
            type="principalsType"
            minOccurs="0"
         />
        <xs:element name="Actions"
            type="actionsType"
         />
    </xs:all>
    <xs:attribute name="version"
        type="versionType"
        use="optional"
        fixed="1.3"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                           | Tipo                                                                                 | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**Acciones**](taskschedulerschema-actions-tasktype-element.md)                   | [**actionsType**](taskschedulerschema-actionstype-complextype.md)                   | Especifica las acciones realizadas por la tarea.<br/>                                                                             |
| [**Data**](taskschedulerschema-data-tasktype-element.md)                         | [**Datatype**](taskschedulerschema-datatype-complextype.md)                         | Especifica los datos de suma asociados a la tarea, pero el servicio Programador de tareas de otro modo.<br/>         |
| [**Entidades de seguridad**](taskschedulerschema-principals-tasktype-element.md)             | [**principalsType**](taskschedulerschema-principalstype-complextype.md)             | Especifica los contextos de seguridad que se pueden usar para ejecutar la tarea.<br/>                                                        |
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica información administrativa sobre la tarea, como el autor de la tarea y la fecha en que se registra la tarea.<br/> |
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md)                 | [**settingsType**](taskschedulerschema-settingstype-complextype.md)                 | Especifica la configuración que el Programador de tareas utiliza para realizar la tarea.<br/>                                                 |
| [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md)                 | [**triggersType**](taskschedulerschema-triggerstype-complextype.md)                 | Especifica los desencadenadores que inician la tarea.<br/>                                                                              |



## <a name="attributes"></a>Atributos



| Nombre    | Tipo                                                              | Descripción                                   |
|---------|-------------------------------------------------------------------|-----------------------------------------------|
| version | [**versionType**](taskschedulerschema-versiontype-simpletype.md) | Especifica la versión de la tarea.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas tipos complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





