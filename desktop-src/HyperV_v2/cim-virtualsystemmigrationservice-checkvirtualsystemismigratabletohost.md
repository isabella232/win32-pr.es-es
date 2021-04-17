---
description: Método para realizar una comprobación previa para determinar si es probable que un sistema virtual se migre correctamente a un host de destino especificado por un nombre de red o una dirección IP.
ms.assetid: bfcd4063-30fe-4d18-9df9-7b84a680814c
title: Método CheckVirtualSystemIsMigratableToHost de la clase CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5769691a792b8f74225b640b0058ad4bd0e27c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687400"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="b2c48-103">Método CheckVirtualSystemIsMigratableToHost de la \_ clase VirtualSystemMigrationService de CIM</span><span class="sxs-lookup"><span data-stu-id="b2c48-103">CheckVirtualSystemIsMigratableToHost method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="b2c48-104">Método para realizar una comprobación previa para determinar si es probable que un sistema virtual se migre correctamente a un host de destino especificado por un nombre de red o una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="b2c48-104">Method to perform a pre-check to determine whether a virtual system is likely to be successfully migrated to a target host specified by a network name or IP address.</span></span> <span data-ttu-id="b2c48-105">Este método no garantiza que una migración posterior se realice siempre correctamente, debido a la disponibilidad dinámica de los recursos.</span><span class="sxs-lookup"><span data-stu-id="b2c48-105">This method does not guarantee that a subsequent migration will always succeed, due to dynamic resource availability.</span></span>

<span data-ttu-id="b2c48-106">Descripción del código de retorno:</span><span class="sxs-lookup"><span data-stu-id="b2c48-106">Return code description:</span></span>

<span data-ttu-id="b2c48-107">Nota: este método está pensado como una solución transitoria únicamente hasta que esté disponible el modelado de la compatibilidad con clústeres.</span><span class="sxs-lookup"><span data-stu-id="b2c48-107">Note: This method is intended as a transitional solution only until modeling of cluster support is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2c48-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2c48-108">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="b2c48-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2c48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2c48-110">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2c48-110">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c48-111">Una referencia de [**\_ ComputerSystem de CIM**](cim-computersystem.md) al sistema del equipo virtual de origen que se va a migrar.</span><span class="sxs-lookup"><span data-stu-id="b2c48-111">A [**CIM\_ComputerSystem**](cim-computersystem.md) reference to the source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="b2c48-112">*DestinationHost* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2c48-112">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c48-113">Sistema host de destino para la migración.</span><span class="sxs-lookup"><span data-stu-id="b2c48-113">Target host system for the migration.</span></span>

