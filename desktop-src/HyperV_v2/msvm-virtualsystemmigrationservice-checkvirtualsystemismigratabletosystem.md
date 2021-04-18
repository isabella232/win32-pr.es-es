---
description: Determina si el sistema virtual especificado se puede migrar a un sistema de destino.
ms.assetid: 2E340737-DEE9-4853-ACD8-BEE2A8C69D6D
title: Método CheckVirtualSystemIsMigratableToSystem de la clase Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3e8f294f7e30740e3afab8987c734dbbdbd12acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686577"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="716c1-103">Método CheckVirtualSystemIsMigratableToSystem de la \_ clase VirtualSystemMigrationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="716c1-103">CheckVirtualSystemIsMigratableToSystem method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="716c1-104">Determina si el sistema virtual especificado se puede migrar a un sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="716c1-104">Determines whether the specified virtual system can be migrated to a destination system.</span></span>

## <a name="syntax"></a><span data-ttu-id="716c1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="716c1-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  Msvm_ComputerSystem REF DestinationSystem,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="716c1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="716c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="716c1-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="716c1-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="716c1-108">Una referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa la máquina virtual para probar la capacidad de migración de.</span><span class="sxs-lookup"><span data-stu-id="716c1-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="716c1-109">*DestinationSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="716c1-109">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="716c1-110">Una referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa la máquina virtual en la que se va a probar la capacidad de migración.</span><span class="sxs-lookup"><span data-stu-id="716c1-110">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability to.</span></span>

</dd> <dt>

<span data-ttu-id="716c1-111">*MigrationSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="716c1-111">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="716c1-112">Instancia insertada de la clase [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) que representa la configuración de la operación de migración.</span><span class="sxs-lookup"><span data-stu-id="716c1-112">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="716c1-113">*NewSystemSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="716c1-113">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="716c1-114">Instancia insertada de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa las nuevas propiedades aplicables al sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="716c1-114">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="716c1-115">*NewResourceSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="716c1-115">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="716c1-116">Matriz de cadenas que contiene una instancia incrustada de la clase [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que representa las nuevas propiedades aplicables a los recursos virtuales del sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="716c1-116">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="716c1-117">*IsMigratable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="716c1-117">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="716c1-118">Recibe el resultado de la comprobación de la migración que indica si el sistema virtual se puede migrar correctamente.</span><span class="sxs-lookup"><span data-stu-id="716c1-118">Receives the migration check result indicating whether the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="716c1-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="716c1-119">Return value</span></span>

<span data-ttu-id="716c1-120">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="716c1-120">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="716c1-121">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="716c1-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="716c1-122">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="716c1-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="716c1-123">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="716c1-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="716c1-124">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="716c1-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="716c1-125">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="716c1-125">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="716c1-126">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="716c1-126">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="716c1-127">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="716c1-127">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="716c1-128">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="716c1-128">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="716c1-129">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="716c1-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="716c1-130">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="716c1-130">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="716c1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="716c1-131">Requirements</span></span>



| <span data-ttu-id="716c1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="716c1-132">Requirement</span></span> | <span data-ttu-id="716c1-133">Value</span><span class="sxs-lookup"><span data-stu-id="716c1-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="716c1-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="716c1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="716c1-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="716c1-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="716c1-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="716c1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="716c1-137">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="716c1-137">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="716c1-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="716c1-138">Namespace</span></span><br/>                | <span data-ttu-id="716c1-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="716c1-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="716c1-140">MOF</span><span class="sxs-lookup"><span data-stu-id="716c1-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="716c1-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="716c1-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="716c1-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="716c1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="716c1-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="716c1-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="716c1-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="716c1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="716c1-145">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="716c1-145">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




