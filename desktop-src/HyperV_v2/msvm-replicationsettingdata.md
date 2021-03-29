---
description: Representa la configuración específica de la replicación para una máquina virtual.
ms.assetid: f6f6a413-a949-4aca-930b-37e39bdc1fdb
title: Msvm_ReplicationSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationSettingData
- Msvm_ReplicationSettingData.InstanceID
- Msvm_ReplicationSettingData.Caption
- Msvm_ReplicationSettingData.Description
- Msvm_ReplicationSettingData.ElementName
- Msvm_ReplicationSettingData.VirtualSystemIdentifier
- Msvm_ReplicationSettingData.VirtualSystemType
- Msvm_ReplicationSettingData.Notes
- Msvm_ReplicationSettingData.CreationTime
- Msvm_ReplicationSettingData.ConfigurationID
- Msvm_ReplicationSettingData.ConfigurationDataRoot
- Msvm_ReplicationSettingData.ConfigurationFile
- Msvm_ReplicationSettingData.SnapshotDataRoot
- Msvm_ReplicationSettingData.SuspendDataRoot
- Msvm_ReplicationSettingData.SwapFileDataRoot
- Msvm_ReplicationSettingData.LogDataRoot
- Msvm_ReplicationSettingData.AutomaticStartupAction
- Msvm_ReplicationSettingData.AutomaticStartupActionDelay
- Msvm_ReplicationSettingData.AutomaticStartupActionSequenceNumber
- Msvm_ReplicationSettingData.AutomaticShutdownAction
- Msvm_ReplicationSettingData.AutomaticRecoveryAction
- Msvm_ReplicationSettingData.RecoveryFile
- Msvm_ReplicationSettingData.AuthenticationType
- Msvm_ReplicationSettingData.CertificateThumbPrint
- Msvm_ReplicationSettingData.RootCertificateThumbPrint
- Msvm_ReplicationSettingData.CompressionEnabled
- Msvm_ReplicationSettingData.BypassProxyServer
- Msvm_ReplicationSettingData.RecoveryConnectionPoint
- Msvm_ReplicationSettingData.RecoveryHostSystem
- Msvm_ReplicationSettingData.PrimaryConnectionPoint
- Msvm_ReplicationSettingData.PrimaryHostSystem
- Msvm_ReplicationSettingData.RecoveryServerPortNumber
- Msvm_ReplicationSettingData.ReplicateHostKvpItems
- Msvm_ReplicationSettingData.ApplicationConsistentSnapshotInterval
- Msvm_ReplicationSettingData.RecoveryHistory
- Msvm_ReplicationSettingData.IncludedDisks
- Msvm_ReplicationSettingData.AutoResynchronizeEnabled
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalStart
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalEnd
- Msvm_ReplicationSettingData.EnableWriteOrderPreservationAcrossDisks
- Msvm_ReplicationSettingData.ReplicationProvider
- Msvm_ReplicationSettingData.AdditionalSettings
- Msvm_ReplicationSettingData.ReplicationInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35bb97e531f8aca5f74801d55a71e5b3f2850c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277382"
---
# <a name="msvm_replicationsettingdata-class"></a><span data-ttu-id="ea326-103">MSVM \_ ReplicationSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="ea326-103">Msvm\_ReplicationSettingData class</span></span>

<span data-ttu-id="ea326-104">Representa la configuración específica de la replicación para una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ea326-104">Represents the replication-specific settings for a virtual machine.</span></span> <span data-ttu-id="ea326-105">El cliente pasa una instancia de esta clase a [**MSVM \_ ReplicationService. CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) para crear una relación de replicación.</span><span class="sxs-lookup"><span data-stu-id="ea326-105">The client passes an instance of this class to [**Msvm\_ReplicationService.CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) to create a replication relationship.</span></span> <span data-ttu-id="ea326-106">El cliente no puede cambiar directamente los valores de cualquiera de las propiedades de esta clase; debe llamar al método [**MSVM \_ ReplicationService. ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) para cambiar los valores.</span><span class="sxs-lookup"><span data-stu-id="ea326-106">The client can't directly change the values of any of the properties for this class; it must call the [**Msvm\_ReplicationService.ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) method to change the values.</span></span> <span data-ttu-id="ea326-107">Cada relación de replicación tiene una única instancia de configuración.</span><span class="sxs-lookup"><span data-stu-id="ea326-107">Each replication relationship has a single instance of settings.</span></span>

