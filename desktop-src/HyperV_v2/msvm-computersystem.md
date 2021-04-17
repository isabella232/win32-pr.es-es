---
description: Representa un sistema de equipo físico o una máquina virtual.
ms.assetid: 1db9e169-1466-4898-ab95-e9d622fe43cb
title: Msvm_ComputerSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem
- Msvm_ComputerSystem.SetPowerState
- Msvm_ComputerSystem.InstanceID
- Msvm_ComputerSystem.Caption
- Msvm_ComputerSystem.Description
- Msvm_ComputerSystem.ElementName
- Msvm_ComputerSystem.InstallDate
- Msvm_ComputerSystem.OperationalStatus
- Msvm_ComputerSystem.StatusDescriptions
- Msvm_ComputerSystem.Status
- Msvm_ComputerSystem.HealthState
- Msvm_ComputerSystem.CommunicationStatus
- Msvm_ComputerSystem.DetailedStatus
- Msvm_ComputerSystem.OperatingStatus
- Msvm_ComputerSystem.PrimaryStatus
- Msvm_ComputerSystem.EnabledState
- Msvm_ComputerSystem.OtherEnabledState
- Msvm_ComputerSystem.RequestedState
- Msvm_ComputerSystem.EnabledDefault
- Msvm_ComputerSystem.TimeOfLastStateChange
- Msvm_ComputerSystem.AvailableRequestedStates
- Msvm_ComputerSystem.TransitioningToState
- Msvm_ComputerSystem.CreationClassName
- Msvm_ComputerSystem.Name
- Msvm_ComputerSystem.PrimaryOwnerName
- Msvm_ComputerSystem.PrimaryOwnerContact
- Msvm_ComputerSystem.Roles
- Msvm_ComputerSystem.NameFormat
- Msvm_ComputerSystem.OtherIdentifyingInfo
- Msvm_ComputerSystem.IdentifyingDescriptions
- Msvm_ComputerSystem.Dedicated
- Msvm_ComputerSystem.OtherDedicatedDescriptions
- Msvm_ComputerSystem.ResetCapability
- Msvm_ComputerSystem.PowerManagementCapabilities
- Msvm_ComputerSystem.OnTimeInMilliseconds
- Msvm_ComputerSystem.ProcessID
- Msvm_ComputerSystem.TimeOfLastConfigurationChange
- Msvm_ComputerSystem.NumberOfNumaNodes
- Msvm_ComputerSystem.ReplicationState
- Msvm_ComputerSystem.ReplicationHealth
- Msvm_ComputerSystem.ReplicationMode
- Msvm_ComputerSystem.FailedOverReplicationType
- Msvm_ComputerSystem.LastReplicationType
- Msvm_ComputerSystem.LastApplicationConsistentReplicationTime
- Msvm_ComputerSystem.LastReplicationTime
- Msvm_ComputerSystem.LastSuccessfulBackupTime
- Msvm_ComputerSystem.EnhancedSessionModeState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae36179e14b584bad4e68350e27d485cdc10c42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551875"
---
# <a name="msvm_computersystem-class"></a><span data-ttu-id="bfa52-103">MSVM \_ clase ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="bfa52-103">Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="bfa52-104">Representa un sistema de equipo físico o una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-104">Represents a physical computer system or virtual machine.</span></span>

