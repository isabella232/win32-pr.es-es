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
# <a name="systempropertiestype-complex-type"></a><span data-ttu-id="048fc-104">Tipo complejo de SystemPropertiesType</span><span class="sxs-lookup"><span data-stu-id="048fc-104">SystemPropertiesType Complex Type</span></span>

<span data-ttu-id="048fc-105">Define la información que identifica al proveedor y cómo se habilitó, el evento, el canal en el que se escribió el evento e información del sistema, como los identificadores de proceso y de subproceso.</span><span class="sxs-lookup"><span data-stu-id="048fc-105">Defines the information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="048fc-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="048fc-106">Child elements</span></span>



| <span data-ttu-id="048fc-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="048fc-107">Element</span></span>                                                                         | <span data-ttu-id="048fc-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="048fc-108">Type</span></span>                                                        | <span data-ttu-id="048fc-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="048fc-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="048fc-110">**Channel**</span><span class="sxs-lookup"><span data-stu-id="048fc-110">**Channel**</span></span>](eventschema-channel-systempropertiestype-element.md)             | <span data-ttu-id="048fc-111">anyURI</span><span class="sxs-lookup"><span data-stu-id="048fc-111">anyURI</span></span>                                                      | <span data-ttu-id="048fc-112">Canal en el que se registró el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-112">The channel to which the event was logged.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="048fc-113">**Computer**</span><span class="sxs-lookup"><span data-stu-id="048fc-113">**Computer**</span></span>](eventschema-computer-systempropertiestype-element.md)           | <span data-ttu-id="048fc-114">string</span><span class="sxs-lookup"><span data-stu-id="048fc-114">string</span></span>                                                      | <span data-ttu-id="048fc-115">nombre del equipo en el que se produjo el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-115">The name of the computer on which the event occurred.</span></span><br/>                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="048fc-116">**Relación**</span><span class="sxs-lookup"><span data-stu-id="048fc-116">**Correlation**</span></span>](eventschema-correlation-systempropertiestype-element.md)     |                                                             | <span data-ttu-id="048fc-117">Los identificadores de actividad que los consumidores pueden usar para agrupar eventos relacionados.</span><span class="sxs-lookup"><span data-stu-id="048fc-117">The activity identifiers that consumers can use to group related events together.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="048fc-118">**EventId**</span><span class="sxs-lookup"><span data-stu-id="048fc-118">**EventID**</span></span>](eventschema-eventid-systempropertiestype-element.md)             |                                                             | <span data-ttu-id="048fc-119">Identificador que el proveedor usó para identificar el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-119">The identifier that the provider used to identify the event.</span></span><br/>                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="048fc-120">**EventRecordID**</span><span class="sxs-lookup"><span data-stu-id="048fc-120">**EventRecordID**</span></span>](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | <span data-ttu-id="048fc-121">Número de registro asignado al evento cuando se registró.</span><span class="sxs-lookup"><span data-stu-id="048fc-121">The record number assigned to the event when it was logged.</span></span><br/>                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="048fc-122">**Ejecución**</span><span class="sxs-lookup"><span data-stu-id="048fc-122">**Execution**</span></span>](eventschema-execution-systempropertiestype-element.md)         |                                                             | <span data-ttu-id="048fc-123">Contiene información sobre el proceso y el subproceso que registró el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-123">Contains information about the process and thread that logged the event.</span></span><br/>                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="048fc-124">**Palabras clave**</span><span class="sxs-lookup"><span data-stu-id="048fc-124">**Keywords**</span></span>](eventschema-keywords-systempropertiestype-element.md)           | [<span data-ttu-id="048fc-125">**HexInt64Type**</span><span class="sxs-lookup"><span data-stu-id="048fc-125">**HexInt64Type**</span></span>](eventschema-hexint64type-simpletype.md) | <span data-ttu-id="048fc-126">Máscara de máscara de las palabras clave definidas en el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-126">A bitmask of the keywords defined in the event.</span></span> <span data-ttu-id="048fc-127">Las palabras clave se usan para clasificar los tipos de eventos (por ejemplo, los eventos asociados a la lectura de datos).</span><span class="sxs-lookup"><span data-stu-id="048fc-127">Keywords are used to classify types of events (for example, events associated with reading data).</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="048fc-128">**Dosis**</span><span class="sxs-lookup"><span data-stu-id="048fc-128">**Level**</span></span>](eventschema-level-systempropertiestype-element.md)                 | <span data-ttu-id="048fc-129">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="048fc-129">unsignedByte</span></span>                                                | <span data-ttu-id="048fc-130">Nivel de gravedad definido en el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-130">The severity level defined in the event.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="048fc-131">**Código de operación**</span><span class="sxs-lookup"><span data-stu-id="048fc-131">**Opcode**</span></span>](eventschema-opcode-systempropertiestype-element.md)               | <span data-ttu-id="048fc-132">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="048fc-132">unsignedByte</span></span>                                                | <span data-ttu-id="048fc-133">Código de operación definido en el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-133">The opcode defined in the event.</span></span> <span data-ttu-id="048fc-134">La tarea y el código de operación se typcially usar para identificar la ubicación en la aplicación desde donde se registró el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-134">Task and opcode are typcially used to identify the location in the application from where the event was logged.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="048fc-135">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="048fc-135">**Provider**</span></span>](eventschema-provider-systempropertiestype-element.md)           |                                                             | <span data-ttu-id="048fc-136">Identifica el proveedor que registró el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-136">Identifies the provider that logged the event.</span></span> <span data-ttu-id="048fc-137">Los atributos **Name** y **GUID** se incluyen si el proveedor utiliza un manifiesto de instrumentación para definir sus eventos; de lo contrario, el atributo **EventSourceName** se incluye si un proveedor de eventos heredado (mediante la API de [registro de eventos](/windows/desktop/EventLog/event-logging) ) registró el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-137">The **Name** and **Guid** attributes are included if the provider used an instrumentation manifest to define its events; otherwise, the **EventSourceName** attribute is included if a legacy event provider (using the [Event Logging](/windows/desktop/EventLog/event-logging) API) logged the event.</span></span><br/> |
| [<span data-ttu-id="048fc-138">**Seguridad**</span><span class="sxs-lookup"><span data-stu-id="048fc-138">**Security**</span></span>](eventschema-security-systempropertiestype-element.md)           |                                                             | <span data-ttu-id="048fc-139">Identifica el usuario que registró el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-139">Identifies the user that logged the event.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="048fc-140">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="048fc-140">**Task**</span></span>](eventschema-task-systempropertiestype-element.md)                   | <span data-ttu-id="048fc-141">unsignedShort</span><span class="sxs-lookup"><span data-stu-id="048fc-141">unsignedShort</span></span>                                               | <span data-ttu-id="048fc-142">Tarea definida en el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-142">The task defined in the event.</span></span> <span data-ttu-id="048fc-143">Task y OpCode se utilizan normalmente para identificar la ubicación en la aplicación desde donde se registró el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-143">Task and opcode are typically used to identify the location in the application from where the event was logged.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="048fc-144">**TimeCreated**</span><span class="sxs-lookup"><span data-stu-id="048fc-144">**TimeCreated**</span></span>](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | <span data-ttu-id="048fc-145">Marca de tiempo que identifica Cuándo se registró el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-145">The time stamp that identifies when the event was logged.</span></span> <span data-ttu-id="048fc-146">La marca de tiempo incluirá el atributo **SystemTime** o el atributo **RawTime** .</span><span class="sxs-lookup"><span data-stu-id="048fc-146">The time stamp will include either the **SystemTime** attribute or the **RawTime** attribute.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="048fc-147">**Versión**</span><span class="sxs-lookup"><span data-stu-id="048fc-147">**Version**</span></span>](schema-version-systempropertiestype-element.md)                  | <span data-ttu-id="048fc-148">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="048fc-148">unsignedByte</span></span>                                                | <span data-ttu-id="048fc-149">Número de versión de la definición del evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-149">The version number of the event's definition.</span></span><br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a><span data-ttu-id="048fc-150">Atributos</span><span class="sxs-lookup"><span data-stu-id="048fc-150">Attributes</span></span>



