---
description: Representa el estado del controlador S3 emulado que se encuentra en cada configuración de máquina virtual.
ms.assetid: 194E0195-1AFF-4298-8000-2249495818C2
title: Clase Msvm_S3DisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_S3DisplayController
- Msvm_S3DisplayController.SetPowerState
- Msvm_S3DisplayController.EnableDevice
- Msvm_S3DisplayController.OnlineDevice
- Msvm_S3DisplayController.QuiesceDevice
- Msvm_S3DisplayController.SaveProperties
- Msvm_S3DisplayController.RestoreProperties
- Msvm_S3DisplayController.InstanceID
- Msvm_S3DisplayController.Caption
- Msvm_S3DisplayController.Description
- Msvm_S3DisplayController.ElementName
- Msvm_S3DisplayController.InstallDate
- Msvm_S3DisplayController.Name
- Msvm_S3DisplayController.OperationalStatus
- Msvm_S3DisplayController.StatusDescriptions
- Msvm_S3DisplayController.Status
- Msvm_S3DisplayController.HealthState
- Msvm_S3DisplayController.CommunicationStatus
- Msvm_S3DisplayController.DetailedStatus
- Msvm_S3DisplayController.OperatingStatus
- Msvm_S3DisplayController.PrimaryStatus
- Msvm_S3DisplayController.EnabledState
- Msvm_S3DisplayController.OtherEnabledState
- Msvm_S3DisplayController.RequestedState
- Msvm_S3DisplayController.EnabledDefault
- Msvm_S3DisplayController.TimeOfLastStateChange
- Msvm_S3DisplayController.AvailableRequestedStates
- Msvm_S3DisplayController.TransitioningToState
- Msvm_S3DisplayController.SystemCreationClassName
- Msvm_S3DisplayController.SystemName
- Msvm_S3DisplayController.CreationClassName
- Msvm_S3DisplayController.DeviceID
- Msvm_S3DisplayController.PowerManagementSupported
- Msvm_S3DisplayController.PowerManagementCapabilities
- Msvm_S3DisplayController.Availability
- Msvm_S3DisplayController.StatusInfo
- Msvm_S3DisplayController.LastErrorCode
- Msvm_S3DisplayController.ErrorDescription
- Msvm_S3DisplayController.ErrorCleared
- Msvm_S3DisplayController.OtherIdentifyingInfo
- Msvm_S3DisplayController.PowerOnHours
- Msvm_S3DisplayController.TotalPowerOnHours
- Msvm_S3DisplayController.IdentifyingDescriptions
- Msvm_S3DisplayController.AdditionalAvailability
- Msvm_S3DisplayController.MaxQuiesceTime
- Msvm_S3DisplayController.TimeOfLastReset
- Msvm_S3DisplayController.ProtocolSupported
- Msvm_S3DisplayController.MaxNumberControlled
- Msvm_S3DisplayController.ProtocolDescription
- Msvm_S3DisplayController.VideoProcessor
- Msvm_S3DisplayController.VideoMemoryType
- Msvm_S3DisplayController.OtherVideoMemoryType
- Msvm_S3DisplayController.NumberOfVideoPages
- Msvm_S3DisplayController.MaxMemorySupported
- Msvm_S3DisplayController.AcceleratorCapabilities
- Msvm_S3DisplayController.CapabilityDescriptions
- Msvm_S3DisplayController.OtherVideoArchitecture
- Msvm_S3DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a4195ff8947bf92d8e4af3a95df320ed950ab21e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156944"
---
# <a name="msvm_s3displaycontroller-class"></a><span data-ttu-id="79a21-103">MSVM \_ S3DisplayController (clase)</span><span class="sxs-lookup"><span data-stu-id="79a21-103">Msvm\_S3DisplayController class</span></span>

