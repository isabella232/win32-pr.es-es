---
description: Método para destinar, migrar o cambiar la ubicación de un sistema virtual a un sistema de destino.
ms.assetid: 210d31f1-093f-4fd5-afd7-5f028b4cb343
title: Método MigrateVirtualSystemToSystem de la clase CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1459d80785725914cbaa5dda5b81e8d2fabad5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909193"
---
# <a name="migratevirtualsystemtosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="7eb89-103">Método MigrateVirtualSystemToSystem de la \_ clase VirtualSystemMigrationService de CIM</span><span class="sxs-lookup"><span data-stu-id="7eb89-103">MigrateVirtualSystemToSystem method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="7eb89-104">Método para destinar, migrar o cambiar la ubicación de un sistema virtual a un sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="7eb89-104">Method to move, migrate or relocate a virtual system to a target system.</span></span>

<span data-ttu-id="7eb89-105">Descripción del código de retorno:</span><span class="sxs-lookup"><span data-stu-id="7eb89-105">Return code description:</span></span>

## <a name="syntax"></a><span data-ttu-id="7eb89-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7eb89-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="7eb89-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7eb89-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eb89-108">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7eb89-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb89-109">Sistema del equipo virtual de origen que se va a migrar.</span><span class="sxs-lookup"><span data-stu-id="7eb89-109">Source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="7eb89-110">*DestinationSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7eb89-110">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb89-111">Sistema host de destino en el que se migra el sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7eb89-111">Destination host system whereto migrate the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="7eb89-112">*MigrationSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7eb89-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb89-113">Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) que representa la configuración de migración aplicable a la operación de migración.</span><span class="sxs-lookup"><span data-stu-id="7eb89-113">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="7eb89-114">*NewSystemSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7eb89-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb89-115">Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa las nuevas propiedades aplicables al sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="7eb89-115">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="7eb89-116">*NewResourceSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7eb89-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb89-117">Matriz de cadenas que contiene una instancia incrustada de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa las nuevas propiedades aplicables a los recursos virtuales en el ámbito del sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="7eb89-117">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="7eb89-118">*NewComputerSystem* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7eb89-118">*NewComputerSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb89-119">Referencia a una instancia de la clase de [**\_ ComputerSystem de CIM**](cim-computersystem.md) que representa el sistema del equipo virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="7eb89-119">Reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class representing the virtual computer system after it has been migrated.</span></span>

</dd> <dt>

<span data-ttu-id="7eb89-120">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7eb89-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7eb89-121">Si la operación es de larga ejecución, opcionalmente se puede devolver un [**\_ ConcreteJob de CIM**](cim-concretejob.md) que represente el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7eb89-121">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eb89-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7eb89-122">Return value</span></span>

<span data-ttu-id="7eb89-123">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="7eb89-123">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="7eb89-124">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7eb89-124">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="7eb89-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="7eb89-125">Description</span></span>                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7eb89-126"><dt>**Completado sin error**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7eb89-126"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="7eb89-127">Se migró el sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7eb89-127">Virtual system was migrated.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="7eb89-128"><dt>**No compatible**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7eb89-128"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="7eb89-129">Método no admitido por la implementación de.</span><span class="sxs-lookup"><span data-stu-id="7eb89-129">Method not supported by implementation.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="7eb89-130"><dt>**Error**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7eb89-130"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                                     | <span data-ttu-id="7eb89-131">No se pudo migrar el sistema virtual por motivos no especificados.</span><span class="sxs-lookup"><span data-stu-id="7eb89-131">Virtual system migration failed for unspecified reasons.</span></span><br/>                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="7eb89-132"><dt>**Tiempo de espera**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7eb89-132"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                                    | <span data-ttu-id="7eb89-133">Tiempo de espera de migración del sistema virtual; no se conoce el estado del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7eb89-133">Virtual system migration time out; the virtual system state is unknown.</span></span><br/>                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="7eb89-134"><dt>**Parámetro 4 no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7eb89-134"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="7eb89-135">Uno o más parámetros no son válidos formalmente; por ejemplo, el valor del parámetro de sistema de destino no contiene una ruta de acceso de objeto válida.</span><span class="sxs-lookup"><span data-stu-id="7eb89-135">One or more parameters are formally invalid For example, the value of the Destination System parameter does not contain a valid object path.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="7eb89-136"><dt>**Estado 5 no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7eb89-136"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>                              | <span data-ttu-id="7eb89-137">El sistema virtual de origen, el sistema host de origen o el sistema host de destino están en un estado que permite la iniciación de la migración del sistema virtual solicitada. puede tratarse de una condición temporal.</span><span class="sxs-lookup"><span data-stu-id="7eb89-137">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="7eb89-138"><dt>**Parámetros no compatibles**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7eb89-138"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>                    | <span data-ttu-id="7eb89-139">Uno o varios parámetros de entrada no son compatibles como un conjunto o con respecto al host de destino.</span><span class="sxs-lookup"><span data-stu-id="7eb89-139">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="7eb89-140">Por ejemplo, el valor del parámetro *MigrationNewSettingData* contiene propiedades que no son compatibles con el sistema host de destino identificado por el valor del parámetro *DestinationSystem* .</span><span class="sxs-lookup"><span data-stu-id="7eb89-140">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationSystem* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="7eb89-141"><dt>**DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="7eb89-141"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="7eb89-142"><dt>**Parámetros de método comprobados: trabajo iniciado**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="7eb89-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="7eb89-143"><dt>**Método reservado**</dt> <dt>.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="7eb89-143"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="7eb89-144">32768 <dt>**específico del proveedor**</dt> <dt>... 65535</dt></span><span class="sxs-lookup"><span data-stu-id="7eb89-144"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="7eb89-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eb89-145">Requirements</span></span>



| <span data-ttu-id="7eb89-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eb89-146">Requirement</span></span> | <span data-ttu-id="7eb89-147">Value</span><span class="sxs-lookup"><span data-stu-id="7eb89-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eb89-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7eb89-148">Minimum supported client</span></span><br/> | <span data-ttu-id="7eb89-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7eb89-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7eb89-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7eb89-150">Minimum supported server</span></span><br/> | <span data-ttu-id="7eb89-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7eb89-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7eb89-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7eb89-152">Namespace</span></span><br/>                | <span data-ttu-id="7eb89-153">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="7eb89-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7eb89-154">MOF</span><span class="sxs-lookup"><span data-stu-id="7eb89-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7eb89-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7eb89-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7eb89-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7eb89-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eb89-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7eb89-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7eb89-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="7eb89-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eb89-159">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="7eb89-159">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




