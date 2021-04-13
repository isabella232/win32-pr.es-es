---
title: Tipo complejo de RenderingInfoType
description: Define los mensajes representados para el evento.
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- RenderingInfoType tipo complejo EventLog
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d0e4224ec9b90e84cbacbf5ede852763edd8e4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492683"
---
# <a name="renderinginfotype-complex-type"></a><span data-ttu-id="e526f-104">Tipo complejo de RenderingInfoType</span><span class="sxs-lookup"><span data-stu-id="e526f-104">RenderingInfoType Complex Type</span></span>

<span data-ttu-id="e526f-105">Define los mensajes representados para el evento.</span><span class="sxs-lookup"><span data-stu-id="e526f-105">Defines the rendered messages for the event.</span></span>

``` syntax
<xs:complexType name="RenderingInfoType">
    <xs:sequence>
        <xs:element name="Message"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Channel"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Provider"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="Keyword"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="Culture"
        type="language"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e526f-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e526f-106">Child elements</span></span>



| <span data-ttu-id="e526f-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="e526f-107">Element</span></span>                                                             | <span data-ttu-id="e526f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e526f-108">Type</span></span>   | <span data-ttu-id="e526f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e526f-109">Description</span></span>                                                                   |
|---------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="e526f-110">**Channel**</span><span class="sxs-lookup"><span data-stu-id="e526f-110">**Channel**</span></span>](eventschema-task-renderingtype-element.md)           | <span data-ttu-id="e526f-111">string</span><span class="sxs-lookup"><span data-stu-id="e526f-111">string</span></span> | <span data-ttu-id="e526f-112">Cadena de mensaje representada del canal especificado en el evento.</span><span class="sxs-lookup"><span data-stu-id="e526f-112">The rendered message string of the channel specified in the event.</span></span><br/> |
| [<span data-ttu-id="e526f-113">**Palabra clave**</span><span class="sxs-lookup"><span data-stu-id="e526f-113">**Keyword**</span></span>](eventschema-keyword-keywords-element.md)             | <span data-ttu-id="e526f-114">string</span><span class="sxs-lookup"><span data-stu-id="e526f-114">string</span></span> | <span data-ttu-id="e526f-115">Cadena de mensaje representada de una palabra clave especificada en el evento.</span><span class="sxs-lookup"><span data-stu-id="e526f-115">The rendered message string of a keyword specified in the event.</span></span><br/>   |
| [<span data-ttu-id="e526f-116">**Palabras clave**</span><span class="sxs-lookup"><span data-stu-id="e526f-116">**Keywords**</span></span>](eventschema-keywords-renderingtype-element.md)      |        | <span data-ttu-id="e526f-117">Una lista de palabras clave representadas.</span><span class="sxs-lookup"><span data-stu-id="e526f-117">A list of rendered keywords.</span></span><br/>                                       |
| [<span data-ttu-id="e526f-118">**Dosis**</span><span class="sxs-lookup"><span data-stu-id="e526f-118">**Level**</span></span>](eventschema-level-renderingtype-element.md)            | <span data-ttu-id="e526f-119">string</span><span class="sxs-lookup"><span data-stu-id="e526f-119">string</span></span> | <span data-ttu-id="e526f-120">Cadena de mensaje representada del nivel especificado en el evento.</span><span class="sxs-lookup"><span data-stu-id="e526f-120">The rendered message string of the level specified in the event.</span></span><br/>   |
| [<span data-ttu-id="e526f-121">**Message**</span><span class="sxs-lookup"><span data-stu-id="e526f-121">**Message**</span></span>](eventschema-message-renderingtype-element.md)        | <span data-ttu-id="e526f-122">string</span><span class="sxs-lookup"><span data-stu-id="e526f-122">string</span></span> | <span data-ttu-id="e526f-123">Cadena de mensaje presentada del evento.</span><span class="sxs-lookup"><span data-stu-id="e526f-123">The rendered message string of the event.</span></span><br/>                          |
| [<span data-ttu-id="e526f-124">**Código de operación**</span><span class="sxs-lookup"><span data-stu-id="e526f-124">**Opcode**</span></span>](eventschema-opcode-renderingtype-element.md)          | <span data-ttu-id="e526f-125">string</span><span class="sxs-lookup"><span data-stu-id="e526f-125">string</span></span> | <span data-ttu-id="e526f-126">Cadena de mensaje representada del código de operación especificado en el evento.</span><span class="sxs-lookup"><span data-stu-id="e526f-126">The rendered message string of the opcode specified in the event.</span></span><br/>  |
| [<span data-ttu-id="e526f-127">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="e526f-127">**Provider**</span></span>](eventschema-publisher-renderinginfotype-element.md) | <span data-ttu-id="e526f-128">string</span><span class="sxs-lookup"><span data-stu-id="e526f-128">string</span></span> | <span data-ttu-id="e526f-129">Cadena de mensaje representada para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="e526f-129">The rendered message string for the provider.</span></span><br/>                      |
| [<span data-ttu-id="e526f-130">**Tarea**</span><span class="sxs-lookup"><span data-stu-id="e526f-130">**Task**</span></span>](eventschema-task-renderingtype-element.md)              | <span data-ttu-id="e526f-131">string</span><span class="sxs-lookup"><span data-stu-id="e526f-131">string</span></span> | <span data-ttu-id="e526f-132">Cadena de mensaje representada de la tarea especificada en el evento.</span><span class="sxs-lookup"><span data-stu-id="e526f-132">The rendered message string of the task specified in the event.</span></span><br/>    |



## <a name="attributes"></a><span data-ttu-id="e526f-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="e526f-133">Attributes</span></span>



| <span data-ttu-id="e526f-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="e526f-134">Name</span></span>    | <span data-ttu-id="e526f-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="e526f-135">Type</span></span>     | <span data-ttu-id="e526f-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="e526f-136">Description</span></span>                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e526f-137">Referencia cultural</span><span class="sxs-lookup"><span data-stu-id="e526f-137">Culture</span></span> | <span data-ttu-id="e526f-138">language</span><span class="sxs-lookup"><span data-stu-id="e526f-138">language</span></span> | <span data-ttu-id="e526f-139">El nombre de idioma (por ejemplo, en-US) que identifica la configuración regional que se usa para representar las cadenas de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e526f-139">The language name (for example, en-US) that identifies the locale used to render the message strings.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e526f-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e526f-140">Remarks</span></span>

<span data-ttu-id="e526f-141">Solo los eventos recopilados mediante el servicio [recopilador de eventos de Windows](/windows/desktop/WEC/windows-event-collector) contendrán esta sección.</span><span class="sxs-lookup"><span data-stu-id="e526f-141">Only events that have been collected using the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service will contain this section.</span></span>

## <a name="requirements"></a><span data-ttu-id="e526f-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e526f-142">Requirements</span></span>



| <span data-ttu-id="e526f-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="e526f-143">Requirement</span></span> | <span data-ttu-id="e526f-144">Value</span><span class="sxs-lookup"><span data-stu-id="e526f-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e526f-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e526f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e526f-146">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e526f-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e526f-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e526f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e526f-148">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e526f-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