<span data-ttu-id="79a21-104">Representa el estado del controlador S3 emulado que se encuentra en cada configuración de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79a21-104">Represents the state of the emulated S3 controller that is present in each virtual machine configuration.</span></span> <span data-ttu-id="79a21-105">Solo un controlador de pantalla puede estar activo en una máquina virtual en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="79a21-105">Only one display controller can be active in a virtual machine at any time.</span></span>

> [!Note]  
> <span data-ttu-id="79a21-106">Esta clase solo se aplica a las máquinas virtuales de generación 1.</span><span class="sxs-lookup"><span data-stu-id="79a21-106">This class only applies to generation 1 virtual machines.</span></span>

 

<span data-ttu-id="79a21-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="79a21-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="79a21-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79a21-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_S3DisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Emulated Display Controller";
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
  string   EnabledState = 3;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_S3DisplayController";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Virtual S3 Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 32768;
  uint32   MaxMemorySupported = 134217728;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="79a21-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="79a21-109">Members</span></span>

<span data-ttu-id="79a21-110">La clase **MSVM \_ S3DisplayController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="79a21-110">The **Msvm\_S3DisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="79a21-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="79a21-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="79a21-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79a21-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="79a21-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="79a21-113">Methods</span></span>

<span data-ttu-id="79a21-114">La clase **MSVM \_ S3DisplayController** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="79a21-114">The **Msvm\_S3DisplayController** class has these methods.</span></span>