<span data-ttu-id="ea326-108">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ea326-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea326-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea326-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID = "Microsoft:Virtual Machine GUID\HVR";
  string   Caption = "Replication Settings";
  string   Description = "Virtual Machine Replication Settings Data";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType = "Microsoft:Hyper-V:Replica";
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
  uint16   AuthenticationType;
  string   CertificateThumbPrint;
  string   RootCertificateThumbPrint;
  boolean  CompressionEnabled;
  boolean  BypassProxyServer;
  string   RecoveryConnectionPoint;
  string   RecoveryHostSystem;
  string   PrimaryConnectionPoint;
  string   PrimaryHostSystem;
  uint16   RecoveryServerPortNumber = 0;
  boolean  ReplicateHostKvpItems = True;
  uint16   ApplicationConsistentSnapshotInterval;
  uint16   RecoveryHistory = 0;
  string   IncludedDisks[];
  boolean  AutoResynchronizeEnabled = False;
  datetime AutoResynchronizeIntervalStart = 00000000183000.000000:000;
  datetime AutoResynchronizeIntervalEnd = 00000000060000.000000:000;
  boolean  EnableWriteOrderPreservationAcrossDisks;
  string   ReplicationProvider;
  string   AdditionalSettings;
  uint16   ReplicationInterval = 300;
};
```

## <a name="members"></a><span data-ttu-id="ea326-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="ea326-110">Members</span></span>

<span data-ttu-id="ea326-111">La clase **MSVM \_ ReplicationSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ea326-111">The **Msvm\_ReplicationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ea326-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ea326-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea326-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ea326-113">Properties</span></span>

<span data-ttu-id="ea326-114">La clase **MSVM \_ ReplicationSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ea326-114">The **Msvm\_ReplicationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea326-115">**AdditionalSettings**</span><span class="sxs-lookup"><span data-stu-id="ea326-115">**AdditionalSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-118">Configuración de replicación adicional que puede usar el proveedor de puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="ea326-118">Additional replication settings that the endpoint provider can use.</span></span>

<span data-ttu-id="ea326-119">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="ea326-119">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-120">**ApplicationConsistentSnapshotInterval**</span><span class="sxs-lookup"><span data-stu-id="ea326-120">**ApplicationConsistentSnapshotInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-121">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea326-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-123">El intervalo de tiempo entre las instantáneas coherentes con la aplicación, especificado en horas.</span><span class="sxs-lookup"><span data-stu-id="ea326-123">The time interval between application consistent snapshots, specified in hours.</span></span> <span data-ttu-id="ea326-124">Los valores válidos son de 1 hora a 12 horas.</span><span class="sxs-lookup"><span data-stu-id="ea326-124">Valid values are from 1 hour to 12 hours.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-125">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="ea326-125">**AuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea326-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-128">Defina el modo de autenticación usado para conectarse al servidor de recuperación.</span><span class="sxs-lookup"><span data-stu-id="ea326-128">Define authentication mode used to connect to recover server.</span></span>

<dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="ea326-129"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Autenticación Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="ea326-129"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ea326-130">Autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="ea326-130">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="ea326-131"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticación basada en certificados** (2)</span><span class="sxs-lookup"><span data-stu-id="ea326-131"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ea326-132">Autenticación basada en certificados.</span><span class="sxs-lookup"><span data-stu-id="ea326-132">Certificate based authentication.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ea326-133">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="ea326-133">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-134">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea326-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-136">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ea326-136">Not used.</span></span>

<span data-ttu-id="ea326-137">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea326-137">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea326-138">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="ea326-138">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea326-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-141">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ea326-141">Not used.</span></span>

<span data-ttu-id="ea326-142">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea326-142">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea326-143">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="ea326-143">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-144">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea326-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-146">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ea326-146">Not used.</span></span>

<span data-ttu-id="ea326-147">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea326-147">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea326-148">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="ea326-148">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-149">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ea326-149">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-151">El tiempo de retardo antes de que la máquina virtual se inicie automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ea326-151">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="ea326-152">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ea326-152">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-153">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="ea326-153">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-154">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea326-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-156">Número que indica la secuencia relativa de activación de la máquina virtual cuando se inicia el sistema host.</span><span class="sxs-lookup"><span data-stu-id="ea326-156">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="ea326-157">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ea326-157">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-158">**AutoResynchronizeEnabled**</span><span class="sxs-lookup"><span data-stu-id="ea326-158">**AutoResynchronizeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-159">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ea326-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-161">Especifica si las operaciones de resincronización se desencadenan automáticamente cuando se produce un error de replicación debido a errores de hardware y energía.</span><span class="sxs-lookup"><span data-stu-id="ea326-161">Specifies whether resynchronization operations are automatically triggered when a replication error occurs due to power and hardware failures.</span></span> <span data-ttu-id="ea326-162">Las operaciones de resincronización solo se desencadenan cuando el error se produce entre las horas especificadas por las propiedades **AutoResynchronizeIntervalStart** y **AutoResynchronizeIntervalEnd** .</span><span class="sxs-lookup"><span data-stu-id="ea326-162">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="ea326-163">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="ea326-163">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-164">**AutoResynchronizeIntervalEnd**</span><span class="sxs-lookup"><span data-stu-id="ea326-164">**AutoResynchronizeIntervalEnd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-165">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ea326-165">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-167">Especifica la hora de finalización de las operaciones de resincronización automática que se van a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="ea326-167">Specifies the end time for automatic resynchronization operations to be triggered.</span></span> <span data-ttu-id="ea326-168">Este valor se encuentra en la hora local.</span><span class="sxs-lookup"><span data-stu-id="ea326-168">This value is in local time.</span></span> <span data-ttu-id="ea326-169">El valor predeterminado es 06:00 (6:00 A.M.).</span><span class="sxs-lookup"><span data-stu-id="ea326-169">The default value is 06:00 (6:00 A.M.).</span></span>

<span data-ttu-id="ea326-170">Las operaciones de resincronización solo se desencadenan cuando el error se produce entre las horas especificadas por las propiedades **AutoResynchronizeIntervalStart** y **AutoResynchronizeIntervalEnd** .</span><span class="sxs-lookup"><span data-stu-id="ea326-170">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="ea326-171">Las operaciones de resincronización también pueden programarse para que se desencadenen durante el siguiente intervalo.</span><span class="sxs-lookup"><span data-stu-id="ea326-171">Resynchronization operations can also be scheduled so that they are triggered during the next interval.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-172">**AutoResynchronizeIntervalStart**</span><span class="sxs-lookup"><span data-stu-id="ea326-172">**AutoResynchronizeIntervalStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-173">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ea326-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-175">Especifica la hora de inicio de las operaciones de resincronización automática que se van a desencadenar.</span><span class="sxs-lookup"><span data-stu-id="ea326-175">Specifies the start time for automatic resynchronization operations to be triggered.</span></span> <span data-ttu-id="ea326-176">Este valor se encuentra en la hora local.</span><span class="sxs-lookup"><span data-stu-id="ea326-176">This value is in local time.</span></span> <span data-ttu-id="ea326-177">El valor predeterminado es 18:30 (6:30 P.M.).</span><span class="sxs-lookup"><span data-stu-id="ea326-177">The default value is 18:30 (6:30 P.M.).</span></span>

<span data-ttu-id="ea326-178">Las operaciones de resincronización solo se desencadenan cuando el error se produce entre las horas especificadas por las propiedades **AutoResynchronizeIntervalStart** y **AutoResynchronizeIntervalEnd** .</span><span class="sxs-lookup"><span data-stu-id="ea326-178">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="ea326-179">Las operaciones de resincronización también pueden programarse para que se desencadenen durante el siguiente intervalo.</span><span class="sxs-lookup"><span data-stu-id="ea326-179">Resynchronization operations can also be scheduled so that they are triggered during the next interval.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-180">**BypassProxyServer**</span><span class="sxs-lookup"><span data-stu-id="ea326-180">**BypassProxyServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-181">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ea326-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-183">Especifica si se debe omitir el servidor proxy al conectarse a un servidor de recuperación.</span><span class="sxs-lookup"><span data-stu-id="ea326-183">Specifies whether the proxy server should be bypassed when connecting to a recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ea326-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-187">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ea326-187">A short description of the object.</span></span> <span data-ttu-id="ea326-188">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración de replicación".</span><span class="sxs-lookup"><span data-stu-id="ea326-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Settings".</span></span>

</dd> <dt>

<span data-ttu-id="ea326-189">**CertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="ea326-189">**CertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea326-192">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="ea326-192">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="ea326-193">Huella digital del certificado que se usará cuando la propiedad **AuthenticationType** sea autenticación basada en certificados.</span><span class="sxs-lookup"><span data-stu-id="ea326-193">Certificate thumbprint to use when the **AuthenticationType** property is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-194">**CompressionEnabled**</span><span class="sxs-lookup"><span data-stu-id="ea326-194">**CompressionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-195">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ea326-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-197">Especifica si los datos de replicación se comprimirán mientras se envían al servidor de recuperación.</span><span class="sxs-lookup"><span data-stu-id="ea326-197">Specifies whether replication data will be compressed while sending it to the recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-198">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="ea326-198">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-201">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ea326-201">Not used.</span></span>

<span data-ttu-id="ea326-202">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea326-202">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea326-203">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="ea326-203">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-206">La ruta de acceso relativa y el nombre de un archivo donde se almacena la información sobre la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ea326-206">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="ea326-207">Esta ruta de acceso es relativa a la propiedad **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="ea326-207">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="ea326-208">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ea326-208">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-209">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="ea326-209">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-212">Identificador único de la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ea326-212">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="ea326-213">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ea326-213">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-214">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="ea326-214">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-215">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ea326-215">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-217">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ea326-217">The date and time at which the settings for the virtual machine were created.</span></span> <span data-ttu-id="ea326-218">Si este objeto representa la configuración actual de la máquina virtual, este valor sería la hora a la que se creó el sistema.</span><span class="sxs-lookup"><span data-stu-id="ea326-218">If this object represents the current settings for the virtual machine, this value would be the time at which the system was created.</span></span> <span data-ttu-id="ea326-219">Si este objeto representa la configuración de instantánea de la máquina virtual, este valor sería la hora a la que se tomó la instantánea.</span><span class="sxs-lookup"><span data-stu-id="ea326-219">If this object represents the snapshot settings for the virtual machine, this value would be the time at which the snapshot was taken.</span></span> <span data-ttu-id="ea326-220">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea326-220">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="ea326-221">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ea326-221">This is a read-only property, but it can be changed by using the [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="ea326-222">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea326-222">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea326-223">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ea326-223">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-224">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-226">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ea326-226">A description of the object.</span></span> <span data-ttu-id="ea326-227">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "datos de configuración de replicación de máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="ea326-227">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Machine Replication Settings Data".</span></span>

</dd> <dt>

<span data-ttu-id="ea326-228">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ea326-228">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-229">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-231">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="ea326-231">A display name for the object.</span></span> <span data-ttu-id="ea326-232">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y está establecida en el nombre para mostrar de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ea326-232">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is set to the display name for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-233">**EnableWriteOrderPreservationAcrossDisks**</span><span class="sxs-lookup"><span data-stu-id="ea326-233">**EnableWriteOrderPreservationAcrossDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-234">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ea326-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea326-236">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sin valor")</span><span class="sxs-lookup"><span data-stu-id="ea326-236">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="ea326-237">Especifica si todos los discos duros virtuales de replicación de la máquina virtual se replican al mismo punto en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="ea326-237">Specifies whether all replicating virtual hard disks for the virtual machine are replicated to the same point in time.</span></span> <span data-ttu-id="ea326-238">Esto garantiza que la replicación respete el orden de escritura de las aplicaciones en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ea326-238">This ensures replication honors the write-order of the applications in the virtual machine.</span></span>

<span data-ttu-id="ea326-239">**Windows 8.1:** A partir de Windows 8.1 y Windows Server 2012 R2, esta propiedad está en desuso y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="ea326-239">**Windows 8.1:** Beginning with Windows 8.1 and Windows Server 2012 R2, this property is deprecated and always set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-240">**IncludedDisks**</span><span class="sxs-lookup"><span data-stu-id="ea326-240">**IncludedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-241">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ea326-241">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea326-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea326-243">Calificadores: **HyperVEmbeddedInstance** ("CIM \_ StorageAllocationSettingData"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="ea326-243">Qualifiers: **HyperVEmbeddedInstance** ("CIM\_StorageAllocationSettingData"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ea326-244">La lista de discos duros virtuales (VHD) conectados al sistema que replicará el motor de replicación.</span><span class="sxs-lookup"><span data-stu-id="ea326-244">The list of virtual hard disks (VHDs) attached to the system that will be replicated by the replication engine.</span></span> <span data-ttu-id="ea326-245">Se trata de una matriz de cadenas, cada una de las cuales contiene el **InstanceID** del [**\_ StorageAllocationSettingData de MSVM**](msvm-storageallocationsettingdata.md) que representa el VHD.</span><span class="sxs-lookup"><span data-stu-id="ea326-245">This is an array of strings, each containing the **InstanceID** of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) that represents the VHD.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ea326-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea326-249">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="ea326-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ea326-250">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="ea326-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ea326-251">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea326-251">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="ea326-252">En Windows 8, siempre se establece en "Microsoft:*GUID de máquina virtual* \\ HVR".</span><span class="sxs-lookup"><span data-stu-id="ea326-252">For Windows 8, it is always set to "Microsoft:*Virtual Machine GUID*\\HVR".</span></span> <span data-ttu-id="ea326-253">Por Windows 8.1, se establece en "Microsoft:*GUID de máquina virtual* \\ HVR \\<0/1>".</span><span class="sxs-lookup"><span data-stu-id="ea326-253">For Windows 8.1, it is set to "Microsoft:*Virtual Machine GUID*\\HVR\\<0/1>".</span></span> <span data-ttu-id="ea326-254">En el valor Windows 8.1, 0 indica principal y 1 indica replicación extendida.</span><span class="sxs-lookup"><span data-stu-id="ea326-254">In the Windows 8.1 value, 0 indicates primary and 1 indicates extended replication.</span></span> <span data-ttu-id="ea326-255">Para obtener más información acerca de la replicación extendida, consulte [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).</span><span class="sxs-lookup"><span data-stu-id="ea326-255">For more info about extended replication, see [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea326-256">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="ea326-256">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-259">La ruta de acceso de un directorio en el que se almacena la información de registro de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ea326-259">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="ea326-260">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ea326-260">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-261">**Notas**</span><span class="sxs-lookup"><span data-stu-id="ea326-261">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-262">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ea326-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea326-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-264">No se utiliza y no se puede establecer.</span><span class="sxs-lookup"><span data-stu-id="ea326-264">Not used and can't be set.</span></span>

<span data-ttu-id="ea326-265">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea326-265">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea326-266">**PrimaryConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="ea326-266">**PrimaryConnectionPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-267">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea326-269">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ea326-269">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ea326-270">Nombre del punto de conexión principal.</span><span class="sxs-lookup"><span data-stu-id="ea326-270">The name of the primary connection point.</span></span> <span data-ttu-id="ea326-271">En el caso de un clúster principal, este es el nombre de la CAP de agente.</span><span class="sxs-lookup"><span data-stu-id="ea326-271">In the case of a primary cluster, this is the broker CAP name.</span></span> <span data-ttu-id="ea326-272">En el caso de un servidor principal independiente, es el nombre del sistema host.</span><span class="sxs-lookup"><span data-stu-id="ea326-272">In the case of a standalone primary server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-273">**PrimaryHostSystem**</span><span class="sxs-lookup"><span data-stu-id="ea326-273">**PrimaryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-274">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea326-276">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ea326-276">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ea326-277">El nombre de dominio completo del sistema host principal que hospeda la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ea326-277">The fully qualified domain name of the primary host system that is hosting the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-278">**RecoveryConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="ea326-278">**RecoveryConnectionPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-279">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea326-281">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ea326-281">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ea326-282">Nombre del punto de conexión de recuperación.</span><span class="sxs-lookup"><span data-stu-id="ea326-282">The name of the recovery connection point.</span></span> <span data-ttu-id="ea326-283">En el caso de un clúster de recuperación, este es el nombre de la CAP de agente.</span><span class="sxs-lookup"><span data-stu-id="ea326-283">In the case of a recovery cluster, this is the broker CAP name.</span></span> <span data-ttu-id="ea326-284">En el caso de un servidor de recuperación independiente, es el nombre del sistema host.</span><span class="sxs-lookup"><span data-stu-id="ea326-284">In the case of a standalone recovery server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-285">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="ea326-285">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-288">La ruta de acceso completa de un archivo donde se almacena información relacionada con la recuperación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ea326-288">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="ea326-289">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ea326-289">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-290">**RecoveryHistory**</span><span class="sxs-lookup"><span data-stu-id="ea326-290">**RecoveryHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-291">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea326-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-293">El número máximo de instantáneas de recuperación que se almacenarán en el servidor de recuperación.</span><span class="sxs-lookup"><span data-stu-id="ea326-293">The maximum number of recovery snapshots that will be stored on the recovery server.</span></span> <span data-ttu-id="ea326-294">Los valores válidos son de 0 a 24.</span><span class="sxs-lookup"><span data-stu-id="ea326-294">Valid values are from 0 to 24.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-295">**RecoveryHostSystem**</span><span class="sxs-lookup"><span data-stu-id="ea326-295">**RecoveryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-296">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea326-298">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ea326-298">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ea326-299">El nombre de dominio completo del sistema host de recuperación que hospeda la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ea326-299">The fully qualified domain name of the recovery host system which is hosting the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-300">**RecoveryServerPortNumber**</span><span class="sxs-lookup"><span data-stu-id="ea326-300">**RecoveryServerPortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-301">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea326-301">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-303">Número de puerto del servidor de recuperación que se va a usar al establecer una conexión segura para la replicación.</span><span class="sxs-lookup"><span data-stu-id="ea326-303">The recovery server port number to use when making a secure connection for replication.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-304">**ReplicateHostKvpItems**</span><span class="sxs-lookup"><span data-stu-id="ea326-304">**ReplicateHostKvpItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-305">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ea326-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-307">Especifica si se deben replicar los [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)de solo host de la máquina virtual principal a la máquina virtual de recuperación.</span><span class="sxs-lookup"><span data-stu-id="ea326-307">Specifies whether host-only [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)s should be replicated from the primary virtual machine to the recovery virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-308">**ReplicationInterval**</span><span class="sxs-lookup"><span data-stu-id="ea326-308">**ReplicationInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-309">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea326-309">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-311">Intervalo de replicación de una relación de replicación en segundos.</span><span class="sxs-lookup"><span data-stu-id="ea326-311">Replication interval of a replication relationship in seconds.</span></span> <span data-ttu-id="ea326-312">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="ea326-312">Valid values are:</span></span>

<span data-ttu-id="ea326-313">30</span><span class="sxs-lookup"><span data-stu-id="ea326-313">30</span></span>

<span data-ttu-id="ea326-314">300</span><span class="sxs-lookup"><span data-stu-id="ea326-314">300</span></span>

<span data-ttu-id="ea326-315">900</span><span class="sxs-lookup"><span data-stu-id="ea326-315">900</span></span>

<span data-ttu-id="ea326-316">El valor predeterminado es 300 segundos.</span><span class="sxs-lookup"><span data-stu-id="ea326-316">Default value is 300 seconds.</span></span>

<span data-ttu-id="ea326-317">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="ea326-317">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-318">**ReplicationProvider**</span><span class="sxs-lookup"><span data-stu-id="ea326-318">**ReplicationProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-319">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-321">La ruta de acceso a la instancia de la clase [**MSVM \_ ReplicationProvider**](msvm-replicationprovider.md) que identifica el extremo del proveedor de replicación.</span><span class="sxs-lookup"><span data-stu-id="ea326-321">The path to the instance of the [**Msvm\_ReplicationProvider**](msvm-replicationprovider.md) class that identifies the replication provider endpoint.</span></span>

<span data-ttu-id="ea326-322">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="ea326-322">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-323">**RootCertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="ea326-323">**RootCertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea326-326">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="ea326-326">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="ea326-327">Huella digital del certificado raíz del certificado en uso cuando **AuthenticationType** es 2 (autorización basada en certificado).</span><span class="sxs-lookup"><span data-stu-id="ea326-327">Root certificate thumbprint of the certificate in use when **AuthenticationType** is 2 (certificate based authorization).</span></span>

</dd> <dt>

<span data-ttu-id="ea326-328">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="ea326-328">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-329">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-331">La ruta de acceso de un directorio donde se almacena información sobre las instantáneas de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ea326-331">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="ea326-332">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ea326-332">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-333">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="ea326-333">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-334">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-336">La ruta de acceso de un directorio donde se almacena información relacionada con la suspensión de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ea326-336">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="ea326-337">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ea326-337">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-338">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="ea326-338">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-339">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-341">La ruta de acceso de un directorio donde se almacenan los archivos de intercambio de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ea326-341">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="ea326-342">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ea326-342">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea326-343">**Virtualsystemidentifer**</span><span class="sxs-lookup"><span data-stu-id="ea326-343">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-344">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-346">Nombre del objeto [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) al que pertenecen estos datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="ea326-346">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="ea326-347">Esta propiedad es una invalidación de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea326-347">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea326-348">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="ea326-348">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea326-349">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ea326-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea326-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ea326-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea326-351">Especifica el tipo de máquina virtual que representan los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="ea326-351">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="ea326-352">Esta propiedad se hereda de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))y siempre está establecida en "Microsoft: Hyper-V: replica".</span><span class="sxs-lookup"><span data-stu-id="ea326-352">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is always set to "Microsoft:Hyper-V:Replica".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea326-353">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea326-353">Requirements</span></span>



| <span data-ttu-id="ea326-354">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea326-354">Requirement</span></span> | <span data-ttu-id="ea326-355">Value</span><span class="sxs-lookup"><span data-stu-id="ea326-355">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea326-356">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea326-356">Minimum supported client</span></span><br/> | <span data-ttu-id="ea326-357">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea326-357">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ea326-358">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea326-358">Minimum supported server</span></span><br/> | <span data-ttu-id="ea326-359">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea326-359">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ea326-360">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ea326-360">Namespace</span></span><br/>                | <span data-ttu-id="ea326-361">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ea326-361">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ea326-362">MOF</span><span class="sxs-lookup"><span data-stu-id="ea326-362">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea326-363"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea326-363"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea326-364">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ea326-364">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea326-365"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ea326-365"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ea326-366">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea326-366">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea326-367">**\_VIRTUALSYSTEMSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="ea326-367">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> <dt>

[<span data-ttu-id="ea326-368">**ModifyReplicationSettings**</span><span class="sxs-lookup"><span data-stu-id="ea326-368">**ModifyReplicationSettings**</span></span>](modifyreplicationsettings-msvm-replicationservice.md)
</dt> </dl>

 

