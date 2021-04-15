---
title: Tipo complejo de DefinitionType
description: Define una lista de eventos que el proveedor puede registrar.
ms.assetid: 6d401ced-be1a-409a-8f4d-2d977a33ff8d
keywords:
- DefinitionType tipo complejo EventLog
topic_type:
- apiref
api_name:
- DefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82fbf7ec7db6f64f1bac9776376fa8fe89659d9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695924"
---
# <a name="definitiontype-complex-type"></a><span data-ttu-id="cce47-104">Tipo complejo de DefinitionType</span><span class="sxs-lookup"><span data-stu-id="cce47-104">DefinitionType Complex Type</span></span>

<span data-ttu-id="cce47-105">Define una lista de eventos que el proveedor puede registrar.</span><span class="sxs-lookup"><span data-stu-id="cce47-105">Defines a list of events that your provider can log.</span></span>

``` syntax
<xs:complexType name="DefinitionType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="event"
            type="EventDefinitionType"
         />
        <xs:element name="task"
            type="TaskEventDefinitionType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="cce47-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cce47-106">Child elements</span></span>



| <span data-ttu-id="cce47-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="cce47-107">Element</span></span>                                                           | <span data-ttu-id="cce47-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="cce47-108">Type</span></span>                                                                                       | <span data-ttu-id="cce47-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cce47-109">Description</span></span>                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cce47-110">**ceso**</span><span class="sxs-lookup"><span data-stu-id="cce47-110">**event**</span></span>](eventmanifestschema-event-definitiontype-element.md) | [<span data-ttu-id="cce47-111">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="cce47-111">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md)         | <span data-ttu-id="cce47-112">Define un evento que el proveedor puede registrar.</span><span class="sxs-lookup"><span data-stu-id="cce47-112">Defines an event that your provider can log.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="cce47-113">**Task**</span><span class="sxs-lookup"><span data-stu-id="cce47-113">**task**</span></span>](eventmanifestschema-task-definitiontype-element.md)   | [<span data-ttu-id="cce47-114">**TaskEventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="cce47-114">**TaskEventDefinitionType**</span></span>](eventmanifestschema-taskeventdefinitiontype-complextype.md) | <span data-ttu-id="cce47-115">No se admite.</span><span class="sxs-lookup"><span data-stu-id="cce47-115">Not supported.</span></span><br/> <span data-ttu-id="cce47-116">**Windows Server 2008 y Windows Vista:** Define un evento específico de la tarea que el proveedor puede registrar.</span><span class="sxs-lookup"><span data-stu-id="cce47-116">**Windows Server 2008 and Windows Vista:** Defines a task-specific event that your provider can log.</span></span> <span data-ttu-id="cce47-117">(A partir del compilador de mensajes que se incluye con la versión de Windows 7 del Windows SDK, ya no se admiten eventos específicos de tareas).</span><span class="sxs-lookup"><span data-stu-id="cce47-117">(Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, task-specific events are no longer supported.)</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cce47-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cce47-118">Requirements</span></span>



| <span data-ttu-id="cce47-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cce47-119">Requirement</span></span> | <span data-ttu-id="cce47-120">Value</span><span class="sxs-lookup"><span data-stu-id="cce47-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cce47-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cce47-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cce47-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cce47-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cce47-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cce47-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cce47-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cce47-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





