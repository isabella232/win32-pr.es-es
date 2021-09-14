---
title: Elemento Execution (SystemPropertiesType)
description: Contiene información sobre el proceso y el subproceso que registró el evento.
ms.assetid: 4d2feb0d-a3e6-479c-aa34-cd95a708add5
keywords:
- Elemento Execution EventLog
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374347"
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

El **tipo complejo SystemPropertiesType** define el elemento [**Execution.**](eventschema-systempropertiestype-complextype.md)

## <a name="attributes"></a>Atributos



| Nombre          | Tipo         | Descripción                                                                                               |
|---------------|--------------|-----------------------------------------------------------------------------------------------------------|
| KernelTime    | unsignedInt  | Tiempo de ejecución transcurrido para instrucciones en modo kernel, en unidades de tiempo de CPU.<br/>                        |
| ProcessID     | unsignedInt  | Identifica el proceso que ha generado el evento.<br/>                                               |
| ProcessorID   | unsignedByte | Número de identificación del procesador que procesó el evento.<br/>                          |
| ProcessorTime | unsignedInt  | Para las sesiones privadas de ETW, el tiempo de ejecución transcurrido para las instrucciones de modo de usuario, en los tics de CPU.<br/> |
| SessionID     | unsignedInt  | Número de identificación de la sesión de Terminal Server en la que ocurrió el evento.<br/>         |
| ThreadID      | unsignedInt  | Identifica el subproceso que ha generado el evento.<br/>                                                |
| UserTime      | unsignedInt  | Tiempo de ejecución transcurrido para instrucciones en modo de usuario, en unidades de tiempo de CPU.<br/>                          |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**System (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





