---
title: Interfaz IRDVTaskPlugin
description: La interfaz IRDVTaskPlugin se implementa mediante un agente de tareas de actualización de la máquina virtual para permitir que el agente de tareas Administre las actualizaciones del sistema de una máquina virtual.
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IRDVTaskPlugin
- Servicios de Escritorio remoto de la interfaz IRDVTaskPlugin, descrito
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59e90e899e8084f7fbc6b0b6f11067061eaa807b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997077"
---
# <a name="irdvtaskplugin-interface"></a><span data-ttu-id="b0048-105">Interfaz IRDVTaskPlugin</span><span class="sxs-lookup"><span data-stu-id="b0048-105">IRDVTaskPlugin interface</span></span>

<span data-ttu-id="b0048-106">La interfaz **IRDVTaskPlugin** se implementa mediante un *agente de tareas* de actualización de la máquina virtual para permitir que el agente de tareas Administre las actualizaciones del sistema de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b0048-106">The **IRDVTaskPlugin** interface is implemented by a virtual machine update *task agent* to allow the task agent to manage system updates for a virtual machine.</span></span> <span data-ttu-id="b0048-107">Esta interfaz la usa el *agente de desencadenador*, que se implementa mediante el sistema host.</span><span class="sxs-lookup"><span data-stu-id="b0048-107">This interface is used by the *trigger agent*, which is implemented by the host system.</span></span>

## <a name="members"></a><span data-ttu-id="b0048-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b0048-108">Members</span></span>

<span data-ttu-id="b0048-109">La interfaz **IRDVTaskPlugin** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b0048-109">The **IRDVTaskPlugin** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b0048-110">**IRDVTaskPlugin** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b0048-110">**IRDVTaskPlugin** also has these types of members:</span></span>

-   [<span data-ttu-id="b0048-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b0048-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b0048-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b0048-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b0048-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="b0048-113">Methods</span></span>

<span data-ttu-id="b0048-114">La interfaz **IRDVTaskPlugin** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b0048-114">The **IRDVTaskPlugin** interface has these methods.</span></span>



| <span data-ttu-id="b0048-115">Método</span><span class="sxs-lookup"><span data-stu-id="b0048-115">Method</span></span>                                          | <span data-ttu-id="b0048-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0048-116">Description</span></span>                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="b0048-117">**Inicialización**</span><span class="sxs-lookup"><span data-stu-id="b0048-117">**Initialize**</span></span>](irdvtaskplugin-initialize.md) | <span data-ttu-id="b0048-118">Se llama para inicializar el agente de tareas.</span><span class="sxs-lookup"><span data-stu-id="b0048-118">Called to initialize the task agent.</span></span><br/>                    |
| [<span data-ttu-id="b0048-119">**StartTask**</span><span class="sxs-lookup"><span data-stu-id="b0048-119">**StartTask**</span></span>](irdvtaskplugin-starttask.md)   | <span data-ttu-id="b0048-120">Se llama para iniciar la tarea de actualización en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b0048-120">Called to start the update task on the virtual machine.</span></span><br/> |
| [<span data-ttu-id="b0048-121">**Terminate**</span><span class="sxs-lookup"><span data-stu-id="b0048-121">**Terminate**</span></span>](irdvtaskplugin-terminate.md)   | <span data-ttu-id="b0048-122">Se llama cuando se está cerrando el agente de tareas.</span><span class="sxs-lookup"><span data-stu-id="b0048-122">Called when the task agent is being shut down.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="b0048-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b0048-123">Properties</span></span>

<span data-ttu-id="b0048-124">La interfaz **IRDVTaskPlugin** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b0048-124">The **IRDVTaskPlugin** interface has these properties.</span></span>



| <span data-ttu-id="b0048-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b0048-125">Property</span></span>                                                   | <span data-ttu-id="b0048-126">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="b0048-126">Access type</span></span>          | <span data-ttu-id="b0048-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0048-127">Description</span></span>                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [<span data-ttu-id="b0048-128">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="b0048-128">**PluginName**</span></span>](irdvtaskplugin-pluginname.md)<br/> | <span data-ttu-id="b0048-129">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="b0048-129">Read-only</span></span><br/> | <span data-ttu-id="b0048-130">Contiene el nombre para mostrar del agente de tareas.</span><span class="sxs-lookup"><span data-stu-id="b0048-130">Contains the display name of the task agent.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b0048-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0048-131">Remarks</span></span>

