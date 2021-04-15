---
description: Esta clase representa un trabajo de operación de exportación de punto de referencia de colección.
ms.assetid: c752ff1d-163c-4aa9-b29e-76478a18a08c
title: Msvm_CollectionReferencePointExportJob (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob
- Msvm_CollectionReferencePointExportJob.Cancellable
- Msvm_CollectionReferencePointExportJob.ErrorSummaryDescription
- Msvm_CollectionReferencePointExportJob.CollectionId
- Msvm_CollectionReferencePointExportJob.ReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.BaseReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.VirtualMachineId
- Msvm_CollectionReferencePointExportJob.ExportDirectory
- Msvm_CollectionReferencePointExportJob.ExportedDisks
- Msvm_CollectionReferencePointExportJob.ExportedLogFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedConfigFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedRuntimeFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedGuestStateFilePaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d21fab1519664471bdc2bb5d7102d94cbe3dde1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688718"
---
# <a name="msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="f78c6-103">MSVM \_ CollectionReferencePointExportJob (clase)</span><span class="sxs-lookup"><span data-stu-id="f78c6-103">Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="f78c6-104">Esta clase representa un trabajo de operación de exportación de punto de referencia de colección.</span><span class="sxs-lookup"><span data-stu-id="f78c6-104">This class represents a collection reference point export operation job.</span></span>

<span data-ttu-id="f78c6-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f78c6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f78c6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f78c6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  CollectionId;
  string  ReferencePointGroupId;
  string  BaseReferencePointGroupId;
  string  VirtualMachineId[];
  string  ExportDirectory;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePaths[];
  string  ExportedRuntimeFilePaths[];
  string  ExportedGuestStateFilePaths[];
};
```

## <a name="members"></a><span data-ttu-id="f78c6-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f78c6-107">Members</span></span>

<span data-ttu-id="f78c6-108">La clase **MSVM \_ CollectionReferencePointExportJob** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f78c6-108">The **Msvm\_CollectionReferencePointExportJob** class has these types of members:</span></span>

-   [<span data-ttu-id="f78c6-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="f78c6-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="f78c6-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f78c6-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f78c6-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f78c6-111">Methods</span></span>

<span data-ttu-id="f78c6-112">La clase **MSVM \_ CollectionReferencePointExportJob** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f78c6-112">The **Msvm\_CollectionReferencePointExportJob** class has these methods.</span></span>



| <span data-ttu-id="f78c6-113">Método</span><span class="sxs-lookup"><span data-stu-id="f78c6-113">Method</span></span>                                                                                  | <span data-ttu-id="f78c6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f78c6-114">Description</span></span>                                        |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="f78c6-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="f78c6-115">**GetError**</span></span>](msvm-collectionreferencepointexportjob-geterror.md)                     | <span data-ttu-id="f78c6-116">Recupera un error.</span><span class="sxs-lookup"><span data-stu-id="f78c6-116">Retrieves an error.</span></span><br/>                     |
| [<span data-ttu-id="f78c6-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="f78c6-117">**GetErrorEx**</span></span>](msvm-collectionreferencepointexportjob-geterrorex.md)                 | <span data-ttu-id="f78c6-118">Recupera información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="f78c6-118">Retrieves additional error information.</span></span><br/> |
| [<span data-ttu-id="f78c6-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f78c6-119">**RequestStateChange**</span></span>](msvm-collectionreferencepointexportjob-requeststatechange.md) | <span data-ttu-id="f78c6-120">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="f78c6-120">Requests a state change.</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="f78c6-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f78c6-121">Properties</span></span>

<span data-ttu-id="f78c6-122">La clase **MSVM \_ CollectionReferencePointExportJob** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f78c6-122">The **Msvm\_CollectionReferencePointExportJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f78c6-123">**BaseReferencePointGroupId**</span><span class="sxs-lookup"><span data-stu-id="f78c6-123">**BaseReferencePointGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f78c6-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f78c6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f78c6-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f78c6-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f78c6-126">GUID del punto de referencia de colección que se usa como base en exportoperation.</span><span class="sxs-lookup"><span data-stu-id="f78c6-126">GUID of the collection reference point which is used as the base in the exportoperation.</span></span>

</dd> <dt>

<span data-ttu-id="f78c6-127">**Cancelable**</span><span class="sxs-lookup"><span data-stu-id="f78c6-127">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f78c6-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f78c6-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f78c6-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f78c6-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f78c6-130">Indica si se puede cancelar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f78c6-130">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="f78c6-131">El valor de esta propiedad no garantiza que una solicitud para cancelar el trabajo se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="f78c6-131">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="f78c6-132">**Recopilación**</span><span class="sxs-lookup"><span data-stu-id="f78c6-132">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f78c6-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f78c6-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f78c6-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f78c6-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f78c6-135">GUID del grupo de máquinas virtuales para el que los archivos de registro wereexported.</span><span class="sxs-lookup"><span data-stu-id="f78c6-135">GUID of the virtual machine group for which log files wereexported.</span></span>

</dd> <dt>

<span data-ttu-id="f78c6-136">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="f78c6-136">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f78c6-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f78c6-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f78c6-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f78c6-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f78c6-139">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabajo de CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="f78c6-139">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="f78c6-140">Contiene una descripción del Resumen de errores.</span><span class="sxs-lookup"><span data-stu-id="f78c6-140">Contains an error summary description.</span></span>

</dd> <dt>

<span data-ttu-id="f78c6-141">**ExportDirectory**</span><span class="sxs-lookup"><span data-stu-id="f78c6-141">**ExportDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f78c6-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f78c6-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f78c6-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f78c6-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f78c6-144">Ubicación de exportación.</span><span class="sxs-lookup"><span data-stu-id="f78c6-144">Export Location.</span></span>

</dd> <dt>

<span data-ttu-id="f78c6-145">**ExportedConfigFilePaths**</span><span class="sxs-lookup"><span data-stu-id="f78c6-145">**ExportedConfigFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f78c6-146">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="f78c6-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f78c6-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f78c6-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f78c6-148">Ruta de acceso del archivo de configuración de la máquina virtual exportada.</span><span class="sxs-lookup"><span data-stu-id="f78c6-148">Path of the exported virtual machine config file.</span></span>

</dd> <dt>

<span data-ttu-id="f78c6-149">**ExportedDisks**</span><span class="sxs-lookup"><span data-stu-id="f78c6-149">**ExportedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f78c6-150">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="f78c6-150">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f78c6-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f78c6-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f78c6-152">Identificadores de instancia de los discos virtuales para los que se exportaron los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="f78c6-152">Instance IDs of virtual disks for which log files were exported.</span></span>

</dd> <dt>

<span data-ttu-id="f78c6-153">**ExportedGuestStateFilePaths**</span><span class="sxs-lookup"><span data-stu-id="f78c6-153">**ExportedGuestStateFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f78c6-154">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="f78c6-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f78c6-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f78c6-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f78c6-156">Ruta de acceso del archivo de estado invitado de la máquina virtual exportada.</span><span class="sxs-lookup"><span data-stu-id="f78c6-156">Path of the exported virtual machine guest state file.</span></span>

> [!Note]  
> <span data-ttu-id="f78c6-157">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="f78c6-157">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="f78c6-158">**ExportedLogFilePaths**</span><span class="sxs-lookup"><span data-stu-id="f78c6-158">**ExportedLogFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f78c6-159">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="f78c6-159">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f78c6-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f78c6-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f78c6-161">Rutas de acceso de los archivos de registro que se exportaron.</span><span class="sxs-lookup"><span data-stu-id="f78c6-161">Paths of the log files which were exported.</span></span>

</dd> <dt>

<span data-ttu-id="f78c6-162">**ExportedRuntimeFilePaths**</span><span class="sxs-lookup"><span data-stu-id="f78c6-162">**ExportedRuntimeFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f78c6-163">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="f78c6-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f78c6-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f78c6-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f78c6-165">Ruta de acceso del archivo de estado de tiempo de ejecución de la máquina virtual exportado.</span><span class="sxs-lookup"><span data-stu-id="f78c6-165">Path of the exported virtual machine runtime state file.</span></span>

</dd> <dt>

<span data-ttu-id="f78c6-166">**ReferencePointGroupId**</span><span class="sxs-lookup"><span data-stu-id="f78c6-166">**ReferencePointGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f78c6-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f78c6-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f78c6-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f78c6-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f78c6-169">GUID del punto de referencia de la colección que se exporta.</span><span class="sxs-lookup"><span data-stu-id="f78c6-169">GUID of the collection reference point which is exported.</span></span>

</dd> <dt>

<span data-ttu-id="f78c6-170">**VirtualMachineId**</span><span class="sxs-lookup"><span data-stu-id="f78c6-170">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f78c6-171">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="f78c6-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f78c6-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f78c6-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f78c6-173">GUID de las máquinas virtuales para las que se ha realizado la operación de exportación.</span><span class="sxs-lookup"><span data-stu-id="f78c6-173">GUID of the virtual machines for which export operation has been performed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f78c6-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f78c6-174">Requirements</span></span>



| <span data-ttu-id="f78c6-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="f78c6-175">Requirement</span></span> | <span data-ttu-id="f78c6-176">Value</span><span class="sxs-lookup"><span data-stu-id="f78c6-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f78c6-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f78c6-177">Minimum supported client</span></span><br/> | <span data-ttu-id="f78c6-178">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="f78c6-178">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f78c6-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f78c6-179">Minimum supported server</span></span><br/> | <span data-ttu-id="f78c6-180">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f78c6-180">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f78c6-181">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f78c6-181">Namespace</span></span><br/>                | <span data-ttu-id="f78c6-182">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f78c6-182">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f78c6-183">MOF</span><span class="sxs-lookup"><span data-stu-id="f78c6-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f78c6-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f78c6-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f78c6-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f78c6-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f78c6-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f78c6-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f78c6-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="f78c6-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f78c6-188">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="f78c6-188">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

