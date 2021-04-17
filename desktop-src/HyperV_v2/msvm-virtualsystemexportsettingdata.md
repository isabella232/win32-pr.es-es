---
description: Proporciona información adicional que se va a usar con el método ExportSystemDefinition de la \_ clase VirtualSystemManagementService de MSVM.
ms.assetid: 86396A76-83EC-476E-86A9-83861A002152
title: Msvm_VirtualSystemExportSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemExportSettingData
- Msvm_VirtualSystemExportSettingData.CaptureLiveState
- Msvm_VirtualSystemExportSettingData.InstanceID
- Msvm_VirtualSystemExportSettingData.Caption
- Msvm_VirtualSystemExportSettingData.Description
- Msvm_VirtualSystemExportSettingData.ElementName
- Msvm_VirtualSystemExportSettingData.CopySnapshotConfiguration
- Msvm_VirtualSystemExportSettingData.CopyVmRuntimeInformation
- Msvm_VirtualSystemExportSettingData.CopyVmStorage
- Msvm_VirtualSystemExportSettingData.CreateVmExportSubdirectory
- Msvm_VirtualSystemExportSettingData.SnapshotVirtualSystem
- Msvm_VirtualSystemExportSettingData.BackupIntent
- Msvm_VirtualSystemExportSettingData.ExportForLiveMigration
- Msvm_VirtualSystemExportSettingData.DisableDifferentialOfIgnoredStorage
- Msvm_VirtualSystemExportSettingData.ExcludedVirtualHardDisks
- Msvm_VirtualSystemExportSettingData.DifferentialBackupBase
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77bd451912063ec1164abf14247d81e1d258f56f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686598"
---
# <a name="msvm_virtualsystemexportsettingdata-class"></a><span data-ttu-id="a1996-103">MSVM \_ VirtualSystemExportSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="a1996-103">Msvm\_VirtualSystemExportSettingData class</span></span>

