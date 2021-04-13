---
title: UserId (logonTriggerType), elemento
description: Identificador del usuario. La tarea se inicia cuando este usuario inicia sesión en el equipo.
ms.assetid: 52568899-e351-4ee1-b613-d7c42d7b983d
keywords:
- UserId, elemento Programador de tareas
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69d6534122b4b5e11a18a64ffa9bbb5e29e2a68a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535481"
---
# <a name="userid-logontriggertype-element"></a><span data-ttu-id="416b2-105">UserId (logonTriggerType), elemento</span><span class="sxs-lookup"><span data-stu-id="416b2-105">UserId (logonTriggerType) Element</span></span>

<span data-ttu-id="416b2-106">Identificador del usuario.</span><span class="sxs-lookup"><span data-stu-id="416b2-106">Identifier of the user.</span></span> <span data-ttu-id="416b2-107">La tarea se inicia cuando este usuario inicia sesión en el equipo.</span><span class="sxs-lookup"><span data-stu-id="416b2-107">The task is started when this user logs on to the computer.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="416b2-108">El elemento **userid** se define mediante el tipo complejo [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="416b2-108">The **UserId** element is defined by the [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="416b2-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="416b2-109">Parent element</span></span>



| <span data-ttu-id="416b2-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="416b2-110">Element</span></span>                                                                       | <span data-ttu-id="416b2-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="416b2-111">Derived from</span></span>                                                                 | <span data-ttu-id="416b2-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="416b2-112">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="416b2-113">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="416b2-113">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md) | [<span data-ttu-id="416b2-114">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="416b2-114">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md) | <span data-ttu-id="416b2-115">Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="416b2-115">Specifies a trigger that starts a task when a user logs on.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="416b2-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="416b2-116">Remarks</span></span>

<span data-ttu-id="416b2-117">Para el desarrollo de scripting, el identificador de usuario para el desencadenador logon se especifica mediante la propiedad [**LogonTrigger. userid**](logontrigger-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="416b2-117">For scripting development, the user identifier for the logon trigger is specified using the [**LogonTrigger.UserId**](logontrigger-userid.md) property.</span></span>

<span data-ttu-id="416b2-118">En el desarrollo de C++, el identificador de usuario para el desencadenador logon se especifica mediante la propiedad [**ILogonTrigger:: userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) .</span><span class="sxs-lookup"><span data-stu-id="416b2-118">For C++ development, the user identifier for the logon trigger is specified using the [**ILogonTrigger::UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="416b2-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="416b2-119">Examples</span></span>

<span data-ttu-id="416b2-120">Para obtener un ejemplo completo del XML de una tarea que especifica un desencadenador Logon, vea [ejemplo de desencadenador de inicio de sesión (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="416b2-120">For a complete example of the XML for a task that specifies a logon trigger, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="416b2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="416b2-121">Requirements</span></span>



| <span data-ttu-id="416b2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="416b2-122">Requirement</span></span> | <span data-ttu-id="416b2-123">Value</span><span class="sxs-lookup"><span data-stu-id="416b2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="416b2-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="416b2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="416b2-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="416b2-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="416b2-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="416b2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="416b2-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="416b2-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="416b2-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="416b2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="416b2-129">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="416b2-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="416b2-130">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="416b2-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





