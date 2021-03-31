---
description: Representa un modificador de Canal de fibra virtual.
ms.assetid: 4300747b-3ffc-4caf-8f0b-76cab6d2294e
title: Msvm_VirtualFcSwitch (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitch
- Msvm_VirtualFcSwitch.SetPowerState
- Msvm_VirtualFcSwitch.InstanceID
- Msvm_VirtualFcSwitch.Caption
- Msvm_VirtualFcSwitch.Description
- Msvm_VirtualFcSwitch.ElementName
- Msvm_VirtualFcSwitch.InstallDate
- Msvm_VirtualFcSwitch.OperationalStatus
- Msvm_VirtualFcSwitch.StatusDescriptions
- Msvm_VirtualFcSwitch.Status
- Msvm_VirtualFcSwitch.HealthState
- Msvm_VirtualFcSwitch.CommunicationStatus
- Msvm_VirtualFcSwitch.DetailedStatus
- Msvm_VirtualFcSwitch.OperatingStatus
- Msvm_VirtualFcSwitch.PrimaryStatus
- Msvm_VirtualFcSwitch.EnabledState
- Msvm_VirtualFcSwitch.OtherEnabledState
- Msvm_VirtualFcSwitch.RequestedState
- Msvm_VirtualFcSwitch.EnabledDefault
- Msvm_VirtualFcSwitch.TimeOfLastStateChange
- Msvm_VirtualFcSwitch.AvailableRequestedStates
- Msvm_VirtualFcSwitch.TransitioningToState
- Msvm_VirtualFcSwitch.CreationClassName
- Msvm_VirtualFcSwitch.Name
- Msvm_VirtualFcSwitch.PrimaryOwnerName
- Msvm_VirtualFcSwitch.PrimaryOwnerContact
- Msvm_VirtualFcSwitch.Roles
- Msvm_VirtualFcSwitch.NameFormat
- Msvm_VirtualFcSwitch.OtherIdentifyingInfo
- Msvm_VirtualFcSwitch.IdentifyingDescriptions
- Msvm_VirtualFcSwitch.Dedicated
- Msvm_VirtualFcSwitch.OtherDedicatedDescriptions
- Msvm_VirtualFcSwitch.ResetCapability
- Msvm_VirtualFcSwitch.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66c6b7a284a2751b1c9b664428a9c90db9f468a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153891"
---
# <a name="msvm_virtualfcswitch-class"></a><span data-ttu-id="25f74-103">MSVM \_ VirtualFcSwitch (clase)</span><span class="sxs-lookup"><span data-stu-id="25f74-103">Msvm\_VirtualFcSwitch class</span></span>

<span data-ttu-id="25f74-104">Representa un modificador de Canal de fibra virtual.</span><span class="sxs-lookup"><span data-stu-id="25f74-104">Represents a virtual Fibre Channel switch.</span></span> <span data-ttu-id="25f74-105">Cada modificador está asociado a un puerto físico Canal de fibra al que se pueden conectar muchos puertos de Canal de fibra sintéticos.</span><span class="sxs-lookup"><span data-stu-id="25f74-105">Each switch is associated with one physical Fibre Channel port to which many synthetic Fibre Channel ports can be connected.</span></span> <span data-ttu-id="25f74-106">El propio conmutador no es muy configurable y actúa principalmente como un marcador de posición.</span><span class="sxs-lookup"><span data-stu-id="25f74-106">The switch itself is not highly configurable and acts mostly as a placeholder.</span></span>

<span data-ttu-id="25f74-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="25f74-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="25f74-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25f74-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitch : CIM_ComputerSystem
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
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability;
  uint16   PowerManagementCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="25f74-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="25f74-109">Members</span></span>

<span data-ttu-id="25f74-110">La clase **MSVM \_ VirtualFcSwitch** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="25f74-110">The **Msvm\_VirtualFcSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="25f74-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="25f74-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="25f74-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25f74-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="25f74-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="25f74-113">Methods</span></span>

<span data-ttu-id="25f74-114">La clase **MSVM \_ VirtualFcSwitch** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="25f74-114">The **Msvm\_VirtualFcSwitch** class has these methods.</span></span>



| <span data-ttu-id="25f74-115">Método</span><span class="sxs-lookup"><span data-stu-id="25f74-115">Method</span></span>                                                                | <span data-ttu-id="25f74-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="25f74-116">Description</span></span>                              |
|:----------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="25f74-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="25f74-117">**RequestStateChange**</span></span>](msvm-virtualfcswitch-requeststatechange.md) | <span data-ttu-id="25f74-118">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="25f74-118">Requests a state change.</span></span><br/>      |
| <span data-ttu-id="25f74-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="25f74-119">**SetPowerState**</span></span>                                                     | <span data-ttu-id="25f74-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="25f74-120">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="25f74-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25f74-121">Properties</span></span>

<span data-ttu-id="25f74-122">La clase **MSVM \_ VirtualFcSwitch** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="25f74-122">The **Msvm\_VirtualFcSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25f74-123">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="25f74-123">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-124">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25f74-124">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="25f74-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-126">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="25f74-126">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="25f74-127">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual del objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="25f74-127">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="25f74-128">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="25f74-128">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="25f74-129">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="25f74-129">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="25f74-130">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="25f74-130">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="25f74-131"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="25f74-131"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-132"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="25f74-132"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-133"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="25f74-133"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-134"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="25f74-134"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-135"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="25f74-135"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-136"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="25f74-136"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-137"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="25f74-137"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-138"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="25f74-138"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-139"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="25f74-139"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-140"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="25f74-140"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="25f74-141">)</span><span class="sxs-lookup"><span data-stu-id="25f74-141">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="25f74-142">**Caption**</span><span class="sxs-lookup"><span data-stu-id="25f74-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25f74-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-145">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="25f74-145">A short description of the object.</span></span> <span data-ttu-id="25f74-146">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="25f74-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="25f74-147">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="25f74-147">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-148">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25f74-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-150">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="25f74-150">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="25f74-151">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="25f74-151">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="25f74-152">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="25f74-152">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="25f74-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="25f74-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="25f74-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="25f74-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="25f74-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="25f74-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="25f74-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="25f74-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="25f74-160">)</span><span class="sxs-lookup"><span data-stu-id="25f74-160">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="25f74-161">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="25f74-161">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25f74-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-164">Nombre de la clase o subclase que se usa en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="25f74-164">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="25f74-165">Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system).</span><span class="sxs-lookup"><span data-stu-id="25f74-165">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).</span></span>