<span data-ttu-id="a1996-104">Proporciona información adicional que se va a usar con el método [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) de la clase [**\_ VirtualSystemManagementService de MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="a1996-104">Provides additional information to be used with the [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="a1996-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a1996-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1996-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1996-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemExportSettingData : CIM_SettingData
{
  uint8   CaptureLiveState;
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint8   CopySnapshotConfiguration;
  boolean CopyVmRuntimeInformation;
  boolean CopyVmStorage;
  boolean CreateVmExportSubdirectory;
  string  SnapshotVirtualSystem;
  uint8   BackupIntent;
  boolean ExportForLiveMigration;
  boolean DisableDifferentialOfIgnoredStorage;
  string  ExcludedVirtualHardDisks[];
  string  DifferentialBackupBase;
};
```

## <a name="members"></a><span data-ttu-id="a1996-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1996-107">Members</span></span>

<span data-ttu-id="a1996-108">La clase **MSVM \_ VirtualSystemExportSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a1996-108">The **Msvm\_VirtualSystemExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a1996-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1996-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1996-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1996-110">Properties</span></span>

<span data-ttu-id="a1996-111">La clase **MSVM \_ VirtualSystemExportSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a1996-111">The **Msvm\_VirtualSystemExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1996-112">**BackupIntent**</span><span class="sxs-lookup"><span data-stu-id="a1996-112">**BackupIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1996-113">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a1996-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a1996-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1996-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a1996-115">Indica el intento de uso de los conjuntos de copia de seguridad exportados.</span><span class="sxs-lookup"><span data-stu-id="a1996-115">Indicates the intent on how the exported backup sets would be used.</span></span>

> [!Note]  
> <span data-ttu-id="a1996-116">Esta propiedad se agregó en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a1996-116">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span data-ttu-id="a1996-117"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)</span><span class="sxs-lookup"><span data-stu-id="a1996-117"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a1996-118">Todos los conjuntos de copia de seguridad completos y diferenciales exportados se conservarán tal como están.</span><span class="sxs-lookup"><span data-stu-id="a1996-118">All exported full and differential backup sets would be preserved as they are.</span></span>

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span data-ttu-id="a1996-119"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)</span><span class="sxs-lookup"><span data-stu-id="a1996-119"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a1996-120">Los conjuntos de copia de seguridad completos y diferenciales exportados se combinarán para sintetizar los conjuntos de copia de seguridad completos.</span><span class="sxs-lookup"><span data-stu-id="a1996-120">The exported full and differential backup sets would be merged to synthesize full backup sets.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a1996-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a1996-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1996-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a1996-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1996-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a1996-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1996-124">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="a1996-124">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="a1996-125">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a1996-125">A short description of the object.</span></span> <span data-ttu-id="a1996-126">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a1996-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1996-127">**CaptureLiveState**</span><span class="sxs-lookup"><span data-stu-id="a1996-127">**CaptureLiveState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1996-128">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a1996-128">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a1996-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1996-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a1996-130">Indica qué estado capturar si el destino de la exportación es una máquina virtual en ejecución.</span><span class="sxs-lookup"><span data-stu-id="a1996-130">Indicates what state to capture if the target of the export is a running VM.</span></span>

<dt>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>

<span data-ttu-id="a1996-131"><span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)</span><span class="sxs-lookup"><span data-stu-id="a1996-131"><span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a1996-132">No se exportarán archivos de estado guardados para la máquina virtual en ejecución y se colocarán en un estado coherente con el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a1996-132">No saved state files will be exported for the running VM, placing it in a crash consistent state.</span></span>

</dd> <dt>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>

<span data-ttu-id="a1996-133"><span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)</span><span class="sxs-lookup"><span data-stu-id="a1996-133"><span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a1996-134">Los archivos de estado guardados de la máquina virtual en ejecución se exportarán junto con la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1996-134">Saved state files for the running VM will be exported along with the VM configuration.</span></span>

</dd> <dt>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>

<span data-ttu-id="a1996-135"><span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)</span><span class="sxs-lookup"><span data-stu-id="a1996-135"><span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a1996-136">Se exportará el estado coherente con la aplicación de la máquina virtual en ejecución.</span><span class="sxs-lookup"><span data-stu-id="a1996-136">Application-consistent state of the running VM will be exported.</span></span>

> [!Note]  
> <span data-ttu-id="a1996-137">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a1996-137">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a1996-138">**CopySnapshotConfiguration**</span><span class="sxs-lookup"><span data-stu-id="a1996-138">**CopySnapshotConfiguration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1996-139">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a1996-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a1996-140">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1996-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a1996-141">Indica qué instantáneas se van a exportar con la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1996-141">Indicates what snapshots are to be exported with the virtual machine.</span></span>

<dt>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>

<span data-ttu-id="a1996-142"><span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0)</span><span class="sxs-lookup"><span data-stu-id="a1996-142"><span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a1996-143">Todas las instantáneas se exportarán con la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1996-143">All snapshots will be exported with the virtual machine.</span></span>

</dd> <dt>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>

<span data-ttu-id="a1996-144"><span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1)</span><span class="sxs-lookup"><span data-stu-id="a1996-144"><span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a1996-145">No se exportará ninguna instantánea con la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1996-145">No snapshots will be exported with the virtual machine.</span></span>

</dd> <dt>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>

<span data-ttu-id="a1996-146"><span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2)</span><span class="sxs-lookup"><span data-stu-id="a1996-146"><span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a1996-147">Las instantáneas identificadas por la propiedad **SnapshotVirtualSystem** se exportarán con la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1996-147">The snapshots identified by the **SnapshotVirtualSystem** property will be exported with the virtual machine.</span></span> <span data-ttu-id="a1996-148">Se omiten las propiedades **CopyVmStorage** y **CopyVmRuntimeInformation** , el almacenamiento y la información en tiempo de ejecución se exportan con la máquina virtual y los discos de diferenciación de VHD se combinarán en un nuevo VHD.</span><span class="sxs-lookup"><span data-stu-id="a1996-148">The **CopyVmStorage** and **CopyVmRuntimeInformation** properties are ignored, storage and run-time information is exported with the virtual machine, and any VHD differencing disks will be merged into a new VHD.</span></span>

</dd> <dt>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>

<span data-ttu-id="a1996-149"><span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)</span><span class="sxs-lookup"><span data-stu-id="a1996-149"><span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a1996-150">La instantánea identificada por la propiedad **SnapshotVirtualSystem** se exportará con el fin de realizar una copia de seguridad de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1996-150">The snapshot identified by the **SnapshotVirtualSystem** property will be exported for the purpose of backing up the VM.</span></span> <span data-ttu-id="a1996-151">La configuración exportada usará el identificador de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1996-151">The exported configuration will use ID of the VM.</span></span>

> [!Note]  
> <span data-ttu-id="a1996-152">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a1996-152">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a1996-153">**CopyVmRuntimeInformation**</span><span class="sxs-lookup"><span data-stu-id="a1996-153">**CopyVmRuntimeInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1996-154">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a1996-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1996-155">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1996-155">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a1996-156">Indica si la información de tiempo de ejecución de la máquina virtual se copiará cuando se exporte la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1996-156">Indicates whether the virtual machine run-time information will be copied when the virtual machine is exported.</span></span>



| <span data-ttu-id="a1996-157">Value</span><span class="sxs-lookup"><span data-stu-id="a1996-157">Value</span></span>                                                                                | <span data-ttu-id="a1996-158">Significado</span><span class="sxs-lookup"><span data-stu-id="a1996-158">Meaning</span></span>                                                                 |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a1996-159"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="a1996-159"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="a1996-160">Se copiará la información en tiempo de ejecución de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1996-160">The virtual machine run-time information will be copied.</span></span><br/>     |
| <dl> <span data-ttu-id="a1996-161"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="a1996-161"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="a1996-162">No se copiará la información en tiempo de ejecución de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1996-162">The virtual machine run-time information will not be copied.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a1996-163">**CopyVmStorage**</span><span class="sxs-lookup"><span data-stu-id="a1996-163">**CopyVmStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1996-164">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a1996-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1996-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1996-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a1996-166">Indica si el almacenamiento de la máquina virtual se copiará cuando se exporte la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1996-166">Indicates whether the virtual machine storage will be copied when the virtual machine is exported.</span></span>



| <span data-ttu-id="a1996-167">Value</span><span class="sxs-lookup"><span data-stu-id="a1996-167">Value</span></span>                                                                                | <span data-ttu-id="a1996-168">Significado</span><span class="sxs-lookup"><span data-stu-id="a1996-168">Meaning</span></span>                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="a1996-169"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="a1996-169"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="a1996-170">Se copiará el almacenamiento de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1996-170">The virtual machine storage will be copied.</span></span><br/>     |
| <dl> <span data-ttu-id="a1996-171"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="a1996-171"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="a1996-172">No se copiará el almacenamiento de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1996-172">The virtual machine storage will not be copied.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a1996-173">**CreateVmExportSubdirectory**</span><span class="sxs-lookup"><span data-stu-id="a1996-173">**CreateVmExportSubdirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1996-174">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a1996-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1996-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1996-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a1996-176">Indica si se creará un subdirectorio con el nombre de la máquina virtual cuando se exporte la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1996-176">Indicates whether a subdirectory with the name of the virtual machine will be created when the virtual machine is exported.</span></span>



| <span data-ttu-id="a1996-177">Value</span><span class="sxs-lookup"><span data-stu-id="a1996-177">Value</span></span>                                                                                | <span data-ttu-id="a1996-178">Significado</span><span class="sxs-lookup"><span data-stu-id="a1996-178">Meaning</span></span>                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="a1996-179"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="a1996-179"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="a1996-180">Se creará un subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="a1996-180">A subdirectory will be created.</span></span><br/>     |
| <dl> <span data-ttu-id="a1996-181"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="a1996-181"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="a1996-182">No se creará un subdirectorio.</span><span class="sxs-lookup"><span data-stu-id="a1996-182">A subdirectory will not be created.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a1996-183">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a1996-183">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1996-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a1996-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1996-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a1996-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1996-186">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a1996-186">A description of the object.</span></span> <span data-ttu-id="a1996-187">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a1996-187">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a1996-188">**DifferentialBackupBase**</span><span class="sxs-lookup"><span data-stu-id="a1996-188">**DifferentialBackupBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1996-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a1996-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1996-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1996-190">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a1996-191">Base para la exportación diferencial.</span><span class="sxs-lookup"><span data-stu-id="a1996-191">Base for differential export.</span></span> <span data-ttu-id="a1996-192">Se trata de una ruta de acceso a una instancia de [**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que representa el punto de referencia o la ruta de acceso a una instancia de [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa la instantánea que se va a usar como base para la exportación diferencial.</span><span class="sxs-lookup"><span data-stu-id="a1996-192">This is either path to a [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance that represents the reference point or path to a [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instance that represents the snapshot to be used as a base for differential export.</span></span> <span data-ttu-id="a1996-193">Si la propiedad **CopySnapshotConfiguration** no está establecida en 3 (**ExportOneSnapshotForBackup**), se omite esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="a1996-193">If the **CopySnapshotConfiguration** property is not set to 3(**ExportOneSnapshotForBackup**), this property is ignored.</span></span>

> [!Note]  
> <span data-ttu-id="a1996-194">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a1996-194">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="a1996-195">**DisableDifferentialOfIgnoredStorage**</span><span class="sxs-lookup"><span data-stu-id="a1996-195">**DisableDifferentialOfIgnoredStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1996-196">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a1996-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1996-197">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1996-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a1996-198">Indica si se crearán discos de diferenciación o no para el almacenamiento omitido durante la exportación.</span><span class="sxs-lookup"><span data-stu-id="a1996-198">Indicates whether differencing disks will be created or not for storage ignored during export.</span></span> <span data-ttu-id="a1996-199">De forma predeterminada, se establece en false, lo que significa que se crean discos de diferenciación para el almacenamiento que no se va a copiar en el destino de exportación.</span><span class="sxs-lookup"><span data-stu-id="a1996-199">By default this is set to false, which means that differencing disks are created for the storage that is not going to be copied over to the export destination.</span></span>

> [!Note]  
> <span data-ttu-id="a1996-200">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="a1996-200">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="a1996-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a1996-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1996-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a1996-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1996-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a1996-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a1996-204">Nombre para mostrar de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="a1996-204">The display name for this instance.</span></span> <span data-ttu-id="a1996-205">Además, el nombre para mostrar se puede usar como una propiedad de índice para una búsqueda o una consulta.</span><span class="sxs-lookup"><span data-stu-id="a1996-205">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="a1996-206">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a1996-206">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a1996-207">**ExcludedVirtualHardDisks**</span><span class="sxs-lookup"><span data-stu-id="a1996-207">**ExcludedVirtualHardDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1996-208">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="a1996-208">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a1996-209">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1996-209">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a1996-210">Matriz de identificadores de instancia de [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) (RASD) que representan los discos duros virtuales que se solicitan que se excluyan de la operación de exportación.</span><span class="sxs-lookup"><span data-stu-id="a1996-210">Array of [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) (RASD) instance IDs that represent the virtual hard disks that are requested to be excluded from the export operation.</span></span> <span data-ttu-id="a1996-211">Si al menos uno de los identificadores proporcionados no es un disco duro virtual conectado válido, se producirá un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="a1996-211">If at least one of the supplied IDs is not a valid attached virtual hard disk, the operation will fail.</span></span>

<span data-ttu-id="a1996-212">Los discos duros virtuales a los que hace referencia esta propiedad pueden ser de la máquina virtual o de cualquiera de sus instantáneas.</span><span class="sxs-lookup"><span data-stu-id="a1996-212">The virtual hard disks referenced by this property may be from the VM and/or from any of its snapshots.</span></span> <span data-ttu-id="a1996-213">No se admite la exclusión de discos duros virtuales cuando la propiedad **CopySnapshotConfiguration** está establecida en 0 (ExportAllSnapshots).</span><span class="sxs-lookup"><span data-stu-id="a1996-213">Exclusion of virtual hard disks is not supported when property **CopySnapshotConfiguration** is set to 0(ExportAllSnapshots).</span></span>

<span data-ttu-id="a1996-214">Tenga en cuenta que el identificador de instancia de RASD para los discos duros virtuales representa la ubicación a la que están conectados y, al excluir este identificador, se excluyen todos los discos duros virtuales conectados en esa ubicación a lo largo del árbol de instantáneas de la máquina virtual, independientemente de que sean realmente una cadena de disco duro virtual válida.</span><span class="sxs-lookup"><span data-stu-id="a1996-214">Note that the RASD instance ID for virtual hard disks represents the location they are attached to, and excluding through this ID excludes all virtual hard disks attached in that location throughout the virtual machine's snapshot tree, regardless of them really being a valid virtual hard disk chain.</span></span>

> [!Note]  
> <span data-ttu-id="a1996-215">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="a1996-215">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="a1996-216">**ExportForLiveMigration**</span><span class="sxs-lookup"><span data-stu-id="a1996-216">**ExportForLiveMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1996-217">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a1996-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a1996-218">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1996-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a1996-219">Indica si la máquina virtual exportada está pensada para usarse en la migración en vivo.</span><span class="sxs-lookup"><span data-stu-id="a1996-219">Indicates whether the exported VM is intended to be used in live migration.</span></span>

> [!Note]  
> <span data-ttu-id="a1996-220">Agregado en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a1996-220">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="a1996-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a1996-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1996-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a1996-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1996-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a1996-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1996-224">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="a1996-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a1996-225">Dentro del ámbito del espacio de nombres de la creación de instancias, identifica de forma opaca y única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="a1996-225">Within the scope of the instantiating Namespace, opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a1996-226">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a1996-226">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a1996-227">**SnapshotVirtualSystem**</span><span class="sxs-lookup"><span data-stu-id="a1996-227">**SnapshotVirtualSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1996-228">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a1996-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a1996-229">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a1996-229">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a1996-230">Ruta de acceso a una instancia de [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa la instantánea que se va a exportar con la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a1996-230">Path to a [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instance that represents the snapshot to be exported with the virtual machine.</span></span> <span data-ttu-id="a1996-231">Si la propiedad **CopySnapshotConfiguration** no está establecida en 2 (ExportOneSnapshot), se omite esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="a1996-231">If the **CopySnapshotConfiguration** property is not set to 2 (ExportOneSnapshot), this property is ignored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1996-232">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1996-232">Remarks</span></span>

<span data-ttu-id="a1996-233">El acceso a la clase **MSVM \_ VirtualSystemExportSettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="a1996-233">Access to the **Msvm\_VirtualSystemExportSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a1996-234">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a1996-234">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1996-235">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1996-235">Requirements</span></span>



| <span data-ttu-id="a1996-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1996-236">Requirement</span></span> | <span data-ttu-id="a1996-237">Value</span><span class="sxs-lookup"><span data-stu-id="a1996-237">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1996-238">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1996-238">Minimum supported client</span></span><br/> | <span data-ttu-id="a1996-239">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1996-239">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a1996-240">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1996-240">Minimum supported server</span></span><br/> | <span data-ttu-id="a1996-241">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1996-241">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a1996-242">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a1996-242">Namespace</span></span><br/>                | <span data-ttu-id="a1996-243">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a1996-243">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a1996-244">MOF</span><span class="sxs-lookup"><span data-stu-id="a1996-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1996-245"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1996-245"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1996-246">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a1996-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1996-247"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a1996-247"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a1996-248">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1996-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1996-249">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a1996-249">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="a1996-250">Clases de administración de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="a1996-250">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> <dt>

[<span data-ttu-id="a1996-251">**ExportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="a1996-251">**ExportSystemDefinition**</span></span>](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

