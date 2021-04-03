---
description: Representa el estado del controlador de pantalla sintético presente en cada configuración de máquina virtual.
ms.assetid: E496B887-9032-43D8-A7D2-67BB77342AFD
title: Clase Msvm_SyntheticDisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayController
- Msvm_SyntheticDisplayController.SetPowerState
- Msvm_SyntheticDisplayController.EnableDevice
- Msvm_SyntheticDisplayController.OnlineDevice
- Msvm_SyntheticDisplayController.QuiesceDevice
- Msvm_SyntheticDisplayController.SaveProperties
- Msvm_SyntheticDisplayController.RestoreProperties
- Msvm_SyntheticDisplayController.InstanceID
- Msvm_SyntheticDisplayController.Caption
- Msvm_SyntheticDisplayController.Description
- Msvm_SyntheticDisplayController.ElementName
- Msvm_SyntheticDisplayController.InstallDate
- Msvm_SyntheticDisplayController.Name
- Msvm_SyntheticDisplayController.OperationalStatus
- Msvm_SyntheticDisplayController.StatusDescriptions
- Msvm_SyntheticDisplayController.Status
- Msvm_SyntheticDisplayController.HealthState
- Msvm_SyntheticDisplayController.CommunicationStatus
- Msvm_SyntheticDisplayController.DetailedStatus
- Msvm_SyntheticDisplayController.OperatingStatus
- Msvm_SyntheticDisplayController.PrimaryStatus
- Msvm_SyntheticDisplayController.EnabledState
- Msvm_SyntheticDisplayController.OtherEnabledState
- Msvm_SyntheticDisplayController.RequestedState
- Msvm_SyntheticDisplayController.EnabledDefault
- Msvm_SyntheticDisplayController.TimeOfLastStateChange
- Msvm_SyntheticDisplayController.AvailableRequestedStates
- Msvm_SyntheticDisplayController.TransitioningToState
- Msvm_SyntheticDisplayController.SystemCreationClassName
- Msvm_SyntheticDisplayController.SystemName
- Msvm_SyntheticDisplayController.CreationClassName
- Msvm_SyntheticDisplayController.DeviceID
- Msvm_SyntheticDisplayController.PowerManagementSupported
- Msvm_SyntheticDisplayController.PowerManagementCapabilities
- Msvm_SyntheticDisplayController.Availability
- Msvm_SyntheticDisplayController.StatusInfo
- Msvm_SyntheticDisplayController.LastErrorCode
- Msvm_SyntheticDisplayController.ErrorDescription
- Msvm_SyntheticDisplayController.ErrorCleared
- Msvm_SyntheticDisplayController.PowerOnHours
- Msvm_SyntheticDisplayController.TotalPowerOnHours
- Msvm_SyntheticDisplayController.OtherIdentifyingInfo
- Msvm_SyntheticDisplayController.IdentifyingDescriptions
- Msvm_SyntheticDisplayController.AdditionalAvailability
- Msvm_SyntheticDisplayController.MaxQuiesceTime
- Msvm_SyntheticDisplayController.TimeOfLastReset
- Msvm_SyntheticDisplayController.ProtocolSupported
- Msvm_SyntheticDisplayController.MaxNumberControlled
- Msvm_SyntheticDisplayController.ProtocolDescription
- Msvm_SyntheticDisplayController.VideoProcessor
- Msvm_SyntheticDisplayController.VideoMemoryType
- Msvm_SyntheticDisplayController.OtherVideoMemoryType
- Msvm_SyntheticDisplayController.NumberOfVideoPages
- Msvm_SyntheticDisplayController.MaxMemorySupported
- Msvm_SyntheticDisplayController.AcceleratorCapabilities
- Msvm_SyntheticDisplayController.CapabilityDescriptions
- Msvm_SyntheticDisplayController.OtherVideoArchitecture
- Msvm_SyntheticDisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7f566bf2a75b3ed4f503da245d7b6ce428dce5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908445"
---
# <a name="msvm_syntheticdisplaycontroller-class"></a><span data-ttu-id="3a1ea-103">MSVM \_ SyntheticDisplayController (clase)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-103">Msvm\_SyntheticDisplayController class</span></span>

<span data-ttu-id="3a1ea-104">Representa el estado del controlador de pantalla sintético presente en cada configuración de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-104">Represents the state of the synthetic display controller that is present in each virtual machine configuration.</span></span> <span data-ttu-id="3a1ea-105">Solo un controlador de pantalla puede estar activo en una máquina virtual en cualquier momento y el controlador sintético solo se puede activar cuando el sistema operativo invitado ha cargado los servicios de aceleración de vídeo necesarios.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-105">Only one display controller can be active in a virtual machine at any time and the synthetic controller can be activated only when the guest operating system has loaded the required video acceleration services.</span></span>

