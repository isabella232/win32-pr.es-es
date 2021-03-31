---
title: Interfaz IRDVTaskPluginNotifySink
description: El agente de tareas usa la interfaz IRDVTaskPluginNotifySink para comunicarse con el agente desencadenador.
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IRDVTaskPluginNotifySink
- Servicios de Escritorio remoto de la interfaz IRDVTaskPluginNotifySink, descrito
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0dadaf387fcf6e8381404440e0d31dd210b9f8a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802702"
---
# <a name="irdvtaskpluginnotifysink-interface"></a><span data-ttu-id="3c972-105">Interfaz IRDVTaskPluginNotifySink</span><span class="sxs-lookup"><span data-stu-id="3c972-105">IRDVTaskPluginNotifySink interface</span></span>

<span data-ttu-id="3c972-106">El agente de tareas usa la interfaz **IRDVTaskPluginNotifySink** para comunicarse con el agente desencadenador.</span><span class="sxs-lookup"><span data-stu-id="3c972-106">The **IRDVTaskPluginNotifySink** interface is used by the task agent to communicate with the trigger agent.</span></span> <span data-ttu-id="3c972-107">Un puntero a esta interfaz se pasa al agente de tarea en el método [**IRDVTaskPlugin:: Initialize**](irdvtaskplugin-initialize.md) .</span><span class="sxs-lookup"><span data-stu-id="3c972-107">A pointer to this interface is passed to the task agent in the [**IRDVTaskPlugin::Initialize**](irdvtaskplugin-initialize.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="3c972-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3c972-108">Members</span></span>

<span data-ttu-id="3c972-109">La interfaz **IRDVTaskPluginNotifySink** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3c972-109">The **IRDVTaskPluginNotifySink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3c972-110">**IRDVTaskPluginNotifySink** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3c972-110">**IRDVTaskPluginNotifySink** also has these types of members:</span></span>

-   [<span data-ttu-id="3c972-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="3c972-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3c972-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3c972-112">Methods</span></span>

<span data-ttu-id="3c972-113">La interfaz **IRDVTaskPluginNotifySink** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3c972-113">The **IRDVTaskPluginNotifySink** interface has these methods.</span></span>



| <span data-ttu-id="3c972-114">Método</span><span class="sxs-lookup"><span data-stu-id="3c972-114">Method</span></span>                                                                  | <span data-ttu-id="3c972-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c972-115">Description</span></span>                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="3c972-116">**DeleteSchedule**</span><span class="sxs-lookup"><span data-stu-id="3c972-116">**DeleteSchedule**</span></span>](irdvtaskpluginnotifysink-deleteschedule.md)       | <span data-ttu-id="3c972-117">El agente de tareas lo llama para eliminar una tarea programada.</span><span class="sxs-lookup"><span data-stu-id="3c972-117">Called by the task agent to delete a scheduled task.</span></span><br/>                   |
| [<span data-ttu-id="3c972-118">**OnTaskStateChange**</span><span class="sxs-lookup"><span data-stu-id="3c972-118">**OnTaskStateChange**</span></span>](irdvtaskpluginnotifysink-ontaskstatechange.md) | <span data-ttu-id="3c972-119">Se usa para notificar al agente de desencadenador que el estado de una tarea ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="3c972-119">Used to notify the trigger agent that the state of a task has changed.</span></span><br/> |
| [<span data-ttu-id="3c972-120">**Terminado**</span><span class="sxs-lookup"><span data-stu-id="3c972-120">**OnTerminated**</span></span>](irdvtaskpluginnotifysink-onterminated.md)           | <span data-ttu-id="3c972-121">El agente de tareas lo llama para solicitar que se cierre el agente de tareas.</span><span class="sxs-lookup"><span data-stu-id="3c972-121">Called by the task agent to request that the task agent be shut down.</span></span><br/>  |
| [<span data-ttu-id="3c972-122">**ScheduleTask (**</span><span class="sxs-lookup"><span data-stu-id="3c972-122">**ScheduleTask**</span></span>](irdvtaskpluginnotifysink-scheduletask.md)           | <span data-ttu-id="3c972-123">Llamado por el agente de tareas para programar una tarea.</span><span class="sxs-lookup"><span data-stu-id="3c972-123">Called by the task agent to schedule a task.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="3c972-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c972-124">Remarks</span></span>

<span data-ttu-id="3c972-125">Aunque esta interfaz es compatible con los sistemas operativos identificados en los requisitos siguientes, solo se usará si la máquina virtual está hospedada en Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="3c972-125">Although this interface is supported on the operating systems identified in the Requirements below, it will only be used if the virtual machine is hosted on Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c972-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c972-126">Requirements</span></span>



| <span data-ttu-id="3c972-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c972-127">Requirement</span></span> | <span data-ttu-id="3c972-128">Value</span><span class="sxs-lookup"><span data-stu-id="3c972-128">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="3c972-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c972-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3c972-130">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="3c972-130">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="3c972-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c972-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3c972-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3c972-132">Windows Server 2008 R2</span></span><br/> |



 

