---
description: 'Más información sobre: método CheckVirtualSystemIsMigratableToSystem de la clase CIM_VirtualSystemMigrationService'
ms.assetid: d3f7c926-804f-4c7c-8964-a8e464155417
title: Método CheckVirtualSystemIsMigratableToSystem de la clase CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: be85c51cb507fea3cea14f1706ffa8f67af06c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687399"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="64df6-103">Método CheckVirtualSystemIsMigratableToSystem de la \_ clase VirtualSystemMigrationService de CIM</span><span class="sxs-lookup"><span data-stu-id="64df6-103">CheckVirtualSystemIsMigratableToSystem method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="64df6-104">Método para realizar una comprobación previa para determinar si es probable que un sistema virtual se migre correctamente a un sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="64df6-104">Method to perform a pre-check to determine whether a virtual system is likely to be successfully migrated to a target system.</span></span> <span data-ttu-id="64df6-105">Este método no garantiza que una migración posterior se realice siempre correctamente, debido a la disponibilidad dinámica de los recursos.</span><span class="sxs-lookup"><span data-stu-id="64df6-105">This method does not guarantee that a subsequent migration will always succeed, due to dynamic resource availability.</span></span> <span data-ttu-id="64df6-106">Descripción del código de retorno:</span><span class="sxs-lookup"><span data-stu-id="64df6-106">Return code description:</span></span>

## <a name="syntax"></a><span data-ttu-id="64df6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64df6-107">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="64df6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64df6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64df6-109">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64df6-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64df6-110">[**CIM \_**](cim-computersystem.md) Instancia de ComputerSystem que hace referencia al sistema del equipo virtual de origen que se va a migrar.</span><span class="sxs-lookup"><span data-stu-id="64df6-110">[**CIM\_ComputerSystem**](cim-computersystem.md) instance referencing the source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="64df6-111">*DestinationSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64df6-111">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64df6-112">[**CIM \_ Instancia del sistema**](cim-system.md) que hace referencia al sistema de destino en el que se va a migrar el sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="64df6-112">[**CIM\_System**](cim-system.md) instance referencing the destination system onto which to migrate the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="64df6-113">*MigrationSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64df6-113">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64df6-114">Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) que representa la configuración de migración aplicable a la operación de migración.</span><span class="sxs-lookup"><span data-stu-id="64df6-114">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="64df6-115">*NewSystemSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64df6-115">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64df6-116">Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa las nuevas propiedades aplicables al sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="64df6-116">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="64df6-117">*NewResourceSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="64df6-117">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64df6-118">Matriz de cadenas que contiene una instancia incrustada de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa las nuevas propiedades aplicables a los recursos virtuales en el ámbito del sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="64df6-118">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="64df6-119">*IsMigratable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="64df6-119">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64df6-120">Resultado de la comprobación de la migración que indica si el sistema virtual se puede migrar correctamente.</span><span class="sxs-lookup"><span data-stu-id="64df6-120">The migration check result indicating whether or not the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64df6-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64df6-121">Return value</span></span>

<span data-ttu-id="64df6-122">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="64df6-122">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="64df6-123">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64df6-123">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="64df6-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="64df6-124">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="64df6-125"><dt>**Completado sin error**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="64df6-125"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="64df6-126">Comprobación realizada; resultado indicado a través del valor del \[ parámetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="64df6-126">Check performed; result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="64df6-127"><dt>**No compatible**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="64df6-127"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="64df6-128">Método no admitido por la implementación de.</span><span class="sxs-lookup"><span data-stu-id="64df6-128">Method not supported by implementation.</span></span> <span data-ttu-id="64df6-129">No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="64df6-129">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="64df6-130"><dt>**Error**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="64df6-130"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="64df6-131">Error al comprobar los motivos no especificados.</span><span class="sxs-lookup"><span data-stu-id="64df6-131">Check failed for unspecified reasons.</span></span> <span data-ttu-id="64df6-132">No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="64df6-132">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="64df6-133"><dt>**Tiempo de espera**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="64df6-133"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                    | <span data-ttu-id="64df6-134">Se agotó el tiempo de espera de la comprobación. No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="64df6-134">Check timed out. No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="64df6-135"><dt>**Parámetro 4 no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="64df6-135"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="64df6-136">Uno o más parámetros no son válidos formalmente.</span><span class="sxs-lookup"><span data-stu-id="64df6-136">One or more parameters are formally invalid.</span></span> <span data-ttu-id="64df6-137">Por ejemplo, el valor del parámetro *DestinationSystem* no incluye una ruta de acceso de objeto válida.</span><span class="sxs-lookup"><span data-stu-id="64df6-137">For example, the value of the *DestinationSystem* parameter does not comprise a valid object path.</span></span> <span data-ttu-id="64df6-138">No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="64df6-138">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="64df6-139"><dt>**Estado 5 no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="64df6-139"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>              | <span data-ttu-id="64df6-140">El sistema virtual de origen, el sistema host de origen o el sistema host de destino están en un estado que permite la iniciación de la migración del sistema virtual solicitada. puede tratarse de una condición temporal.</span><span class="sxs-lookup"><span data-stu-id="64df6-140">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span> <span data-ttu-id="64df6-141">No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="64df6-141">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="64df6-142"><dt>**Parámetros no compatibles**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="64df6-142"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>    | <span data-ttu-id="64df6-143">Uno o varios parámetros de entrada no son compatibles como un conjunto o con respecto al host de destino.</span><span class="sxs-lookup"><span data-stu-id="64df6-143">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="64df6-144">Por ejemplo, el valor del parámetro *NewSettingData* contiene propiedades que no son compatibles con el sistema host de destino identificado por el valor del parámetro *DestinationSystem* .</span><span class="sxs-lookup"><span data-stu-id="64df6-144">For example the value of the *NewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationSystem* parameter.</span></span> <span data-ttu-id="64df6-145">No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="64df6-145">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="64df6-146"><dt>**DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="64df6-146"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="64df6-147"><dt>**Método reservado**</dt> <dt>.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="64df6-147"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="64df6-148">32768 <dt>**específico del proveedor**</dt> <dt>... 65535</dt></span><span class="sxs-lookup"><span data-stu-id="64df6-148"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="64df6-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64df6-149">Requirements</span></span>



| <span data-ttu-id="64df6-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="64df6-150">Requirement</span></span> | <span data-ttu-id="64df6-151">Value</span><span class="sxs-lookup"><span data-stu-id="64df6-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64df6-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64df6-152">Minimum supported client</span></span><br/> | <span data-ttu-id="64df6-153">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="64df6-153">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="64df6-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64df6-154">Minimum supported server</span></span><br/> | <span data-ttu-id="64df6-155">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="64df6-155">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="64df6-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="64df6-156">Namespace</span></span><br/>                | <span data-ttu-id="64df6-157">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="64df6-157">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="64df6-158">MOF</span><span class="sxs-lookup"><span data-stu-id="64df6-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64df6-159"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64df6-159"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="64df6-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="64df6-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64df6-161"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64df6-161"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="64df6-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="64df6-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64df6-163">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="64df6-163">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




