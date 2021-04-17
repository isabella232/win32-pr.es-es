---
description: Se usa en los métodos GetSummaryInformation y GetDefinitionFileSummaryInformation de la \_ clase MSVM VirtualSystemManagementService para recuperar rápidamente la información común relacionada con una máquina virtual o una instantánea.
ms.assetid: 8D188BB2-4A56-4738-94DD-64D9F9B90B73
title: Msvm_SummaryInformation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformation
- Msvm_SummaryInformation.InstanceID
- Msvm_SummaryInformation.AllocatedGPU
- Msvm_SummaryInformation.Shielded
- Msvm_SummaryInformation.AsynchronousTasks
- Msvm_SummaryInformation.CreationTime
- Msvm_SummaryInformation.ElementName
- Msvm_SummaryInformation.EnabledState
- Msvm_SummaryInformation.OtherEnabledState
- Msvm_SummaryInformation.GuestOperatingSystem
- Msvm_SummaryInformation.HealthState
- Msvm_SummaryInformation.Heartbeat
- Msvm_SummaryInformation.MemoryUsage
- Msvm_SummaryInformation.MemoryAvailable
- Msvm_SummaryInformation.AvailableMemoryBuffer
- Msvm_SummaryInformation.SwapFilesInUse
- Msvm_SummaryInformation.Name
- Msvm_SummaryInformation.Notes
- Msvm_SummaryInformation.Version
- Msvm_SummaryInformation.NumberOfProcessors
- Msvm_SummaryInformation.OperationalStatus
- Msvm_SummaryInformation.ProcessorLoad
- Msvm_SummaryInformation.ProcessorLoadHistory
- Msvm_SummaryInformation.Snapshots
- Msvm_SummaryInformation.StatusDescriptions
- Msvm_SummaryInformation.ThumbnailImage
- Msvm_SummaryInformation.ThumbnailImageHeight
- Msvm_SummaryInformation.ThumbnailImageWidth
- Msvm_SummaryInformation.UpTime
- Msvm_SummaryInformation.ReplicationState
- Msvm_SummaryInformation.ReplicationStateEx
- Msvm_SummaryInformation.ReplicationHealth
- Msvm_SummaryInformation.ReplicationHealthEx
- Msvm_SummaryInformation.ReplicationMode
- Msvm_SummaryInformation.TestReplicaSystem
- Msvm_SummaryInformation.ApplicationHealth
- Msvm_SummaryInformation.IntegrationServicesVersionState
- Msvm_SummaryInformation.MemorySpansPhysicalNumaNodes
- Msvm_SummaryInformation.ReplicationProviderId
- Msvm_SummaryInformation.EnhancedSessionModeState
- Msvm_SummaryInformation.VirtualSwitchNames
- Msvm_SummaryInformation.VirtualSystemSubType
- Msvm_SummaryInformation.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 817d025551ae10002b008a181edd8a7dfd2ec68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652447"
---
# <a name="msvm_summaryinformation-class"></a><span data-ttu-id="dc374-103">MSVM \_ SummaryInformation (clase)</span><span class="sxs-lookup"><span data-stu-id="dc374-103">Msvm\_SummaryInformation class</span></span>

