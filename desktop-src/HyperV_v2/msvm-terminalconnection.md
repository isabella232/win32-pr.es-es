---
description: Indica el estado de una sesión remota activa que interactúa con una máquina virtual.
ms.assetid: EAE6082F-A0CB-4E75-8029-51E20649C0A8
title: Msvm_TerminalConnection (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalConnection
- Msvm_TerminalConnection.InstanceID
- Msvm_TerminalConnection.Caption
- Msvm_TerminalConnection.Description
- Msvm_TerminalConnection.ElementName
- Msvm_TerminalConnection.InstallDate
- Msvm_TerminalConnection.Name
- Msvm_TerminalConnection.OperationalStatus
- Msvm_TerminalConnection.StatusDescriptions
- Msvm_TerminalConnection.Status
- Msvm_TerminalConnection.HealthState
- Msvm_TerminalConnection.CommunicationStatus
- Msvm_TerminalConnection.DetailedStatus
- Msvm_TerminalConnection.OperatingStatus
- Msvm_TerminalConnection.PrimaryStatus
- Msvm_TerminalConnection.EnabledState
- Msvm_TerminalConnection.OtherEnabledState
- Msvm_TerminalConnection.RequestedState
- Msvm_TerminalConnection.EnabledDefault
- Msvm_TerminalConnection.TimeOfLastStateChange
- Msvm_TerminalConnection.AvailableRequestedStates
- Msvm_TerminalConnection.TransitioningToState
- Msvm_TerminalConnection.ConnectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66be5000fb7fdd4404e07c87673e3359065af6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817094"
---
# <a name="msvm_terminalconnection-class"></a><span data-ttu-id="8771f-103">MSVM \_ TerminalConnection (clase)</span><span class="sxs-lookup"><span data-stu-id="8771f-103">Msvm\_TerminalConnection class</span></span>

<span data-ttu-id="8771f-104">Indica el estado de una sesión remota activa que interactúa con una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8771f-104">Indicates the state of an active remote session interacting with a virtual machine.</span></span> <span data-ttu-id="8771f-105">Solo puede haber una conexión a la vez.</span><span class="sxs-lookup"><span data-stu-id="8771f-105">There can only be one connection at a time.</span></span>

<span data-ttu-id="8771f-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8771f-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8771f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8771f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalConnection : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
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
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   ConnectionID;
};
```

## <a name="members"></a><span data-ttu-id="8771f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8771f-108">Members</span></span>

<span data-ttu-id="8771f-109">La clase **MSVM \_ TerminalConnection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8771f-109">The **Msvm\_TerminalConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="8771f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="8771f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8771f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8771f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8771f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8771f-112">Methods</span></span>

<span data-ttu-id="8771f-113">La clase **MSVM \_ TerminalConnection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8771f-113">The **Msvm\_TerminalConnection** class has these methods.</span></span>



| <span data-ttu-id="8771f-114">Método</span><span class="sxs-lookup"><span data-stu-id="8771f-114">Method</span></span>                                                                   | <span data-ttu-id="8771f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8771f-115">Description</span></span>                         |
|:-------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="8771f-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="8771f-116">**RequestStateChange**</span></span>](msvm-terminalconnection-requeststatechange.md) | <span data-ttu-id="8771f-117">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="8771f-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8771f-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8771f-118">Properties</span></span>

<span data-ttu-id="8771f-119">La clase **MSVM \_ TerminalConnection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8771f-119">The **Msvm\_TerminalConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8771f-120">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="8771f-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-121">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8771f-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8771f-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-123">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="8771f-123">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="8771f-124">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="8771f-124">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8771f-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8771f-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8771f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-128">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8771f-128">A short description of the object.</span></span> <span data-ttu-id="8771f-129">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8771f-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8771f-130">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="8771f-130">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-131">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8771f-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-133">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="8771f-133">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8771f-134">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="8771f-134">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8771f-135">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8771f-135">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8771f-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="8771f-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="8771f-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="8771f-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="8771f-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="8771f-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8771f-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="8771f-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8771f-143">)</span><span class="sxs-lookup"><span data-stu-id="8771f-143">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8771f-144">**ConnectionID**</span><span class="sxs-lookup"><span data-stu-id="8771f-144">**ConnectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8771f-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8771f-147">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8771f-147">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8771f-148">Identificador único de una instancia del objeto de conexión de terminal.</span><span class="sxs-lookup"><span data-stu-id="8771f-148">The unique identifier for an instance of the terminal connection object.</span></span> <span data-ttu-id="8771f-149">El identificador tiene el formato "Microsoft:*VMID* \\ *index*".</span><span class="sxs-lookup"><span data-stu-id="8771f-149">The identifier is of the form "Microsoft:*VMID*\\*Index*".</span></span> <span data-ttu-id="8771f-150">Por ejemplo, "Microsoft: 67A5D397-A02D-11DB-AC13-001676AA34F0 \\ 0".</span><span class="sxs-lookup"><span data-stu-id="8771f-150">For example, "Microsoft:67A5D397-A02D-11DB-AC13-001676AA34F0\\0".</span></span>

</dd> <dt>

<span data-ttu-id="8771f-151">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8771f-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8771f-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-154">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8771f-154">A description of the object.</span></span> <span data-ttu-id="8771f-155">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8771f-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8771f-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8771f-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-157">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8771f-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-159">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="8771f-159">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8771f-160">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="8771f-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8771f-161">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8771f-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8771f-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="8771f-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="8771f-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="8771f-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="8771f-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="8771f-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="8771f-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8771f-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="8771f-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8771f-170">)</span><span class="sxs-lookup"><span data-stu-id="8771f-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8771f-171">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8771f-171">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8771f-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-174">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="8771f-174">A display name for the object.</span></span> <span data-ttu-id="8771f-175">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8771f-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8771f-176">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="8771f-176">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-177">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8771f-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-179">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="8771f-179">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="8771f-180">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8771f-180">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="8771f-181">Value</span><span class="sxs-lookup"><span data-stu-id="8771f-181">Value</span></span>                                                                        | <span data-ttu-id="8771f-182">Significado</span><span class="sxs-lookup"><span data-stu-id="8771f-182">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="8771f-183"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8771f-183"><dt>2</dt></span></span> </dl> | <span data-ttu-id="8771f-184">habilitado</span><span class="sxs-lookup"><span data-stu-id="8771f-184">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="8771f-185"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8771f-185"><dt>3</dt></span></span> </dl> | <span data-ttu-id="8771f-186">Disabled</span><span class="sxs-lookup"><span data-stu-id="8771f-186">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8771f-187">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8771f-187">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-188">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8771f-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-190">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="8771f-190">The enabled and disabled states of an element.</span></span> <span data-ttu-id="8771f-191">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="8771f-191">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="8771f-192">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8771f-192">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="8771f-193">Value</span><span class="sxs-lookup"><span data-stu-id="8771f-193">Value</span></span>                                                                        | <span data-ttu-id="8771f-194">Significado</span><span class="sxs-lookup"><span data-stu-id="8771f-194">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="8771f-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8771f-195"><dt>2</dt></span></span> </dl> | <span data-ttu-id="8771f-196">habilitado</span><span class="sxs-lookup"><span data-stu-id="8771f-196">Enabled</span></span><br/>        |
| <dl> <span data-ttu-id="8771f-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8771f-197"><dt>3</dt></span></span> </dl> | <span data-ttu-id="8771f-198">Disabled</span><span class="sxs-lookup"><span data-stu-id="8771f-198">Disabled</span></span><br/>       |
| <dl> <span data-ttu-id="8771f-199"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="8771f-199"><dt>5</dt></span></span> </dl> | <span data-ttu-id="8771f-200">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="8771f-200">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8771f-201">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8771f-201">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-202">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8771f-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-204">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="8771f-204">The current health of the element.</span></span> <span data-ttu-id="8771f-205">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="8771f-205">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="8771f-206">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="8771f-206">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="8771f-207">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="8771f-207">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="8771f-208">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8771f-208">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-209">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8771f-209">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-211">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8771f-211">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="8771f-212">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8771f-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8771f-213">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8771f-213">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-214">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8771f-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8771f-216">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="8771f-216">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8771f-217">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="8771f-217">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8771f-218">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8771f-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8771f-219">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="8771f-219">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-220">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8771f-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-222">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="8771f-222">The label by which the object is known.</span></span> <span data-ttu-id="8771f-223">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y es igual que la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="8771f-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="8771f-224">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="8771f-224">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-225">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8771f-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-227">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="8771f-227">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8771f-228">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="8771f-228">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8771f-229">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8771f-229">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8771f-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="8771f-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="8771f-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="8771f-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="8771f-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="8771f-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="8771f-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="8771f-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="8771f-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="8771f-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="8771f-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="8771f-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="8771f-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="8771f-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="8771f-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="8771f-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="8771f-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="8771f-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8771f-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="8771f-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8771f-249">)</span><span class="sxs-lookup"><span data-stu-id="8771f-249">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8771f-250">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8771f-250">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-251">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8771f-251">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8771f-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-253">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="8771f-253">The current statuses of the object.</span></span> <span data-ttu-id="8771f-254">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8771f-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8771f-255">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="8771f-255">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-256">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8771f-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-258">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="8771f-258">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="8771f-259">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="8771f-259">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="8771f-260">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="8771f-260">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8771f-261">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="8771f-261">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-262">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8771f-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-264">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="8771f-264">Provides high level status information.</span></span> <span data-ttu-id="8771f-265">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="8771f-265">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="8771f-266">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="8771f-266">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8771f-267">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8771f-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8771f-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="8771f-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-269"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="8771f-269"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="8771f-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="8771f-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8771f-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8771f-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="8771f-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8771f-274">)</span><span class="sxs-lookup"><span data-stu-id="8771f-274">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8771f-275">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="8771f-275">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-276">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8771f-276">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-277">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-278">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="8771f-278">The last requested or desired state for the element.</span></span> <span data-ttu-id="8771f-279">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="8771f-279">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="8771f-280">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="8771f-280">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="8771f-281">Una instancia concreta de [**\_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no ser compatible con **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="8771f-281">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="8771f-282">Si esto ocurre, se usa el valor 12.</span><span class="sxs-lookup"><span data-stu-id="8771f-282">If this occurs, the value 12 is used.</span></span> <span data-ttu-id="8771f-283">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="8771f-283">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>



| <span data-ttu-id="8771f-284">Value</span><span class="sxs-lookup"><span data-stu-id="8771f-284">Value</span></span>                                                                         | <span data-ttu-id="8771f-285">Significado</span><span class="sxs-lookup"><span data-stu-id="8771f-285">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="8771f-286"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="8771f-286"><dt>12</dt></span></span> </dl> | <span data-ttu-id="8771f-287">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="8771f-287">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8771f-288">**Estado**</span><span class="sxs-lookup"><span data-stu-id="8771f-288">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-289">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8771f-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-291">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="8771f-291">The current status of the object.</span></span> <span data-ttu-id="8771f-292">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="8771f-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8771f-293">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8771f-293">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-294">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="8771f-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8771f-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-296">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="8771f-296">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="8771f-297">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8771f-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8771f-298">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="8771f-298">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-299">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8771f-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-301">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="8771f-301">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="8771f-302">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="8771f-302">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8771f-303">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="8771f-303">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8771f-304">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8771f-304">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8771f-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8771f-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8771f-306">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="8771f-306">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="8771f-307">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8771f-307">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="8771f-308">Value</span><span class="sxs-lookup"><span data-stu-id="8771f-308">Value</span></span>                                                                         | <span data-ttu-id="8771f-309">Significado</span><span class="sxs-lookup"><span data-stu-id="8771f-309">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="8771f-310"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="8771f-310"><dt>12</dt></span></span> </dl> | <span data-ttu-id="8771f-311">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="8771f-311">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8771f-312">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8771f-312">Remarks</span></span>

<span data-ttu-id="8771f-313">El acceso a la clase **MSVM \_ TerminalConnection** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="8771f-313">Access to the **Msvm\_TerminalConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8771f-314">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8771f-314">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="8771f-315">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8771f-315">Requirements</span></span>



| <span data-ttu-id="8771f-316">Requisito</span><span class="sxs-lookup"><span data-stu-id="8771f-316">Requirement</span></span> | <span data-ttu-id="8771f-317">Value</span><span class="sxs-lookup"><span data-stu-id="8771f-317">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8771f-318">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8771f-318">Minimum supported client</span></span><br/> | <span data-ttu-id="8771f-319">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="8771f-319">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8771f-320">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8771f-320">Minimum supported server</span></span><br/> | <span data-ttu-id="8771f-321">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8771f-321">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8771f-322">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8771f-322">Namespace</span></span><br/>                | <span data-ttu-id="8771f-323">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="8771f-323">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8771f-324">MOF</span><span class="sxs-lookup"><span data-stu-id="8771f-324">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8771f-325"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8771f-325"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8771f-326">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8771f-326">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8771f-327"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8771f-327"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8771f-328">Vea también</span><span class="sxs-lookup"><span data-stu-id="8771f-328">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8771f-329">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="8771f-329">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> <dt>

<span data-ttu-id="8771f-330">[**\_ENABLEDLOGICALELEMENT CIM**](/previous-versions//cc136818(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8771f-330">[**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8771f-331">Clases de vídeo</span><span class="sxs-lookup"><span data-stu-id="8771f-331">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

