---
description: Representa la configuración específica de virtualización de una máquina virtual.
ms.assetid: BE81405E-E773-41CE-9441-33D60B63550E
title: Msvm_VirtualSystemSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingData
- Msvm_VirtualSystemSettingData.InstanceID
- Msvm_VirtualSystemSettingData.Caption
- Msvm_VirtualSystemSettingData.Description
- Msvm_VirtualSystemSettingData.ElementName
- Msvm_VirtualSystemSettingData.VirtualSystemIdentifier
- Msvm_VirtualSystemSettingData.VirtualSystemType
- Msvm_VirtualSystemSettingData.Notes
- Msvm_VirtualSystemSettingData.CreationTime
- Msvm_VirtualSystemSettingData.ConfigurationID
- Msvm_VirtualSystemSettingData.ConfigurationDataRoot
- Msvm_VirtualSystemSettingData.ConfigurationFile
- Msvm_VirtualSystemSettingData.SnapshotDataRoot
- Msvm_VirtualSystemSettingData.SuspendDataRoot
- Msvm_VirtualSystemSettingData.SwapFileDataRoot
- Msvm_VirtualSystemSettingData.LogDataRoot
- Msvm_VirtualSystemSettingData.AutomaticStartupAction
- Msvm_VirtualSystemSettingData.AutomaticStartupActionDelay
- Msvm_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualSystemSettingData.AutomaticShutdownAction
- Msvm_VirtualSystemSettingData.AutomaticRecoveryAction
- Msvm_VirtualSystemSettingData.RecoveryFile
- Msvm_VirtualSystemSettingData.BIOSGUID
- Msvm_VirtualSystemSettingData.BIOSSerialNumber
- Msvm_VirtualSystemSettingData.BaseBoardSerialNumber
- Msvm_VirtualSystemSettingData.ChassisSerialNumber
- Msvm_VirtualSystemSettingData.Architecture
- Msvm_VirtualSystemSettingData.ChassisAssetTag
- Msvm_VirtualSystemSettingData.BIOSNumLock
- Msvm_VirtualSystemSettingData.BootOrder
- Msvm_VirtualSystemSettingData.Parent
- Msvm_VirtualSystemSettingData.UserSnapshotType
- Msvm_VirtualSystemSettingData.IsSaved
- Msvm_VirtualSystemSettingData.AdditionalRecoveryInformation
- Msvm_VirtualSystemSettingData.AllowFullSCSICommandSet
- Msvm_VirtualSystemSettingData.DebugChannelId
- Msvm_VirtualSystemSettingData.DebugPortEnabled
- Msvm_VirtualSystemSettingData.DebugPort
- Msvm_VirtualSystemSettingData.Version
- Msvm_VirtualSystemSettingData.IncrementalBackupEnabled
- Msvm_VirtualSystemSettingData.VirtualNumaEnabled
- Msvm_VirtualSystemSettingData.AllowReducedFcRedundancy
- Msvm_VirtualSystemSettingData.VirtualSystemSubType
- Msvm_VirtualSystemSettingData.BootSourceOrder
- Msvm_VirtualSystemSettingData.PauseAfterBootFailure
- Msvm_VirtualSystemSettingData.NetworkBootPreferredProtocol
- Msvm_VirtualSystemSettingData.GuestControlledCacheTypes
- Msvm_VirtualSystemSettingData.AutomaticSnapshotsEnabled
- Msvm_VirtualSystemSettingData.IsAutomaticSnapshot
- Msvm_VirtualSystemSettingData.GuestStateFile
- Msvm_VirtualSystemSettingData.GuestStateDataRoot
- Msvm_VirtualSystemSettingData.LockOnDisconnect
- Msvm_VirtualSystemSettingData.ParentPackage
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorActionTimeout
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorAction
- Msvm_VirtualSystemSettingData.ConsoleMode
- Msvm_VirtualSystemSettingData.SecureBootEnabled
- Msvm_VirtualSystemSettingData.SecureBootTemplateId
- Msvm_VirtualSystemSettingData.LowMmioGapSize
- Msvm_VirtualSystemSettingData.HighMmioGapSize
- Msvm_VirtualSystemSettingData.EnhancedSessionTransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2787abbacfe4220b135544eecd3aeb7e86596c81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000955"
---
# <a name="msvm_virtualsystemsettingdata-class"></a><span data-ttu-id="e70e4-103">MSVM \_ VirtualSystemSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="e70e4-103">Msvm\_VirtualSystemSettingData class</span></span>

<span data-ttu-id="e70e4-104">Representa la configuración específica de virtualización de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-104">Represents the virtualization-specific settings for a virtual machine.</span></span>

