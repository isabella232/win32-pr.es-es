---
title: Task (DefinitionType), elemento
description: Define un evento específico de la tarea que el proveedor puede registrar. | Task (DefinitionType), elemento
ms.assetid: 0e880720-1896-43cf-b702-cabca8ab1430
keywords:
- elemento de tarea EventLog
topic_type:
- apiref
api_name:
- task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 35fe629c17b8ede4064de3fb11d05c8e8c84f202
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698088"
---
# <a name="task-definitiontype-element"></a><span data-ttu-id="80f0b-105">Task (DefinitionType), elemento</span><span class="sxs-lookup"><span data-stu-id="80f0b-105">task (DefinitionType) Element</span></span>

<span data-ttu-id="80f0b-106">\[A partir del compilador de mensajes que se incluye con la versión de Windows 7 del Windows SDK, este elemento ya no está disponible.\]</span><span class="sxs-lookup"><span data-stu-id="80f0b-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="80f0b-107">Define un evento específico de la tarea que el proveedor puede registrar.</span><span class="sxs-lookup"><span data-stu-id="80f0b-107">Defines a task-specific event that your provider can log.</span></span>

``` syntax
<xs:element name="task"
    type="TaskEventDefinitionType"
 />
```

<span data-ttu-id="80f0b-108">El elemento **Task** se define mediante el tipo complejo [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="80f0b-108">The **task** element is defined by the [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="80f0b-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80f0b-109">Requirements</span></span>



| <span data-ttu-id="80f0b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="80f0b-110">Requirement</span></span> | <span data-ttu-id="80f0b-111">Value</span><span class="sxs-lookup"><span data-stu-id="80f0b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="80f0b-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80f0b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="80f0b-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="80f0b-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="80f0b-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80f0b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="80f0b-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="80f0b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80f0b-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="80f0b-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="80f0b-117">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="80f0b-117">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="80f0b-118">**eventos (ProviderType)**</span><span class="sxs-lookup"><span data-stu-id="80f0b-118">**events (ProviderType)**</span></span>](eventmanifestschema-events-providertype-element.md)
</dt> </dl>

 

 





