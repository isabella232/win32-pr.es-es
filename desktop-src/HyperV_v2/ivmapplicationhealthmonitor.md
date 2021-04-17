---
description: Notifica el estado de mantenimiento de una aplicación que se ejecuta en una máquina virtual a los componentes de integración de Hyper-V que se ejecutan en la misma máquina virtual.
ms.assetid: C463391B-669C-4CBA-9EC7-7E0ABC5A63A1
title: Interfaz IVmApplicationHealthMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: ac9f6574dd8261a120e434cc0351fd07985c71a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687194"
---
# <a name="ivmapplicationhealthmonitor-interface"></a><span data-ttu-id="1c550-103">Interfaz IVmApplicationHealthMonitor</span><span class="sxs-lookup"><span data-stu-id="1c550-103">IVmApplicationHealthMonitor interface</span></span>

<span data-ttu-id="1c550-104">Notifica el estado de mantenimiento de una aplicación que se ejecuta en una máquina virtual a los componentes de integración de Hyper-V que se ejecutan en la misma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1c550-104">Reports the health status of an application that is running in a virtual machine to the Hyper-V integration components running in the same virtual machine.</span></span> <span data-ttu-id="1c550-105">El estado de las aplicaciones que se ejecutan en la máquina virtual se refleja en el \[ valor de la propiedad OperationalStatus 1 \] de la clase [**MSVM \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="1c550-105">The state of the applications running in the virtual machine are reflected in the **OperationalStatus**\[1\] property value of the [**Msvm\_HeartbeatComponent**](msvm-heartbeatcomponent.md) class.</span></span> <span data-ttu-id="1c550-106">Esta interfaz también proporciona una manera de restablecer todo el estado de la aplicación acumulado en Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="1c550-106">This interface also provides a way to reset all of the application state accumulated in Hyper-V.</span></span>

<span data-ttu-id="1c550-107">Esta interfaz la implementan los componentes de integración de Hyper-V de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1c550-107">This interface is implemented by the Windows 8 Hyper-V integration components.</span></span> <span data-ttu-id="1c550-108">Una instancia de esta interfaz se obtiene creando una instancia del CLSID **397a2e5f-348c-482d-b9a3-57d383b483cd** .</span><span class="sxs-lookup"><span data-stu-id="1c550-108">An instance of this interface is obtained by creating an instance of the **397a2e5f-348c-482d-b9a3-57d383b483cd** CLSID.</span></span>

## <a name="members"></a><span data-ttu-id="1c550-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1c550-109">Members</span></span>

<span data-ttu-id="1c550-110">La interfaz **IVmApplicationHealthMonitor** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="1c550-110">The **IVmApplicationHealthMonitor** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="1c550-111">**IVmApplicationHealthMonitor** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1c550-111">**IVmApplicationHealthMonitor** also has these types of members:</span></span>

-   [<span data-ttu-id="1c550-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c550-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1c550-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c550-113">Methods</span></span>

<span data-ttu-id="1c550-114">La interfaz **IVmApplicationHealthMonitor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1c550-114">The **IVmApplicationHealthMonitor** interface has these methods.</span></span>



| <span data-ttu-id="1c550-115">Método</span><span class="sxs-lookup"><span data-stu-id="1c550-115">Method</span></span>                                                                                   | <span data-ttu-id="1c550-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c550-116">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c550-117">**ResetAllApplicationState**</span><span class="sxs-lookup"><span data-stu-id="1c550-117">**ResetAllApplicationState**</span></span>](ivmapplicationhealthmonitor-resetallapplicationstate.md) | <span data-ttu-id="1c550-118">Restablece el estado de mantenimiento de todas las aplicaciones de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1c550-118">Resets the health state for all applications in a virtual machine.</span></span><br/>            |
| [<span data-ttu-id="1c550-119">**SetApplicationState**</span><span class="sxs-lookup"><span data-stu-id="1c550-119">**SetApplicationState**</span></span>](ivmapplicationhealthmonitor-setapplicationstate.md)           | <span data-ttu-id="1c550-120">Establece el estado de mantenimiento de una aplicación que se ejecuta en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1c550-120">Sets the health state of an application that is running in a virtual machine.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1c550-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c550-121">Remarks</span></span>

<span data-ttu-id="1c550-122">Para usar este elemento de programación, los componentes de integración de Windows 8 deben estar instalados en la máquina virtual en la que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1c550-122">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c550-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c550-123">Requirements</span></span>



| <span data-ttu-id="1c550-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c550-124">Requirement</span></span> | <span data-ttu-id="1c550-125">Value</span><span class="sxs-lookup"><span data-stu-id="1c550-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c550-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c550-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1c550-127">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c550-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="1c550-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c550-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1c550-129">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c550-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                                                                                           |
| <span data-ttu-id="1c550-130">Versión</span><span class="sxs-lookup"><span data-stu-id="1c550-130">Version</span></span><br/>                  | <span data-ttu-id="1c550-131">Componentes de integración para Windows 8</span><span class="sxs-lookup"><span data-stu-id="1c550-131">Integration components for Windows 8</span></span><br/>                                                                                                                                |
| <span data-ttu-id="1c550-132">IDL</span><span class="sxs-lookup"><span data-stu-id="1c550-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1c550-133"><dt>VmApplicationHealthMonitor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1c550-133"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="1c550-134">IID</span><span class="sxs-lookup"><span data-stu-id="1c550-134">IID</span></span><br/>                      | <span data-ttu-id="1c550-135">IID \_ IVmApplicationHealthMonitor se define como 267a0284-848f-447e-a096-5e10a1a76bca</span><span class="sxs-lookup"><span data-stu-id="1c550-135">IID\_IVmApplicationHealthMonitor is defined as 267a0284-848f-447e-a096-5e10a1a76bca</span></span><br/> <span data-ttu-id="1c550-136">El identificador de objeto se define como 397a2e5f-348c-482d-b9a3-57d383b483cd</span><span class="sxs-lookup"><span data-stu-id="1c550-136">Object Identifier is defined as 397a2e5f-348c-482d-b9a3-57d383b483cd</span></span><br/> |



 

