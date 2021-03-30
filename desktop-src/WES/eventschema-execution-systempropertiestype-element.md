---
title: Elemento Execution (SystemPropertiesType)
description: Contiene información sobre el proceso y el subproceso que registró el evento.
ms.assetid: 4d2feb0d-a3e6-479c-aa34-cd95a708add5
keywords:
- EventLog del elemento de ejecución
topic_type:
- apiref
api_name:
- Execution
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64137153ffb0f1ba9816f060f0d5af0a2c6ee8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801418"
---
# <a name="execution-systempropertiestype-element"></a>Elemento Execution (SystemPropertiesType)

Contiene información sobre el proceso y el subproceso que registró el evento.

``` syntax
<xs:element name="Execution">
    <xs:complexType>
        <xs:attribute name="ProcessID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ThreadID"
            type="unsignedInt"
            use="required"
         />
        <xs:attribute name="ProcessorID"
            type="unsignedByte"
            use="optional"
         />
        <xs:attribute name="SessionID"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="KernelTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="UserTime"
            type="unsignedInt"
            use="optional"
         />
        <xs:attribute name="ProcessorTime"
            type="unsignedInt"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

El elemento de **ejecución** se define mediante el tipo complejo de [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nombre          | Tipo         | Descripción                                                                                               |
|---------------|--------------|-----------------------------------------------------------------------------------------------------------|
| KernelTime    | unsignedInt  | Tiempo de ejecución transcurrido para instrucciones en modo kernel, en unidades de tiempo de CPU.<br/>                        |
| ProcessID     | unsignedInt  | Identifica el proceso que ha generado el evento.<br/>                                               |
| ProcessorID   | unsignedByte | Número de identificación del procesador que procesó el evento.<br/>                          |
| ProcessorTime | unsignedInt  | En el caso de las sesiones privadas de ETW, el tiempo de ejecución transcurrido para instrucciones en modo de usuario, en TICs de CPU.<br/> |
| SessionID     | unsignedInt  | Número de identificación de la sesión de Terminal Server en la que ocurrió el evento.<br/>         |
| ThreadID      | unsignedInt  | Identifica el subproceso que ha generado el evento.<br/>                                                |
| UserTime      | unsignedInt  | Tiempo de ejecución transcurrido para instrucciones en modo de usuario, en unidades de tiempo de CPU.<br/>                          |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Sistema (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





