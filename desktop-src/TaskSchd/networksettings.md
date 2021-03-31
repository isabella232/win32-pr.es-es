---
title: Objeto NetworkSettings
description: En el caso de scripting, proporciona la configuración que el servicio Programador de tareas utiliza para obtener un perfil de red.
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- Objeto NetworkSettings Programador de tareas
- Programador de tareas de objeto NetworkSettings, descrito
topic_type:
- apiref
api_name:
- NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1eecfbbdd4e3ea00c8d2412ae912594f2ec297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491093"
---
# <a name="networksettings-object"></a><span data-ttu-id="b1106-105">Objeto NetworkSettings</span><span class="sxs-lookup"><span data-stu-id="b1106-105">NetworkSettings object</span></span>

<span data-ttu-id="b1106-106">En el caso de scripting, proporciona la configuración que el servicio Programador de tareas utiliza para obtener un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="b1106-106">For scripting, provides the settings that the Task Scheduler service uses to obtain a network profile.</span></span>

## <a name="members"></a><span data-ttu-id="b1106-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b1106-107">Members</span></span>

<span data-ttu-id="b1106-108">El objeto **NetworkSettings** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b1106-108">The **NetworkSettings** object has these types of members:</span></span>

-   [<span data-ttu-id="b1106-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b1106-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1106-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b1106-110">Properties</span></span>

<span data-ttu-id="b1106-111">El objeto **NetworkSettings** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b1106-111">The **NetworkSettings** object has these properties.</span></span>



| <span data-ttu-id="b1106-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b1106-112">Property</span></span>                                        | <span data-ttu-id="b1106-113">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="b1106-113">Access type</span></span>           | <span data-ttu-id="b1106-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1106-114">Description</span></span>                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1106-115">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="b1106-115">**Id**</span></span>](networksettings-id.md)<br/>     | <span data-ttu-id="b1106-116">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b1106-116">Read/write</span></span><br/> | <span data-ttu-id="b1106-117">Obtiene o establece un valor GUID que identifica un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="b1106-117">Gets or sets a GUID value that identifies a network profile.</span></span><br/>                        |
| [<span data-ttu-id="b1106-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="b1106-118">**Name**</span></span>](networksettings-name.md)<br/> | <span data-ttu-id="b1106-119">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b1106-119">Read/write</span></span><br/> | <span data-ttu-id="b1106-120">Obtiene o establece el nombre de un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="b1106-120">Gets or sets the name of a network profile.</span></span> <span data-ttu-id="b1106-121">El nombre se usa para fines de presentación.</span><span class="sxs-lookup"><span data-stu-id="b1106-121">The name is used for display purposes.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="b1106-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1106-122">Remarks</span></span>

<span data-ttu-id="b1106-123">Al leer o escribir su propio XML para una tarea, la configuración de red se especifica mediante el elemento [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="b1106-123">When reading or writing your own XML for a task, network settings are specified using the [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1106-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1106-124">Requirements</span></span>



| <span data-ttu-id="b1106-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1106-125">Requirement</span></span> | <span data-ttu-id="b1106-126">Value</span><span class="sxs-lookup"><span data-stu-id="b1106-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1106-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1106-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b1106-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b1106-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b1106-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1106-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b1106-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1106-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b1106-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b1106-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="b1106-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b1106-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b1106-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b1106-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1106-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1106-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1106-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1106-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1106-136">Objetos Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="b1106-136">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="b1106-137">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="b1106-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





