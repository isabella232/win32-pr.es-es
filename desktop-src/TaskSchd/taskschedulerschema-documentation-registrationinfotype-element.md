---
title: Elemento Documentation (registrationInfoType)
description: Especifica cualquier documentación adicional para la tarea.
ms.assetid: 5f0d2df3-4eef-430b-85a9-602bb29b85c7
keywords:
- Elemento Documentation Programador de tareas
topic_type:
- apiref
api_name:
- Documentation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3407a6611886f867734dc7f32cd867a2930d3d2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686230"
---
# <a name="documentation-registrationinfotype-element"></a><span data-ttu-id="78436-104">Elemento Documentation (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="78436-104">Documentation (registrationInfoType) Element</span></span>

<span data-ttu-id="78436-105">Especifica cualquier documentación adicional para la tarea.</span><span class="sxs-lookup"><span data-stu-id="78436-105">Specifies any additional documentation for the task.</span></span>

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="78436-106">El elemento **Documentation** se define mediante el tipo complejo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="78436-106">The **Documentation** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="78436-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="78436-107">Parent element</span></span>



| <span data-ttu-id="78436-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="78436-108">Element</span></span>                                                                           | <span data-ttu-id="78436-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="78436-109">Derived from</span></span>                                                                         | <span data-ttu-id="78436-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="78436-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78436-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="78436-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="78436-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="78436-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="78436-113">Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="78436-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="78436-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78436-114">Remarks</span></span>

<span data-ttu-id="78436-115">En el caso de las aplicaciones de scripting, se especifica documentación de tarea adicional mediante el uso de la propiedad [**umentation deRegistrationInfo.Doc**](registrationinfo-documentation.md) .</span><span class="sxs-lookup"><span data-stu-id="78436-115">For scripting applications, additional task documentation is specified using the using the [**RegistrationInfo.Documentation**](registrationinfo-documentation.md) property.</span></span>

<span data-ttu-id="78436-116">En el caso de las aplicaciones de C++, se especifica documentación de tareas adicional mediante el uso de la propiedad [**IRegistrationInfo::D kumentace**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) .</span><span class="sxs-lookup"><span data-stu-id="78436-116">For C++ applications, additional task documentation is specified using the using the [**IRegistrationInfo::Documentation**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="78436-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78436-117">Requirements</span></span>



| <span data-ttu-id="78436-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="78436-118">Requirement</span></span> | <span data-ttu-id="78436-119">Value</span><span class="sxs-lookup"><span data-stu-id="78436-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="78436-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78436-120">Minimum supported client</span></span><br/> | <span data-ttu-id="78436-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="78436-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="78436-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78436-122">Minimum supported server</span></span><br/> | <span data-ttu-id="78436-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="78436-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78436-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="78436-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78436-125">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="78436-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