| <span data-ttu-id="79a21-115">Método</span><span class="sxs-lookup"><span data-stu-id="79a21-115">Method</span></span>                                                                    | <span data-ttu-id="79a21-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="79a21-116">Description</span></span>                              |
|:--------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="79a21-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="79a21-117">**EnableDevice**</span></span>                                                          | <span data-ttu-id="79a21-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="79a21-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="79a21-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="79a21-119">**OnlineDevice**</span></span>                                                          | <span data-ttu-id="79a21-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="79a21-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="79a21-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="79a21-121">**QuiesceDevice**</span></span>                                                         | <span data-ttu-id="79a21-122">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="79a21-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="79a21-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="79a21-123">**RequestStateChange**</span></span>](msvm-s3displaycontroller-requeststatechange.md) | <span data-ttu-id="79a21-124">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="79a21-124">Requests a state change.</span></span> <br/>     |
| [<span data-ttu-id="79a21-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="79a21-125">**Reset**</span></span>](msvm-s3displaycontroller-reset.md)                           | <span data-ttu-id="79a21-126">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="79a21-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="79a21-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="79a21-127">**RestoreProperties**</span></span>                                                     | <span data-ttu-id="79a21-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="79a21-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="79a21-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="79a21-129">**SaveProperties**</span></span>                                                        | <span data-ttu-id="79a21-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="79a21-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="79a21-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="79a21-131">**SetPowerState**</span></span>                                                         | <span data-ttu-id="79a21-132">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="79a21-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="79a21-133">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79a21-133">Properties</span></span>

<span data-ttu-id="79a21-134">La clase **MSVM \_ S3DisplayController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="79a21-134">The **Msvm\_S3DisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79a21-135">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="79a21-135">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-136">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79a21-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-138">Las capacidades de gráficos y 3D del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="79a21-138">The graphics and 3D capabilities of the display controller.</span></span> <span data-ttu-id="79a21-139">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79a21-139">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="79a21-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-141">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79a21-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-143">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79a21-143">Any additional availability and status of the device.</span></span> <span data-ttu-id="79a21-144">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="79a21-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-145">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="79a21-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-146">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-148">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79a21-148">The primary availability and status of the device.</span></span> <span data-ttu-id="79a21-149">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="79a21-149">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="79a21-150">Value</span><span class="sxs-lookup"><span data-stu-id="79a21-150">Value</span></span>                                                                        | <span data-ttu-id="79a21-151">Significado</span><span class="sxs-lookup"><span data-stu-id="79a21-151">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="79a21-152"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="79a21-152"><dt>6</dt></span></span> </dl> | <span data-ttu-id="79a21-153">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="79a21-153">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="79a21-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="79a21-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-155">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79a21-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-157">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="79a21-157">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="79a21-158">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="79a21-158">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="79a21-159">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="79a21-159">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-160">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="79a21-160">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79a21-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-162">Una matriz de cadenas de forma libre que proporcionan explicaciones más detalladas para cualquiera de las características del acelerador de vídeo indicadas en la matriz **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="79a21-162">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="79a21-163">Cada entrada de esta matriz está relacionada con la entrada de la matriz **AcceleratorCapabilities** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="79a21-163">Each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span> <span data-ttu-id="79a21-164">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79a21-164">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="79a21-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-168">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="79a21-168">A short description of the object.</span></span> <span data-ttu-id="79a21-169">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="79a21-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-170">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="79a21-170">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-171">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-173">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="79a21-173">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="79a21-174">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="79a21-174">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="79a21-175">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="79a21-175">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="79a21-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="79a21-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="79a21-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="79a21-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="79a21-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="79a21-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="79a21-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="79a21-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="79a21-183">)</span><span class="sxs-lookup"><span data-stu-id="79a21-183">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="79a21-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="79a21-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-185">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-187">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="79a21-187">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="79a21-188">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "MSVM \_ S3DisplayController".</span><span class="sxs-lookup"><span data-stu-id="79a21-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_S3DisplayController".</span></span>

</dd> <dt>

<span data-ttu-id="79a21-189">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="79a21-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-192">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="79a21-192">A description of the object.</span></span> <span data-ttu-id="79a21-193">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="79a21-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="79a21-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-195">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-197">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="79a21-197">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="79a21-198">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="79a21-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="79a21-199">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="79a21-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="79a21-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="79a21-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="79a21-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="79a21-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="79a21-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="79a21-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="79a21-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="79a21-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="79a21-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="79a21-208">)</span><span class="sxs-lookup"><span data-stu-id="79a21-208">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="79a21-209">**ID**</span><span class="sxs-lookup"><span data-stu-id="79a21-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-212">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79a21-212">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="79a21-213">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="79a21-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="79a21-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-215">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-217">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="79a21-217">A display name for the object.</span></span> <span data-ttu-id="79a21-218">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="79a21-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-219">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="79a21-219">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-220">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-222">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="79a21-222">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="79a21-223">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79a21-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="79a21-224">Value</span><span class="sxs-lookup"><span data-stu-id="79a21-224">Value</span></span>                                                                        | <span data-ttu-id="79a21-225">Significado</span><span class="sxs-lookup"><span data-stu-id="79a21-225">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="79a21-226"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="79a21-226"><dt>2</dt></span></span> </dl> | <span data-ttu-id="79a21-227">habilitado</span><span class="sxs-lookup"><span data-stu-id="79a21-227">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="79a21-228"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="79a21-228"><dt>3</dt></span></span> </dl> | <span data-ttu-id="79a21-229">Disabled</span><span class="sxs-lookup"><span data-stu-id="79a21-229">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="79a21-230">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="79a21-230">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-231">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-233">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="79a21-233">The enabled and disabled states of an element.</span></span> <span data-ttu-id="79a21-234">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="79a21-234">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="79a21-235">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada) o 3 (deshabilitada).</span><span class="sxs-lookup"><span data-stu-id="79a21-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="79a21-236">Value</span><span class="sxs-lookup"><span data-stu-id="79a21-236">Value</span></span>                                                                        | <span data-ttu-id="79a21-237">Significado</span><span class="sxs-lookup"><span data-stu-id="79a21-237">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="79a21-238"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="79a21-238"><dt>2</dt></span></span> </dl> | <span data-ttu-id="79a21-239">habilitado</span><span class="sxs-lookup"><span data-stu-id="79a21-239">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="79a21-240"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="79a21-240"><dt>3</dt></span></span> </dl> | <span data-ttu-id="79a21-241">Disabled</span><span class="sxs-lookup"><span data-stu-id="79a21-241">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="79a21-242">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="79a21-242">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-243">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="79a21-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-245">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="79a21-245">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="79a21-246">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="79a21-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79a21-247">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="79a21-247">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-248">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-250">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="79a21-250">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="79a21-251">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="79a21-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79a21-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="79a21-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-253">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-255">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="79a21-255">The current health of the element.</span></span> <span data-ttu-id="79a21-256">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="79a21-256">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="79a21-257">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="79a21-257">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="79a21-258">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="79a21-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="79a21-259">Value</span><span class="sxs-lookup"><span data-stu-id="79a21-259">Value</span></span>                                                                        | <span data-ttu-id="79a21-260">Significado</span><span class="sxs-lookup"><span data-stu-id="79a21-260">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="79a21-261"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="79a21-261"><dt>5</dt></span></span> </dl> | <span data-ttu-id="79a21-262">Aceptar</span><span class="sxs-lookup"><span data-stu-id="79a21-262">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="79a21-263">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="79a21-263">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-264">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="79a21-264">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79a21-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-266">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="79a21-266">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="79a21-267">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="79a21-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="79a21-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="79a21-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-269">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="79a21-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-271">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79a21-271">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="79a21-272">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="79a21-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-273">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="79a21-273">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-274">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79a21-276">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="79a21-276">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="79a21-277">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="79a21-277">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="79a21-278">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="79a21-278">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-279">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="79a21-279">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-280">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79a21-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-282">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79a21-282">The last error code reported by the logical device.</span></span> <span data-ttu-id="79a21-283">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="79a21-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79a21-284">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="79a21-284">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-285">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79a21-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-287">Cantidad máxima de memoria admitida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="79a21-287">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="79a21-288">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79a21-288">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-289">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="79a21-289">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-290">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79a21-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-292">Número máximo de entidades directamente direccionables admitidas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="79a21-292">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="79a21-293">Se debe utilizar un valor de 0 si el número es desconocido o ilimitado.</span><span class="sxs-lookup"><span data-stu-id="79a21-293">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="79a21-294">Protocolo usado por el controlador para tener acceso a los dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="79a21-294">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="79a21-295">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="79a21-295">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-296">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="79a21-296">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-297">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79a21-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-299">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="79a21-299">This property has been deprecated.</span></span> <span data-ttu-id="79a21-300">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="79a21-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-301">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="79a21-301">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-302">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-304">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="79a21-304">The label by which the object is known.</span></span> <span data-ttu-id="79a21-305">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="79a21-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-306">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="79a21-306">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-307">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79a21-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-309">El número de páginas de vídeo admitidas dadas las resoluciones actuales y la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="79a21-309">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="79a21-310">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79a21-310">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-311">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="79a21-311">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-312">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-312">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-314">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="79a21-314">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="79a21-315">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="79a21-315">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="79a21-316">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="79a21-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="79a21-317"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="79a21-317"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-318"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="79a21-318"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-319"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="79a21-319"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-320"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="79a21-320"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-321"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="79a21-321"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-322"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="79a21-322"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-323"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="79a21-323"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-324"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="79a21-324"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-325"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="79a21-325"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-326"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="79a21-326"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-327"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="79a21-327"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-328"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="79a21-328"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-329"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="79a21-329"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-330"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="79a21-330"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-331"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="79a21-331"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-332"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="79a21-332"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-333"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="79a21-333"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-334"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="79a21-334"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-335"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="79a21-335"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="79a21-336">)</span><span class="sxs-lookup"><span data-stu-id="79a21-336">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="79a21-337">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="79a21-337">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-338">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79a21-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-340">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="79a21-340">The current statuses of the object.</span></span> <span data-ttu-id="79a21-341">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="79a21-341">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-342">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="79a21-342">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-343">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-345">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="79a21-345">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="79a21-346">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="79a21-346">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="79a21-347">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="79a21-347">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="79a21-348">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="79a21-348">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-349">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="79a21-349">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79a21-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-351">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79a21-351">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="79a21-352">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="79a21-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="79a21-353">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="79a21-353">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-354">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-356">Cadena que describe el tipo de arquitectura de vídeo cuando la propiedad **videoarchitecture** es 1 ("Other").</span><span class="sxs-lookup"><span data-stu-id="79a21-356">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="79a21-357">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79a21-357">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-358">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="79a21-358">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-359">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-360">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-361">El tipo de memoria de vídeo cuando la propiedad **VideoMemoryType** de la instancia es 1 (otra).</span><span class="sxs-lookup"><span data-stu-id="79a21-361">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="79a21-362">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79a21-362">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-363">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="79a21-363">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-364">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-364">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79a21-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-366">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79a21-366">The power management capabilities of the device.</span></span> <span data-ttu-id="79a21-367">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="79a21-367">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79a21-368">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="79a21-368">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-369">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="79a21-369">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-371">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="79a21-371">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="79a21-372">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="79a21-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79a21-373">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="79a21-373">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-374">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79a21-374">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-376">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="79a21-376">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="79a21-377">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="79a21-377">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79a21-378">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="79a21-378">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-379">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-381">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="79a21-381">Provides high level status information.</span></span> <span data-ttu-id="79a21-382">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="79a21-382">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="79a21-383">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="79a21-383">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="79a21-384">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="79a21-384">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="79a21-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="79a21-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-386"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="79a21-386"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-387"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="79a21-387"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-388"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="79a21-388"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-389"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="79a21-389"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-390"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="79a21-390"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="79a21-391">)</span><span class="sxs-lookup"><span data-stu-id="79a21-391">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="79a21-392">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="79a21-392">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-393">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-395">Una cadena que proporciona más información relacionada con el protocolo compatible con el controlador.</span><span class="sxs-lookup"><span data-stu-id="79a21-395">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="79a21-396">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="79a21-396">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-397">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="79a21-397">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-398">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-400">Protocolo usado por el controlador para tener acceso a los dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="79a21-400">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="79a21-401">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="79a21-401">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-402">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="79a21-402">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-403">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-405">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="79a21-405">The last requested or desired state for the element.</span></span> <span data-ttu-id="79a21-406">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="79a21-406">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="79a21-407">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="79a21-407">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="79a21-408">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79a21-408">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="79a21-409">Value</span><span class="sxs-lookup"><span data-stu-id="79a21-409">Value</span></span>                                                                         | <span data-ttu-id="79a21-410">Significado</span><span class="sxs-lookup"><span data-stu-id="79a21-410">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="79a21-411"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="79a21-411"><dt>12</dt></span></span> </dl> | <span data-ttu-id="79a21-412">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="79a21-412">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="79a21-413">**Estado**</span><span class="sxs-lookup"><span data-stu-id="79a21-413">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-414">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-415">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-416">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="79a21-416">The current status of the object.</span></span> <span data-ttu-id="79a21-417">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="79a21-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79a21-418">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="79a21-418">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-419">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="79a21-419">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="79a21-420">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-421">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="79a21-421">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="79a21-422">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "OK".</span><span class="sxs-lookup"><span data-stu-id="79a21-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="79a21-423">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="79a21-423">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-424">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-425">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-426">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79a21-426">The current state of the logical device.</span></span> <span data-ttu-id="79a21-427">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="79a21-427">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79a21-428">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="79a21-428">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-429">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-430">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-431">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="79a21-431">The scoping system's creation class name.</span></span> <span data-ttu-id="79a21-432">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="79a21-432">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="79a21-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-434">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-436">Identificador único de la máquina virtual de ámbito.</span><span class="sxs-lookup"><span data-stu-id="79a21-436">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="79a21-437">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="79a21-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-438">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="79a21-438">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-439">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="79a21-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-441">La última vez que se encendió la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79a21-441">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="79a21-442">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="79a21-442">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-443">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="79a21-443">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-444">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="79a21-444">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-445">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-446">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="79a21-446">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="79a21-447">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79a21-447">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-448">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="79a21-448">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-449">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79a21-449">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-450">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-451">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79a21-451">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="79a21-452">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="79a21-452">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="79a21-453">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="79a21-453">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-454">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-455">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-456">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="79a21-456">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="79a21-457">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="79a21-457">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="79a21-458">**Videoarquitectura**</span><span class="sxs-lookup"><span data-stu-id="79a21-458">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-459">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-460">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-461">Especifica la arquitectura de vídeo del controlador de pantalla utilizada para generar la señal de vídeo.</span><span class="sxs-lookup"><span data-stu-id="79a21-461">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="79a21-462">Normalmente, un procesador de vídeo dedicado genera la señal de vídeo de acuerdo con la arquitectura especificada.</span><span class="sxs-lookup"><span data-stu-id="79a21-462">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="79a21-463">Es un indicador de la capacidad de resolución máxima del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="79a21-463">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="79a21-464">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79a21-464">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="79a21-465"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="79a21-465"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-466"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="79a21-466"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-467"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="79a21-467"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-468"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="79a21-468"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-469"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="79a21-469"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-470"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="79a21-470"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-471"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="79a21-471"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-472"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="79a21-472"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-473"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="79a21-473"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-474"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="79a21-474"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-475"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="79a21-475"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-476"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Búfer de trama lineal** (11)</span><span class="sxs-lookup"><span data-stu-id="79a21-476"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-477"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="79a21-477"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-478"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="79a21-478"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="79a21-479"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="79a21-479"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="79a21-480">)</span><span class="sxs-lookup"><span data-stu-id="79a21-480">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="79a21-481">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="79a21-481">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-482">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79a21-482">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-483">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-484">El tipo de memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="79a21-484">The type of video memory.</span></span> <span data-ttu-id="79a21-485">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79a21-485">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="79a21-486">**Videoprocesador**</span><span class="sxs-lookup"><span data-stu-id="79a21-486">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79a21-487">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79a21-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79a21-488">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79a21-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79a21-489">Cadena que describe el procesador o controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="79a21-489">A string that describes the video processor/controller.</span></span> <span data-ttu-id="79a21-490">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79a21-490">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79a21-491">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79a21-491">Remarks</span></span>

