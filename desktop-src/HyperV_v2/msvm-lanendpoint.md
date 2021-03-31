---
description: Representa el punto de conexión lógico para un adaptador de red. Cuando el punto de conexión de LAN está conectado a un puerto de conmutador, el adaptador de red conectado al punto de conexión de LAN tiene conectividad de red.
ms.assetid: 68aad05e-64b5-44dc-ab5b-8f3051fa77ca
title: Msvm_LANEndpoint (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LANEndpoint
- Msvm_LANEndpoint.InstanceID
- Msvm_LANEndpoint.Caption
- Msvm_LANEndpoint.Description
- Msvm_LANEndpoint.ElementName
- Msvm_LANEndpoint.InstallDate
- Msvm_LANEndpoint.Name
- Msvm_LANEndpoint.OperationalStatus
- Msvm_LANEndpoint.StatusDescriptions
- Msvm_LANEndpoint.Status
- Msvm_LANEndpoint.HealthState
- Msvm_LANEndpoint.CommunicationStatus
- Msvm_LANEndpoint.DetailedStatus
- Msvm_LANEndpoint.OperatingStatus
- Msvm_LANEndpoint.PrimaryStatus
- Msvm_LANEndpoint.EnabledState
- Msvm_LANEndpoint.OtherEnabledState
- Msvm_LANEndpoint.RequestedState
- Msvm_LANEndpoint.EnabledDefault
- Msvm_LANEndpoint.TimeOfLastStateChange
- Msvm_LANEndpoint.AvailableRequestedStates
- Msvm_LANEndpoint.TransitioningToState
- Msvm_LANEndpoint.SystemCreationClassName
- Msvm_LANEndpoint.SystemName
- Msvm_LANEndpoint.CreationClassName
- Msvm_LANEndpoint.NameFormat
- Msvm_LANEndpoint.ProtocolType
- Msvm_LANEndpoint.ProtocolIFType
- Msvm_LANEndpoint.OtherTypeDescription
- Msvm_LANEndpoint.LANID
- Msvm_LANEndpoint.LANType
- Msvm_LANEndpoint.OtherLANType
- Msvm_LANEndpoint.MACAddress
- Msvm_LANEndpoint.AliasAddresses
- Msvm_LANEndpoint.GroupAddresses
- Msvm_LANEndpoint.MaxDataSize
- Msvm_LANEndpoint.Connected
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7585b92461b435b99a05ed198c4c501e10703439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277053"
---
# <a name="msvm_lanendpoint-class"></a><span data-ttu-id="78413-104">MSVM \_ LANEndpoint (clase)</span><span class="sxs-lookup"><span data-stu-id="78413-104">Msvm\_LANEndpoint class</span></span>

<span data-ttu-id="78413-105">Representa el punto de conexión lógico para un adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="78413-105">Represents the logical connection point for a network adapter.</span></span> <span data-ttu-id="78413-106">Cuando el punto de conexión de LAN está conectado a un puerto de conmutador, el adaptador de red conectado al punto de conexión de LAN tiene conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="78413-106">When the LAN endpoint is connected to a switch port, the network adapter connected to the LAN endpoint has network connectivity.</span></span>

<span data-ttu-id="78413-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="78413-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="78413-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78413-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LANEndpoint : CIM_LANEndpoint
{
  string   InstanceID;
  string   Caption = "LAN Endpoint";
  string   Description = "Microsoft Virtual LAN Endpoint";
  string   ElementName;
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
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_LANEndpoint";
  string   NameFormat = "Microsoft Virtual Device ID";
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
};
```

## <a name="members"></a><span data-ttu-id="78413-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="78413-109">Members</span></span>

<span data-ttu-id="78413-110">La clase **MSVM \_ LANEndpoint** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="78413-110">The **Msvm\_LANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="78413-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="78413-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="78413-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="78413-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="78413-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="78413-113">Methods</span></span>

<span data-ttu-id="78413-114">La clase **MSVM \_ LANEndpoint** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="78413-114">The **Msvm\_LANEndpoint** class has these methods.</span></span>



| <span data-ttu-id="78413-115">Método</span><span class="sxs-lookup"><span data-stu-id="78413-115">Method</span></span>                                                            | <span data-ttu-id="78413-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="78413-116">Description</span></span>                         |
|:------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="78413-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="78413-117">**RequestStateChange**</span></span>](msvm-lanendpoint-requeststatechange.md) | <span data-ttu-id="78413-118">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="78413-118">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="78413-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="78413-119">Properties</span></span>

<span data-ttu-id="78413-120">La clase **MSVM \_ LANEndpoint** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="78413-120">The **Msvm\_LANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78413-121">**AliasAddresses**</span><span class="sxs-lookup"><span data-stu-id="78413-121">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-122">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="78413-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="78413-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-124">Otras direcciones de unidifusión que se pueden usar para comunicarse con el punto de conexión de LAN.</span><span class="sxs-lookup"><span data-stu-id="78413-124">Other unicast addresses that may be used to communicate with the LAN endpoint.</span></span> <span data-ttu-id="78413-125">Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="78413-125">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="78413-126">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="78413-126">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-127">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78413-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="78413-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-129">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="78413-129">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="78413-130">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="78413-130">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="78413-131">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="78413-131">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="78413-132">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="78413-132">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="78413-133">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="78413-133">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="78413-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="78413-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="78413-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="78413-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="78413-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="78413-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="78413-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="78413-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="78413-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="78413-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="78413-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="78413-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="78413-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="78413-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="78413-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="78413-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="78413-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="78413-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="78413-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="78413-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="78413-144">)</span><span class="sxs-lookup"><span data-stu-id="78413-144">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78413-145">**Caption**</span><span class="sxs-lookup"><span data-stu-id="78413-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78413-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78413-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-148">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="78413-148">A short description of the object.</span></span> <span data-ttu-id="78413-149">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "punto de conexión de LAN".</span><span class="sxs-lookup"><span data-stu-id="78413-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "LAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="78413-150">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="78413-150">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-151">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78413-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78413-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-153">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="78413-153">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="78413-154">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="78413-154">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="78413-155">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="78413-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="78413-156">**Conectada**</span><span class="sxs-lookup"><span data-stu-id="78413-156">**Connected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-157">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="78413-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78413-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-159">Esta propiedad se establece en **true** si el punto de conexión de LAN está conectado a un puerto de conmutador.</span><span class="sxs-lookup"><span data-stu-id="78413-159">This property is set to **True** if the LAN endpoint is connected to a switch port.</span></span>

</dd> <dt>

<span data-ttu-id="78413-160">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="78413-160">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78413-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78413-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78413-163">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="78413-163">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="78413-164">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="78413-164">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="78413-165">Esta propiedad se hereda de [**CIM \_ punto**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)y siempre se establece en "MSVM \_ LANEndpoint".</span><span class="sxs-lookup"><span data-stu-id="78413-165">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_LANEndpoint".</span></span>

</dd> <dt>

<span data-ttu-id="78413-166">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="78413-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78413-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78413-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-169">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="78413-169">A description of the object.</span></span> <span data-ttu-id="78413-170">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "punto de conexión de LAN virtual de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="78413-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual LAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="78413-171">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="78413-171">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-172">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78413-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78413-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-174">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="78413-174">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="78413-175">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="78413-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="78413-176">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="78413-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="78413-177">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="78413-177">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78413-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78413-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-180">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="78413-180">A display name for the object.</span></span> <span data-ttu-id="78413-181">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="78413-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="78413-182">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="78413-182">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-183">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78413-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78413-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-185">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="78413-185">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="78413-186">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) y tendrá uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="78413-186">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="78413-187"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="78413-187"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="78413-188"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="78413-188"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="78413-189"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitada pero sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="78413-189"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78413-190">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="78413-190">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-191">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78413-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78413-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-193">Especifica el estado habilitado del sistema planeado.</span><span class="sxs-lookup"><span data-stu-id="78413-193">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="78413-194">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="78413-194">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="78413-195">Value</span><span class="sxs-lookup"><span data-stu-id="78413-195">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="78413-196">Significado</span><span class="sxs-lookup"><span data-stu-id="78413-196">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="78413-197"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="78413-197"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="78413-198">El sistema está desactivado.</span><span class="sxs-lookup"><span data-stu-id="78413-198">The system is turned off.</span></span><br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="78413-199"><dt>**No aplicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="78413-199"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="78413-200">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="78413-200">The element does not support being enabled or disabled.</span></span><br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="78413-201"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="78413-201"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="78413-202">El sistema está habilitado, pero sin conexión.</span><span class="sxs-lookup"><span data-stu-id="78413-202">The system is enabled, but offline.</span></span> <span data-ttu-id="78413-203">Se quitarán las nuevas solicitudes.</span><span class="sxs-lookup"><span data-stu-id="78413-203">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="78413-204">**GroupAddresses**</span><span class="sxs-lookup"><span data-stu-id="78413-204">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-205">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="78413-205">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="78413-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-207">Direcciones de multidifusión a las que el punto de conexión de LAN realiza escuchas.</span><span class="sxs-lookup"><span data-stu-id="78413-207">Multicast addresses to which the LAN endpoint listens.</span></span> <span data-ttu-id="78413-208">Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="78413-208">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="78413-209">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="78413-209">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-210">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78413-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78413-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-212">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="78413-212">The current health of the element.</span></span> <span data-ttu-id="78413-213">Esta propiedad expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="78413-213">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="78413-214">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="78413-214">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="78413-215">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="78413-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="78413-216">Value</span><span class="sxs-lookup"><span data-stu-id="78413-216">Value</span></span>                                                                        | <span data-ttu-id="78413-217">Significado</span><span class="sxs-lookup"><span data-stu-id="78413-217">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="78413-218"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="78413-218"><dt>5</dt></span></span> </dl> | <span data-ttu-id="78413-219">El estado de mantenimiento es normal.</span><span class="sxs-lookup"><span data-stu-id="78413-219">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="78413-220">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="78413-220">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-221">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="78413-221">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="78413-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-223">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="78413-223">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="78413-224">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="78413-224">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="78413-225">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="78413-225">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-226">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78413-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78413-227">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78413-228">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="78413-228">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="78413-229">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="78413-229">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="78413-230">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="78413-230">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="78413-231">**LANID**</span><span class="sxs-lookup"><span data-stu-id="78413-231">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-232">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78413-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78413-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-234">Etiqueta o identificador del segmento de LAN al que está conectado el extremo.</span><span class="sxs-lookup"><span data-stu-id="78413-234">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="78413-235">Si el extremo no está activo o conectado actualmente, o no se conoce esta información, esta propiedad será **null**.</span><span class="sxs-lookup"><span data-stu-id="78413-235">If the endpoint is not currently active/connected, or this information is not known, then this property will be **Null**.</span></span> <span data-ttu-id="78413-236">Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="78413-236">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="78413-237">**LANType**</span><span class="sxs-lookup"><span data-stu-id="78413-237">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-238">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78413-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78413-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-240">Esta propiedad está en desuso en lugar de la propiedad **protocolType** .</span><span class="sxs-lookup"><span data-stu-id="78413-240">This property is deprecated in lieu of the **ProtocolType** property.</span></span> <span data-ttu-id="78413-241">Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="78413-241">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="78413-242">**Mac**</span><span class="sxs-lookup"><span data-stu-id="78413-242">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78413-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78413-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78413-245">Calificadores: **MaxLen** (12)</span><span class="sxs-lookup"><span data-stu-id="78413-245">Qualifiers: **MaxLen** ( 12 )</span></span>
</dt> </dl>

<span data-ttu-id="78413-246">Dirección MAC que se usa en la comunicación con el punto de conexión de LAN.</span><span class="sxs-lookup"><span data-stu-id="78413-246">The MAC address used in communication with the LAN endpoint.</span></span> <span data-ttu-id="78413-247">La dirección MAC tiene el formato de doce dígitos hexadecimales (por ejemplo, "010203040506"), donde cada par representa uno de los seis octetos de la dirección MAC en orden de bits canónico según RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="78413-247">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span> <span data-ttu-id="78413-248">Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="78413-248">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="78413-249">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="78413-249">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-250">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78413-250">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78413-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78413-252">Calificadores: **unidades** ("bits")</span><span class="sxs-lookup"><span data-stu-id="78413-252">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="78413-253">Tamaño máximo, en número de bits, del campo de información que puede ser enviado o recibido por el punto de conexión de LAN.</span><span class="sxs-lookup"><span data-stu-id="78413-253">The largest size, in number of bits, of the information field that may be sent or received by the LAN endpoint.</span></span> <span data-ttu-id="78413-254">Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="78413-254">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="78413-255">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="78413-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-256">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78413-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78413-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-258">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="78413-258">The label by which the object is known.</span></span> <span data-ttu-id="78413-259">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="78413-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="78413-260">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="78413-260">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78413-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78413-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78413-263">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="78413-263">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="78413-264">Contiene la heurística de nomenclatura que se selecciona para asegurarse de que el valor de la propiedad **Name** es único.</span><span class="sxs-lookup"><span data-stu-id="78413-264">Contains the naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="78413-265">Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)y se establece en "ID. de dispositivo virtual de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="78413-265">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is set to "Microsoft Virtual Device ID".</span></span>

</dd> <dt>

<span data-ttu-id="78413-266">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="78413-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-267">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78413-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78413-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-269">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="78413-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="78413-270">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="78413-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="78413-271">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="78413-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="78413-272">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="78413-272">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-273">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78413-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="78413-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-275">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="78413-275">The current statuses of the object.</span></span> <span data-ttu-id="78413-276">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="78413-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="78413-277">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="78413-277">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-278">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78413-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78413-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-280">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="78413-280">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="78413-281">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="78413-281">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="78413-282">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="78413-282">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="78413-283">**OtherLANType**</span><span class="sxs-lookup"><span data-stu-id="78413-283">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-284">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78413-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78413-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-286">Esta propiedad está en desuso en lugar de la propiedad **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="78413-286">This property is deprecated in lieu of the **OtherTypeDescription** property.</span></span> <span data-ttu-id="78413-287">Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="78413-287">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="78413-288">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="78413-288">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-289">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78413-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78413-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78413-291">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="78413-291">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="78413-292">Una cadena que describe el tipo de extremo de protocolo cuando la propiedad **ProtocolIFType** de esta clase (o cualquiera de sus subclases) está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="78413-292">A string that describes the type of protocol endpoint when the **ProtocolIFType** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="78413-293">Esta propiedad debe establecerse en **null** cuando la propiedad **ProtocolIFType** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="78413-293">This property should be set to **Null** when the **ProtocolIFType** property is any value other than 1.</span></span> <span data-ttu-id="78413-294">Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="78413-294">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="78413-295">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="78413-295">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-296">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78413-296">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78413-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-298">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="78413-298">Provides high level status information.</span></span> <span data-ttu-id="78413-299">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="78413-299">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="78413-300">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="78413-300">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="78413-301">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="78413-301">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="78413-302">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="78413-302">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-303">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78413-303">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78413-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-305">La propiedad se utiliza para categorizar y clasificar las instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="78413-305">The property is used to categorize and classify instances of this class.</span></span> <span data-ttu-id="78413-306">Si **ProtocolIFType** se establece en 1 (otro), se debe proporcionar la información de tipo en la propiedad **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="78413-306">If the **ProtocolIFType** is set to 1 (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span> <span data-ttu-id="78413-307">Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="78413-307">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

> [!Note]  
> <span data-ttu-id="78413-308">**ProtocolIFType** es una enumeración que está sincronizada con la [MIB de ifType de IANA](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="78413-308">**ProtocolIFType** is an enumeration that is synchronized with the [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="78413-309">También se incluyen los valores adicionales definidos por DMTF.</span><span class="sxs-lookup"><span data-stu-id="78413-309">Additional values defined by the DMTF are also included.</span></span>

 

<dl> <dt>

<span data-ttu-id="78413-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="78413-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="78413-311"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="78413-311"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="78413-312"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Normal 1822** (2)</span><span class="sxs-lookup"><span data-stu-id="78413-312"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Regular 1822** (2)</span></span>
</dt> <dt>

<span data-ttu-id="78413-313"><span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)</span><span class="sxs-lookup"><span data-stu-id="78413-313"><span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)</span></span>
</dt> <dt>

<span data-ttu-id="78413-314"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X. 25** (4)</span><span class="sxs-lookup"><span data-stu-id="78413-314"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X.25** (4)</span></span>
</dt> <dt>

<span data-ttu-id="78413-315"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X. 25** (5)</span><span class="sxs-lookup"><span data-stu-id="78413-315"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X.25** (5)</span></span>
</dt> <dt>

<span data-ttu-id="78413-316"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**Ethernet CSMA/CD** (6)</span><span class="sxs-lookup"><span data-stu-id="78413-316"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**Ethernet CSMA/CD** (6)</span></span>
</dt> <dt>

<span data-ttu-id="78413-317"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802,3 CSMA/CD** (7)</span><span class="sxs-lookup"><span data-stu-id="78413-317"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802.3 CSMA/CD** (7)</span></span>
</dt> <dt>

<span data-ttu-id="78413-318"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**Bus de token ISO 802,4** (8)</span><span class="sxs-lookup"><span data-stu-id="78413-318"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**ISO 802.4 Token Bus** (8)</span></span>
</dt> <dt>

<span data-ttu-id="78413-319"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**Token ring ISO 802,5** (9)</span><span class="sxs-lookup"><span data-stu-id="78413-319"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**ISO 802.5 Token Ring** (9)</span></span>
</dt> <dt>

<span data-ttu-id="78413-320"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802,6 Man** (10)</span><span class="sxs-lookup"><span data-stu-id="78413-320"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802.6 MAN** (10)</span></span>
</dt> <dt>

<span data-ttu-id="78413-321"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11)</span><span class="sxs-lookup"><span data-stu-id="78413-321"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11)</span></span>
</dt> <dt>

<span data-ttu-id="78413-322"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10mbit** (12)</span><span class="sxs-lookup"><span data-stu-id="78413-322"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10Mbit** (12)</span></span>
</dt> <dt>

<span data-ttu-id="78413-323"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13)</span><span class="sxs-lookup"><span data-stu-id="78413-323"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13)</span></span>
</dt> <dt>

<span data-ttu-id="78413-324"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**HyperChannel** (14)</span><span class="sxs-lookup"><span data-stu-id="78413-324"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**HyperChannel** (14)</span></span>
</dt> <dt>

<span data-ttu-id="78413-325"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)</span><span class="sxs-lookup"><span data-stu-id="78413-325"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)</span></span>
</dt> <dt>

<span data-ttu-id="78413-326"><span id="LAP-B"></span><span id="lap-b"></span>**LAP-B** (16)</span><span class="sxs-lookup"><span data-stu-id="78413-326"><span id="LAP-B"></span><span id="lap-b"></span>**LAP-B** (16)</span></span>
</dt> <dt>

<span data-ttu-id="78413-327"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)</span><span class="sxs-lookup"><span data-stu-id="78413-327"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)</span></span>
</dt> <dt>

<span data-ttu-id="78413-328"><span id="DS1"></span><span id="ds1"></span>**DS1** (18)</span><span class="sxs-lookup"><span data-stu-id="78413-328"><span id="DS1"></span><span id="ds1"></span>**DS1** (18)</span></span>
</dt> <dt>

<span data-ttu-id="78413-329"><span id="E1"></span><span id="e1"></span>**E1** (19)</span><span class="sxs-lookup"><span data-stu-id="78413-329"><span id="E1"></span><span id="e1"></span>**E1** (19)</span></span>
</dt> <dt>

<span data-ttu-id="78413-330"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**ISDN básico** (20)</span><span class="sxs-lookup"><span data-stu-id="78413-330"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**Basic ISDN** (20)</span></span>
</dt> <dt>

<span data-ttu-id="78413-331"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**ISDN principal** (21)</span><span class="sxs-lookup"><span data-stu-id="78413-331"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**Primary ISDN** (21)</span></span>
</dt> <dt>

<span data-ttu-id="78413-332"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Serie punto a punto de propiedad** (22)</span><span class="sxs-lookup"><span data-stu-id="78413-332"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Proprietary Point-to-Point Serial** (22)</span></span>
</dt> <dt>

<span data-ttu-id="78413-333"><span id="PPP"></span><span id="ppp"></span>**PPP** (23)</span><span class="sxs-lookup"><span data-stu-id="78413-333"><span id="PPP"></span><span id="ppp"></span>**PPP** (23)</span></span>
</dt> <dt>

<span data-ttu-id="78413-334"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Bucle invertido de software** (24)</span><span class="sxs-lookup"><span data-stu-id="78413-334"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Software Loopback** (24)</span></span>
</dt> <dt>

<span data-ttu-id="78413-335"><span id="EON"></span><span id="eon"></span>**EON** (25)</span><span class="sxs-lookup"><span data-stu-id="78413-335"><span id="EON"></span><span id="eon"></span>**EON** (25)</span></span>
</dt> <dt>

<span data-ttu-id="78413-336"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26)</span><span class="sxs-lookup"><span data-stu-id="78413-336"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="78413-337"><span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)</span><span class="sxs-lookup"><span data-stu-id="78413-337"><span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)</span></span>
</dt> <dt>

<span data-ttu-id="78413-338"><span id="SLIP"></span><span id="slip"></span>**Slip** (28)</span><span class="sxs-lookup"><span data-stu-id="78413-338"><span id="SLIP"></span><span id="slip"></span>**SLIP** (28)</span></span>
</dt> <dt>

<span data-ttu-id="78413-339"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)</span><span class="sxs-lookup"><span data-stu-id="78413-339"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)</span></span>
</dt> <dt>

<span data-ttu-id="78413-340"><span id="DS3"></span><span id="ds3"></span>**DS3** (30)</span><span class="sxs-lookup"><span data-stu-id="78413-340"><span id="DS3"></span><span id="ds3"></span>**DS3** (30)</span></span>
</dt> <dt>

<span data-ttu-id="78413-341"><span id="SIP"></span><span id="sip"></span>**SIP** (31)</span><span class="sxs-lookup"><span data-stu-id="78413-341"><span id="SIP"></span><span id="sip"></span>**SIP** (31)</span></span>
</dt> <dt>

<span data-ttu-id="78413-342"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (32)</span><span class="sxs-lookup"><span data-stu-id="78413-342"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (32)</span></span>
</dt> <dt>

<span data-ttu-id="78413-343"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)</span><span class="sxs-lookup"><span data-stu-id="78413-343"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)</span></span>
</dt> <dt>

<span data-ttu-id="78413-344"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Parallel** (34)</span><span class="sxs-lookup"><span data-stu-id="78413-344"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Parallel** (34)</span></span>
</dt> <dt>

<span data-ttu-id="78413-345"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNET** (35)</span><span class="sxs-lookup"><span data-stu-id="78413-345"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNet** (35)</span></span>
</dt> <dt>

<span data-ttu-id="78413-346"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNET Plus** (36)</span><span class="sxs-lookup"><span data-stu-id="78413-346"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNet Plus** (36)</span></span>
</dt> <dt>

<span data-ttu-id="78413-347"><span id="ATM"></span><span id="atm"></span>**ATM** (37)</span><span class="sxs-lookup"><span data-stu-id="78413-347"><span id="ATM"></span><span id="atm"></span>**ATM** (37)</span></span>
</dt> <dt>

<span data-ttu-id="78413-348"><span id="MIO_X.25"></span><span id="mio_x.25"></span>**Mio X. 25** (38)</span><span class="sxs-lookup"><span data-stu-id="78413-348"><span id="MIO_X.25"></span><span id="mio_x.25"></span>**MIO X.25** (38)</span></span>
</dt> <dt>

<span data-ttu-id="78413-349"><span id="SONET"></span><span id="sonet"></span>**SONET** (39)</span><span class="sxs-lookup"><span data-stu-id="78413-349"><span id="SONET"></span><span id="sonet"></span>**SONET** (39)</span></span>
</dt> <dt>

<span data-ttu-id="78413-350"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**X. 25 ntaje** (40)</span><span class="sxs-lookup"><span data-stu-id="78413-350"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**X.25 PLE** (40)</span></span>
</dt> <dt>

<span data-ttu-id="78413-351"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211 c** (41)</span><span class="sxs-lookup"><span data-stu-id="78413-351"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211c** (41)</span></span>
</dt> <dt>

<span data-ttu-id="78413-352"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)</span><span class="sxs-lookup"><span data-stu-id="78413-352"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)</span></span>
</dt> <dt>

<span data-ttu-id="78413-353"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXi** (43)</span><span class="sxs-lookup"><span data-stu-id="78413-353"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXI** (43)</span></span>
</dt> <dt>

<span data-ttu-id="78413-354"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Servicio Frame Relay** (44)</span><span class="sxs-lookup"><span data-stu-id="78413-354"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Frame Relay Service** (44)</span></span>
</dt> <dt>

<span data-ttu-id="78413-355"><span id="V.35"></span><span id="v.35"></span>**V. 35** (45)</span><span class="sxs-lookup"><span data-stu-id="78413-355"><span id="V.35"></span><span id="v.35"></span>**V.35** (45)</span></span>
</dt> <dt>

<span data-ttu-id="78413-356"><span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)</span><span class="sxs-lookup"><span data-stu-id="78413-356"><span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)</span></span>
</dt> <dt>

<span data-ttu-id="78413-357"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (47)</span><span class="sxs-lookup"><span data-stu-id="78413-357"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (47)</span></span>
</dt> <dt>

<span data-ttu-id="78413-358"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Módem** (48)</span><span class="sxs-lookup"><span data-stu-id="78413-358"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Modem** (48)</span></span>
</dt> <dt>

<span data-ttu-id="78413-359"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)</span><span class="sxs-lookup"><span data-stu-id="78413-359"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)</span></span>
</dt> <dt>

<span data-ttu-id="78413-360"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**Ruta de acceso Sonet** (50)</span><span class="sxs-lookup"><span data-stu-id="78413-360"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**SONET Path** (50)</span></span>
</dt> <dt>

<span data-ttu-id="78413-361"><span id="SONET_VT"></span><span id="sonet_vt"></span>**VT de SONET** (51)</span><span class="sxs-lookup"><span data-stu-id="78413-361"><span id="SONET_VT"></span><span id="sonet_vt"></span>**SONET VT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="78413-362"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)</span><span class="sxs-lookup"><span data-stu-id="78413-362"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)</span></span>
</dt> <dt>

<span data-ttu-id="78413-363"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Propietario virtual/interno** (53)</span><span class="sxs-lookup"><span data-stu-id="78413-363"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Proprietary Virtual/Internal** (53)</span></span>
</dt> <dt>

<span data-ttu-id="78413-364"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Multiplexor propietario** (54)</span><span class="sxs-lookup"><span data-stu-id="78413-364"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Proprietary Multiplexor** (54)</span></span>
</dt> <dt>

<span data-ttu-id="78413-365"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802,12** (55)</span><span class="sxs-lookup"><span data-stu-id="78413-365"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802.12** (55)</span></span>
</dt> <dt>

<span data-ttu-id="78413-366"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Canal de fibra** (56)</span><span class="sxs-lookup"><span data-stu-id="78413-366"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)</span></span>
</dt> <dt>

<span data-ttu-id="78413-367"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**Interfaz HIPPI** (57)</span><span class="sxs-lookup"><span data-stu-id="78413-367"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**HIPPI Interface** (57)</span></span>
</dt> <dt>

<span data-ttu-id="78413-368"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Interconexión de Frame Relay** (58)</span><span class="sxs-lookup"><span data-stu-id="78413-368"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Frame Relay Interconnect** (58)</span></span>
</dt> <dt>

<span data-ttu-id="78413-369"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**LAN emulada ATM para 802,3** (59)</span><span class="sxs-lookup"><span data-stu-id="78413-369"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**ATM Emulated LAN for 802.3** (59)</span></span>
</dt> <dt>

<span data-ttu-id="78413-370"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**LAN emulada ATM para 802,5** (60)</span><span class="sxs-lookup"><span data-stu-id="78413-370"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**ATM Emulated LAN for 802.5** (60)</span></span>
</dt> <dt>

<span data-ttu-id="78413-371"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**Circuito emulado ATM** (61)</span><span class="sxs-lookup"><span data-stu-id="78413-371"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**ATM Emulated Circuit** (61)</span></span>
</dt> <dt>

<span data-ttu-id="78413-372"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Fast Ethernet (100BaseT)** (62)</span><span class="sxs-lookup"><span data-stu-id="78413-372"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Fast Ethernet (100BaseT)** (62)</span></span>
</dt> <dt>

<span data-ttu-id="78413-373"><span id="ISDN"></span><span id="isdn"></span>**ISDN (RDSI** ) (63)</span><span class="sxs-lookup"><span data-stu-id="78413-373"><span id="ISDN"></span><span id="isdn"></span>**ISDN** (63)</span></span>
</dt> <dt>

<span data-ttu-id="78413-374"><span id="V.11"></span><span id="v.11"></span>**V. 11** (64)</span><span class="sxs-lookup"><span data-stu-id="78413-374"><span id="V.11"></span><span id="v.11"></span>**V.11** (64)</span></span>
</dt> <dt>

<span data-ttu-id="78413-375"><span id="V.36"></span><span id="v.36"></span>**V. 36** (65)</span><span class="sxs-lookup"><span data-stu-id="78413-375"><span id="V.36"></span><span id="v.36"></span>**V.36** (65)</span></span>
</dt> <dt>

<span data-ttu-id="78413-376"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 en 64k** (66)</span><span class="sxs-lookup"><span data-stu-id="78413-376"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 at 64K** (66)</span></span>
</dt> <dt>

<span data-ttu-id="78413-377"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 a 2 MB** (67)</span><span class="sxs-lookup"><span data-stu-id="78413-377"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 at 2Mb** (67)</span></span>
</dt> <dt>

<span data-ttu-id="78413-378"><span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)</span><span class="sxs-lookup"><span data-stu-id="78413-378"><span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)</span></span>
</dt> <dt>

<span data-ttu-id="78413-379"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)</span><span class="sxs-lookup"><span data-stu-id="78413-379"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)</span></span>
</dt> <dt>

<span data-ttu-id="78413-380"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Canal** (70)</span><span class="sxs-lookup"><span data-stu-id="78413-380"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Channel** (70)</span></span>
</dt> <dt>

<span data-ttu-id="78413-381"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="78413-381"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)</span></span>
</dt> <dt>

<span data-ttu-id="78413-382"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**Canal IBM 260/370 OEMI** (72)</span><span class="sxs-lookup"><span data-stu-id="78413-382"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**IBM 260/370 OEMI Channel** (72)</span></span>
</dt> <dt>

<span data-ttu-id="78413-383"><span id="ESCON"></span><span id="escon"></span>**ESCON** (73)</span><span class="sxs-lookup"><span data-stu-id="78413-383"><span id="ESCON"></span><span id="escon"></span>**ESCON** (73)</span></span>
</dt> <dt>

<span data-ttu-id="78413-384"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Conmutación de vínculos de datos** (74)</span><span class="sxs-lookup"><span data-stu-id="78413-384"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Data Link Switching** (74)</span></span>
</dt> <dt>

<span data-ttu-id="78413-385"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**Interfaz ISDN S/T** (75)</span><span class="sxs-lookup"><span data-stu-id="78413-385"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**ISDN S/T Interface** (75)</span></span>
</dt> <dt>

<span data-ttu-id="78413-386"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**Interfaz U ISDN** (76)</span><span class="sxs-lookup"><span data-stu-id="78413-386"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**ISDN U Interface** (76)</span></span>
</dt> <dt>

<span data-ttu-id="78413-387"><span id="LAP-D"></span><span id="lap-d"></span>**LAP-D** (77)</span><span class="sxs-lookup"><span data-stu-id="78413-387"><span id="LAP-D"></span><span id="lap-d"></span>**LAP-D** (77)</span></span>
</dt> <dt>

<span data-ttu-id="78413-388"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**Conmutador IP** (78)</span><span class="sxs-lookup"><span data-stu-id="78413-388"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**IP Switch** (78)</span></span>
</dt> <dt>

<span data-ttu-id="78413-389"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Puente de enrutamiento de origen remoto** (79)</span><span class="sxs-lookup"><span data-stu-id="78413-389"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Remote Source Route Bridging** (79)</span></span>
</dt> <dt>

<span data-ttu-id="78413-390"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM lógica** (80)</span><span class="sxs-lookup"><span data-stu-id="78413-390"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM Logical** (80)</span></span>
</dt> <dt>

<span data-ttu-id="78413-391"><span id="DS0"></span><span id="ds0"></span>**DS0** (81)</span><span class="sxs-lookup"><span data-stu-id="78413-391"><span id="DS0"></span><span id="ds0"></span>**DS0** (81)</span></span>
</dt> <dt>

<span data-ttu-id="78413-392"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**Agrupación de DS0** (82)</span><span class="sxs-lookup"><span data-stu-id="78413-392"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**DS0 Bundle** (82)</span></span>
</dt> <dt>

<span data-ttu-id="78413-393"><span id="BSC"></span><span id="bsc"></span>**BSC** (83)</span><span class="sxs-lookup"><span data-stu-id="78413-393"><span id="BSC"></span><span id="bsc"></span>**BSC** (83)</span></span>
</dt> <dt>

<span data-ttu-id="78413-394"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)</span><span class="sxs-lookup"><span data-stu-id="78413-394"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)</span></span>
</dt> <dt>

<span data-ttu-id="78413-395"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Combat net radio** (85)</span><span class="sxs-lookup"><span data-stu-id="78413-395"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Combat Net Radio** (85)</span></span>
</dt> <dt>

<span data-ttu-id="78413-396"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>Con **ISO 802.5 r DTR** (86)</span><span class="sxs-lookup"><span data-stu-id="78413-396"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5r DTR** (86)</span></span>
</dt> <dt>

<span data-ttu-id="78413-397"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Sistema de informes ext pos Loc** (87)</span><span class="sxs-lookup"><span data-stu-id="78413-397"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Ext Pos Loc Report System** (87)</span></span>
</dt> <dt>

<span data-ttu-id="78413-398"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**Protocolo de acceso remoto AppleTalk** (88)</span><span class="sxs-lookup"><span data-stu-id="78413-398"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**AppleTalk Remote Access Protocol** (88)</span></span>
</dt> <dt>

<span data-ttu-id="78413-399"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**Sin conexión propietaria** (89)</span><span class="sxs-lookup"><span data-stu-id="78413-399"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**Proprietary Connectionless** (89)</span></span>
</dt> <dt>

<span data-ttu-id="78413-400"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**Controladora de host ITU X. 29** (90)</span><span class="sxs-lookup"><span data-stu-id="78413-400"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**ITU X.29 Host PAD** (90)</span></span>
</dt> <dt>

<span data-ttu-id="78413-401"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**Pad de terminal X. 3 de ITU** (91)</span><span class="sxs-lookup"><span data-stu-id="78413-401"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**ITU X.3 Terminal PAD** (91)</span></span>
</dt> <dt>

<span data-ttu-id="78413-402"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**MPI Frame Relay** (92)</span><span class="sxs-lookup"><span data-stu-id="78413-402"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**Frame Relay MPI** (92)</span></span>
</dt> <dt>

<span data-ttu-id="78413-403"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X. 213** (93)</span><span class="sxs-lookup"><span data-stu-id="78413-403"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X.213** (93)</span></span>
</dt> <dt>

<span data-ttu-id="78413-404"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)</span><span class="sxs-lookup"><span data-stu-id="78413-404"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)</span></span>
</dt> <dt>

<span data-ttu-id="78413-405"><span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)</span><span class="sxs-lookup"><span data-stu-id="78413-405"><span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)</span></span>
</dt> <dt>

<span data-ttu-id="78413-406"><span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)</span><span class="sxs-lookup"><span data-stu-id="78413-406"><span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)</span></span>
</dt> <dt>

<span data-ttu-id="78413-407"><span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)</span><span class="sxs-lookup"><span data-stu-id="78413-407"><span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)</span></span>
</dt> <dt>

<span data-ttu-id="78413-408"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802,5 CRFP** (98)</span><span class="sxs-lookup"><span data-stu-id="78413-408"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802.5 CRFP** (98)</span></span>
</dt> <dt>

<span data-ttu-id="78413-409"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99)</span><span class="sxs-lookup"><span data-stu-id="78413-409"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99)</span></span>
</dt> <dt>

<span data-ttu-id="78413-410"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Recepción y transmisión de voz** (100)</span><span class="sxs-lookup"><span data-stu-id="78413-410"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Voice Receive and Transmit** (100)</span></span>
</dt> <dt>

<span data-ttu-id="78413-411"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Oficina de intercambio de voz extranjera** (101)</span><span class="sxs-lookup"><span data-stu-id="78413-411"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Voice Foreign Exchange Office** (101)</span></span>
</dt> <dt>

<span data-ttu-id="78413-412"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Servicio de intercambio de voz externa** (102)</span><span class="sxs-lookup"><span data-stu-id="78413-412"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Voice Foreign Exchange Service** (102)</span></span>
</dt> <dt>

<span data-ttu-id="78413-413"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Encapsulación de voz** (103)</span><span class="sxs-lookup"><span data-stu-id="78413-413"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Voice Encapsulation** (103)</span></span>
</dt> <dt>

<span data-ttu-id="78413-414"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voz sobre IP** (104)</span><span class="sxs-lookup"><span data-stu-id="78413-414"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voice over IP** (104)</span></span>
</dt> <dt>

<span data-ttu-id="78413-415"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**ATM DXi** (105)</span><span class="sxs-lookup"><span data-stu-id="78413-415"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**ATM DXI** (105)</span></span>
</dt> <dt>

<span data-ttu-id="78413-416"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**ATM Funi** (106)</span><span class="sxs-lookup"><span data-stu-id="78413-416"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**ATM FUNI** (106)</span></span>
</dt> <dt>

<span data-ttu-id="78413-417"><span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM IMA** (107)</span><span class="sxs-lookup"><span data-stu-id="78413-417"><span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM IMA** (107)</span></span>
</dt> <dt>

<span data-ttu-id="78413-418"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**Paquete Multilink de PPP** (108)</span><span class="sxs-lookup"><span data-stu-id="78413-418"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**PPP Multilink Bundle** (108)</span></span>
</dt> <dt>

<span data-ttu-id="78413-419"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP sobre CDLC** (109)</span><span class="sxs-lookup"><span data-stu-id="78413-419"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP over CDLC** (109)</span></span>
</dt> <dt>

<span data-ttu-id="78413-420"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP a través de garra** (110)</span><span class="sxs-lookup"><span data-stu-id="78413-420"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP over CLAW** (110)</span></span>
</dt> <dt>

<span data-ttu-id="78413-421"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Pila a pila** (111)</span><span class="sxs-lookup"><span data-stu-id="78413-421"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Stack to Stack** (111)</span></span>
</dt> <dt>

<span data-ttu-id="78413-422"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Dirección IP virtual** (112)</span><span class="sxs-lookup"><span data-stu-id="78413-422"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Virtual IP Address** (112)</span></span>
</dt> <dt>

<span data-ttu-id="78413-423"><span id="MPC"></span><span id="mpc"></span>**MPC** (113)</span><span class="sxs-lookup"><span data-stu-id="78413-423"><span id="MPC"></span><span id="mpc"></span>**MPC** (113)</span></span>
</dt> <dt>

<span data-ttu-id="78413-424"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP sobre ATM** (114)</span><span class="sxs-lookup"><span data-stu-id="78413-424"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP over ATM** (114)</span></span>
</dt> <dt>

<span data-ttu-id="78413-425"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**ISO 802.5** (115)</span><span class="sxs-lookup"><span data-stu-id="78413-425"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**ISO 802.5j Fibre Token Ring** (115)</span></span>
</dt> <dt>

<span data-ttu-id="78413-426"><span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116)</span><span class="sxs-lookup"><span data-stu-id="78413-426"><span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116)</span></span>
</dt> <dt>

<span data-ttu-id="78413-427"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit Ethernet** (117)</span><span class="sxs-lookup"><span data-stu-id="78413-427"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit Ethernet** (117)</span></span>
</dt> <dt>

<span data-ttu-id="78413-428"><span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)</span><span class="sxs-lookup"><span data-stu-id="78413-428"><span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)</span></span>
</dt> <dt>

<span data-ttu-id="78413-429"><span id="LAP-F"></span><span id="lap-f"></span>**LAP-F** (119)</span><span class="sxs-lookup"><span data-stu-id="78413-429"><span id="LAP-F"></span><span id="lap-f"></span>**LAP-F** (119)</span></span>
</dt> <dt>

<span data-ttu-id="78413-430"><span id="V.37"></span><span id="v.37"></span>**V. 37** (120)</span><span class="sxs-lookup"><span data-stu-id="78413-430"><span id="V.37"></span><span id="v.37"></span>**V.37** (120)</span></span>
</dt> <dt>

<span data-ttu-id="78413-431"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X. 25 MLP** (121)</span><span class="sxs-lookup"><span data-stu-id="78413-431"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X.25 MLP** (121)</span></span>
</dt> <dt>

<span data-ttu-id="78413-432"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**Grupo de captura X. 25** (122)</span><span class="sxs-lookup"><span data-stu-id="78413-432"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**X.25 Hunt Group** (122)</span></span>
</dt> <dt>

<span data-ttu-id="78413-433"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Transp HDLC** (123)</span><span class="sxs-lookup"><span data-stu-id="78413-433"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Transp HDLC** (123)</span></span>
</dt> <dt>

<span data-ttu-id="78413-434"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Canal de intercalación** (124)</span><span class="sxs-lookup"><span data-stu-id="78413-434"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Interleave Channel** (124)</span></span>
</dt> <dt>

<span data-ttu-id="78413-435"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**Canal rápido** (125)</span><span class="sxs-lookup"><span data-stu-id="78413-435"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**FAST Channel** (125)</span></span>
</dt> <dt>

<span data-ttu-id="78413-436"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (para APPN HPR en redes IP)** (126)</span><span class="sxs-lookup"><span data-stu-id="78413-436"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (for APPN HPR in IP Networks)** (126)</span></span>
</dt> <dt>

<span data-ttu-id="78413-437"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**Capa de Mac CATV** (127)</span><span class="sxs-lookup"><span data-stu-id="78413-437"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**CATV MAC Layer** (127)</span></span>
</dt> <dt>

<span data-ttu-id="78413-438"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV downstream** (128)</span><span class="sxs-lookup"><span data-stu-id="78413-438"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV Downstream** (128)</span></span>
</dt> <dt>

<span data-ttu-id="78413-439"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV ascendente** (129)</span><span class="sxs-lookup"><span data-stu-id="78413-439"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV Upstream** (129)</span></span>
</dt> <dt>

<span data-ttu-id="78413-440"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Conmutador 12MPP de Avalon** (130)</span><span class="sxs-lookup"><span data-stu-id="78413-440"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Avalon 12MPP Switch** (130)</span></span>
</dt> <dt>

<span data-ttu-id="78413-441"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Túnel** (131)</span><span class="sxs-lookup"><span data-stu-id="78413-441"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Tunnel** (131)</span></span>
</dt> <dt>

<span data-ttu-id="78413-442"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Café** (132)</span><span class="sxs-lookup"><span data-stu-id="78413-442"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Coffee** (132)</span></span>
</dt> <dt>

<span data-ttu-id="78413-443"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Servicio de emulación de circuito** (133)</span><span class="sxs-lookup"><span data-stu-id="78413-443"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Circuit Emulation Service** (133)</span></span>
</dt> <dt>

<span data-ttu-id="78413-444"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**Subinterfaz ATM** (134)</span><span class="sxs-lookup"><span data-stu-id="78413-444"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**ATM SubInterface** (134)</span></span>
</dt> <dt>

<span data-ttu-id="78413-445"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**VLAN de nivel 2 mediante 802.1 q** (135)</span><span class="sxs-lookup"><span data-stu-id="78413-445"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**Layer 2 VLAN using 802.1Q** (135)</span></span>
</dt> <dt>

<span data-ttu-id="78413-446"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**VLAN de nivel 3 con IP** (136)</span><span class="sxs-lookup"><span data-stu-id="78413-446"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**Layer 3 VLAN using IP** (136)</span></span>
</dt> <dt>

<span data-ttu-id="78413-447"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**VLAN de nivel 3 con IPX** (137)</span><span class="sxs-lookup"><span data-stu-id="78413-447"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**Layer 3 VLAN using IPX** (137)</span></span>
</dt> <dt>

<span data-ttu-id="78413-448"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Línea de alimentación digital** (138)</span><span class="sxs-lookup"><span data-stu-id="78413-448"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Digital Power Line** (138)</span></span>
</dt> <dt>

<span data-ttu-id="78413-449"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Correo multimedia a través de IP** (139)</span><span class="sxs-lookup"><span data-stu-id="78413-449"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Multimedia Mail over IP** (139)</span></span>
</dt> <dt>

<span data-ttu-id="78413-450"><span id="DTM"></span><span id="dtm"></span>**DTM** (140)</span><span class="sxs-lookup"><span data-stu-id="78413-450"><span id="DTM"></span><span id="dtm"></span>**DTM** (140)</span></span>
</dt> <dt>

<span data-ttu-id="78413-451"><span id="DCN"></span><span id="dcn"></span>**DCN** (141)</span><span class="sxs-lookup"><span data-stu-id="78413-451"><span id="DCN"></span><span id="dcn"></span>**DCN** (141)</span></span>
</dt> <dt>

<span data-ttu-id="78413-452"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**Reenvío IP** (142)</span><span class="sxs-lookup"><span data-stu-id="78413-452"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**IP Forwarding** (142)</span></span>
</dt> <dt>

<span data-ttu-id="78413-453"><span id="MSDSL"></span><span id="msdsl"></span>**MSDSL** (143)</span><span class="sxs-lookup"><span data-stu-id="78413-453"><span id="MSDSL"></span><span id="msdsl"></span>**MSDSL** (143)</span></span>
</dt> <dt>

<span data-ttu-id="78413-454"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)</span><span class="sxs-lookup"><span data-stu-id="78413-454"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)</span></span>
</dt> <dt>

<span data-ttu-id="78413-455"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**If-GSN/HIPPI-6400** (145)</span><span class="sxs-lookup"><span data-stu-id="78413-455"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**IF-GSN/HIPPI-6400** (145)</span></span>
</dt> <dt>

<span data-ttu-id="78413-456"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**Capa de Mac DVB-RCC** (146)</span><span class="sxs-lookup"><span data-stu-id="78413-456"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**DVB-RCC MAC Layer** (146)</span></span>
</dt> <dt>

<span data-ttu-id="78413-457"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-RCC downstream** (147)</span><span class="sxs-lookup"><span data-stu-id="78413-457"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-RCC Downstream** (147)</span></span>
</dt> <dt>

<span data-ttu-id="78413-458"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-nivel superior de RCC** (148)</span><span class="sxs-lookup"><span data-stu-id="78413-458"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-RCC Upstream** (148)</span></span>
</dt> <dt>

<span data-ttu-id="78413-459"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**ATM virtual** (149)</span><span class="sxs-lookup"><span data-stu-id="78413-459"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**ATM Virtual** (149)</span></span>
</dt> <dt>

<span data-ttu-id="78413-460"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**Túnel MPLS** (150)</span><span class="sxs-lookup"><span data-stu-id="78413-460"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**MPLS Tunnel** (150)</span></span>
</dt> <dt>

<span data-ttu-id="78413-461"><span id="SRP"></span><span id="srp"></span>**SRP** (151)</span><span class="sxs-lookup"><span data-stu-id="78413-461"><span id="SRP"></span><span id="srp"></span>**SRP** (151)</span></span>
</dt> <dt>

<span data-ttu-id="78413-462"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voz sobre ATM** (152)</span><span class="sxs-lookup"><span data-stu-id="78413-462"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voice over ATM** (152)</span></span>
</dt> <dt>

<span data-ttu-id="78413-463"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Voz sobre Frame Relay** (153)</span><span class="sxs-lookup"><span data-stu-id="78413-463"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Voice over Frame Relay** (153)</span></span>
</dt> <dt>

<span data-ttu-id="78413-464"><span id="ISDL"></span><span id="isdl"></span>**ISDL** (154)</span><span class="sxs-lookup"><span data-stu-id="78413-464"><span id="ISDL"></span><span id="isdl"></span>**ISDL** (154)</span></span>
</dt> <dt>

<span data-ttu-id="78413-465"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Vínculo compuesto** (155)</span><span class="sxs-lookup"><span data-stu-id="78413-465"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Composite Link** (155)</span></span>
</dt> <dt>

<span data-ttu-id="78413-466"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**Vínculo de señalización de SS7** (156)</span><span class="sxs-lookup"><span data-stu-id="78413-466"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**SS7 Signaling Link** (156)</span></span>
</dt> <dt>

<span data-ttu-id="78413-467"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Inalámbrica P2P de propiedad** (157)</span><span class="sxs-lookup"><span data-stu-id="78413-467"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Proprietary P2P Wireless** (157)</span></span>
</dt> <dt>

<span data-ttu-id="78413-468"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Fotograma hacia delante** (158)</span><span class="sxs-lookup"><span data-stu-id="78413-468"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Frame Forward** (158)</span></span>
</dt> <dt>

<span data-ttu-id="78413-469"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**Multiprotocolo RFC1483 a través de ATM** (159)</span><span class="sxs-lookup"><span data-stu-id="78413-469"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 Multiprotocol over ATM** (159)</span></span>
</dt> <dt>

<span data-ttu-id="78413-470"><span id="USB"></span><span id="usb"></span>**USB** (160)</span><span class="sxs-lookup"><span data-stu-id="78413-470"><span id="USB"></span><span id="usb"></span>**USB** (160)</span></span>
</dt> <dt>

<span data-ttu-id="78413-471"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**Agregado de vínculo de ad de IEEE 802.3** (161)</span><span class="sxs-lookup"><span data-stu-id="78413-471"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**IEEE 802.3ad Link Aggregate** (161)</span></span>
</dt> <dt>

<span data-ttu-id="78413-472"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**Cuentas de directivas BGP** (162)</span><span class="sxs-lookup"><span data-stu-id="78413-472"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**BGP Policy Accounting** (162)</span></span>
</dt> <dt>

<span data-ttu-id="78413-473"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 Multilink fr** (163)</span><span class="sxs-lookup"><span data-stu-id="78413-473"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 Multilink FR** (163)</span></span>
</dt> <dt>

<span data-ttu-id="78413-474"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**H. 323 Gatekeeper** (164)</span><span class="sxs-lookup"><span data-stu-id="78413-474"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**H.323 Gatekeeper** (164)</span></span>
</dt> <dt>

<span data-ttu-id="78413-475"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**H. 323 proxy** (165)</span><span class="sxs-lookup"><span data-stu-id="78413-475"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**H.323 Proxy** (165)</span></span>
</dt> <dt>

<span data-ttu-id="78413-476"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)</span><span class="sxs-lookup"><span data-stu-id="78413-476"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)</span></span>
</dt> <dt>

<span data-ttu-id="78413-477"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Vínculo de señalización de varias frecuencias** (167)</span><span class="sxs-lookup"><span data-stu-id="78413-477"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Multi-Frequency Signaling Link** (167)</span></span>
</dt> <dt>

<span data-ttu-id="78413-478"><span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)</span><span class="sxs-lookup"><span data-stu-id="78413-478"><span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)</span></span>
</dt> <dt>

<span data-ttu-id="78413-479"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)</span><span class="sxs-lookup"><span data-stu-id="78413-479"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)</span></span>
</dt> <dt>

<span data-ttu-id="78413-480"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**Vínculo de datos de instalación DS1** (170)</span><span class="sxs-lookup"><span data-stu-id="78413-480"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**DS1 Facility Data Link** (170)</span></span>
</dt> <dt>

<span data-ttu-id="78413-481"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Paquete sobre SONET/SDH** (171)</span><span class="sxs-lookup"><span data-stu-id="78413-481"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Packet over SONET/SDH** (171)</span></span>
</dt> <dt>

<span data-ttu-id="78413-482"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**Entrada DVB-ASI** (172)</span><span class="sxs-lookup"><span data-stu-id="78413-482"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**DVB-ASI Input** (172)</span></span>
</dt> <dt>

<span data-ttu-id="78413-483"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**Salida DVB-ASI** (173)</span><span class="sxs-lookup"><span data-stu-id="78413-483"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**DVB-ASI Output** (173)</span></span>
</dt> <dt>

<span data-ttu-id="78413-484"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Línea de alimentación** (174)</span><span class="sxs-lookup"><span data-stu-id="78413-484"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Power Line** (174)</span></span>
</dt> <dt>

<span data-ttu-id="78413-485"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Señalización no asociada a la instalación** (175)</span><span class="sxs-lookup"><span data-stu-id="78413-485"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Non Facility Associated Signaling** (175)</span></span>
</dt> <dt>

<span data-ttu-id="78413-486"><span id="TR008"></span><span id="tr008"></span>**TR008** (176)</span><span class="sxs-lookup"><span data-stu-id="78413-486"><span id="TR008"></span><span id="tr008"></span>**TR008** (176)</span></span>
</dt> <dt>

<span data-ttu-id="78413-487"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)</span><span class="sxs-lookup"><span data-stu-id="78413-487"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)</span></span>
</dt> <dt>

<span data-ttu-id="78413-488"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)</span><span class="sxs-lookup"><span data-stu-id="78413-488"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)</span></span>
</dt> <dt>

<span data-ttu-id="78413-489"><span id="ISUP"></span><span id="isup"></span>**IsUp** (179)</span><span class="sxs-lookup"><span data-stu-id="78413-489"><span id="ISUP"></span><span id="isup"></span>**ISUP** (179)</span></span>
</dt> <dt>

<span data-ttu-id="78413-490"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Capa de Mac inalámbrica patentada** (180)</span><span class="sxs-lookup"><span data-stu-id="78413-490"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Proprietary Wireless MAC Layer** (180)</span></span>
</dt> <dt>

<span data-ttu-id="78413-491"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>De **bajada inalámbrica de propiedad** (181)</span><span class="sxs-lookup"><span data-stu-id="78413-491"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**Proprietary Wireless Downstream** (181)</span></span>
</dt> <dt>

<span data-ttu-id="78413-492"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Entrada de flujo inalámbrico de propiedad** (182)</span><span class="sxs-lookup"><span data-stu-id="78413-492"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Proprietary Wireless Upstream** (182)</span></span>
</dt> <dt>

<span data-ttu-id="78413-493"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HIPERLAN tipo 2** (183)</span><span class="sxs-lookup"><span data-stu-id="78413-493"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HIPERLAN Type 2** (183)</span></span>
</dt> <dt>

<span data-ttu-id="78413-494"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Punto de acceso inalámbrico de banda ancha propietario a multipoint** (184)</span><span class="sxs-lookup"><span data-stu-id="78413-494"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Proprietary Broadband Wireless Access Point to Multipoint** (184)</span></span>
</dt> <dt>

<span data-ttu-id="78413-495"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**Canal de sobrecarga de SONET** (185)</span><span class="sxs-lookup"><span data-stu-id="78413-495"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**SONET Overhead Channel** (185)</span></span>
</dt> <dt>

<span data-ttu-id="78413-496"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Canal de sobrecarga de contenedor digital** (186)</span><span class="sxs-lookup"><span data-stu-id="78413-496"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Digital Wrapper Overhead Channel** (186)</span></span>
</dt> <dt>

<span data-ttu-id="78413-497"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**Nivel 2 de adaptación ATM** (187)</span><span class="sxs-lookup"><span data-stu-id="78413-497"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**ATM Adaptation Layer 2** (187)</span></span>
</dt> <dt>

<span data-ttu-id="78413-498"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Mac de radio** (188)</span><span class="sxs-lookup"><span data-stu-id="78413-498"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Radio MAC** (188)</span></span>
</dt> <dt>

<span data-ttu-id="78413-499"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**Radio ATM** (189)</span><span class="sxs-lookup"><span data-stu-id="78413-499"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**ATM Radio** (189)</span></span>
</dt> <dt>

<span data-ttu-id="78413-500"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Tronco entre equipos** (190)</span><span class="sxs-lookup"><span data-stu-id="78413-500"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Inter Machine Trunk** (190)</span></span>
</dt> <dt>

<span data-ttu-id="78413-501"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**DSL mvl** (191)</span><span class="sxs-lookup"><span data-stu-id="78413-501"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**MVL DSL** (191)</span></span>
</dt> <dt>

<span data-ttu-id="78413-502"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**DSL de lectura larga** (192)</span><span class="sxs-lookup"><span data-stu-id="78413-502"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**Long Read DSL** (192)</span></span>
</dt> <dt>

<span data-ttu-id="78413-503"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Extremo DLCI de Frame Relay** (193)</span><span class="sxs-lookup"><span data-stu-id="78413-503"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Frame Relay DLCI Endpoint** (193)</span></span>
</dt> <dt>

<span data-ttu-id="78413-504"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**Punto de conexión de ATM VCI** (194)</span><span class="sxs-lookup"><span data-stu-id="78413-504"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**ATM VCI Endpoint** (194)</span></span>
</dt> <dt>

<span data-ttu-id="78413-505"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Canal óptico** (195)</span><span class="sxs-lookup"><span data-stu-id="78413-505"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Optical Channel** (195)</span></span>
</dt> <dt>

<span data-ttu-id="78413-506"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Transporte óptico** (196)</span><span class="sxs-lookup"><span data-stu-id="78413-506"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Optical Transport** (196)</span></span>
</dt> <dt>

<span data-ttu-id="78413-507"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**ATM de propiedad** (197)</span><span class="sxs-lookup"><span data-stu-id="78413-507"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**Proprietary ATM** (197)</span></span>
</dt> <dt>

<span data-ttu-id="78413-508"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Cable de voz sobre** (198)</span><span class="sxs-lookup"><span data-stu-id="78413-508"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Voice over Cable** (198)</span></span>
</dt> <dt>

<span data-ttu-id="78413-509"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**InfiniBand** (199)</span><span class="sxs-lookup"><span data-stu-id="78413-509"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**Infiniband** (199)</span></span>
</dt> <dt>

<span data-ttu-id="78413-510"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**Vínculo te** (200)</span><span class="sxs-lookup"><span data-stu-id="78413-510"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**TE Link** (200)</span></span>
</dt> <dt>

<span data-ttu-id="78413-511"><span id="Q.2931"></span><span id="q.2931"></span>**P. 2931** (201)</span><span class="sxs-lookup"><span data-stu-id="78413-511"><span id="Q.2931"></span><span id="q.2931"></span>**Q.2931** (201)</span></span>
</dt> <dt>

<span data-ttu-id="78413-512"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Grupo troncal virtual** (202)</span><span class="sxs-lookup"><span data-stu-id="78413-512"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Virtual Trunk Group** (202)</span></span>
</dt> <dt>

<span data-ttu-id="78413-513"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**Grupo de tronco de SIP** (203)</span><span class="sxs-lookup"><span data-stu-id="78413-513"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**SIP Trunk Group** (203)</span></span>
</dt> <dt>

<span data-ttu-id="78413-514"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**Señalización de SIP** (204)</span><span class="sxs-lookup"><span data-stu-id="78413-514"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**SIP Signaling** (204)</span></span>
</dt> <dt>

<span data-ttu-id="78413-515"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**Canal de nivel superior de CATV** (205)</span><span class="sxs-lookup"><span data-stu-id="78413-515"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**CATV Upstream Channel** (205)</span></span>
</dt> <dt>

<span data-ttu-id="78413-516"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206)</span><span class="sxs-lookup"><span data-stu-id="78413-516"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206)</span></span>
</dt> <dt>

<span data-ttu-id="78413-517"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155MB pon** (207)</span><span class="sxs-lookup"><span data-stu-id="78413-517"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155Mb PON** (207)</span></span>
</dt> <dt>

<span data-ttu-id="78413-518"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622MB pon** (208)</span><span class="sxs-lookup"><span data-stu-id="78413-518"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622Mb PON** (208)</span></span>
</dt> <dt>

<span data-ttu-id="78413-519"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Puente transparente** (209)</span><span class="sxs-lookup"><span data-stu-id="78413-519"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Transparent Bridge** (209)</span></span>
</dt> <dt>

<span data-ttu-id="78413-520"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Grupo de líneas** (210)</span><span class="sxs-lookup"><span data-stu-id="78413-520"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Line Group** (210)</span></span>
</dt> <dt>

<span data-ttu-id="78413-521"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Grupo de características de & de voz** (211)</span><span class="sxs-lookup"><span data-stu-id="78413-521"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Voice & Feature Group** (211)</span></span>
</dt> <dt>

<span data-ttu-id="78413-522"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voice FGD EANA** (212)</span><span class="sxs-lookup"><span data-stu-id="78413-522"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voice FGD EANA** (212)</span></span>
</dt> <dt>

<span data-ttu-id="78413-523"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>La **voz** (213)</span><span class="sxs-lookup"><span data-stu-id="78413-523"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voice DID** (213)</span></span>
</dt> <dt>

<span data-ttu-id="78413-524"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**Transporte MPEG** (214)</span><span class="sxs-lookup"><span data-stu-id="78413-524"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**MPEG Transport** (214)</span></span>
</dt> <dt>

<span data-ttu-id="78413-525"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6to4** (215)</span><span class="sxs-lookup"><span data-stu-id="78413-525"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6To4** (215)</span></span>
</dt> <dt>

<span data-ttu-id="78413-526"><span id="GTP"></span><span id="gtp"></span>**GTP** (216)</span><span class="sxs-lookup"><span data-stu-id="78413-526"><span id="GTP"></span><span id="gtp"></span>**GTP** (216)</span></span>
</dt> <dt>

<span data-ttu-id="78413-527"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>Parapág **EtherLoop 1** (217)</span><span class="sxs-lookup"><span data-stu-id="78413-527"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne EtherLoop 1** (217)</span></span>
</dt> <dt>

<span data-ttu-id="78413-528"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**EtherLoop 2** (218)</span><span class="sxs-lookup"><span data-stu-id="78413-528"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne EtherLoop 2** (218)</span></span>
</dt> <dt>

<span data-ttu-id="78413-529"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Grupo de canales ópticos** (219)</span><span class="sxs-lookup"><span data-stu-id="78413-529"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Optical Channel Group** (219)</span></span>
</dt> <dt>

<span data-ttu-id="78413-530"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)</span><span class="sxs-lookup"><span data-stu-id="78413-530"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)</span></span>
</dt> <dt>

<span data-ttu-id="78413-531"><span id="GFP"></span><span id="gfp"></span>**GFP** (221)</span><span class="sxs-lookup"><span data-stu-id="78413-531"><span id="GFP"></span><span id="gfp"></span>**GFP** (221)</span></span>
</dt> <dt>

<span data-ttu-id="78413-532"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222)</span><span class="sxs-lookup"><span data-stu-id="78413-532"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222)</span></span>
</dt> <dt>

<span data-ttu-id="78413-533"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223)</span><span class="sxs-lookup"><span data-stu-id="78413-533"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223)</span></span>
</dt> <dt>

<span data-ttu-id="78413-534"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**FCIP** (224)</span><span class="sxs-lookup"><span data-stu-id="78413-534"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**Fcip** (224)</span></span>
</dt> <dt>

<span data-ttu-id="78413-535"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA reservado** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="78413-535"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)</span></span>
</dt> <dt>

<span data-ttu-id="78413-536"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="78413-536"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="78413-537"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="78413-537"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="78413-538"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/V6** (4098)</span><span class="sxs-lookup"><span data-stu-id="78413-538"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="78413-539"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099)</span><span class="sxs-lookup"><span data-stu-id="78413-539"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="78413-540"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)</span><span class="sxs-lookup"><span data-stu-id="78413-540"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)</span></span>
</dt> <dt>

<span data-ttu-id="78413-541"><span id="SNA"></span><span id="sna"></span>**SNA** (4101)</span><span class="sxs-lookup"><span data-stu-id="78413-541"><span id="SNA"></span><span id="sna"></span>**SNA** (4101)</span></span>
</dt> <dt>

<span data-ttu-id="78413-542"><span id="CONP"></span><span id="conp"></span>**CONP** (4102)</span><span class="sxs-lookup"><span data-stu-id="78413-542"><span id="CONP"></span><span id="conp"></span>**CONP** (4102)</span></span>
</dt> <dt>

<span data-ttu-id="78413-543"><span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)</span><span class="sxs-lookup"><span data-stu-id="78413-543"><span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)</span></span>
</dt> <dt>

<span data-ttu-id="78413-544"><span id="VINES"></span><span id="vines"></span>**Vines** (4104)</span><span class="sxs-lookup"><span data-stu-id="78413-544"><span id="VINES"></span><span id="vines"></span>**VINES** (4104)</span></span>
</dt> <dt>

<span data-ttu-id="78413-545"><span id="XNS"></span><span id="xns"></span>**XNS** (4105)</span><span class="sxs-lookup"><span data-stu-id="78413-545"><span id="XNS"></span><span id="xns"></span>**XNS** (4105)</span></span>
</dt> <dt>

<span data-ttu-id="78413-546"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**Extremo de canal de ISDN B** (4106)</span><span class="sxs-lookup"><span data-stu-id="78413-546"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**ISDN B Channel Endpoint** (4106)</span></span>
</dt> <dt>

<span data-ttu-id="78413-547"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**Extremo de canal D ISDN (RDSI** ) (4107)</span><span class="sxs-lookup"><span data-stu-id="78413-547"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**ISDN D Channel Endpoint** (4107)</span></span>
</dt> <dt>

<span data-ttu-id="78413-548"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108)</span><span class="sxs-lookup"><span data-stu-id="78413-548"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108)</span></span>
</dt> <dt>

<span data-ttu-id="78413-549"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)</span><span class="sxs-lookup"><span data-stu-id="78413-549"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)</span></span>
</dt> <dt>

<span data-ttu-id="78413-550"><span id="UDP"></span><span id="udp"></span>**UDP** (4110)</span><span class="sxs-lookup"><span data-stu-id="78413-550"><span id="UDP"></span><span id="udp"></span>**UDP** (4110)</span></span>
</dt> <dt>

<span data-ttu-id="78413-551"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111)</span><span class="sxs-lookup"><span data-stu-id="78413-551"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111)</span></span>
</dt> <dt>

<span data-ttu-id="78413-552"><span id="802.11a"></span><span id="802.11A"></span>**802.11 a** (4112)</span><span class="sxs-lookup"><span data-stu-id="78413-552"><span id="802.11a"></span><span id="802.11A"></span>**802.11a** (4112)</span></span>
</dt> <dt>

<span data-ttu-id="78413-553"><span id="802.11b"></span><span id="802.11B"></span>**802.11 b** (4113)</span><span class="sxs-lookup"><span data-stu-id="78413-553"><span id="802.11b"></span><span id="802.11B"></span>**802.11b** (4113)</span></span>
</dt> <dt>

<span data-ttu-id="78413-554"><span id="802.11g"></span><span id="802.11G"></span>**802.11 g** (4114)</span><span class="sxs-lookup"><span data-stu-id="78413-554"><span id="802.11g"></span><span id="802.11G"></span>**802.11g** (4114)</span></span>
</dt> <dt>

<span data-ttu-id="78413-555"><span id="802.11h"></span><span id="802.11H"></span>**802.11 h** (4115)</span><span class="sxs-lookup"><span data-stu-id="78413-555"><span id="802.11h"></span><span id="802.11H"></span>**802.11h** (4115)</span></span>
</dt> <dt>

<span data-ttu-id="78413-556"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200)</span><span class="sxs-lookup"><span data-stu-id="78413-556"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200)</span></span>
</dt> <dt>

<span data-ttu-id="78413-557"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)</span><span class="sxs-lookup"><span data-stu-id="78413-557"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)</span></span>
</dt> <dt>

<span data-ttu-id="78413-558"><span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)</span><span class="sxs-lookup"><span data-stu-id="78413-558"><span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)</span></span>
</dt> <dt>

<span data-ttu-id="78413-559"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)</span><span class="sxs-lookup"><span data-stu-id="78413-559"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)</span></span>
</dt> <dt>

<span data-ttu-id="78413-560"><span id="HTTP"></span><span id="http"></span>**Http** (4204)</span><span class="sxs-lookup"><span data-stu-id="78413-560"><span id="HTTP"></span><span id="http"></span>**HTTP** (4204)</span></span>
</dt> <dt>

<span data-ttu-id="78413-561"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205)</span><span class="sxs-lookup"><span data-stu-id="78413-561"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205)</span></span>
</dt> <dt>

<span data-ttu-id="78413-562"><span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)</span><span class="sxs-lookup"><span data-stu-id="78413-562"><span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)</span></span>
</dt> <dt>

<span data-ttu-id="78413-563"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)</span><span class="sxs-lookup"><span data-stu-id="78413-563"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)</span></span>
</dt> <dt>

<span data-ttu-id="78413-564"><span id="SSH"></span><span id="ssh"></span>**Ssh** (4401)</span><span class="sxs-lookup"><span data-stu-id="78413-564"><span id="SSH"></span><span id="ssh"></span>**SSH** (4401)</span></span>
</dt> <dt>

<span data-ttu-id="78413-565"><span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)</span><span class="sxs-lookup"><span data-stu-id="78413-565"><span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)</span></span>
</dt> <dt>

<span data-ttu-id="78413-566"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)</span><span class="sxs-lookup"><span data-stu-id="78413-566"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)</span></span>
</dt> <dt>

<span data-ttu-id="78413-567"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)</span><span class="sxs-lookup"><span data-stu-id="78413-567"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)</span></span>
</dt> <dt>

<span data-ttu-id="78413-568"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405)</span><span class="sxs-lookup"><span data-stu-id="78413-568"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405)</span></span>
</dt> <dt>

<span data-ttu-id="78413-569"><span id="HTTPS"></span><span id="https"></span>**Https** (4406)</span><span class="sxs-lookup"><span data-stu-id="78413-569"><span id="HTTPS"></span><span id="https"></span>**HTTPS** (4406)</span></span>
</dt> <dt>

<span data-ttu-id="78413-570"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="78413-570"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="78413-571"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (32768..</span><span class="sxs-lookup"><span data-stu-id="78413-571"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768..</span></span> <span data-ttu-id="78413-572">)</span><span class="sxs-lookup"><span data-stu-id="78413-572">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="78413-573">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="78413-573">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-574">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78413-574">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78413-575">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-575">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-576">Esta propiedad está en desuso en lugar de la propiedad **ProtocolIFType** .</span><span class="sxs-lookup"><span data-stu-id="78413-576">This property is deprecated in lieu of the **ProtocolIFType** property.</span></span> <span data-ttu-id="78413-577">Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="78413-577">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="78413-578">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="78413-578">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-579">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78413-579">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78413-580">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-580">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-581">Último estado solicitado o deseado para el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="78413-581">The last requested or desired state for the management service.</span></span> <span data-ttu-id="78413-582">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="78413-582">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="78413-583">Value</span><span class="sxs-lookup"><span data-stu-id="78413-583">Value</span></span>                                                                         | <span data-ttu-id="78413-584">Significado</span><span class="sxs-lookup"><span data-stu-id="78413-584">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="78413-585"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="78413-585"><dt>12</dt></span></span> </dl> | <span data-ttu-id="78413-586">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="78413-586">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="78413-587">**Estado**</span><span class="sxs-lookup"><span data-stu-id="78413-587">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-588">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78413-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78413-589">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-589">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-590">Describe el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="78413-590">Describes the status of the element.</span></span> <span data-ttu-id="78413-591">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="78413-591">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="78413-592">ACEPTAR</span><span class="sxs-lookup"><span data-stu-id="78413-592">"OK"</span></span>

<span data-ttu-id="78413-593">Error</span><span class="sxs-lookup"><span data-stu-id="78413-593">"Error"</span></span>

<span data-ttu-id="78413-594">Degradado</span><span class="sxs-lookup"><span data-stu-id="78413-594">"Degraded"</span></span>

<span data-ttu-id="78413-595">Unknown</span><span class="sxs-lookup"><span data-stu-id="78413-595">"Unknown"</span></span>

<span data-ttu-id="78413-596">"Pred FAIL"</span><span class="sxs-lookup"><span data-stu-id="78413-596">"Pred Fail"</span></span>

<span data-ttu-id="78413-597">Comenzar</span><span class="sxs-lookup"><span data-stu-id="78413-597">"Starting"</span></span>

<span data-ttu-id="78413-598">Bloqueo</span><span class="sxs-lookup"><span data-stu-id="78413-598">"Stopping"</span></span>

<span data-ttu-id="78413-599">Servicio</span><span class="sxs-lookup"><span data-stu-id="78413-599">"Service"</span></span>

<span data-ttu-id="78413-600">Calca</span><span class="sxs-lookup"><span data-stu-id="78413-600">"Stressed"</span></span>

<span data-ttu-id="78413-601">"Recover"</span><span class="sxs-lookup"><span data-stu-id="78413-601">"NonRecover"</span></span>

<span data-ttu-id="78413-602">"Sin contacto"</span><span class="sxs-lookup"><span data-stu-id="78413-602">"No Contact"</span></span>

<span data-ttu-id="78413-603">"Pérdida de comunicación"</span><span class="sxs-lookup"><span data-stu-id="78413-603">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="78413-604">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="78413-604">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-605">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="78413-605">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="78413-606">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-606">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-607">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="78413-607">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="78413-608">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "OK".</span><span class="sxs-lookup"><span data-stu-id="78413-608">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="78413-609">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="78413-609">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-610">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78413-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78413-611">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-611">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-612">Nombre de la clase de creación del sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="78413-612">The hosting system's creation class name.</span></span> <span data-ttu-id="78413-613">Esta propiedad se hereda de [**\_ punto CIM**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="78413-613">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="78413-614">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="78413-614">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-615">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78413-615">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78413-616">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-616">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78413-617">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="78413-617">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="78413-618">Nombre del sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="78413-618">The name of the hosting system.</span></span> <span data-ttu-id="78413-619">Esta propiedad se hereda de [**\_ punto CIM**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="78413-619">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="78413-620">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="78413-620">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-621">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="78413-621">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="78413-622">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-622">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-623">Fecha y hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="78413-623">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="78413-624">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se admite.</span><span class="sxs-lookup"><span data-stu-id="78413-624">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="78413-625">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="78413-625">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78413-626">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78413-626">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78413-627">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78413-627">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78413-628">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="78413-628">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="78413-629">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="78413-629">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78413-630">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78413-630">Requirements</span></span>



| <span data-ttu-id="78413-631">Requisito</span><span class="sxs-lookup"><span data-stu-id="78413-631">Requirement</span></span> | <span data-ttu-id="78413-632">Value</span><span class="sxs-lookup"><span data-stu-id="78413-632">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78413-633">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78413-633">Minimum supported client</span></span><br/> | <span data-ttu-id="78413-634">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="78413-634">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="78413-635">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78413-635">Minimum supported server</span></span><br/> | <span data-ttu-id="78413-636">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="78413-636">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="78413-637">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="78413-637">Namespace</span></span><br/>                | <span data-ttu-id="78413-638">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="78413-638">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="78413-639">MOF</span><span class="sxs-lookup"><span data-stu-id="78413-639">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78413-640"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78413-640"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="78413-641">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="78413-641">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78413-642"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="78413-642"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

