---
title: OpCode (TaskEventDefinitionType) (elemento)
description: Contiene un código de operación específico de la tarea para un evento. Se supone que todas las definiciones de código de operación son específicas de la tarea para la tarea que contiene las definiciones de evento.
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- elemento OpCode EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9f3b58353163e1ee5b9abeb04007a4a9d449e5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696028"
---
# <a name="opcode-taskeventdefinitiontype-element"></a><span data-ttu-id="a427f-105">OpCode (TaskEventDefinitionType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="a427f-105">opcode (TaskEventDefinitionType) Element</span></span>

<span data-ttu-id="a427f-106">\[A partir del compilador de mensajes que se incluye con la versión de Windows 7 del Windows SDK, este elemento ya no está disponible.\]</span><span class="sxs-lookup"><span data-stu-id="a427f-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="a427f-107">Contiene un código de operación específico de la tarea para un evento.</span><span class="sxs-lookup"><span data-stu-id="a427f-107">Contains a task-specific opcode for an event.</span></span> <span data-ttu-id="a427f-108">Se supone que todas las definiciones de código de operación son específicas de la tarea para la tarea que contiene las definiciones de evento.</span><span class="sxs-lookup"><span data-stu-id="a427f-108">All of the opcode definitions are assumed to be task-specific for the task that contains the event definitions.</span></span>

``` syntax
<xs:element name="opcode">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="event"
                type="EventDefinitionType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
        <xs:attribute name="name"
            type="QName"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="a427f-109">El elemento **OpCode** se define mediante el tipo complejo [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a427f-109">The **opcode** element is defined by the [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a427f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a427f-110">Child elements</span></span>



| <span data-ttu-id="a427f-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="a427f-111">Element</span></span>                                                   | <span data-ttu-id="a427f-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="a427f-112">Type</span></span>                                                                               | <span data-ttu-id="a427f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="a427f-113">Description</span></span>                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="a427f-114">**ceso**</span><span class="sxs-lookup"><span data-stu-id="a427f-114">**event**</span></span>](eventmanifestschema-event-opcode-element.md) | [<span data-ttu-id="a427f-115">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="a427f-115">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md) | <span data-ttu-id="a427f-116">Evento que se publica con una tarea.</span><span class="sxs-lookup"><span data-stu-id="a427f-116">An event that is published with a task.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="a427f-117">Atributos</span><span class="sxs-lookup"><span data-stu-id="a427f-117">Attributes</span></span>



| <span data-ttu-id="a427f-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="a427f-118">Name</span></span> | <span data-ttu-id="a427f-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="a427f-119">Type</span></span>      | <span data-ttu-id="a427f-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="a427f-120">Description</span></span>                                      |
|------|-----------|--------------------------------------------------|
| <span data-ttu-id="a427f-121">name</span><span class="sxs-lookup"><span data-stu-id="a427f-121">name</span></span> | <span data-ttu-id="a427f-122">**QName**</span><span class="sxs-lookup"><span data-stu-id="a427f-122">**QName**</span></span> | <span data-ttu-id="a427f-123">Nombre del código de operación específico de la tarea.</span><span class="sxs-lookup"><span data-stu-id="a427f-123">The name of the task-specific opcode.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a427f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a427f-124">Requirements</span></span>



| <span data-ttu-id="a427f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a427f-125">Requirement</span></span> | <span data-ttu-id="a427f-126">Value</span><span class="sxs-lookup"><span data-stu-id="a427f-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a427f-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a427f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a427f-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a427f-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a427f-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a427f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a427f-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a427f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a427f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a427f-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="a427f-132">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="a427f-132">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="a427f-133">**tarea (DefinitionType)**</span><span class="sxs-lookup"><span data-stu-id="a427f-133">**task (DefinitionType)**</span></span>](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





