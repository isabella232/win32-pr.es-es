---
description: Administra todas las conexiones remotas de terminal a un host determinado.
ms.assetid: 7eacb8a6-cb8d-4a2a-951e-f5286cf484e7
title: Msvm_TerminalService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService
- Msvm_TerminalService.InstanceID
- Msvm_TerminalService.Caption
- Msvm_TerminalService.Description
- Msvm_TerminalService.ElementName
- Msvm_TerminalService.InstallDate
- Msvm_TerminalService.OperationalStatus
- Msvm_TerminalService.StatusDescriptions
- Msvm_TerminalService.Status
- Msvm_TerminalService.HealthState
- Msvm_TerminalService.CommunicationStatus
- Msvm_TerminalService.DetailedStatus
- Msvm_TerminalService.OperatingStatus
- Msvm_TerminalService.PrimaryStatus
- Msvm_TerminalService.EnabledState
- Msvm_TerminalService.OtherEnabledState
- Msvm_TerminalService.RequestedState
- Msvm_TerminalService.EnabledDefault
- Msvm_TerminalService.TimeOfLastStateChange
- Msvm_TerminalService.AvailableRequestedStates
- Msvm_TerminalService.TransitioningToState
- Msvm_TerminalService.SystemCreationClassName
- Msvm_TerminalService.SystemName
- Msvm_TerminalService.Name
- Msvm_TerminalService.CreationClassName
- Msvm_TerminalService.PrimaryOwnerName
- Msvm_TerminalService.PrimaryOwnerContact
- Msvm_TerminalService.StartMode
- Msvm_TerminalService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76b12bb49391909638d20df817a3693938c3222c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687116"
---
# <a name="msvm_terminalservice-class"></a><span data-ttu-id="a183c-103">MSVM \_ TerminalService (clase)</span><span class="sxs-lookup"><span data-stu-id="a183c-103">Msvm\_TerminalService class</span></span>

<span data-ttu-id="a183c-104">Administra todas las conexiones remotas de terminal a un host determinado.</span><span class="sxs-lookup"><span data-stu-id="a183c-104">Manages all remote terminal connections to a particular host.</span></span> <span data-ttu-id="a183c-105">El servicio usa un puerto configurable para iniciar todas las conexiones de terminal.</span><span class="sxs-lookup"><span data-stu-id="a183c-105">The service uses a configurable port to initiate all terminal connections.</span></span>

<span data-ttu-id="a183c-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a183c-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a183c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a183c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Terminal Service";
  string   Description = "Microsoft Virtual Terminal Service";
  string   ElementName = "Hyper-V Terminal Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The virtual terminal connection management service is fully operational" };
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
  string   Name = "termsvc";
  string   CreationClassName = "Msvm_TerminalService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="a183c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a183c-108">Members</span></span>

<span data-ttu-id="a183c-109">La clase **MSVM \_ TerminalService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a183c-109">The **Msvm\_TerminalService** class has these types of members:</span></span>

