---
title: Tipo complejo SystemPropertiesType
description: Define la información que identifica el proveedor y cómo se ha habilitado, el evento, el canal en el que se escribió el evento y la información del sistema, como los IDs de proceso y subproceso.
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- Registro de eventos de tipo complejo SystemPropertiesType
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f7391362938502f0c307faab4d7b9166633647b093e5154b3aa56512c6ee4e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620245"
---
# <a name="systempropertiestype-complex-type"></a>Tipo complejo SystemPropertiesType

Define la información que identifica el proveedor y cómo se ha habilitado, el evento, el canal en el que se escribió el evento y la información del sistema, como los IDs de proceso y subproceso.

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
| [**Correlación**](eventschema-correlation-systempropertiestype-element.md)     |                                                             | Identificadores de actividad que los consumidores pueden usar para agrupar eventos relacionados.<br/>                                                                                                                                                                                                                                                 |
| [**Eventid**](eventschema-eventid-systempropertiestype-element.md)             |                                                             | Identificador que el proveedor usó para identificar el evento.<br/>                                                                                                                                                                                                                                                                      |
| [**EventRecordID**](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | Número de registro asignado al evento cuando se registró.<br/>                                                                                                                                                                                                                                                                       |
| [**Ejecución**](eventschema-execution-systempropertiestype-element.md)         |                                                             | Contiene información sobre el proceso y el subproceso que registró el evento.<br/>                                                                                                                                                                                                                                                          |
| [**Palabras clave**](eventschema-keywords-systempropertiestype-element.md)           | [**HexInt64Type**](eventschema-hexint64type-simpletype.md) | Máscara de bits de las palabras clave definidas en el evento . Las palabras clave se usan para clasificar tipos de eventos (por ejemplo, eventos asociados a la lectura de datos).<br/>                                                                                                                                                                                 |
| [**Nivel**](eventschema-level-systempropertiestype-element.md)                 | unsignedByte                                                | Nivel de gravedad definido en el evento.<br/>                                                                                                                                                                                                                                                                                          |
| [**Código de operación**](eventschema-opcode-systempropertiestype-element.md)               | unsignedByte                                                | Código de operación definido en el evento. La tarea y el código de operación se usan de forma típica para identificar la ubicación en la aplicación desde la que se registró el evento.<br/>                                                                                                                                                                                  |
| [**Proveedor**](eventschema-provider-systempropertiestype-element.md)           |                                                             | Identifica el proveedor que registró el evento. Los **atributos Name** y **Guid** se incluyen si el proveedor usó un manifiesto de instrumentación para definir sus eventos; De lo contrario, **el atributo EventSourceName** se incluye si un proveedor de eventos heredado (mediante la API [de](/windows/desktop/EventLog/event-logging) registro de eventos) registró el evento.<br/> |
| [**Seguridad**](eventschema-security-systempropertiestype-element.md)           |                                                             | Identifica el usuario que registró el evento.<br/>                                                                                                                                                                                                                                                                                        |
| [**Tarea**](eventschema-task-systempropertiestype-element.md)                   | unsignedShort                                               | Tarea definida en el evento . La tarea y el código de operación se usan normalmente para identificar la ubicación en la aplicación desde la que se registró el evento.<br/>                                                                                                                                                                                    |
| [**TimeCreated**](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | Marca de tiempo que identifica cuándo se registró el evento. La marca de tiempo incluirá el atributo **SystemTime** o **el atributo RawTime.**<br/>                                                                                                                                                                           |
| [**Versión**](schema-version-systempropertiestype-element.md)                  | unsignedByte                                                | Número de versión de la definición del evento.<br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a>Atributos



| Nombre              | Tipo                                                | Descripción                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de actividad        | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificador único global que identifica la actividad actual. Los eventos que se publican con este identificador forman parte de la misma actividad.<br/>                                                                                                                                         |
| EventSourceName   | string                                              | Nombre del origen del evento que publicó el evento (si el origen del evento es de la API de registro de eventos [heredada).](/windows/desktop/EventLog/event-logging)<br/>                                                                                                                                                      |
| Guid              | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificador único global que identifica de forma única el proveedor.<br/>                                                                                                                                                                                                                        |
| KernelTime        | unsignedInt                                         | Tiempo de ejecución transcurrido para instrucciones en modo kernel, en unidades de tiempo de CPU. Si usa una sesión privada de ETW, use el valor del miembro ProcessorTime en su lugar. Solo está disponible para los eventos registrados en un archivo de registro de seguimiento de eventos (archivo .etl).<br/>                                               |
| Nombre              | anyURI                                              | Nombre del proveedor.<br/>                                                                                                                                                                                                                                                                    |
| ProcessID         | unsignedInt                                         | Identifica el proceso que ha generado el evento.<br/>                                                                                                                                                                                                                                             |
| ProcessorID       | unsignedByte                                        | Número de identificación del procesador que procesó el evento. Solo está disponible para los eventos registrados en un archivo de registro de seguimiento de eventos (archivo .etl).<br/>                                                                                                                                             |
| ProcessorTime     | unsignedInt                                         | Para las sesiones privadas de ETW, el tiempo de ejecución transcurrido para las instrucciones de modo de usuario, en los tics de CPU. Solo está disponible para los eventos registrados en un archivo de registro de seguimiento de eventos (archivo .etl).<br/>                                                                                                                    |
| Calificadores        | **unsignedShort**                                   | Un proveedor heredado usa un número de 32 bits para identificar sus eventos. Si un proveedor heredado registra el evento, el valor del elemento **EventID** contiene los 16 bits de orden inferior del identificador de evento y el atributo **Qualifier** contiene los 16 bits de orden superior del identificador de evento.<br/> |
| RawTime           | unsignedLong                                        | Valor de marca de tiempo sin procesar; el formato de la marca de tiempo depende del origen de hora utilizado para recopilar el seguimiento. La marca de tiempo sin procesar ofrece mayor precisión que la hora del sistema. La salida del evento representado solo contendrá tiempo sin procesar si usa TraceRpt.exe con el modificador -rts.<br/>                 |
| RelatedActivityID | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificador único global que identifica la actividad a la que se ha transferido el control. A continuación, los eventos relacionados tendrían este identificador como identificador activityID.<br/>                                                                                                            |
| SessionID         | unsignedInt                                         | Número de identificación de la sesión de Terminal Server en la que ocurrió el evento. Solo está disponible para los eventos registrados en un archivo de registro de seguimiento de eventos (archivo .etl).<br/>                                                                                                                            |
| SystemTime        | dateTime                                            | Hora del sistema del momento en que se registró el evento.<br/>                                                                                                                                                                                                                                                |
| ThreadID          | unsignedInt                                         | Identifica el subproceso que ha generado el evento.<br/>                                                                                                                                                                                                                                              |
| UserID            | string                                              | Identificador de seguridad (SID) del usuario en forma de cadena.<br/>                                                                                                                                                                                                                                    |
| UserTime          | unsignedInt                                         | Tiempo de ejecución transcurrido para instrucciones en modo de usuario, en unidades de tiempo de CPU. Si usa una sesión privada de ETW, use el valor del miembro ProcessorTime en su lugar. Solo está disponible para los eventos registrados en un archivo de registro de seguimiento de eventos (archivo .etl).<br/>                                                 |



## <a name="remarks"></a>Comentarios

De forma predeterminada, el evento contiene el nombre de dominio completo (FQDN) de un equipo. Para usar el nombre NETBIOS en lugar del FQDN, debe crear un valor del Registro DWORD denominado CompatFlags bajo la siguiente clave del Registro y establecer el valor de CompatFlags en 0x2.

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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