</dd> <dt>

<span data-ttu-id="25f74-166">**Dedicado**</span><span class="sxs-lookup"><span data-stu-id="25f74-166">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-167">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25f74-167">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="25f74-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-169">Indica si el sistema informático es un sistema especial (dedicado a un uso determinado), en lugar de un sistema de uso general.</span><span class="sxs-lookup"><span data-stu-id="25f74-169">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="25f74-170">Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en 0 (no dedicado).</span><span class="sxs-lookup"><span data-stu-id="25f74-170">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="25f74-171">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25f74-171">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25f74-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-174">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="25f74-174">A description of the object.</span></span> <span data-ttu-id="25f74-175">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="25f74-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="25f74-176">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="25f74-176">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-177">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25f74-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-179">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="25f74-179">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="25f74-180">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="25f74-180">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="25f74-181">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="25f74-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="25f74-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="25f74-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="25f74-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="25f74-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="25f74-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="25f74-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="25f74-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="25f74-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="25f74-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="25f74-190">)</span><span class="sxs-lookup"><span data-stu-id="25f74-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="25f74-191">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="25f74-191">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25f74-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-194">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="25f74-194">A display name for the object.</span></span> <span data-ttu-id="25f74-195">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="25f74-195">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="25f74-196">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="25f74-196">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-197">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25f74-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-199">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="25f74-199">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="25f74-200">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) y tendrá uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="25f74-200">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="25f74-201"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="25f74-201"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-202"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="25f74-202"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-203"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitada pero sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="25f74-203"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="25f74-204">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="25f74-204">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-205">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25f74-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-207">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="25f74-207">The enabled and disabled states of an element.</span></span> <span data-ttu-id="25f74-208">Esta propiedad también puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="25f74-208">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="25f74-209">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="25f74-209">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="25f74-210">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="25f74-210">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-211">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25f74-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-213">Especifica el estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="25f74-213">Specifies the current health of the element.</span></span> <span data-ttu-id="25f74-214">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="25f74-214">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="25f74-215">Cuando se produzca un error crítico, compruebe el registro de eventos para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="25f74-215">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="25f74-216">La propiedad **EnabledState** también puede contener más información.</span><span class="sxs-lookup"><span data-stu-id="25f74-216">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="25f74-217">Por ejemplo, si el espacio en disco es muy bajo, **HealthState** se establece en 25, la máquina virtual se pausa y **EnabledState** se establece en 32768 (en pausa).</span><span class="sxs-lookup"><span data-stu-id="25f74-217">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="25f74-218">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="25f74-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="25f74-219">Value</span><span class="sxs-lookup"><span data-stu-id="25f74-219">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="25f74-220">Significado</span><span class="sxs-lookup"><span data-stu-id="25f74-220">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="25f74-221"><dt>**Aceptar**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="25f74-221"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="25f74-222">El elemento es totalmente funcional y funciona dentro de los parámetros operativos normales y sin errores.</span><span class="sxs-lookup"><span data-stu-id="25f74-222">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="25f74-223"><dt>**Error principal**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="25f74-223"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="25f74-224">El elemento ha sufrido un error importante.</span><span class="sxs-lookup"><span data-stu-id="25f74-224">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="25f74-225"><dt>**Error crítico**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="25f74-225"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="25f74-226">El elemento no es funcional y es posible que la recuperación no sea posible.</span><span class="sxs-lookup"><span data-stu-id="25f74-226">The element is nonfunctional and recovery might not be possible.</span></span><br/>                                         |



 

