---
title: Tipo complejo de EventType
description: Define el nodo raíz del esquema de eventos.
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- EventLog de tipo complejo de EventType
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1103570b6c1d9f51a8cbe8fe5628460690fb32cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421987"
---
# <a name="eventtype-complex-type"></a><span data-ttu-id="1b7ac-104">Tipo complejo de EventType</span><span class="sxs-lookup"><span data-stu-id="1b7ac-104">EventType Complex Type</span></span>

<span data-ttu-id="1b7ac-105">Define el nodo raíz del esquema de eventos.</span><span class="sxs-lookup"><span data-stu-id="1b7ac-105">Defines the root node of the Event schema.</span></span>

``` syntax
<xs:complexType name="EventType">
    <xs:sequence>
        <xs:element name="System"
            type="SystemPropertiesType"
         />
        <xs:choice>
            <xs:element name="EventData"
                type="EventDataType"
                minOccurs="0"
             />
            <xs:element name="UserData"
                type="UserDataType"
                minOccurs="0"
             />
            <xs:element name="DebugData"
                type="DebugDataType"
                minOccurs="0"
             />
            <xs:element name="BinaryEventData"
                type="hexBinary"
                minOccurs="0"
             />
            <xs:element name="ProcessingErrorData"
                type="ProcessingErrorDataType"
                minOccurs="0"
             />
        </xs:choice>
        <xs:element name="RenderingInfo"
            type="RenderingInfoType"
            minOccurs="0"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1b7ac-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1b7ac-106">Child elements</span></span>



| <span data-ttu-id="1b7ac-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="1b7ac-107">Element</span></span>                                                                          | <span data-ttu-id="1b7ac-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b7ac-108">Type</span></span>                                                                               | <span data-ttu-id="1b7ac-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b7ac-109">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b7ac-110">**BinaryEventData**</span><span class="sxs-lookup"><span data-stu-id="1b7ac-110">**BinaryEventData**</span></span>](eventschema-binaryeventdata-eventtype-element.md)         | <span data-ttu-id="1b7ac-111">hexBinary</span><span class="sxs-lookup"><span data-stu-id="1b7ac-111">hexBinary</span></span>                                                                          | <span data-ttu-id="1b7ac-112">Contiene los datos del evento como un BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="1b7ac-112">Contains the event data as a binary blob.</span></span> <span data-ttu-id="1b7ac-113">Los datos de evento se representan como un BLOB binario si la función de representación no encuentra los metadatos usados para descodificar el evento.</span><span class="sxs-lookup"><span data-stu-id="1b7ac-113">The event data is rendered as a binary blob if the rendering function cannot find the metadata used to decode the event.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="1b7ac-114">**DebugData**</span><span class="sxs-lookup"><span data-stu-id="1b7ac-114">**DebugData**</span></span>](eventschema-debugdata-eventtype-element.md)                     | [<span data-ttu-id="1b7ac-115">**DebugDataType**</span><span class="sxs-lookup"><span data-stu-id="1b7ac-115">**DebugDataType**</span></span>](eventschema-debugdatatype-complextype.md)                     | <span data-ttu-id="1b7ac-116">Contiene los datos que se pueden registrar para los eventos de preprocesador de seguimiento de software (WPP) de Windows.</span><span class="sxs-lookup"><span data-stu-id="1b7ac-116">Contains the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="1b7ac-117">**EventData**</span><span class="sxs-lookup"><span data-stu-id="1b7ac-117">**EventData**</span></span>](eventschema-eventdata-eventtype-element.md)                     | [<span data-ttu-id="1b7ac-118">**EventDataType**</span><span class="sxs-lookup"><span data-stu-id="1b7ac-118">**EventDataType**</span></span>](eventschema-eventdatatype-complextype.md)                     | <span data-ttu-id="1b7ac-119">Contiene los datos del evento.</span><span class="sxs-lookup"><span data-stu-id="1b7ac-119">Contains the event data.</span></span> <span data-ttu-id="1b7ac-120">El orden de los elementos de datos de la plantilla determina el diseño de los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="1b7ac-120">The order of the data items in the template determines the layout of the event data.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="1b7ac-121">**ProcessingErrorData**</span><span class="sxs-lookup"><span data-stu-id="1b7ac-121">**ProcessingErrorData**</span></span>](eventschema-processingerrordata-eventtype-element.md) | [<span data-ttu-id="1b7ac-122">**ProcessingErrorDataType**</span><span class="sxs-lookup"><span data-stu-id="1b7ac-122">**ProcessingErrorDataType**</span></span>](eventschema-processingerrordatatype-complextype.md) | <span data-ttu-id="1b7ac-123">Contiene detalles del error que se produjo al intentar representar el evento.</span><span class="sxs-lookup"><span data-stu-id="1b7ac-123">Contains details of the error that occurred while trying to render the event.</span></span> <span data-ttu-id="1b7ac-124">Esto puede ocurrir si los datos del evento no coinciden con la definición de datos del evento en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="1b7ac-124">This can occur if the event data does not match the event data definition in the manifest.</span></span> <span data-ttu-id="1b7ac-125">Los datos de evento se incluyen como un BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="1b7ac-125">The event data is included as a binary blob.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="1b7ac-126">**RenderingInfo**</span><span class="sxs-lookup"><span data-stu-id="1b7ac-126">**RenderingInfo**</span></span>](eventschema-renderinginfo-eventtype-element.md)             | [<span data-ttu-id="1b7ac-127">**RenderingInfoType**</span><span class="sxs-lookup"><span data-stu-id="1b7ac-127">**RenderingInfoType**</span></span>](eventschema-renderingtype-complextype.md)                 | <span data-ttu-id="1b7ac-128">Contiene las cadenas de mensaje representadas para el evento (incluye la cadena de mensaje del evento y las cadenas de mensaje para cualquiera de las propiedades del evento como el nivel, la tarea y el código de operación).</span><span class="sxs-lookup"><span data-stu-id="1b7ac-128">Contains the rendered message strings for the event (includes the event's message string and the message strings for any of the event's properties such as level, task, and opcode).</span></span> <span data-ttu-id="1b7ac-129">Solo los eventos recopilados mediante el servicio [recopilador de eventos de Windows](/windows/desktop/WEC/windows-event-collector) contendrán esta sección.</span><span class="sxs-lookup"><span data-stu-id="1b7ac-129">Only events that have been collected using the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service will contain this section.</span></span><br/> |
| [<span data-ttu-id="1b7ac-130">**System**</span><span class="sxs-lookup"><span data-stu-id="1b7ac-130">**System**</span></span>](eventschema-system-eventtype-element.md)                           | [<span data-ttu-id="1b7ac-131">**SystemPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="1b7ac-131">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)       | <span data-ttu-id="1b7ac-132">Contiene información que identifica al proveedor y cómo se habilitó, el evento, el canal en el que se escribió el evento e información del sistema, como los identificadores de proceso y de subproceso.</span><span class="sxs-lookup"><span data-stu-id="1b7ac-132">Contains information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="1b7ac-133">**UserData**</span><span class="sxs-lookup"><span data-stu-id="1b7ac-133">**UserData**</span></span>](eventschema-userdata-eventtype-element.md)                       | [<span data-ttu-id="1b7ac-134">**UserDataType**</span><span class="sxs-lookup"><span data-stu-id="1b7ac-134">**UserDataType**</span></span>](eventschema-userdatatype-complextype.md)                       | <span data-ttu-id="1b7ac-135">Contiene los datos del evento.</span><span class="sxs-lookup"><span data-stu-id="1b7ac-135">Contains the event data.</span></span> <span data-ttu-id="1b7ac-136">La sección de datos de usuario de la plantilla determina el diseño de los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="1b7ac-136">The user data section of the template determines the layout of the event data.</span></span><br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="1b7ac-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b7ac-137">Remarks</span></span>

<span data-ttu-id="1b7ac-138">Normalmente, esta sección contendrá la sección **EventData** o **UserData** .</span><span class="sxs-lookup"><span data-stu-id="1b7ac-138">Typically, this section will contain with the **EventData** or **UserData** section.</span></span> <span data-ttu-id="1b7ac-139">La sección **EventData** se usa si la plantilla no contiene una sección **UserData** .</span><span class="sxs-lookup"><span data-stu-id="1b7ac-139">The **EventData** section is used if the template does not contain a **UserData** section.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b7ac-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b7ac-140">Requirements</span></span>



| <span data-ttu-id="1b7ac-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b7ac-141">Requirement</span></span> | <span data-ttu-id="1b7ac-142">Value</span><span class="sxs-lookup"><span data-stu-id="1b7ac-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1b7ac-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b7ac-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1b7ac-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1b7ac-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1b7ac-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b7ac-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1b7ac-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b7ac-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

