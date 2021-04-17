---
title: Tipo complejo de TaskEventDefinitionType
description: Define un evento específico de la tarea que el proveedor puede registrar. | Tipo complejo de TaskEventDefinitionType
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- TaskEventDefinitionType tipo complejo EventLog
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ebf752dbaf97ceced84b6bd9698faf7b191c07e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698139"
---
# <a name="taskeventdefinitiontype-complex-type"></a><span data-ttu-id="81617-105">Tipo complejo de TaskEventDefinitionType</span><span class="sxs-lookup"><span data-stu-id="81617-105">TaskEventDefinitionType Complex Type</span></span>

<span data-ttu-id="81617-106">\[A partir del compilador de mensajes que se incluye con la versión de Windows 7 del Windows SDK, el tipo complejo de TaskEventDefinitionType ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="81617-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, the TaskEventDefinitionType complex type is no longer available.</span></span> <span data-ttu-id="81617-107">En su lugar, use códigos de tiempo específicos de la tarea para proporcionar la misma funcionalidad.\]</span><span class="sxs-lookup"><span data-stu-id="81617-107">Instead use task-specific opcodes to provide the same functionality.\]</span></span>

<span data-ttu-id="81617-108">Define un evento específico de la tarea que el proveedor puede registrar.</span><span class="sxs-lookup"><span data-stu-id="81617-108">Defines a task-specific event that your provider can log.</span></span>

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
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
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="81617-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="81617-109">Child elements</span></span>



| <span data-ttu-id="81617-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="81617-110">Element</span></span>                                                                      | <span data-ttu-id="81617-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="81617-111">Type</span></span>                                                                               | <span data-ttu-id="81617-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="81617-112">Description</span></span>                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="81617-113">**event**</span><span class="sxs-lookup"><span data-stu-id="81617-113">**event**</span></span>                                                                    | [<span data-ttu-id="81617-114">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="81617-114">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md) | <span data-ttu-id="81617-115">Evento específico de tarea publicado con una tarea.</span><span class="sxs-lookup"><span data-stu-id="81617-115">A task-specific event published with a task.</span></span><br/> |
| [<span data-ttu-id="81617-116">**Código**</span><span class="sxs-lookup"><span data-stu-id="81617-116">**opcode**</span></span>](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | <span data-ttu-id="81617-117">Un código de operación específico de la tarea que para un evento.</span><span class="sxs-lookup"><span data-stu-id="81617-117">A task-specific opcode that for an event.</span></span> <br/>   |



## <a name="attributes"></a><span data-ttu-id="81617-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="81617-118">Attributes</span></span>



| <span data-ttu-id="81617-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="81617-119">Name</span></span> | <span data-ttu-id="81617-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="81617-120">Type</span></span>      | <span data-ttu-id="81617-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="81617-121">Description</span></span>                                      |
|------|-----------|--------------------------------------------------|
| <span data-ttu-id="81617-122">name</span><span class="sxs-lookup"><span data-stu-id="81617-122">name</span></span> | <span data-ttu-id="81617-123">**QName**</span><span class="sxs-lookup"><span data-stu-id="81617-123">**QName**</span></span> | <span data-ttu-id="81617-124">Nombre del código de operación específico de la tarea.</span><span class="sxs-lookup"><span data-stu-id="81617-124">The name of the task-specific opcode.</span></span><br/> |
| <span data-ttu-id="81617-125">name</span><span class="sxs-lookup"><span data-stu-id="81617-125">name</span></span> | <span data-ttu-id="81617-126">anyURI</span><span class="sxs-lookup"><span data-stu-id="81617-126">anyURI</span></span>    | <span data-ttu-id="81617-127">Nombre de la tarea.</span><span class="sxs-lookup"><span data-stu-id="81617-127">The name of the task.</span></span><br/>                 |



## <a name="requirements"></a><span data-ttu-id="81617-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81617-128">Requirements</span></span>



| <span data-ttu-id="81617-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="81617-129">Requirement</span></span> | <span data-ttu-id="81617-130">Value</span><span class="sxs-lookup"><span data-stu-id="81617-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="81617-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81617-131">Minimum supported client</span></span><br/> | <span data-ttu-id="81617-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="81617-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="81617-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81617-133">Minimum supported server</span></span><br/> | <span data-ttu-id="81617-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="81617-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





