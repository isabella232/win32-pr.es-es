---
description: Representa el controlador de pantalla sintético 3D que se asigna a una máquina virtual.
ms.assetid: 5679668B-7D0B-421C-92B6-8A320090DFF7
title: Clase Msvm_Synthetic3DDisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayController
- Msvm_Synthetic3DDisplayController.RequestStateChange
- Msvm_Synthetic3DDisplayController.SetPowerState
- Msvm_Synthetic3DDisplayController.Reset
- Msvm_Synthetic3DDisplayController.EnableDevice
- Msvm_Synthetic3DDisplayController.OnlineDevice
- Msvm_Synthetic3DDisplayController.QuiesceDevice
- Msvm_Synthetic3DDisplayController.SaveProperties
- Msvm_Synthetic3DDisplayController.RestoreProperties
- Msvm_Synthetic3DDisplayController.InstanceID
- Msvm_Synthetic3DDisplayController.Caption
- Msvm_Synthetic3DDisplayController.Description
- Msvm_Synthetic3DDisplayController.ElementName
- Msvm_Synthetic3DDisplayController.InstallDate
- Msvm_Synthetic3DDisplayController.Name
- Msvm_Synthetic3DDisplayController.OperationalStatus
- Msvm_Synthetic3DDisplayController.StatusDescriptions
- Msvm_Synthetic3DDisplayController.Status
- Msvm_Synthetic3DDisplayController.HealthState
- Msvm_Synthetic3DDisplayController.CommunicationStatus
- Msvm_Synthetic3DDisplayController.DetailedStatus
- Msvm_Synthetic3DDisplayController.OperatingStatus
- Msvm_Synthetic3DDisplayController.PrimaryStatus
- Msvm_Synthetic3DDisplayController.EnabledState
- Msvm_Synthetic3DDisplayController.OtherEnabledState
- Msvm_Synthetic3DDisplayController.RequestedState
- Msvm_Synthetic3DDisplayController.EnabledDefault
- Msvm_Synthetic3DDisplayController.TimeOfLastStateChange
- Msvm_Synthetic3DDisplayController.AvailableRequestedStates
- Msvm_Synthetic3DDisplayController.TransitioningToState
- Msvm_Synthetic3DDisplayController.SystemCreationClassName
- Msvm_Synthetic3DDisplayController.SystemName
- Msvm_Synthetic3DDisplayController.CreationClassName
- Msvm_Synthetic3DDisplayController.DeviceID
- Msvm_Synthetic3DDisplayController.PowerManagementSupported
- Msvm_Synthetic3DDisplayController.PowerManagementCapabilities
- Msvm_Synthetic3DDisplayController.Availability
- Msvm_Synthetic3DDisplayController.StatusInfo
- Msvm_Synthetic3DDisplayController.LastErrorCode
- Msvm_Synthetic3DDisplayController.ErrorDescription
- Msvm_Synthetic3DDisplayController.ErrorCleared
- Msvm_Synthetic3DDisplayController.PowerOnHours
- Msvm_Synthetic3DDisplayController.TotalPowerOnHours
- Msvm_Synthetic3DDisplayController.OtherIdentifyingInfo
- Msvm_Synthetic3DDisplayController.IdentifyingDescriptions
- Msvm_Synthetic3DDisplayController.AdditionalAvailability
- Msvm_Synthetic3DDisplayController.MaxQuiesceTime
- Msvm_Synthetic3DDisplayController.TimeOfLastReset
- Msvm_Synthetic3DDisplayController.ProtocolSupported
- Msvm_Synthetic3DDisplayController.MaxNumberControlled
- Msvm_Synthetic3DDisplayController.ProtocolDescription
- Msvm_Synthetic3DDisplayController.VideoProcessor
- Msvm_Synthetic3DDisplayController.VideoMemoryType
- Msvm_Synthetic3DDisplayController.OtherVideoMemoryType
- Msvm_Synthetic3DDisplayController.NumberOfVideoPages
- Msvm_Synthetic3DDisplayController.MaxMemorySupported
- Msvm_Synthetic3DDisplayController.AcceleratorCapabilities
- Msvm_Synthetic3DDisplayController.CapabilityDescriptions
- Msvm_Synthetic3DDisplayController.OtherVideoArchitecture
- Msvm_Synthetic3DDisplayController.VideoArchitecture
- Msvm_Synthetic3DDisplayController.AllocatedGPU
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0cd102fe29cf34aa0930ca264c8820868da7daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687265"
---
# <a name="msvm_synthetic3ddisplaycontroller-class"></a><span data-ttu-id="85ef8-103">MSVM \_ Synthetic3DDisplayController (clase)</span><span class="sxs-lookup"><span data-stu-id="85ef8-103">Msvm\_Synthetic3DDisplayController class</span></span>

