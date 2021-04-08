---
description: Representa un conmutador Ethernet virtual. Cada conmutador tiene muchos puertos diferentes a los que se pueden conectar los adaptadores de red. El propio conmutador no es muy configurable y actúa principalmente como un marcador de posición.
ms.assetid: 9415477a-9423-40fa-a887-3a93da1374af
title: Msvm_VirtualEthernetSwitch (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitch
- Msvm_VirtualEthernetSwitch.SetPowerState
- Msvm_VirtualEthernetSwitch.InstanceID
- Msvm_VirtualEthernetSwitch.Caption
- Msvm_VirtualEthernetSwitch.Description
- Msvm_VirtualEthernetSwitch.ElementName
- Msvm_VirtualEthernetSwitch.InstallDate
- Msvm_VirtualEthernetSwitch.OperationalStatus
- Msvm_VirtualEthernetSwitch.StatusDescriptions
- Msvm_VirtualEthernetSwitch.Status
- Msvm_VirtualEthernetSwitch.HealthState
- Msvm_VirtualEthernetSwitch.CommunicationStatus
- Msvm_VirtualEthernetSwitch.DetailedStatus
- Msvm_VirtualEthernetSwitch.OperatingStatus
- Msvm_VirtualEthernetSwitch.PrimaryStatus
- Msvm_VirtualEthernetSwitch.EnabledState
- Msvm_VirtualEthernetSwitch.OtherEnabledState
- Msvm_VirtualEthernetSwitch.RequestedState
- Msvm_VirtualEthernetSwitch.EnabledDefault
- Msvm_VirtualEthernetSwitch.TimeOfLastStateChange
- Msvm_VirtualEthernetSwitch.AvailableRequestedStates
- Msvm_VirtualEthernetSwitch.TransitioningToState
- Msvm_VirtualEthernetSwitch.CreationClassName
- Msvm_VirtualEthernetSwitch.Name
- Msvm_VirtualEthernetSwitch.PrimaryOwnerName
- Msvm_VirtualEthernetSwitch.PrimaryOwnerContact
- Msvm_VirtualEthernetSwitch.Roles
- Msvm_VirtualEthernetSwitch.NameFormat
- Msvm_VirtualEthernetSwitch.OtherIdentifyingInfo
- Msvm_VirtualEthernetSwitch.IdentifyingDescriptions
- Msvm_VirtualEthernetSwitch.Dedicated
- Msvm_VirtualEthernetSwitch.OtherDedicatedDescriptions
- Msvm_VirtualEthernetSwitch.ResetCapability
- Msvm_VirtualEthernetSwitch.PowerManagementCapabilities
- Msvm_VirtualEthernetSwitch.MaxVMQOffloads
- Msvm_VirtualEthernetSwitch.MaxIOVOffloads
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1cd916e24a6e34ed6a70002c4988f55810050c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911010"
---
# <a name="msvm_virtualethernetswitch-class"></a><span data-ttu-id="41d92-105">MSVM \_ VirtualEthernetSwitch (clase)</span><span class="sxs-lookup"><span data-stu-id="41d92-105">Msvm\_VirtualEthernetSwitch class</span></span>

<span data-ttu-id="41d92-106">Representa un conmutador Ethernet virtual.</span><span class="sxs-lookup"><span data-stu-id="41d92-106">Represents a virtual Ethernet switch.</span></span> <span data-ttu-id="41d92-107">Cada conmutador tiene muchos puertos diferentes a los que se pueden conectar los adaptadores de red.</span><span class="sxs-lookup"><span data-stu-id="41d92-107">Each switch has many different ports to which network adapters can be attached.</span></span> <span data-ttu-id="41d92-108">El propio conmutador no es muy configurable y actúa principalmente como un marcador de posición.</span><span class="sxs-lookup"><span data-stu-id="41d92-108">The switch itself is not highly configurable and acts mostly as a placeholder.</span></span>

<span data-ttu-id="41d92-109">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="41d92-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d92-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41d92-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitch : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption = "Virtual Switch";
  string   Description = "Microsoft Virtual Switch";
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
  string   CreationClassName = "Msvm_VirtualEthernetSwitch";
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 5;
  uint16   PowerManagementCapabilities[];
  uint32   MaxVMQOffloads;
  uint32   MaxIOVOffloads;
};
```

## <a name="members"></a><span data-ttu-id="41d92-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="41d92-111">Members</span></span>

<span data-ttu-id="41d92-112">La clase **MSVM \_ VirtualEthernetSwitch** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="41d92-112">The **Msvm\_VirtualEthernetSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="41d92-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="41d92-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="41d92-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41d92-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="41d92-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="41d92-115">Methods</span></span>

<span data-ttu-id="41d92-116">La clase **MSVM \_ VirtualEthernetSwitch** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="41d92-116">The **Msvm\_VirtualEthernetSwitch** class has these methods.</span></span>



| <span data-ttu-id="41d92-117">Método</span><span class="sxs-lookup"><span data-stu-id="41d92-117">Method</span></span>                                                                      | <span data-ttu-id="41d92-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="41d92-118">Description</span></span>                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="41d92-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="41d92-119">**RequestStateChange**</span></span>](msvm-virtualethernetswitch-requeststatechange.md) | <span data-ttu-id="41d92-120">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="41d92-120">Requests a state change.</span></span><br/>      |
| <span data-ttu-id="41d92-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="41d92-121">**SetPowerState**</span></span>                                                           | <span data-ttu-id="41d92-122">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="41d92-122">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="41d92-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41d92-123">Properties</span></span>

<span data-ttu-id="41d92-124">La clase **MSVM \_ VirtualEthernetSwitch** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="41d92-124">The **Msvm\_VirtualEthernetSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41d92-125">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="41d92-125">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-126">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d92-126">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41d92-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-128">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="41d92-128">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="41d92-129">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual del objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="41d92-129">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="41d92-130">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="41d92-130">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="41d92-131">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="41d92-131">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="41d92-132">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="41d92-132">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="41d92-133"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="41d92-133"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-134"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="41d92-134"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-135"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="41d92-135"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-136"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="41d92-136"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-137"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="41d92-137"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-138"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="41d92-138"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-139"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="41d92-139"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-140"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="41d92-140"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-141"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="41d92-141"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-142"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="41d92-142"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="41d92-143">)</span><span class="sxs-lookup"><span data-stu-id="41d92-143">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41d92-144">**Caption**</span><span class="sxs-lookup"><span data-stu-id="41d92-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d92-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-147">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="41d92-147">A short description of the object.</span></span> <span data-ttu-id="41d92-148">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "Virtual Switch".</span><span class="sxs-lookup"><span data-stu-id="41d92-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Switch".</span></span>

</dd> <dt>

<span data-ttu-id="41d92-149">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="41d92-149">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-150">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d92-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-152">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="41d92-152">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="41d92-153">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="41d92-153">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="41d92-154">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="41d92-154">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="41d92-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="41d92-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-156"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="41d92-156"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-157"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="41d92-157"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-158"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="41d92-158"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-159"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="41d92-159"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-160"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="41d92-160"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-161"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="41d92-161"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="41d92-162">)</span><span class="sxs-lookup"><span data-stu-id="41d92-162">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41d92-163">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="41d92-163">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d92-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-166">Nombre de la clase o subclase que se usa en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="41d92-166">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="41d92-167">Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre se establece en "MSVM \_ VirtualEthernetSwitch".</span><span class="sxs-lookup"><span data-stu-id="41d92-167">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="41d92-168">**Dedicado**</span><span class="sxs-lookup"><span data-stu-id="41d92-168">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-169">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d92-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41d92-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-171">Indica si el sistema informático es un sistema especial (dedicado a un uso determinado), en lugar de un sistema de uso general.</span><span class="sxs-lookup"><span data-stu-id="41d92-171">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="41d92-172">Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en 0 (no dedicado).</span><span class="sxs-lookup"><span data-stu-id="41d92-172">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="41d92-173">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="41d92-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d92-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-176">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="41d92-176">A description of the object.</span></span> <span data-ttu-id="41d92-177">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "conmutador virtual de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="41d92-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Switch".</span></span>

</dd> <dt>

<span data-ttu-id="41d92-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="41d92-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-179">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d92-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-181">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="41d92-181">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="41d92-182">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="41d92-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="41d92-183">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="41d92-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="41d92-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="41d92-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="41d92-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="41d92-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="41d92-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="41d92-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="41d92-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="41d92-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="41d92-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="41d92-192">)</span><span class="sxs-lookup"><span data-stu-id="41d92-192">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41d92-193">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="41d92-193">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d92-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-196">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="41d92-196">A display name for the object.</span></span> <span data-ttu-id="41d92-197">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="41d92-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="41d92-198">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="41d92-198">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-199">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d92-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-201">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="41d92-201">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="41d92-202">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) y tendrá uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="41d92-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="41d92-203"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="41d92-203"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-204"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="41d92-204"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-205"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitada pero sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="41d92-205"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41d92-206">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="41d92-206">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-207">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d92-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-209">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="41d92-209">The enabled and disabled states of an element.</span></span> <span data-ttu-id="41d92-210">Esta propiedad también puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="41d92-210">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="41d92-211">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="41d92-211">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="41d92-212">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="41d92-212">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-213">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d92-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-215">Especifica el estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="41d92-215">Specifies the current health of the element.</span></span> <span data-ttu-id="41d92-216">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="41d92-216">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="41d92-217">Cuando se produzca un error crítico, compruebe el registro de eventos para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="41d92-217">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="41d92-218">La propiedad **EnabledState** también puede contener más información.</span><span class="sxs-lookup"><span data-stu-id="41d92-218">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="41d92-219">Por ejemplo, si el espacio en disco es muy bajo, **HealthState** se establece en 25, la máquina virtual se pausa y **EnabledState** se establece en 32768 (en pausa).</span><span class="sxs-lookup"><span data-stu-id="41d92-219">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="41d92-220">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="41d92-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="41d92-221">Value</span><span class="sxs-lookup"><span data-stu-id="41d92-221">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="41d92-222">Significado</span><span class="sxs-lookup"><span data-stu-id="41d92-222">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="41d92-223"><dt>**Aceptar**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="41d92-223"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="41d92-224">El elemento es totalmente funcional y funciona dentro de los parámetros operativos normales y sin errores.</span><span class="sxs-lookup"><span data-stu-id="41d92-224">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="41d92-225"><dt>**Error principal**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="41d92-225"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="41d92-226">El elemento ha sufrido un error importante.</span><span class="sxs-lookup"><span data-stu-id="41d92-226">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="41d92-227"><dt>**Error crítico**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="41d92-227"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="41d92-228">El elemento no es funcional y es posible que la recuperación no sea posible.</span><span class="sxs-lookup"><span data-stu-id="41d92-228">The element is nonfunctional, and recovery might not be possible.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="41d92-229">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="41d92-229">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-230">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="41d92-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41d92-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-232">Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="41d92-232">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41d92-233">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="41d92-233">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-234">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="41d92-234">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-236">Fecha y hora en que se creó la configuración de la máquina virtual para una máquina virtual, o **null**, para un sistema operativo de administración.</span><span class="sxs-lookup"><span data-stu-id="41d92-236">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="41d92-237">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="41d92-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="41d92-238">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="41d92-238">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-239">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d92-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d92-241">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="41d92-241">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="41d92-242">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="41d92-242">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="41d92-243">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="41d92-243">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="41d92-244">**MaxIOVOffloads**</span><span class="sxs-lookup"><span data-stu-id="41d92-244">**MaxIOVOffloads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-245">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41d92-245">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-247">El número máximo de descargas de funciones virtuales de virtualización de e/s de raíz única (SR-IOV) disponibles en este conmutador.</span><span class="sxs-lookup"><span data-stu-id="41d92-247">The maximum number of single root IO virtualization (SR-IOV) virtual function offloads available on this switch.</span></span>

</dd> <dt>

<span data-ttu-id="41d92-248">**MaxVMQOffloads**</span><span class="sxs-lookup"><span data-stu-id="41d92-248">**MaxVMQOffloads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-249">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41d92-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-250">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="41d92-250">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="41d92-251">El número máximo de descargas de Virtual Machine Queue (VMQ) permitidas para un puerto en este conmutador.</span><span class="sxs-lookup"><span data-stu-id="41d92-251">The maximum number of virtual machine queue (VMQ) offloads allowed for a port on this switch.</span></span>

</dd> <dt>

<span data-ttu-id="41d92-252">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="41d92-252">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-253">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d92-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-255">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="41d92-255">The label by which the object is known.</span></span> <span data-ttu-id="41d92-256">Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre está establecida en "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="41d92-256">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="41d92-257">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="41d92-257">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d92-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-260">Cadena que identifica el modo en que se generó el nombre del sistema mediante la heurística de subclases.</span><span class="sxs-lookup"><span data-stu-id="41d92-260">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="41d92-261">Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="41d92-261">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41d92-262">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="41d92-262">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-263">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d92-263">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-265">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="41d92-265">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="41d92-266">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="41d92-266">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="41d92-267">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="41d92-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="41d92-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="41d92-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-269"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="41d92-269"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-270"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="41d92-270"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-271"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="41d92-271"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-272"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="41d92-272"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-273"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="41d92-273"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-274"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="41d92-274"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-275"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="41d92-275"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-276"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="41d92-276"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-277"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="41d92-277"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-278"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="41d92-278"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-279"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="41d92-279"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-280"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="41d92-280"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-281"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="41d92-281"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-282"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="41d92-282"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-283"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="41d92-283"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-284"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="41d92-284"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-285"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="41d92-285"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-286"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="41d92-286"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="41d92-287">)</span><span class="sxs-lookup"><span data-stu-id="41d92-287">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41d92-288">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="41d92-288">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-289">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d92-289">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41d92-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-291">Una matriz que contiene los Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="41d92-291">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="41d92-292">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="41d92-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="41d92-293">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="41d92-293">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-294">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="41d92-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41d92-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-296">Una cadena que describe cómo o por qué el sistema está dedicado cuando la matriz **dedicada** incluye el valor 2 (otro).</span><span class="sxs-lookup"><span data-stu-id="41d92-296">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="41d92-297">Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="41d92-297">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41d92-298">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="41d92-298">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-299">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d92-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-301">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="41d92-301">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="41d92-302">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="41d92-302">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="41d92-303">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="41d92-303">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41d92-304">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="41d92-304">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-305">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="41d92-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41d92-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-307">Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="41d92-307">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41d92-308">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="41d92-308">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-309">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d92-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41d92-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-311">Esta propiedad se hereda de [**un \_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="41d92-311">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="41d92-312">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="41d92-312">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-313">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d92-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-315">Cadena que indica cómo se puede alcanzar el propietario del sistema principal (por ejemplo, un número de teléfono o una dirección de correo electrónico).</span><span class="sxs-lookup"><span data-stu-id="41d92-315">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="41d92-316">Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="41d92-316">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41d92-317">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="41d92-317">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-318">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d92-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-320">Nombre del propietario del sistema principal.</span><span class="sxs-lookup"><span data-stu-id="41d92-320">The name of the primary system owner.</span></span> <span data-ttu-id="41d92-321">Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="41d92-321">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41d92-322">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="41d92-322">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-323">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d92-323">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-325">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="41d92-325">Provides high level status information.</span></span> <span data-ttu-id="41d92-326">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="41d92-326">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="41d92-327">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="41d92-327">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="41d92-328">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="41d92-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="41d92-329"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="41d92-329"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-330"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="41d92-330"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-331"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="41d92-331"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-332"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="41d92-332"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="41d92-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="41d92-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="41d92-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="41d92-335">)</span><span class="sxs-lookup"><span data-stu-id="41d92-335">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41d92-336">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="41d92-336">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-337">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d92-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-339">Último estado solicitado o deseado del elemento que se pasa al método **RequestStateChange** , o 12 (no aplicable) si no hay ningún cambio de estado en curso.</span><span class="sxs-lookup"><span data-stu-id="41d92-339">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="41d92-340">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="41d92-340">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="41d92-341">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="41d92-341">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="41d92-342">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="41d92-342">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="41d92-343">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="41d92-343">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-344">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d92-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-346">Esta propiedad se hereda de [**un \_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en 5 (no implementado).</span><span class="sxs-lookup"><span data-stu-id="41d92-346">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 5 (Not implemented).</span></span>

</dd> <dt>

<span data-ttu-id="41d92-347">**Roles**</span><span class="sxs-lookup"><span data-stu-id="41d92-347">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-348">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="41d92-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41d92-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-350">Matriz de cadenas que describen los roles que el sistema desempeña en el entorno de tecnología de la información.</span><span class="sxs-lookup"><span data-stu-id="41d92-350">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="41d92-351">Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="41d92-351">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41d92-352">**Estado**</span><span class="sxs-lookup"><span data-stu-id="41d92-352">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-353">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d92-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-355">Cadena que especifica el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="41d92-355">A string that specifies the status of the element.</span></span> <span data-ttu-id="41d92-356">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="41d92-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="41d92-357">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="41d92-357">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-358">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="41d92-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41d92-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d92-360">Calificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="41d92-360">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="41d92-361">Una matriz que contiene cadenas que describen los valores correspondientes de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="41d92-361">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="41d92-362">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="41d92-362">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="41d92-363">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="41d92-363">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-364">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="41d92-364">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-366">Fecha y hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="41d92-366">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="41d92-367">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="41d92-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="41d92-368">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="41d92-368">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d92-369">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d92-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41d92-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d92-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d92-371">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="41d92-371">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="41d92-372">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="41d92-372">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41d92-373">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41d92-373">Requirements</span></span>



| <span data-ttu-id="41d92-374">Requisito</span><span class="sxs-lookup"><span data-stu-id="41d92-374">Requirement</span></span> | <span data-ttu-id="41d92-375">Value</span><span class="sxs-lookup"><span data-stu-id="41d92-375">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41d92-376">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41d92-376">Minimum supported client</span></span><br/> | <span data-ttu-id="41d92-377">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="41d92-377">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="41d92-378">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41d92-378">Minimum supported server</span></span><br/> | <span data-ttu-id="41d92-379">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="41d92-379">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="41d92-380">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="41d92-380">Namespace</span></span><br/>                | <span data-ttu-id="41d92-381">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="41d92-381">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="41d92-382">MOF</span><span class="sxs-lookup"><span data-stu-id="41d92-382">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41d92-383"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41d92-383"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="41d92-384">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="41d92-384">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41d92-385"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="41d92-385"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

