---
description: Actúa como marcador de posición para el servicio dentro del conmutador que aprende las direcciones MAC y sirve como puente entre las \_ clases MSVM VirtualEthernetSwitch y MSVM \_ DynamicForwardingEntry.
ms.assetid: E617DBC3-F5DD-4875-B3CC-E120A2218EBE
title: Msvm_TransparentBridgingService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingService
- Msvm_TransparentBridgingService.InstanceID
- Msvm_TransparentBridgingService.Caption
- Msvm_TransparentBridgingService.Description
- Msvm_TransparentBridgingService.ElementName
- Msvm_TransparentBridgingService.InstallDate
- Msvm_TransparentBridgingService.OperationalStatus
- Msvm_TransparentBridgingService.StatusDescriptions
- Msvm_TransparentBridgingService.Status
- Msvm_TransparentBridgingService.HealthState
- Msvm_TransparentBridgingService.CommunicationStatus
- Msvm_TransparentBridgingService.DetailedStatus
- Msvm_TransparentBridgingService.OperatingStatus
- Msvm_TransparentBridgingService.PrimaryStatus
- Msvm_TransparentBridgingService.EnabledState
- Msvm_TransparentBridgingService.OtherEnabledState
- Msvm_TransparentBridgingService.RequestedState
- Msvm_TransparentBridgingService.EnabledDefault
- Msvm_TransparentBridgingService.TimeOfLastStateChange
- Msvm_TransparentBridgingService.AvailableRequestedStates
- Msvm_TransparentBridgingService.TransitioningToState
- Msvm_TransparentBridgingService.SystemCreationClassName
- Msvm_TransparentBridgingService.SystemName
- Msvm_TransparentBridgingService.CreationClassName
- Msvm_TransparentBridgingService.Name
- Msvm_TransparentBridgingService.PrimaryOwnerName
- Msvm_TransparentBridgingService.PrimaryOwnerContact
- Msvm_TransparentBridgingService.StartMode
- Msvm_TransparentBridgingService.Started
- Msvm_TransparentBridgingService.Keywords
- Msvm_TransparentBridgingService.ServiceURL
- Msvm_TransparentBridgingService.StartupConditions
- Msvm_TransparentBridgingService.StartupParameters
- Msvm_TransparentBridgingService.ProtocolType
- Msvm_TransparentBridgingService.OtherProtocolType
- Msvm_TransparentBridgingService.AgingTime
- Msvm_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f5daacf42bc221fa98f56d0c5b84140e3784c2ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001399"
---
# <a name="msvm_transparentbridgingservice-class"></a><span data-ttu-id="9981c-103">MSVM \_ TransparentBridgingService (clase)</span><span class="sxs-lookup"><span data-stu-id="9981c-103">Msvm\_TransparentBridgingService class</span></span>

<span data-ttu-id="9981c-104">Actúa como marcador de posición para el servicio dentro del conmutador que aprende las direcciones MAC y sirve como puente entre las clases [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) y [**MSVM \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) .</span><span class="sxs-lookup"><span data-stu-id="9981c-104">Serves as a placeholder for the service inside the switch that learns MAC addresses and serves as a bridge between the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) and [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) classes.</span></span>