<span data-ttu-id="3a1ea-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a1ea-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a1ea-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Synthetic Display Controller";
  string   ElementName = "Display Controller";
  datetime InstallDate;
  string   Name = "Display Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_SyntheticDisplayController";
  string   DeviceID = "Microsoft:GUID";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 1024;
  uint32   MaxMemorySupported = 4194304;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="3a1ea-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3a1ea-108">Members</span></span>

<span data-ttu-id="3a1ea-109">La clase **MSVM \_ SyntheticDisplayController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3a1ea-109">The **Msvm\_SyntheticDisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="3a1ea-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="3a1ea-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3a1ea-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a1ea-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3a1ea-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3a1ea-112">Methods</span></span>

<span data-ttu-id="3a1ea-113">La clase **MSVM \_ SyntheticDisplayController** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-113">The **Msvm\_SyntheticDisplayController** class has these methods.</span></span>



| <span data-ttu-id="3a1ea-114">Método</span><span class="sxs-lookup"><span data-stu-id="3a1ea-114">Method</span></span>                                                                           | <span data-ttu-id="3a1ea-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a1ea-115">Description</span></span>                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="3a1ea-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-116">**EnableDevice**</span></span>                                                                 | <span data-ttu-id="3a1ea-117">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3a1ea-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-118">**OnlineDevice**</span></span>                                                                 | <span data-ttu-id="3a1ea-119">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3a1ea-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-120">**QuiesceDevice**</span></span>                                                                | <span data-ttu-id="3a1ea-121">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="3a1ea-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-122">**RequestStateChange**</span></span>](msvm-syntheticdisplaycontroller-requeststatechange.md) | <span data-ttu-id="3a1ea-123">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="3a1ea-124">**Reset**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-124">**Reset**</span></span>](msvm-syntheticdisplaycontroller-reset.md)                           | <span data-ttu-id="3a1ea-125">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="3a1ea-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-126">**RestoreProperties**</span></span>                                                            | <span data-ttu-id="3a1ea-127">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3a1ea-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-128">**SaveProperties**</span></span>                                                               | <span data-ttu-id="3a1ea-129">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3a1ea-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-130">**SetPowerState**</span></span>                                                                | <span data-ttu-id="3a1ea-131">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3a1ea-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a1ea-132">Properties</span></span>

