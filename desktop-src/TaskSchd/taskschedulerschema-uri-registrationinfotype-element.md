---
title: Elemento URI (registrationInfoType)
description: Especifica el URI de la tarea.
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- Programador de tareas del elemento URI
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be3f5782ba5fc02bc3309abfe337c029d0341667
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803962"
---
# <a name="uri-registrationinfotype-element"></a><span data-ttu-id="5581d-104">Elemento URI (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="5581d-104">URI (registrationInfoType) Element</span></span>

<span data-ttu-id="5581d-105">Especifica el URI de la tarea.</span><span class="sxs-lookup"><span data-stu-id="5581d-105">Specifies the URI of the task.</span></span> <span data-ttu-id="5581d-106">Este elemento se usa para especificar dónde se coloca la tarea registrada en la jerarquía de carpetas de tareas.</span><span class="sxs-lookup"><span data-stu-id="5581d-106">This element is used to specify where the registered task is placed in the task folder hierarchy.</span></span>

``` syntax
<xs:element name="URI"
    type="anyURI"
    minOccurs="0"
 />
```

<span data-ttu-id="5581d-107">El elemento **URI** se define mediante el tipo complejo de [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5581d-107">The **URI** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5581d-108">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="5581d-108">Parent element</span></span>



| <span data-ttu-id="5581d-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="5581d-109">Element</span></span>                                                                           | <span data-ttu-id="5581d-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="5581d-110">Derived from</span></span>                                                                         | <span data-ttu-id="5581d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5581d-111">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5581d-112">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="5581d-112">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="5581d-113">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="5581d-113">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="5581d-114">Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="5581d-114">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5581d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5581d-115">Remarks</span></span>

<span data-ttu-id="5581d-116">Para el desarrollo de scripting, el URI de la tarea se especifica mediante la propiedad [**RegistrationInfo. Uri**](registrationinfo-uri.md) .</span><span class="sxs-lookup"><span data-stu-id="5581d-116">For scripting development, the URI of the task is specified using the [**RegistrationInfo.URI**](registrationinfo-uri.md) property.</span></span>

<span data-ttu-id="5581d-117">En el desarrollo de C++, el URI de la tarea se especifica mediante la propiedad [**IRegistrationInfo:: URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) .</span><span class="sxs-lookup"><span data-stu-id="5581d-117">For C++ development, the URI of the task is specified using the [**IRegistrationInfo::URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5581d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5581d-118">Requirements</span></span>



| <span data-ttu-id="5581d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5581d-119">Requirement</span></span> | <span data-ttu-id="5581d-120">Value</span><span class="sxs-lookup"><span data-stu-id="5581d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5581d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5581d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5581d-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5581d-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5581d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5581d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5581d-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5581d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5581d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5581d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5581d-126">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="5581d-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5581d-127">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="5581d-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





