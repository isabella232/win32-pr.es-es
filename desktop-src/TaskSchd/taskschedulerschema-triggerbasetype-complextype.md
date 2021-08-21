---
title: tipo complejo triggerBaseType
description: Define el atributo, los elementos secundarios base y la información de secuenciación para todos los tipos complejos de desencadenador.
ms.assetid: 1a2d004a-6f52-42b7-b0d0-ace8d27e9166
keywords:
- tipo complejo triggerBaseType Programador de tareas
topic_type:
- apiref
api_name:
- triggerBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21eed68ff260d199a46adabc0e560533658c6cc1398d00f9507b80b40fb69955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611016"
---
# <a name="triggerbasetype-complex-type"></a>tipo complejo triggerBaseType

Define el atributo, los elementos secundarios base y la información de secuenciación para todos los tipos complejos de desencadenador.

``` syntax
<xs:complexType name="triggerBaseType"
    abstract="true"
>
    <xs:sequence>
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="EndBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Repetition"
            type="repetitionType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                      | Tipo                                                                     | Descripción                                                                                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**habilitado**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Especifica que el desencadenador está habilitado.<br/>                                                                      |
| [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Fecha y hora en que se desactiva el desencadenador.<br/>                                                          |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Especifica el intervalo en el que el desencadenador puede iniciar la tarea.<br/>                                                 |
| [**Repetición**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Especifica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez que se activa el desencadenador.<br/> |
| [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Fecha y hora en que se activa el desencadenador.<br/>                                                            |



## <a name="attributes"></a>Atributos



| Nombre | Tipo | Descripción                           |
|------|------|---------------------------------------|
| id   | ID   | Identificador del desencadenador.<br/> |



## <a name="remarks"></a>Observaciones

Los tipos complejos de desencadenador incluyen lo siguiente.

-   [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)
-   [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)
-   [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)
-   [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)
-   [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)
-   [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md)
-   [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





