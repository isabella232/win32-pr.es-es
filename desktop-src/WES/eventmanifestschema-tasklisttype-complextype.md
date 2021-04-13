---
title: Tipo complejo de TaskListType
description: Define una lista de tareas que se usan para identificar los componentes de una aplicación.
ms.assetid: 41a46967-7c5b-4555-9f65-bd9582c0c492
keywords:
- TaskListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- TaskListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad427743242ada8901e904fc4e03620ccc72f405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421887"
---
# <a name="tasklisttype-complex-type"></a><span data-ttu-id="e24e2-104">Tipo complejo de TaskListType</span><span class="sxs-lookup"><span data-stu-id="e24e2-104">TaskListType Complex Type</span></span>

<span data-ttu-id="e24e2-105">Define una lista de tareas que se usan para identificar los componentes de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e24e2-105">Defines a list of tasks that are used to identify the components of an application.</span></span>

``` syntax
<xs:complexType name="TaskListType">
    <xs:sequence>
        <xs:element name="task"
            type="TaskType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e24e2-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e24e2-106">Child elements</span></span>



| <span data-ttu-id="e24e2-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="e24e2-107">Element</span></span>                                                       | <span data-ttu-id="e24e2-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e24e2-108">Type</span></span>                                                         | <span data-ttu-id="e24e2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e24e2-109">Description</span></span>                                                       |
|---------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="e24e2-110">**Task**</span><span class="sxs-lookup"><span data-stu-id="e24e2-110">**task**</span></span>](eventmanifestschema-task-tasklisttype-element.md) | [<span data-ttu-id="e24e2-111">**TaskType**</span><span class="sxs-lookup"><span data-stu-id="e24e2-111">**TaskType**</span></span>](eventmanifestschema-tasktype-complextype.md) | <span data-ttu-id="e24e2-112">Define un componente o subcomponente de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e24e2-112">Defines a component or subcomponent of an application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e24e2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e24e2-113">Requirements</span></span>



| <span data-ttu-id="e24e2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e24e2-114">Requirement</span></span> | <span data-ttu-id="e24e2-115">Value</span><span class="sxs-lookup"><span data-stu-id="e24e2-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e24e2-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e24e2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e24e2-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e24e2-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e24e2-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e24e2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e24e2-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e24e2-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





