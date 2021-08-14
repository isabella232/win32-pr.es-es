---
title: Tipo simple multipleInstancesPolicyType
description: Define las constantes de directiva de instancia para el elemento MultipleInstancesPolicy (settingsType).
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- Tipo simple multipleInstancesPolicyType Programador de tareas
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e8e847e268486e58bc36bd1bcf9f454b2d8af7b7664d0372613c40c818f932f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758515"
---
# <a name="multipleinstancespolicytype-simple-type"></a>Tipo simple multipleInstancesPolicyType

Define las constantes de directiva de instancia [**para el elemento MultipleInstancesPolicy (settingsType).**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

``` syntax
<xs:simpleType name="multipleInstancesPolicyType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="Parallel"
         />
        <xs:enumeration
            value="Queue"
         />
        <xs:enumeration
            value="IgnoreNew"
         />
        <xs:enumeration
            value="StopExisting"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeración

El **tipo simple multipleInstancesPolicyType** define los valores siguientes.



| Valor        | Descripción                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| Paralelo     | Inicia una nueva instancia mientras se ejecuta una instancia existente.<br/>                           |
| Cola        | Inicia una nueva instancia de la tarea una vez completadas todas las demás instancias de la tarea.<br/>      |
| IgnoreNew    | Predeterminada. No inicia una nueva instancia si se está ejecutando una instancia existente de la tarea.<br/> |
| StopExisting | Detiene una instancia existente de la tarea antes de iniciar la nueva instancia.<br/>                |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema simple](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