<span data-ttu-id="dc374-104">Se usa en los métodos [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) y [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para recuperar rápidamente la información común relacionada con una máquina virtual o una instantánea.</span><span class="sxs-lookup"><span data-stu-id="dc374-104">Used in the [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) and [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) methods in the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to quickly retrieve common information related to a virtual machine or snapshot.</span></span>

<span data-ttu-id="dc374-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="dc374-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc374-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc374-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformation : Msvm_SummaryInformationBase
{
  string                       InstanceID;
  string                       AllocatedGPU;
  boolean                      Shielded;
  CIM_ConcreteJob              AsynchronousTasks[];
  DateTime                     CreationTime;
  string                       ElementName;
  uint16                       EnabledState;
  string                       OtherEnabledState;
  string                       GuestOperatingSystem;
  uint16                       HealthState;
  uint16                       Heartbeat;
  uint64                       MemoryUsage;
  sint32                       MemoryAvailable;
  sint32                       AvailableMemoryBuffer;
  boolean                      SwapFilesInUse;
  string                       Name;
  string                       Notes;
  string                       Version;
  uint16                       NumberOfProcessors;
  uint16                       OperationalStatus[];
  uint16                       ProcessorLoad;
  uint16                       ProcessorLoadHistory[];
  CIM_VirtualSystemSettingData Snapshots[];
  string                       StatusDescriptions[];
  uint8                        ThumbnailImage[];
  uint16                       ThumbnailImageHeight;
  uint16                       ThumbnailImageWidth;
  uint64                       UpTime;
  uint16                       ReplicationState;
  uint16                       ReplicationStateEx[];
  uint16                       ReplicationHealth;
  uint16                       ReplicationHealthEx[];
  uint16                       ReplicationMode;
  CIM_ComputerSystem       REF TestReplicaSystem;
  uint16                       ApplicationHealth;
  uint16                       IntegrationServicesVersionState;
  boolean                      MemorySpansPhysicalNumaNodes;
  string                       ReplicationProviderId[];
  uint16                       EnhancedSessionModeState;
  string                       VirtualSwitchNames[];
  string                       VirtualSystemSubType;
  string                       HostComputerSystemName;
};
```

## <a name="members"></a><span data-ttu-id="dc374-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc374-107">Members</span></span>

<span data-ttu-id="dc374-108">La clase **MSVM \_ SummaryInformation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dc374-108">The **Msvm\_SummaryInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="dc374-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc374-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc374-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc374-110">Properties</span></span>

<span data-ttu-id="dc374-111">La clase **MSVM \_ SummaryInformation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dc374-111">The **Msvm\_SummaryInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc374-112">**AllocatedGPU**</span><span class="sxs-lookup"><span data-stu-id="dc374-112">**AllocatedGPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc374-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-115">El identificador de la unidad de procesamiento de gráficos (GPU) física asignada a esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-115">The identifier of the physical graphics processing unit (GPU) allocated to this virtual machine.</span></span> <span data-ttu-id="dc374-116">Esta propiedad solo se aplica a las máquinas virtuales que usan RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="dc374-116">This property only applies to virtual machines that use RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-117">**ApplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="dc374-117">**ApplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-118">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-120">El estado actual de mantenimiento de la aplicación para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-120">The current application health status for the virtual machine.</span></span> <span data-ttu-id="dc374-121">Esta propiedad no es válida para las instancias de **MSVM \_ SummaryInformation** que representan una instantánea de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-121">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dc374-122">**Aceptar** (2)</span><span class="sxs-lookup"><span data-stu-id="dc374-122">**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Critical"></span><span id="application_critical"></span><span id="APPLICATION_CRITICAL"></span>

<span data-ttu-id="dc374-123">**Aplicación crítica** (32782)</span><span class="sxs-lookup"><span data-stu-id="dc374-123">**Application Critical** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dc374-124">**Deshabilitado** (32896)</span><span class="sxs-lookup"><span data-stu-id="dc374-124">**Disabled** (32896)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc374-125">**AsynchronousTasks**</span><span class="sxs-lookup"><span data-stu-id="dc374-125">**AsynchronousTasks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-126">Tipo de datos: matriz **\_ ConcreteJob de CIM**</span><span class="sxs-lookup"><span data-stu-id="dc374-126">Data type: **CIM\_ConcreteJob** array</span></span>
</dt> <dt>

<span data-ttu-id="dc374-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc374-128">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="dc374-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="dc374-129">Matriz de instancias de [**MSVM \_ ConcreteJob**](msvm-concretejob.md) que representan cualquier operación asincrónica relacionada con la máquina virtual que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="dc374-129">An array of [**Msvm\_ConcreteJob**](msvm-concretejob.md) instances that represent any asynchronous operations related to the virtual machine that are currently executing.</span></span> <span data-ttu-id="dc374-130">Esta propiedad no es válida para las instancias de **MSVM \_ SummaryInformation** que representan una instantánea de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-130">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-131">**AvailableMemoryBuffer**</span><span class="sxs-lookup"><span data-stu-id="dc374-131">**AvailableMemoryBuffer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dc374-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-134">El porcentaje de búfer de memoria disponible para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-134">The percentage of available memory buffer for the virtual machine.</span></span> <span data-ttu-id="dc374-135">Cuando se habilita la memoria dinámica para una máquina virtual, esta propiedad representa la proporción de búfer de memoria disponible en el búfer de memoria ideal para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-135">When dynamic memory is enabled for a virtual machine, this property represents the ratio of available memory buffer to the ideal memory buffer for the virtual machine.</span></span> <span data-ttu-id="dc374-136">El tamaño de búfer de memoria ideal se configura mediante la propiedad **TargetMemoryBuffer** de la clase [**\_ MemorySettingData de MSVM**](msvm-memorysettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="dc374-136">The ideal memory buffer size is configured by using the **TargetMemoryBuffer** property of the [**Msvm\_MemorySettingData**](msvm-memorysettingdata.md) class.</span></span>

<span data-ttu-id="dc374-137">Esta propiedad no es válida para las instancias de la clase **MSVM \_ SummaryInformation** que representan máquinas virtuales para las que la memoria dinámica no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="dc374-137">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent virtual machines for which dynamic memory is not enabled.</span></span>

<span data-ttu-id="dc374-138">Esta propiedad no es válida para las instancias de la clase **MSVM \_ SummaryInformation** que representan una instantánea de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-138">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-139">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="dc374-139">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-140">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dc374-140">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-142">La hora a la que se creó la máquina virtual o la instantánea.</span><span class="sxs-lookup"><span data-stu-id="dc374-142">The time at which the virtual machine or snapshot was created.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="dc374-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc374-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-146">Nombre para mostrar de la máquina virtual o de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="dc374-146">The display name for the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-147">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="dc374-147">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-148">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-150">Estado actual de la máquina virtual o de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="dc374-150">The current state of the virtual machine or snapshot.</span></span> <span data-ttu-id="dc374-151">Vea la propiedad **EnabledState** de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) para ver los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="dc374-151">See the **EnabledState** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-152">**EnhancedSessionModeState**</span><span class="sxs-lookup"><span data-stu-id="dc374-152">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-153">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-155">Indica si el host permite conexiones de modo mejorado y, si se permiten, si están disponibles para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-155">Indicates whether enhanced mode connections are allowed by the host, and if allowed, whether they are available to the virtual machine.</span></span>

<span data-ttu-id="dc374-156">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="dc374-156">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="dc374-157">**Permitido y disponible** (2)</span><span class="sxs-lookup"><span data-stu-id="dc374-157">**Allowed and available** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="dc374-158">**No permitido** (3)</span><span class="sxs-lookup"><span data-stu-id="dc374-158">**Not allowed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="dc374-159">**Permitido pero no disponible** (6)</span><span class="sxs-lookup"><span data-stu-id="dc374-159">**Allowed but not available** (6 )</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc374-160">**GuestOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="dc374-160">**GuestOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc374-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-163">Nombre del sistema operativo invitado, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="dc374-163">The name of the guest operating system, if available.</span></span> <span data-ttu-id="dc374-164">Si esta información no está disponible, el valor de esta propiedad es **null**.</span><span class="sxs-lookup"><span data-stu-id="dc374-164">If this information is not available, the value of this property is **Null**.</span></span> <span data-ttu-id="dc374-165">Esta propiedad no es válida para las instancias de **MSVM \_ SummaryInformation** que representan una instantánea de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-165">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-166">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="dc374-166">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-167">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-169">El estado de mantenimiento actual de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-169">The current health state for the virtual machine.</span></span> <span data-ttu-id="dc374-170">Esta propiedad no es válida para las instancias de **MSVM \_ SummaryInformation** que representan una instantánea de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-170">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-171">**Heartbeat**</span><span class="sxs-lookup"><span data-stu-id="dc374-171">**Heartbeat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-172">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-174">El estado de latido actual de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-174">The current heartbeat status for the virtual machine.</span></span> <span data-ttu-id="dc374-175">Para obtener más información, vea la documentación de la propiedad [**StatusDescriptions**](msvm-heartbeatcomponent.md) de la clase **\_ HeartbeatComponent de MSVM** .</span><span class="sxs-lookup"><span data-stu-id="dc374-175">For more information, see the documentation for the [**StatusDescriptions**](msvm-heartbeatcomponent.md) property of the **Msvm\_HeartbeatComponent** class.</span></span> <span data-ttu-id="dc374-176">Esta propiedad no es válida para las instancias de **MSVM \_ SummaryInformation** que representan una instantánea de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-176">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

<dl> <dt>

<span data-ttu-id="dc374-177"><span id="OK"></span><span id="ok"></span>**Aceptar** (2)</span><span class="sxs-lookup"><span data-stu-id="dc374-177"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dc374-178"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span><span class="sxs-lookup"><span data-stu-id="dc374-178"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span></span>
</dt> <dt>

<span data-ttu-id="dc374-179"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (12)</span><span class="sxs-lookup"><span data-stu-id="dc374-179"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>
</dt> <dt>

<span data-ttu-id="dc374-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (13)</span><span class="sxs-lookup"><span data-stu-id="dc374-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dc374-181">**HostComputerSystemName**</span><span class="sxs-lookup"><span data-stu-id="dc374-181">**HostComputerSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc374-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-184">Nombre del equipo que hospeda esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-184">The name of the computer hosting this virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="dc374-185">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="dc374-185">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="dc374-186">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dc374-186">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc374-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc374-189">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement. InstanceId"), [**clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dc374-189">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dc374-190">InstanceID es una propiedad opcional que se puede usar para identificar de forma opaca y única una instancia de esta clase dentro del ámbito del espacio de nombres de la instancia.</span><span class="sxs-lookup"><span data-stu-id="dc374-190">InstanceID is an optional property that may be used to opaquely and uniquely identify an instance of this class within the scope of the instantiating Namespace.</span></span> <span data-ttu-id="dc374-191">Varias subclases de esta clase pueden invalidar esta propiedad para que sea necesaria, o una clave.</span><span class="sxs-lookup"><span data-stu-id="dc374-191">Various subclasses of this class may override this property to make it required, or a key.</span></span> <span data-ttu-id="dc374-192">Estas subclases también pueden modificar los algoritmos preferidos para garantizar la exclusividad que se definen a continuación.</span><span class="sxs-lookup"><span data-stu-id="dc374-192">Such subclasses may also modify the preferred algorithms for ensuring uniqueness that are defined below.</span></span>

<span data-ttu-id="dc374-193">Para garantizar la unicidad dentro del espacio de nombres, el valor de InstanceID debe construirse con el siguiente algoritmo "preferido":</span><span class="sxs-lookup"><span data-stu-id="dc374-193">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm:</span></span>

<span data-ttu-id="dc374-194"><OrgID>:<LocalID></span><span class="sxs-lookup"><span data-stu-id="dc374-194"><OrgID>:<LocalID></span></span>

<span data-ttu-id="dc374-195">Donde <OrgID> y <LocalID> se separan con dos puntos (:), donde <OrgID> debe incluir un nombre de propiedad intelectual, marca registrada o de otro tipo, que sea propiedad de la entidad empresarial que está creando o definiendo el InstanceID o que es un identificador registrado asignado a la entidad empresarial por una entidad global reconocida.</span><span class="sxs-lookup"><span data-stu-id="dc374-195">Where <OrgID> and <LocalID> are separated by a colon (:), and where <OrgID> must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="dc374-196">(Este requisito es similar al <Schema Name> \_ <Class Name> estructura de los nombres de clase de esquema.) Además, para garantizar la exclusividad, <OrgID> no debe contener un signo de dos puntos (:).</span><span class="sxs-lookup"><span data-stu-id="dc374-196">(This requirement is similar to the <Schema Name>\_<Class Name> structure of Schema class names.) In addition, to ensure uniqueness, <OrgID> must not contain a colon (:).</span></span> <span data-ttu-id="dc374-197">Al utilizar este algoritmo, el primer signo de dos puntos que aparece en InstanceID debe aparecer entre <OrgID> y <LocalID> .</span><span class="sxs-lookup"><span data-stu-id="dc374-197">When using this algorithm, the first colon to appear in InstanceID must appear between <OrgID> and <LocalID>.</span></span>

<span data-ttu-id="dc374-198"><LocalID> la entidad de negocio elige y no se debe reutilizar para identificar distintos elementos subyacentes (del mundo real).</span><span class="sxs-lookup"><span data-stu-id="dc374-198"><LocalID> is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="dc374-199">Si no es NULL y no se usa el algoritmo "preferido" anterior, la entidad de definición debe asegurarse de que el InstanceID resultante no se reutiliza en ningún InstanceIDs generado por este u otros proveedores para el espacio de nombres de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="dc374-199">If not null and the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span>

<span data-ttu-id="dc374-200">Si no se establece en null para las instancias definidas por DMTF, se debe usar el algoritmo "preferido" con el <OrgID> establecido en CIM.</span><span class="sxs-lookup"><span data-stu-id="dc374-200">If not set to null for DMTF-defined instances, the "preferred" algorithm must be used with the <OrgID> set to CIM.</span></span>

> [!Note]  
> <span data-ttu-id="dc374-201">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="dc374-201">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="dc374-202">**IntegrationServicesVersionState**</span><span class="sxs-lookup"><span data-stu-id="dc374-202">**IntegrationServicesVersionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-203">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-205">Indica si los servicios de integración instalados en la máquina virtual están actualizados.</span><span class="sxs-lookup"><span data-stu-id="dc374-205">Indicates whether the integration services installed in the virtual machine are up to date.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc374-206">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="dc374-206">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="UpToDate"></span><span id="uptodate"></span><span id="UPTODATE"></span>

<span data-ttu-id="dc374-207">**UpToDate** (1)</span><span class="sxs-lookup"><span data-stu-id="dc374-207">**UpToDate** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mismatch"></span><span id="mismatch"></span><span id="MISMATCH"></span>

<span data-ttu-id="dc374-208">**No coincide** (2)</span><span class="sxs-lookup"><span data-stu-id="dc374-208">**Mismatch** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc374-209">**MemoryAvailable**</span><span class="sxs-lookup"><span data-stu-id="dc374-209">**MemoryAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-210">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dc374-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-212">El porcentaje de la memoria actual disponible para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-212">The percentage of the current memory available to the virtual machine.</span></span> <span data-ttu-id="dc374-213">Cuando se habilita la memoria dinámica para una máquina virtual, esta propiedad representa la relación entre la memoria disponible de la máquina virtual y la memoria física total asignada a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-213">When dynamic memory is enabled for a virtual machine, this property represents the ratio of available memory of the virtual machine to the total physical memory assigned to the virtual machine.</span></span> <span data-ttu-id="dc374-214">Cuando una máquina virtual no tiene memoria disponible, esta propiedad será negativa y contendrá la proporción de memoria necesaria para la máquina virtual en la memoria física total asignada a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-214">When a virtual machine has no available memory, this property will be negative, and it will contain the ratio of memory needed for the virtual machine to the total physical memory assigned to the virtual machine.</span></span>

<span data-ttu-id="dc374-215">Esta propiedad no es válida para las instancias de la clase **MSVM \_ SummaryInformation** que representan máquinas virtuales para las que la memoria dinámica no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="dc374-215">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent virtual machines for which dynamic memory is not enabled.</span></span>

<span data-ttu-id="dc374-216">Esta propiedad no es válida para las instancias de la clase **MSVM \_ SummaryInformation** que representan una instantánea de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-216">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-217">**MemorySpansPhysicalNumaNodes**</span><span class="sxs-lookup"><span data-stu-id="dc374-217">**MemorySpansPhysicalNumaNodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-218">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dc374-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-220">Indica si la memoria de uno o varios de los nodos de acceso a memoria no uniforme (NUMA) virtual de la máquina virtual abarca varios nodos NUMA físicos del sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="dc374-220">Indicates whether the memory of the one or more of the virtual nonuniform memory access (NUMA) nodes of the virtual machine spans multiple physical NUMA nodes of the hosting computer system.</span></span> <span data-ttu-id="dc374-221">Contiene **true** si la memoria abarca varios nodos Numa físicos o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dc374-221">Contains **True** if the memory spans multiple physical NUMA nodes or **False** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-222">**MemoryUsage**</span><span class="sxs-lookup"><span data-stu-id="dc374-222">**MemoryUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-223">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc374-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-225">El uso de memoria actual, en megabytes, de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-225">The current memory usage, in megabytes, of the virtual machine.</span></span> <span data-ttu-id="dc374-226">Esta propiedad no es válida para las instancias de **MSVM \_ SummaryInformation** que representan una instantánea de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-226">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-227">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="dc374-227">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-228">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc374-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-230">Nombre único de la máquina virtual o de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="dc374-230">The unique name for the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-231">**Notas**</span><span class="sxs-lookup"><span data-stu-id="dc374-231">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-232">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc374-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-234">Notas asociadas a la máquina virtual o a la instantánea.</span><span class="sxs-lookup"><span data-stu-id="dc374-234">The notes associated with the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-235">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="dc374-235">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-236">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-238">El número total de procesadores virtuales asignados a la máquina virtual o a la instantánea.</span><span class="sxs-lookup"><span data-stu-id="dc374-238">The total number of virtual processors allocated to the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-239">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="dc374-239">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-240">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dc374-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc374-242">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="dc374-242">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="dc374-243">Los Estados operativos actuales de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-243">The current operational statuses of the virtual machine.</span></span> <span data-ttu-id="dc374-244">Vea la propiedad **OperationalStatus** de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) para ver los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="dc374-244">See the **OperationalStatus** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-245">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="dc374-245">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-246">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc374-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-248">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="dc374-248">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1.</span></span> <span data-ttu-id="dc374-249">Esta propiedad se establecerá en **null** cuando **EnabledState** sea cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="dc374-249">This property will be set to **Null** when **EnabledState** is any value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-250">**ProcessorLoad**</span><span class="sxs-lookup"><span data-stu-id="dc374-250">**ProcessorLoad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-251">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-253">El uso actual del procesador de la máquina virtual, en porcentaje.</span><span class="sxs-lookup"><span data-stu-id="dc374-253">The current processor usage of the virtual machine, in percentage.</span></span> <span data-ttu-id="dc374-254">Esta propiedad no es válida para las instancias de **MSVM \_ SummaryInformation** que representan una instantánea de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-254">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-255">**ProcessorLoadHistory**</span><span class="sxs-lookup"><span data-stu-id="dc374-255">**ProcessorLoadHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-256">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dc374-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc374-258">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="dc374-258">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="dc374-259">Una matriz de los ejemplos anteriores de 100 del uso del procesador, en porcentaje, para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-259">An array of the previous 100 samples of the processor usage, in percentage, for the virtual machine.</span></span> <span data-ttu-id="dc374-260">Esta propiedad no es válida para las instancias de **MSVM \_ SummaryInformation** que representan una instantánea de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-260">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-261">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="dc374-261">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-262">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc374-264">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**MSVM \_ SummaryInformation**.**ReplicationHealthEx**")</span><span class="sxs-lookup"><span data-stu-id="dc374-264">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm\_SummaryInformation**.**ReplicationHealthEx**")</span></span>
</dt> </dl>

<span data-ttu-id="dc374-265">Mantenimiento de la replicación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-265">The replication health for the virtual machine.</span></span> <span data-ttu-id="dc374-266">Consulte la propiedad **ReplicationHealth** de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) para ver los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="dc374-266">See the **ReplicationHealth** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

> [!Note]  
> <span data-ttu-id="dc374-267">Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use **ReplicationHealthEx**.</span><span class="sxs-lookup"><span data-stu-id="dc374-267">This property is deprecated starting with Windows 8.1; instead, use the **ReplicationHealthEx**.</span></span>

 

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dc374-268">**No aplicable** (0)</span><span class="sxs-lookup"><span data-stu-id="dc374-268">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="dc374-269">**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="dc374-269">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="dc374-270">**ADVERTENCIA** (2)</span><span class="sxs-lookup"><span data-stu-id="dc374-270">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="dc374-271">**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="dc374-271">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc374-272">**ReplicationHealthEx**</span><span class="sxs-lookup"><span data-stu-id="dc374-272">**ReplicationHealthEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-273">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dc374-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc374-275">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="dc374-275">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="dc374-276">La matriz de valores de mantenimiento de la replicación para las distintas relaciones de replicación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-276">The array of replication health values for the various replication relationships of the virtual machine.</span></span> <span data-ttu-id="dc374-277">Vea la propiedad **ReplicationHealth** de la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para ver los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="dc374-277">See the **ReplicationHealth** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class for possible values.</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dc374-278">**No aplicable** (0)</span><span class="sxs-lookup"><span data-stu-id="dc374-278">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="dc374-279">**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="dc374-279">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="dc374-280">**ADVERTENCIA** (2)</span><span class="sxs-lookup"><span data-stu-id="dc374-280">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="dc374-281">**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="dc374-281">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc374-282">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="dc374-282">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-283">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-285">El tipo de replicación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-285">The replication type for the virtual machine.</span></span> <span data-ttu-id="dc374-286">Consulte la propiedad **ReplicationMode** de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) para ver los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="dc374-286">See the **ReplicationMode** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="dc374-287">**Ninguno** (0)</span><span class="sxs-lookup"><span data-stu-id="dc374-287">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="dc374-288">**Principal** (1)</span><span class="sxs-lookup"><span data-stu-id="dc374-288">**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="dc374-289">**Réplica** (2)</span><span class="sxs-lookup"><span data-stu-id="dc374-289">**Replica** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="dc374-290">**Réplica de prueba** (3)</span><span class="sxs-lookup"><span data-stu-id="dc374-290">**Test Replica** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span data-ttu-id="dc374-291">**Réplica extendida** (4)</span><span class="sxs-lookup"><span data-stu-id="dc374-291">**Extended Replica** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc374-292">**ReplicationProviderId**</span><span class="sxs-lookup"><span data-stu-id="dc374-292">**ReplicationProviderId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-293">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="dc374-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dc374-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc374-295">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="dc374-295">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="dc374-296">Para la máquina virtual principal o de réplica extendida, este es el identificador del proveedor de replicación principal.</span><span class="sxs-lookup"><span data-stu-id="dc374-296">For the primary or extended replica virtual machine, this is the primary replication provider ID.</span></span> <span data-ttu-id="dc374-297">En el caso de una máquina virtual de réplica y si está habilitada la replicación extendida, este es el identificador de proveedor para la relación extendida.</span><span class="sxs-lookup"><span data-stu-id="dc374-297">For a replica virtual machine and if extended replication is enabled, this is the provider ID for extended relationship.</span></span>

<span data-ttu-id="dc374-298">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="dc374-298">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-299">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="dc374-299">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-300">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-300">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc374-302">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**MSVM \_ SummaryInformation**.**ReplicationStateEx**")</span><span class="sxs-lookup"><span data-stu-id="dc374-302">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm\_SummaryInformation**.**ReplicationStateEx**")</span></span>
</dt> </dl>

<span data-ttu-id="dc374-303">El estado de replicación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-303">The replication state for the virtual machine.</span></span> <span data-ttu-id="dc374-304">Consulte la propiedad **ReplicationState** de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) para ver los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="dc374-304">See the **ReplicationState** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

> [!Note]  
> <span data-ttu-id="dc374-305">Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use **ReplicationStateEx**.</span><span class="sxs-lookup"><span data-stu-id="dc374-305">This property is deprecated starting with Windows 8.1; instead, use the **ReplicationStateEx**.</span></span>

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dc374-306">**Deshabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="dc374-306">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="dc374-307">**Listo para la replicación** (1)</span><span class="sxs-lookup"><span data-stu-id="dc374-307">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="dc374-308">**Esperando para completar la replicación inicial** (2)</span><span class="sxs-lookup"><span data-stu-id="dc374-308">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="dc374-309">**Replicando** (3)</span><span class="sxs-lookup"><span data-stu-id="dc374-309">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="dc374-310">**Replicación sincronizada completa** (4)</span><span class="sxs-lookup"><span data-stu-id="dc374-310">**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="dc374-311">**Recuperado** (5)</span><span class="sxs-lookup"><span data-stu-id="dc374-311">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="dc374-312">**Confirmado** (6)</span><span class="sxs-lookup"><span data-stu-id="dc374-312">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="dc374-313">**Suspendido** (7)</span><span class="sxs-lookup"><span data-stu-id="dc374-313">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="dc374-314">**Crítico** (8)</span><span class="sxs-lookup"><span data-stu-id="dc374-314">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="dc374-315">**Esperando para iniciar la resincronización** (9)</span><span class="sxs-lookup"><span data-stu-id="dc374-315">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="dc374-316">Volver a **sincronizar** (10)</span><span class="sxs-lookup"><span data-stu-id="dc374-316">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="dc374-317">**Resincronización suspendida** (11)</span><span class="sxs-lookup"><span data-stu-id="dc374-317">**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="dc374-318">**Conmutación por error en curso** (12)</span><span class="sxs-lookup"><span data-stu-id="dc374-318">**Failover in progress** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc374-319">**ReplicationStateEx**</span><span class="sxs-lookup"><span data-stu-id="dc374-319">**ReplicationStateEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-320">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dc374-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc374-322">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="dc374-322">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="dc374-323">La matriz de valores de estado de replicación para las distintas relaciones de replicación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-323">The array of replication state values for the various replication relationships of the virtual machine.</span></span> <span data-ttu-id="dc374-324">Vea la propiedad **ReplicationState** de la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para ver los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="dc374-324">See the **ReplicationState** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class for possible values.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dc374-325"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="dc374-325"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="dc374-326"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Listo para la replicación** (1)</span><span class="sxs-lookup"><span data-stu-id="dc374-326"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="dc374-327"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Esperando para completar la replicación inicial** (2)</span><span class="sxs-lookup"><span data-stu-id="dc374-327"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="dc374-328"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicando** (3)</span><span class="sxs-lookup"><span data-stu-id="dc374-328"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="dc374-329"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replicación sincronizada completa** (4)</span><span class="sxs-lookup"><span data-stu-id="dc374-329"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="dc374-330"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recuperado** (5)</span><span class="sxs-lookup"><span data-stu-id="dc374-330"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="dc374-331"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Confirmado** (6)</span><span class="sxs-lookup"><span data-stu-id="dc374-331"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="dc374-332"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendido** (7)</span><span class="sxs-lookup"><span data-stu-id="dc374-332"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="dc374-333"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (8)</span><span class="sxs-lookup"><span data-stu-id="dc374-333"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="dc374-334"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Esperando para iniciar la resincronización** (9)</span><span class="sxs-lookup"><span data-stu-id="dc374-334"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="dc374-335"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>Volver a **sincronizar** (10)</span><span class="sxs-lookup"><span data-stu-id="dc374-335"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="dc374-336"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resincronización suspendida** (11)</span><span class="sxs-lookup"><span data-stu-id="dc374-336"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="dc374-337"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Conmutación por error en curso** (12)</span><span class="sxs-lookup"><span data-stu-id="dc374-337"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="dc374-338"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Conmutación por recuperación en curso** (13)</span><span class="sxs-lookup"><span data-stu-id="dc374-338"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="dc374-339"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Conmutación por recuperación completada** (14)</span><span class="sxs-lookup"><span data-stu-id="dc374-339"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback complete** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span data-ttu-id="dc374-340"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Actualización de disco en curso** (15)</span><span class="sxs-lookup"><span data-stu-id="dc374-340"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Disk update in progress** (15)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="dc374-341">Agregado en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="dc374-341">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span data-ttu-id="dc374-342"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Actualización de disco crítica** (16)</span><span class="sxs-lookup"><span data-stu-id="dc374-342"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Disk update critical** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="dc374-343">Agregado en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="dc374-343">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc374-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (17)</span><span class="sxs-lookup"><span data-stu-id="dc374-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (17)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="dc374-345">Agregado en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="dc374-345">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="dc374-346"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Reasignar la replicación en curso** (18)</span><span class="sxs-lookup"><span data-stu-id="dc374-346"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose replication in progress** (18)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="dc374-347">Agregado en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="dc374-347">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span data-ttu-id="dc374-348"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Preparado para la replicación de sincronización** (19)</span><span class="sxs-lookup"><span data-stu-id="dc374-348"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Prepared for sync replication** (19)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="dc374-349">Agregado en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="dc374-349">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span data-ttu-id="dc374-350"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Preparado para la replicación inversa de grupo** (20)</span><span class="sxs-lookup"><span data-stu-id="dc374-350"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Prepared for group reverse replication** (20)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="dc374-351">Agregado en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="dc374-351">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span data-ttu-id="dc374-352"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**FireDrill en curso** (21)</span><span class="sxs-lookup"><span data-stu-id="dc374-352"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in progress** (21)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="dc374-353">Agregado en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="dc374-353">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc374-354">**Blindada**</span><span class="sxs-lookup"><span data-stu-id="dc374-354">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-355">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dc374-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-357">Indica si la protección está configurada para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-357">Indicates whether or not shielding is configured for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="dc374-358">Agregado en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="dc374-358">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="dc374-359">**Instantáneas**</span><span class="sxs-lookup"><span data-stu-id="dc374-359">**Snapshots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-360">Tipo de datos: matriz **\_ VirtualSystemSettingData de CIM**</span><span class="sxs-lookup"><span data-stu-id="dc374-360">Data type: **CIM\_VirtualSystemSettingData** array</span></span>
</dt> <dt>

<span data-ttu-id="dc374-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc374-362">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="dc374-362">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="dc374-363">Una matriz de instancias de [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representan las instantáneas de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-363">An array of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instances that represent the snapshots for the virtual machine.</span></span> <span data-ttu-id="dc374-364">Esta propiedad no es válida para las instancias de **MSVM \_ SummaryInformation** que representan una instantánea de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-364">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-365">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="dc374-365">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-366">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="dc374-366">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dc374-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc374-368">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="dc374-368">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="dc374-369">Cadenas que describen los valores correspondientes de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="dc374-369">Strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="dc374-370">Esto corresponde a la propiedad **StatusDescriptions** de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="dc374-370">This corresponds to the **StatusDescriptions** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-371">**SwapFilesInUse**</span><span class="sxs-lookup"><span data-stu-id="dc374-371">**SwapFilesInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-372">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dc374-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-373">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-374">Indica si la paginación de segundo nivel está activa.</span><span class="sxs-lookup"><span data-stu-id="dc374-374">Indicates whether second level paging is active.</span></span> <span data-ttu-id="dc374-375">Contiene **true** si la paginación de segundo nivel está activa o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dc374-375">Contains **True** if second level paging is active or **False** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-376">**TestReplicaSystem**</span><span class="sxs-lookup"><span data-stu-id="dc374-376">**TestReplicaSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-377">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="dc374-377">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-378">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-379">Referencia a una instancia de un equipo de [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual de réplica de prueba de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-379">Reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the test replica virtual machine for the virtual machine.</span></span> <span data-ttu-id="dc374-380">Esta propiedad no es válida para las instancias de **MSVM \_ SummaryInformation** que representan una instantánea de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-380">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-381">**ThumbnailImage**</span><span class="sxs-lookup"><span data-stu-id="dc374-381">**ThumbnailImage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-382">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="dc374-382">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="dc374-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc374-384">Calificadores: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ MSVM SummaryInformation**.**ThumbnailImageWidth**","**MSVM \_ SummaryInformation**.**ThumbnailImageHeight**")</span><span class="sxs-lookup"><span data-stu-id="dc374-384">Qualifiers: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImageWidth**", "**Msvm\_SummaryInformation**.**ThumbnailImageHeight**")</span></span>
</dt> </dl>

<span data-ttu-id="dc374-385">Una matriz que contiene una pequeña imagen en miniatura del escritorio de la máquina virtual o de la instantánea en formato RGB565.</span><span class="sxs-lookup"><span data-stu-id="dc374-385">An array that contains a small, thumbnail-sized image of the desktop for the virtual machine or snapshot in RGB565 format.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-386">**ThumbnailImageHeight**</span><span class="sxs-lookup"><span data-stu-id="dc374-386">**ThumbnailImageHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-387">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc374-389">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**ThumbnailImage**")</span><span class="sxs-lookup"><span data-stu-id="dc374-389">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImage**")</span></span>
</dt> </dl>

<span data-ttu-id="dc374-390">Alto en píxeles de la imagen en la propiedad ThumbnailImage.</span><span class="sxs-lookup"><span data-stu-id="dc374-390">The height in pixels of the image in the ThumbnailImage property.</span></span>

> [!Note]  
> <span data-ttu-id="dc374-391">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="dc374-391">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="dc374-392">**ThumbnailImageWidth**</span><span class="sxs-lookup"><span data-stu-id="dc374-392">**ThumbnailImageWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-393">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc374-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc374-395">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**ThumbnailImage**")</span><span class="sxs-lookup"><span data-stu-id="dc374-395">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImage**")</span></span>
</dt> </dl>

<span data-ttu-id="dc374-396">Ancho en píxeles de la imagen en la propiedad ThumbnailImage.</span><span class="sxs-lookup"><span data-stu-id="dc374-396">The width in pixels of the image in the ThumbnailImage property.</span></span>

> [!Note]  
> <span data-ttu-id="dc374-397">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="dc374-397">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="dc374-398">**Actividad**</span><span class="sxs-lookup"><span data-stu-id="dc374-398">**UpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-399">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc374-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-401">La cantidad de tiempo transcurrido desde que se inició por última vez la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-401">The amount of time since the virtual machine was last booted.</span></span> <span data-ttu-id="dc374-402">Esta propiedad no es válida para las instancias de **MSVM \_ SummaryInformation** que representan una instantánea de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-402">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-403">**Versión**</span><span class="sxs-lookup"><span data-stu-id="dc374-403">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-404">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc374-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-405">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-406">La versión del sistema virtual en un formato de "Major. minor", por ejemplo "2,0".</span><span class="sxs-lookup"><span data-stu-id="dc374-406">The version of the virtual system in a format of "major.minor", for example "2.0".</span></span>

> [!Note]  
> <span data-ttu-id="dc374-407">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="dc374-407">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="dc374-408">**VirtualSwitchNames**</span><span class="sxs-lookup"><span data-stu-id="dc374-408">**VirtualSwitchNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-409">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="dc374-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dc374-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc374-411">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="dc374-411">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="dc374-412">Cadenas que especifican los nombres descriptivos de los conmutadores virtuales a los que está conectada la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-412">Strings that specify the friendly names of the virtual switches the virtual machine is connected to.</span></span>

<span data-ttu-id="dc374-413">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="dc374-413">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="dc374-414">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="dc374-414">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc374-415">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc374-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc374-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc374-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc374-417">Subtipo del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="dc374-417">The subtype of the virtual system.</span></span>

<span data-ttu-id="dc374-418">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="dc374-418">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="dc374-419">**Microsoft: Hyper-V: subtipo: 1** ()</span><span class="sxs-lookup"><span data-stu-id="dc374-419">**Microsoft:Hyper-V:SubType:1** ()</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="dc374-420">**Microsoft: Hyper-V: subtipo: 2** ()</span><span class="sxs-lookup"><span data-stu-id="dc374-420">**Microsoft:Hyper-V:SubType:2** ()</span></span>


<span data-ttu-id="dc374-421"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dc374-421"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="dc374-422">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc374-422">Remarks</span></span>

<span data-ttu-id="dc374-423">El acceso a la clase **MSVM \_ SummaryInformation** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="dc374-423">Access to the **Msvm\_SummaryInformation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dc374-424">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="dc374-424">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc374-425">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc374-425">Requirements</span></span>



| <span data-ttu-id="dc374-426">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc374-426">Requirement</span></span> | <span data-ttu-id="dc374-427">Value</span><span class="sxs-lookup"><span data-stu-id="dc374-427">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc374-428">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc374-428">Minimum supported client</span></span><br/> | <span data-ttu-id="dc374-429">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="dc374-429">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dc374-430">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc374-430">Minimum supported server</span></span><br/> | <span data-ttu-id="dc374-431">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="dc374-431">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dc374-432">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dc374-432">Namespace</span></span><br/>                | <span data-ttu-id="dc374-433">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="dc374-433">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dc374-434">MOF</span><span class="sxs-lookup"><span data-stu-id="dc374-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc374-435"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc374-435"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc374-436">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc374-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc374-437"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc374-437"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dc374-438">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc374-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc374-439">**MSVM \_ SummaryInformationBase**</span><span class="sxs-lookup"><span data-stu-id="dc374-439">**Msvm\_SummaryInformationBase**</span></span>](msvm-summaryinformationbase.md)
</dt> <dt>

[<span data-ttu-id="dc374-440">Clases de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="dc374-440">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

