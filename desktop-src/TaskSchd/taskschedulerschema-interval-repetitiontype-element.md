---
title: Elemento Interval (repetitionType)
description: Especifica la cantidad de tiempo entre cada reinicio de la tarea.
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Programador de tareas de elemento Interval
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9720bc2257d4c0b45116089bfdd4113335fc6b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996157"
---
# <a name="interval-repetitiontype-element"></a>Elemento Interval (repetitionType)

Especifica la cantidad de tiempo entre cada reinicio de la tarea. El formato de esta cadena es P <days> DT <hours> H <minutes> M <seconds> S (por ejemplo, "PT5M" es de 5 minutos, "PT1H" es 1 hora y "PT20M" es de 20 minutos). El tiempo máximo permitido es de 31 días y el tiempo mínimo permitido es 1 minuto.

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento se define mediante el tipo complejo de [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                      | Derivado de                                                             | Descripción                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Repetición**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, el intervalo del patrón de repetición se especifica mediante la propiedad [**RepetitionPattern. Interval**](repetitionpattern-interval.md) .

En el desarrollo de C++, el intervalo del patrón de repetición se especifica mediante la propiedad [**IRepetitionPattern:: Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) .

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que usa un intervalo de repetición, vea [ejemplo de desencadenador diario (XML)](daily-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





