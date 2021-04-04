---
title: Tipo complejo de SystemPropertiesType
description: Define la información que identifica al proveedor y cómo se habilitó, el evento, el canal en el que se escribió el evento e información del sistema, como los identificadores de proceso y de subproceso.
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- SystemPropertiesType tipo complejo EventLog
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce78a804c52ed492bd4b2a42332f8eda36b4c3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803193"
---
# <a name="systempropertiestype-complex-type"></a>Tipo complejo de SystemPropertiesType

Define la información que identifica al proveedor y cómo se habilitó, el evento, el canal en el que se escribió el evento e información del sistema, como los identificadores de proceso y de subproceso.

``` syntax
<xs:complexType name="SystemPropertiesType">
    <xs:sequence>
        <xs:element name="Provider">
            <xs:complexType>
                <xs:attribute name="Name"
                    type="anyURI"
                    use="optional"
                 />
                <xs:attribute name="Guid"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="EventSourceName"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="EventID">
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedShort"
                    >
                        <xs:attribute name="Qualifiers"
                            type="unsignedShort"
                            use="optional"
                         />
                    </xs:extension>
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Version"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="unsignedShort"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            type="HexInt64Type"
            minOccurs="0"
         />
        <xs:element name="TimeCreated"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="SystemTime"
                    type="dateTime"
                    use="optional"
                 />
                <xs:attribute name="RawTime"
                    type="unsignedLong"
                    use="optional"
                 />
            </xs:complexType>
            <xs:key name="uniqueAtt">
                <xs:selector
                    xpath="."
                 />
                <xs:field
                    xpath="@SystemTime|@RawTime"
                 />
            </xs:key>
        </xs:element>
        <xs:element name="EventRecordID"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedLong"
                     />
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Correlation"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ActivityID"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="RelatedActivityID"
                    type="GUIDType"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Execution"
            minOccurs="0"
        >
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
        <xs:element name="Channel"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="Computer"
            type="string"
         />
        <xs:element name="Security"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="UserID"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                         | Tipo                                                        | Descripción                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Channel**](eventschema-channel-systempropertiestype-element.md)             | anyURI                                                      | Canal en el que se registró el evento.<br/>                                                                                                                                                                                                                                                                                        |
| [**Computer**](eventschema-computer-systempropertiestype-element.md)           | string                                                      | nombre del equipo en el que se produjo el evento.<br/>                                                                                                                                                                                                                                                                             |
| [**Relación**](eventschema-correlation-systempropertiestype-element.md)     |                                                             | Los identificadores de actividad que los consumidores pueden usar para agrupar eventos relacionados.<br/>                                                                                                                                                                                                                                                 |
| [**EventId**](eventschema-eventid-systempropertiestype-element.md)             |                                                             | Identificador que el proveedor usó para identificar el evento.<br/>                                                                                                                                                                                                                                                                      |
| [**EventRecordID**](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | Número de registro asignado al evento cuando se registró.<br/>                                                                                                                                                                                                                                                                       |
| [**Ejecución**](eventschema-execution-systempropertiestype-element.md)         |                                                             | Contiene información sobre el proceso y el subproceso que registró el evento.<br/>                                                                                                                                                                                                                                                          |
| [**Palabras clave**](eventschema-keywords-systempropertiestype-element.md)           | [**HexInt64Type**](eventschema-hexint64type-simpletype.md) | Máscara de máscara de las palabras clave definidas en el evento. Las palabras clave se usan para clasificar los tipos de eventos (por ejemplo, los eventos asociados a la lectura de datos).<br/>                                                                                                                                                                                 |
| [**Dosis**](eventschema-level-systempropertiestype-element.md)                 | unsignedByte                                                | Nivel de gravedad definido en el evento.<br/>                                                                                                                                                                                                                                                                                          |
| [**Código de operación**](eventschema-opcode-systempropertiestype-element.md)               | unsignedByte                                                | Código de operación definido en el evento. La tarea y el código de operación se typcially usar para identificar la ubicación en la aplicación desde donde se registró el evento.<br/>                                                                                                                                                                                  |
| [**Proveedor**](eventschema-provider-systempropertiestype-element.md)           |                                                             | Identifica el proveedor que registró el evento. Los atributos **Name** y **GUID** se incluyen si el proveedor utiliza un manifiesto de instrumentación para definir sus eventos; de lo contrario, el atributo **EventSourceName** se incluye si un proveedor de eventos heredado (mediante la API de [registro de eventos](/windows/desktop/EventLog/event-logging) ) registró el evento.<br/> |
| [**Seguridad**](eventschema-security-systempropertiestype-element.md)           |                                                             | Identifica el usuario que registró el evento.<br/>                                                                                                                                                                                                                                                                                        |
| [**Tarea**](eventschema-task-systempropertiestype-element.md)                   | unsignedShort                                               | Tarea definida en el evento. Task y OpCode se utilizan normalmente para identificar la ubicación en la aplicación desde donde se registró el evento.<br/>                                                                                                                                                                                    |
| [**TimeCreated**](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | Marca de tiempo que identifica Cuándo se registró el evento. La marca de tiempo incluirá el atributo **SystemTime** o el atributo **RawTime** .<br/>                                                                                                                                                                           |
| [**Versión**](schema-version-systempropertiestype-element.md)                  | unsignedByte                                                | Número de versión de la definición del evento.<br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a>Atributos



| Nombre              | Tipo                                                | Descripción                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de actividad        | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificador único global que identifica la actividad actual. Los eventos que se publican con este identificador forman parte de la misma actividad.<br/>                                                                                                                                         |
| EventSourceName   | string                                              | Nombre del origen de eventos que publicó el evento (si el origen del evento es de la API de [registro de eventos](/windows/desktop/EventLog/event-logging) heredada).<br/>                                                                                                                                                      |
| Guid              | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificador único global que identifica de forma única el proveedor.<br/>                                                                                                                                                                                                                        |
| KernelTime        | unsignedInt                                         | Tiempo de ejecución transcurrido para instrucciones en modo kernel, en unidades de tiempo de CPU. Si usa una sesión privada de ETW, use el valor del miembro ProcessorTime en su lugar. Solo está disponible para los eventos registrados en un archivo de registro de seguimiento de eventos (archivo. ETL).<br/>                                               |
| Nombre              | anyURI                                              | Nombre del proveedor.<br/>                                                                                                                                                                                                                                                                    |
| ProcessID         | unsignedInt                                         | Identifica el proceso que ha generado el evento.<br/>                                                                                                                                                                                                                                             |
| ProcessorID       | unsignedByte                                        | Número de identificación del procesador que procesó el evento. Solo está disponible para los eventos registrados en un archivo de registro de seguimiento de eventos (archivo. ETL).<br/>                                                                                                                                             |
| ProcessorTime     | unsignedInt                                         | En el caso de las sesiones privadas de ETW, el tiempo de ejecución transcurrido para instrucciones en modo de usuario, en TICs de CPU. Solo está disponible para los eventos registrados en un archivo de registro de seguimiento de eventos (archivo. ETL).<br/>                                                                                                                    |
| Calificadores        | **unsignedShort**                                   | Un proveedor heredado utiliza un número de 32 bits para identificar sus eventos. Si un proveedor heredado registra el evento, el valor del elemento **EventID** contiene los 16 bits de orden inferior del identificador de evento y el atributo **calificador** contiene los 16 bits de orden superior del identificador de evento.<br/> |
| RawTime           | unsignedLong                                        | Valor de marca de tiempo sin formato; el formato de la marca de tiempo depende del origen de hora usado para recopilar el seguimiento. La marca de tiempo sin formato ofrece una precisión mayor que la hora del sistema. La salida del evento representado solo contendrá el tiempo sin formato si usa TraceRpt.exe con el modificador-RTS.<br/>                 |
| RelatedActivityID | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificador único global que identifica la actividad a la que se transfirió el control. Los eventos relacionados tendrían este identificador como su identificador ActivityID.<br/>                                                                                                            |
| SessionID         | unsignedInt                                         | Número de identificación de la sesión de Terminal Server en la que ocurrió el evento. Solo está disponible para los eventos registrados en un archivo de registro de seguimiento de eventos (archivo. ETL).<br/>                                                                                                                            |
| SystemTime        | dateTime                                            | Hora del sistema en la que se registró el evento.<br/>                                                                                                                                                                                                                                                |
| ThreadID          | unsignedInt                                         | Identifica el subproceso que ha generado el evento.<br/>                                                                                                                                                                                                                                              |
| UserID            | string                                              | El identificador de seguridad (SID) del usuario en forma de cadena.<br/>                                                                                                                                                                                                                                    |
| UserTime          | unsignedInt                                         | Tiempo de ejecución transcurrido para instrucciones en modo de usuario, en unidades de tiempo de CPU. Si usa una sesión privada de ETW, use el valor del miembro ProcessorTime en su lugar. Solo está disponible para los eventos registrados en un archivo de registro de seguimiento de eventos (archivo. ETL).<br/>                                                 |



## <a name="remarks"></a>Observaciones

De forma predeterminada, el evento contiene el nombre de dominio completo (FQDN) de un equipo. Para usar el nombre de NETBIOS en lugar del FQDN, debe crear un valor de registro DWORD denominado CompatFlags en la siguiente clave del registro y establecer el valor de CompatFlags en 0x2.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               WINEVT
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

