---
description: Mueve, migra o reubica un sistema virtual en un sistema de destino.
ms.assetid: 3a0be791-4514-4ce2-b4e8-3735bd6ea1d7
title: Método MigrateVirtualSystemToSystem de la clase Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a346596b094b60456af8e2b63865bec1171d99ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360593"
---
# <a name="migratevirtualsystemtosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="e6484-103">Método MigrateVirtualSystemToSystem de la \_ clase VirtualSystemMigrationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="e6484-103">MigrateVirtualSystemToSystem method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="e6484-104">Mueve, migra o reubica un sistema virtual en un sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="e6484-104">Moves, migrates, or relocates a virtual system to a target system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6484-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6484-105">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ComputerSystem REF NewComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e6484-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6484-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6484-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6484-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6484-108">Una referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa el sistema del equipo virtual que se va a migrar.</span><span class="sxs-lookup"><span data-stu-id="e6484-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="e6484-109">*DestinationSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6484-109">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6484-110">Referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa el sistema al que se va a migrar.</span><span class="sxs-lookup"><span data-stu-id="e6484-110">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system to be migrated to.</span></span>

</dd> <dt>

<span data-ttu-id="e6484-111">*MigrationSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6484-111">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6484-112">Instancia insertada de la clase [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) que representa la configuración de la operación de migración.</span><span class="sxs-lookup"><span data-stu-id="e6484-112">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="e6484-113">*NewSystemSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6484-113">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6484-114">Instancia insertada de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa las nuevas propiedades aplicables al sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="e6484-114">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="e6484-115">*NewResourceSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e6484-115">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6484-116">Matriz de cadenas que contiene una instancia incrustada de la clase [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que representa las nuevas propiedades aplicables a los recursos virtuales del sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="e6484-116">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="e6484-117">*NewComputerSystem* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e6484-117">*NewComputerSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6484-118">Una referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa el nuevo sistema migrado.</span><span class="sxs-lookup"><span data-stu-id="e6484-118">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the new migrated system.</span></span>

</dd> <dt>

<span data-ttu-id="e6484-119">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e6484-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6484-120">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6484-120">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6484-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6484-121">Return value</span></span>

<span data-ttu-id="e6484-122">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e6484-122">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e6484-123">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="e6484-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e6484-124">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="e6484-124">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e6484-125">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="e6484-125">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e6484-126">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="e6484-126">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e6484-127">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="e6484-127">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e6484-128">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="e6484-128">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e6484-129">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="e6484-129">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e6484-130">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e6484-130">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e6484-131">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e6484-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e6484-132">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e6484-132">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="e6484-133">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="e6484-133">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e6484-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6484-134">Requirements</span></span>



| <span data-ttu-id="e6484-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6484-135">Requirement</span></span> | <span data-ttu-id="e6484-136">Value</span><span class="sxs-lookup"><span data-stu-id="e6484-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6484-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6484-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e6484-138">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e6484-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e6484-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6484-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e6484-140">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e6484-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6484-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e6484-141">Namespace</span></span><br/>                | <span data-ttu-id="e6484-142">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e6484-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e6484-143">MOF</span><span class="sxs-lookup"><span data-stu-id="e6484-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6484-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6484-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6484-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e6484-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6484-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6484-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e6484-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6484-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6484-148">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="e6484-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