<span data-ttu-id="bfa52-105">Para recuperar información de VMMS, use la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="bfa52-105">To retrieve information for the VMMS, use the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="bfa52-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="bfa52-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa52-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfa52-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 1;
  uint16   PowerManagementCapabilities[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
  uint16   NumberOfNumaNodes;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   ReplicationMode;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  DateTime LastApplicationConsistentReplicationTime;
  DateTime LastReplicationTime;
  DateTime LastSuccessfulBackupTime;
  uint16   EnhancedSessionModeState;
};
```

## <a name="members"></a><span data-ttu-id="bfa52-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="bfa52-108">Members</span></span>

<span data-ttu-id="bfa52-109">La clase **MSVM \_ ComputerSystem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bfa52-109">The **Msvm\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="bfa52-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="bfa52-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="bfa52-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bfa52-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bfa52-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="bfa52-112">Methods</span></span>

<span data-ttu-id="bfa52-113">La **clase \_ ComputerSystem de MSVM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bfa52-113">The **Msvm\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="bfa52-114">Método</span><span class="sxs-lookup"><span data-stu-id="bfa52-114">Method</span></span>                                                                                         | <span data-ttu-id="bfa52-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfa52-115">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bfa52-116">**InjectNonMaskableInterrupt**</span><span class="sxs-lookup"><span data-stu-id="bfa52-116">**InjectNonMaskableInterrupt**</span></span>](injectnonmaskableinterrupt-msvm-computersystem.md)           | <span data-ttu-id="bfa52-117">Inserta una interrupción no enmascarable en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-117">Injects a non-maskable interrupt into the virtual machine.</span></span> <span data-ttu-id="bfa52-118">Este método solo se admite para las instancias de la clase **MSVM \_ ComputerSystem** que representan una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-118">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/> <span data-ttu-id="bfa52-119">**Windows 8.1:** Este método no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="bfa52-119">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                    |
| [<span data-ttu-id="bfa52-120">**RequestReplicationStateChange**</span><span class="sxs-lookup"><span data-stu-id="bfa52-120">**RequestReplicationStateChange**</span></span>](msvm-computersystem-requestreplicationstatechange.md)     | <span data-ttu-id="bfa52-121">Solicita que el estado de replicación de la máquina virtual se cambie al valor especificado.</span><span class="sxs-lookup"><span data-stu-id="bfa52-121">Requests that the replication state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="bfa52-122">Este método solo se admite para las instancias de la clase **MSVM \_ ComputerSystem** que representan una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-122">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="bfa52-123">**RequestReplicationStateChangeEx**</span><span class="sxs-lookup"><span data-stu-id="bfa52-123">**RequestReplicationStateChangeEx**</span></span>](msvm-requestreplicationstatechangeex-computersystem.md) | <span data-ttu-id="bfa52-124">Solicita que el estado de replicación de la máquina virtual se cambie al valor especificado.</span><span class="sxs-lookup"><span data-stu-id="bfa52-124">Requests that the replication state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="bfa52-125">Este método solo se admite para las instancias de la clase **MSVM \_ ComputerSystem** que representan una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-125">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/> <span data-ttu-id="bfa52-126">**Windows 8.1:** Este método no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="bfa52-126">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="bfa52-127">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="bfa52-127">**RequestStateChange**</span></span>](requeststatechange-msvm-computersystem.md)                           | <span data-ttu-id="bfa52-128">Solicita que se cambie el estado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-128">Requests that the state of the virtual machine be changed.</span></span> <span data-ttu-id="bfa52-129">Este método solo se admite para las instancias de la clase **MSVM \_ ComputerSystem** que representan una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-129">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="bfa52-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="bfa52-130">**SetPowerState**</span></span>                                                                              | <span data-ttu-id="bfa52-131">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="bfa52-131">This method is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a><span data-ttu-id="bfa52-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bfa52-132">Properties</span></span>

<span data-ttu-id="bfa52-133">La **clase \_ ComputerSystem de MSVM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bfa52-133">The **Msvm\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bfa52-134">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="bfa52-134">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-135">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-137">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="bfa52-137">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="bfa52-138">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual del objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bfa52-138">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="bfa52-139">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-139">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="bfa52-140">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-140">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="bfa52-141">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bfa52-141">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="bfa52-142"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="bfa52-142"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-143"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="bfa52-143"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-144"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="bfa52-144"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-145"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="bfa52-145"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-146"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="bfa52-146"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-147"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="bfa52-147"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-148"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="bfa52-148"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-149"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="bfa52-149"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-150"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="bfa52-150"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-151"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="bfa52-151"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="bfa52-152">)</span><span class="sxs-lookup"><span data-stu-id="bfa52-152">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bfa52-153">**Caption**</span><span class="sxs-lookup"><span data-stu-id="bfa52-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bfa52-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-156">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="bfa52-156">A short description of the object.</span></span> <span data-ttu-id="bfa52-157">Esta propiedad se hereda de la clase [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) y contendrá uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bfa52-157">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class, and it will contain one of the following values.</span></span>



| <span data-ttu-id="bfa52-158">Value</span><span class="sxs-lookup"><span data-stu-id="bfa52-158">Value</span></span>                                                                                                | <span data-ttu-id="bfa52-159">Significado</span><span class="sxs-lookup"><span data-stu-id="bfa52-159">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="bfa52-160"><dt>"Máquina virtual"</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-160"><dt>"Virtual Machine"</dt></span></span> </dl>         | <span data-ttu-id="bfa52-161">La instancia representa una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-161">The instance represents a virtual machine.</span></span><br/>    |
| <dl> <span data-ttu-id="bfa52-162"><dt>"Sistema del equipo host"</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-162"><dt>"Hosting Computer System"</dt></span></span> </dl> | <span data-ttu-id="bfa52-163">La instancia representa el equipo host.</span><span class="sxs-lookup"><span data-stu-id="bfa52-163">The instance represents the hosting computer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bfa52-164">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="bfa52-164">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-165">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-167">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="bfa52-167">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="bfa52-168">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="bfa52-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bfa52-169">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bfa52-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-170">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bfa52-170">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bfa52-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-173">Nombre de la clase o subclase que se usa en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="bfa52-173">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="bfa52-174">Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre se establece en "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="bfa52-174">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-175">**Dedicado**</span><span class="sxs-lookup"><span data-stu-id="bfa52-175">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-176">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-176">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-178">Indica si el sistema informático es un sistema especial (dedicado a un uso determinado), en lugar de un sistema de uso general.</span><span class="sxs-lookup"><span data-stu-id="bfa52-178">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="bfa52-179">Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en 0 (no dedicado).</span><span class="sxs-lookup"><span data-stu-id="bfa52-179">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-180">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bfa52-180">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bfa52-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-183">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="bfa52-183">A description of the object.</span></span> <span data-ttu-id="bfa52-184">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y contendrá uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bfa52-184">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it will contain one of the following values.</span></span>



| <span data-ttu-id="bfa52-185">Value</span><span class="sxs-lookup"><span data-stu-id="bfa52-185">Value</span></span>                                                                                                          | <span data-ttu-id="bfa52-186">Significado</span><span class="sxs-lookup"><span data-stu-id="bfa52-186">Meaning</span></span>                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="bfa52-187"><dt>"Sistema de equipo virtual de Microsoft"</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-187"><dt>"Microsoft Virtual Computer System"</dt></span></span> </dl> | <span data-ttu-id="bfa52-188">La instancia representa una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-188">The instance represents a virtual machine.</span></span><br/>    |
| <dl> <span data-ttu-id="bfa52-189"><dt>"Sistema de equipo de hospedaje de Microsoft"</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-189"><dt>"Microsoft Hosting Computer System"</dt></span></span> </dl> | <span data-ttu-id="bfa52-190">La instancia representa el equipo host.</span><span class="sxs-lookup"><span data-stu-id="bfa52-190">The instance represents the hosting computer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bfa52-191">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="bfa52-191">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-192">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-194">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="bfa52-194">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="bfa52-195">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="bfa52-195">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bfa52-196">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bfa52-196">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-197">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="bfa52-197">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bfa52-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-200">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="bfa52-200">A display name for the object.</span></span> <span data-ttu-id="bfa52-201">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en el nombre para mostrar del equipo de una máquina virtual o el nombre NetBIOS del sistema operativo de administración.</span><span class="sxs-lookup"><span data-stu-id="bfa52-201">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to the display name of the computer for a virtual machine or the NetBIOS name of the management operating system.</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-202">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="bfa52-202">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-203">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-205">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="bfa52-205">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="bfa52-206">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) y tendrá uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bfa52-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bfa52-207"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="bfa52-207"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-208"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="bfa52-208"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-209"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitada pero sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="bfa52-209"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bfa52-210">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="bfa52-210">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-211">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-213">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="bfa52-213">The enabled and disabled states of an element.</span></span> <span data-ttu-id="bfa52-214">Esta propiedad también puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="bfa52-214">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="bfa52-215">Esta propiedad se hereda de la clase [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) y está establecida en 2 (habilitado) para un equipo físico o uno de los siguientes valores para una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-215">This property is inherited from the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class, and it is set to 2 (Enabled) for a physical computer or one of the following values for a virtual machine.</span></span> <span data-ttu-id="bfa52-216">Para obtener una vista gráfica de estos Estados, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="bfa52-216">For a graphical view of these states, see Remarks.</span></span>



| <span data-ttu-id="bfa52-217">Value</span><span class="sxs-lookup"><span data-stu-id="bfa52-217">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="bfa52-218">Significado</span><span class="sxs-lookup"><span data-stu-id="bfa52-218">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="bfa52-219"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-219"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="bfa52-220">No se pudo determinar el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="bfa52-220">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="bfa52-221"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-221"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="bfa52-222"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-222"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="bfa52-223">El elemento se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="bfa52-223">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="bfa52-224"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-224"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="bfa52-225">El elemento está desactivado.</span><span class="sxs-lookup"><span data-stu-id="bfa52-225">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="bfa52-226"><dt>**Cerrando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-226"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="bfa52-227">El elemento está en el proceso de pasar a un Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="bfa52-227">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="bfa52-228"><dt>**No aplicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-228"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="bfa52-229">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="bfa52-229">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="bfa52-230"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-230"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="bfa52-231">Es posible que el elemento esté completando comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="bfa52-231">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="bfa52-232"><dt>**En la prueba**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-232"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="bfa52-233">El elemento está en un estado de prueba.</span><span class="sxs-lookup"><span data-stu-id="bfa52-233">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="bfa52-234"><dt>**Aplazado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-234"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="bfa52-235">Es posible que el elemento esté completando los comandos, pero pondrá en cola todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="bfa52-235">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="bfa52-236">Modo <dt>**inactivo**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-236"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="bfa52-237">El elemento está habilitado pero en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="bfa52-237">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="bfa52-238">El comportamiento del elemento es similar al estado habilitado (2), pero solo procesa un conjunto restringido de comandos.</span><span class="sxs-lookup"><span data-stu-id="bfa52-238">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="bfa52-239">Todas las demás solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="bfa52-239">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="bfa52-240"><dt>**Inicio**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-240"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="bfa52-241">El elemento está en proceso de pasar a un estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="bfa52-241">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="bfa52-242">Las nuevas solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="bfa52-242">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="bfa52-243">**EnhancedSessionModeState**</span><span class="sxs-lookup"><span data-stu-id="bfa52-243">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-244">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-246">Especifica el estado actual del modo de sesión mejorada en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-246">Specifies the current state of enhanced session mode on the virtual machine.</span></span>

<span data-ttu-id="bfa52-247">El proveedor WMI de Hyper-V genera una [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) cada vez que cambia el **EnhancedSessionModeState** de la clase **MSVM \_ ComputerSystem** .</span><span class="sxs-lookup"><span data-stu-id="bfa52-247">The Hyper-V WMI provider raises an [**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) each time the **EnhancedSessionModeState** of the **Msvm\_ComputerSystem** class changes.</span></span> <span data-ttu-id="bfa52-248">Si una sesión de vmconnection activa recibe un **\_ \_ InstanceModificationEvent**, intenta cambiar al modo de sesión mejorada si el usuario habilita esa configuración.</span><span class="sxs-lookup"><span data-stu-id="bfa52-248">If an active vmconnection session receives an **\_\_InstanceModificationEvent**, it attempts to switch to enhanced session mode if the user enabled that setting.</span></span>

<span data-ttu-id="bfa52-249">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="bfa52-249">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<span data-ttu-id="bfa52-250">**EnhancedSessionModeState** puede tener uno de estos valores:</span><span class="sxs-lookup"><span data-stu-id="bfa52-250">**EnhancedSessionModeState** can be one of these values:</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="bfa52-251"><span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Permitido y disponible** (2)</span><span class="sxs-lookup"><span data-stu-id="bfa52-251"><span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Allowed and available** (2)</span></span>


</dt> <dd>

<span data-ttu-id="bfa52-252">Se permite el modo mejorado y está disponible en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-252">Enhanced mode is allowed and available on the virtual machine.</span></span>

</dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="bfa52-253"><span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**No permitido** (3)</span><span class="sxs-lookup"><span data-stu-id="bfa52-253"><span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Not allowed** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bfa52-254">El modo mejorado no se permite en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-254">Enhanced mode is not allowed on the virtual machine.</span></span>

</dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="bfa52-255"><span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Permitido pero no disponible** (6)</span><span class="sxs-lookup"><span data-stu-id="bfa52-255"><span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Allowed but not available** (6)</span></span>


</dt> <dd>

<span data-ttu-id="bfa52-256">Se permite el modo mejorado, pero no está disponible actualmente en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-256">Enhanced mode is allowed and but not currently available on the virtual machine.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bfa52-257">**FailedOverReplicationType**</span><span class="sxs-lookup"><span data-stu-id="bfa52-257">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-258">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-260">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")</span><span class="sxs-lookup"><span data-stu-id="bfa52-260">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-261">El tipo de punto de datos de recuperación que se aplicó durante la operación de conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="bfa52-261">The type of recovery data point that was applied during the failover operation.</span></span>

> [!Note]  
> <span data-ttu-id="bfa52-262">Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.</span><span class="sxs-lookup"><span data-stu-id="bfa52-262">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="bfa52-263">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="bfa52-263">Possible values are:</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="bfa52-264">**Ninguno** (0)</span><span class="sxs-lookup"><span data-stu-id="bfa52-264">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="bfa52-265">**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="bfa52-265">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="bfa52-266">**Coherente** con la aplicación (2)</span><span class="sxs-lookup"><span data-stu-id="bfa52-266">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="bfa52-267">**Planeada** (3)</span><span class="sxs-lookup"><span data-stu-id="bfa52-267">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bfa52-268">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="bfa52-268">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-269">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-271">Especifica el estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="bfa52-271">Specifies the current health of the element.</span></span> <span data-ttu-id="bfa52-272">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="bfa52-272">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="bfa52-273">Cuando se produzca un error crítico, compruebe el registro de eventos para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="bfa52-273">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="bfa52-274">La propiedad **EnabledState** también puede contener más información.</span><span class="sxs-lookup"><span data-stu-id="bfa52-274">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="bfa52-275">Por ejemplo, si el espacio en disco es muy bajo, **HealthState** se establece en 25, la máquina virtual se pausa y **EnabledState** se establece en 32768 (en pausa).</span><span class="sxs-lookup"><span data-stu-id="bfa52-275">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="bfa52-276">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bfa52-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="bfa52-277">Value</span><span class="sxs-lookup"><span data-stu-id="bfa52-277">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="bfa52-278">Significado</span><span class="sxs-lookup"><span data-stu-id="bfa52-278">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="bfa52-279"><dt>**Aceptar**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-279"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="bfa52-280">La máquina virtual es totalmente funcional y funciona en parámetros operativos normales y sin errores.</span><span class="sxs-lookup"><span data-stu-id="bfa52-280">The virtual machine is fully functional and is operating within normal operational parameters and without error.</span></span><br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="bfa52-281"><dt>**Error principal**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-281"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="bfa52-282">Se produjo un error importante en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-282">The virtual machine has suffered a major failure.</span></span> <span data-ttu-id="bfa52-283">Este valor se usa cuando uno o varios discos que contienen los VHD de la máquina virtual tienen poco espacio en disco y la máquina virtual se ha puesto en pausa.</span><span class="sxs-lookup"><span data-stu-id="bfa52-283">This value is used when one or more disks that contain the virtual machine's VHDs is low on disk space and the virtual machine has been paused.</span></span><br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="bfa52-284"><dt>**Error crítico**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-284"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="bfa52-285">El elemento no es funcional y es posible que la recuperación no sea posible.</span><span class="sxs-lookup"><span data-stu-id="bfa52-285">The element is nonfunctional, and recovery might not be possible.</span></span> <span data-ttu-id="bfa52-286">Esto puede indicar que el proceso de trabajo de la máquina virtual (Vmwp.exe) no responde a las solicitudes de control o información, o que uno o varios discos que contienen los discos duros virtuales de la máquina virtual tienen poco espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="bfa52-286">This can indicate that the worker process for the virtual machine (Vmwp.exe) is not responding to control or information requests, or that one or more disks that contain the VHDs for the virtual machine are low on disk space.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bfa52-287">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bfa52-287">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-288">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="bfa52-288">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-290">Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="bfa52-290">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-291">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bfa52-291">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-292">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bfa52-292">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-294">Fecha y hora en que se creó la configuración de la máquina virtual para una máquina virtual, o **null**, para un sistema operativo de administración.</span><span class="sxs-lookup"><span data-stu-id="bfa52-294">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="bfa52-295">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bfa52-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-296">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bfa52-296">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-297">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bfa52-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-299">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="bfa52-299">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-300">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="bfa52-300">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="bfa52-301">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bfa52-301">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="bfa52-302">En Windows 8, hay una única instancia de [**ReplicationSettingData**](msvm-replicationsettingdata.md) para cada sistema de equipo o máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-302">In Windows 8, there is a single instance of [**ReplicationSettingData**](msvm-replicationsettingdata.md) for every computer system or virtual machine.</span></span> <span data-ttu-id="bfa52-303">Por Windows 8.1, una máquina virtual de recuperación tiene dos instancias de **ReplicationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="bfa52-303">For Windows 8.1, a recovery virtual machine has two instances of **ReplicationSettingData**.</span></span> <span data-ttu-id="bfa52-304">Este cambio distingue y asocia los datos de configuración con la relación de replicación.</span><span class="sxs-lookup"><span data-stu-id="bfa52-304">This change differentiates and associates setting data with replication relationship.</span></span>



| <span data-ttu-id="bfa52-305">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="bfa52-305">Property name</span></span>  | <span data-ttu-id="bfa52-306">Valor de Windows 8</span><span class="sxs-lookup"><span data-stu-id="bfa52-306">Windows 8 value</span></span>               | <span data-ttu-id="bfa52-307">Windows 8.1 valor</span><span class="sxs-lookup"><span data-stu-id="bfa52-307">Windows 8.1 value</span></span>                          |
|----------------|-------------------------------|--------------------------------------------|
| <span data-ttu-id="bfa52-308">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bfa52-308">**InstanceID**</span></span> | <span data-ttu-id="bfa52-309">Microsoft: <vmguid> \\ HVR</span><span class="sxs-lookup"><span data-stu-id="bfa52-309">Microsoft:<vmguid>\\HVR</span></span> | <span data-ttu-id="bfa52-310">Microsoft: <vmguid> \\ HVR \\<0/1></span><span class="sxs-lookup"><span data-stu-id="bfa52-310">Microsoft:<vmguid>\\HVR\\<0/1></span></span> |



 

<span data-ttu-id="bfa52-311">En el valor Windows 8.1, 0 indica principal y 1 indica replicación extendida.</span><span class="sxs-lookup"><span data-stu-id="bfa52-311">In the Windows 8.1 value, 0 indicates primary and 1 indicates extended replication.</span></span> <span data-ttu-id="bfa52-312">Para obtener más información acerca de la replicación extendida, consulte [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).</span><span class="sxs-lookup"><span data-stu-id="bfa52-312">For more info about extended replication, see [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-313">**LastApplicationConsistentReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="bfa52-313">**LastApplicationConsistentReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-314">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bfa52-314">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-316">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")</span><span class="sxs-lookup"><span data-stu-id="bfa52-316">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-317">La hora a la que se recibió la última replicación coherente con la aplicación para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-317">The time at which the last application-consistent replication was received for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="bfa52-318">Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.</span><span class="sxs-lookup"><span data-stu-id="bfa52-318">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

</dd> <dt>

<span data-ttu-id="bfa52-319">**LastReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="bfa52-319">**LastReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-320">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bfa52-320">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-322">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")</span><span class="sxs-lookup"><span data-stu-id="bfa52-322">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-323">La hora a la que se recibió la última replicación durante la recuperación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-323">The time at which the last replication is received on recovery for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="bfa52-324">Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.</span><span class="sxs-lookup"><span data-stu-id="bfa52-324">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

</dd> <dt>

<span data-ttu-id="bfa52-325">**LastReplicationType**</span><span class="sxs-lookup"><span data-stu-id="bfa52-325">**LastReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-326">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-328">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")</span><span class="sxs-lookup"><span data-stu-id="bfa52-328">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-329">El tipo de la última replicación que se recibió para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-329">The type of the last replication that was received for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="bfa52-330">Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.</span><span class="sxs-lookup"><span data-stu-id="bfa52-330">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="bfa52-331">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="bfa52-331">Possible values are:</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="bfa52-332">**Ninguno** (0)</span><span class="sxs-lookup"><span data-stu-id="bfa52-332">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="bfa52-333">**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="bfa52-333">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="bfa52-334">**Coherente** con la aplicación (2)</span><span class="sxs-lookup"><span data-stu-id="bfa52-334">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="bfa52-335">**Planeada** (3)</span><span class="sxs-lookup"><span data-stu-id="bfa52-335">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bfa52-336">**LastSuccessfulBackupTime**</span><span class="sxs-lookup"><span data-stu-id="bfa52-336">**LastSuccessfulBackupTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-337">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bfa52-337">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-339">La hora a la que se completó la última copia de seguridad correcta de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-339">The time at which the last successful backup has completed for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-340">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="bfa52-340">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-341">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bfa52-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-343">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="bfa52-343">The label by which the object is known.</span></span> <span data-ttu-id="bfa52-344">Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre está establecida en "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="bfa52-344">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-345">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="bfa52-345">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-346">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bfa52-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-348">Cadena que identifica el modo en que se generó el nombre del sistema mediante la heurística de subclases.</span><span class="sxs-lookup"><span data-stu-id="bfa52-348">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="bfa52-349">Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="bfa52-349">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-350">**NumberOfNumaNodes**</span><span class="sxs-lookup"><span data-stu-id="bfa52-350">**NumberOfNumaNodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-351">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-352">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-353">El número de nodos de acceso a memoria no uniforme (NUMA) del equipo.</span><span class="sxs-lookup"><span data-stu-id="bfa52-353">The number of nonuniform memory access (NUMA) nodes of the computer system.</span></span> <span data-ttu-id="bfa52-354">Cuando **MSVM \_ ComputerSystem** representa el sistema del equipo host, esta propiedad contiene el recuento de nodos Numa físicos.</span><span class="sxs-lookup"><span data-stu-id="bfa52-354">When **Msvm\_ComputerSystem** represents the hosting computer system, this property contains the count of physical NUMA nodes.</span></span> <span data-ttu-id="bfa52-355">Cuando **MSVM \_ ComputerSystem** representa una máquina virtual, esta propiedad contiene el número de nodos Numa virtuales que se presentan al sistema operativo invitado a través de la tabla de afinidad de recursos del sistema ACPI (SRAT).</span><span class="sxs-lookup"><span data-stu-id="bfa52-355">When **Msvm\_ComputerSystem** represents a virtual machine, this property contains the number of virtual NUMA nodes that are presented to the guest operating system through the ACPI System Resource Affinity Table (SRAT).</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-356">**OnTimeInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="bfa52-356">**OnTimeInMilliseconds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-357">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bfa52-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-359">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos")</span><span class="sxs-lookup"><span data-stu-id="bfa52-359">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-360">Para la máquina virtual, esta propiedad indica el tiempo, en milisegundos, desde la última vez que se activó, restableció o restauró el equipo.</span><span class="sxs-lookup"><span data-stu-id="bfa52-360">For the virtual machine, this property indicates the time, in milliseconds, since the machine was last turned on, reset, or restored.</span></span> <span data-ttu-id="bfa52-361">Esta vez excluye la hora en que la máquina virtual estaba en estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="bfa52-361">This time excludes the time the virtual machine was in the paused state.</span></span> <span data-ttu-id="bfa52-362">En el sistema operativo de administración, esta propiedad se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="bfa52-362">For the management operating system, this property is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-363">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="bfa52-363">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-364">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-366">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="bfa52-366">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="bfa52-367">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="bfa52-367">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bfa52-368">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bfa52-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="bfa52-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-370">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-372">Una matriz que contiene los Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="bfa52-372">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="bfa52-373">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bfa52-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="bfa52-374">El valor en el índice cero (0) es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bfa52-374">The value at index zero (0) is one of the following values.</span></span>



| <span data-ttu-id="bfa52-375">Value</span><span class="sxs-lookup"><span data-stu-id="bfa52-375">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="bfa52-376">Significado</span><span class="sxs-lookup"><span data-stu-id="bfa52-376">Meaning</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="bfa52-377"><dt>**Aceptar**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-377"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                      | <span data-ttu-id="bfa52-378">La máquina virtual es funcional y funciona con normalidad.</span><span class="sxs-lookup"><span data-stu-id="bfa52-378">The virtual machine is functional and operating normally.</span></span><br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="bfa52-379"><dt>**Degradado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-379"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                         | <span data-ttu-id="bfa52-380">La máquina virtual solo es parcialmente funcional.</span><span class="sxs-lookup"><span data-stu-id="bfa52-380">The virtual machine is only partially functional.</span></span> <span data-ttu-id="bfa52-381">Esto indica que no se puede tener acceso al almacenamiento que contiene la configuración.</span><span class="sxs-lookup"><span data-stu-id="bfa52-381">This indicates that the storage that contains the configuration is not accessible.</span></span> <span data-ttu-id="bfa52-382">Una máquina virtual en este estado solo se puede desactivar o eliminar.</span><span class="sxs-lookup"><span data-stu-id="bfa52-382">A virtual machine in this state can only be turned off or deleted.</span></span> <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <span data-ttu-id="bfa52-383"><dt>**Error predictivo**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-383"><dt>**Predictive Failure**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="bfa52-384">La máquina virtual es funcional, pero puede producir un error en el futuro.</span><span class="sxs-lookup"><span data-stu-id="bfa52-384">The virtual machine is functional but may fail in the future.</span></span> <span data-ttu-id="bfa52-385">Esto indica que el almacenamiento que contiene el disco duro virtual de la máquina virtual tiene poco espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="bfa52-385">This indicates that the storage that contains the virtual machine's virtual hard disk is low on free space.</span></span> <span data-ttu-id="bfa52-386">La máquina virtual se pausará si no hay más espacio disponible en disco.</span><span class="sxs-lookup"><span data-stu-id="bfa52-386">The virtual machine will be paused if more disk space is not made available.</span></span><br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <span data-ttu-id="bfa52-387"><dt>**Detenido**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-387"><dt>**Stopped**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="bfa52-388">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="bfa52-388">This value is not supported.</span></span> <span data-ttu-id="bfa52-389">Si se detiene la máquina virtual, la propiedad **EnabledState** tendrá un valor de 3 (deshabilitado).</span><span class="sxs-lookup"><span data-stu-id="bfa52-389">If the virtual machine is stopped, the **EnabledState** property will have a value of 3 (Disabled).</span></span><br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <span data-ttu-id="bfa52-390"><dt>**En el servicio**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-390"><dt>**In Service**</dt> <dt>11</dt></span></span> </dl>                                | <span data-ttu-id="bfa52-391">La máquina virtual está procesando una solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfa52-391">The virtual machine is processing a request.</span></span><br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <span data-ttu-id="bfa52-392"><dt>**Inactivo**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-392"><dt>**Dormant**</dt> <dt>15</dt></span></span> </dl>                                            | <span data-ttu-id="bfa52-393">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="bfa52-393">This value is not supported.</span></span> <span data-ttu-id="bfa52-394">Si la máquina virtual está suspendida o en pausa, la propiedad **EnabledState** tendrá un valor de 32769 (suspendido) o 32768 (en pausa).</span><span class="sxs-lookup"><span data-stu-id="bfa52-394">If the virtual machine is suspended or paused, the **EnabledState** property will have a value of 32769 (Suspended) or 32768 (Paused).</span></span><br/>                                                                                    |



 

<span data-ttu-id="bfa52-395">El valor en el índice uno (1) es opcional y contiene información de estado secundaria.</span><span class="sxs-lookup"><span data-stu-id="bfa52-395">The value at index one (1) is optional and contains secondary status information.</span></span> <span data-ttu-id="bfa52-396">Un cliente debe usar el estado principal del índice cero (0) para determinar si se puede emitir una nueva solicitud a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-396">A client should use the primary status from index zero (0) to determine whether a new request can be issued to the virtual machine.</span></span> <span data-ttu-id="bfa52-397">Si **OperationalStatus** \[ 0 \] es 2 (OK),  \[ \] se puede interrumpir la operación indicada por OperationalStatus 1.</span><span class="sxs-lookup"><span data-stu-id="bfa52-397">If **OperationalStatus**\[0\] is 2 (OK), then the operation indicated by **OperationalStatus**\[1\] can be interrupted.</span></span>

<span data-ttu-id="bfa52-398">El valor de **OperationalStatus** \[ 1 \] es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bfa52-398">The value at **OperationalStatus**\[1\] is one of the following values.</span></span>



| <span data-ttu-id="bfa52-399">Value</span><span class="sxs-lookup"><span data-stu-id="bfa52-399">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="bfa52-400">Significado</span><span class="sxs-lookup"><span data-stu-id="bfa52-400">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <span data-ttu-id="bfa52-401"><dt>**Creando instantánea**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-401"><dt>**Creating Snapshot**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="bfa52-402">Se está creando una instantánea en el proceso de creación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-402">A snapshot is in the process of being created for the virtual machine.</span></span><br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <span data-ttu-id="bfa52-403"><dt>**Aplicando la instantánea**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-403"><dt>**Applying Snapshot**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="bfa52-404">Una instantánea está en proceso de aplicarse a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-404">A snapshot is in the process of being applied to the virtual machine.</span></span><br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <span data-ttu-id="bfa52-405"><dt>**Eliminando instantánea**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-405"><dt>**Deleting Snapshot**</dt> <dt>32770</dt></span></span> </dl>                                 | <span data-ttu-id="bfa52-406">Se está eliminando una instantánea de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-406">A snapshot is in the process of being deleted from the virtual machine.</span></span><br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <span data-ttu-id="bfa52-407"><dt>**Esperando a iniciar**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-407"><dt>**Waiting to Start**</dt> <dt>32771</dt></span></span> </dl>                                     | <span data-ttu-id="bfa52-408">La máquina virtual se iniciará después de que haya transcurrido el retraso de inicio automático.</span><span class="sxs-lookup"><span data-stu-id="bfa52-408">The virtual machine will be started after the automatic startup delay has elapsed.</span></span><br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <span data-ttu-id="bfa52-409"><dt>**Combinación de discos**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-409"><dt>**Merging Disks**</dt> <dt>32772</dt></span></span> </dl>                                                 | <span data-ttu-id="bfa52-410">Se están combinando los discos duros virtuales de las instantáneas eliminadas previamente.</span><span class="sxs-lookup"><span data-stu-id="bfa52-410">Virtual hard disks from previously deleted snapshots are being merged.</span></span><br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="bfa52-411"><dt>**Exportando Máquina Virtual**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-411"><dt>**Exporting Virtual Machine**</dt> <dt>32773</dt></span></span> </dl> | <span data-ttu-id="bfa52-412">La máquina virtual se está exportando.</span><span class="sxs-lookup"><span data-stu-id="bfa52-412">The virtual machine is being exported.</span></span><br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="bfa52-413"><dt>**Migrando la máquina Virtual**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-413"><dt>**Migrating Virtual Machine**</dt> <dt>32774</dt></span></span> </dl> | <span data-ttu-id="bfa52-414">La máquina virtual se está migrando en directo desde un equipo físico a otro.</span><span class="sxs-lookup"><span data-stu-id="bfa52-414">The virtual machine is being migrated live from one physical computer to another.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="bfa52-415">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bfa52-415">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-416">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="bfa52-416">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-417">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-418">Una cadena que describe cómo o por qué el sistema está dedicado cuando la matriz **dedicada** incluye el valor 2 (otro).</span><span class="sxs-lookup"><span data-stu-id="bfa52-418">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="bfa52-419">Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="bfa52-419">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-420">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="bfa52-420">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-421">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bfa52-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-423">El estado habilitado o deshabilitado de la máquina virtual cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="bfa52-423">The enabled or disabled state of the virtual machine when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="bfa52-424">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="bfa52-424">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="bfa52-425">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="bfa52-425">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-426">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="bfa52-426">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-427">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="bfa52-427">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-428">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-429">Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="bfa52-429">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bfa52-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-431">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-432">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-433">Esta propiedad se hereda de [**un \_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="bfa52-433">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-434">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="bfa52-434">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-435">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bfa52-435">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-436">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-437">Cadena que indica cómo se puede alcanzar el propietario del sistema principal (por ejemplo, un número de teléfono o una dirección de correo electrónico).</span><span class="sxs-lookup"><span data-stu-id="bfa52-437">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="bfa52-438">Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="bfa52-438">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-439">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="bfa52-439">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-440">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bfa52-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-441">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-442">Nombre del propietario del sistema principal.</span><span class="sxs-lookup"><span data-stu-id="bfa52-442">The name of the primary system owner.</span></span> <span data-ttu-id="bfa52-443">Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="bfa52-443">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-444">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="bfa52-444">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-445">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-445">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-446">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-447">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="bfa52-447">Provides high level status information.</span></span> <span data-ttu-id="bfa52-448">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="bfa52-448">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="bfa52-449">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="bfa52-449">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="bfa52-450">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bfa52-450">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-451">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="bfa52-451">**ProcessID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-452">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bfa52-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-453">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-454">El identificador del proceso en el que se está ejecutando esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-454">The identifier of the process under which this virtual machine is running.</span></span> <span data-ttu-id="bfa52-455">Este valor se puede usar para identificar de forma única la instancia de Vmwp.exe en el sistema que ejecuta la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-455">This value can be used to uniquely identify the instance of Vmwp.exe on the system that is running the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-456">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="bfa52-456">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-457">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-457">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-458">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-459">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")</span><span class="sxs-lookup"><span data-stu-id="bfa52-459">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-460">Mantenimiento de la replicación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-460">The replication health for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="bfa52-461">Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.</span><span class="sxs-lookup"><span data-stu-id="bfa52-461">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="bfa52-462">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="bfa52-462">Possible values are:</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="bfa52-463">**No aplicable** (0)</span><span class="sxs-lookup"><span data-stu-id="bfa52-463">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="bfa52-464">**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="bfa52-464">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="bfa52-465">**ADVERTENCIA** (2)</span><span class="sxs-lookup"><span data-stu-id="bfa52-465">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="bfa52-466">**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="bfa52-466">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bfa52-467">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="bfa52-467">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-468">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-468">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-469">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-470">Especifica el modo de replicación para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-470">Specifies the replication mode for the virtual machine.</span></span> <span data-ttu-id="bfa52-471">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="bfa52-471">This will be one of the following values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="bfa52-472"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno** (0)</span><span class="sxs-lookup"><span data-stu-id="bfa52-472"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="bfa52-473"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Principal** (1)</span><span class="sxs-lookup"><span data-stu-id="bfa52-473"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="bfa52-474"><span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Réplica** (2)</span><span class="sxs-lookup"><span data-stu-id="bfa52-474"><span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Replica** (2)</span></span>


</dt> <dd>

<span data-ttu-id="bfa52-475">Recuperación</span><span class="sxs-lookup"><span data-stu-id="bfa52-475">Recovery</span></span>

</dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="bfa52-476"><span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Réplica de prueba** (3)</span><span class="sxs-lookup"><span data-stu-id="bfa52-476"><span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Test Replica** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bfa52-477">Réplica</span><span class="sxs-lookup"><span data-stu-id="bfa52-477">Replica</span></span>

</dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span data-ttu-id="bfa52-478"><span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Réplica extendida** (4)</span><span class="sxs-lookup"><span data-stu-id="bfa52-478"><span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Extended Replica** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bfa52-479">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="bfa52-479">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-480">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-481">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-482">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**")</span><span class="sxs-lookup"><span data-stu-id="bfa52-482">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**")</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-483">El estado de replicación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-483">The replication state for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="bfa52-484">Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.</span><span class="sxs-lookup"><span data-stu-id="bfa52-484">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="bfa52-485">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="bfa52-485">Possible values are:</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bfa52-486">**Deshabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="bfa52-486">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="bfa52-487">**Listo para la replicación** (1)</span><span class="sxs-lookup"><span data-stu-id="bfa52-487">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="bfa52-488">**Esperando para completar la replicación inicial** (2)</span><span class="sxs-lookup"><span data-stu-id="bfa52-488">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="bfa52-489">**Replicando** (3)</span><span class="sxs-lookup"><span data-stu-id="bfa52-489">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="bfa52-490">**Replicación sincronizada completa** (4)</span><span class="sxs-lookup"><span data-stu-id="bfa52-490">**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="bfa52-491">**Recuperado** (5)</span><span class="sxs-lookup"><span data-stu-id="bfa52-491">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="bfa52-492">**Confirmado** (6)</span><span class="sxs-lookup"><span data-stu-id="bfa52-492">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="bfa52-493">**Suspendido** (7)</span><span class="sxs-lookup"><span data-stu-id="bfa52-493">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="bfa52-494">**Crítico** (8)</span><span class="sxs-lookup"><span data-stu-id="bfa52-494">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="bfa52-495">**Esperando para iniciar la resincronización** (9)</span><span class="sxs-lookup"><span data-stu-id="bfa52-495">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="bfa52-496">Volver a **sincronizar** (10)</span><span class="sxs-lookup"><span data-stu-id="bfa52-496">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="bfa52-497">**Resincronización suspendida** (11)</span><span class="sxs-lookup"><span data-stu-id="bfa52-497">**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="bfa52-498">**Conmutación por error en curso** (12)</span><span class="sxs-lookup"><span data-stu-id="bfa52-498">**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="bfa52-499">**Conmutación por recuperación en curso** (13)</span><span class="sxs-lookup"><span data-stu-id="bfa52-499">**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="bfa52-500">**Conmutación por recuperación completada** (14)</span><span class="sxs-lookup"><span data-stu-id="bfa52-500">**Failback complete** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bfa52-501">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="bfa52-501">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-502">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-502">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-503">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-504">Último estado solicitado o deseado de la máquina virtual tal como se pasó al método [**RequestStateChange**](requeststatechange-msvm-computersystem.md) , o 12 (no aplicable) si no hay ningún cambio de estado en curso.</span><span class="sxs-lookup"><span data-stu-id="bfa52-504">The last requested or desired state for the virtual machine as passed to the [**RequestStateChange**](requeststatechange-msvm-computersystem.md) method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="bfa52-505">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="bfa52-505">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="bfa52-506">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="bfa52-506">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="bfa52-507">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bfa52-507">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-508">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="bfa52-508">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-509">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-509">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-510">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-511">Esta propiedad se hereda de [**un \_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="bfa52-511">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-512">**Roles**</span><span class="sxs-lookup"><span data-stu-id="bfa52-512">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-513">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="bfa52-513">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-514">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-515">Matriz de cadenas que describen los roles que el sistema desempeña en el entorno de tecnología de la información.</span><span class="sxs-lookup"><span data-stu-id="bfa52-515">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="bfa52-516">Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="bfa52-516">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-517">**Estado**</span><span class="sxs-lookup"><span data-stu-id="bfa52-517">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-518">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bfa52-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-519">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-520">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="bfa52-520">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-521">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bfa52-521">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-522">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="bfa52-522">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-523">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-524">Calificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="bfa52-524">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-525">Una matriz que contiene cadenas que describen los valores correspondientes de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="bfa52-525">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="bfa52-526">Por ejemplo, si 11 (en servicio) es el valor asignado a **OperationalStatus** \[ 0 \] , **StatusDescriptions** \[ 0 \] puede incluir una explicación sobre el motivo por el que la máquina virtual está procesando una solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfa52-526">For example, if 11 (In Service) is the value assigned to **OperationalStatus**\[0\], then **StatusDescriptions**\[0\] may contain an explanation as to why the virtual machine is processing a request.</span></span> <span data-ttu-id="bfa52-527">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="bfa52-527">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-528">**TimeOfLastConfigurationChange**</span><span class="sxs-lookup"><span data-stu-id="bfa52-528">**TimeOfLastConfigurationChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-529">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bfa52-529">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-530">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-531">Fecha y hora en que se modificó por última vez el archivo de configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-531">The date and time when the virtual machine configuration file was last modified.</span></span> <span data-ttu-id="bfa52-532">El archivo de configuración se modifica durante ciertas operaciones de máquina virtual, así como cuando se agrega, modifica o quita cualquiera de las configuraciones de dispositivo o máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-532">The configuration file is modified during certain virtual machine operations, as well as when any of the virtual machine or device settings are added, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-533">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="bfa52-533">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-534">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bfa52-534">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-535">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-536">Fecha y hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="bfa52-536">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="bfa52-537">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bfa52-537">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bfa52-538">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="bfa52-538">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfa52-539">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bfa52-539">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bfa52-540">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfa52-540">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfa52-541">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="bfa52-541">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="bfa52-542">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="bfa52-542">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfa52-543">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfa52-543">Remarks</span></span>

<span data-ttu-id="bfa52-544">En la ilustración siguiente se muestran los valores **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="bfa52-544">The following illustration shows the **EnabledState** values.</span></span>

![diagrama de estado de los valores enabledstate para Windows Server 2008 R2](images/msvm-computersystem-enabledstate-win2008r2.png)

<span data-ttu-id="bfa52-546">Cuando cambia una propiedad de la clase **MSVM \_ ComputerSystem** , el proveedor WMI indica un evento [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) que describe los cambios.</span><span class="sxs-lookup"><span data-stu-id="bfa52-546">When a property of the **Msvm\_ComputerSystem** class changes, the WMI provider indicates an [**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) event that describes the changes.</span></span> <span data-ttu-id="bfa52-547">El estado anterior se encuentra en la propiedad **PreviousInstance** y el nuevo estado se incluye en la propiedad **TargetInstance** .</span><span class="sxs-lookup"><span data-stu-id="bfa52-547">The previous state is contained in the **PreviousInstance** property, and the new state is contained in the **TargetInstance** property.</span></span> <span data-ttu-id="bfa52-548">Este evento es asincrónico; en el momento en que se procesa el evento **\_ \_ InstanceModificationEvent** , es posible que la propiedad **TargetInstance** no refleje el estado actual.</span><span class="sxs-lookup"><span data-stu-id="bfa52-548">This event is asynchronous; by the time the **\_\_InstanceModificationEvent** event is processed, the **TargetInstance** property may not reflect the current state.</span></span>

<span data-ttu-id="bfa52-549">El acceso a la clase **MSVM \_ ComputerSystem** podría estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="bfa52-549">Access to the **Msvm\_ComputerSystem** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bfa52-550">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bfa52-550">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="bfa52-551">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bfa52-551">Examples</span></span>

<span data-ttu-id="bfa52-552">Consulte [consultar objetos de red](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bfa52-552">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfa52-553">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfa52-553">Requirements</span></span>



| <span data-ttu-id="bfa52-554">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfa52-554">Requirement</span></span> | <span data-ttu-id="bfa52-555">Value</span><span class="sxs-lookup"><span data-stu-id="bfa52-555">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa52-556">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfa52-556">Minimum supported client</span></span><br/> | <span data-ttu-id="bfa52-557">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="bfa52-557">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bfa52-558">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfa52-558">Minimum supported server</span></span><br/> | <span data-ttu-id="bfa52-559">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="bfa52-559">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bfa52-560">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bfa52-560">Namespace</span></span><br/>                | <span data-ttu-id="bfa52-561">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bfa52-561">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bfa52-562">MOF</span><span class="sxs-lookup"><span data-stu-id="bfa52-562">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfa52-563"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-563"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bfa52-564">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bfa52-564">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfa52-565"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bfa52-565"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bfa52-566">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfa52-566">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa52-567">**ComputerSystem de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="bfa52-567">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dt>

[<span data-ttu-id="bfa52-568">**\_\_InstanceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="bfa52-568">**\_\_InstanceModificationEvent**</span></span>](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[<span data-ttu-id="bfa52-569">**ComputerSystem de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="bfa52-569">**CIM\_ComputerSystem**</span></span>](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[<span data-ttu-id="bfa52-570">**MSVM \_ ComputerSystem (V1)**</span><span class="sxs-lookup"><span data-stu-id="bfa52-570">**Msvm\_ComputerSystem (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[<span data-ttu-id="bfa52-571">Clases de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="bfa52-571">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

