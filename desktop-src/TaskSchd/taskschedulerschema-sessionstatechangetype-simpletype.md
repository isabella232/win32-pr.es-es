---
title: Tipo simple de sessionStateChangeType
description: Define los valores para el tipo de Terminal Server cambio de estado de sesión que puede usar para desencadenar la inicio de una tarea.
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- Programador de tareas de tipo simple sessionStateChangeType
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a77fb563b59ccd8d63d38c6c85f16ff74ac404b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492269"
---
# <a name="sessionstatechangetype-simple-type"></a><span data-ttu-id="863d1-104">Tipo simple de sessionStateChangeType</span><span class="sxs-lookup"><span data-stu-id="863d1-104">sessionStateChangeType Simple Type</span></span>

<span data-ttu-id="863d1-105">Define los valores para el tipo de Terminal Server cambio de estado de sesión que puede usar para desencadenar la inicio de una tarea.</span><span class="sxs-lookup"><span data-stu-id="863d1-105">Defines values for the kind of Terminal Server session state change you can use to trigger a task to start.</span></span>

``` syntax
<xs:simpleType name="sessionStateChangeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="ConsoleConnect"
         />
        <xs:enumeration
            value="ConsoleDisconnect"
         />
        <xs:enumeration
            value="RemoteConnect"
         />
        <xs:enumeration
            value="RemoteDisconnect"
         />
        <xs:enumeration
            value="SessionLock"
         />
        <xs:enumeration
            value="SessionUnlock"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="863d1-106">Valores de enumeración</span><span class="sxs-lookup"><span data-stu-id="863d1-106">Enumeration values</span></span>

<span data-ttu-id="863d1-107">El tipo simple **sessionStateChangeType** define los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="863d1-107">The **sessionStateChangeType** simple type defines the following values.</span></span>



| <span data-ttu-id="863d1-108">Value</span><span class="sxs-lookup"><span data-stu-id="863d1-108">Value</span></span>             | <span data-ttu-id="863d1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="863d1-109">Description</span></span>                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="863d1-110">ConsoleConnect</span><span class="sxs-lookup"><span data-stu-id="863d1-110">ConsoleConnect</span></span>    | <span data-ttu-id="863d1-111">Terminal Server cambio del estado de conexión de la consola.</span><span class="sxs-lookup"><span data-stu-id="863d1-111">Terminal Server console connection state change.</span></span> <span data-ttu-id="863d1-112">Por ejemplo, cuando se conecta a una sesión de usuario en el equipo local mediante el cambio de usuarios en el equipo.</span><span class="sxs-lookup"><span data-stu-id="863d1-112">For example, when you connect to a user session on the local computer by switching users on the computer.</span></span> <br/>                            |
| <span data-ttu-id="863d1-113">ConsoleDisconnect</span><span class="sxs-lookup"><span data-stu-id="863d1-113">ConsoleDisconnect</span></span> | <span data-ttu-id="863d1-114">Terminal Server cambio de estado de desconexión de la consola.</span><span class="sxs-lookup"><span data-stu-id="863d1-114">Terminal Server console disconnection state change.</span></span> <span data-ttu-id="863d1-115">Por ejemplo, cuando se desconecta a una sesión de usuario en el equipo local mediante el cambio de usuarios en el equipo.</span><span class="sxs-lookup"><span data-stu-id="863d1-115">For example, when you disconnect to a user session on the local computer by switching users on the computer.</span></span> <br/>                      |
| <span data-ttu-id="863d1-116">RemoteConnect</span><span class="sxs-lookup"><span data-stu-id="863d1-116">RemoteConnect</span></span>     | <span data-ttu-id="863d1-117">Terminal Server cambio de estado de la conexión remota.</span><span class="sxs-lookup"><span data-stu-id="863d1-117">Terminal Server remote connection state change.</span></span> <span data-ttu-id="863d1-118">Por ejemplo, cuando un usuario se conecta a una sesión de usuario mediante el programa de Conexión a Escritorio remoto desde un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="863d1-118">For example, when a user connects to a user session by using the Remote Desktop Connection program from a remote computer.</span></span> <br/>            |
| <span data-ttu-id="863d1-119">RemoteDisconnect</span><span class="sxs-lookup"><span data-stu-id="863d1-119">RemoteDisconnect</span></span>  | <span data-ttu-id="863d1-120">Terminal Server cambio de estado de desconexión remota.</span><span class="sxs-lookup"><span data-stu-id="863d1-120">Terminal Server remote disconnection state change.</span></span> <span data-ttu-id="863d1-121">Por ejemplo, cuando un usuario se desconecta de una sesión de usuario mientras usa el programa Conexión a Escritorio remoto desde un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="863d1-121">For example, when a user disconnects from a user session while using the Remote Desktop Connection program from a remote computer.</span></span> <br/> |
| <span data-ttu-id="863d1-122">SessionLock</span><span class="sxs-lookup"><span data-stu-id="863d1-122">SessionLock</span></span>       | <span data-ttu-id="863d1-123">Terminal Server cambio de estado de la sesión bloqueada.</span><span class="sxs-lookup"><span data-stu-id="863d1-123">Terminal Server session locked state change.</span></span> <span data-ttu-id="863d1-124">Por ejemplo, este cambio de estado hace que la tarea se ejecute cuando el equipo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="863d1-124">For example, this state change causes the task to run when the computer is locked.</span></span> <br/>                                                       |
| <span data-ttu-id="863d1-125">SessionUnlock</span><span class="sxs-lookup"><span data-stu-id="863d1-125">SessionUnlock</span></span>     | <span data-ttu-id="863d1-126">Terminal Server cambio de estado desbloqueado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="863d1-126">Terminal Server session unlocked state change.</span></span> <span data-ttu-id="863d1-127">Por ejemplo, este cambio de estado hace que la tarea se ejecute cuando se desbloquea el equipo.</span><span class="sxs-lookup"><span data-stu-id="863d1-127">For example, this state change causes the task to run when the computer is unlocked.</span></span><br/>                                                    |



## <a name="requirements"></a><span data-ttu-id="863d1-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="863d1-128">Requirements</span></span>



| <span data-ttu-id="863d1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="863d1-129">Requirement</span></span> | <span data-ttu-id="863d1-130">Value</span><span class="sxs-lookup"><span data-stu-id="863d1-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="863d1-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="863d1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="863d1-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="863d1-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="863d1-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="863d1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="863d1-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="863d1-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





