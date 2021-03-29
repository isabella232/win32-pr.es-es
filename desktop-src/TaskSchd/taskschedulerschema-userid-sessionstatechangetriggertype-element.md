---
title: UserId (sessionStateChangeTriggerType), elemento
description: Contiene el usuario para la sesión de Terminal Server. Cuando se detecta un cambio de estado de sesión para este usuario, se inicia una tarea.
ms.assetid: 7605f444-b2c9-4bba-a035-f1307c01184f
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
ms.openlocfilehash: cd66a05d25ea9b44f124d55ccc0cbb2c628aeeb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534972"
---
# <a name="userid-sessionstatechangetriggertype-element"></a><span data-ttu-id="22e48-105">UserId (sessionStateChangeTriggerType), elemento</span><span class="sxs-lookup"><span data-stu-id="22e48-105">UserId (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="22e48-106">Contiene el usuario para la sesión de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="22e48-106">Contains the user for the Terminal Server session.</span></span> <span data-ttu-id="22e48-107">Cuando se detecta un cambio de estado de sesión para este usuario, se inicia una tarea.</span><span class="sxs-lookup"><span data-stu-id="22e48-107">When a session state change is detected for this user, a task is started.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="22e48-108">El elemento **userid** se define mediante el tipo complejo [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="22e48-108">The **UserId** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="22e48-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="22e48-109">Parent element</span></span>



| <span data-ttu-id="22e48-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="22e48-110">Element</span></span>                       | <span data-ttu-id="22e48-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="22e48-111">Derived from</span></span>                                                                                           | <span data-ttu-id="22e48-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="22e48-112">Description</span></span>                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22e48-113">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="22e48-113">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="22e48-114">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="22e48-114">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="22e48-115">Especifica un desencadenador que inicia una tarea cuando se cambia el estado de una sesión de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="22e48-115">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="22e48-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22e48-116">Remarks</span></span>

<span data-ttu-id="22e48-117">Para el desarrollo de C++, consulte [**propiedad userid de ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).</span><span class="sxs-lookup"><span data-stu-id="22e48-117">For C++ development, see [**UserId Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).</span></span>

<span data-ttu-id="22e48-118">Para el desarrollo de scripts, vea [**SessionStateChangeTrigger. userid**](sessionstatechangetrigger-userid.md).</span><span class="sxs-lookup"><span data-stu-id="22e48-118">For script development, see [**SessionStateChangeTrigger.UserId**](sessionstatechangetrigger-userid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22e48-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22e48-119">Requirements</span></span>



| <span data-ttu-id="22e48-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="22e48-120">Requirement</span></span> | <span data-ttu-id="22e48-121">Value</span><span class="sxs-lookup"><span data-stu-id="22e48-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="22e48-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22e48-122">Minimum supported client</span></span><br/> | <span data-ttu-id="22e48-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="22e48-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="22e48-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22e48-124">Minimum supported server</span></span><br/> | <span data-ttu-id="22e48-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="22e48-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