<span data-ttu-id="3a1ea-133">La clase **MSVM \_ SyntheticDisplayController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-133">The **Msvm\_SyntheticDisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a1ea-134">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-134">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-135">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-137">Los gráficos y las capacidades 3D del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-137">The graphics and 3-D capabilities of the display controller.</span></span> <span data-ttu-id="3a1ea-138">Esta propiedad se hereda de [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))y siempre está establecida en 2 (acelerador de gráficos).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-138">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 2 (Graphics Accelerator).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-140">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-142">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre está establecida en 6 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-143">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-144">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-146">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre está establecida en 6 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-148">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-150">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="3a1ea-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="3a1ea-151">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-152">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-152">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-153">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-155">Matriz de cadenas de forma libre que proporcionan explicaciones más detalladas para cualquiera de las características del acelerador de vídeo indicadas en la matriz de propiedades **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="3a1ea-155">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** property array.</span></span> <span data-ttu-id="3a1ea-156">Cada entrada de esta matriz está relacionada con la entrada de la matriz de propiedades **AcceleratorCapabilities** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-156">Each entry of this array is related to the entry in the **AcceleratorCapabilities** property array that is located at the same index.</span></span> <span data-ttu-id="3a1ea-157">Esta propiedad se hereda de [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))y siempre está establecida en "Acelerador de gráficos".</span><span class="sxs-lookup"><span data-stu-id="3a1ea-157">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to "Graphics Accelerator".</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-158">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-161">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-161">A short description of the object.</span></span> <span data-ttu-id="3a1ea-162">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "controlador de pantalla".</span><span class="sxs-lookup"><span data-stu-id="3a1ea-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Display Controller".</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-163">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-163">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-164">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-166">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-166">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="3a1ea-167">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-167">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3a1ea-168">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-168">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3a1ea-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="3a1ea-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3a1ea-176">)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3a1ea-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-178">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-180">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-180">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3a1ea-181">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "MSVM \_ SyntheticDisplayController".</span><span class="sxs-lookup"><span data-stu-id="3a1ea-181">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_SyntheticDisplayController".</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-182">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-182">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-185">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-185">A description of the object.</span></span> <span data-ttu-id="3a1ea-186">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "controlador de pantalla sintética de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="3a1ea-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Synthetic Display Controller".</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-187">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-187">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-188">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-190">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-190">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="3a1ea-191">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3a1ea-192">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3a1ea-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="3a1ea-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3a1ea-201">)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-201">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3a1ea-202">**ID**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-202">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-205">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="3a1ea-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-209">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-209">A display name for the object.</span></span> <span data-ttu-id="3a1ea-210">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "controlador de pantalla" de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Display Controller" by default.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-212">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-214">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-214">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="3a1ea-215">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-216">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-216">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-219">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-219">The enabled and disabled states of an element.</span></span> <span data-ttu-id="3a1ea-220">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-220">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="3a1ea-221">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada) o 3 (deshabilitada).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-221">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled) or 3 (Disabled).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-222">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-222">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-223">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-225">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-225">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-226">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-226">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-229">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-229">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-230">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-230">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-231">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-231">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-233">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-233">The current health of the element.</span></span> <span data-ttu-id="3a1ea-234">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subelementos.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-234">This attribute expresses the health of this element but not necessarily that of its subelements.</span></span> <span data-ttu-id="3a1ea-235">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-235">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="3a1ea-236">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-237">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-237">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-238">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-238">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-240">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-240">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-241">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-241">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-242">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-242">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-244">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-244">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="3a1ea-245">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-249">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-250">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3a1ea-251">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-252">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-252">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-253">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-253">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-255">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-256">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-256">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-257">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-257">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-259">Cantidad máxima de memoria admitida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-259">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="3a1ea-260">Esta propiedad se hereda de [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))y siempre está establecida en 4.194.304 (0x400000).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-260">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 4,194,304 (0x400000).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-261">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-261">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-262">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-264">Número máximo de entidades directamente direccionables admitidas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-264">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="3a1ea-265">Se debe utilizar un valor de 0 si el número es desconocido o ilimitado.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-265">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="3a1ea-266">Protocolo usado por el controlador para tener acceso a los dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-266">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="3a1ea-267">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller)y siempre está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-267">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-268">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-268">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-269">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-271">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-272">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-272">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-273">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-275">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-275">The label by which the object is known.</span></span> <span data-ttu-id="3a1ea-276">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y es igual que la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="3a1ea-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-277">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-277">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-278">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-280">El número de páginas de vídeo admitidas dadas las resoluciones actuales y la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-280">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="3a1ea-281">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85))y siempre se establece en 1024.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-281">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 1024.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-282">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-282">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-283">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-285">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="3a1ea-285">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="3a1ea-286">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-286">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3a1ea-287">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3a1ea-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="3a1ea-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3a1ea-307">)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-307">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3a1ea-308">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-308">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-309">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-311">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-311">The current statuses of the object.</span></span> <span data-ttu-id="3a1ea-312">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-313">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-313">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-314">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-316">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-316">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="3a1ea-317">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-317">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="3a1ea-318">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-319">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-319">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-320">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-320">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-322">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-322">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-323">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-323">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-326">Cadena que describe el tipo de arquitectura de vídeo cuando la propiedad **videoarchitecture** es 1 ("Other").</span><span class="sxs-lookup"><span data-stu-id="3a1ea-326">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="3a1ea-327">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-327">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-328">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-328">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-329">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-331">El tipo de memoria de vídeo cuando la propiedad **VideoMemoryType** de la instancia es 1 (otra).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-331">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="3a1ea-332">Esta propiedad se hereda de [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-332">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-333">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-333">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-334">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-334">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-336">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-336">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-337">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-337">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-338">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-338">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-340">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-341">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-341">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-342">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-344">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-345">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-345">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-346">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-348">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-348">Provides high level status information.</span></span> <span data-ttu-id="3a1ea-349">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-349">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="3a1ea-350">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-350">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3a1ea-351">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-351">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3a1ea-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-353"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-353"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-354"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-354"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-355"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-355"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-356"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-356"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-357"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="3a1ea-357"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3a1ea-358">)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-358">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3a1ea-359">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-359">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-360">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-362">Una cadena que proporciona más información relacionada con el protocolo compatible con el controlador.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-362">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="3a1ea-363">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller)y siempre está establecida en "vídeo".</span><span class="sxs-lookup"><span data-stu-id="3a1ea-363">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to "Video".</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-364">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-364">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-365">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-365">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-367">Protocolo usado por el controlador para tener acceso a los dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-367">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="3a1ea-368">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller)y siempre está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-368">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-369">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-369">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-370">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-372">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-372">The last requested or desired state for the element.</span></span> <span data-ttu-id="3a1ea-373">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-373">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="3a1ea-374">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-374">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="3a1ea-375">Una instancia concreta de [**\_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no ser compatible con **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-375">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="3a1ea-376">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-376">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="3a1ea-377">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM** y está establecida en 2 (habilitado), 3 (deshabilitado) o 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-377">This property is inherited from **CIM\_EnabledLogicalElement**, and it is set to 2 (Enabled), 3 (Disabled), or 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-378">**Estado**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-379">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-381">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-381">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-382">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-382">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-383">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-383">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-384">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-385">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="3a1ea-385">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="3a1ea-386">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "OK".</span><span class="sxs-lookup"><span data-stu-id="3a1ea-386">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-387">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-387">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-388">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-388">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-389">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-390">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-390">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-391">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-391">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-392">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-394">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-394">The scoping system's creation class name.</span></span> <span data-ttu-id="3a1ea-395">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="3a1ea-395">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-396">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-396">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-397">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-398">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-399">Identificador único de la máquina virtual de ámbito.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-399">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="3a1ea-400">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-401">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-401">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-402">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-402">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-404">La última vez que se encendió la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-404">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="3a1ea-405">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-405">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-406">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-406">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-407">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-407">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-409">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-409">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="3a1ea-410">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-410">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-411">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-411">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-412">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-412">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-414">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-414">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-415">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-415">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-416">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-417">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-418">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-418">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="3a1ea-419">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-419">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-420">**Videoarquitectura**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-420">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-421">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-423">Especifica la arquitectura de vídeo del controlador de pantalla utilizada para generar la señal de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-423">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="3a1ea-424">Normalmente, un procesador de vídeo dedicado genera la señal de vídeo de acuerdo con la arquitectura especificada.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-424">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="3a1ea-425">Es un indicador de la capacidad de resolución máxima del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-425">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="3a1ea-426">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-426">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="3a1ea-427"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-427"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-428"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-428"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-429"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-429"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-430"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-430"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-431"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-431"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-432"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-432"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-433"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-433"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-434"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-434"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-435"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-435"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-436"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-436"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-437"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-437"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-438"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Búfer de trama lineal** (11)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-438"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-439"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-439"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-440"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-440"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-441"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="3a1ea-441"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3a1ea-442">)</span><span class="sxs-lookup"><span data-stu-id="3a1ea-442">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3a1ea-443">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-443">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-444">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-444">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-445">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-446">El tipo de memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-446">The type of video memory.</span></span> <span data-ttu-id="3a1ea-447">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85))y siempre está establecida en 2 (VRAM).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-447">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 2 (VRAM).</span></span>

