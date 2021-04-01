---
title: Tipo simple de multipleInstancesPolicyType
description: Define las constantes de directiva de instancia para el elemento MultipleInstancesPolicy (settingsType).
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- Programador de tareas de tipo simple multipleInstancesPolicyType
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29a3523ef16224836ada474fb32265084453479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996607"
---
# <a name="multipleinstancespolicytype-simple-type"></a>Tipo simple de multipleInstancesPolicyType

Define las constantes de directiva de instancia para el elemento [**MultipleInstancesPolicy (settingsType)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) .

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

El tipo simple **multipleInstancesPolicyType** define los siguientes valores.



| Value        | Descripción                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| Paralelo     | Inicia una nueva instancia mientras se está ejecutando una instancia existente.<br/>                           |
| Cola        | Inicia una nueva instancia de la tarea después de que todas las demás instancias de la tarea se hayan completado.<br/>      |
| IgnoreNew    | Predeterminada. No inicia una nueva instancia si se está ejecutando una instancia existente de la tarea.<br/> |
| StopExisting | Detiene una instancia existente de la tarea antes de iniciar una nueva instancia.<br/>                |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos simples de esquema de Programador de tareas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





