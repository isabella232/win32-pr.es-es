---
description: Representa una instancia de un componente de extensión enlazado a un conmutador Ethernet virtual.
ms.assetid: 5b3e26e3-4cb9-47c9-865e-2f3232bbfc8e
title: Msvm_EthernetSwitchExtension (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtension
- Msvm_EthernetSwitchExtension.InstanceID
- Msvm_EthernetSwitchExtension.Caption
- Msvm_EthernetSwitchExtension.Description
- Msvm_EthernetSwitchExtension.ElementName
- Msvm_EthernetSwitchExtension.InstallDate
- Msvm_EthernetSwitchExtension.OperationalStatus
- Msvm_EthernetSwitchExtension.StatusDescriptions
- Msvm_EthernetSwitchExtension.Status
- Msvm_EthernetSwitchExtension.HealthState
- Msvm_EthernetSwitchExtension.CommunicationStatus
- Msvm_EthernetSwitchExtension.DetailedStatus
- Msvm_EthernetSwitchExtension.OperatingStatus
- Msvm_EthernetSwitchExtension.PrimaryStatus
- Msvm_EthernetSwitchExtension.EnabledState
- Msvm_EthernetSwitchExtension.OtherEnabledState
- Msvm_EthernetSwitchExtension.RequestedState
- Msvm_EthernetSwitchExtension.EnabledDefault
- Msvm_EthernetSwitchExtension.TimeOfLastStateChange
- Msvm_EthernetSwitchExtension.AvailableRequestedStates
- Msvm_EthernetSwitchExtension.TransitioningToState
- Msvm_EthernetSwitchExtension.SystemCreationClassName
- Msvm_EthernetSwitchExtension.SystemName
- Msvm_EthernetSwitchExtension.CreationClassName
- Msvm_EthernetSwitchExtension.Name
- Msvm_EthernetSwitchExtension.ExtensionType
- Msvm_EthernetSwitchExtension.Vendor
- Msvm_EthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a6d760737ded1a12cf369ccb3a46595627d8e38e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670033"
---
# <a name="msvm_ethernetswitchextension-class"></a><span data-ttu-id="5a12f-103">MSVM \_ EthernetSwitchExtension (clase)</span><span class="sxs-lookup"><span data-stu-id="5a12f-103">Msvm\_EthernetSwitchExtension class</span></span>

<span data-ttu-id="5a12f-104">Representa una instancia de un componente de extensión enlazado a un conmutador Ethernet virtual.</span><span class="sxs-lookup"><span data-stu-id="5a12f-104">Represents an instance of an extension component bound to a virtual Ethernet switch.</span></span>

<span data-ttu-id="5a12f-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5a12f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a12f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a12f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtension : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption = "Virtual Switch Extension";
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
  string   SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string   SystemName;
  string   CreationClassName = "Msvm_EthernetSwitchExtension";
  string   Name;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="5a12f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5a12f-107">Members</span></span>

<span data-ttu-id="5a12f-108">La clase **MSVM \_ EthernetSwitchExtension** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5a12f-108">The **Msvm\_EthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="5a12f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5a12f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="5a12f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5a12f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5a12f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5a12f-111">Methods</span></span>

<span data-ttu-id="5a12f-112">La clase **MSVM \_ EthernetSwitchExtension** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5a12f-112">The **Msvm\_EthernetSwitchExtension** class has these methods.</span></span>



| <span data-ttu-id="5a12f-113">Método</span><span class="sxs-lookup"><span data-stu-id="5a12f-113">Method</span></span>                                                                        | <span data-ttu-id="5a12f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a12f-114">Description</span></span>                         |
|:------------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="5a12f-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="5a12f-115">**RequestStateChange**</span></span>](msvm-ethernetswitchextension-requeststatechange.md) | <span data-ttu-id="5a12f-116">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="5a12f-116">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5a12f-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5a12f-117">Properties</span></span>

<span data-ttu-id="5a12f-118">La clase **MSVM \_ EthernetSwitchExtension** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5a12f-118">The **Msvm\_EthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a12f-119">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="5a12f-119">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-120">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a12f-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-122">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="5a12f-122">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="5a12f-123">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5a12f-123">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="5a12f-124">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="5a12f-124">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="5a12f-125">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="5a12f-125">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="5a12f-126">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5a12f-126">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="5a12f-127"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="5a12f-127"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-128"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5a12f-128"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-129"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="5a12f-129"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-130"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="5a12f-130"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-131"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="5a12f-131"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-132"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="5a12f-132"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-133"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="5a12f-133"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-134"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="5a12f-134"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-135"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="5a12f-135"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-136"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="5a12f-136"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="5a12f-137">)</span><span class="sxs-lookup"><span data-stu-id="5a12f-137">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5a12f-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5a12f-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a12f-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-141">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="5a12f-141">A short description of the object.</span></span> <span data-ttu-id="5a12f-142">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "extensión de conmutador virtual".</span><span class="sxs-lookup"><span data-stu-id="5a12f-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Switch Extension".</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-143">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="5a12f-143">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-144">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a12f-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-146">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="5a12f-146">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="5a12f-147">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="5a12f-147">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5a12f-148">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5a12f-148">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-149">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5a12f-149">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a12f-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-152">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5a12f-152">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-153">Nombre de la clase o subclase que se usa en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="5a12f-153">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="5a12f-154">Esta propiedad siempre se establece en "MSVM \_ EthernetSwitchExtension".</span><span class="sxs-lookup"><span data-stu-id="5a12f-154">This property is always set to "Msvm\_EthernetSwitchExtension".</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-155">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5a12f-155">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a12f-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-158">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="5a12f-158">A description of the object.</span></span> <span data-ttu-id="5a12f-159">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5a12f-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-160">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="5a12f-160">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-161">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a12f-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-163">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="5a12f-163">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="5a12f-164">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="5a12f-164">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5a12f-165">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5a12f-165">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-166">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5a12f-166">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a12f-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-169">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="5a12f-169">A display name for the object.</span></span> <span data-ttu-id="5a12f-170">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5a12f-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-171">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="5a12f-171">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-172">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a12f-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-174">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5a12f-174">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="5a12f-175">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) y tendrá uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5a12f-175">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5a12f-176"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="5a12f-176"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-177"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5a12f-177"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-178"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitada pero sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="5a12f-178"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5a12f-179">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="5a12f-179">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-180">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a12f-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-182">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5a12f-182">The enabled and disabled states of an element.</span></span> <span data-ttu-id="5a12f-183">Esta propiedad también puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="5a12f-183">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="5a12f-184">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5a12f-184">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="5a12f-185">Value</span><span class="sxs-lookup"><span data-stu-id="5a12f-185">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="5a12f-186">Significado</span><span class="sxs-lookup"><span data-stu-id="5a12f-186">Meaning</span></span>                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="5a12f-187"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-187"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 |                                                                                                                                                                                                             |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="5a12f-188"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-188"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                             |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="5a12f-189"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-189"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="5a12f-190">El elemento es o puede ejecutar comandos, procesará cualquier comando en cola y pondrá en cola nuevas solicitudes.</span><span class="sxs-lookup"><span data-stu-id="5a12f-190">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                        |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="5a12f-191"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-191"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="5a12f-192">El elemento no ejecutará comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="5a12f-192">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                            |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="5a12f-193"><dt>**Cerrando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-193"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="5a12f-194">El elemento está en el proceso de pasar a un Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="5a12f-194">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                      |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="5a12f-195"><dt>**No aplicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-195"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="5a12f-196">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="5a12f-196">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                          |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="5a12f-197"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-197"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="5a12f-198">Es posible que el elemento esté completando comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="5a12f-198">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                     |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="5a12f-199"><dt>**En la prueba**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-199"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="5a12f-200">El elemento está en un estado de prueba.</span><span class="sxs-lookup"><span data-stu-id="5a12f-200">The element is in a test state.</span></span><br/>                                                                                                                                                                  |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="5a12f-201"><dt>**Aplazado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-201"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="5a12f-202">Es posible que el elemento esté completando los comandos, pero pondrá en cola todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="5a12f-202">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                    |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="5a12f-203">Modo <dt>**inactivo**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-203"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="5a12f-204">El elemento está habilitado pero en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="5a12f-204">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="5a12f-205">El comportamiento del elemento es similar al estado habilitado, pero solo procesa un conjunto restringido de comandos.</span><span class="sxs-lookup"><span data-stu-id="5a12f-205">The behavior of the element is similar to the Enabled state, but it processes only a restricted set of commands.</span></span> <span data-ttu-id="5a12f-206">Todas las demás solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="5a12f-206">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="5a12f-207"><dt>**Inicio**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-207"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="5a12f-208">El elemento está en proceso de pasar a un estado habilitado.</span><span class="sxs-lookup"><span data-stu-id="5a12f-208">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="5a12f-209">Las nuevas solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="5a12f-209">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="5a12f-210"><dt>**DMTF reservado**</dt> <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-210"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="5a12f-211">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5a12f-211">Reserved.</span></span><br/>                                                                                                                                                                                        |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="5a12f-212"><dt>**Proveedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-212"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="5a12f-213">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5a12f-213">Reserved.</span></span><br/>                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="5a12f-214">**ExtensionType**</span><span class="sxs-lookup"><span data-stu-id="5a12f-214">**ExtensionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-215">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5a12f-215">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-217">Indica el tipo del componente de extensión.</span><span class="sxs-lookup"><span data-stu-id="5a12f-217">Indicates the type of the extension component.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a12f-218">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="5a12f-218">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

