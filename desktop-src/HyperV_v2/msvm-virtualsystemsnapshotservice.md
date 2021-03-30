---
description: Servicio para crear, aplicar y destruir instantáneas de máquinas virtuales.
ms.assetid: 34efe124-d198-4bad-a3c9-e8457a5faa5e
title: Msvm_VirtualSystemSnapshotService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService
- Msvm_VirtualSystemSnapshotService.StartService
- Msvm_VirtualSystemSnapshotService.StopService
- Msvm_VirtualSystemSnapshotService.InstanceID
- Msvm_VirtualSystemSnapshotService.Caption
- Msvm_VirtualSystemSnapshotService.Description
- Msvm_VirtualSystemSnapshotService.ElementName
- Msvm_VirtualSystemSnapshotService.InstallDate
- Msvm_VirtualSystemSnapshotService.Name
- Msvm_VirtualSystemSnapshotService.OperationalStatus
- Msvm_VirtualSystemSnapshotService.StatusDescriptions
- Msvm_VirtualSystemSnapshotService.Status
- Msvm_VirtualSystemSnapshotService.HealthState
- Msvm_VirtualSystemSnapshotService.CommunicationStatus
- Msvm_VirtualSystemSnapshotService.DetailedStatus
- Msvm_VirtualSystemSnapshotService.OperatingStatus
- Msvm_VirtualSystemSnapshotService.PrimaryStatus
- Msvm_VirtualSystemSnapshotService.EnabledState
- Msvm_VirtualSystemSnapshotService.OtherEnabledState
- Msvm_VirtualSystemSnapshotService.RequestedState
- Msvm_VirtualSystemSnapshotService.EnabledDefault
- Msvm_VirtualSystemSnapshotService.TimeOfLastStateChange
- Msvm_VirtualSystemSnapshotService.AvailableRequestedStates
- Msvm_VirtualSystemSnapshotService.TransitioningToState
- Msvm_VirtualSystemSnapshotService.SystemCreationClassName
- Msvm_VirtualSystemSnapshotService.SystemName
- Msvm_VirtualSystemSnapshotService.CreationClassName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerContact
- Msvm_VirtualSystemSnapshotService.StartMode
- Msvm_VirtualSystemSnapshotService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be84d70dd9478012e747626a9a566464d7587789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907691"
---
# <a name="msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="1d854-103">MSVM \_ VirtualSystemSnapshotService (clase)</span><span class="sxs-lookup"><span data-stu-id="1d854-103">Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="1d854-104">Servicio para crear, aplicar y destruir instantáneas de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="1d854-104">Service to create, apply, and destroy snapshots of virtual machines.</span></span>

