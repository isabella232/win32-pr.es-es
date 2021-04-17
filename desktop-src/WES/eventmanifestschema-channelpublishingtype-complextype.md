---
title: Tipo complejo de ChannelPublishingType
description: Define las propiedades de registro para la sesión que utiliza el canal. | Tipo complejo de ChannelPublishingType
ms.assetid: 4b3980f4-8652-4070-97c0-99cd1a9fc85a
keywords:
- ChannelPublishingType tipo complejo EventLog
topic_type:
- apiref
api_name:
- ChannelPublishingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af84685f25705f6f8c54a85b9befb6df791593ed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698148"
---
# <a name="channelpublishingtype-complex-type"></a><span data-ttu-id="cadbf-105">Tipo complejo de ChannelPublishingType</span><span class="sxs-lookup"><span data-stu-id="cadbf-105">ChannelPublishingType Complex Type</span></span>

<span data-ttu-id="cadbf-106">Define las propiedades de registro para la sesión que utiliza el canal.</span><span class="sxs-lookup"><span data-stu-id="cadbf-106">Defines the logging properties for the session that the channel uses.</span></span>

``` syntax
<xs:complexType name="ChannelPublishingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="level"
            type="UInt8Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="UInt64Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="controlGuid"
            type="GUIDType"
            minOccurs="0"
         />
        <xs:element name="bufferSize"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="minBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="fileMax"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="maxBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="latency"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="clockType"
            default="SystemTime"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="SystemTime"
                     />
                    <xs:enumeration
                        value="QPC"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="sidType"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="None"
                     />
                    <xs:enumeration
                        value="Publishing"
                     />
                </xs:restriction>
            </xs:simpleType>
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

## <a name="child-elements"></a><span data-ttu-id="cadbf-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cadbf-107">Child elements</span></span>



| <span data-ttu-id="cadbf-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="cadbf-108">Element</span></span>                                                                              | <span data-ttu-id="cadbf-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="cadbf-109">Type</span></span>                                                              | <span data-ttu-id="cadbf-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cadbf-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cadbf-111">**bufferSize**</span><span class="sxs-lookup"><span data-stu-id="cadbf-111">**bufferSize**</span></span>](eventmanifestschema-buffersize-channelpublishingtype-element.md)   | [<span data-ttu-id="cadbf-112">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="cadbf-112">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="cadbf-113">Cantidad de memoria, en kilobytes, que se va a asignar para cada búfer.</span><span class="sxs-lookup"><span data-stu-id="cadbf-113">The amount of memory, in kilobytes, to allocate for each buffer.</span></span> <span data-ttu-id="cadbf-114">Si espera una tasa de eventos relativamente baja, el tamaño del búfer debe establecerse en el tamaño de página de memoria.</span><span class="sxs-lookup"><span data-stu-id="cadbf-114">If you expect a relatively low event rate, the buffer size should be set to the memory page size.</span></span> <span data-ttu-id="cadbf-115">Si se espera que la tasa de eventos sea relativamente alta, debe especificar un tamaño de búfer mayor y aumentar el número máximo de búferes.</span><span class="sxs-lookup"><span data-stu-id="cadbf-115">If the event rate is expected to be relatively high, you should specify a larger buffer size and increase the maximum number of buffers.</span></span><br/> <span data-ttu-id="cadbf-116">El tamaño del búfer afecta a la velocidad a la que se rellenan los búferes y se deben vaciar.</span><span class="sxs-lookup"><span data-stu-id="cadbf-116">The buffer size affects the rate at which buffers fill and must be flushed.</span></span> <span data-ttu-id="cadbf-117">Aunque un tamaño de búfer pequeño requiere menos memoria, aumenta la velocidad a la que se deben vaciar los búferes.</span><span class="sxs-lookup"><span data-stu-id="cadbf-117">Although a small buffer size requires less memory, it increases the rate at which buffers must be flushed.</span></span><br/> <span data-ttu-id="cadbf-118">El tamaño de búfer predeterminado para los canales analíticos y de depuración es de 4 KB y para el administrador y operativo es de 64 KB.</span><span class="sxs-lookup"><span data-stu-id="cadbf-118">The default buffer size for Analytic and Debug channels is 4 KB and for Admin and Operational it is 64 KB.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="cadbf-119">**clockType**</span><span class="sxs-lookup"><span data-stu-id="cadbf-119">**clockType**</span></span>](eventmanifestschema-clocktype-channelpublishingtype-element.md)     |                                                                   | <span data-ttu-id="cadbf-120">Resolución del reloj que se va a usar al registrar la marca de tiempo para cada evento.</span><span class="sxs-lookup"><span data-stu-id="cadbf-120">The clock resolution to use when logging the time stamp for each event.</span></span> <span data-ttu-id="cadbf-121">Puede especificar SystemTime o QPC.</span><span class="sxs-lookup"><span data-stu-id="cadbf-121">You can specify SystemTime or QPC.</span></span> <span data-ttu-id="cadbf-122">SystemTime proporciona una marca de tiempo de baja resolución (10 milisegundos), pero es relativamente menos costosa de recuperar.</span><span class="sxs-lookup"><span data-stu-id="cadbf-122">SystemTime provides a low-resolution (10 milliseconds) time stamp but is comparatively less expensive to retrieve.</span></span> <span data-ttu-id="cadbf-123">El valor predeterminado es SystemTime.</span><span class="sxs-lookup"><span data-stu-id="cadbf-123">The default is SystemTime.</span></span> <br/> <span data-ttu-id="cadbf-124">El contador de rendimiento de consultas (QPC) proporciona una marca de tiempo de alta resolución (100 nanosegundos), pero es comparativamente más costosa de recuperar.</span><span class="sxs-lookup"><span data-stu-id="cadbf-124">Query performance counter (QPC) provides a high-resolution (100 nanoseconds) time stamp but is comparatively more expensive to retrieve.</span></span> <span data-ttu-id="cadbf-125">Debe QPC si tiene tasas de eventos altas o si el consumidor combina eventos de distintos búferes.</span><span class="sxs-lookup"><span data-stu-id="cadbf-125">You should QPC if you have high event rates or if the consumer merges events from different buffers.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="cadbf-126">**controlGuid**</span><span class="sxs-lookup"><span data-stu-id="cadbf-126">**controlGuid**</span></span>](eventmanifestschema-controlguid-channelpublishingtype-element.md) | [<span data-ttu-id="cadbf-127">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="cadbf-127">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="cadbf-128">Identifica el GUID de sesión para una sesión de ETW que contiene eventos WPP.</span><span class="sxs-lookup"><span data-stu-id="cadbf-128">Identifies the session GUID for an ETW session that contains WPP events.</span></span> <span data-ttu-id="cadbf-129">Esta configuración solo se permite para los canales de tipo Debug.</span><span class="sxs-lookup"><span data-stu-id="cadbf-129">This setting is only allowed for channels of type Debug.</span></span> <span data-ttu-id="cadbf-130">Estos canales no se pueden habilitar por completo con las palabras clave establecidas en cero (0x0000000000000000).</span><span class="sxs-lookup"><span data-stu-id="cadbf-130">These channels cannot be fully enabled with keywords set to zero (0x0000000000000000).</span></span> <span data-ttu-id="cadbf-131">Deben estar habilitadas con las palabras clave establecidas en 0xffffffffffffffff.</span><span class="sxs-lookup"><span data-stu-id="cadbf-131">They must be enabled with keywords set to 0xffffffffffffffff.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="cadbf-132">**fileMax**</span><span class="sxs-lookup"><span data-stu-id="cadbf-132">**fileMax**</span></span>                                                                          | [<span data-ttu-id="cadbf-133">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="cadbf-133">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="cadbf-134">El número máximo de veces que desea que el servicio cree un nuevo archivo de registro cuando el canal está habilitado (incluye el reinicio del equipo).</span><span class="sxs-lookup"><span data-stu-id="cadbf-134">The maximum number of times that you want the service to create a new log file when the channel is enabled (includes when the computer is restarted).</span></span> <span data-ttu-id="cadbf-135">Si el valor es 0 o 1, el servicio sobrescribirá el archivo de registro cada vez que se habilite el canal y se perderán los eventos anteriores.</span><span class="sxs-lookup"><span data-stu-id="cadbf-135">If the value is 0 or 1, the service will overwrite the log file each time the channel is enabled and the previous events will be lost.</span></span> <span data-ttu-id="cadbf-136">Si el valor es mayor que 1, el servicio creará un nuevo archivo de registro cada vez que se habilite el canal para conservar los eventos.</span><span class="sxs-lookup"><span data-stu-id="cadbf-136">If the value is greater than 1, the service will create a new log file each time the channel is enabled in order to preserve the events.</span></span> <span data-ttu-id="cadbf-137">El valor predeterminado es 1 y el máximo que se puede especificar es 16.</span><span class="sxs-lookup"><span data-stu-id="cadbf-137">The default is 1 and the maximum that you can specify is 16.</span></span><br/> <span data-ttu-id="cadbf-138">El servicio anexa un número decimal de tres dígitos entre 0 y fileMax 1 a cada nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="cadbf-138">The service appends a three digit decimal number between 0 and fileMax 1 to each file name.</span></span> <span data-ttu-id="cadbf-139">Por ejemplo, *filename*. ETL.xxx, donde xxx es el número decimal de tres dígitos.</span><span class="sxs-lookup"><span data-stu-id="cadbf-139">For example, *filename*.etl.xxx, where xxx is the three digit decimal number.</span></span> <span data-ttu-id="cadbf-140">Los archivos se encuentran en% WINDIR% \\ system32 \\ winevt \\ logs.</span><span class="sxs-lookup"><span data-stu-id="cadbf-140">The files are located in %windir%\\System32\\winevt\\Logs.</span></span><br/> |
| [<span data-ttu-id="cadbf-141">**palabra**</span><span class="sxs-lookup"><span data-stu-id="cadbf-141">**keywords**</span></span>](eventmanifestschema-keywords-channelpublishingtype-element.md)       | [<span data-ttu-id="cadbf-142">**UInt64Type**</span><span class="sxs-lookup"><span data-stu-id="cadbf-142">**UInt64Type**</span></span>](eventmanifestschema-hexint64type-simpletype.md) | <span data-ttu-id="cadbf-143">Máscara de máscara que determina la categoría de eventos que se escriben en el canal.</span><span class="sxs-lookup"><span data-stu-id="cadbf-143">A bitmask that determines the category of events that are written to the channel.</span></span> <span data-ttu-id="cadbf-144">Si el valor del atributo **Keywords** es 0, todos los eventos que escribe el proveedor se escriben en el canal; de lo contrario, solo se escriben en el canal los eventos que han definido una palabra clave que se incluye en las **palabras clave** de máscara de claves.</span><span class="sxs-lookup"><span data-stu-id="cadbf-144">If the value of **keywords** attribute is 0, all events that the provider writes are written to the channel; otherwise only events that have defined a keyword that is included in the **keywords** bitmask are written to the channel.</span></span> <span data-ttu-id="cadbf-145">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="cadbf-145">The default is 0.</span></span><br/> <span data-ttu-id="cadbf-146">Los canales de depuración que tienen establecido el atributo controlGuid deben establecer el atributo **Keywords** en 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="cadbf-146">Debug channels that have the controlGuid attribute set must set the **keywords** attribute to 0xFFFFFFFFFFFFFFFF.</span></span><br/> <span data-ttu-id="cadbf-147">La sesión pasa el valor Keywords al proveedor cuando habilita el proveedor.</span><span class="sxs-lookup"><span data-stu-id="cadbf-147">The session passes the keywords value to the provider when it enables the provider.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="cadbf-148">**duplica**</span><span class="sxs-lookup"><span data-stu-id="cadbf-148">**latency**</span></span>](eventmanifestschema-latency-channelpublishingtype-element.md)         | [<span data-ttu-id="cadbf-149">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="cadbf-149">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="cadbf-150">Tiempo de espera antes de vaciar los búferes, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="cadbf-150">The time to wait before flushing the buffers, in milliseconds.</span></span> <span data-ttu-id="cadbf-151">Si es cero, ETW vacía los búferes en cuanto se llenan.</span><span class="sxs-lookup"><span data-stu-id="cadbf-151">If zero, ETW flushes the buffers as soon as they become full.</span></span> <span data-ttu-id="cadbf-152">Si es distinto de cero, ETW vacía todos los búferes que contienen eventos en función del valor, incluso si el búfer no está lleno.</span><span class="sxs-lookup"><span data-stu-id="cadbf-152">If nonzero, ETW flushes all buffers that contain events based on the value even if the buffer is not full.</span></span> <span data-ttu-id="cadbf-153">Normalmente, solo desea vaciar los búferes cuando se llenan.</span><span class="sxs-lookup"><span data-stu-id="cadbf-153">Typically, you want to flush buffers only when they become full.</span></span> <span data-ttu-id="cadbf-154">Forzar el vaciado de los búferes puede aumentar el tamaño del archivo de registro con espacio en búfer sin rellenar.</span><span class="sxs-lookup"><span data-stu-id="cadbf-154">Forcing the buffers to flush can increase the file size of the log file with unfilled buffer space.</span></span> <span data-ttu-id="cadbf-155">El valor predeterminado es 1 segundo para los registros operativos y de administración, y 5 segundos para los registros analíticos y de depuración.</span><span class="sxs-lookup"><span data-stu-id="cadbf-155">The default value is 1 second for Admin and Operational logs and 5 seconds for Analytic and Debug logs.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="cadbf-156">**Nivel**</span><span class="sxs-lookup"><span data-stu-id="cadbf-156">**level**</span></span>](eventmanifestschema-level-channelpublishingtype-element.md)             | [<span data-ttu-id="cadbf-157">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="cadbf-157">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="cadbf-158">Nivel de gravedad de los eventos que se van a escribir en el canal.</span><span class="sxs-lookup"><span data-stu-id="cadbf-158">The severity level of the events to write to the channel.</span></span> <span data-ttu-id="cadbf-159">El servicio escribe eventos en el canal que tienen un valor de nivel que es menor o igual que el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="cadbf-159">The service writes events to the channel that have a level value that is less than or equal to the specified value.</span></span> <span data-ttu-id="cadbf-160">El valor predeterminado es 0, lo que significa que se deben registrar los eventos con cualquier valor de nivel.</span><span class="sxs-lookup"><span data-stu-id="cadbf-160">The default is 0, which means to log events with any level value.</span></span><br/> <span data-ttu-id="cadbf-161">La sesión pasa el valor de nivel al proveedor cuando habilita el proveedor.</span><span class="sxs-lookup"><span data-stu-id="cadbf-161">The session passes the level value to the provider when it enables the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="cadbf-162">**maxBuffers**</span><span class="sxs-lookup"><span data-stu-id="cadbf-162">**maxBuffers**</span></span>](eventmanifestschema-maxbuffers-channelpublishingtype-element.md)   | [<span data-ttu-id="cadbf-163">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="cadbf-163">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="cadbf-164">Número máximo de búferes que se van a asignar a la sesión.</span><span class="sxs-lookup"><span data-stu-id="cadbf-164">The maximum number of buffers to allocate for the session.</span></span> <span data-ttu-id="cadbf-165">Normalmente, este valor es el número mínimo de búferes más veinte.</span><span class="sxs-lookup"><span data-stu-id="cadbf-165">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="cadbf-166">Este valor debe ser mayor o igual que el valor especificado para minBuffers.</span><span class="sxs-lookup"><span data-stu-id="cadbf-166">This value must be greater than or equal to the value specified for minBuffers.</span></span><br/> <span data-ttu-id="cadbf-167">El número máximo predeterminado de búferes para los canales analíticos y de depuración es de 10 KB y para el administrador y operativo es de 64 KB.</span><span class="sxs-lookup"><span data-stu-id="cadbf-167">The default maximum number of buffers for Analytic and Debug channels is 10 KB and for Admin and Operational it is 64 KB.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="cadbf-168">**minBuffers**</span><span class="sxs-lookup"><span data-stu-id="cadbf-168">**minBuffers**</span></span>](eventmanifestschema-minbuffers-channelpublishingtype-element.md)   | [<span data-ttu-id="cadbf-169">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="cadbf-169">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="cadbf-170">Número mínimo de búferes que se van a asignar a la sesión.</span><span class="sxs-lookup"><span data-stu-id="cadbf-170">The minimum number of buffers to allocate for the session.</span></span> <span data-ttu-id="cadbf-171">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="cadbf-171">The default is zero.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="cadbf-172">**SID**</span><span class="sxs-lookup"><span data-stu-id="cadbf-172">**sidType**</span></span>](eventmanifestschema-sidtype-channelpublishingtype-element.md)         |                                                                   | <span data-ttu-id="cadbf-173">Determina si se debe incluir un identificador de seguridad (SID) de la entidad de seguridad con cada evento escrito en el canal.</span><span class="sxs-lookup"><span data-stu-id="cadbf-173">Determines whether to include a security identifier (SID) of the principal with each event written to the channel.</span></span> <span data-ttu-id="cadbf-174">Para incluir el SID con el evento, establezca este atributo en "Publishing".</span><span class="sxs-lookup"><span data-stu-id="cadbf-174">To include the SID with the event, set this attribute to "Publishing".</span></span> <span data-ttu-id="cadbf-175">El SID se establece basándose en la identidad del subproceso en el momento en que se escribe el evento.</span><span class="sxs-lookup"><span data-stu-id="cadbf-175">The SID is set based on the thread identity at the time the event is written.</span></span> <span data-ttu-id="cadbf-176">Si no desea incluir el SID con el evento, establezca este atributo en "none".</span><span class="sxs-lookup"><span data-stu-id="cadbf-176">If you do not want to include the SID with the event, set this attribute to "None".</span></span> <span data-ttu-id="cadbf-177">El valor predeterminado es "Publishing".</span><span class="sxs-lookup"><span data-stu-id="cadbf-177">The default is "Publishing".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="cadbf-178">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cadbf-178">Remarks</span></span>

<span data-ttu-id="cadbf-179">Puede especificar esta información de publicación para los tipos de canal analíticos y de depuración o para cualquier canal que especifique el aislamiento personalizado.</span><span class="sxs-lookup"><span data-stu-id="cadbf-179">You can specify this publishing information for Analytic and Debug channel types or for any channel that specifies Custom isolation.</span></span>

<span data-ttu-id="cadbf-180">Aunque puede especificar el nivel y las palabras clave, debe tener en cuenta que estos serán los únicos eventos que recibirá del proveedor para ese canal.</span><span class="sxs-lookup"><span data-stu-id="cadbf-180">Although you can specify level and keywords, you should consider that these will be the only events that you will receive from the provider for that channel.</span></span>

<span data-ttu-id="cadbf-181">Cuando un búfer está lleno, ETW vacía el búfer en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="cadbf-181">When a buffer is full, ETW flushes the buffer to the log file.</span></span> <span data-ttu-id="cadbf-182">Si los búferes se rellenan más rápido de lo que se pueden vaciar, se asignan nuevos búferes y se agregan al grupo de búferes de la sesión, hasta el número máximo especificado.</span><span class="sxs-lookup"><span data-stu-id="cadbf-182">If the buffers are filled faster than they can be flushed, new buffers are allocated and added to the session's buffer pool, up to the maximum number specified.</span></span> <span data-ttu-id="cadbf-183">Más allá de este límite, la sesión descarta los eventos entrantes hasta que un búfer esté disponible.</span><span class="sxs-lookup"><span data-stu-id="cadbf-183">Beyond this limit, the session discards incoming events until a buffer becomes available.</span></span>

## <a name="requirements"></a><span data-ttu-id="cadbf-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cadbf-184">Requirements</span></span>



| <span data-ttu-id="cadbf-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="cadbf-185">Requirement</span></span> | <span data-ttu-id="cadbf-186">Value</span><span class="sxs-lookup"><span data-stu-id="cadbf-186">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cadbf-187">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cadbf-187">Minimum supported client</span></span><br/> | <span data-ttu-id="cadbf-188">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cadbf-188">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cadbf-189">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cadbf-189">Minimum supported server</span></span><br/> | <span data-ttu-id="cadbf-190">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cadbf-190">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