<span data-ttu-id="9981c-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9981c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9981c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9981c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingService : CIM_TransparentBridgingService
{
  string   InstanceID;
  string   Caption = "Virtual Switch Transparent Bridging Service";
  string   Description = "Microsoft Virtual Switch Transparent Bridging Service";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
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
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_TransparentBridgingService";
  string   Name;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode = "Automatic";
  boolean  Started = True;
  string   Keywords[];
  string   ServiceURL;
  string   StartupConditions[];
  string   StartupParameters[];
  uint16   ProtocolType = 15;
  string   OtherProtocolType;
  uint32   AgingTime = 300;
  uint32   FID = 0;
};
```

## <a name="members"></a><span data-ttu-id="9981c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9981c-107">Members</span></span>

<span data-ttu-id="9981c-108">La clase **MSVM \_ TransparentBridgingService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9981c-108">The **Msvm\_TransparentBridgingService** class has these types of members:</span></span>

-   [<span data-ttu-id="9981c-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="9981c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="9981c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9981c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9981c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="9981c-111">Methods</span></span>

<span data-ttu-id="9981c-112">La clase **MSVM \_ TransparentBridgingService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9981c-112">The **Msvm\_TransparentBridgingService** class has these methods.</span></span>



| <span data-ttu-id="9981c-113">Método</span><span class="sxs-lookup"><span data-stu-id="9981c-113">Method</span></span>                                                                           | <span data-ttu-id="9981c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9981c-114">Description</span></span>                         |
|:---------------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="9981c-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="9981c-115">**RequestStateChange**</span></span>](msvm-transparentbridgingservice-requeststatechange.md) | <span data-ttu-id="9981c-116">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="9981c-116">Requests a state change.</span></span><br/> |
| [<span data-ttu-id="9981c-117">**StartService**</span><span class="sxs-lookup"><span data-stu-id="9981c-117">**StartService**</span></span>](msvm-transparentbridgingservice-startservice.md)             | <span data-ttu-id="9981c-118">inicia el servicio.</span><span class="sxs-lookup"><span data-stu-id="9981c-118">Starts the service.</span></span><br/>      |
| [<span data-ttu-id="9981c-119">**StopService**</span><span class="sxs-lookup"><span data-stu-id="9981c-119">**StopService**</span></span>](msvm-transparentbridgingservice-stopservice.md)               | <span data-ttu-id="9981c-120">detiene el servicio.</span><span class="sxs-lookup"><span data-stu-id="9981c-120">Stops the service.</span></span><br/>       |



 

### <a name="properties"></a><span data-ttu-id="9981c-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9981c-121">Properties</span></span>

<span data-ttu-id="9981c-122">La clase **MSVM \_ TransparentBridgingService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9981c-122">The **Msvm\_TransparentBridgingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9981c-123">**AgingTime**</span><span class="sxs-lookup"><span data-stu-id="9981c-123">**AgingTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9981c-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-126">Período de tiempo de espera, en segundos, para la caducidad de direcciones MAC aprendidas dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="9981c-126">The time-out period, in seconds, for aging out dynamically learned MAC addresses.</span></span> <span data-ttu-id="9981c-127">Esta propiedad se hereda de [**\_ TransparentBridgingService CIM**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span><span class="sxs-lookup"><span data-stu-id="9981c-127">This property is inherited from [**CIM\_TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-128">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="9981c-128">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-129">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9981c-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9981c-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-131">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="9981c-131">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="9981c-132">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9981c-132">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-133">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9981c-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9981c-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-136">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="9981c-136">A short description of the object.</span></span> <span data-ttu-id="9981c-137">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre es "servicio de puente transparente de conmutador virtual".</span><span class="sxs-lookup"><span data-stu-id="9981c-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always "Virtual Switch Transparent Bridging Service".</span></span>

</dd> <dt>

<span data-ttu-id="9981c-138">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="9981c-138">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9981c-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-141">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="9981c-141">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9981c-142">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="9981c-142">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9981c-143">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9981c-143">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9981c-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9981c-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-145"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="9981c-145"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-146"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="9981c-146"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-147"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="9981c-147"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-148"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="9981c-148"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9981c-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-150"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="9981c-150"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9981c-151">)</span><span class="sxs-lookup"><span data-stu-id="9981c-151">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9981c-152">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9981c-152">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9981c-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-155">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="9981c-155">A short description of the object.</span></span> <span data-ttu-id="9981c-156">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9981c-156">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-157">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9981c-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9981c-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-160">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="9981c-160">A description of the object.</span></span> <span data-ttu-id="9981c-161">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "servicio de puente transparente de conmutador virtual de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="9981c-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Switch Transparent Bridging Service".</span></span>

</dd> <dt>

<span data-ttu-id="9981c-162">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9981c-162">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-163">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9981c-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-165">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="9981c-165">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9981c-166">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="9981c-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9981c-167">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9981c-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9981c-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="9981c-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-169"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="9981c-169"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-170"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="9981c-170"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-171"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="9981c-171"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-172"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="9981c-172"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-173"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="9981c-173"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9981c-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="9981c-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9981c-176">)</span><span class="sxs-lookup"><span data-stu-id="9981c-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9981c-177">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9981c-177">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9981c-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-180">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="9981c-180">A display name for the object.</span></span> <span data-ttu-id="9981c-181">Esta propiedad permite a cada instancia definir un nombre para mostrar además de las propiedades de clave, los datos de identidad y la información de descripción.</span><span class="sxs-lookup"><span data-stu-id="9981c-181">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="9981c-182">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9981c-182">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-183">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="9981c-183">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-184">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9981c-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-186">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="9981c-186">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="9981c-187">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9981c-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-188">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9981c-188">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-189">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9981c-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-191">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="9981c-191">The enabled and disabled states of an element.</span></span> <span data-ttu-id="9981c-192">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9981c-192">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-193">**FID**</span><span class="sxs-lookup"><span data-stu-id="9981c-193">**FID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-194">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9981c-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-196">Identificador de la base de datos de filtrado utilizado por los modificadores que admiten VLAN y que tienen más de una base de datos de filtrado.</span><span class="sxs-lookup"><span data-stu-id="9981c-196">The filtering database identifier used by switches that support VLAN and that have more than one filtering database.</span></span> <span data-ttu-id="9981c-197">Esta propiedad se hereda de [**\_ TransparentBridgingService CIM**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span><span class="sxs-lookup"><span data-stu-id="9981c-197">This property is inherited from [**CIM\_TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-198">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9981c-198">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-199">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9981c-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-201">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="9981c-201">The current health of the element.</span></span> <span data-ttu-id="9981c-202">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="9981c-202">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="9981c-203">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9981c-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-204">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9981c-204">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-205">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9981c-205">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-207">Especifica la hora a la que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="9981c-207">Specifies the time when the object was installed.</span></span> <span data-ttu-id="9981c-208">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="9981c-208">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="9981c-209">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9981c-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9981c-210">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9981c-210">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-211">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9981c-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9981c-213">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="9981c-213">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9981c-214">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="9981c-214">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9981c-215">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9981c-215">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-216">**Palabras clave**</span><span class="sxs-lookup"><span data-stu-id="9981c-216">**Keywords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-217">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="9981c-217">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9981c-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-219">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="9981c-219">Do not use.</span></span> <span data-ttu-id="9981c-220">Matriz de cadenas de forma libre que proporciona palabras y frases descriptivas que se pueden usar en las consultas.</span><span class="sxs-lookup"><span data-stu-id="9981c-220">A free-form array of strings that provide descriptive words and phrases that can be used in queries.</span></span> <span data-ttu-id="9981c-221">Esta propiedad no está implementada porque no está normalizada.</span><span class="sxs-lookup"><span data-stu-id="9981c-221">This property is not implemented because it is not standardized.</span></span> <span data-ttu-id="9981c-222">Si esta propiedad fuera una construcción de consulta necesaria, se necesitaría más arriba en la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="9981c-222">If this property were a necessary query construct, then it would be required higher in the inheritance hierarchy.</span></span> <span data-ttu-id="9981c-223">Esta propiedad se hereda de [**la \_ NetworkService de CIM**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9981c-223">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-224">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="9981c-224">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9981c-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-227">Nombre que identifica de forma única el servicio y proporciona una indicación de la funcionalidad que se administra.</span><span class="sxs-lookup"><span data-stu-id="9981c-227">A name that uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="9981c-228">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9981c-228">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-229">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="9981c-229">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-230">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9981c-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-232">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="9981c-232">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9981c-233">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="9981c-233">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9981c-234">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9981c-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9981c-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9981c-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="9981c-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="9981c-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="9981c-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="9981c-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="9981c-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="9981c-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="9981c-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="9981c-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="9981c-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="9981c-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="9981c-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="9981c-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="9981c-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="9981c-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="9981c-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="9981c-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9981c-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="9981c-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9981c-254">)</span><span class="sxs-lookup"><span data-stu-id="9981c-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9981c-255">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9981c-255">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-256">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9981c-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9981c-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-258">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="9981c-258">The current status of the element.</span></span> <span data-ttu-id="9981c-259">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9981c-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-260">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="9981c-260">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9981c-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-263">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="9981c-263">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="9981c-264">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9981c-264">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9981c-265">**OtherProtocolType**</span><span class="sxs-lookup"><span data-stu-id="9981c-265">**OtherProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-266">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9981c-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-268">El tipo de protocolo que se reenvía cuando el valor de **protocolType** es 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="9981c-268">The type of protocol that is being forwarded when the value of **ProtocolType** is 1 (Other).</span></span> <span data-ttu-id="9981c-269">Esta propiedad se hereda de [**\_ ForwardingService CIM**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span><span class="sxs-lookup"><span data-stu-id="9981c-269">This property is inherited from [**CIM\_ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-270">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="9981c-270">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-271">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9981c-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-273">Una cadena que proporciona información sobre cómo se puede alcanzar el propietario principal del servicio.</span><span class="sxs-lookup"><span data-stu-id="9981c-273">A string that provides information about how the primary owner of the Service can be reached.</span></span> <span data-ttu-id="9981c-274">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9981c-274">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-275">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="9981c-275">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-276">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9981c-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-277">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-278">Nombre del propietario principal del servicio, si se ha definido uno.</span><span class="sxs-lookup"><span data-stu-id="9981c-278">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="9981c-279">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9981c-279">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-280">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="9981c-280">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-281">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9981c-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-283">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="9981c-283">Provides high level status information.</span></span> <span data-ttu-id="9981c-284">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="9981c-284">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="9981c-285">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="9981c-285">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9981c-286">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9981c-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9981c-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9981c-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-288"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="9981c-288"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-289"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="9981c-289"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-290"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="9981c-290"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-291"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9981c-291"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9981c-292"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="9981c-292"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9981c-293">)</span><span class="sxs-lookup"><span data-stu-id="9981c-293">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9981c-294">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="9981c-294">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-295">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9981c-295">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-297">El tipo de protocolo que se va a reenviar.</span><span class="sxs-lookup"><span data-stu-id="9981c-297">The type of protocol that is being forwarded.</span></span> <span data-ttu-id="9981c-298">Esta propiedad se hereda de [**\_ ForwardingService CIM**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span><span class="sxs-lookup"><span data-stu-id="9981c-298">This property is inherited from [**CIM\_ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-299">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9981c-299">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-300">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9981c-300">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-302">Último estado solicitado o deseado para el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="9981c-302">The last requested or desired state for the management service.</span></span> <span data-ttu-id="9981c-303">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9981c-303">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-304">**ServiceURL**</span><span class="sxs-lookup"><span data-stu-id="9981c-304">**ServiceURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-305">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9981c-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-307">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="9981c-307">Do not use.</span></span> <span data-ttu-id="9981c-308">Una dirección URL que proporciona el protocolo, la ubicación de red y otra información específica del servicio necesaria para obtener acceso al servicio.</span><span class="sxs-lookup"><span data-stu-id="9981c-308">A URL that provides the protocol, network location, and other service-specific information required to access the service.</span></span> <span data-ttu-id="9981c-309">En su lugar, use la clase **ServiceAccessURI** , que coloca correctamente la semántica del acceso al servicio y clarifica el formato de la información.</span><span class="sxs-lookup"><span data-stu-id="9981c-309">Instead, use the **ServiceAccessURI** class, which correctly positions the semantics of the service access, and clarifies the format of the information.</span></span> <span data-ttu-id="9981c-310">Esta propiedad se hereda de [**la \_ NetworkService de CIM**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9981c-310">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-311">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="9981c-311">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-312">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9981c-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-314">Indica si el servicio se ha iniciado (**true**) o detenido (**false**).</span><span class="sxs-lookup"><span data-stu-id="9981c-314">Indicates whether the service has been started (**True**), or stopped (**False**).</span></span> <span data-ttu-id="9981c-315">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9981c-315">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-316">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="9981c-316">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-317">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9981c-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-319">Indica si el servicio se inicia automáticamente por un sistema, un sistema operativo, etc., o si se inicia solo después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9981c-319">Indicates whether the service is automatically started by a system, an operating system, and so on, or is started only upon request.</span></span> <span data-ttu-id="9981c-320">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9981c-320">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-321">**StartupConditions**</span><span class="sxs-lookup"><span data-stu-id="9981c-321">**StartupConditions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-322">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="9981c-322">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9981c-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-324">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="9981c-324">Do not use.</span></span> <span data-ttu-id="9981c-325">Matriz de cadenas de forma libre que especifica las condiciones previas específicas que se deben cumplir para que este servicio se inicie correctamente.</span><span class="sxs-lookup"><span data-stu-id="9981c-325">A free-form array of strings that specify any specific preconditions that must be met for this service to start correctly.</span></span> <span data-ttu-id="9981c-326">Esta propiedad no es útil porque no está normalizada.</span><span class="sxs-lookup"><span data-stu-id="9981c-326">This property is not useful because it is not standardized.</span></span> <span data-ttu-id="9981c-327">Si esta propiedad fuera una construcción necesaria, se necesitaría más arriba en la jerarquía de herencia (en el servicio).</span><span class="sxs-lookup"><span data-stu-id="9981c-327">If this property were a necessary construct, then it would be required higher in the inheritance hierarchy (on Service).</span></span> <span data-ttu-id="9981c-328">Esta propiedad se hereda de [**la \_ NetworkService de CIM**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9981c-328">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-329">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="9981c-329">**StartupParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-330">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="9981c-330">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9981c-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-332">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="9981c-332">Do not use.</span></span> <span data-ttu-id="9981c-333">Matriz de cadenas de forma libre que especifica los parámetros específicos que se deben proporcionar al método **StartService** para que este servicio se inicie correctamente.</span><span class="sxs-lookup"><span data-stu-id="9981c-333">A free-form array of strings that specify any specific parameters that must be supplied to the **StartService** method for this service to start correctly.</span></span> <span data-ttu-id="9981c-334">Si este método se ha refinado, sus parámetros transmitirían más formalmente esta información.</span><span class="sxs-lookup"><span data-stu-id="9981c-334">If this method were refined, then its parameters would more formally convey this information.</span></span> <span data-ttu-id="9981c-335">Esta propiedad se hereda de [**la \_ NetworkService de CIM**](/previous-versions//cc136875(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9981c-335">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-336">**Estado**</span><span class="sxs-lookup"><span data-stu-id="9981c-336">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-337">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9981c-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-339">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9981c-339">The current status of the object.</span></span> <span data-ttu-id="9981c-340">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9981c-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-341">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9981c-341">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-342">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="9981c-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9981c-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-344">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="9981c-344">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9981c-345">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9981c-345">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-346">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9981c-346">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-347">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9981c-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-349">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="9981c-349">The creation class name of the scoping system.</span></span> <span data-ttu-id="9981c-350">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9981c-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-351">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9981c-351">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9981c-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-354">Nombre NetBIOS del sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="9981c-354">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="9981c-355">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="9981c-355">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="9981c-356">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="9981c-356">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-357">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9981c-357">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-359">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="9981c-359">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="9981c-360">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9981c-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9981c-361">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="9981c-361">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9981c-362">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9981c-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9981c-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9981c-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9981c-364">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="9981c-364">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9981c-365">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9981c-365">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9981c-366">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9981c-366">Remarks</span></span>

<span data-ttu-id="9981c-367">El acceso a la clase **MSVM \_ TransparentBridgingService** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="9981c-367">Access to the **Msvm\_TransparentBridgingService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9981c-368">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9981c-368">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9981c-369">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9981c-369">Requirements</span></span>



| <span data-ttu-id="9981c-370">Requisito</span><span class="sxs-lookup"><span data-stu-id="9981c-370">Requirement</span></span> | <span data-ttu-id="9981c-371">Value</span><span class="sxs-lookup"><span data-stu-id="9981c-371">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9981c-372">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9981c-372">Minimum supported client</span></span><br/> | <span data-ttu-id="9981c-373">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="9981c-373">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9981c-374">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9981c-374">Minimum supported server</span></span><br/> | <span data-ttu-id="9981c-375">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9981c-375">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9981c-376">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9981c-376">Namespace</span></span><br/>                | <span data-ttu-id="9981c-377">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9981c-377">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9981c-378">MOF</span><span class="sxs-lookup"><span data-stu-id="9981c-378">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9981c-379"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9981c-379"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9981c-380">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9981c-380">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9981c-381"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9981c-381"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9981c-382">Vea también</span><span class="sxs-lookup"><span data-stu-id="9981c-382">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9981c-383">**\_TRANSPARENTBRIDGINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="9981c-383">**CIM\_TransparentBridgingService**</span></span>](cim-transparentbridgingservice.md)
</dt> <dt>

[<span data-ttu-id="9981c-384">**\_TRANSPARENTBRIDGINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="9981c-384">**CIM\_TransparentBridgingService**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice)
</dt> </dl>

 