<span data-ttu-id="5a12f-219">**Capturar** (1)</span><span class="sxs-lookup"><span data-stu-id="5a12f-219">**Capture** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

<span data-ttu-id="5a12f-220">**Filtrar** (2)</span><span class="sxs-lookup"><span data-stu-id="5a12f-220">**Filter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

<span data-ttu-id="5a12f-221">**Reenvío** (3)</span><span class="sxs-lookup"><span data-stu-id="5a12f-221">**Forwarding** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

<span data-ttu-id="5a12f-222">**Supervisión** (4)</span><span class="sxs-lookup"><span data-stu-id="5a12f-222">**Monitoring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

<span data-ttu-id="5a12f-223">**Nativo** (5)</span><span class="sxs-lookup"><span data-stu-id="5a12f-223">**Native** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a12f-224">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="5a12f-224">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-225">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a12f-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-227">Especifica el estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="5a12f-227">Specifies the current health of the element.</span></span> <span data-ttu-id="5a12f-228">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="5a12f-228">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="5a12f-229">Cuando se produzca un error crítico, compruebe el registro de eventos para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="5a12f-229">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="5a12f-230">La propiedad **EnabledState** también puede contener más información.</span><span class="sxs-lookup"><span data-stu-id="5a12f-230">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="5a12f-231">Por ejemplo, si el espacio en disco es muy bajo, **HealthState** se establece en 25, la máquina virtual se pausa y **EnabledState** se establece en 32768 (en pausa).</span><span class="sxs-lookup"><span data-stu-id="5a12f-231">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="5a12f-232">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5a12f-232">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="5a12f-233">Value</span><span class="sxs-lookup"><span data-stu-id="5a12f-233">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="5a12f-234">Significado</span><span class="sxs-lookup"><span data-stu-id="5a12f-234">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="5a12f-235"><dt>**Aceptar**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-235"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="5a12f-236">El elemento es totalmente funcional y funciona dentro de los parámetros operativos normales y sin errores.</span><span class="sxs-lookup"><span data-stu-id="5a12f-236">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="5a12f-237"><dt>**Error principal**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-237"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="5a12f-238">El elemento ha sufrido un error importante.</span><span class="sxs-lookup"><span data-stu-id="5a12f-238">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="5a12f-239"><dt>**Error crítico**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-239"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="5a12f-240">El elemento no es funcional y es posible que la recuperación no sea posible.</span><span class="sxs-lookup"><span data-stu-id="5a12f-240">The element is nonfunctional, and recovery might not be possible.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="5a12f-241">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5a12f-241">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-242">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5a12f-242">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-244">Fecha y hora en que se creó la configuración de la máquina virtual para una máquina virtual, o **null**, para un sistema operativo de administración.</span><span class="sxs-lookup"><span data-stu-id="5a12f-244">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="5a12f-245">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5a12f-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5a12f-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a12f-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-249">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="5a12f-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-250">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="5a12f-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5a12f-251">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5a12f-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-252">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="5a12f-252">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-253">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a12f-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-255">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5a12f-255">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-256">Nombre único del componente de extensión.</span><span class="sxs-lookup"><span data-stu-id="5a12f-256">The unique name of the extension component.</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-257">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="5a12f-257">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-258">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a12f-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-260">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="5a12f-260">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="5a12f-261">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="5a12f-261">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5a12f-262">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5a12f-262">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-263">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="5a12f-263">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-264">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a12f-264">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-266">Una matriz que contiene los Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="5a12f-266">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="5a12f-267">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5a12f-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-268">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="5a12f-268">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-269">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a12f-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-271">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="5a12f-271">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="5a12f-272">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="5a12f-272">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="5a12f-273">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="5a12f-273">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-274">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="5a12f-274">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-275">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a12f-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-277">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="5a12f-277">Provides high level status information.</span></span> <span data-ttu-id="5a12f-278">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="5a12f-278">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="5a12f-279">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="5a12f-279">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5a12f-280">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5a12f-280">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-281">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="5a12f-281">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-282">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a12f-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-284">Último estado solicitado o deseado del elemento que se pasa al método **RequestStateChange** , o 12 (no aplicable) si no hay ningún cambio de estado en curso.</span><span class="sxs-lookup"><span data-stu-id="5a12f-284">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="5a12f-285">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="5a12f-285">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="5a12f-286">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="5a12f-286">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="5a12f-287">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5a12f-287">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-288">**Estado**</span><span class="sxs-lookup"><span data-stu-id="5a12f-288">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-289">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a12f-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-291">Cadena que especifica el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="5a12f-291">A string that specifies the status of the element.</span></span> <span data-ttu-id="5a12f-292">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5a12f-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-293">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5a12f-293">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-294">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="5a12f-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-296">Calificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="5a12f-296">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-297">Una matriz que contiene cadenas que describen los valores correspondientes de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="5a12f-297">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="5a12f-298">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5a12f-298">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-299">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5a12f-299">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a12f-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-302">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5a12f-302">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-303">Nombre de la clase de creación del sistema.</span><span class="sxs-lookup"><span data-stu-id="5a12f-303">The system creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-304">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5a12f-304">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-305">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a12f-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-307">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5a12f-307">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-308">Nombre del conmutador virtual al que está enlazada la instancia de extensión.</span><span class="sxs-lookup"><span data-stu-id="5a12f-308">The name of the virtual switch to which the extension instance is bound to.</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-309">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="5a12f-309">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-310">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5a12f-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-312">Fecha y hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="5a12f-312">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="5a12f-313">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5a12f-313">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-314">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="5a12f-314">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-315">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a12f-315">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-317">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="5a12f-317">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="5a12f-318">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="5a12f-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-319">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="5a12f-319">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-320">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a12f-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-322">Indica que el proveedor proporciona la extensión.</span><span class="sxs-lookup"><span data-stu-id="5a12f-322">Indicates the vendor providing the extension.</span></span>