<span data-ttu-id="85ef8-104">Representa el controlador de pantalla sintético 3D que se asigna a una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="85ef8-104">Represents the synthetic 3-D display controller that is assigned to a virtual machine.</span></span> <span data-ttu-id="85ef8-105">Esta clase solo se usa con máquinas virtuales que usan RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="85ef8-105">This class is only used with virtual machines that use RemoteFX.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85ef8-106">Al agregar un controlador de pantalla sintético 3D a una máquina virtual, debe deshabilitar cualquier controlador de pantalla sintético ([**MSVM \_ SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)) que esté conectado a esa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="85ef8-106">When you add a synthetic 3-D display controller to a virtual machine, you must disable any synthetic display controller ([**Msvm\_SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)) that is attached to that virtual machine.</span></span>

 

<span data-ttu-id="85ef8-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="85ef8-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="85ef8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85ef8-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_Synthetic3DDisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 2048;
  uint32   MaxMemorySupported = 8388608;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
  string   AllocatedGPU;
};
```

## <a name="members"></a><span data-ttu-id="85ef8-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="85ef8-109">Members</span></span>

<span data-ttu-id="85ef8-110">La clase **MSVM \_ Synthetic3DDisplayController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="85ef8-110">The **Msvm\_Synthetic3DDisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="85ef8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="85ef8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="85ef8-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85ef8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="85ef8-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="85ef8-113">Methods</span></span>

<span data-ttu-id="85ef8-114">La clase **MSVM \_ Synthetic3DDisplayController** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="85ef8-114">The **Msvm\_Synthetic3DDisplayController** class has these methods.</span></span>



| <span data-ttu-id="85ef8-115">Método</span><span class="sxs-lookup"><span data-stu-id="85ef8-115">Method</span></span>                 | <span data-ttu-id="85ef8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="85ef8-116">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="85ef8-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="85ef8-117">**EnableDevice**</span></span>       | <span data-ttu-id="85ef8-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="85ef8-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="85ef8-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="85ef8-119">**OnlineDevice**</span></span>       | <span data-ttu-id="85ef8-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="85ef8-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="85ef8-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="85ef8-121">**QuiesceDevice**</span></span>      | <span data-ttu-id="85ef8-122">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="85ef8-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="85ef8-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="85ef8-123">**RequestStateChange**</span></span> | <span data-ttu-id="85ef8-124">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="85ef8-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="85ef8-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="85ef8-125">**Reset**</span></span>              | <span data-ttu-id="85ef8-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="85ef8-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="85ef8-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="85ef8-127">**RestoreProperties**</span></span>  | <span data-ttu-id="85ef8-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="85ef8-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="85ef8-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="85ef8-129">**SaveProperties**</span></span>     | <span data-ttu-id="85ef8-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="85ef8-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="85ef8-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="85ef8-131">**SetPowerState**</span></span>      | <span data-ttu-id="85ef8-132">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="85ef8-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="85ef8-133">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85ef8-133">Properties</span></span>

<span data-ttu-id="85ef8-134">La clase **MSVM \_ Synthetic3DDisplayController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="85ef8-134">The **Msvm\_Synthetic3DDisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85ef8-135">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="85ef8-135">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-136">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-138">Los gráficos y las capacidades 3D del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="85ef8-138">The graphics and 3-D capabilities of the display controller.</span></span> <span data-ttu-id="85ef8-139">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85ef8-139">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="85ef8-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-141">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-143">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre está establecida en 6 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="85ef8-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-144">**AllocatedGPU**</span><span class="sxs-lookup"><span data-stu-id="85ef8-144">**AllocatedGPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-147">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="85ef8-147">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-148">El identificador de la unidad de procesamiento de gráficos (GPU) física asignada a esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="85ef8-148">The identifier of the physical graphics processing unit (GPU) allocated to this virtual machine.</span></span> <span data-ttu-id="85ef8-149">Esta propiedad solo se aplica a las máquinas virtuales que usan RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="85ef8-149">This property only applies to virtual machines that use RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-150">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="85ef8-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-151">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-153">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre está establecida en 6 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="85ef8-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="85ef8-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-155">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-157">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="85ef8-157">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="85ef8-158">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="85ef8-158">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-159">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="85ef8-159">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-160">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="85ef8-160">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-162">Matriz de cadenas de forma libre que proporcionan explicaciones más detalladas para cualquiera de las características del acelerador de vídeo indicadas en la matriz de propiedades **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="85ef8-162">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** property array.</span></span> <span data-ttu-id="85ef8-163">Cada entrada de esta matriz está relacionada con la entrada de la matriz de propiedades **AcceleratorCapabilities** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="85ef8-163">Each entry of this array is related to the entry in the **AcceleratorCapabilities** property array that is located at the same index.</span></span> <span data-ttu-id="85ef8-164">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85ef8-164">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="85ef8-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-168">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="85ef8-168">A short description of the object.</span></span> <span data-ttu-id="85ef8-169">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="85ef8-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-170">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="85ef8-170">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-171">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-173">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="85ef8-173">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="85ef8-174">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="85ef8-174">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="85ef8-175">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="85ef8-175">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="85ef8-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="85ef8-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="85ef8-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="85ef8-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="85ef8-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="85ef8-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="85ef8-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="85ef8-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="85ef8-183">)</span><span class="sxs-lookup"><span data-stu-id="85ef8-183">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="85ef8-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="85ef8-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-185">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-187">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="85ef8-187">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="85ef8-188">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="85ef8-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-189">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85ef8-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-192">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="85ef8-192">A description of the object.</span></span> <span data-ttu-id="85ef8-193">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="85ef8-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="85ef8-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-195">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-197">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="85ef8-197">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="85ef8-198">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="85ef8-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="85ef8-199">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="85ef8-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="85ef8-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="85ef8-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="85ef8-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="85ef8-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="85ef8-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="85ef8-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="85ef8-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="85ef8-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="85ef8-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="85ef8-208">)</span><span class="sxs-lookup"><span data-stu-id="85ef8-208">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="85ef8-209">**ID**</span><span class="sxs-lookup"><span data-stu-id="85ef8-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-212">Identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85ef8-212">The device identifier.</span></span> <span data-ttu-id="85ef8-213">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="85ef8-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="85ef8-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-215">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-217">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="85ef8-217">A display name for the object.</span></span> <span data-ttu-id="85ef8-218">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="85ef8-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-219">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="85ef8-219">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-220">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-222">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="85ef8-222">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="85ef8-223">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="85ef8-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-224">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="85ef8-224">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-227">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="85ef8-227">The enabled and disabled states of an element.</span></span> <span data-ttu-id="85ef8-228">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="85ef8-228">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="85ef8-229">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitado) o 3 (deshabilitada).</span><span class="sxs-lookup"><span data-stu-id="85ef8-229">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to either 2 (Enabled) or 3 (Disabled).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-230">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="85ef8-230">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-231">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85ef8-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-233">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ef8-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="85ef8-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-235">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-237">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ef8-237">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-238">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="85ef8-238">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-239">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-241">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="85ef8-241">The current health of the element.</span></span> <span data-ttu-id="85ef8-242">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subelementos.</span><span class="sxs-lookup"><span data-stu-id="85ef8-242">This attribute expresses the health of this element but not necessarily that of its subelements.</span></span> <span data-ttu-id="85ef8-243">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="85ef8-243">The possible values are from 0 through 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="85ef8-244">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="85ef8-244">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-245">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="85ef8-245">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-246">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="85ef8-246">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-248">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="85ef8-248">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="85ef8-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-250">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85ef8-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-252">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="85ef8-252">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="85ef8-253">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="85ef8-253">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-254">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="85ef8-254">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-255">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-257">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="85ef8-257">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-258">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="85ef8-258">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="85ef8-259">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="85ef8-259">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-260">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="85ef8-260">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-261">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85ef8-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-263">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ef8-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-264">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="85ef8-264">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-265">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85ef8-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-266">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-267">Cantidad máxima de memoria admitida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="85ef8-267">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="85ef8-268">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85ef8-268">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-269">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="85ef8-269">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-270">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85ef8-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-271">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-272">Número máximo de entidades directamente direccionables admitidas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="85ef8-272">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="85ef8-273">Se debe utilizar un valor de 0 si el número es desconocido o ilimitado.</span><span class="sxs-lookup"><span data-stu-id="85ef8-273">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="85ef8-274">Protocolo usado por el controlador para tener acceso a los dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="85ef8-274">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="85ef8-275">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="85ef8-275">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-276">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="85ef8-276">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-277">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="85ef8-277">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-279">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ef8-279">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-280">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="85ef8-280">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-281">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-283">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="85ef8-283">The label by which the object is known.</span></span> <span data-ttu-id="85ef8-284">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="85ef8-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-285">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="85ef8-285">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-286">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="85ef8-286">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-288">El número de páginas de vídeo admitidas dadas las resoluciones actuales y la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="85ef8-288">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="85ef8-289">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85ef8-289">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-290">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="85ef8-290">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-291">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-293">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="85ef8-293">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="85ef8-294">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="85ef8-294">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="85ef8-295">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="85ef8-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="85ef8-296"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="85ef8-296"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-297"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="85ef8-297"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-298"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="85ef8-298"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-299"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="85ef8-299"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-300"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="85ef8-300"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-301"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="85ef8-301"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-302"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="85ef8-302"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-303"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="85ef8-303"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-304"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="85ef8-304"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-305"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="85ef8-305"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-306"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="85ef8-306"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-307"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="85ef8-307"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-308"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="85ef8-308"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-309"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="85ef8-309"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-310"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="85ef8-310"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-311"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="85ef8-311"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-312"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="85ef8-312"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-313"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="85ef8-313"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-314"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="85ef8-314"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="85ef8-315">)</span><span class="sxs-lookup"><span data-stu-id="85ef8-315">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="85ef8-316">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="85ef8-316">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-317">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-317">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-319">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="85ef8-319">The current statuses of the object.</span></span> <span data-ttu-id="85ef8-320">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="85ef8-320">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-321">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="85ef8-321">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-322">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-324">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="85ef8-324">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="85ef8-325">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="85ef8-325">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="85ef8-326">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="85ef8-326">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-327">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="85ef8-327">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-328">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="85ef8-328">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-330">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="85ef8-330">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-331">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="85ef8-331">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-332">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-334">Cadena que describe el tipo de arquitectura de vídeo cuando la propiedad **videoarchitecture** es 1 ("Other").</span><span class="sxs-lookup"><span data-stu-id="85ef8-334">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="85ef8-335">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85ef8-335">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-336">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="85ef8-336">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-337">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-339">El tipo de memoria de vídeo cuando la propiedad **VideoMemoryType** de la instancia es 1 (otra).</span><span class="sxs-lookup"><span data-stu-id="85ef8-339">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="85ef8-340">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85ef8-340">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-341">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="85ef8-341">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-342">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-342">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-344">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ef8-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-345">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="85ef8-345">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-346">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="85ef8-346">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-348">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ef8-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-349">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="85ef8-349">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-350">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="85ef8-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-352">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ef8-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-353">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="85ef8-353">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-354">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-354">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-356">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="85ef8-356">Provides high level status information.</span></span> <span data-ttu-id="85ef8-357">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="85ef8-357">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="85ef8-358">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="85ef8-358">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="85ef8-359">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="85ef8-359">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="85ef8-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="85ef8-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-361"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="85ef8-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="85ef8-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="85ef8-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="85ef8-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="85ef8-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="85ef8-366">)</span><span class="sxs-lookup"><span data-stu-id="85ef8-366">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="85ef8-367">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="85ef8-367">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-368">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-370">Una cadena que proporciona más información relacionada con el protocolo compatible con el controlador.</span><span class="sxs-lookup"><span data-stu-id="85ef8-370">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="85ef8-371">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="85ef8-371">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-372">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="85ef8-372">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-373">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-374">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-375">Protocolo usado por el controlador para tener acceso a los dispositivos controlados.</span><span class="sxs-lookup"><span data-stu-id="85ef8-375">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="85ef8-376">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="85ef8-376">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-377">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="85ef8-377">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-378">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-378">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-379">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-380">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="85ef8-380">The last requested or desired state for the element.</span></span> <span data-ttu-id="85ef8-381">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="85ef8-381">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="85ef8-382">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="85ef8-382">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="85ef8-383">Una instancia concreta de [**\_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no ser compatible con **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="85ef8-383">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="85ef8-384">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="85ef8-384">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="85ef8-385">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM** y siempre está establecida en 2 (habilitada), 3 (deshabilitada) o 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="85ef8-385">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 2 (Enabled), 3 (Disabled), or 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-386">**Estado**</span><span class="sxs-lookup"><span data-stu-id="85ef8-386">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-387">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-389">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ef8-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-390">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="85ef8-390">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-391">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="85ef8-391">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-392">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-393">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="85ef8-393">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="85ef8-394">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="85ef8-394">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-395">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="85ef8-395">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-396">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-398">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ef8-398">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-399">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="85ef8-399">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-400">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-401">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-402">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="85ef8-402">The scoping system's creation class name.</span></span> <span data-ttu-id="85ef8-403">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="85ef8-403">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-404">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="85ef8-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-405">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-406">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-407">Identificador único de la máquina virtual de ámbito.</span><span class="sxs-lookup"><span data-stu-id="85ef8-407">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="85ef8-408">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="85ef8-408">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-409">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="85ef8-409">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-410">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85ef8-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-411">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-412">La última vez que se encendió la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="85ef8-412">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="85ef8-413">Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="85ef8-413">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-414">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="85ef8-414">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-415">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85ef8-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-417">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="85ef8-417">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="85ef8-418">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85ef8-418">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-419">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="85ef8-419">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-420">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="85ef8-420">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-422">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="85ef8-422">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-423">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="85ef8-423">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-424">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-425">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-426">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="85ef8-426">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="85ef8-427">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="85ef8-427">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-428">**Videoarquitectura**</span><span class="sxs-lookup"><span data-stu-id="85ef8-428">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-429">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-430">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-431">Especifica la arquitectura de vídeo del controlador de pantalla utilizada para generar la señal de vídeo.</span><span class="sxs-lookup"><span data-stu-id="85ef8-431">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="85ef8-432">Normalmente, un procesador de vídeo dedicado genera la señal de vídeo de acuerdo con la arquitectura especificada.</span><span class="sxs-lookup"><span data-stu-id="85ef8-432">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="85ef8-433">Es un indicador de la capacidad de resolución máxima del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="85ef8-433">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="85ef8-434">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85ef8-434">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="85ef8-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="85ef8-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-436"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="85ef8-436"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-437"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="85ef8-437"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-438"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="85ef8-438"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-439"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="85ef8-439"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-440"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="85ef8-440"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-441"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="85ef8-441"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-442"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="85ef8-442"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-443"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="85ef8-443"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-444"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="85ef8-444"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-445"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="85ef8-445"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-446"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Búfer de trama lineal** (11)</span><span class="sxs-lookup"><span data-stu-id="85ef8-446"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-447"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="85ef8-447"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-448"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="85ef8-448"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-449"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="85ef8-449"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="85ef8-450">)</span><span class="sxs-lookup"><span data-stu-id="85ef8-450">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="85ef8-451">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="85ef8-451">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-452">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="85ef8-452">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-453">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-454">El tipo de memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="85ef8-454">The type of video memory.</span></span> <span data-ttu-id="85ef8-455">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85ef8-455">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="85ef8-456">**Videoprocesador**</span><span class="sxs-lookup"><span data-stu-id="85ef8-456">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85ef8-457">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="85ef8-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85ef8-458">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85ef8-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85ef8-459">Cadena que describe el procesador o controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="85ef8-459">A string that describes the video processor/controller.</span></span> <span data-ttu-id="85ef8-460">Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85ef8-460">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85ef8-461">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85ef8-461">Requirements</span></span>



| <span data-ttu-id="85ef8-462">Requisito</span><span class="sxs-lookup"><span data-stu-id="85ef8-462">Requirement</span></span> | <span data-ttu-id="85ef8-463">Value</span><span class="sxs-lookup"><span data-stu-id="85ef8-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85ef8-464">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85ef8-464">Minimum supported client</span></span><br/> | <span data-ttu-id="85ef8-465">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="85ef8-465">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="85ef8-466">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85ef8-466">Minimum supported server</span></span><br/> | <span data-ttu-id="85ef8-467">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="85ef8-467">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="85ef8-468">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="85ef8-468">Namespace</span></span><br/>                | <span data-ttu-id="85ef8-469">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="85ef8-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="85ef8-470">MOF</span><span class="sxs-lookup"><span data-stu-id="85ef8-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85ef8-471"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85ef8-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="85ef8-472">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85ef8-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85ef8-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="85ef8-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="85ef8-474">Vea también</span><span class="sxs-lookup"><span data-stu-id="85ef8-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ef8-475">**\_DISPLAYCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="85ef8-475">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> </dl>

 