</dd> <dt>

<span data-ttu-id="25f74-227">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="25f74-227">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-228">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="25f74-228">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="25f74-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-230">Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="25f74-230">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="25f74-231">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="25f74-231">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-232">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="25f74-232">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-234">Fecha y hora en que se creó la configuración de la máquina virtual para una máquina virtual, o **null**, para un sistema operativo de administración.</span><span class="sxs-lookup"><span data-stu-id="25f74-234">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="25f74-235">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="25f74-235">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="25f74-236">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="25f74-236">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25f74-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f74-239">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="25f74-239">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="25f74-240">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="25f74-240">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="25f74-241">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="25f74-241">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="25f74-242">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="25f74-242">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25f74-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-245">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="25f74-245">The label by which the object is known.</span></span> <span data-ttu-id="25f74-246">Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system).</span><span class="sxs-lookup"><span data-stu-id="25f74-246">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).</span></span>

</dd> <dt>

<span data-ttu-id="25f74-247">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="25f74-247">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-248">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25f74-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-250">Cadena que identifica el modo en que se generó el nombre del sistema mediante la heurística de subclases.</span><span class="sxs-lookup"><span data-stu-id="25f74-250">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="25f74-251">Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="25f74-251">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="25f74-252">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="25f74-252">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-253">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25f74-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-255">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="25f74-255">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="25f74-256">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="25f74-256">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="25f74-257">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="25f74-257">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="25f74-258"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="25f74-258"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-259"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="25f74-259"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-260"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="25f74-260"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-261"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="25f74-261"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-262"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="25f74-262"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-263"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="25f74-263"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-264"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="25f74-264"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-265"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="25f74-265"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-266"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="25f74-266"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-267"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="25f74-267"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-268"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="25f74-268"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-269"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="25f74-269"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-270"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="25f74-270"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-271"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="25f74-271"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-272"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="25f74-272"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-273"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="25f74-273"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-274"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="25f74-274"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-275"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="25f74-275"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-276"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="25f74-276"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="25f74-277">)</span><span class="sxs-lookup"><span data-stu-id="25f74-277">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="25f74-278">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="25f74-278">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-279">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25f74-279">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="25f74-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-281">Una matriz que contiene los Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="25f74-281">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="25f74-282">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="25f74-282">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="25f74-283">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="25f74-283">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-284">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="25f74-284">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="25f74-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-286">Una cadena que describe cómo o por qué el sistema está dedicado cuando la matriz **dedicada** incluye el valor 2 (otro).</span><span class="sxs-lookup"><span data-stu-id="25f74-286">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="25f74-287">Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="25f74-287">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="25f74-288">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="25f74-288">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-289">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25f74-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-291">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="25f74-291">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="25f74-292">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="25f74-292">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="25f74-293">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="25f74-293">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="25f74-294">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="25f74-294">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-295">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="25f74-295">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="25f74-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-297">Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="25f74-297">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="25f74-298">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="25f74-298">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-299">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25f74-299">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="25f74-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-301">Esta propiedad se hereda de [**un \_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="25f74-301">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="25f74-302">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="25f74-302">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25f74-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-305">Cadena que indica cómo se puede alcanzar el propietario del sistema principal (por ejemplo, un número de teléfono o una dirección de correo electrónico).</span><span class="sxs-lookup"><span data-stu-id="25f74-305">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="25f74-306">Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="25f74-306">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="25f74-307">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="25f74-307">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-308">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25f74-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-310">Nombre del propietario del sistema principal.</span><span class="sxs-lookup"><span data-stu-id="25f74-310">The name of the primary system owner.</span></span> <span data-ttu-id="25f74-311">Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="25f74-311">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="25f74-312">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="25f74-312">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-313">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25f74-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-315">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="25f74-315">Provides high level status information.</span></span> <span data-ttu-id="25f74-316">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="25f74-316">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="25f74-317">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="25f74-317">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="25f74-318">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="25f74-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="25f74-319"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="25f74-319"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-320"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="25f74-320"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-321"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="25f74-321"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-322"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="25f74-322"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-323"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="25f74-323"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="25f74-324"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="25f74-324"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="25f74-325">)</span><span class="sxs-lookup"><span data-stu-id="25f74-325">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="25f74-326">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="25f74-326">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-327">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25f74-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-329">Último estado solicitado o deseado del elemento que se pasa al método **RequestStateChange** , o 12 (no aplicable) si no hay ningún cambio de estado en curso.</span><span class="sxs-lookup"><span data-stu-id="25f74-329">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="25f74-330">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="25f74-330">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="25f74-331">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="25f74-331">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="25f74-332">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="25f74-332">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="25f74-333">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="25f74-333">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-334">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25f74-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-336">Esta propiedad se hereda de [**un \_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem).</span><span class="sxs-lookup"><span data-stu-id="25f74-336">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem).</span></span>