</dd> <dt>

<span data-ttu-id="5a12f-323">**Versión**</span><span class="sxs-lookup"><span data-stu-id="5a12f-323">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a12f-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a12f-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a12f-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a12f-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a12f-326">Versión de la extensión en un formato de "*principal*. *secundaria*", por ejemplo" 2,0 ".</span><span class="sxs-lookup"><span data-stu-id="5a12f-326">The version of the extension in a format of "*major*.*minor*", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a12f-327">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a12f-327">Requirements</span></span>



| <span data-ttu-id="5a12f-328">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a12f-328">Requirement</span></span> | <span data-ttu-id="5a12f-329">Value</span><span class="sxs-lookup"><span data-stu-id="5a12f-329">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a12f-330">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a12f-330">Minimum supported client</span></span><br/> | <span data-ttu-id="5a12f-331">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a12f-331">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5a12f-332">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a12f-332">Minimum supported server</span></span><br/> | <span data-ttu-id="5a12f-333">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a12f-333">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5a12f-334">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5a12f-334">Namespace</span></span><br/>                | <span data-ttu-id="5a12f-335">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="5a12f-335">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5a12f-336">MOF</span><span class="sxs-lookup"><span data-stu-id="5a12f-336">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a12f-337"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-337"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a12f-338">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5a12f-338">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a12f-339"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5a12f-339"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