</dd> <dt>

<span data-ttu-id="3a1ea-448">**Videoprocesador**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-448">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a1ea-449">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-449">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a1ea-450">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a1ea-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a1ea-451">Cadena que describe el procesador o controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-451">A string that describes the video processor/controller.</span></span> <span data-ttu-id="3a1ea-452">Esta propiedad se hereda de [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))y siempre está establecida en "procesador de vídeo sintético".</span><span class="sxs-lookup"><span data-stu-id="3a1ea-452">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to "Synthetic Video Processor".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a1ea-453">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a1ea-453">Remarks</span></span>

<span data-ttu-id="3a1ea-454">El acceso a la clase **MSVM \_ SyntheticDisplayController** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="3a1ea-454">Access to the **Msvm\_SyntheticDisplayController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3a1ea-455">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3a1ea-455">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a1ea-456">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a1ea-456">Requirements</span></span>



| <span data-ttu-id="3a1ea-457">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a1ea-457">Requirement</span></span> | <span data-ttu-id="3a1ea-458">Value</span><span class="sxs-lookup"><span data-stu-id="3a1ea-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a1ea-459">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a1ea-459">Minimum supported client</span></span><br/> | <span data-ttu-id="3a1ea-460">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a1ea-460">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3a1ea-461">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a1ea-461">Minimum supported server</span></span><br/> | <span data-ttu-id="3a1ea-462">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a1ea-462">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a1ea-463">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3a1ea-463">Namespace</span></span><br/>                | <span data-ttu-id="3a1ea-464">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3a1ea-464">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3a1ea-465">MOF</span><span class="sxs-lookup"><span data-stu-id="3a1ea-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a1ea-466"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a1ea-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a1ea-467">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3a1ea-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a1ea-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a1ea-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3a1ea-469">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a1ea-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a1ea-470">**\_DISPLAYCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="3a1ea-470">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> <dt>

<span data-ttu-id="3a1ea-471">[**\_DISPLAYCONTROLLER CIM**](/previous-versions//cc136810(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3a1ea-471">[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3a1ea-472">Clases de vídeo</span><span class="sxs-lookup"><span data-stu-id="3a1ea-472">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