| <span data-ttu-id="048fc-151">Nombre</span><span class="sxs-lookup"><span data-stu-id="048fc-151">Name</span></span>              | <span data-ttu-id="048fc-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="048fc-152">Type</span></span>                                                | <span data-ttu-id="048fc-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="048fc-153">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="048fc-154">Identificador de actividad</span><span class="sxs-lookup"><span data-stu-id="048fc-154">ActivityID</span></span>        | [<span data-ttu-id="048fc-155">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="048fc-155">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="048fc-156">Identificador único global que identifica la actividad actual.</span><span class="sxs-lookup"><span data-stu-id="048fc-156">A globally unique identifier that identifies the current activity.</span></span> <span data-ttu-id="048fc-157">Los eventos que se publican con este identificador forman parte de la misma actividad.</span><span class="sxs-lookup"><span data-stu-id="048fc-157">The events that are published with this identifier are part of the same activity.</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="048fc-158">EventSourceName</span><span class="sxs-lookup"><span data-stu-id="048fc-158">EventSourceName</span></span>   | <span data-ttu-id="048fc-159">string</span><span class="sxs-lookup"><span data-stu-id="048fc-159">string</span></span>                                              | <span data-ttu-id="048fc-160">Nombre del origen de eventos que publicó el evento (si el origen del evento es de la API de [registro de eventos](/windows/desktop/EventLog/event-logging) heredada).</span><span class="sxs-lookup"><span data-stu-id="048fc-160">The name of the event source that published the event (if the event source is from the legacy [Event Logging](/windows/desktop/EventLog/event-logging) API).</span></span><br/>                                                                                                                                                      |
| <span data-ttu-id="048fc-161">Guid</span><span class="sxs-lookup"><span data-stu-id="048fc-161">Guid</span></span>              | [<span data-ttu-id="048fc-162">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="048fc-162">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="048fc-163">Identificador único global que identifica de forma única el proveedor.</span><span class="sxs-lookup"><span data-stu-id="048fc-163">The globally unique identifier that uniquely identifies the provider.</span></span><br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="048fc-164">KernelTime</span><span class="sxs-lookup"><span data-stu-id="048fc-164">KernelTime</span></span>        | <span data-ttu-id="048fc-165">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="048fc-165">unsignedInt</span></span>                                         | <span data-ttu-id="048fc-166">Tiempo de ejecución transcurrido para instrucciones en modo kernel, en unidades de tiempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="048fc-166">Elapsed execution time for kernel-mode instructions, in CPU time units.</span></span> <span data-ttu-id="048fc-167">Si usa una sesión privada de ETW, use el valor del miembro ProcessorTime en su lugar.</span><span class="sxs-lookup"><span data-stu-id="048fc-167">If you are using an ETW private session, use the value in the ProcessorTime member instead.</span></span> <span data-ttu-id="048fc-168">Solo está disponible para los eventos registrados en un archivo de registro de seguimiento de eventos (archivo. ETL).</span><span class="sxs-lookup"><span data-stu-id="048fc-168">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                               |
| <span data-ttu-id="048fc-169">Nombre</span><span class="sxs-lookup"><span data-stu-id="048fc-169">Name</span></span>              | <span data-ttu-id="048fc-170">anyURI</span><span class="sxs-lookup"><span data-stu-id="048fc-170">anyURI</span></span>                                              | <span data-ttu-id="048fc-171">Nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="048fc-171">The name of the provider.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="048fc-172">ProcessID</span><span class="sxs-lookup"><span data-stu-id="048fc-172">ProcessID</span></span>         | <span data-ttu-id="048fc-173">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="048fc-173">unsignedInt</span></span>                                         | <span data-ttu-id="048fc-174">Identifica el proceso que ha generado el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-174">Identifies the process that generated the event.</span></span><br/>                                                                                                                                                                                                                                             |
| <span data-ttu-id="048fc-175">ProcessorID</span><span class="sxs-lookup"><span data-stu-id="048fc-175">ProcessorID</span></span>       | <span data-ttu-id="048fc-176">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="048fc-176">unsignedByte</span></span>                                        | <span data-ttu-id="048fc-177">Número de identificación del procesador que procesó el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-177">The identification number for the processor that processed the event.</span></span> <span data-ttu-id="048fc-178">Solo está disponible para los eventos registrados en un archivo de registro de seguimiento de eventos (archivo. ETL).</span><span class="sxs-lookup"><span data-stu-id="048fc-178">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                                             |
| <span data-ttu-id="048fc-179">ProcessorTime</span><span class="sxs-lookup"><span data-stu-id="048fc-179">ProcessorTime</span></span>     | <span data-ttu-id="048fc-180">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="048fc-180">unsignedInt</span></span>                                         | <span data-ttu-id="048fc-181">En el caso de las sesiones privadas de ETW, el tiempo de ejecución transcurrido para instrucciones en modo de usuario, en TICs de CPU.</span><span class="sxs-lookup"><span data-stu-id="048fc-181">For ETW private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.</span></span> <span data-ttu-id="048fc-182">Solo está disponible para los eventos registrados en un archivo de registro de seguimiento de eventos (archivo. ETL).</span><span class="sxs-lookup"><span data-stu-id="048fc-182">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                    |
| <span data-ttu-id="048fc-183">Calificadores</span><span class="sxs-lookup"><span data-stu-id="048fc-183">Qualifiers</span></span>        | <span data-ttu-id="048fc-184">**unsignedShort**</span><span class="sxs-lookup"><span data-stu-id="048fc-184">**unsignedShort**</span></span>                                   | <span data-ttu-id="048fc-185">Un proveedor heredado utiliza un número de 32 bits para identificar sus eventos.</span><span class="sxs-lookup"><span data-stu-id="048fc-185">A legacy provider uses a 32-bit number to identify its events.</span></span> <span data-ttu-id="048fc-186">Si un proveedor heredado registra el evento, el valor del elemento **EventID** contiene los 16 bits de orden inferior del identificador de evento y el atributo **calificador** contiene los 16 bits de orden superior del identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-186">If the event is logged by a legacy provider, the value of **EventID** element contains the low-order 16 bits of the event identifier and the **Qualifier** attribute contains the high-order 16 bits of the event identifier.</span></span><br/> |
| <span data-ttu-id="048fc-187">RawTime</span><span class="sxs-lookup"><span data-stu-id="048fc-187">RawTime</span></span>           | <span data-ttu-id="048fc-188">unsignedLong</span><span class="sxs-lookup"><span data-stu-id="048fc-188">unsignedLong</span></span>                                        | <span data-ttu-id="048fc-189">Valor de marca de tiempo sin formato; el formato de la marca de tiempo depende del origen de hora usado para recopilar el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="048fc-189">The raw time stamp value; the format of the time stamp depends on the time source used to collect the trace.</span></span> <span data-ttu-id="048fc-190">La marca de tiempo sin formato ofrece una precisión mayor que la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="048fc-190">The raw time stamp offers higher precision than system time.</span></span> <span data-ttu-id="048fc-191">La salida del evento representado solo contendrá el tiempo sin formato si usa TraceRpt.exe con el modificador-RTS.</span><span class="sxs-lookup"><span data-stu-id="048fc-191">The rendered event output will only contain raw time if you use TraceRpt.exe with the -rts switch.</span></span><br/>                 |
| <span data-ttu-id="048fc-192">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="048fc-192">RelatedActivityID</span></span> | [<span data-ttu-id="048fc-193">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="048fc-193">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="048fc-194">Identificador único global que identifica la actividad a la que se transfirió el control.</span><span class="sxs-lookup"><span data-stu-id="048fc-194">A globally unique identifier that identifies the activity to which control was transferred to.</span></span> <span data-ttu-id="048fc-195">Los eventos relacionados tendrían este identificador como su identificador ActivityID.</span><span class="sxs-lookup"><span data-stu-id="048fc-195">The related events would then have this identifier as their ActivityID identifier.</span></span><br/>                                                                                                            |
| <span data-ttu-id="048fc-196">SessionID</span><span class="sxs-lookup"><span data-stu-id="048fc-196">SessionID</span></span>         | <span data-ttu-id="048fc-197">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="048fc-197">unsignedInt</span></span>                                         | <span data-ttu-id="048fc-198">Número de identificación de la sesión de Terminal Server en la que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-198">The identification number for the terminal server session in which the event occurred.</span></span> <span data-ttu-id="048fc-199">Solo está disponible para los eventos registrados en un archivo de registro de seguimiento de eventos (archivo. ETL).</span><span class="sxs-lookup"><span data-stu-id="048fc-199">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                            |
| <span data-ttu-id="048fc-200">SystemTime</span><span class="sxs-lookup"><span data-stu-id="048fc-200">SystemTime</span></span>        | <span data-ttu-id="048fc-201">dateTime</span><span class="sxs-lookup"><span data-stu-id="048fc-201">dateTime</span></span>                                            | <span data-ttu-id="048fc-202">Hora del sistema en la que se registró el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-202">The system time of when the event was logged.</span></span><br/>                                                                                                                                                                                                                                                |
| <span data-ttu-id="048fc-203">ThreadID</span><span class="sxs-lookup"><span data-stu-id="048fc-203">ThreadID</span></span>          | <span data-ttu-id="048fc-204">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="048fc-204">unsignedInt</span></span>                                         | <span data-ttu-id="048fc-205">Identifica el subproceso que ha generado el evento.</span><span class="sxs-lookup"><span data-stu-id="048fc-205">Identifies the thread that generated the event.</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="048fc-206">UserID</span><span class="sxs-lookup"><span data-stu-id="048fc-206">UserID</span></span>            | <span data-ttu-id="048fc-207">string</span><span class="sxs-lookup"><span data-stu-id="048fc-207">string</span></span>                                              | <span data-ttu-id="048fc-208">El identificador de seguridad (SID) del usuario en forma de cadena.</span><span class="sxs-lookup"><span data-stu-id="048fc-208">The security identifier (SID) of the user in string form.</span></span><br/>                                                                                                                                                                                                                                    |
| <span data-ttu-id="048fc-209">UserTime</span><span class="sxs-lookup"><span data-stu-id="048fc-209">UserTime</span></span>          | <span data-ttu-id="048fc-210">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="048fc-210">unsignedInt</span></span>                                         | <span data-ttu-id="048fc-211">Tiempo de ejecución transcurrido para instrucciones en modo de usuario, en unidades de tiempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="048fc-211">Elapsed execution time for user-mode instructions, in CPU time units.</span></span> <span data-ttu-id="048fc-212">Si usa una sesión privada de ETW, use el valor del miembro ProcessorTime en su lugar.</span><span class="sxs-lookup"><span data-stu-id="048fc-212">If you are using an ETW private session, use the value in the ProcessorTime member instead.</span></span> <span data-ttu-id="048fc-213">Solo está disponible para los eventos registrados en un archivo de registro de seguimiento de eventos (archivo. ETL).</span><span class="sxs-lookup"><span data-stu-id="048fc-213">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                 |



## <a name="remarks"></a><span data-ttu-id="048fc-214">Observaciones</span><span class="sxs-lookup"><span data-stu-id="048fc-214">Remarks</span></span>

<span data-ttu-id="048fc-215">De forma predeterminada, el evento contiene el nombre de dominio completo (FQDN) de un equipo.</span><span class="sxs-lookup"><span data-stu-id="048fc-215">By default, the event contains the fully qualified domain name (FQDN) of a computer.</span></span> <span data-ttu-id="048fc-216">Para usar el nombre de NETBIOS en lugar del FQDN, debe crear un valor de registro DWORD denominado CompatFlags en la siguiente clave del registro y establecer el valor de CompatFlags en 0x2.</span><span class="sxs-lookup"><span data-stu-id="048fc-216">To use the NETBIOS name rather than the FQDN, you must create a DWORD registry value named CompatFlags under the following registry key, and set the value of CompatFlags to 0x2.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               WINEVT
```

## <a name="requirements"></a><span data-ttu-id="048fc-217">Requisitos</span><span class="sxs-lookup"><span data-stu-id="048fc-217">Requirements</span></span>



| <span data-ttu-id="048fc-218">Requisito</span><span class="sxs-lookup"><span data-stu-id="048fc-218">Requirement</span></span> | <span data-ttu-id="048fc-219">Value</span><span class="sxs-lookup"><span data-stu-id="048fc-219">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="048fc-220">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="048fc-220">Minimum supported client</span></span><br/> | <span data-ttu-id="048fc-221">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="048fc-221">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="048fc-222">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="048fc-222">Minimum supported server</span></span><br/> | <span data-ttu-id="048fc-223">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="048fc-223">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

