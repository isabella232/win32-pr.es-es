---
description: Determina si el sistema virtual especificado se puede migrar a un host de destino especificado por un nombre de red o una dirección IP.
ms.assetid: eacc8448-4683-48df-81b9-8599292944db
title: Método CheckVirtualSystemIsMigratableToHost de la clase Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b81f6562f892acbaa5bf7ff7f4f3c772574bd96d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687355"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="51079-103">Método CheckVirtualSystemIsMigratableToHost de la \_ clase VirtualSystemMigrationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="51079-103">CheckVirtualSystemIsMigratableToHost method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="51079-104">Determina si el sistema virtual especificado se puede migrar a un host de destino especificado por un nombre de red o una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="51079-104">Determines whether the specified virtual system can be migrated to a target host specified by a network name or IP address.</span></span>

## <a name="syntax"></a><span data-ttu-id="51079-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51079-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  string                  DestinationHost,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="51079-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51079-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51079-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51079-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51079-108">Una referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa la máquina virtual para probar la capacidad de migración de.</span><span class="sxs-lookup"><span data-stu-id="51079-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="51079-109">*DestinationHost* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51079-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51079-110">Nombre del sistema host para la migración.</span><span class="sxs-lookup"><span data-stu-id="51079-110">The name of the host system for the migration.</span></span> <span data-ttu-id="51079-111">El formato de este nombre se especifica mediante la propiedad **DestinationHostFormatsSupported** de la clase [**MSVM \_ VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) asociada a esta clase.</span><span class="sxs-lookup"><span data-stu-id="51079-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="51079-112">*MigrationSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51079-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51079-113">Instancia insertada de la clase [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) que representa la configuración de la operación de migración.</span><span class="sxs-lookup"><span data-stu-id="51079-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="51079-114">*NewSystemSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51079-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51079-115">Instancia insertada de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa las nuevas propiedades aplicables al sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="51079-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="51079-116">*NewResourceSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51079-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51079-117">Matriz de cadenas que contiene una instancia incrustada de la clase [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que representa las nuevas propiedades aplicables a los recursos virtuales del sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="51079-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="51079-118">*IsMigratable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="51079-118">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51079-119">Recibe el resultado de la comprobación de la migración que indica si el sistema virtual se puede migrar correctamente.</span><span class="sxs-lookup"><span data-stu-id="51079-119">Receives the migration check result indicating whether the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51079-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51079-120">Return value</span></span>

<span data-ttu-id="51079-121">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="51079-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="51079-122">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="51079-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="51079-123">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="51079-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="51079-124">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="51079-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="51079-125">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="51079-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="51079-126">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="51079-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="51079-127">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="51079-127">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="51079-128">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="51079-128">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="51079-129">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="51079-129">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="51079-130">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="51079-130">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="51079-131">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="51079-131">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="51079-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51079-132">Requirements</span></span>



| <span data-ttu-id="51079-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="51079-133">Requirement</span></span> | <span data-ttu-id="51079-134">Value</span><span class="sxs-lookup"><span data-stu-id="51079-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51079-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51079-135">Minimum supported client</span></span><br/> | <span data-ttu-id="51079-136">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="51079-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="51079-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51079-137">Minimum supported server</span></span><br/> | <span data-ttu-id="51079-138">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="51079-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="51079-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="51079-139">Namespace</span></span><br/>                | <span data-ttu-id="51079-140">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="51079-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="51079-141">MOF</span><span class="sxs-lookup"><span data-stu-id="51079-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51079-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51079-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="51079-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="51079-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51079-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="51079-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="51079-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="51079-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51079-146">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="51079-146">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




