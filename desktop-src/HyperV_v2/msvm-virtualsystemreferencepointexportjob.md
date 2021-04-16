---
description: Esta clase representa un trabajo de operación de exportación de punto de referencia del sistema virtual.
ms.assetid: 3d8e117c-4863-441a-9264-c33f05fbc5ef
title: Msvm_VirtualSystemReferencePointExportJob (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob
- Msvm_VirtualSystemReferencePointExportJob.Cancellable
- Msvm_VirtualSystemReferencePointExportJob.ErrorSummaryDescription
- Msvm_VirtualSystemReferencePointExportJob.ExportDirectory
- Msvm_VirtualSystemReferencePointExportJob.VirtualMachineId
- Msvm_VirtualSystemReferencePointExportJob.ReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.BaseReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.ExportedDisks
- Msvm_VirtualSystemReferencePointExportJob.ExportedLogFilePaths
- Msvm_VirtualSystemReferencePointExportJob.ExportedConfigFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedRuntimeFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedGuestStateFilePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04b5d8f27efae4817062917541af9bb488cec32c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547294"
---
# <a name="msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="f14bb-103">MSVM \_ VirtualSystemReferencePointExportJob (clase)</span><span class="sxs-lookup"><span data-stu-id="f14bb-103">Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="f14bb-104">Esta clase representa un trabajo de operación de exportación de punto de referencia del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="f14bb-104">This class represents a virtual system reference point export operation job.</span></span>

<span data-ttu-id="f14bb-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f14bb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f14bb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f14bb-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  ExportDirectory;
  string  VirtualMachineId;
  string  ReferencePointId;
  string  BaseReferencePointId;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePath;
  string  ExportedRuntimeFilePath;
  string  ExportedGuestStateFilePath;
};
```

## <a name="members"></a><span data-ttu-id="f14bb-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f14bb-107">Members</span></span>

<span data-ttu-id="f14bb-108">La clase **MSVM \_ VirtualSystemReferencePointExportJob** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f14bb-108">The **Msvm\_VirtualSystemReferencePointExportJob** class has these types of members:</span></span>

-   [<span data-ttu-id="f14bb-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="f14bb-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="f14bb-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f14bb-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f14bb-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f14bb-111">Methods</span></span>

<span data-ttu-id="f14bb-112">La clase **MSVM \_ VirtualSystemReferencePointExportJob** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f14bb-112">The **Msvm\_VirtualSystemReferencePointExportJob** class has these methods.</span></span>



| <span data-ttu-id="f14bb-113">Método</span><span class="sxs-lookup"><span data-stu-id="f14bb-113">Method</span></span>                                                                                     | <span data-ttu-id="f14bb-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f14bb-114">Description</span></span>                                        |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="f14bb-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="f14bb-115">**GetError**</span></span>](msvm-virtualsystemreferencepointexportjob-geterror.md)                     | <span data-ttu-id="f14bb-116">Recupera el error.</span><span class="sxs-lookup"><span data-stu-id="f14bb-116">Retrieves the error.</span></span><br/>                    |
| [<span data-ttu-id="f14bb-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="f14bb-117">**GetErrorEx**</span></span>](msvm-virtualsystemreferencepointexportjob-geterrorex.md)                 | <span data-ttu-id="f14bb-118">Recupera información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="f14bb-118">Retrieves additional error information.</span></span><br/> |
| [<span data-ttu-id="f14bb-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f14bb-119">**RequestStateChange**</span></span>](msvm-virtualsystemreferencepointexportjob-requeststatechange.md) | <span data-ttu-id="f14bb-120">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="f14bb-120">Requests a state change.</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="f14bb-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f14bb-121">Properties</span></span>

<span data-ttu-id="f14bb-122">La clase **MSVM \_ VirtualSystemReferencePointExportJob** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f14bb-122">The **Msvm\_VirtualSystemReferencePointExportJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f14bb-123">**BaseReferencePointId**</span><span class="sxs-lookup"><span data-stu-id="f14bb-123">**BaseReferencePointId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f14bb-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f14bb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f14bb-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f14bb-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f14bb-126">GUID del punto de referencia que se utiliza como base en la operación de exportación.</span><span class="sxs-lookup"><span data-stu-id="f14bb-126">GUID of the reference point which is used as the base in the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="f14bb-127">**Cancelable**</span><span class="sxs-lookup"><span data-stu-id="f14bb-127">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f14bb-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f14bb-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f14bb-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f14bb-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f14bb-130">Indica si se puede cancelar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f14bb-130">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="f14bb-131">El valor de esta propiedad no garantiza que una solicitud para cancelar el trabajo se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="f14bb-131">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="f14bb-132">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="f14bb-132">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f14bb-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f14bb-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f14bb-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f14bb-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f14bb-135">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabajo de CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="f14bb-135">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="f14bb-136">Contiene una descripción del Resumen de errores.</span><span class="sxs-lookup"><span data-stu-id="f14bb-136">Contains an error summary description.</span></span>

</dd> <dt>

<span data-ttu-id="f14bb-137">**ExportDirectory**</span><span class="sxs-lookup"><span data-stu-id="f14bb-137">**ExportDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f14bb-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f14bb-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f14bb-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f14bb-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f14bb-140">La ubicación de exportación.</span><span class="sxs-lookup"><span data-stu-id="f14bb-140">The export location.</span></span>

</dd> <dt>

<span data-ttu-id="f14bb-141">**ExportedConfigFilePath**</span><span class="sxs-lookup"><span data-stu-id="f14bb-141">**ExportedConfigFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f14bb-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f14bb-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f14bb-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f14bb-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f14bb-144">Ruta de acceso del archivo de configuración exportado.</span><span class="sxs-lookup"><span data-stu-id="f14bb-144">Path of the exported config file.</span></span>

</dd> <dt>

<span data-ttu-id="f14bb-145">**ExportedDisks**</span><span class="sxs-lookup"><span data-stu-id="f14bb-145">**ExportedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f14bb-146">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="f14bb-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f14bb-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f14bb-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f14bb-148">Identificadores de instancia de los discos virtuales para los que se exportaron los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="f14bb-148">Instance IDs of virtual disks for which log files were exported.</span></span>

</dd> <dt>

<span data-ttu-id="f14bb-149">**ExportedGuestStateFilePath**</span><span class="sxs-lookup"><span data-stu-id="f14bb-149">**ExportedGuestStateFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f14bb-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f14bb-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f14bb-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f14bb-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f14bb-152">Ruta de acceso del archivo de estado de invitado exportado.</span><span class="sxs-lookup"><span data-stu-id="f14bb-152">Path of the exported guest state file.</span></span>

> [!Note]  
> <span data-ttu-id="f14bb-153">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="f14bb-153">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="f14bb-154">**ExportedLogFilePaths**</span><span class="sxs-lookup"><span data-stu-id="f14bb-154">**ExportedLogFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f14bb-155">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="f14bb-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f14bb-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f14bb-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f14bb-157">Rutas de acceso de los archivos de registro que se exportaron.</span><span class="sxs-lookup"><span data-stu-id="f14bb-157">Paths of the log files which were exported.</span></span>

</dd> <dt>

<span data-ttu-id="f14bb-158">**ExportedRuntimeFilePath**</span><span class="sxs-lookup"><span data-stu-id="f14bb-158">**ExportedRuntimeFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f14bb-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f14bb-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f14bb-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f14bb-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f14bb-161">Ruta de acceso del archivo de estado en tiempo de ejecución exportado.</span><span class="sxs-lookup"><span data-stu-id="f14bb-161">Path of the exported runtime state file.</span></span>

</dd> <dt>

<span data-ttu-id="f14bb-162">**ReferencePointId**</span><span class="sxs-lookup"><span data-stu-id="f14bb-162">**ReferencePointId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f14bb-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f14bb-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f14bb-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f14bb-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f14bb-165">GUID del punto de referencia que se exporta.</span><span class="sxs-lookup"><span data-stu-id="f14bb-165">GUID of the reference point which is exported.</span></span>

</dd> <dt>

<span data-ttu-id="f14bb-166">**VirtualMachineId**</span><span class="sxs-lookup"><span data-stu-id="f14bb-166">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f14bb-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f14bb-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f14bb-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f14bb-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f14bb-169">GUID de la máquina virtual para la que se exportaron los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="f14bb-169">GUID of the virtual machine for which log files were exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f14bb-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f14bb-170">Requirements</span></span>



| <span data-ttu-id="f14bb-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="f14bb-171">Requirement</span></span> | <span data-ttu-id="f14bb-172">Value</span><span class="sxs-lookup"><span data-stu-id="f14bb-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f14bb-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f14bb-173">Minimum supported client</span></span><br/> | <span data-ttu-id="f14bb-174">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="f14bb-174">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f14bb-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f14bb-175">Minimum supported server</span></span><br/> | <span data-ttu-id="f14bb-176">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f14bb-176">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f14bb-177">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f14bb-177">Namespace</span></span><br/>                | <span data-ttu-id="f14bb-178">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f14bb-178">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f14bb-179">MOF</span><span class="sxs-lookup"><span data-stu-id="f14bb-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f14bb-180"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f14bb-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f14bb-181">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f14bb-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f14bb-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f14bb-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f14bb-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="f14bb-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f14bb-184">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="f14bb-184">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