</dd> <dt>

<span data-ttu-id="25f74-337">**Roles**</span><span class="sxs-lookup"><span data-stu-id="25f74-337">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-338">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="25f74-338">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="25f74-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-340">Matriz de cadenas que describen los roles que el sistema desempeña en el entorno de tecnología de la información.</span><span class="sxs-lookup"><span data-stu-id="25f74-340">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="25f74-341">Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="25f74-341">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="25f74-342">**Estado**</span><span class="sxs-lookup"><span data-stu-id="25f74-342">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-343">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25f74-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-345">Cadena que especifica el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="25f74-345">A string that specifies the status of the element.</span></span> <span data-ttu-id="25f74-346">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="25f74-346">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="25f74-347">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="25f74-347">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-348">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="25f74-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="25f74-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25f74-350">Calificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="25f74-350">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="25f74-351">Una matriz que contiene cadenas que describen los valores correspondientes de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="25f74-351">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="25f74-352">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="25f74-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="25f74-353">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="25f74-353">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-354">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="25f74-354">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-356">Fecha y hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="25f74-356">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="25f74-357">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="25f74-357">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="25f74-358">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="25f74-358">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25f74-359">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25f74-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25f74-360">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25f74-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25f74-361">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="25f74-361">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="25f74-362">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="25f74-362">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25f74-363">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25f74-363">Requirements</span></span>



| <span data-ttu-id="25f74-364">Requisito</span><span class="sxs-lookup"><span data-stu-id="25f74-364">Requirement</span></span> | <span data-ttu-id="25f74-365">Value</span><span class="sxs-lookup"><span data-stu-id="25f74-365">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25f74-366">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25f74-366">Minimum supported client</span></span><br/> | <span data-ttu-id="25f74-367">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="25f74-367">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="25f74-368">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25f74-368">Minimum supported server</span></span><br/> | <span data-ttu-id="25f74-369">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="25f74-369">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="25f74-370">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="25f74-370">Namespace</span></span><br/>                | <span data-ttu-id="25f74-371">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="25f74-371">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="25f74-372">MOF</span><span class="sxs-lookup"><span data-stu-id="25f74-372">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25f74-373"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25f74-373"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="25f74-374">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="25f74-374">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25f74-375"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="25f74-375"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