<span data-ttu-id="e70e4-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e70e4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70e4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e70e4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption = "Virtual Machine Settings";
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   Architecture;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
  string   Parent;
  uint16   UserSnapshotType;
  boolean  IsSaved;
  string   AdditionalRecoveryInformation;
  boolean  AllowFullSCSICommandSet;
  uint32   DebugChannelId;
  uint16   DebugPortEnabled;
  uint32   DebugPort;
  string   Version;
  boolean  IncrementalBackupEnabled;
  boolean  VirtualNumaEnabled;
  boolean  AllowReducedFcRedundancy = False;
  string   VirtualSystemSubType;
  string   BootSourceOrder[];
  boolean  PauseAfterBootFailure;
  uint16   NetworkBootPreferredProtocol;
  boolean  GuestControlledCacheTypes;
  boolean  AutomaticSnapshotsEnabled;
  boolean  IsAutomaticSnapshot;
  string   GuestStateFile;
  string   GuestStateDataRoot;
  boolean  LockOnDisconnect;
  string   ParentPackage;
  datetime AutomaticCriticalErrorActionTimeout;
  uint16   AutomaticCriticalErrorAction;
  uint16   ConsoleMode;
  boolean  SecureBootEnabled;
  string   SecureBootTemplateId;
  uint64   LowMmioGapSize;
  uint64   HighMmioGapSize;
  uint16   EnhancedSessionTransportType;
};
```

## <a name="members"></a><span data-ttu-id="e70e4-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e70e4-107">Members</span></span>

<span data-ttu-id="e70e4-108">La clase **MSVM \_ VirtualSystemSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e70e4-108">The **Msvm\_VirtualSystemSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e70e4-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e70e4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e70e4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e70e4-110">Properties</span></span>

<span data-ttu-id="e70e4-111">La clase **MSVM \_ VirtualSystemSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e70e4-111">The **Msvm\_VirtualSystemSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e70e4-112">**AdditionalRecoveryInformation**</span><span class="sxs-lookup"><span data-stu-id="e70e4-112">**AdditionalRecoveryInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-115">Cualquier información adicional proporcionada a la acción de recuperación.</span><span class="sxs-lookup"><span data-stu-id="e70e4-115">Any additional information provided to the recovery action.</span></span> <span data-ttu-id="e70e4-116">El significado de esta propiedad se define mediante la acción de **AutomaticRecoveryAction**.</span><span class="sxs-lookup"><span data-stu-id="e70e4-116">The meaning of this property is defined by the action in **AutomaticRecoveryAction**.</span></span> <span data-ttu-id="e70e4-117">Si **AutomaticRecoveryAction** es 0 ("none") o 1 ("restart"), este valor es **null**.</span><span class="sxs-lookup"><span data-stu-id="e70e4-117">If **AutomaticRecoveryAction** is 0 ("None") or 1 ("Restart"), this value is **Null**.</span></span> <span data-ttu-id="e70e4-118">Si **AutomaticRecoveryAction** es 2 ("revertir a instantánea"), se trata de la ruta de acceso al objeto de una instantánea que se debe aplicar en caso de error del proceso de trabajo de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-118">If **AutomaticRecoveryAction** is 2 ("Revert to Snapshot"), this is the object path to a snapshot that should be applied on failure of the virtual machine worker process.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-119">**AllowFullSCSICommandSet**</span><span class="sxs-lookup"><span data-stu-id="e70e4-119">**AllowFullSCSICommandSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-120">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e70e4-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-122">**True** si los comandos SCSI del sistema operativo invitado se pasan a discos de acceso directo; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e70e4-122">**True** if SCSI commands from the guest operating system are passed to pass-through disks; otherwise, **False**.</span></span> <span data-ttu-id="e70e4-123">Si **es true**, los comandos SCSI emitidos por el sistema operativo invitado a discos de acceso directo no se filtran.</span><span class="sxs-lookup"><span data-stu-id="e70e4-123">If **True**, SCSI commands emitted by the guest operating system to pass-through disks are not filtered.</span></span> <span data-ttu-id="e70e4-124">Se recomienda que el filtrado de SCSI permanezca habilitado para las implementaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e70e4-124">We recommend that SCSI filtering remain enabled for production deployments.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-125">**AllowReducedFcRedundancy**</span><span class="sxs-lookup"><span data-stu-id="e70e4-125">**AllowReducedFcRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-126">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e70e4-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-128">Especifica si se permite la migración en vivo de una máquina virtual configurada con un adaptador de Canal de fibra virtual a un equipo de destino que puede tener o no rutas de acceso reducidas a los dispositivos Canal de fibra de destino.</span><span class="sxs-lookup"><span data-stu-id="e70e4-128">Specifies whether live migration of a virtual machine that is configured with a virtual Fibre Channel adapter is allowed to a destination computer that may have no or reduced paths to the target Fibre Channel devices.</span></span> <span data-ttu-id="e70e4-129">Esta propiedad debe borrarse después de una migración en vivo.</span><span class="sxs-lookup"><span data-stu-id="e70e4-129">This property should be cleared after a live migration.</span></span>



| <span data-ttu-id="e70e4-130">Value</span><span class="sxs-lookup"><span data-stu-id="e70e4-130">Value</span></span>                                                                            | <span data-ttu-id="e70e4-131">Significado</span><span class="sxs-lookup"><span data-stu-id="e70e4-131">Meaning</span></span>                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e70e4-132"><dt>False</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-132"><dt>False</dt></span></span> </dl> | <span data-ttu-id="e70e4-133">No se puede migrar en vivo la máquina virtual a un equipo de destino que pueda no tener rutas de acceso reducidas al Canal de fibra dispositivos de destino.</span><span class="sxs-lookup"><span data-stu-id="e70e4-133">The virtual machine cannot be live migrated to a target computer that may have no or reduced paths to the target Fibre Channel devices.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="e70e4-134"><dt>True</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-134"><dt>True</dt></span></span> </dl>  | <span data-ttu-id="e70e4-135">La máquina virtual se puede migrar en vivo a un equipo de destino que puede tener rutas de acceso no reducidas al Canal de fibra dispositivos de destino.</span><span class="sxs-lookup"><span data-stu-id="e70e4-135">The virtual machine can be live migrated to a target computer that may have no or reduced paths to the target Fibre Channel devices.</span></span> <span data-ttu-id="e70e4-136">Es posible que el sistema operativo invitado pierda la conectividad con el almacenamiento y se comporte de forma impredecible.</span><span class="sxs-lookup"><span data-stu-id="e70e4-136">The guest operating system may lose connectivity to storage and may behave in an unpredictable manner.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e70e4-137">**Arquitectura**</span><span class="sxs-lookup"><span data-stu-id="e70e4-137">**Architecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-140">La arquitectura de este sistema.</span><span class="sxs-lookup"><span data-stu-id="e70e4-140">The architecture of this system.</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-141">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="e70e4-141">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="x64"></span><span id="X64"></span>

<span data-ttu-id="e70e4-142">**x64** ()</span><span class="sxs-lookup"><span data-stu-id="e70e4-142">**x64** ()</span></span>


</dt> <dd></dd> <dt>

<span id="arm64"></span><span id="ARM64"></span>

<span data-ttu-id="e70e4-143">**arm64** ()</span><span class="sxs-lookup"><span data-stu-id="e70e4-143">**arm64** ()</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e70e4-144">**AutomaticCriticalErrorAction**</span><span class="sxs-lookup"><span data-stu-id="e70e4-144">**AutomaticCriticalErrorAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-145">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e70e4-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-146">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-147">Identifica la acción que se realizará en la máquina virtual cuando se produce un error crítico, como el almacenamiento desconectado.</span><span class="sxs-lookup"><span data-stu-id="e70e4-147">Identifies the action to be taken on VM, when a critical error happens, like storage disconnect.</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-148">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e70e4-148">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="e70e4-149"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno** (0)</span><span class="sxs-lookup"><span data-stu-id="e70e4-149"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e70e4-150">No se realizará ninguna acción específica para las condiciones de error críticas.</span><span class="sxs-lookup"><span data-stu-id="e70e4-150">No specific action will be taken for critical error conditions.</span></span>

</dd> <dt>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>

<span data-ttu-id="e70e4-151"><span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Pausar reanudación** (1)</span><span class="sxs-lookup"><span data-stu-id="e70e4-151"><span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Pause Resume** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e70e4-152">Hace que la máquina virtual esté en pausa y se reanude automáticamente cuando se resuelva la condición de error crítico.</span><span class="sxs-lookup"><span data-stu-id="e70e4-152">Causes the VM to be paused and automatically resumed when the critical error condition is resolved.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e70e4-153">**AutomaticCriticalErrorActionTimeout**</span><span class="sxs-lookup"><span data-stu-id="e70e4-153">**AutomaticCriticalErrorActionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-154">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e70e4-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-155">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-156">Calificadores: [**subtipo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Interval")</span><span class="sxs-lookup"><span data-stu-id="e70e4-156">Qualifiers: [**SubType**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("interval")</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-157">Identifica la duración máxima para la que se realizará el **AutomaticCriticalErrorAction** para resolver el error crítico.</span><span class="sxs-lookup"><span data-stu-id="e70e4-157">Identifies the maximum duration for which the **AutomaticCriticalErrorAction** will be performed to resolve the critical error.</span></span> <span data-ttu-id="e70e4-158">Esto solo es aplicable cuando el valor de la propiedad **AutomaticCriticalErrorAction** no es 0 (ninguno).</span><span class="sxs-lookup"><span data-stu-id="e70e4-158">This is applicable only when the value of the **AutomaticCriticalErrorAction** property is not 0 (None).</span></span> <span data-ttu-id="e70e4-159">Una vez que expire el tiempo de espera, se apagará la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-159">Once the timeout expires, the VM will be powered off.</span></span> <span data-ttu-id="e70e4-160">El valor se redondeará al minuto más cercano.</span><span class="sxs-lookup"><span data-stu-id="e70e4-160">The value will be rounded up to the nearest minute.</span></span> <span data-ttu-id="e70e4-161">Un valor de 0 implica que la máquina virtual debe apagarse inmediatamente cuando encuentra una condición de error crítico.</span><span class="sxs-lookup"><span data-stu-id="e70e4-161">A value of 0 implies that the VM should be powered off immediately when it encounters a critical error condition.</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-162">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e70e4-162">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="e70e4-163">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="e70e4-163">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-164">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e70e4-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-166">Acción que se debe realizar para la máquina virtual cuando se produce un error en el software ejecutado por la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-166">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="e70e4-167">Los errores en este caso significan un error que es detectado por la plataforma del host, como una condición de estado de espera no interrumpida.</span><span class="sxs-lookup"><span data-stu-id="e70e4-167">Failures in this case means a failure that is detectable by the host platform, such as a noninterruptible wait state condition.</span></span> <span data-ttu-id="e70e4-168">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-168">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="e70e4-169">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e70e4-169">This can be one of the following values.</span></span>



| <span data-ttu-id="e70e4-170">Value</span><span class="sxs-lookup"><span data-stu-id="e70e4-170">Value</span></span>                                                                               | <span data-ttu-id="e70e4-171">Significado</span><span class="sxs-lookup"><span data-stu-id="e70e4-171">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="e70e4-172"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-172"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="e70e4-173">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e70e4-173">None.</span></span><br/>               |
| <dl> <span data-ttu-id="e70e4-174"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-174"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="e70e4-175">Restart. (Reiniciar)</span><span class="sxs-lookup"><span data-stu-id="e70e4-175">Restart.</span></span><br/>            |
| <dl> <span data-ttu-id="e70e4-176"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-176"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="e70e4-177">Revertir a la instantánea.</span><span class="sxs-lookup"><span data-stu-id="e70e4-177">Revert to snapshot.</span></span><br/> |
| <dl> <span data-ttu-id="e70e4-178"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-178"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="e70e4-179">Reservado.</span><span class="sxs-lookup"><span data-stu-id="e70e4-179">Reserved.</span></span><br/>           |



 

</dd> <dt>

<span data-ttu-id="e70e4-180">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="e70e4-180">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-181">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e70e4-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-183">Acción que se realizará para la máquina virtual cuando se apague el host.</span><span class="sxs-lookup"><span data-stu-id="e70e4-183">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="e70e4-184">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-184">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="e70e4-185">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e70e4-185">This can be one of the following values.</span></span>



| <span data-ttu-id="e70e4-186">Value</span><span class="sxs-lookup"><span data-stu-id="e70e4-186">Value</span></span>                                                                               | <span data-ttu-id="e70e4-187">Significado</span><span class="sxs-lookup"><span data-stu-id="e70e4-187">Meaning</span></span>                |
|-------------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="e70e4-188"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-188"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="e70e4-189">Apaga.</span><span class="sxs-lookup"><span data-stu-id="e70e4-189">Turn off.</span></span><br/>   |
| <dl> <span data-ttu-id="e70e4-190"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-190"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="e70e4-191">Guardar estado.</span><span class="sxs-lookup"><span data-stu-id="e70e4-191">Save state.</span></span><br/> |
| <dl> <span data-ttu-id="e70e4-192"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-192"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="e70e4-193">Apagar.</span><span class="sxs-lookup"><span data-stu-id="e70e4-193">Shutdown.</span></span><br/>   |
| <dl> <span data-ttu-id="e70e4-194"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-194"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="e70e4-195">Reservado.</span><span class="sxs-lookup"><span data-stu-id="e70e4-195">Reserved.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="e70e4-196">**AutomaticSnapshotsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e70e4-196">**AutomaticSnapshotsEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-197">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e70e4-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-198">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-198">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-199">Indica si esta máquina virtual debe tener habilitadas las instantáneas automáticas.</span><span class="sxs-lookup"><span data-stu-id="e70e4-199">Indicates whether this virtual machine should have automatic snapshots enabled.</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-200">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="e70e4-200">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="e70e4-201">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="e70e4-201">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-202">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e70e4-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-204">Acción que se realizará para la máquina virtual cuando se inicie el host.</span><span class="sxs-lookup"><span data-stu-id="e70e4-204">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="e70e4-205">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-205">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="e70e4-206">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e70e4-206">This can be one of the following values.</span></span>



| <span data-ttu-id="e70e4-207">Value</span><span class="sxs-lookup"><span data-stu-id="e70e4-207">Value</span></span>                                                                               | <span data-ttu-id="e70e4-208">Significado</span><span class="sxs-lookup"><span data-stu-id="e70e4-208">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="e70e4-209"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-209"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="e70e4-210">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e70e4-210">None.</span></span><br/>                         |
| <dl> <span data-ttu-id="e70e4-211"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-211"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="e70e4-212">Reiniciar si estaba activo previamente.</span><span class="sxs-lookup"><span data-stu-id="e70e4-212">Restart if previously active.</span></span><br/> |
| <dl> <span data-ttu-id="e70e4-213"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-213"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="e70e4-214">Iniciar siempre.</span><span class="sxs-lookup"><span data-stu-id="e70e4-214">Always start.</span></span><br/>                 |
| <dl> <span data-ttu-id="e70e4-215"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-215"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="e70e4-216">Reservado.</span><span class="sxs-lookup"><span data-stu-id="e70e4-216">Reserved.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="e70e4-217">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="e70e4-217">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-218">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e70e4-218">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-220">El tiempo de retardo antes de que la máquina virtual se inicie automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e70e4-220">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="e70e4-221">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-221">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-222">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="e70e4-222">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-223">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e70e4-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-225">Número que indica la secuencia relativa de activación de la máquina virtual cuando se inicia el sistema host.</span><span class="sxs-lookup"><span data-stu-id="e70e4-225">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="e70e4-226">Un número menor indica la activación anterior.</span><span class="sxs-lookup"><span data-stu-id="e70e4-226">A lower number indicates earlier activation.</span></span> <span data-ttu-id="e70e4-227">Si una o más configuraciones muestran el mismo valor, la secuencia depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="e70e4-227">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="e70e4-228">Un valor de 0 indica que la secuencia depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="e70e4-228">A value of 0 indicates that the sequence is implementation dependent.</span></span> <span data-ttu-id="e70e4-229">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-229">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-230">**BaseBoardSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="e70e4-230">**BaseBoardSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-231">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-232">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-233">Número de serie del panel base de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-233">The serial number of the base board for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-234">**BIOSGUID**</span><span class="sxs-lookup"><span data-stu-id="e70e4-234">**BIOSGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-235">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-236">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-237">Identificador único global del BIOS de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-237">The globally unique identifier for the BIOS of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-238">**BIOSNumLock**</span><span class="sxs-lookup"><span data-stu-id="e70e4-238">**BIOSNumLock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-239">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e70e4-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-240">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-240">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-241">**True** si la tecla Bloq Num está establecida en on por el BIOS; **False** si la tecla Bloq Num está establecida en OFF por el BIOS.</span><span class="sxs-lookup"><span data-stu-id="e70e4-241">**True** if the num lock key is set to on by the BIOS; **False** if the num lock key is set to off by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-242">**BIOSSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="e70e4-242">**BIOSSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-244">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-244">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-245">Número de serie del BIOS de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-245">The serial number of the BIOS for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-246">**BootOrder**</span><span class="sxs-lookup"><span data-stu-id="e70e4-246">**BootOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-247">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e70e4-247">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-248">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-248">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-249">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span><span class="sxs-lookup"><span data-stu-id="e70e4-249">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-250">El orden de arranque establecido en el BIOS de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-250">The boot order set within the BIOS of the virtual machine.</span></span> <span data-ttu-id="e70e4-251">Esta propiedad es una matriz de valores, de **BootOrder** \[ 0 \] a **BootOrder** \[ 3 \] , ambos incluidos, donde cada valor indica un dispositivo desde el que arrancar.</span><span class="sxs-lookup"><span data-stu-id="e70e4-251">This property is an array of values, **BootOrder**\[0\] through **BootOrder**\[3\], inclusive, where each value indicates a device to boot from.</span></span> <span data-ttu-id="e70e4-252">Cada uno de los 4 valores de la matriz se debe establecer y no debe ser igual que otro valor de la matriz.</span><span class="sxs-lookup"><span data-stu-id="e70e4-252">Each of the 4 values in the array must be set and must not be the same as another value in the array.</span></span> <span data-ttu-id="e70e4-253">En primer lugar, la máquina virtual intentará arrancar desde el dispositivo indicado por el primer valor de la matriz.</span><span class="sxs-lookup"><span data-stu-id="e70e4-253">The virtual machine will first attempt to boot from the device indicated by the first value within the array.</span></span> <span data-ttu-id="e70e4-254">Si ese dispositivo no contiene un sector de arranque, la máquina virtual intentará arrancar desde el siguiente dispositivo especificado por la propiedad **BootOrder** , etc.</span><span class="sxs-lookup"><span data-stu-id="e70e4-254">If that device does not contain a boot sector, the virtual machine will attempt to boot from the next device specified by the **BootOrder** property and so on.</span></span> <span data-ttu-id="e70e4-255">Si no hay ningún dispositivo especificado en **BootOrder** que contenga un sector de arranque, la máquina virtual no se iniciará.</span><span class="sxs-lookup"><span data-stu-id="e70e4-255">If no device specified within the **BootOrder** contains a boot sector the virtual machine will fail to boot.</span></span> <span data-ttu-id="e70e4-256">El valor predeterminado de una máquina virtual es \[ 0, 1, 2, 3 \] .</span><span class="sxs-lookup"><span data-stu-id="e70e4-256">The default value for a virtual machine is \[0, 1, 2, 3\].</span></span>

<dt>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>

<span data-ttu-id="e70e4-257"><span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Disquete** (0)</span><span class="sxs-lookup"><span data-stu-id="e70e4-257"><span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Floppy** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e70e4-258">La máquina virtual intentará arrancar desde el disquete en la unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="e70e4-258">The virtual machine will attempt to boot from the floppy disk within the floppy drive.</span></span>

</dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="e70e4-259"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)</span><span class="sxs-lookup"><span data-stu-id="e70e4-259"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e70e4-260">La máquina virtual intentará arrancar desde el primer disco de CD o DVD encontrado con un sector de arranque.</span><span class="sxs-lookup"><span data-stu-id="e70e4-260">The virtual machine will attempt to boot from the first CD or DVD disk found with a boot sector.</span></span>

</dd> <dt>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>

<span data-ttu-id="e70e4-261"><span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**Unidad de disco duro IDE** (2)</span><span class="sxs-lookup"><span data-stu-id="e70e4-261"><span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**IDE Hard Drive** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e70e4-262">La máquina virtual intentará arrancar desde la primera unidad de disco duro que se encuentra en un sector de arranque.</span><span class="sxs-lookup"><span data-stu-id="e70e4-262">The virtual machine will attempt to boot from the first hard disk drive found with a boot sector.</span></span>

</dd> <dt>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>

<span data-ttu-id="e70e4-263"><span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**Arranque PXE** (3)</span><span class="sxs-lookup"><span data-stu-id="e70e4-263"><span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**PXE Boot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e70e4-264">La máquina virtual intentará realizar un arranque PXE desde la red.</span><span class="sxs-lookup"><span data-stu-id="e70e4-264">The virtual machine will attempt to PXE boot from the network.</span></span>

</dd> <dt>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>

<span data-ttu-id="e70e4-265"><span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**Unidad de disco duro SCSI** (4)</span><span class="sxs-lookup"><span data-stu-id="e70e4-265"><span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**SCSI Hard Drive** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="e70e4-266"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (5.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e70e4-266"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (5..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e70e4-267">**BootSourceOrder**</span><span class="sxs-lookup"><span data-stu-id="e70e4-267">**BootSourceOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-268">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e70e4-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-269">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-270">El orden de origen de arranque de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-270">The boot source order for the virtual machine.</span></span>

<span data-ttu-id="e70e4-271">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e70e4-271">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-272">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e70e4-272">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-273">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-275">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e70e4-275">A short description of the object.</span></span> <span data-ttu-id="e70e4-276">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e70e4-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-277">**ChassisAssetTag**</span><span class="sxs-lookup"><span data-stu-id="e70e4-277">**ChassisAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-278">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-279">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-279">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-280">Etiqueta de recurso del chasis de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-280">The asset tag of the chassis for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-281">**ChassisSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="e70e4-281">**ChassisSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-282">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-283">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-283">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-284">Número de serie del chasis de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-284">The serial number of the chassis for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-285">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="e70e4-285">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-288">La ruta de acceso de un directorio donde se almacena la información sobre la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-288">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="e70e4-289">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-289">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-290">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="e70e4-290">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-291">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-293">La ruta de acceso relativa y el nombre de un archivo donde se almacena la información sobre la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-293">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="e70e4-294">Esta ruta de acceso es relativa a la propiedad **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="e70e4-294">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="e70e4-295">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-295">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-296">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="e70e4-296">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-297">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-299">Identificador único de la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-299">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="e70e4-300">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-300">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-301">**ConsoleMode**</span><span class="sxs-lookup"><span data-stu-id="e70e4-301">**ConsoleMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-302">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e70e4-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-303">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-303">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-304">Identifica el modo de consola de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-304">Identifies the Console Mode for the VM.</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-305">Esta propiedad se agregó en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e70e4-305">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="e70e4-306">**Valor predeterminado** (0)</span><span class="sxs-lookup"><span data-stu-id="e70e4-306">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="COM1"></span><span id="com1"></span>

<span data-ttu-id="e70e4-307">**COM1** (1)</span><span class="sxs-lookup"><span data-stu-id="e70e4-307">**COM1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="COM2"></span><span id="com2"></span>

<span data-ttu-id="e70e4-308">**COM2** (2)</span><span class="sxs-lookup"><span data-stu-id="e70e4-308">**COM2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="e70e4-309">**Ninguno** (3)</span><span class="sxs-lookup"><span data-stu-id="e70e4-309">**None** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e70e4-310">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="e70e4-310">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-311">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e70e4-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-313">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-313">The date and time at which the settings for the virtual machine were created.</span></span> <span data-ttu-id="e70e4-314">Si este objeto representa la configuración actual de la máquina virtual, este valor sería la hora a la que se creó el sistema.</span><span class="sxs-lookup"><span data-stu-id="e70e4-314">If this object represents the current settings for the virtual machine, this value would be the time at which the system was created.</span></span> <span data-ttu-id="e70e4-315">Si este objeto representa la configuración de instantánea de la máquina virtual, este valor sería la hora a la que se tomó la instantánea.</span><span class="sxs-lookup"><span data-stu-id="e70e4-315">If this object represents the snapshot settings for the virtual machine, this value would be the time at which the snapshot was taken.</span></span> <span data-ttu-id="e70e4-316">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-316">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-317">**DebugChannelId**</span><span class="sxs-lookup"><span data-stu-id="e70e4-317">**DebugChannelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-318">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e70e4-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-319">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-319">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-320">El identificador de canal que se usa para depurar la máquina virtual mediante el depurador unificado.</span><span class="sxs-lookup"><span data-stu-id="e70e4-320">The channel identifier used to debug the virtual machine using the unified debugger.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-321">**Pura**</span><span class="sxs-lookup"><span data-stu-id="e70e4-321">**DebugPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-322">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e70e4-322">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-323">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-323">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-324">Puerto TCP/IP que se usa para depurar la máquina virtual mediante la depuración sintética.</span><span class="sxs-lookup"><span data-stu-id="e70e4-324">The TCP/IP port used to debug the virtual machine using synthetic debugging.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-325">**DebugPortEnabled**</span><span class="sxs-lookup"><span data-stu-id="e70e4-325">**DebugPortEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-326">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e70e4-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-327">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-327">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-328">Especifica si la máquina virtual usa la depuración sintética.</span><span class="sxs-lookup"><span data-stu-id="e70e4-328">Specifies whether the virtual machine is using synthetic debugging.</span></span> <span data-ttu-id="e70e4-329">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e70e4-329">This can be one of the following values.</span></span>

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="e70e4-330"><span id="Off"></span><span id="off"></span><span id="OFF"></span>**Desactivado** (0)</span><span class="sxs-lookup"><span data-stu-id="e70e4-330"><span id="Off"></span><span id="off"></span><span id="OFF"></span>**Off** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="On"></span><span id="on"></span><span id="ON"></span>

<span data-ttu-id="e70e4-331"><span id="On"></span><span id="on"></span><span id="ON"></span>**En** (1)</span><span class="sxs-lookup"><span data-stu-id="e70e4-331"><span id="On"></span><span id="on"></span><span id="ON"></span>**On** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>

<span data-ttu-id="e70e4-332"><span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)</span><span class="sxs-lookup"><span data-stu-id="e70e4-332"><span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e70e4-333">Asignación automática</span><span class="sxs-lookup"><span data-stu-id="e70e4-333">Auto-assigned</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e70e4-334">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e70e4-334">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-335">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-337">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e70e4-337">A description of the object.</span></span> <span data-ttu-id="e70e4-338">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e70e4-338">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to one of the following values.</span></span>



| <span data-ttu-id="e70e4-339">Value</span><span class="sxs-lookup"><span data-stu-id="e70e4-339">Value</span></span>                                                                                                                  | <span data-ttu-id="e70e4-340">Significado</span><span class="sxs-lookup"><span data-stu-id="e70e4-340">Meaning</span></span>                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="e70e4-341"><dt>"Configuración activa de la máquina virtual"</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-341"><dt>"Active settings for the virtual machine"</dt></span></span> </dl>   | <span data-ttu-id="e70e4-342">Esta instancia hace referencia a una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-342">This instance refers to a virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="e70e4-343"><dt>"Configuración de instantáneas de la máquina virtual"</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-343"><dt>"Snapshot settings for the virtual machine"</dt></span></span> </dl> | <span data-ttu-id="e70e4-344">Esta instancia hace referencia a una instantánea.</span><span class="sxs-lookup"><span data-stu-id="e70e4-344">This instance refers to a snapshot.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="e70e4-345">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e70e4-345">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-346">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-348">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="e70e4-348">A display name for the object.</span></span> <span data-ttu-id="e70e4-349">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))y siempre se establece en el nombre para mostrar de la máquina.</span><span class="sxs-lookup"><span data-stu-id="e70e4-349">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is always set to the display name for the machine.</span></span> <span data-ttu-id="e70e4-350">Este nombre no puede superar los 100 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="e70e4-350">This name may not exceed 100 characters in length.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-351">**EnhancedSessionTransportType**</span><span class="sxs-lookup"><span data-stu-id="e70e4-351">**EnhancedSessionTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-352">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e70e4-352">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-353">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-353">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-354">Indica el tipo de transporte que se va a utilizar al conectarse a una sesión mejorada.</span><span class="sxs-lookup"><span data-stu-id="e70e4-354">Indicates the transport type to use when connecting to an enhanced session.</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-355">Esta propiedad se agregó en la versión 1803 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e70e4-355">This property was added in Windows 10, version 1803.</span></span>

 

<dt>

<span id="VMBus_Pipe"></span><span id="vmbus_pipe"></span><span id="VMBUS_PIPE"></span>

<span data-ttu-id="e70e4-356">**Canalización de VMBus** (0)</span><span class="sxs-lookup"><span data-stu-id="e70e4-356">**VMBus Pipe** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Hyper-V_Socket"></span><span id="hyper-v_socket"></span><span id="HYPER-V_SOCKET"></span>

<span data-ttu-id="e70e4-357">**Socket de Hyper-V** (1)</span><span class="sxs-lookup"><span data-stu-id="e70e4-357">**Hyper-V Socket** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e70e4-358">**GuestControlledCacheTypes**</span><span class="sxs-lookup"><span data-stu-id="e70e4-358">**GuestControlledCacheTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-359">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e70e4-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-360">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-360">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-361">Indica si el invitado puede controlar los tipos de caché.</span><span class="sxs-lookup"><span data-stu-id="e70e4-361">Indicates whether the guest can control cache types.</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-362">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e70e4-362">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="e70e4-363">**GuestStateDataRoot**</span><span class="sxs-lookup"><span data-stu-id="e70e4-363">**GuestStateDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-364">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-366">Filepath de un directorio donde se almacena información sobre el estado de tiempo de ejecución de invitado.</span><span class="sxs-lookup"><span data-stu-id="e70e4-366">Filepath of a directory where information about the guest runtime state is stored.</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-367">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="e70e4-367">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="e70e4-368">**GuestStateFile**</span><span class="sxs-lookup"><span data-stu-id="e70e4-368">**GuestStateFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-369">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-371">Ruta de acceso de un archivo donde se almacena información sobre el estado de tiempo de ejecución de invitado.</span><span class="sxs-lookup"><span data-stu-id="e70e4-371">Filepath of a file where information about the guest runtime state is stored.</span></span> <span data-ttu-id="e70e4-372">Una ruta de acceso relativa se anexa al valor de la propiedad **GuestStateDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="e70e4-372">A relative path appends to the value of the **GuestStateDataRoot** property.</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-373">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="e70e4-373">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="e70e4-374">**HighMmioGapSize**</span><span class="sxs-lookup"><span data-stu-id="e70e4-374">**HighMmioGapSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-375">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e70e4-375">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-376">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-376">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-377">El tamaño de alto (más de 4 GB) Memory-Mapped intervalo de e/s en MB</span><span class="sxs-lookup"><span data-stu-id="e70e4-377">The size of the High (above 4GB) Memory-Mapped IO Gap in MB</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-378">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e70e4-378">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="e70e4-379">**IncrementalBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="e70e4-379">**IncrementalBackupEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-380">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e70e4-380">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-381">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-381">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-382">Indica si la VSS Writer de Hyper-V admite la realización de copias de seguridad incrementales de esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-382">Indicates whether the Hyper-V VSS writer supports taking incremental backups of this virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-383">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e70e4-383">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-384">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-385">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-386">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="e70e4-386">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-387">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="e70e4-387">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e70e4-388">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-388">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-389">**IsAutomaticSnapshot**</span><span class="sxs-lookup"><span data-stu-id="e70e4-389">**IsAutomaticSnapshot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-390">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e70e4-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-391">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-392">Indica si se trata de una instantánea que se ha creado automáticamente para el usuario.</span><span class="sxs-lookup"><span data-stu-id="e70e4-392">Indicates whether this is a snapshot created automatically for the user.</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-393">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="e70e4-393">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="e70e4-394">**IsSaved**</span><span class="sxs-lookup"><span data-stu-id="e70e4-394">**IsSaved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-395">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e70e4-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-396">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-397">**True** si la configuración tiene una referencia a un archivo de estado guardado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e70e4-397">**True** if the configuration has a reference to a saved state file; otherwise, **False**.</span></span> <span data-ttu-id="e70e4-398">Esto no indica la presencia de este tipo de archivo, solo que la configuración especifica uno.</span><span class="sxs-lookup"><span data-stu-id="e70e4-398">This does not indicate the presence of such a file, only that the configuration specifies one.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-399">**LockOnDisconnect**</span><span class="sxs-lookup"><span data-stu-id="e70e4-399">**LockOnDisconnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-400">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e70e4-400">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-401">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-401">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-402">Bloquear la consola al desconectarse de vmconnect.</span><span class="sxs-lookup"><span data-stu-id="e70e4-402">Lock the console when disconnecting from vmconnect.</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-403">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e70e4-403">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="e70e4-404">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="e70e4-404">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-405">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-406">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-407">La ruta de acceso de un directorio en el que se almacena la información de registro de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-407">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="e70e4-408">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-408">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-409">**LowMmioGapSize**</span><span class="sxs-lookup"><span data-stu-id="e70e4-409">**LowMmioGapSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-410">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e70e4-410">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-411">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-411">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-412">Configura el tamaño, en megabytes, de la primera brecha de MMIO para una máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="e70e4-412">Configures the size, in megabytes, of the first MMIO gap for a virtual machine (VM).</span></span>

<span data-ttu-id="e70e4-413">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e70e4-413">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<span data-ttu-id="e70e4-414">Intervalo: 128 3584</span><span class="sxs-lookup"><span data-stu-id="e70e4-414">Range: 128 3584</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-415">**NetworkBootPreferredProtocol**</span><span class="sxs-lookup"><span data-stu-id="e70e4-415">**NetworkBootPreferredProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-416">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e70e4-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-417">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-417">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-418">Determina si el protocolo preferido para el arranque PXE es IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="e70e4-418">Determines if the preferred protocol for PXE boot is IPv4 or IPv6.</span></span>

<span data-ttu-id="e70e4-419">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e70e4-419">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="e70e4-420">**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="e70e4-420">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="e70e4-421">**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="e70e4-421">**IPv6** (4097)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e70e4-422">**Notas**</span><span class="sxs-lookup"><span data-stu-id="e70e4-422">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-423">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e70e4-423">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-424">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-425">Notas proporcionadas por el usuario que están relacionadas con la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-425">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="e70e4-426">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-426">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-427">**Parent**</span><span class="sxs-lookup"><span data-stu-id="e70e4-427">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-428">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-430">Si esta instancia no representa un sistema basado en una instantánea de una máquina virtual, esta propiedad es **null**.</span><span class="sxs-lookup"><span data-stu-id="e70e4-430">If this instance does not represent a system based on a snapshot of a virtual machine, this property is **Null**.</span></span> <span data-ttu-id="e70e4-431">De lo contrario, la propiedad contiene la ruta de acceso del objeto **\_ VirtualSystemSettingData MSVM** en el que se basa esta instancia.</span><span class="sxs-lookup"><span data-stu-id="e70e4-431">Otherwise, the property holds the object path of the **Msvm\_VirtualSystemSettingData** object on which this instance is based.</span></span> <span data-ttu-id="e70e4-432">Al crear una jerarquía de árbol de instantáneas para la máquina virtual, esta propiedad hace referencia al objeto del que se deriva la instancia actual (la instancia actual es el nodo secundario y el objeto al que se hace referencia en esta propiedad es el nodo primario).</span><span class="sxs-lookup"><span data-stu-id="e70e4-432">When building a snapshot tree hierarchy for the virtual machine, this property references the object from which the current instance is derived (the current instance is the child node and the object referenced in this property is the parent node.)</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-433">**ParentPackage**</span><span class="sxs-lookup"><span data-stu-id="e70e4-433">**ParentPackage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-434">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-435">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-435">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-436">Si este sistema es un contenedor, la ruta de acceso al MSVM \_ ContainerPackage desde el que se basa este sistema.</span><span class="sxs-lookup"><span data-stu-id="e70e4-436">If this system is a container, the path to the Msvm\_ContainerPackage from which this system is based.</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-437">Agregado en Windows 10; se quitó en Windows 10, versión 1703.</span><span class="sxs-lookup"><span data-stu-id="e70e4-437">Added in Windows 10; removed in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="e70e4-438">**PauseAfterBootFailure**</span><span class="sxs-lookup"><span data-stu-id="e70e4-438">**PauseAfterBootFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-439">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e70e4-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-440">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-440">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-441">Indica si el BIOS se detiene después de que se produzca un error en la entrada de arranque esperando a que el usuario presione una tecla.</span><span class="sxs-lookup"><span data-stu-id="e70e4-441">Indicates whether the BIOS pauses after every boot entry failure waiting for the user to press a key.</span></span> <span data-ttu-id="e70e4-442">**True** si el BIOS se pausa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e70e4-442">**True** if the BIOS pauses; otherwise, **False**.</span></span>

<span data-ttu-id="e70e4-443">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e70e4-443">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-444">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="e70e4-444">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-445">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-446">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-447">La ruta de acceso completa de un archivo donde se almacena información relacionada con la recuperación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-447">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="e70e4-448">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-448">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-449">**SecureBootEnabled**</span><span class="sxs-lookup"><span data-stu-id="e70e4-449">**SecureBootEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-450">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e70e4-450">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-451">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-451">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-452">Indica si está habilitado el arranque seguro para la máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="e70e4-452">Indicates whether secure boot is enabled for the virtual machine (VM).</span></span> <span data-ttu-id="e70e4-453">**True** si está habilitado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="e70e4-453">**True** if enabled; otherwise, **False**.</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-454">El arranque seguro solo se puede habilitar para las máquinas virtuales de generación 2.</span><span class="sxs-lookup"><span data-stu-id="e70e4-454">Secure boot can only be enabled for generation 2 VMs.</span></span>

 

<span data-ttu-id="e70e4-455">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e70e4-455">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-456">**SecureBootTemplateId**</span><span class="sxs-lookup"><span data-stu-id="e70e4-456">**SecureBootTemplateId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-457">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-458">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-458">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-459">Identificador único global de la plantilla de valores iniciales de las variables relacionadas con el arranque seguro de UEFI.</span><span class="sxs-lookup"><span data-stu-id="e70e4-459">The globally-unique identifier of the template of intial values of UEFI Secure Boot related variables.</span></span>

<span data-ttu-id="e70e4-460">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e70e4-460">This is a read-only property, but it can be changed using the [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-461">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e70e4-461">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="e70e4-462">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="e70e4-462">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-463">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-464">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-465">La ruta de acceso de un directorio donde se almacena información sobre las instantáneas de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-465">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="e70e4-466">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-466">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-467">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="e70e4-467">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-468">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-469">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-470">La ruta de acceso de un directorio donde se almacena información relacionada con la suspensión de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-470">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="e70e4-471">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-471">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-472">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="e70e4-472">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-473">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-473">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-474">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-475">La ruta de acceso de un directorio donde se almacenan los archivos de intercambio de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e70e4-475">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="e70e4-476">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-476">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-477">**UserSnapshotType**</span><span class="sxs-lookup"><span data-stu-id="e70e4-477">**UserSnapshotType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-478">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e70e4-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-479">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-479">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-480">Indica el tipo de instantánea definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="e70e4-480">Indicates the user-defined snapshot type.</span></span>

> [!Note]  
> <span data-ttu-id="e70e4-481">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e70e4-481">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="e70e4-482"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deshabilitar** (2)</span><span class="sxs-lookup"><span data-stu-id="e70e4-482"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e70e4-483">Deshabilite la creación de cualquier instantánea.</span><span class="sxs-lookup"><span data-stu-id="e70e4-483">Disable the creation of any snapshot.</span></span>

</dd> <dt>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>

<span data-ttu-id="e70e4-484"><span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)</span><span class="sxs-lookup"><span data-stu-id="e70e4-484"><span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e70e4-485">Instantánea coherente con los datos para su uso en el entorno de producción. Realiza una instantánea con el estado de la aplicación cuando no está disponible la capacidad de crear una instantánea coherente con los datos.</span><span class="sxs-lookup"><span data-stu-id="e70e4-485">Data-consistent snapshot for use in the production environment.Performs a snapshot with application state when the ability to create data consistent snapshot is not available.</span></span>

</dd> <dt>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>

<span data-ttu-id="e70e4-486"><span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)</span><span class="sxs-lookup"><span data-stu-id="e70e4-486"><span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e70e4-487">Instantánea coherente con los datos para su uso en el entorno de producción. No crea una instantánea con el estado de la aplicación si no es posible crear una instantánea coherente con los datos.</span><span class="sxs-lookup"><span data-stu-id="e70e4-487">Data-consistent snapshot for use in the production environment.Does not create a snapshot with application state if it is not possible to create a data consistent snapshot.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="e70e4-488"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (5)</span><span class="sxs-lookup"><span data-stu-id="e70e4-488"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e70e4-489">Instantánea que contiene la información de memoria y de dispositivo para fines de desarrollo y pruebas.</span><span class="sxs-lookup"><span data-stu-id="e70e4-489">Snapshot that contains memory and device information for test and development purpose.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e70e4-490">**Versión**</span><span class="sxs-lookup"><span data-stu-id="e70e4-490">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-491">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-492">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-493">La versión de la máquina virtual con el formato "Major. minor", por ejemplo "2,0".</span><span class="sxs-lookup"><span data-stu-id="e70e4-493">The version of the virtual machine in a format of "major.minor", for example "2.0".</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-494">**VirtualNumaEnabled**</span><span class="sxs-lookup"><span data-stu-id="e70e4-494">**VirtualNumaEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-495">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e70e4-495">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-496">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e70e4-496">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-497">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**","[**MSVM \_ MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")</span><span class="sxs-lookup"><span data-stu-id="e70e4-497">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**", "[**Msvm\_MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-498">**True** si los nodos de acceso a memoria no uniforme (Numa) virtual se proyectan en la máquina virtual; **False** si la máquina virtual tendrá un solo nodo.</span><span class="sxs-lookup"><span data-stu-id="e70e4-498">**True** if virtual non-uniform memory access (NUMA) nodes are projected into the virtual machine; **False** if the virtual machine will have a single node.</span></span> <span data-ttu-id="e70e4-499">Si es **true**, el número de nodos Numa virtuales proyectados en la máquina virtual se determina a partir de los valores de las propiedades [**MSVM \_ ProcessorSettingData. MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) y [**MSVM MemorySettingData. \_ MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="e70e4-499">If **True**, the number of virtual NUMA nodes projected into the virtual machine is determined from the values of the [**Msvm\_ProcessorSettingData.MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) and [**Msvm\_MemorySettingData.MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-500">**Virtualsystemidentifer**</span><span class="sxs-lookup"><span data-stu-id="e70e4-500">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-501">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-502">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-503">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemSettingData. virtualsystemidentifer"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**")</span><span class="sxs-lookup"><span data-stu-id="e70e4-503">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemSettingData.VirtualSystemIdentifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-504">Nombre del objeto [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) al que pertenecen estos datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="e70e4-504">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="e70e4-505">Esta propiedad es una invalidación de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e70e4-505">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e70e4-506">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="e70e4-506">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-507">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-507">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-508">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-509">Los valores válidos para esta propiedad son Microsoft: Hyper-V: SubType: 1 y Microsoft: Hyper-V: SubType: 2.</span><span class="sxs-lookup"><span data-stu-id="e70e4-509">The valid values for this property are Microsoft:Hyper-V:SubType:1 and Microsoft:Hyper-V:SubType:2.</span></span> <span data-ttu-id="e70e4-510">Una máquina virtual de generación 1 es el subtipo 1.</span><span class="sxs-lookup"><span data-stu-id="e70e4-510">A  Generation 1  VM is subtype 1.</span></span> <span data-ttu-id="e70e4-511">Una máquina virtual de generación 2 es el subtipo 2.</span><span class="sxs-lookup"><span data-stu-id="e70e4-511">A  Generation 2  VM is subtype 2.</span></span>

<span data-ttu-id="e70e4-512">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e70e4-512">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="e70e4-513">**Microsoft: Hyper-v: subtipo: 1** ("Microsoft: Hyper-v: SubType: 1")</span><span class="sxs-lookup"><span data-stu-id="e70e4-513">**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="e70e4-514">**Microsoft: Hyper-v: subtipo: 2** ("Microsoft: Hyper-v: SubType: 2")</span><span class="sxs-lookup"><span data-stu-id="e70e4-514">**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e70e4-515">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="e70e4-515">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e4-516">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e70e4-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e70e4-517">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e70e4-517">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e70e4-518">Especifica el tipo de máquina virtual que representan los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="e70e4-518">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="e70e4-519">Esta propiedad se hereda de la [**clase \_ VirtualSystemSettingData de CIM**](/previous-versions//cc136954(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e70e4-519">This property is inherited from the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) class.</span></span> <span data-ttu-id="e70e4-520">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e70e4-520">This will be one of the following values.</span></span>



| <span data-ttu-id="e70e4-521">Value</span><span class="sxs-lookup"><span data-stu-id="e70e4-521">Value</span></span>                                                                                                                                 | <span data-ttu-id="e70e4-522">Significado</span><span class="sxs-lookup"><span data-stu-id="e70e4-522">Meaning</span></span>                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="e70e4-523"><dt>"Microsoft: Hyper-V: System: realizado"</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-523"><dt>"Microsoft:Hyper-V:System:Realized"</dt></span></span> </dl>                        | <span data-ttu-id="e70e4-524">Una máquina virtual realizada.</span><span class="sxs-lookup"><span data-stu-id="e70e4-524">A realized virtual machine.</span></span><br/>               |
| <dl> <span data-ttu-id="e70e4-525"><dt>"Microsoft: Hyper-V: System: planeado"</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-525"><dt>"Microsoft:Hyper-V:System:Planned"</dt></span></span> </dl>                         | <span data-ttu-id="e70e4-526">Una máquina virtual planeada.</span><span class="sxs-lookup"><span data-stu-id="e70e4-526">A planned virtual machine.</span></span><br/>                |
| <dl> <span data-ttu-id="e70e4-527"><dt>"Microsoft: Hyper-V: Snapshot: realizado"</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-527"><dt>"Microsoft:Hyper-V:Snapshot:Realized"</dt></span></span> </dl>                      | <span data-ttu-id="e70e4-528">Una instantánea de una máquina virtual realizada.</span><span class="sxs-lookup"><span data-stu-id="e70e4-528">A snapshot of a realized virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="e70e4-529"><dt>"Microsoft: Hyper-V: Snapshot: Recovery"</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-529"><dt>"Microsoft:Hyper-V:Snapshot:Recovery"</dt></span></span> </dl>                      | <span data-ttu-id="e70e4-530">Una instantánea de una máquina virtual de recuperación.</span><span class="sxs-lookup"><span data-stu-id="e70e4-530">A snapshot of a recovery virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="e70e4-531"><dt>"Microsoft: Hyper-V: Snapshot: planeado"</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-531"><dt>"Microsoft:Hyper-V:Snapshot:Planned"</dt></span></span> </dl>                       | <span data-ttu-id="e70e4-532">Una instantánea de una máquina virtual planeada.</span><span class="sxs-lookup"><span data-stu-id="e70e4-532">A snapshot of a planned virtual machine.</span></span><br/>  |
| <dl> <span data-ttu-id="e70e4-533"><dt>"Microsoft: Hyper-V: Snapshot: Missing"</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-533"><dt>"Microsoft:Hyper-V:Snapshot:Missing"</dt></span></span> </dl>                       | <span data-ttu-id="e70e4-534">Una instantánea que falta.</span><span class="sxs-lookup"><span data-stu-id="e70e4-534">A missing snapshot.</span></span><br/>                       |
| <dl> <span data-ttu-id="e70e4-535"><dt>"Microsoft: Hyper-V: Snapshot: replica: Standard"</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-535"><dt>"Microsoft:Hyper-V:Snapshot:Replica:Standard"</dt></span></span> </dl>              | <span data-ttu-id="e70e4-536">Una instantánea de punto de replicación basada en tiempo.</span><span class="sxs-lookup"><span data-stu-id="e70e4-536">A time-based replication point snapshot.</span></span><br/>  |
| <dl> <span data-ttu-id="e70e4-537"><dt>"Microsoft: Hyper-V: Snapshot: replica: ApplicationConsistent"</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-537"><dt>"Microsoft:Hyper-V:Snapshot:Replica:ApplicationConsistent"</dt></span></span> </dl> | <span data-ttu-id="e70e4-538">Una instantánea de punto de replicación de VSS.</span><span class="sxs-lookup"><span data-stu-id="e70e4-538">A VSS replication point snapshot.</span></span><br/>         |
| <dl> <span data-ttu-id="e70e4-539"><dt>"Microsoft: Hyper-V: Snapshot: replica: PlannedFailover"</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-539"><dt>"Microsoft:Hyper-V:Snapshot:Replica:PlannedFailover"</dt></span></span> </dl>       | <span data-ttu-id="e70e4-540">Una instantánea de replicación planeada.</span><span class="sxs-lookup"><span data-stu-id="e70e4-540">A planned replication snapshot.</span></span><br/>           |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e70e4-541">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e70e4-541">Remarks</span></span>

<span data-ttu-id="e70e4-542">El acceso a la clase **MSVM \_ VirtualSystemSettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="e70e4-542">Access to the **Msvm\_VirtualSystemSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e70e4-543">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e70e4-543">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e70e4-544">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e70e4-544">Requirements</span></span>



| <span data-ttu-id="e70e4-545">Requisito</span><span class="sxs-lookup"><span data-stu-id="e70e4-545">Requirement</span></span> | <span data-ttu-id="e70e4-546">Value</span><span class="sxs-lookup"><span data-stu-id="e70e4-546">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e70e4-547">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e70e4-547">Minimum supported client</span></span><br/> | <span data-ttu-id="e70e4-548">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e70e4-548">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e70e4-549">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e70e4-549">Minimum supported server</span></span><br/> | <span data-ttu-id="e70e4-550">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e70e4-550">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e70e4-551">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e70e4-551">Namespace</span></span><br/>                | <span data-ttu-id="e70e4-552">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e70e4-552">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e70e4-553">MOF</span><span class="sxs-lookup"><span data-stu-id="e70e4-553">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e70e4-554"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-554"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e70e4-555">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e70e4-555">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e70e4-556"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e70e4-556"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e70e4-557">Vea también</span><span class="sxs-lookup"><span data-stu-id="e70e4-557">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e70e4-558">**\_VIRTUALSYSTEMSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="e70e4-558">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> <dt>

<span data-ttu-id="e70e4-559">[**\_VIRTUALSYSTEMSETTINGDATA CIM**](/previous-versions//cc136954(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e70e4-559">[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e70e4-560">Clases de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="e70e4-560">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