<span data-ttu-id="1d854-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1d854-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d854-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d854-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSnapshotService : CIM_VirtualSystemSnapshotService
{
  string   InstanceID;
  string   Caption = "Hyper-V Virtual System Snapshot Service";
  string   Description = "Service for creating, destroying, and applying virtual machine snapshots";
  string   ElementName;
  datetime InstallDate;
  string   Name = "vssnapsvc";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemSnapshotService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="1d854-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1d854-107">Members</span></span>

<span data-ttu-id="1d854-108">La clase **MSVM \_ VirtualSystemSnapshotService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1d854-108">The **Msvm\_VirtualSystemSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="1d854-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="1d854-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="1d854-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1d854-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1d854-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="1d854-111">Methods</span></span>

<span data-ttu-id="1d854-112">La clase **MSVM \_ VirtualSystemSnapshotService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1d854-112">The **Msvm\_VirtualSystemSnapshotService** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="1d854-113">Método</span><span class="sxs-lookup"><span data-stu-id="1d854-113">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1d854-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d854-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1d854-115"><a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>ApplySnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d854-115"><a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>ApplySnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1d854-116">Aplica una instantánea de máquina virtual a la máquina virtual desde la que se creó.</span><span class="sxs-lookup"><span data-stu-id="1d854-116">Applies a virtual machine snapshot to the virtual machine that it was created from.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1d854-117"><a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>ClearSnapshotState</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d854-117"><a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>ClearSnapshotState</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1d854-118">Borra el estado de guardado de una instantánea existente.</span><span class="sxs-lookup"><span data-stu-id="1d854-118">Clears save state from an existing snapshot.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1d854-119"><a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>ConvertToReferencePoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d854-119"><a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>ConvertToReferencePoint</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1d854-120">Convertir una instantánea del sistema virtual existente en un punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="1d854-120">Convert an existing virtual system snapshot to a reference point.</span></span> <span data-ttu-id="1d854-121">La instantánea se elimina como un efecto secundario.</span><span class="sxs-lookup"><span data-stu-id="1d854-121">The snapshot gets deleted as a side effect.</span></span> <span data-ttu-id="1d854-122">Solo las instantáneas de recuperación se pueden convertir en puntos de referencia.</span><span class="sxs-lookup"><span data-stu-id="1d854-122">Only recovery snapshots can be converted to reference points.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1d854-123">La compatibilidad con este método se agregó en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1d854-123">Support for this method was added in Windows 10.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1d854-124"><a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>CreateSnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d854-124"><a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>CreateSnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1d854-125">Crea una instantánea de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1d854-125">Creates a snapshot of a virtual machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1d854-126"><a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d854-126"><a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1d854-127">Destruya una instantánea de máquina virtual existente.</span><span class="sxs-lookup"><span data-stu-id="1d854-127">Destroy an existing virtual machine snapshot.</span></span> <span data-ttu-id="1d854-128">Este método puede, como efecto secundario, destruir otras instantáneas que dependen de la instantánea afectada.</span><span class="sxs-lookup"><span data-stu-id="1d854-128">This method may, as a side effect, destroy other snapshots that are dependent on the affected snapshot.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1d854-129"><a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshotTree</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d854-129"><a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshotTree</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1d854-130">Quita una instantánea existente, y todos sus elementos secundarios, de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1d854-130">Removes an existing snapshot, and all its children, of a virtual machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1d854-131"><a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>RequestStateChange</strong></a></span><span class="sxs-lookup"><span data-stu-id="1d854-131"><a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>RequestStateChange</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1d854-132">Solicita un cambio de estado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="1d854-132">Requests a state change for the element.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1d854-133">La compatibilidad con este método se agregó en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1d854-133">Support for this method was added in Windows 10.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1d854-134"><strong>StartService</strong></span><span class="sxs-lookup"><span data-stu-id="1d854-134"><strong>StartService</strong></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1d854-135">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="1d854-135">This method is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1d854-136"><strong>StopService</strong></span><span class="sxs-lookup"><span data-stu-id="1d854-136"><strong>StopService</strong></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1d854-137">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="1d854-137">This method is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="1d854-138">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1d854-138">Properties</span></span>

<span data-ttu-id="1d854-139">La clase **MSVM \_ VirtualSystemSnapshotService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1d854-139">The **Msvm\_VirtualSystemSnapshotService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d854-140">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="1d854-140">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-141">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d854-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d854-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-143">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="1d854-143">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method used to initiate a state change.</span></span> <span data-ttu-id="1d854-144">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual del objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1d854-144">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="1d854-145">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="1d854-145">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="1d854-146">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="1d854-146">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="1d854-147">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d854-147">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="1d854-148"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="1d854-148"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-149"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="1d854-149"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-150"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="1d854-150"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-151"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="1d854-151"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-152"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="1d854-152"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-153"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="1d854-153"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-154"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="1d854-154"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-155"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="1d854-155"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-156"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="1d854-156"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-157"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="1d854-157"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="1d854-158">)</span><span class="sxs-lookup"><span data-stu-id="1d854-158">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d854-159">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1d854-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d854-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-162">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="1d854-162">A short description of the object.</span></span> <span data-ttu-id="1d854-163">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "servicio de instantánea de sistema virtual de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="1d854-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Snapshot Service".</span></span>

</dd> <dt>

<span data-ttu-id="1d854-164">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="1d854-164">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-165">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d854-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-167">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="1d854-167">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1d854-168">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="1d854-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1d854-169">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d854-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1d854-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d854-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-171"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="1d854-171"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-172"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="1d854-172"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-173"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="1d854-173"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-174"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="1d854-174"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1d854-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-176"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="1d854-176"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1d854-177">)</span><span class="sxs-lookup"><span data-stu-id="1d854-177">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d854-178">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d854-178">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d854-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d854-181">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="1d854-181">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1d854-182">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="1d854-182">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1d854-183">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ VirtualSystemSnapshotService".</span><span class="sxs-lookup"><span data-stu-id="1d854-183">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemSnapshotService".</span></span>

</dd> <dt>

<span data-ttu-id="1d854-184">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d854-184">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d854-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-187">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="1d854-187">A description of the object.</span></span> <span data-ttu-id="1d854-188">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio para crear, destruir y aplicar instantáneas de máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="1d854-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Service for creating, destroying, and applying virtual machine snapshots".</span></span>

</dd> <dt>

<span data-ttu-id="1d854-189">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1d854-189">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-190">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d854-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-192">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="1d854-192">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1d854-193">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="1d854-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1d854-194">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d854-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1d854-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="1d854-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="1d854-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="1d854-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="1d854-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="1d854-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="1d854-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1d854-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="1d854-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1d854-203">)</span><span class="sxs-lookup"><span data-stu-id="1d854-203">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d854-204">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1d854-204">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-205">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d854-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-207">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="1d854-207">A display name for the object.</span></span> <span data-ttu-id="1d854-208">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1d854-208">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d854-209">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="1d854-209">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-210">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d854-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-212">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="1d854-212">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="1d854-213">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="1d854-213">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="1d854-214">Value</span><span class="sxs-lookup"><span data-stu-id="1d854-214">Value</span></span>                                                                        | <span data-ttu-id="1d854-215">Significado</span><span class="sxs-lookup"><span data-stu-id="1d854-215">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="1d854-216"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-216"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1d854-217">habilitado</span><span class="sxs-lookup"><span data-stu-id="1d854-217">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1d854-218">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="1d854-218">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-219">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d854-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-221">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="1d854-221">The enabled and disabled states of an element.</span></span> <span data-ttu-id="1d854-222">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="1d854-222">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="1d854-223">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="1d854-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="1d854-224">Value</span><span class="sxs-lookup"><span data-stu-id="1d854-224">Value</span></span>                                                                        | <span data-ttu-id="1d854-225">Significado</span><span class="sxs-lookup"><span data-stu-id="1d854-225">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="1d854-226"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-226"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1d854-227">habilitado</span><span class="sxs-lookup"><span data-stu-id="1d854-227">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1d854-228">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1d854-228">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-229">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d854-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-231">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="1d854-231">The current health of the element.</span></span> <span data-ttu-id="1d854-232">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="1d854-232">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="1d854-233">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="1d854-233">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="1d854-234">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="1d854-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="1d854-235">Value</span><span class="sxs-lookup"><span data-stu-id="1d854-235">Value</span></span>                                                                        | <span data-ttu-id="1d854-236">Significado</span><span class="sxs-lookup"><span data-stu-id="1d854-236">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="1d854-237"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-237"><dt>5</dt></span></span> </dl> | <span data-ttu-id="1d854-238">El estado de mantenimiento es normal.</span><span class="sxs-lookup"><span data-stu-id="1d854-238">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1d854-239">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1d854-239">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-240">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d854-240">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-242">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1d854-242">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="1d854-243">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d854-243">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d854-244">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1d854-244">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-245">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d854-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d854-247">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="1d854-247">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1d854-248">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="1d854-248">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1d854-249">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1d854-249">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1d854-250">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1d854-250">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-251">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d854-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d854-253">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="1d854-253">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1d854-254">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="1d854-254">The label by which the object is known.</span></span> <span data-ttu-id="1d854-255">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre se establece en "vssnapsvc".</span><span class="sxs-lookup"><span data-stu-id="1d854-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vssnapsvc".</span></span>

