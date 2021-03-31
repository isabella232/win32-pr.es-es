---
description: Representa el servicio de migración del sistema virtual. Se usa para migrar un sistema virtual o para migrar el almacenamiento de un sistema virtual de una plataforma de virtualización a otra.
ms.assetid: af25e405-4498-40a8-ba8e-4b3873c56097
title: Msvm_VirtualSystemMigrationService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService
- Msvm_VirtualSystemMigrationService.InstanceID
- Msvm_VirtualSystemMigrationService.Caption
- Msvm_VirtualSystemMigrationService.Description
- Msvm_VirtualSystemMigrationService.ElementName
- Msvm_VirtualSystemMigrationService.InstallDate
- Msvm_VirtualSystemMigrationService.OperationalStatus
- Msvm_VirtualSystemMigrationService.StatusDescriptions
- Msvm_VirtualSystemMigrationService.Status
- Msvm_VirtualSystemMigrationService.HealthState
- Msvm_VirtualSystemMigrationService.CommunicationStatus
- Msvm_VirtualSystemMigrationService.DetailedStatus
- Msvm_VirtualSystemMigrationService.OperatingStatus
- Msvm_VirtualSystemMigrationService.PrimaryStatus
- Msvm_VirtualSystemMigrationService.EnabledState
- Msvm_VirtualSystemMigrationService.OtherEnabledState
- Msvm_VirtualSystemMigrationService.RequestedState
- Msvm_VirtualSystemMigrationService.EnabledDefault
- Msvm_VirtualSystemMigrationService.TimeOfLastStateChange
- Msvm_VirtualSystemMigrationService.AvailableRequestedStates
- Msvm_VirtualSystemMigrationService.TransitioningToState
- Msvm_VirtualSystemMigrationService.SystemCreationClassName
- Msvm_VirtualSystemMigrationService.SystemName
- Msvm_VirtualSystemMigrationService.Name
- Msvm_VirtualSystemMigrationService.CreationClassName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerContact
- Msvm_VirtualSystemMigrationService.StartMode
- Msvm_VirtualSystemMigrationService.Started
- Msvm_VirtualSystemMigrationService.ActiveVirtualSystemMigrationCount
- Msvm_VirtualSystemMigrationService.ActiveStorageMigrationCount
- Msvm_VirtualSystemMigrationService.MigrationServiceListenerIPAddressList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e80cb12e6e6767b49670a1aff68c9791f224068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808767"
---
# <a name="msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="e2d8c-104">MSVM \_ VirtualSystemMigrationService (clase)</span><span class="sxs-lookup"><span data-stu-id="e2d8c-104">Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="e2d8c-105">Representa el servicio de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-105">Represents the virtual system migration service.</span></span> <span data-ttu-id="e2d8c-106">Se usa para migrar un sistema virtual o para migrar el almacenamiento de un sistema virtual de una plataforma de virtualización a otra.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-106">It is used for migrating a virtual system or for migrating the storage of a virtual system from one virtualization platform to another.</span></span>

