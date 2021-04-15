---
title: Win32_RdvhManagement (clase)
description: Describe un servicio de administración de Escritorio remoto virtual (RDVH).
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Win32_RdvhManagement clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RdvhManagement de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RdvhManagement
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01e2cde81173035d00587782dc45d9ddeb66fcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676769"
---
# <a name="win32_rdvhmanagement-class"></a><span data-ttu-id="72d41-105">\_Clase Win32 RdvhManagement</span><span class="sxs-lookup"><span data-stu-id="72d41-105">Win32\_RdvhManagement class</span></span>

<span data-ttu-id="72d41-106">Describe un servicio de administración de Escritorio remoto virtual (RDVH).</span><span class="sxs-lookup"><span data-stu-id="72d41-106">Describes a Remote Desktop Virtual Host (RDVH) management service.</span></span>

<span data-ttu-id="72d41-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="72d41-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="72d41-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72d41-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_RdvhManagement
{
};
```

## <a name="members"></a><span data-ttu-id="72d41-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="72d41-109">Members</span></span>

<span data-ttu-id="72d41-110">La **clase \_ RdvhManagement de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="72d41-110">The **Win32\_RdvhManagement** class has these types of members:</span></span>

-   [<span data-ttu-id="72d41-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="72d41-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="72d41-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="72d41-112">Methods</span></span>

<span data-ttu-id="72d41-113">La clase **Win32 \_ RdvhManagement** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="72d41-113">The **Win32\_RdvhManagement** class has these methods.</span></span>



| <span data-ttu-id="72d41-114">Método</span><span class="sxs-lookup"><span data-stu-id="72d41-114">Method</span></span>                                                                                  | <span data-ttu-id="72d41-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="72d41-115">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72d41-116">**RdvCreateUserDiskTemplate**</span><span class="sxs-lookup"><span data-stu-id="72d41-116">**RdvCreateUserDiskTemplate**</span></span>](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | <span data-ttu-id="72d41-117">Crea una plantilla de disco de usuario de tamaño máximo especificado y en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="72d41-117">Creates User Disk Template of specified max size and at the specified location.</span></span> <span data-ttu-id="72d41-118">Todos los discos de usuario creados tendrán tamaños máximos que coincidan con el tamaño máximo de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="72d41-118">All User Disks created will have max sizes matching the Template's max size.</span></span><br/> |
| [<span data-ttu-id="72d41-119">**RdvMigrateVmToDifferentHost**</span><span class="sxs-lookup"><span data-stu-id="72d41-119">**RdvMigrateVmToDifferentHost**</span></span>](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | <span data-ttu-id="72d41-120">Inicia una migración en vivo de la máquina virtual en escenarios VDI.</span><span class="sxs-lookup"><span data-stu-id="72d41-120">Initiates a live migration of virtual machine in VDI scenarios</span></span><br/>                                                                                               |
| [<span data-ttu-id="72d41-121">**RdvCopyBaseVmLocally**</span><span class="sxs-lookup"><span data-stu-id="72d41-121">**RdvCopyBaseVmLocally**</span></span>](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | <span data-ttu-id="72d41-122">Copia localmente la ubicación de la máquina virtual base en Host de RDV Server</span><span class="sxs-lookup"><span data-stu-id="72d41-122">Copies Base VM location locally to RDV Host server</span></span><br/>                                                                                                           |
| [<span data-ttu-id="72d41-123">**RdvCreateUserDiskTemplate**</span><span class="sxs-lookup"><span data-stu-id="72d41-123">**RdvCreateUserDiskTemplate**</span></span>](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | <span data-ttu-id="72d41-124">Crea una plantilla de disco de usuario de tamaño máximo especificado y en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="72d41-124">Creates User Disk Template of specified max size and at the specified location.</span></span> <span data-ttu-id="72d41-125">Todos los discos de usuario creados tendrán tamaños máximos que coincidan con el tamaño máximo de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="72d41-125">All User Disks created will have max sizes matching the Template's max size.</span></span><br/> |
| [<span data-ttu-id="72d41-126">**RdvMigrateVmToDifferentHost**</span><span class="sxs-lookup"><span data-stu-id="72d41-126">**RdvMigrateVmToDifferentHost**</span></span>](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | <span data-ttu-id="72d41-127">Inicia una migración en vivo de la máquina virtual en escenarios VDI.</span><span class="sxs-lookup"><span data-stu-id="72d41-127">Initiates a live migration of virtual machine in VDI scenarios.</span></span><br/>                                                                                              |
| [<span data-ttu-id="72d41-128">**RdvSetupVMPermissions**</span><span class="sxs-lookup"><span data-stu-id="72d41-128">**RdvSetupVMPermissions**</span></span>](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | <span data-ttu-id="72d41-129">Establece permisos en la máquina virtual para el autor de la llamada</span><span class="sxs-lookup"><span data-stu-id="72d41-129">Sets permissions in VM for the caller</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="72d41-130">**RdvUndoVMPermissions**</span><span class="sxs-lookup"><span data-stu-id="72d41-130">**RdvUndoVMPermissions**</span></span>](rdvundovmpermissions-win32-rdvhmanagement.md)               | <span data-ttu-id="72d41-131">Revierte los permisos de la máquina virtual establecida por RdvSetupVMPermissions</span><span class="sxs-lookup"><span data-stu-id="72d41-131">Reverts permissions in VM set by RdvSetupVMPermissions</span></span><br/>                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="72d41-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72d41-132">Requirements</span></span>



| <span data-ttu-id="72d41-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="72d41-133">Requirement</span></span> | <span data-ttu-id="72d41-134">Value</span><span class="sxs-lookup"><span data-stu-id="72d41-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="72d41-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72d41-135">Minimum supported client</span></span><br/> | <span data-ttu-id="72d41-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="72d41-136">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="72d41-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72d41-137">Minimum supported server</span></span><br/> | <span data-ttu-id="72d41-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72d41-138">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="72d41-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="72d41-139">Namespace</span></span><br/>                | <span data-ttu-id="72d41-140">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="72d41-140">Root\\cimv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="72d41-141">MOF</span><span class="sxs-lookup"><span data-stu-id="72d41-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72d41-142"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72d41-142"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="72d41-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="72d41-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72d41-144"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72d41-144"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

 





