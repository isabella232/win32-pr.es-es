---
title: Grupo actionGroup
description: Define el grupo de acciones que puede realizar una tarea.
ms.assetid: a43ba021-4a40-4e2c-a57f-bd6ee17706ba
keywords:
- Programador de tareas de grupo actionGroup
- Programador de tareas actionGroup
topic_type:
- apiref
api_name:
- actionGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af06598c6eca092f474467bea16a7d7b95a9563f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801777"
---
# <a name="actiongroup-group"></a><span data-ttu-id="66d28-105">Grupo actionGroup</span><span class="sxs-lookup"><span data-stu-id="66d28-105">actionGroup Group</span></span>

<span data-ttu-id="66d28-106">Define el grupo de acciones que puede realizar una tarea.</span><span class="sxs-lookup"><span data-stu-id="66d28-106">Defines the group of actions that a task can perform.</span></span>

``` syntax
<xs:group name="actionGroup">
    <xs:choice>
        <xs:element name="Exec"
            type="execType"
         />
        <xs:element name="ComHandler"
            type="comHandlerType"
         />
        <xs:element name="SendEmail"
            type="sendEmailType"
         />
        <xs:element name="ShowMessage"
            type="showMessageType"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="66d28-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="66d28-107">Child elements</span></span>



| <span data-ttu-id="66d28-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="66d28-108">Element</span></span>                                                                    | <span data-ttu-id="66d28-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="66d28-109">Type</span></span>                                                                       | <span data-ttu-id="66d28-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="66d28-110">Description</span></span>                                                             |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="66d28-111">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="66d28-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | [<span data-ttu-id="66d28-112">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="66d28-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)   | <span data-ttu-id="66d28-113">Representa una acción que activa un controlador.</span><span class="sxs-lookup"><span data-stu-id="66d28-113">Represents an action that fires a handler.</span></span><br/>                   |
| [<span data-ttu-id="66d28-114">**Ejec**</span><span class="sxs-lookup"><span data-stu-id="66d28-114">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | [<span data-ttu-id="66d28-115">**execType**</span><span class="sxs-lookup"><span data-stu-id="66d28-115">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)               | <span data-ttu-id="66d28-116">Representa una acción que ejecuta una operación de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="66d28-116">Represents an action that executes a command-line operation.</span></span><br/> |
| [<span data-ttu-id="66d28-117">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="66d28-117">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | [<span data-ttu-id="66d28-118">**sendEmailType**</span><span class="sxs-lookup"><span data-stu-id="66d28-118">**sendEmailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)     | <span data-ttu-id="66d28-119">Representa una acción que envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="66d28-119">Represents an action that sends an email message.</span></span><br/>            |
| [<span data-ttu-id="66d28-120">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="66d28-120">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="66d28-121">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="66d28-121">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="66d28-122">Representa una acción que muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="66d28-122">Represents an action that shows a message box.</span></span><br/>               |



## <a name="remarks"></a><span data-ttu-id="66d28-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66d28-123">Remarks</span></span>

<span data-ttu-id="66d28-124">Al leer o escribir XML, los elementos definidos por este grupo son los elementos secundarios del elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="66d28-124">When reading or writing XML, the elements that are defined by this group are the child elements of the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="66d28-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66d28-125">Requirements</span></span>



| <span data-ttu-id="66d28-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="66d28-126">Requirement</span></span> | <span data-ttu-id="66d28-127">Value</span><span class="sxs-lookup"><span data-stu-id="66d28-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="66d28-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66d28-128">Minimum supported client</span></span><br/> | <span data-ttu-id="66d28-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="66d28-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="66d28-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66d28-130">Minimum supported server</span></span><br/> | <span data-ttu-id="66d28-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="66d28-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66d28-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="66d28-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d28-133">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="66d28-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





