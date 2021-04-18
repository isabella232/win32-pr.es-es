---
description: Representa el extremo de VLAN de un puerto de conmutador.
ms.assetid: 82F2EC39-0C9C-4A9D-A6C4-1543A62A341D
title: Msvm_VLANEndpoint (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VLANEndpoint
- Msvm_VLANEndpoint.InstanceID
- Msvm_VLANEndpoint.Caption
- Msvm_VLANEndpoint.Description
- Msvm_VLANEndpoint.ElementName
- Msvm_VLANEndpoint.InstallDate
- Msvm_VLANEndpoint.Name
- Msvm_VLANEndpoint.OperationalStatus
- Msvm_VLANEndpoint.StatusDescriptions
- Msvm_VLANEndpoint.Status
- Msvm_VLANEndpoint.HealthState
- Msvm_VLANEndpoint.CommunicationStatus
- Msvm_VLANEndpoint.DetailedStatus
- Msvm_VLANEndpoint.OperatingStatus
- Msvm_VLANEndpoint.PrimaryStatus
- Msvm_VLANEndpoint.EnabledState
- Msvm_VLANEndpoint.OtherEnabledState
- Msvm_VLANEndpoint.RequestedState
- Msvm_VLANEndpoint.EnabledDefault
- Msvm_VLANEndpoint.TimeOfLastStateChange
- Msvm_VLANEndpoint.AvailableRequestedStates
- Msvm_VLANEndpoint.TransitioningToState
- Msvm_VLANEndpoint.SystemCreationClassName
- Msvm_VLANEndpoint.SystemName
- Msvm_VLANEndpoint.CreationClassName
- Msvm_VLANEndpoint.NameFormat
- Msvm_VLANEndpoint.ProtocolType
- Msvm_VLANEndpoint.ProtocolIFType
- Msvm_VLANEndpoint.OtherTypeDescription
- Msvm_VLANEndpoint.DesiredEndpointMode
- Msvm_VLANEndpoint.OtherEndpointMode
- Msvm_VLANEndpoint.OperationalEndpointMode
- Msvm_VLANEndpoint.DesiredVLANTrunkEncapsulation
- Msvm_VLANEndpoint.OtherTrunkEncapsulation
- Msvm_VLANEndpoint.OperationalVLANTrunkEncapsulation
- Msvm_VLANEndpoint.GVRPStatus
- Msvm_VLANEndpoint.SupportedEndpointModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5606e18fd1327f17feaac07570e5bf8c0c8eb59d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666315"
---
# <a name="msvm_vlanendpoint-class"></a><span data-ttu-id="68e0a-103">MSVM \_ VLANEndpoint (clase)</span><span class="sxs-lookup"><span data-stu-id="68e0a-103">Msvm\_VLANEndpoint class</span></span>

<span data-ttu-id="68e0a-104">Representa el extremo de VLAN de un puerto de conmutador.</span><span class="sxs-lookup"><span data-stu-id="68e0a-104">Represents the VLAN endpoint of a switch port.</span></span> <span data-ttu-id="68e0a-105">La configuración de este punto de conexión cambiará la manera en que el puerto del conmutador envía los paquetes de VLAN a través del conmutador.</span><span class="sxs-lookup"><span data-stu-id="68e0a-105">The configuration of this endpoint will change the way the switch port sends VLAN packets through the switch.</span></span>

<span data-ttu-id="68e0a-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="68e0a-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="68e0a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68e0a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VLANEndpoint : CIM_VLANEndpoint
{
  string   InstanceID;
  String   Caption = "VLAN Endpoint";
  string   Description = "Microsoft VLAN Endpoint";
  String   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  String   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualSwitch";
  string   SystemName;
  String   CreationClassName = "Msvm_VLANEndpoint";
  String   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 1;
  String   OtherTypeDescription = "Virtual Ethernet";
  uint16   DesiredEndpointMode;
  string   OtherEndpointMode;
  uint16   OperationalEndpointMode;
  uint16   DesiredVLANTrunkEncapsulation;
  string   OtherTrunkEncapsulation;
  uint16   OperationalVLANTrunkEncapsulation;
  uint16   GVRPStatus;
  uint16   SupportedEndpointModes[];
};
```

## <a name="members"></a><span data-ttu-id="68e0a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="68e0a-108">Members</span></span>

<span data-ttu-id="68e0a-109">La clase **MSVM \_ VLANEndpoint** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="68e0a-109">The **Msvm\_VLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="68e0a-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="68e0a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="68e0a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68e0a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="68e0a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="68e0a-112">Methods</span></span>

<span data-ttu-id="68e0a-113">La clase **MSVM \_ VLANEndpoint** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="68e0a-113">The **Msvm\_VLANEndpoint** class has these methods.</span></span>



| <span data-ttu-id="68e0a-114">Método</span><span class="sxs-lookup"><span data-stu-id="68e0a-114">Method</span></span>                                                             | <span data-ttu-id="68e0a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="68e0a-115">Description</span></span>                         |
|:-------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="68e0a-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="68e0a-116">**RequestStateChange**</span></span>](msvm-vlanendpoint-requeststatechange.md) | <span data-ttu-id="68e0a-117">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="68e0a-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="68e0a-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68e0a-118">Properties</span></span>

<span data-ttu-id="68e0a-119">La clase **MSVM \_ VLANEndpoint** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="68e0a-119">The **Msvm\_VLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68e0a-120">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="68e0a-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-121">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-123">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="68e0a-123">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="68e0a-124">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="68e0a-124">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="68e0a-125">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="68e0a-125">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="68e0a-126">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="68e0a-126">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="68e0a-127">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="68e0a-127">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="68e0a-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="68e0a-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="68e0a-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="68e0a-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="68e0a-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="68e0a-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="68e0a-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="68e0a-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="68e0a-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="68e0a-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="68e0a-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="68e0a-138">)</span><span class="sxs-lookup"><span data-stu-id="68e0a-138">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="68e0a-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="68e0a-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68e0a-140">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-142">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="68e0a-142">A short description of the object.</span></span> <span data-ttu-id="68e0a-143">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "punto de conexión de VLAN".</span><span class="sxs-lookup"><span data-stu-id="68e0a-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "VLAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-144">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="68e0a-144">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-145">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-147">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="68e0a-147">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="68e0a-148">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="68e0a-148">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="68e0a-149">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="68e0a-149">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-150">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="68e0a-150">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68e0a-151">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-153">El nombre de la clase o la subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="68e0a-153">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="68e0a-154">Esta propiedad se hereda de [**CIM \_ punto**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)y siempre se establece en "MSVM \_ VLANEndpoint".</span><span class="sxs-lookup"><span data-stu-id="68e0a-154">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_VLANEndpoint".</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-155">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="68e0a-155">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68e0a-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-158">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="68e0a-158">A description of the object.</span></span> <span data-ttu-id="68e0a-159">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "punto de conexión de VLAN de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="68e0a-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft VLAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-160">**DesiredEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="68e0a-160">**DesiredEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-161">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-162">Tipo de acceso: solo escritura</span><span class="sxs-lookup"><span data-stu-id="68e0a-162">Access type: Write-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-163">Modo VLAN deseado que se solicita para su uso.</span><span class="sxs-lookup"><span data-stu-id="68e0a-163">The desired VLAN mode that is requested for use.</span></span> <span data-ttu-id="68e0a-164">La propiedad **OperationalEndpointMode** proporciona el modo actual.</span><span class="sxs-lookup"><span data-stu-id="68e0a-164">The current mode is given by the **OperationalEndpointMode** property.</span></span> <span data-ttu-id="68e0a-165">Esta propiedad se hereda de [**\_ VLANEndpoint CIM**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="68e0a-165">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>



| <span data-ttu-id="68e0a-166">Value</span><span class="sxs-lookup"><span data-stu-id="68e0a-166">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="68e0a-167">Significado</span><span class="sxs-lookup"><span data-stu-id="68e0a-167">Meaning</span></span>                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="68e0a-168"><dt>**DMTF reservado**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-168"><dt>**DMTF Reserved**</dt> <dt>0</dt></span></span> </dl>                       |                                                                                                                                                                                                                                                                                  |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="68e0a-169"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-169"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                       |                                                                                                                                                                                                                                                                                  |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <span data-ttu-id="68e0a-170"><dt>**Acceso**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-170"><dt>**Access**</dt> <dt>2</dt></span></span> </dl>                                                   | <span data-ttu-id="68e0a-171">Coloca el puerto del punto de conexión o del conmutador en el modo de no troncal permanente y negocia para convertir el vínculo en un vínculo de no tronco.</span><span class="sxs-lookup"><span data-stu-id="68e0a-171">Puts the endpoint/switch port into permanent nontrunking mode and negotiates to convert the link into a nontrunk link.</span></span> <span data-ttu-id="68e0a-172">El punto de conexión se convierte en una interfaz que no es de tronco.</span><span class="sxs-lookup"><span data-stu-id="68e0a-172">The endpoint becomes a nontrunk interface.</span></span><br/>                                                                                                     |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <span data-ttu-id="68e0a-173"><dt>**Dynamic Auto**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-173"><dt>**Dynamic Auto**</dt> <dt>3</dt></span></span> </dl>                           | <span data-ttu-id="68e0a-174">Hace que el punto de conexión sea capaz de convertir el vínculo en un vínculo de tronco.</span><span class="sxs-lookup"><span data-stu-id="68e0a-174">Makes the endpoint able to convert the link to a trunk link.</span></span> <span data-ttu-id="68e0a-175">El punto de conexión se convierte en una interfaz troncal si la interfaz vecina está establecida en el modo troncal o el modo deseado.</span><span class="sxs-lookup"><span data-stu-id="68e0a-175">The endpoint becomes a trunk interface if the neighboring interface is set to trunk or desirable mode.</span></span><br/>                                                                                                   |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <span data-ttu-id="68e0a-176"><dt>**Dinámica deseada**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-176"><dt>**Dynamic Desirable**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="68e0a-177">Hace que el punto de conexión intente convertir activamente el vínculo en un vínculo de tronco.</span><span class="sxs-lookup"><span data-stu-id="68e0a-177">Makes the endpoint actively attempt to convert the link to a trunk link.</span></span> <span data-ttu-id="68e0a-178">El punto de conexión se convierte en una interfaz troncal si la interfaz vecina está establecida en el modo troncal, deseable o auto.</span><span class="sxs-lookup"><span data-stu-id="68e0a-178">The endpoint becomes a trunk interface if the neighboring interface is set to trunk, desirable, or auto mode.</span></span> <span data-ttu-id="68e0a-179">El modo de puerto de conmutador predeterminado para todas las interfaces Ethernet es deseable dinámico.</span><span class="sxs-lookup"><span data-stu-id="68e0a-179">The default switch-port mode for all Ethernet interfaces is dynamic desirable.</span></span><br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <span data-ttu-id="68e0a-180"><dt>**Tronco**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-180"><dt>**Trunk**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="68e0a-181">Pone el extremo en el modo de Troncalización permanente y negocia para convertir el vínculo en un vínculo de tronco.</span><span class="sxs-lookup"><span data-stu-id="68e0a-181">Puts the endpoint into permanent trunking mode and negotiates to convert the link into a trunk link.</span></span> <span data-ttu-id="68e0a-182">El punto de conexión se convierte en una interfaz troncal aunque la interfaz vecina no sea una interfaz troncal.</span><span class="sxs-lookup"><span data-stu-id="68e0a-182">The endpoint becomes a trunk interface even if the neighboring interface is not a trunk interface.</span></span><br/>                                                               |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <span data-ttu-id="68e0a-183"><dt>**Túnel Dot1Q**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-183"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span></span> </dl>                           | <span data-ttu-id="68e0a-184">Configura la interfaz como un punto de conexión (no Troncalización) de túnel o puerto que se va a conectar en un vínculo asimétrico con un puerto de tronco de 802.1 Q.</span><span class="sxs-lookup"><span data-stu-id="68e0a-184">Configures the interface as a tunnel (nontrunking) endpoint/port to be connected in an asymmetric link with an 802.1Q trunk port.</span></span> <span data-ttu-id="68e0a-185">la tunelización de 802.1 q se usa para mantener la integridad de la VLAN del cliente en una red del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="68e0a-185">802.1Q tunneling is used to maintain customer VLAN integrity across a service provider network.</span></span><br/>                                     |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="68e0a-186"><dt>**DMTF reservado**</dt> <dt>7 32767</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-186"><dt>**DMTF Reserved**</dt> <dt>7 32767</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="68e0a-187"><dt> **Proveedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-187"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="68e0a-188">**DesiredVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="68e0a-188">**DesiredVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-189">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-191">El tipo de encapsulación de VLAN que se solicita para su uso.</span><span class="sxs-lookup"><span data-stu-id="68e0a-191">The type of VLAN encapsulation that is requested for use.</span></span> <span data-ttu-id="68e0a-192">La encapsulación actualmente en uso se proporciona mediante la propiedad **OperationalVLANTrunkEncapsulation** .</span><span class="sxs-lookup"><span data-stu-id="68e0a-192">The encapsulation currently in use is given by the **OperationalVLANTrunkEncapsulation** property.</span></span> <span data-ttu-id="68e0a-193">Esta propiedad solo es aplicable cuando el punto de conexión funciona en un modo de Troncalización (consulte la propiedad **OperationalEndpointMode** para obtener más detalles).</span><span class="sxs-lookup"><span data-stu-id="68e0a-193">This property is only applicable when the endpoint is operating in a trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="68e0a-194">Esta propiedad es 2 (no aplicable) (es decir, el punto de conexión nunca se colocará en un modo de enlace troncal), un tipo determinado (802.1 Q o un ISL de Cisco) o 5 (Negotiate) (es decir, el resultado de la negociación entre esta interfaz y su vecino).</span><span class="sxs-lookup"><span data-stu-id="68e0a-194">This property is either 2 (Not Applicable) (that is, the endpoint will never be placed in a trunking mode), a particular type (802.1Q or Cisco ISL), or 5 (Negotiate) (that is, the result of the negotiation between this interface and its neighbor).</span></span> <span data-ttu-id="68e0a-195">El valor 5 (Negotiate) no se permite si el punto de conexión no admite la negociación.</span><span class="sxs-lookup"><span data-stu-id="68e0a-195">The value, 5 (Negotiate) is not allowed if the endpoint does not support negotiation.</span></span> <span data-ttu-id="68e0a-196">Esta capacidad depende del hardware y del proveedor.</span><span class="sxs-lookup"><span data-stu-id="68e0a-196">This capability is hardware and vendor dependent.</span></span> <span data-ttu-id="68e0a-197">Esta propiedad se hereda de [**\_ VLANEndpoint CIM**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="68e0a-197">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="68e0a-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="68e0a-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (0)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="68e0a-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-200"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (2)</span><span class="sxs-lookup"><span data-stu-id="68e0a-200"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-201"><span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="68e0a-201"><span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-202"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**ISL de Cisco** (4)</span><span class="sxs-lookup"><span data-stu-id="68e0a-202"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-203"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (5)</span><span class="sxs-lookup"><span data-stu-id="68e0a-203"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (5)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (6 32767)</span><span class="sxs-lookup"><span data-stu-id="68e0a-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (6 32767)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="68e0a-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="68e0a-206">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="68e0a-206">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-207">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-209">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="68e0a-209">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="68e0a-210">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="68e0a-210">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="68e0a-211">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="68e0a-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-212">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="68e0a-212">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68e0a-213">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-215">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="68e0a-215">A display name for the object.</span></span> <span data-ttu-id="68e0a-216">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="68e0a-216">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-217">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="68e0a-217">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-218">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-220">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="68e0a-220">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="68e0a-221">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="68e0a-221">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-222">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="68e0a-222">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-223">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-225">Estados habilitados y deshabilitados de este elemento.</span><span class="sxs-lookup"><span data-stu-id="68e0a-225">The enabled and disabled states of this element.</span></span> <span data-ttu-id="68e0a-226">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="68e0a-226">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-227">**GVRPStatus**</span><span class="sxs-lookup"><span data-stu-id="68e0a-227">**GVRPStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-228">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-230">Indica si el protocolo de registro de VLAN de GARP (GVRP) está habilitado o deshabilitado en el puerto o extremo de tronco.</span><span class="sxs-lookup"><span data-stu-id="68e0a-230">Indicates whether GARP VLAN Registration Protocol (GVRP) is enabled or disabled on the trunk endpoint/port.</span></span> <span data-ttu-id="68e0a-231">Esta propiedad es 2 (no aplicable) a menos que el punto de conexión admita GVRP.</span><span class="sxs-lookup"><span data-stu-id="68e0a-231">This property is 2 (Not Applicable) unless GVRP is supported by the endpoint.</span></span> <span data-ttu-id="68e0a-232">Esta propiedad solo es aplicable cuando el punto de conexión está funcionando en modo de enlace troncal (consulte la propiedad **OperationalEndpointMode** para obtener más detalles).</span><span class="sxs-lookup"><span data-stu-id="68e0a-232">This property is applicable only when the endpoint is operating in trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="68e0a-233">Esta propiedad se hereda de [**\_ VLANEndpoint CIM**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="68e0a-233">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="68e0a-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="68e0a-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-235"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (2)</span><span class="sxs-lookup"><span data-stu-id="68e0a-235"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-236"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="68e0a-236"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-237"><span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="68e0a-237"><span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Disabled** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="68e0a-238">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="68e0a-238">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-239">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-241">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="68e0a-241">The current health of the element.</span></span> <span data-ttu-id="68e0a-242">Esta propiedad expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="68e0a-242">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="68e0a-243">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="68e0a-243">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="68e0a-244">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="68e0a-244">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-245">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="68e0a-245">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-246">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="68e0a-246">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-248">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="68e0a-248">The date and time when the object was installed.</span></span> <span data-ttu-id="68e0a-249">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="68e0a-249">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-250">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="68e0a-250">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-251">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68e0a-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-253">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="68e0a-253">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-254">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="68e0a-254">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="68e0a-255">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="68e0a-255">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-256">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="68e0a-256">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68e0a-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-259">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="68e0a-259">The label by which the object is known.</span></span> <span data-ttu-id="68e0a-260">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="68e0a-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-261">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="68e0a-261">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-262">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68e0a-262">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-264">La heurística de nomenclatura que se selecciona para asegurarse de que el valor de la propiedad **Name** es único.</span><span class="sxs-lookup"><span data-stu-id="68e0a-264">The naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="68e0a-265">Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="68e0a-265">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-266">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="68e0a-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-267">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-269">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="68e0a-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="68e0a-270">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="68e0a-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="68e0a-271">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="68e0a-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-272">**OperationalEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="68e0a-272">**OperationalEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-273">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-273">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-275">El modo de configuración para el extremo de VLAN.</span><span class="sxs-lookup"><span data-stu-id="68e0a-275">The configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="68e0a-276">Esta propiedad se hereda de [**\_ VLANEndpoint CIM**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="68e0a-276">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>



| <span data-ttu-id="68e0a-277">Value</span><span class="sxs-lookup"><span data-stu-id="68e0a-277">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="68e0a-278">Significado</span><span class="sxs-lookup"><span data-stu-id="68e0a-278">Meaning</span></span>                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="68e0a-279"><dt>**DMTF reservado**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-279"><dt>**DMTF Reserved**</dt> <dt>0</dt></span></span> </dl>                       |                                                                                                                                                                                                                                                                     |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="68e0a-280"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-280"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                       | <span data-ttu-id="68e0a-281">El punto de conexión no es compatible con VLAN.</span><span class="sxs-lookup"><span data-stu-id="68e0a-281">The endpoint is not VLAN aware.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <span data-ttu-id="68e0a-282"><dt>**Acceso**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-282"><dt>**Access**</dt> <dt>2</dt></span></span> </dl>                                                   | <span data-ttu-id="68e0a-283">Pone el extremo en modo de no troncal permanente y negocia para convertir el vínculo en un vínculo de no troncal.</span><span class="sxs-lookup"><span data-stu-id="68e0a-283">Puts the endpoint into permanent nontrunking mode and negotiates to convert the link into a nontrunk link.</span></span> <span data-ttu-id="68e0a-284">El punto de conexión se convierte en una interfaz que no es de tronco.</span><span class="sxs-lookup"><span data-stu-id="68e0a-284">The endpoint becomes a nontrunk interface.</span></span><br/>                                                                                                    |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <span data-ttu-id="68e0a-285"><dt>**Dynamic Auto**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-285"><dt>**Dynamic Auto**</dt> <dt>3</dt></span></span> </dl>                           | <span data-ttu-id="68e0a-286">Hace que el punto de conexión sea capaz de convertir el vínculo en un vínculo de tronco.</span><span class="sxs-lookup"><span data-stu-id="68e0a-286">Makes the endpoint able to convert the link to a trunk link.</span></span> <span data-ttu-id="68e0a-287">El punto de conexión se convierte en una interfaz troncal si la interfaz vecina está establecida en el modo troncal o el modo deseado.</span><span class="sxs-lookup"><span data-stu-id="68e0a-287">The endpoint becomes a trunk interface if the neighboring interface is set to trunk or desirable mode.</span></span><br/>                                                                                      |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <span data-ttu-id="68e0a-288"><dt>**Dinámica deseada**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-288"><dt>**Dynamic Desirable**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="68e0a-289">Hace que el punto de conexión intente convertir activamente el vínculo en un vínculo de tronco.</span><span class="sxs-lookup"><span data-stu-id="68e0a-289">Makes the endpoint actively attempt to convert the link to a trunk link.</span></span> <span data-ttu-id="68e0a-290">El punto de conexión se convierte en una interfaz troncal si la interfaz vecina está establecida en el modo troncal, deseable o auto.</span><span class="sxs-lookup"><span data-stu-id="68e0a-290">The endpoint becomes a trunk interface if the neighboring interface is set to trunk, desirable, or auto mode.</span></span> <span data-ttu-id="68e0a-291">Este es el modo de puerto de conmutador predeterminado para todas las interfaces Ethernet.</span><span class="sxs-lookup"><span data-stu-id="68e0a-291">This is the default switch-port mode for all Ethernet interfaces.</span></span><br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <span data-ttu-id="68e0a-292"><dt>**Tronco**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-292"><dt>**Trunk**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="68e0a-293">Pone el extremo en el modo de Troncalización permanente y negocia para convertir el vínculo en un vínculo de tronco.</span><span class="sxs-lookup"><span data-stu-id="68e0a-293">Puts the endpoint into permanent trunking mode and negotiates to convert the link into a trunk link.</span></span> <span data-ttu-id="68e0a-294">El punto de conexión se convierte en una interfaz troncal aunque la interfaz vecina no sea una interfaz troncal.</span><span class="sxs-lookup"><span data-stu-id="68e0a-294">The endpoint becomes a trunk interface even if the neighboring interface is not a trunk interface.</span></span><br/>                                                  |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <span data-ttu-id="68e0a-295"><dt>**Túnel Dot1Q**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-295"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span></span> </dl>                           | <span data-ttu-id="68e0a-296">Configura la interfaz como un punto de conexión (no Troncalización) de túnel o puerto que se va a conectar en un vínculo asimétrico con un puerto de tronco de 802.1 Q.</span><span class="sxs-lookup"><span data-stu-id="68e0a-296">Configures the interface as a tunnel (nontrunking) endpoint/port to be connected in an asymmetric link with an 802.1Q trunk port.</span></span> <span data-ttu-id="68e0a-297">la tunelización de 802.1 q se usa para mantener la integridad de la VLAN del cliente en una red del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="68e0a-297">802.1Q tunneling is used to maintain customer VLAN integrity across a service provider network.</span></span><br/>                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="68e0a-298"><dt>**DMTF reservado**</dt> <dt>7 32767</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-298"><dt>**DMTF Reserved**</dt> <dt>7 32767</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                     |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="68e0a-299"><dt> **Proveedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-299"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="68e0a-300">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="68e0a-300">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-301">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-301">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-303">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="68e0a-303">The current statuses of the object.</span></span> <span data-ttu-id="68e0a-304">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="68e0a-304">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-305">**OperationalVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="68e0a-305">**OperationalVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-306">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-308">El tipo de encapsulación de VLAN que se usa en un puerto o punto de conexión de tronco.</span><span class="sxs-lookup"><span data-stu-id="68e0a-308">The type of VLAN encapsulation in use on a trunk endpoint/port.</span></span> <span data-ttu-id="68e0a-309">Esta propiedad es 2 (no aplicable) (es decir, el extremo no funciona en el modo de tronco), un tipo determinado (3-802.1 Q o 4-Cisco ISL), 5 (Negotiate) (es decir, los puntos de conexión están negociando el tipo de encapsulación).</span><span class="sxs-lookup"><span data-stu-id="68e0a-309">This property is either 2 (Not Applicable) (that is, the endpoint is not operating in trunking mode), a particular type (3 - 802.1Q or 4 - Cisco ISL), 5 (Negotiate) (that is, the endpoints are negotiating the encapsulation type).</span></span> <span data-ttu-id="68e0a-310">Esta propiedad solo es aplicable cuando el punto de conexión funciona en un modo de Troncalización (consulte la propiedad **OperationalEndpointMode** para obtener más detalles).</span><span class="sxs-lookup"><span data-stu-id="68e0a-310">This property is only applicable when the endpoint is operating in a trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="68e0a-311">Esta propiedad se hereda de [**\_ VLANEndpoint CIM**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="68e0a-311">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="68e0a-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="68e0a-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-313"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="68e0a-313"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-314"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (2)</span><span class="sxs-lookup"><span data-stu-id="68e0a-314"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-315"><span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="68e0a-315"><span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-316"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**ISL de Cisco** (4)</span><span class="sxs-lookup"><span data-stu-id="68e0a-316"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-317"><span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Negociar** (5)</span><span class="sxs-lookup"><span data-stu-id="68e0a-317"><span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Negotiating** (5)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-318"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (6 32767)</span><span class="sxs-lookup"><span data-stu-id="68e0a-318"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (6 32767)</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-319"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="68e0a-319"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="68e0a-320">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="68e0a-320">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-321">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68e0a-321">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-323">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="68e0a-323">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="68e0a-324">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="68e0a-324">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="68e0a-325">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="68e0a-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-326">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="68e0a-326">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-327">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68e0a-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-329">El tipo de modelo de punto de conexión de VLAN que es compatible con este extremo de VLAN, cuando el valor de la propiedad **OperationalEndpointMode** se establece en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="68e0a-329">The type of VLAN endpoint model that is supported by this VLAN endpoint, when the value of the **OperationalEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="68e0a-330">Esta propiedad debe establecerse en **null** cuando la propiedad **OperationalEndpointMode** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="68e0a-330">This property should be set to **Null** when the **OperationalEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="68e0a-331">Esta propiedad se hereda de [**\_ VLANEndpoint CIM**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="68e0a-331">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-332">**OtherTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="68e0a-332">**OtherTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-333">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68e0a-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-335">El tipo de encapsulación de VLAN que es compatible con este extremo de VLAN, cuando el valor de la propiedad **OperationalVLANTrunkEncapsulation** se establece en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="68e0a-335">The type of VLAN encapsulation that is supported by this VLAN endpoint, when the value of the **OperationalVLANTrunkEncapsulation** property is set to 1 (Other).</span></span> <span data-ttu-id="68e0a-336">Esta propiedad debe establecerse en **null** cuando la propiedad de encapsulación deseada es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="68e0a-336">This property should be set to **Null** when the desired encapsulation property is any value other than 1.</span></span> <span data-ttu-id="68e0a-337">Esta propiedad se hereda de [**\_ VLANEndpoint CIM**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="68e0a-337">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-338">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="68e0a-338">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-339">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68e0a-339">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-341">El tipo de extremo de protocolo cuando la propiedad **Type** de esta clase (o cualquiera de sus subclases) está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="68e0a-341">The type of protocol endpoint when the **Type** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="68e0a-342">Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)y siempre se establece en "Ethernet virtual".</span><span class="sxs-lookup"><span data-stu-id="68e0a-342">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is always set to "Virtual Ethernet".</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-343">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="68e0a-343">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-344">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-346">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="68e0a-346">Provides high level status information.</span></span> <span data-ttu-id="68e0a-347">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="68e0a-347">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="68e0a-348">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="68e0a-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="68e0a-349">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="68e0a-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-350">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="68e0a-350">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-351">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-352">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-353">La [MIB ifType de IANA](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="68e0a-353">The [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="68e0a-354">Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)y siempre está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="68e0a-354">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-355">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="68e0a-355">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-356">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-356">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-358">Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="68e0a-358">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-359">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="68e0a-359">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-360">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-362">Último estado solicitado o deseado para el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="68e0a-362">The last requested or desired state for the management service.</span></span> <span data-ttu-id="68e0a-363">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="68e0a-363">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="68e0a-364">Value</span><span class="sxs-lookup"><span data-stu-id="68e0a-364">Value</span></span>                                                                         | <span data-ttu-id="68e0a-365">Significado</span><span class="sxs-lookup"><span data-stu-id="68e0a-365">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="68e0a-366"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-366"><dt>12</dt></span></span> </dl> | <span data-ttu-id="68e0a-367">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="68e0a-367">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="68e0a-368">**Estado**</span><span class="sxs-lookup"><span data-stu-id="68e0a-368">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-369">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68e0a-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-371">Describe el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="68e0a-371">Describes the status of the element.</span></span> <span data-ttu-id="68e0a-372">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="68e0a-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="68e0a-373">ACEPTAR</span><span class="sxs-lookup"><span data-stu-id="68e0a-373">"OK"</span></span>

<span data-ttu-id="68e0a-374">Error</span><span class="sxs-lookup"><span data-stu-id="68e0a-374">"Error"</span></span>

<span data-ttu-id="68e0a-375">Degradado</span><span class="sxs-lookup"><span data-stu-id="68e0a-375">"Degraded"</span></span>

<span data-ttu-id="68e0a-376">Unknown</span><span class="sxs-lookup"><span data-stu-id="68e0a-376">"Unknown"</span></span>

<span data-ttu-id="68e0a-377">"Pred FAIL"</span><span class="sxs-lookup"><span data-stu-id="68e0a-377">"Pred Fail"</span></span>

<span data-ttu-id="68e0a-378">Comenzar</span><span class="sxs-lookup"><span data-stu-id="68e0a-378">"Starting"</span></span>

<span data-ttu-id="68e0a-379">Bloqueo</span><span class="sxs-lookup"><span data-stu-id="68e0a-379">"Stopping"</span></span>

<span data-ttu-id="68e0a-380">Servicio</span><span class="sxs-lookup"><span data-stu-id="68e0a-380">"Service"</span></span>

<span data-ttu-id="68e0a-381">Calca</span><span class="sxs-lookup"><span data-stu-id="68e0a-381">"Stressed"</span></span>

<span data-ttu-id="68e0a-382">"Recover"</span><span class="sxs-lookup"><span data-stu-id="68e0a-382">"NonRecover"</span></span>

<span data-ttu-id="68e0a-383">"Sin contacto"</span><span class="sxs-lookup"><span data-stu-id="68e0a-383">"No Contact"</span></span>

<span data-ttu-id="68e0a-384">"Pérdida de comunicación"</span><span class="sxs-lookup"><span data-stu-id="68e0a-384">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-385">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="68e0a-385">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-386">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="68e0a-386">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-388">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="68e0a-388">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="68e0a-389">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "OK".</span><span class="sxs-lookup"><span data-stu-id="68e0a-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-390">**SupportedEndpointModes**</span><span class="sxs-lookup"><span data-stu-id="68e0a-390">**SupportedEndpointModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-391">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-391">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-392">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-393">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="68e0a-393">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-394">Los modos de extremo admitidos por este puerto.</span><span class="sxs-lookup"><span data-stu-id="68e0a-394">The endpoint modes supported by this port.</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-395">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="68e0a-395">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-396">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68e0a-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-398">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="68e0a-398">The creation class name of the scoping system.</span></span> <span data-ttu-id="68e0a-399">Esta propiedad se hereda de [**CIM \_ punto**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)y siempre se establece en "MSVM \_ VirtualSwitch".</span><span class="sxs-lookup"><span data-stu-id="68e0a-399">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_VirtualSwitch"</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-400">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="68e0a-400">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-401">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68e0a-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-403">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="68e0a-403">The system name of the scoping system.</span></span> <span data-ttu-id="68e0a-404">Esta propiedad se hereda de [**\_ punto CIM**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="68e0a-404">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-405">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="68e0a-405">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-406">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="68e0a-406">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-407">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-408">Fecha y hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="68e0a-408">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="68e0a-409">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se admite.</span><span class="sxs-lookup"><span data-stu-id="68e0a-409">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="68e0a-410">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="68e0a-410">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68e0a-411">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68e0a-411">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68e0a-412">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68e0a-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68e0a-413">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="68e0a-413">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="68e0a-414">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="68e0a-414">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68e0a-415">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68e0a-415">Remarks</span></span>

<span data-ttu-id="68e0a-416">El acceso a la clase **MSVM \_ VLANEndpoint** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="68e0a-416">Access to the **Msvm\_VLANEndpoint** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="68e0a-417">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="68e0a-417">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="68e0a-418">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="68e0a-418">Examples</span></span>

<span data-ttu-id="68e0a-419">Consulte [consultar objetos de red](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="68e0a-419">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68e0a-420">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68e0a-420">Requirements</span></span>



| <span data-ttu-id="68e0a-421">Requisito</span><span class="sxs-lookup"><span data-stu-id="68e0a-421">Requirement</span></span> | <span data-ttu-id="68e0a-422">Value</span><span class="sxs-lookup"><span data-stu-id="68e0a-422">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68e0a-423">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68e0a-423">Minimum supported client</span></span><br/> | <span data-ttu-id="68e0a-424">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="68e0a-424">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="68e0a-425">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68e0a-425">Minimum supported server</span></span><br/> | <span data-ttu-id="68e0a-426">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="68e0a-426">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="68e0a-427">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="68e0a-427">Namespace</span></span><br/>                | <span data-ttu-id="68e0a-428">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="68e0a-428">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="68e0a-429">MOF</span><span class="sxs-lookup"><span data-stu-id="68e0a-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68e0a-430"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-430"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="68e0a-431">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68e0a-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68e0a-432"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="68e0a-432"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="68e0a-433">Vea también</span><span class="sxs-lookup"><span data-stu-id="68e0a-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e0a-434">**\_VLANENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="68e0a-434">**CIM\_VLANEndpoint**</span></span>](cim-vlanendpoint.md)
</dt> <dt>

[<span data-ttu-id="68e0a-435">**\_VLANENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="68e0a-435">**CIM\_VLANEndpoint**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)
</dt> </dl>

 