-   [<span data-ttu-id="a183c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a183c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="a183c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a183c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a183c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a183c-112">Methods</span></span>

<span data-ttu-id="a183c-113">La clase **MSVM \_ TerminalService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a183c-113">The **Msvm\_TerminalService** class has these methods.</span></span>



| <span data-ttu-id="a183c-114">Método</span><span class="sxs-lookup"><span data-stu-id="a183c-114">Method</span></span>                                                                                        | <span data-ttu-id="a183c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a183c-115">Description</span></span>                                                                                                      |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a183c-116">**GetInteractiveSessionACL**</span><span class="sxs-lookup"><span data-stu-id="a183c-116">**GetInteractiveSessionACL**</span></span>](getinteractivesessionacl-msvm-terminalservice.md)             | <span data-ttu-id="a183c-117">Recupera la DACL actual que controla el acceso a la sesión interactiva de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a183c-117">Retrieves the current DACL that controls access to the interactive session of a virtual machine.</span></span><br/>      |
| [<span data-ttu-id="a183c-118">**GrantInteractiveSessionAccess**</span><span class="sxs-lookup"><span data-stu-id="a183c-118">**GrantInteractiveSessionAccess**</span></span>](grantinteractivesessionaccess-msvm-terminalservice.md)   | <span data-ttu-id="a183c-119">Concede acceso a la sesión interactiva de la máquina virtual a la lista de confianzas especificada.</span><span class="sxs-lookup"><span data-stu-id="a183c-119">Grants access to the interactive session of the virtual machine to the specified list of trustees.</span></span><br/>    |
| [<span data-ttu-id="a183c-120">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="a183c-120">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-terminalservice.md)                   | <span data-ttu-id="a183c-121">Modifica los datos de configuración para el servicio.</span><span class="sxs-lookup"><span data-stu-id="a183c-121">Modifies the setting data for the service.</span></span><br/>                                                            |
| [<span data-ttu-id="a183c-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="a183c-122">**RequestStateChange**</span></span>](msvm-terminalservice-requeststatechange.md)                         | <span data-ttu-id="a183c-123">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="a183c-123">Requests a state change.</span></span><br/>                                                                              |
| [<span data-ttu-id="a183c-124">**RevokeInteractiveSessionAccess**</span><span class="sxs-lookup"><span data-stu-id="a183c-124">**RevokeInteractiveSessionAccess**</span></span>](revokeinteractivesessionaccess-msvm-terminalservice.md) | <span data-ttu-id="a183c-125">Revoca el acceso a la sesión interactiva de la máquina virtual a partir de la lista de confianzas especificada.</span><span class="sxs-lookup"><span data-stu-id="a183c-125">Revokes access to the interactive session of the virtual machine from the specified list of trustees.</span></span><br/> |
| [<span data-ttu-id="a183c-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="a183c-126">**StartService**</span></span>](msvm-terminalservice-startservice.md)                                     | <span data-ttu-id="a183c-127">inicia el servicio.</span><span class="sxs-lookup"><span data-stu-id="a183c-127">Starts the service.</span></span><br/>                                                                                   |
| [<span data-ttu-id="a183c-128">**StopService**</span><span class="sxs-lookup"><span data-stu-id="a183c-128">**StopService**</span></span>](msvm-terminalservice-stopservice.md)                                       | <span data-ttu-id="a183c-129">detiene el servicio.</span><span class="sxs-lookup"><span data-stu-id="a183c-129">Stops the service.</span></span><br/>                                                                                    |



 

### <a name="properties"></a><span data-ttu-id="a183c-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a183c-130">Properties</span></span>

<span data-ttu-id="a183c-131">La clase **MSVM \_ TerminalService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a183c-131">The **Msvm\_TerminalService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a183c-132">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="a183c-132">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-133">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a183c-133">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a183c-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-135">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="a183c-135">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="a183c-136">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a183c-136">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-137">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a183c-137">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a183c-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-140">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a183c-140">A short description of the object.</span></span> <span data-ttu-id="a183c-141">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a183c-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-142">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="a183c-142">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-143">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a183c-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-145">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="a183c-145">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a183c-146">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a183c-146">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a183c-147">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a183c-147">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a183c-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a183c-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-149"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="a183c-149"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-150"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="a183c-150"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-151"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="a183c-151"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-152"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="a183c-152"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a183c-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="a183c-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a183c-155">)</span><span class="sxs-lookup"><span data-stu-id="a183c-155">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a183c-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a183c-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a183c-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-159">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="a183c-159">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a183c-160">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="a183c-160">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a183c-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a183c-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-164">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a183c-164">A description of the object.</span></span> <span data-ttu-id="a183c-165">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a183c-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a183c-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-167">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a183c-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-169">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="a183c-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a183c-170">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a183c-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a183c-171">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a183c-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a183c-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="a183c-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="a183c-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="a183c-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="a183c-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="a183c-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="a183c-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a183c-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="a183c-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a183c-180">)</span><span class="sxs-lookup"><span data-stu-id="a183c-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a183c-181">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a183c-181">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a183c-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-184">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="a183c-184">A display name for the object.</span></span> <span data-ttu-id="a183c-185">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a183c-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-186">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="a183c-186">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-187">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a183c-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-189">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a183c-189">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="a183c-190">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a183c-190">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-191">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a183c-191">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a183c-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-194">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a183c-194">The enabled and disabled states of an element.</span></span> <span data-ttu-id="a183c-195">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="a183c-195">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="a183c-196">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a183c-196">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-197">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a183c-197">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-198">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a183c-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-200">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="a183c-200">The current health of the element.</span></span> <span data-ttu-id="a183c-201">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="a183c-201">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="a183c-202">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="a183c-202">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="a183c-203">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a183c-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-204">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a183c-204">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-205">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a183c-205">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-207">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a183c-207">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="a183c-208">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a183c-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-209">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a183c-209">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a183c-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a183c-212">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="a183c-212">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a183c-213">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="a183c-213">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a183c-214">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="a183c-214">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a183c-215">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a183c-215">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a183c-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-218">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="a183c-218">The label by which the object is known.</span></span> <span data-ttu-id="a183c-219">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="a183c-219">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-220">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="a183c-220">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-221">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a183c-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-223">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="a183c-223">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a183c-224">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a183c-224">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a183c-225">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a183c-225">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a183c-226"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a183c-226"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-227"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="a183c-227"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-228"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="a183c-228"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-229"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="a183c-229"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-230"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="a183c-230"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-231"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="a183c-231"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-232"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="a183c-232"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-233"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="a183c-233"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-234"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="a183c-234"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-235"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="a183c-235"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-236"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="a183c-236"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-237"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="a183c-237"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-238"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="a183c-238"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-239"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="a183c-239"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-240"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="a183c-240"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-241"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="a183c-241"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-242"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="a183c-242"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-243"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a183c-243"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-244"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="a183c-244"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a183c-245">)</span><span class="sxs-lookup"><span data-stu-id="a183c-245">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a183c-246">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a183c-246">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-247">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a183c-247">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a183c-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-249">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="a183c-249">The current statuses of the object.</span></span> <span data-ttu-id="a183c-250">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a183c-250">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-251">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="a183c-251">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a183c-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-254">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="a183c-254">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="a183c-255">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="a183c-255">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="a183c-256">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a183c-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-257">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="a183c-257">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a183c-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-260">Valor que proporciona información sobre cómo se puede alcanzar el propietario principal del servicio (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.).</span><span class="sxs-lookup"><span data-stu-id="a183c-260">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="a183c-261">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="a183c-261">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-262">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="a183c-262">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-263">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a183c-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-265">Nombre del propietario principal del servicio, si se ha definido uno.</span><span class="sxs-lookup"><span data-stu-id="a183c-265">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="a183c-266">El propietario principal es el contacto de soporte inicial para el servicio.</span><span class="sxs-lookup"><span data-stu-id="a183c-266">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="a183c-267">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="a183c-267">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-268">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="a183c-268">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-269">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a183c-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-271">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="a183c-271">Provides high level status information.</span></span> <span data-ttu-id="a183c-272">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="a183c-272">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="a183c-273">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a183c-273">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a183c-274">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a183c-274">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a183c-275"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a183c-275"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-276"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="a183c-276"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-277"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="a183c-277"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-278"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="a183c-278"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a183c-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a183c-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="a183c-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a183c-281">)</span><span class="sxs-lookup"><span data-stu-id="a183c-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a183c-282">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="a183c-282">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-283">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a183c-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-285">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="a183c-285">The last requested or desired state for the element.</span></span> <span data-ttu-id="a183c-286">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="a183c-286">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="a183c-287">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="a183c-287">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="a183c-288">Una instancia concreta de [**\_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir el método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="a183c-288">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="a183c-289">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="a183c-289">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="a183c-290">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="a183c-290">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="a183c-291">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="a183c-291">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-292">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a183c-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-294">Indica si el servicio se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="a183c-294">Indicates whether the service is currently running.</span></span> <span data-ttu-id="a183c-295">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="a183c-295">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-296">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="a183c-296">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-297">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a183c-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-299">Un valor de cadena que indica si el servicio se inicia automáticamente por un sistema, un sistema operativo o se inicia solo después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a183c-299">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="a183c-300">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="a183c-300">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-301">**Estado**</span><span class="sxs-lookup"><span data-stu-id="a183c-301">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-302">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a183c-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-304">Estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="a183c-304">The status of the element.</span></span> <span data-ttu-id="a183c-305">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a183c-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-306">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a183c-306">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-307">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="a183c-307">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a183c-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-309">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="a183c-309">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a183c-310">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a183c-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-311">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a183c-311">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-312">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a183c-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-314">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a183c-314">The scoping system's creation class name.</span></span> <span data-ttu-id="a183c-315">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="a183c-315">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-316">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a183c-316">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-317">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a183c-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-319">Nombre del sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="a183c-319">The name of the hosting computer system.</span></span> <span data-ttu-id="a183c-320">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="a183c-320">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-321">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="a183c-321">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-322">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a183c-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-324">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="a183c-324">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="a183c-325">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a183c-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a183c-326">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="a183c-326">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a183c-327">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a183c-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a183c-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a183c-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a183c-329">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="a183c-329">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="a183c-330">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a183c-330">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a183c-331">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a183c-331">Remarks</span></span>

<span data-ttu-id="a183c-332">El acceso a la clase **MSVM \_ TerminalService** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="a183c-332">Access to the **Msvm\_TerminalService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a183c-333">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a183c-333">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a183c-334">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a183c-334">Requirements</span></span>



| <span data-ttu-id="a183c-335">Requisito</span><span class="sxs-lookup"><span data-stu-id="a183c-335">Requirement</span></span> | <span data-ttu-id="a183c-336">Value</span><span class="sxs-lookup"><span data-stu-id="a183c-336">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a183c-337">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a183c-337">Minimum supported client</span></span><br/> | <span data-ttu-id="a183c-338">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a183c-338">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a183c-339">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a183c-339">Minimum supported server</span></span><br/> | <span data-ttu-id="a183c-340">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a183c-340">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a183c-341">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a183c-341">Namespace</span></span><br/>                | <span data-ttu-id="a183c-342">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a183c-342">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a183c-343">MOF</span><span class="sxs-lookup"><span data-stu-id="a183c-343">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a183c-344"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a183c-344"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a183c-345">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a183c-345">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a183c-346"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a183c-346"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a183c-347">Vea también</span><span class="sxs-lookup"><span data-stu-id="a183c-347">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a183c-348">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="a183c-348">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