<span data-ttu-id="79a21-492">El acceso a la clase **MSVM \_ S3DisplayController** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="79a21-492">Access to the **Msvm\_S3DisplayController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="79a21-493">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="79a21-493">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="79a21-494">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79a21-494">Requirements</span></span>



| <span data-ttu-id="79a21-495">Requisito</span><span class="sxs-lookup"><span data-stu-id="79a21-495">Requirement</span></span> | <span data-ttu-id="79a21-496">Value</span><span class="sxs-lookup"><span data-stu-id="79a21-496">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79a21-497">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79a21-497">Minimum supported client</span></span><br/> | <span data-ttu-id="79a21-498">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="79a21-498">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="79a21-499">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79a21-499">Minimum supported server</span></span><br/> | <span data-ttu-id="79a21-500">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="79a21-500">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79a21-501">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="79a21-501">Namespace</span></span><br/>                | <span data-ttu-id="79a21-502">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="79a21-502">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="79a21-503">MOF</span><span class="sxs-lookup"><span data-stu-id="79a21-503">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79a21-504"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79a21-504"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79a21-505">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79a21-505">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79a21-506"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79a21-506"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="79a21-507">Vea también</span><span class="sxs-lookup"><span data-stu-id="79a21-507">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79a21-508">**\_DISPLAYCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="79a21-508">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> <dt>

<span data-ttu-id="79a21-509">[**\_DISPLAYCONTROLLER CIM**](/previous-versions//cc136810(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79a21-509">[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="79a21-510">Clases de vídeo</span><span class="sxs-lookup"><span data-stu-id="79a21-510">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