</dd> <dt>

<span data-ttu-id="1d854-256">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="1d854-256">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-257">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d854-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-259">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="1d854-259">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1d854-260">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="1d854-260">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1d854-261">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d854-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1d854-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d854-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="1d854-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="1d854-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="1d854-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="1d854-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="1d854-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="1d854-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="1d854-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="1d854-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="1d854-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="1d854-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="1d854-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="1d854-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="1d854-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="1d854-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="1d854-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="1d854-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1d854-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="1d854-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1d854-281">)</span><span class="sxs-lookup"><span data-stu-id="1d854-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d854-282">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1d854-282">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-283">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d854-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d854-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-285">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="1d854-285">The current statuses of the object.</span></span> <span data-ttu-id="1d854-286">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="1d854-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="1d854-287">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="1d854-287">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-288">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d854-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-290">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="1d854-290">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="1d854-291">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="1d854-291">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="1d854-292">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="1d854-292">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1d854-293">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="1d854-293">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-294">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d854-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d854-296">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="1d854-296">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1d854-297">Cualquier información sobre cómo se puede alcanzar el propietario principal del servicio (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.).</span><span class="sxs-lookup"><span data-stu-id="1d854-297">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="1d854-298">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="1d854-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1d854-299">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="1d854-299">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d854-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d854-302">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="1d854-302">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="1d854-303">Nombre del propietario principal del servicio, si se ha definido uno.</span><span class="sxs-lookup"><span data-stu-id="1d854-303">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="1d854-304">El propietario principal es el contacto de soporte inicial para el servicio.</span><span class="sxs-lookup"><span data-stu-id="1d854-304">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="1d854-305">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="1d854-305">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1d854-306">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="1d854-306">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-307">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d854-307">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-309">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="1d854-309">Provides high level status information.</span></span> <span data-ttu-id="1d854-310">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="1d854-310">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="1d854-311">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="1d854-311">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1d854-312">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1d854-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1d854-313"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d854-313"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-314"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="1d854-314"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-315"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="1d854-315"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-316"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="1d854-316"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-317"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1d854-317"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1d854-318"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="1d854-318"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1d854-319">)</span><span class="sxs-lookup"><span data-stu-id="1d854-319">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d854-320">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="1d854-320">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-321">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d854-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-323">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="1d854-323">The last requested or desired state for the element.</span></span> <span data-ttu-id="1d854-324">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="1d854-324">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="1d854-325">Esta propiedad se proporciona para comparar el último estado solicitado y el actual para un elemento.</span><span class="sxs-lookup"><span data-stu-id="1d854-325">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="1d854-326">Una instancia concreta de la [**clase \_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir la propiedad **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="1d854-326">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="1d854-327">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="1d854-327">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="1d854-328">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM** y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="1d854-328">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="1d854-329">Value</span><span class="sxs-lookup"><span data-stu-id="1d854-329">Value</span></span>                                                                         | <span data-ttu-id="1d854-330">Significado</span><span class="sxs-lookup"><span data-stu-id="1d854-330">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="1d854-331"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-331"><dt>12</dt></span></span> </dl> | <span data-ttu-id="1d854-332">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="1d854-332">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1d854-333">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="1d854-333">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-334">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1d854-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-336">Indica si el servicio se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="1d854-336">Indicates whether the service is currently running.</span></span> <span data-ttu-id="1d854-337">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="1d854-337">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="1d854-338">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="1d854-338">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-339">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d854-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d854-341">Calificadores: **MaxLen** (10)</span><span class="sxs-lookup"><span data-stu-id="1d854-341">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="1d854-342">Un valor de cadena que indica si el servicio se inicia automáticamente por un sistema, un sistema operativo o se inicia solo después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d854-342">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="1d854-343">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="1d854-343">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1d854-344">**Estado**</span><span class="sxs-lookup"><span data-stu-id="1d854-344">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-345">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d854-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-347">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="1d854-347">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1d854-348">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1d854-348">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-349">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="1d854-349">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d854-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-351">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="1d854-351">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="1d854-352">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "el servicio se está ejecutando normalmente".</span><span class="sxs-lookup"><span data-stu-id="1d854-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="1d854-353">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d854-353">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-354">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d854-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d854-356">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="1d854-356">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1d854-357">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="1d854-357">The scoping system's creation class name.</span></span> <span data-ttu-id="1d854-358">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="1d854-358">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="1d854-359">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1d854-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-360">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d854-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d854-362">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="1d854-362">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1d854-363">Nombre NetBIOS del sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="1d854-363">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="1d854-364">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="1d854-364">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="1d854-365">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="1d854-365">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-366">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d854-366">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-368">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="1d854-368">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="1d854-369">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d854-369">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1d854-370">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="1d854-370">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d854-371">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d854-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d854-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d854-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d854-373">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="1d854-373">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="1d854-374">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d854-374">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="1d854-375">Value</span><span class="sxs-lookup"><span data-stu-id="1d854-375">Value</span></span>                                                                                                                                                                                                                                                     | <span data-ttu-id="1d854-376">Significado</span><span class="sxs-lookup"><span data-stu-id="1d854-376">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="1d854-377"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-377"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="1d854-378"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-378"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="1d854-379"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-379"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <span data-ttu-id="1d854-380"><dt>**Apagar**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-380"><dt>**Shut Down**</dt> <dt>4</dt></span></span> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <span data-ttu-id="1d854-381"><dt>**Sin cambio**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-381"><dt>**No Change**</dt> <dt>5</dt></span></span> </dl>                       | <span data-ttu-id="1d854-382">No hay ninguna transición en curso.</span><span class="sxs-lookup"><span data-stu-id="1d854-382">No transition is in progress.</span></span><br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <span data-ttu-id="1d854-383"><dt>**Sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-383"><dt>**Offline**</dt> <dt>6</dt></span></span> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <span data-ttu-id="1d854-384"><dt>**Prueba**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-384"><dt>**Test**</dt> <dt>7</dt></span></span> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <span data-ttu-id="1d854-385"><dt>**Aplazar**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-385"><dt>**Defer**</dt> <dt>8</dt></span></span> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="1d854-386">Modo <dt>**inactivo**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-386"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <span data-ttu-id="1d854-387"><dt>**Reiniciar**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-387"><dt>**Reboot**</dt> <dt>10</dt></span></span> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <span data-ttu-id="1d854-388"><dt>**Restablecer**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-388"><dt>**Reset**</dt> <dt>11</dt></span></span> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="1d854-389"><dt>**No aplicable**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-389"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl>  | <span data-ttu-id="1d854-390">La implementación de no admite la representación de transiciones en curso.</span><span class="sxs-lookup"><span data-stu-id="1d854-390">The implementation does not support representing ongoing transitions.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="1d854-391"><dt> **DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-391"><dt>**DMTF Reserved** </dt> <dt>.. </dt></span></span> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d854-392">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d854-392">Requirements</span></span>



| <span data-ttu-id="1d854-393">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d854-393">Requirement</span></span> | <span data-ttu-id="1d854-394">Value</span><span class="sxs-lookup"><span data-stu-id="1d854-394">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d854-395">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d854-395">Minimum supported client</span></span><br/> | <span data-ttu-id="1d854-396">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d854-396">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1d854-397">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d854-397">Minimum supported server</span></span><br/> | <span data-ttu-id="1d854-398">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d854-398">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1d854-399">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1d854-399">Namespace</span></span><br/>                | <span data-ttu-id="1d854-400">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1d854-400">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1d854-401">MOF</span><span class="sxs-lookup"><span data-stu-id="1d854-401">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d854-402"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-402"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d854-403">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1d854-403">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d854-404"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1d854-404"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

