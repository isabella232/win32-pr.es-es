---
description: Método para desplace, migre o cambie la ubicación de un sistema virtual a un host de destino especificado por un nombre de red o una dirección IP.
ms.assetid: 09fdc0b2-641c-47f5-b270-e26e3acf7ea5
title: Método MigrateVirtualSystemToHost de la clase CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1a90e3adadbb5efc5f9cae3b7710e07c1e05000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687398"
---
# <a name="migratevirtualsystemtohost-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="74aa5-103">Método MigrateVirtualSystemToHost de la \_ clase VirtualSystemMigrationService de CIM</span><span class="sxs-lookup"><span data-stu-id="74aa5-103">MigrateVirtualSystemToHost method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="74aa5-104">Método para desplace, migre o cambie la ubicación de un sistema virtual a un host de destino especificado por un nombre de red o una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="74aa5-104">Method to move, migrate or relocate a virtual system to a target host specified by a network name or IP address.</span></span>

> [!Note]  
> <span data-ttu-id="74aa5-105">Este método está pensado como una solución transitoria únicamente hasta que esté disponible el modelado de la compatibilidad con clústeres.</span><span class="sxs-lookup"><span data-stu-id="74aa5-105">This method is intended as a transitional solution only until modeling of cluster support is available.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="74aa5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74aa5-106">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="74aa5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74aa5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74aa5-108">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74aa5-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74aa5-109">Sistema del equipo virtual de origen que se va a migrar.</span><span class="sxs-lookup"><span data-stu-id="74aa5-109">Source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="74aa5-110">*DestinationHost* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74aa5-110">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74aa5-111">Sistema host de destino para la migración.</span><span class="sxs-lookup"><span data-stu-id="74aa5-111">Target host system for the migration.</span></span>

<span data-ttu-id="74aa5-112">Los formatos aceptables para este parámetro se transmiten a través de los valores de los elementos de la propiedad de matriz **DestinationHostFormatsSupported** \[ \] en la instancia de [**\_ VirtualSystemMigrationCapabilities de CIM**](cim-virtualsystemmigrationcapabilities.md) asociada a través de la Asociación [**\_ ElementCapabilities CIM**](cim-elementcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="74aa5-112">Acceptable formats for this parameter are conveyed through values of elements of the **DestinationHostFormatsSupported**\[ \] array property in the instance of the [**CIM\_VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) that is associated through the [**CIM\_ElementCapabilities**](cim-elementcapabilities.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="74aa5-113">*MigrationSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74aa5-113">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74aa5-114">Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) que representa la configuración de migración aplicable a la operación de migración.</span><span class="sxs-lookup"><span data-stu-id="74aa5-114">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="74aa5-115">*NewSystemSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74aa5-115">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74aa5-116">Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa las nuevas propiedades aplicables al sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="74aa5-116">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="74aa5-117">*NewResourceSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74aa5-117">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74aa5-118">Matriz de cadenas que contiene una instancia incrustada de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa las nuevas propiedades aplicables a los recursos virtuales en el ámbito del sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="74aa5-118">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="74aa5-119">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="74aa5-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74aa5-120">Si la operación es de larga ejecución, opcionalmente se puede devolver un [**\_ ConcreteJob de CIM**](cim-concretejob.md) que represente el trabajo.</span><span class="sxs-lookup"><span data-stu-id="74aa5-120">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74aa5-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74aa5-121">Return value</span></span>

<span data-ttu-id="74aa5-122">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="74aa5-122">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="74aa5-123">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74aa5-123">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="74aa5-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="74aa5-124">Description</span></span>                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74aa5-125"><dt>**Completado sin error**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="74aa5-125"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="74aa5-126">Se migró el sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="74aa5-126">Virtual system was migrated.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="74aa5-127"><dt>**No compatible**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="74aa5-127"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="74aa5-128">Método no admitido por la implementación de.</span><span class="sxs-lookup"><span data-stu-id="74aa5-128">Method not supported by implementation.</span></span><br/>                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="74aa5-129"><dt>**Error**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="74aa5-129"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                                     | <span data-ttu-id="74aa5-130">No se pudo migrar el sistema virtual por motivos no especificados.</span><span class="sxs-lookup"><span data-stu-id="74aa5-130">Virtual system migration failed for unspecified reasons.</span></span><br/>                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="74aa5-131"><dt>**Tiempo de espera**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="74aa5-131"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                                    | <span data-ttu-id="74aa5-132">Tiempo de espera de migración del sistema virtual; no se conoce el estado del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="74aa5-132">Virtual system migration time out; the virtual system state is unknown.</span></span><br/>                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="74aa5-133"><dt>**Parámetro 4 no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="74aa5-133"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="74aa5-134">Uno o más parámetros no son válidos formalmente.</span><span class="sxs-lookup"><span data-stu-id="74aa5-134">One or more parameters are formally invalid.</span></span> <span data-ttu-id="74aa5-135">Por ejemplo, se podría haber especificado el valor del parámetro *DestinationHost* en un formato no admitido.</span><span class="sxs-lookup"><span data-stu-id="74aa5-135">For example, the value of the *DestinationHost* parameter could have been specified in an unsupported format.</span></span><br/>                                                                                                                                    |
| <dl> <span data-ttu-id="74aa5-136"><dt>**Estado 5 no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="74aa5-136"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>                              | <span data-ttu-id="74aa5-137">El sistema virtual de origen, el sistema host de origen o el sistema host de destino están en un estado que permite la iniciación de la migración del sistema virtual solicitada. puede tratarse de una condición temporal.</span><span class="sxs-lookup"><span data-stu-id="74aa5-137">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="74aa5-138"><dt>**Parámetros no compatibles**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="74aa5-138"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>                    | <span data-ttu-id="74aa5-139">Uno o varios parámetros de entrada no son compatibles como un conjunto o con respecto al host de destino.</span><span class="sxs-lookup"><span data-stu-id="74aa5-139">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="74aa5-140">Por ejemplo, el valor del parámetro *MigrationNewSettingData* contiene propiedades que no son compatibles con el sistema host de destino identificado por el valor del parámetro *DestinationHost* .</span><span class="sxs-lookup"><span data-stu-id="74aa5-140">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationHost* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="74aa5-141"><dt>**DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="74aa5-141"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="74aa5-142"><dt>**Parámetros de método comprobados: trabajo iniciado**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="74aa5-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="74aa5-143"><dt>**Método reservado**</dt> <dt>.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="74aa5-143"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="74aa5-144">32768 <dt>**específico del proveedor**</dt> <dt>... 65535</dt></span><span class="sxs-lookup"><span data-stu-id="74aa5-144"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="74aa5-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74aa5-145">Requirements</span></span>



| <span data-ttu-id="74aa5-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="74aa5-146">Requirement</span></span> | <span data-ttu-id="74aa5-147">Value</span><span class="sxs-lookup"><span data-stu-id="74aa5-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74aa5-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74aa5-148">Minimum supported client</span></span><br/> | <span data-ttu-id="74aa5-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="74aa5-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="74aa5-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74aa5-150">Minimum supported server</span></span><br/> | <span data-ttu-id="74aa5-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="74aa5-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="74aa5-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="74aa5-152">Namespace</span></span><br/>                | <span data-ttu-id="74aa5-153">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="74aa5-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="74aa5-154">MOF</span><span class="sxs-lookup"><span data-stu-id="74aa5-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74aa5-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74aa5-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74aa5-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="74aa5-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74aa5-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74aa5-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="74aa5-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="74aa5-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74aa5-159">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="74aa5-159">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




