---
title: Tipo complejo de sessionStateChangeTriggerType
description: Define los elementos que se usan para crear un desencadenador de tarea para la conexión o desconexión de la consola, la conexión remota o la desconexión o las notificaciones de bloqueo o desbloqueo de estación de trabajo.
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- tipo complejo de sessionStateChangeTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8eb3ad02aef3f5bbbc078f8eafa52f3439819cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359858"
---
# <a name="sessionstatechangetriggertype-complex-type"></a><span data-ttu-id="1cae8-104">Tipo complejo de sessionStateChangeTriggerType</span><span class="sxs-lookup"><span data-stu-id="1cae8-104">sessionStateChangeTriggerType Complex Type</span></span>

<span data-ttu-id="1cae8-105">Define los elementos que se usan para crear un desencadenador de tarea para la conexión o desconexión de la consola, la conexión remota o la desconexión o las notificaciones de bloqueo o desbloqueo de estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="1cae8-105">Defines the elements used to create a task trigger for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.</span></span>

``` syntax
<xs:complexType name="sessionStateChangeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="StateChange"
                    type="sessionStateChangeType"
                    minOccurs="1"
                    maxOccurs="1"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1cae8-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1cae8-106">Child elements</span></span>



| <span data-ttu-id="1cae8-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="1cae8-107">Element</span></span>                                                                                      | <span data-ttu-id="1cae8-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="1cae8-108">Type</span></span>                                                                                    | <span data-ttu-id="1cae8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cae8-109">Description</span></span>                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1cae8-110">**Delay**</span><span class="sxs-lookup"><span data-stu-id="1cae8-110">**Delay**</span></span>](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | <span data-ttu-id="1cae8-111">duration</span><span class="sxs-lookup"><span data-stu-id="1cae8-111">duration</span></span>                                                                                | <span data-ttu-id="1cae8-112">Especifica un valor que indica la duración del retraso antes de que se inicie una tarea cuando se detecta un cambio de estado de sesión Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="1cae8-112">Specifies a value that indicates the length of the delay before a task is started when a Terminal Server session state change is detected.</span></span><br/> |
| [<span data-ttu-id="1cae8-113">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="1cae8-113">**StateChange**</span></span>](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [<span data-ttu-id="1cae8-114">**sessionStateChangeType**</span><span class="sxs-lookup"><span data-stu-id="1cae8-114">**sessionStateChangeType**</span></span>](taskschedulerschema-sessionstatechangetype-simpletype.md) | <span data-ttu-id="1cae8-115">Especifica el tipo de Terminal Server cambio de sesión que desencadenaría el inicio de una tarea.</span><span class="sxs-lookup"><span data-stu-id="1cae8-115">Specifies the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                     |
| [<span data-ttu-id="1cae8-116">**Deberían**</span><span class="sxs-lookup"><span data-stu-id="1cae8-116">**UserId**</span></span>](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [<span data-ttu-id="1cae8-117">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="1cae8-117">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                 | <span data-ttu-id="1cae8-118">Especifica el usuario de la sesión de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="1cae8-118">Specifies the user for the Terminal Server session.</span></span> <span data-ttu-id="1cae8-119">Cuando se detecta un cambio de estado de sesión para este usuario, se inicia una tarea.</span><span class="sxs-lookup"><span data-stu-id="1cae8-119">When a session state change is detected for this user, a task is started.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="1cae8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cae8-120">Requirements</span></span>



| <span data-ttu-id="1cae8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cae8-121">Requirement</span></span> | <span data-ttu-id="1cae8-122">Value</span><span class="sxs-lookup"><span data-stu-id="1cae8-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1cae8-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cae8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1cae8-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1cae8-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1cae8-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cae8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1cae8-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1cae8-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





