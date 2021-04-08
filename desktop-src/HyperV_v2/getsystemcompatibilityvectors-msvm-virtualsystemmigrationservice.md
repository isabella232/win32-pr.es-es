---
description: Obtiene una lista de instancias de CompatibilityVector de MSVM \_ que se pueden usar para comprobar la compatibilidad de host de la máquina virtual (VM).
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: 'Msvm_VirtualSystemMigrationService:: GetSystemCompatibilityVectors (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityVectors
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ef8a374d992468247f6dc8f914d7252e7cd2829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000964"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a><span data-ttu-id="2aab3-103">MSVM \_ VirtualSystemMigrationService:: GetSystemCompatibilityVectors (método)</span><span class="sxs-lookup"><span data-stu-id="2aab3-103">Msvm\_VirtualSystemMigrationService::GetSystemCompatibilityVectors method</span></span>

<span data-ttu-id="2aab3-104">Obtiene una lista de instancias de [**\_ CompatibilityVector de MSVM**](msvm-compatibilityvector.md) que se pueden usar para comprobar la compatibilidad de host de la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="2aab3-104">Gets a list of [**Msvm\_CompatibilityVector**](msvm-compatibilityvector.md) instances that can be used to check for virtual machine (VM) to host compatibility.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aab3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2aab3-105">Syntax</span></span>


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a><span data-ttu-id="2aab3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2aab3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aab3-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2aab3-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab3-108">Una referencia a una clase de [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa la máquina virtual para la que se van a recuperar los vectores de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="2aab3-108">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the VM to retrieve compatibility vectors for.</span></span> <span data-ttu-id="2aab3-109">Si este parámetro hace referencia al sistema del equipo host, los datos devueltos en el parámetro *CompatibilityVectors* se pueden usar para determinar si cualquiera de las máquinas virtuales del equipo host se puede migrar rápidamente a otro sistema de host.</span><span class="sxs-lookup"><span data-stu-id="2aab3-109">If this parameter refers to the hosting computer system, the data returned in the *CompatibilityVectors* parameter can be used to determine whether any of the VMs on the hosting computer system can be quickly migrated to another hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="2aab3-110">*CompatibilityVectors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2aab3-110">*CompatibilityVectors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab3-111">Una matriz de instancias de [**MSVM \_ CompatibilityVector**](msvm-compatibilityvector.md) que contiene la información de compatibilidad para las máquinas virtuales o el sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="2aab3-111">An array of [**Msvm\_CompatibilityVector**](msvm-compatibilityvector.md) instances that contain the compatibility info for the VMs or hosting computer system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aab3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2aab3-112">Return value</span></span>

<span data-ttu-id="2aab3-113">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2aab3-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2aab3-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="2aab3-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2aab3-115">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="2aab3-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2aab3-116">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="2aab3-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2aab3-117">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="2aab3-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2aab3-118">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="2aab3-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2aab3-119">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="2aab3-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2aab3-120">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="2aab3-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2aab3-121">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="2aab3-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2aab3-122">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="2aab3-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2aab3-123">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="2aab3-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2aab3-124">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="2aab3-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2aab3-125">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="2aab3-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2aab3-126">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="2aab3-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2aab3-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2aab3-127">Remarks</span></span>

<span data-ttu-id="2aab3-128">**GetSystemCompatibilityVectors** obtiene información de compatibilidad de una máquina virtual (VM) (cuando se ejecuta en un equipo de máquina virtual) o un host (cuando se ejecuta en un sistema de equipo host).</span><span class="sxs-lookup"><span data-stu-id="2aab3-128">**GetSystemCompatibilityVectors** gets compatibility info for a virtual machine (VM) (when run on a VM computer system) or a host (when run on a host computer system).</span></span> <span data-ttu-id="2aab3-129">La información de compatibilidad permanece opaca para el cliente, mientras que la información proporciona una manera de comparar la información de compatibilidad del host con la de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2aab3-129">The compatibility info remains opaque to the client while the info provides a way to compare the host compatibility info with that of the VM.</span></span>

## <a name="requirements"></a><span data-ttu-id="2aab3-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2aab3-130">Requirements</span></span>



| <span data-ttu-id="2aab3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2aab3-131">Requirement</span></span> | <span data-ttu-id="2aab3-132">Value</span><span class="sxs-lookup"><span data-stu-id="2aab3-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2aab3-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2aab3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2aab3-134">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="2aab3-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2aab3-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2aab3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2aab3-136">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2aab3-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2aab3-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2aab3-137">Namespace</span></span><br/>                | <span data-ttu-id="2aab3-138">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2aab3-138">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="2aab3-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2aab3-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2aab3-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2aab3-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2aab3-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2aab3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2aab3-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2aab3-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2aab3-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="2aab3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aab3-144">**MSVM \_ CompatibilityVector**</span><span class="sxs-lookup"><span data-stu-id="2aab3-144">**Msvm\_CompatibilityVector**</span></span>](msvm-compatibilityvector.md)
</dt> <dt>

[<span data-ttu-id="2aab3-145">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="2aab3-145">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