<span data-ttu-id="e2d8c-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2d8c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2d8c-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationService : CIM_VirtualSystemMigrationService
{
  string   InstanceID;
  string   Caption = "Hyper-V Migration Service";
  string   Description = "Hyper-V Migration Service";
  string   ElementName = "Hyper-V Migration Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "migrationwmi";
  string   CreationClassName = "Msvm_VirtualSystemMigrationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
  uint32   ActiveVirtualSystemMigrationCount;
  uint32   ActiveStorageMigrationCount;
  string   MigrationServiceListenerIPAddressList[];
};
```

## <a name="members"></a><span data-ttu-id="e2d8c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e2d8c-109">Members</span></span>

<span data-ttu-id="e2d8c-110">La clase **MSVM \_ VirtualSystemMigrationService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e2d8c-110">The **Msvm\_VirtualSystemMigrationService** class has these types of members:</span></span>

-   [<span data-ttu-id="e2d8c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e2d8c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e2d8c-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2d8c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e2d8c-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="e2d8c-113">Methods</span></span>

<span data-ttu-id="e2d8c-114">La clase **MSVM \_ VirtualSystemMigrationService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-114">The **Msvm\_VirtualSystemMigrationService** class has these methods.</span></span>



| <span data-ttu-id="e2d8c-115">Método</span><span class="sxs-lookup"><span data-stu-id="e2d8c-115">Method</span></span>                                                                                                                  | <span data-ttu-id="e2d8c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2d8c-116">Description</span></span>                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2d8c-117">**AddNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-117">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)                                     | <span data-ttu-id="e2d8c-118">Agrega subredes de red de migración para el servicio de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-118">Adds migration network subnets for the virtual system migration service.</span></span><br/>                                                                                          |
| [<span data-ttu-id="e2d8c-119">**CheckSystemCompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-119">**CheckSystemCompatibilityInfo**</span></span>](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="e2d8c-120">Comprueba la información de compatibilidad para la compatibilidad con el sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-120">Checks the compatibility information for compatibility with the hosting computer system.</span></span><br/>                                                                          |
| [<span data-ttu-id="e2d8c-121">**CheckVirtualSystemIsMigratable**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-121">**CheckVirtualSystemIsMigratable**</span></span>](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md)             | <span data-ttu-id="e2d8c-122">Método para migrar un sistema virtual o el almacenamiento de un sistema virtual a un host de destino especificado por un nombre de host.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-122">Method to migrate a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                              |
| [<span data-ttu-id="e2d8c-123">**CheckVirtualSystemIsMigratableToHost**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-123">**CheckVirtualSystemIsMigratableToHost**</span></span>](checkvirtualsystemismigratabletohost-msvm-virtualsystemmigrationservice.md) | <span data-ttu-id="e2d8c-124">Determina si el sistema virtual especificado se puede migrar a un host de destino especificado por un nombre de red o una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-124">Determines whether the specified virtual system can be migrated to a target host specified by a network name or IP address.</span></span><br/>                                       |
| [<span data-ttu-id="e2d8c-125">**GetSystemCompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-125">**GetSystemCompatibilityInfo**</span></span>](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="e2d8c-126">Genera un BLOB opaco de datos que contiene información de compatibilidad del sistema especificado.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-126">Generates an opaque blob of data that contains compatibility information for the specified system.</span></span><br/>                                                                |
| [<span data-ttu-id="e2d8c-127">**GetSystemCompatibilityVectors**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-127">**GetSystemCompatibilityVectors**</span></span>](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)               | <span data-ttu-id="e2d8c-128">Obtiene vectores de compatibilidad para una máquina virtual o un host.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-128">Gets compatibility vectors for a virtual machine or a host.</span></span><br/> <span data-ttu-id="e2d8c-129">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-129">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="e2d8c-130">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-130">**MigrateVirtualSystemToHost**</span></span>](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="e2d8c-131">Migra un sistema virtual o el almacenamiento de un sistema virtual a un host de destino especificado por un nombre de host.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-131">Migrates a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                                       |
| [<span data-ttu-id="e2d8c-132">**MigrateVirtualSystemToSystem**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-132">**MigrateVirtualSystemToSystem**</span></span>](migratevirtualsystemtosystem-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="e2d8c-133">Mueve, migra o reubica un sistema virtual en un sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-133">Moves, migrates, or relocates a virtual system to a target system.</span></span><br/>                                                                                                |
| [<span data-ttu-id="e2d8c-134">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-134">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="e2d8c-135">Modifica las subredes de la red de migración del servicio de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-135">Modifies migration network subnets of the virtual system migration service.</span></span><br/>                                                                                       |
| [<span data-ttu-id="e2d8c-136">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-136">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="e2d8c-137">Modifica los datos de configuración para el servicio de migración.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-137">Modifies the setting data for the migration service.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e2d8c-138">**RemoveNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-138">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="e2d8c-139">Quita las subredes de la red de migración del servicio de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-139">Removes migration network subnets from the virtual system migration service.</span></span><br/>                                                                                      |
| [<span data-ttu-id="e2d8c-140">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-140">**RequestStateChange**</span></span>](msvm-virtualsystemmigrationservice-requeststatechange.md)                                     | <span data-ttu-id="e2d8c-141">Solicita un cambio de estado</span><span class="sxs-lookup"><span data-stu-id="e2d8c-141">Requests a state change</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="e2d8c-142">**StartService**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-142">**StartService**</span></span>](msvm-virtualsystemmigrationservice-startservice.md)                                                 | <span data-ttu-id="e2d8c-143">inicia el servicio.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-143">Starts the service.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="e2d8c-144">**StopService**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-144">**StopService**</span></span>](msvm-virtualsystemmigrationservice-stopservice.md)                                                   | <span data-ttu-id="e2d8c-145">detiene el servicio.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-145">Stops the service.</span></span><br/>                                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="e2d8c-146">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2d8c-146">Properties</span></span>

<span data-ttu-id="e2d8c-147">La clase **MSVM \_ VirtualSystemMigrationService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-147">The **Msvm\_VirtualSystemMigrationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2d8c-148">**ActiveStorageMigrationCount**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-148">**ActiveStorageMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-151">El número de migraciones de almacenamiento actuales en curso.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-151">The number of current storage migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-152">**ActiveVirtualSystemMigrationCount**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-152">**ActiveVirtualSystemMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-153">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-155">El número de migraciones actuales del sistema virtual en curso.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-155">The number of current virtual system migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-156">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-156">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-157">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-159">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e2d8c-159">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="e2d8c-160">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-160">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-161">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-164">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-164">A short description of the object.</span></span> <span data-ttu-id="e2d8c-165">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de migración de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="e2d8c-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-166">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-166">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-167">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-169">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-169">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e2d8c-170">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2d8c-171">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-172">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-172">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-175">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-175">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e2d8c-176">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ VirtualSystemMigrationService".</span><span class="sxs-lookup"><span data-stu-id="e2d8c-176">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemMigrationService".</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-177">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-177">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-180">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-180">A description of the object.</span></span> <span data-ttu-id="e2d8c-181">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de migración de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="e2d8c-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-182">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-182">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-183">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-185">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-185">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e2d8c-186">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-186">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2d8c-187">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-188">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-188">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-191">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-191">A display name for the object.</span></span> <span data-ttu-id="e2d8c-192">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de migración de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="e2d8c-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-193">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-193">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-194">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-196">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-196">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e2d8c-197">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-197">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-198">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-198">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-201">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-201">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e2d8c-202">Esta propiedad también puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-202">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="e2d8c-203">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-203">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-204">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-204">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-205">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-207">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-207">The current health of the element.</span></span> <span data-ttu-id="e2d8c-208">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-208">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="e2d8c-209">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-209">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="e2d8c-210">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-210">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-211">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-211">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-212">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-212">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-214">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-214">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="e2d8c-215">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-216">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-216">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-219">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-219">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-220">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-220">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e2d8c-221">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-221">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-222">**MigrationServiceListenerIPAddressList**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-222">**MigrationServiceListenerIPAddressList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-223">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-223">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-225">La lista de direcciones IP de host que se pueden usar para la migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-225">The list of host IP addresses that can be used for virtual system migration.</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-226">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-229">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-229">The label by which the object is known.</span></span> <span data-ttu-id="e2d8c-230">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "migrationwmi".</span><span class="sxs-lookup"><span data-stu-id="e2d8c-230">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "migrationwmi".</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-231">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-231">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-232">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-234">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="e2d8c-234">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e2d8c-235">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-235">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2d8c-236">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-237">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-237">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-238">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-238">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-240">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-240">The current statuses of the object.</span></span> <span data-ttu-id="e2d8c-241">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-242">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-242">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-245">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-245">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="e2d8c-246">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-246">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="e2d8c-247">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-248">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-248">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-251">Valor que proporciona información sobre cómo se puede alcanzar el propietario principal del servicio (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-251">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="e2d8c-252">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-252">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-253">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-253">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-254">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-255">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-256">Nombre del propietario principal del servicio, si se ha definido uno.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-256">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="e2d8c-257">El propietario principal es el contacto de soporte inicial para el servicio.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-257">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="e2d8c-258">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-258">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-259">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-259">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-260">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-260">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-262">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-262">Provides high level status information.</span></span> <span data-ttu-id="e2d8c-263">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-263">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="e2d8c-264">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-264">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e2d8c-265">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-265">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-266">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-266">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-267">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-269">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-269">The last requested or desired state for the element.</span></span> <span data-ttu-id="e2d8c-270">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-270">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="e2d8c-271">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-271">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="e2d8c-272">Una instancia concreta de [**\_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir el método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e2d8c-272">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="e2d8c-273">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-273">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="e2d8c-274">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM** y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-274">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-275">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-275">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-276">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-277">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-278">Indica si el servicio se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-278">Indicates whether the service is currently running.</span></span> <span data-ttu-id="e2d8c-279">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-279">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-280">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-280">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-281">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-283">Un valor de cadena que indica si el servicio se inicia automáticamente por un sistema, un sistema operativo o se inicia solo después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-283">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="e2d8c-284">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-284">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-285">**Estado**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-285">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-288">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en "OK".</span><span class="sxs-lookup"><span data-stu-id="e2d8c-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-289">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-289">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-290">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-290">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-292">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e2d8c-292">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e2d8c-293">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y las cadenas siempre se establecen en "OK".</span><span class="sxs-lookup"><span data-stu-id="e2d8c-293">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and the strings are always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-294">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-294">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-295">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-297">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-297">The scoping system's creation class name.</span></span> <span data-ttu-id="e2d8c-298">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="e2d8c-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-299">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-299">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-302">Nombre del sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-302">The name of the hosting computer system.</span></span> <span data-ttu-id="e2d8c-303">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-303">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-304">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-304">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-305">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-305">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-307">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-307">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e2d8c-308">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-308">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e2d8c-309">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-309">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2d8c-310">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e2d8c-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e2d8c-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2d8c-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2d8c-312">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-312">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e2d8c-313">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2d8c-313">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2d8c-314">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2d8c-314">Requirements</span></span>



| <span data-ttu-id="e2d8c-315">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2d8c-315">Requirement</span></span> | <span data-ttu-id="e2d8c-316">Value</span><span class="sxs-lookup"><span data-stu-id="e2d8c-316">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d8c-317">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2d8c-317">Minimum supported client</span></span><br/> | <span data-ttu-id="e2d8c-318">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2d8c-318">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e2d8c-319">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2d8c-319">Minimum supported server</span></span><br/> | <span data-ttu-id="e2d8c-320">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2d8c-320">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e2d8c-321">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e2d8c-321">Namespace</span></span><br/>                | <span data-ttu-id="e2d8c-322">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e2d8c-322">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e2d8c-323">MOF</span><span class="sxs-lookup"><span data-stu-id="e2d8c-323">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2d8c-324"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2d8c-324"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2d8c-325">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e2d8c-325">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2d8c-326"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e2d8c-326"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