<span data-ttu-id="b0048-132">El agente de tareas se ejecuta en la máquina virtual cuando la máquina virtual está programada para una actualización del sistema.</span><span class="sxs-lookup"><span data-stu-id="b0048-132">The task agent is run on the virtual machine when that virtual machine is scheduled for a system update.</span></span> <span data-ttu-id="b0048-133">El agente de tareas actualiza la máquina virtual cuando se llama al método [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="b0048-133">The task agent updates the virtual machine when the [**StartTask**](irdvtaskplugin-starttask.md) method is called.</span></span>

<span data-ttu-id="b0048-134">Para registrar el agente de tareas, agregue la siguiente clave al registro de la máquina virtual:</span><span class="sxs-lookup"><span data-stu-id="b0048-134">To register the task agent, add the following key to the registry of the virtual machine:</span></span>

<span data-ttu-id="b0048-135">**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Terminal Server** \\  \\ **Complementos** de tareas \\ **TaskAgentName**</span><span class="sxs-lookup"><span data-stu-id="b0048-135">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Terminal Server**\\**Task**\\**Plugins**\\**TaskAgentName**</span></span>

<span data-ttu-id="b0048-136">En esta clave del registro, agregue los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="b0048-136">Under this registry key, add the following values:</span></span>



| <span data-ttu-id="b0048-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="b0048-137">Name</span></span>                     | <span data-ttu-id="b0048-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0048-138">Type</span></span>                      | <span data-ttu-id="b0048-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0048-139">Description</span></span>                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="b0048-140">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="b0048-140">**CLSID**</span></span><br/>     | <span data-ttu-id="b0048-141">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="b0048-141">**REG\_SZ**</span></span><br/>    | <span data-ttu-id="b0048-142">Cadena que representa el **CLSID** del agente de tareas.</span><span class="sxs-lookup"><span data-stu-id="b0048-142">A string that represents the **CLSID** of the task agent.</span></span><br/>          |
| <span data-ttu-id="b0048-143">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="b0048-143">**IsEnabled**</span></span><br/> | <span data-ttu-id="b0048-144">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="b0048-144">**REG\_DWORD**</span></span><br/> | <span data-ttu-id="b0048-145">0 si el agente de tareas está deshabilitado o 1 si está habilitado el agente de tareas.</span><span class="sxs-lookup"><span data-stu-id="b0048-145">0 if the task agent is disabled or 1 if the task agent is enabled.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="b0048-146">Se puede registrar más de un agente de tareas, pero solo se usará un agente de tareas.</span><span class="sxs-lookup"><span data-stu-id="b0048-146">More than one task agent can be registered, but only one task agent will be used.</span></span> <span data-ttu-id="b0048-147">Si hay más de un agente de tareas habilitado, solo se usará el primero que se encuentre.</span><span class="sxs-lookup"><span data-stu-id="b0048-147">If more than one task agent is enabled, only the first one found will be used.</span></span>

 

<span data-ttu-id="b0048-148">Aunque esta interfaz es compatible con los sistemas operativos identificados en los requisitos siguientes, solo se usará si la máquina virtual está hospedada en Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b0048-148">Although this interface is supported on the operating systems identified in the Requirements below, it will only be used if the virtual machine is hosted on Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0048-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0048-149">Requirements</span></span>



| <span data-ttu-id="b0048-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0048-150">Requirement</span></span> | <span data-ttu-id="b0048-151">Value</span><span class="sxs-lookup"><span data-stu-id="b0048-151">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="b0048-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0048-152">Minimum supported client</span></span><br/> | <span data-ttu-id="b0048-153">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="b0048-153">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="b0048-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0048-154">Minimum supported server</span></span><br/> | <span data-ttu-id="b0048-155">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b0048-155">Windows Server 2008 R2</span></span><br/> |



 