<span data-ttu-id="b2c48-114">Los formatos aceptables para este parámetro se transmiten a través de los valores de los elementos de la propiedad de matriz **DestinationHostFormatsSupported** \[ \] en la instancia de [**\_ VirtualSystemMigrationCapabilities de CIM**](cim-virtualsystemmigrationcapabilities.md) asociada a través de la Asociación [**\_ ElementCapabilities CIM**](cim-elementcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="b2c48-114">Acceptable formats for this parameter are conveyed through values of elements of the **DestinationHostFormatsSupported**\[ \] array property in the instance of the [**CIM\_VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) that is associated through the [**CIM\_ElementCapabilities**](cim-elementcapabilities.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="b2c48-115">*MigrationSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2c48-115">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c48-116">Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) que representa la configuración de migración aplicable a la operación de migración.</span><span class="sxs-lookup"><span data-stu-id="b2c48-116">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="b2c48-117">*NewSystemSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2c48-117">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c48-118">Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa las nuevas propiedades aplicables al sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="b2c48-118">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="b2c48-119">*NewResourceSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2c48-119">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c48-120">Matriz de cadenas que contiene una instancia incrustada de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa las nuevas propiedades aplicables a los recursos virtuales en el ámbito del sistema virtual después de su migración.</span><span class="sxs-lookup"><span data-stu-id="b2c48-120">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="b2c48-121">*IsMigratable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b2c48-121">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c48-122">Resultado de la comprobación de la migración que indica si el sistema virtual se puede migrar correctamente.</span><span class="sxs-lookup"><span data-stu-id="b2c48-122">The migration check result indicating whether or not the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2c48-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2c48-123">Return value</span></span>

<span data-ttu-id="b2c48-124">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="b2c48-124">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="b2c48-125">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2c48-125">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="b2c48-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2c48-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b2c48-127"><dt>**Completado sin error**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b2c48-127"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="b2c48-128">Comprobación realizada; resultado indicado a través del valor del \[ parámetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="b2c48-128">Check performed; result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="b2c48-129"><dt>**No compatible**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b2c48-129"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="b2c48-130">Método no admitido por la implementación de.</span><span class="sxs-lookup"><span data-stu-id="b2c48-130">Method not supported by implementation.</span></span> <span data-ttu-id="b2c48-131">No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="b2c48-131">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="b2c48-132"><dt>**Error**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b2c48-132"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="b2c48-133">Error al comprobar los motivos no especificados.</span><span class="sxs-lookup"><span data-stu-id="b2c48-133">Check failed for unspecified reasons.</span></span> <span data-ttu-id="b2c48-134">No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="b2c48-134">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="b2c48-135"><dt>**Tiempo de espera**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b2c48-135"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                    | <span data-ttu-id="b2c48-136">Se agotó el tiempo de espera de la comprobación. No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="b2c48-136">Check timed out. No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="b2c48-137"><dt>**Parámetro 4 no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b2c48-137"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="b2c48-138">Uno o más parámetros no son válidos formalmente.</span><span class="sxs-lookup"><span data-stu-id="b2c48-138">One or more parameters are formally invalid.</span></span> <span data-ttu-id="b2c48-139">Por ejemplo, se podría haber especificado el valor del parámetro *DestinationHost* en un formato no admitido.</span><span class="sxs-lookup"><span data-stu-id="b2c48-139">For example, the value of the *DestinationHost* parameter could have been specified in an unsupported format.</span></span> <span data-ttu-id="b2c48-140">No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="b2c48-140">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                    |
| <dl> <span data-ttu-id="b2c48-141"><dt>**Estado 5 no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b2c48-141"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>              | <span data-ttu-id="b2c48-142">El sistema virtual de origen, el sistema host de origen o el sistema host de destino están en un estado que permite la iniciación de la migración del sistema virtual solicitada. puede tratarse de una condición temporal.</span><span class="sxs-lookup"><span data-stu-id="b2c48-142">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span> <span data-ttu-id="b2c48-143">No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="b2c48-143">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="b2c48-144"><dt>**Parámetros no compatibles**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b2c48-144"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>    | <span data-ttu-id="b2c48-145">Uno o varios parámetros de entrada no son compatibles como un conjunto o con respecto al host de destino.</span><span class="sxs-lookup"><span data-stu-id="b2c48-145">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="b2c48-146">Por ejemplo, el valor del parámetro *MigrationNewSettingData* contiene propiedades que no son compatibles con el sistema host de destino identificado por el valor del parámetro *DestinationHost* .</span><span class="sxs-lookup"><span data-stu-id="b2c48-146">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationHost* parameter.</span></span> <span data-ttu-id="b2c48-147">No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="b2c48-147">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="b2c48-148"><dt>**DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="b2c48-148"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="b2c48-149"><dt>**Método reservado**</dt> <dt>.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="b2c48-149"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="b2c48-150">32768 <dt>**específico del proveedor**</dt> <dt>... 65535</dt></span><span class="sxs-lookup"><span data-stu-id="b2c48-150"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="b2c48-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2c48-151">Requirements</span></span>



| <span data-ttu-id="b2c48-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2c48-152">Requirement</span></span> | <span data-ttu-id="b2c48-153">Value</span><span class="sxs-lookup"><span data-stu-id="b2c48-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2c48-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2c48-154">Minimum supported client</span></span><br/> | <span data-ttu-id="b2c48-155">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b2c48-155">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b2c48-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2c48-156">Minimum supported server</span></span><br/> | <span data-ttu-id="b2c48-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b2c48-157">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b2c48-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b2c48-158">Namespace</span></span><br/>                | <span data-ttu-id="b2c48-159">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b2c48-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b2c48-160">MOF</span><span class="sxs-lookup"><span data-stu-id="b2c48-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2c48-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2c48-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2c48-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b2c48-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2c48-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2c48-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2c48-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2c48-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2c48-165">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b2c48-165">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




