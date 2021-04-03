---
description: Determina si el sistema virtual especificado se puede migrar.
ms.assetid: 1bf1b385-162e-41c9-a408-f7ee755a9646
title: Método CheckVirtualSystemIsMigratable de la clase Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratable
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1aed843f3f0f4c6c30eb6125cdd5859cdba902d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907705"
---
# <a name="checkvirtualsystemismigratable-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="dcf21-103">Método CheckVirtualSystemIsMigratable de la \_ clase VirtualSystemMigrationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="dcf21-103">CheckVirtualSystemIsMigratable method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="dcf21-104">Determina si el sistema virtual especificado se puede migrar.</span><span class="sxs-lookup"><span data-stu-id="dcf21-104">Determines whether the specified virtual system can be migrated.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcf21-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dcf21-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratable(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="dcf21-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcf21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcf21-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dcf21-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf21-108">Referencia a una instancia de la clase [**de \_ ComputerSystem de CIM**](cim-computersystem.md) que representa la máquina virtual de la que se va a probar la capacidad de migración.</span><span class="sxs-lookup"><span data-stu-id="dcf21-108">A reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="dcf21-109">*DestinationHost* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dcf21-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf21-110">Nombre del sistema host para la migración.</span><span class="sxs-lookup"><span data-stu-id="dcf21-110">The name of the host system for the migration.</span></span> <span data-ttu-id="dcf21-111">El formato de este nombre se especifica mediante la propiedad **DestinationHostFormatsSupported** de la clase [**MSVM \_ VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) asociada a esta clase.</span><span class="sxs-lookup"><span data-stu-id="dcf21-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="dcf21-112">*MigrationSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dcf21-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf21-113">Instancia insertada de la clase [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) que representa la configuración de la operación de migración.</span><span class="sxs-lookup"><span data-stu-id="dcf21-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="dcf21-114">*NewSystemSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dcf21-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf21-115">Instancia insertada de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa las nuevas propiedades aplicables al sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="dcf21-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="dcf21-116">*NewResourceSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dcf21-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf21-117">Matriz de cadenas que contiene una instancia incrustada de la clase [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que representa las nuevas propiedades aplicables a los recursos virtuales del sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="dcf21-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="dcf21-118">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="dcf21-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf21-119">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dcf21-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcf21-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcf21-120">Return value</span></span>

<span data-ttu-id="dcf21-121">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="dcf21-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="dcf21-122">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="dcf21-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dcf21-123">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="dcf21-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dcf21-124">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="dcf21-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dcf21-125">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="dcf21-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dcf21-126">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="dcf21-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dcf21-127">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="dcf21-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dcf21-128">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="dcf21-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dcf21-129">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="dcf21-129">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dcf21-130">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="dcf21-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dcf21-131">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="dcf21-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dcf21-132">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="dcf21-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dcf21-133">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="dcf21-133">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dcf21-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcf21-134">Requirements</span></span>



| <span data-ttu-id="dcf21-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcf21-135">Requirement</span></span> | <span data-ttu-id="dcf21-136">Value</span><span class="sxs-lookup"><span data-stu-id="dcf21-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf21-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcf21-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dcf21-138">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="dcf21-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dcf21-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcf21-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dcf21-140">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="dcf21-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dcf21-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dcf21-141">Namespace</span></span><br/>                | <span data-ttu-id="dcf21-142">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="dcf21-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dcf21-143">MOF</span><span class="sxs-lookup"><span data-stu-id="dcf21-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcf21-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcf21-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dcf21-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dcf21-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcf21-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dcf21-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dcf21-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcf21-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcf21-148">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="dcf21-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

