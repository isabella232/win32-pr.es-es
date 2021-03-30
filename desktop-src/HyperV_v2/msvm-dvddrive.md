---
description: Representa una unidad de DVD dentro de una máquina virtual.
ms.assetid: BA813950-436F-46F1-8C1F-79C5AB1A459B
title: Clase Msvm_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive
- Msvm_DVDDrive.SetPowerState
- Msvm_DVDDrive.EnableDevice
- Msvm_DVDDrive.OnlineDevice
- Msvm_DVDDrive.QuiesceDevice
- Msvm_DVDDrive.SaveProperties
- Msvm_DVDDrive.RestoreProperties
- Msvm_DVDDrive.InstanceID
- Msvm_DVDDrive.Caption
- Msvm_DVDDrive.Description
- Msvm_DVDDrive.ElementName
- Msvm_DVDDrive.InstallDate
- Msvm_DVDDrive.Name
- Msvm_DVDDrive.OperationalStatus
- Msvm_DVDDrive.StatusDescriptions
- Msvm_DVDDrive.Status
- Msvm_DVDDrive.HealthState
- Msvm_DVDDrive.CommunicationStatus
- Msvm_DVDDrive.DetailedStatus
- Msvm_DVDDrive.OperatingStatus
- Msvm_DVDDrive.PrimaryStatus
- Msvm_DVDDrive.EnabledState
- Msvm_DVDDrive.OtherEnabledState
- Msvm_DVDDrive.RequestedState
- Msvm_DVDDrive.EnabledDefault
- Msvm_DVDDrive.TimeOfLastStateChange
- Msvm_DVDDrive.AvailableRequestedStates
- Msvm_DVDDrive.TransitioningToState
- Msvm_DVDDrive.SystemCreationClassName
- Msvm_DVDDrive.SystemName
- Msvm_DVDDrive.CreationClassName
- Msvm_DVDDrive.DeviceID
- Msvm_DVDDrive.PowerManagementSupported
- Msvm_DVDDrive.PowerManagementCapabilities
- Msvm_DVDDrive.Availability
- Msvm_DVDDrive.StatusInfo
- Msvm_DVDDrive.LastErrorCode
- Msvm_DVDDrive.ErrorDescription
- Msvm_DVDDrive.ErrorCleared
- Msvm_DVDDrive.OtherIdentifyingInfo
- Msvm_DVDDrive.PowerOnHours
- Msvm_DVDDrive.TotalPowerOnHours
- Msvm_DVDDrive.IdentifyingDescriptions
- Msvm_DVDDrive.AdditionalAvailability
- Msvm_DVDDrive.MaxQuiesceTime
- Msvm_DVDDrive.Capabilities
- Msvm_DVDDrive.CapabilityDescriptions
- Msvm_DVDDrive.ErrorMethodology
- Msvm_DVDDrive.CompressionMethod
- Msvm_DVDDrive.NumberOfMediaSupported
- Msvm_DVDDrive.MaxMediaSize
- Msvm_DVDDrive.DefaultBlockSize
- Msvm_DVDDrive.MaxBlockSize
- Msvm_DVDDrive.MinBlockSize
- Msvm_DVDDrive.NeedsCleaning
- Msvm_DVDDrive.MediaIsLocked
- Msvm_DVDDrive.Security
- Msvm_DVDDrive.LastCleaned
- Msvm_DVDDrive.MaxAccessTime
- Msvm_DVDDrive.UncompressedDataRate
- Msvm_DVDDrive.LoadTime
- Msvm_DVDDrive.UnloadTime
- Msvm_DVDDrive.MountCount
- Msvm_DVDDrive.TimeOfLastMount
- Msvm_DVDDrive.TotalMountTime
- Msvm_DVDDrive.UnitsDescription
- Msvm_DVDDrive.MaxUnitsBeforeCleaning
- Msvm_DVDDrive.UnitsUsed
- Msvm_DVDDrive.FormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e4b3c9006babb2c7e18b6aed6e85cbee47299429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912573"
---
# <a name="msvm_dvddrive-class"></a><span data-ttu-id="6515f-103">MSVM \_ DVDDrive (clase)</span><span class="sxs-lookup"><span data-stu-id="6515f-103">Msvm\_DVDDrive class</span></span>

<span data-ttu-id="6515f-104">Representa una unidad de DVD dentro de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6515f-104">Represents a DVD drive inside of a virtual machine.</span></span> <span data-ttu-id="6515f-105">Esta unidad de DVD puede ser un dispositivo de paso a través (si se ha conectado un disco duro físico a la máquina virtual) o sintético y rellenado con medios de archivo ISO.</span><span class="sxs-lookup"><span data-stu-id="6515f-105">This DVD drive can either be a pass-through device (if a physical hard disk was attached to the virtual machine) or synthetic and populated with ISO file media.</span></span> <span data-ttu-id="6515f-106">Dado que las unidades de DVD virtuales y físicas se pueden agregar y quitar de la máquina virtual, hay dos grupos de recursos asociados a esta clase, uno para las unidades de DVD de paso a través y otro para las unidades de DVD virtuales.</span><span class="sxs-lookup"><span data-stu-id="6515f-106">Because virtual and physical DVD drives can be added and removed from the virtual machine, there are two resource pools associated with this class, one for pass-through DVD drives, and the other for virtual DVD drives.</span></span> <span data-ttu-id="6515f-107">Las unidades de DVD solo se pueden agregar o quitar si la máquina virtual está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="6515f-107">DVD drives can only be added or removed if the virtual machine is offline.</span></span>

<span data-ttu-id="6515f-108">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6515f-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6515f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6515f-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DVDDrive : CIM_DVDDrive
{
  string   InstanceID;
  string   Caption = "DVD Drive";
  string   Description = "Microsoft Virtual DVD Drive";
  string   ElementName = "DVD Drive";
  datetime InstallDate;
  string   Name = "DVD Drive";
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
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_DVDDrive";
  string   DeviceID = "Microsoft:GUID\device-specific-data";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint32   Capabilities[] = {3, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Removable Media"};
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 9400000;
  uint64   DefaultBlockSize = 2048;
  uint64   MaxBlockSize = 2048;
  uint64   MinBlockSize = 2048;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = False;
  uint16   Security = 3;
  datetime LastCleaned;
  uint64   MaxAccessTime = 0;
  uint32   UncompressedDataRate;
  uint64   LoadTime = 0;
  uint64   UnloadTime = 0;
  uint64   MountCount = 0;
  datetime TimeOfLastMount;
  uint64   TotalMountTime = 0;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint16   FormatsSupported[] = {16, 22};
};
```

## <a name="members"></a><span data-ttu-id="6515f-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="6515f-110">Members</span></span>

<span data-ttu-id="6515f-111">La clase **MSVM \_ DVDDrive** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6515f-111">The **Msvm\_DVDDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="6515f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="6515f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="6515f-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6515f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6515f-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="6515f-114">Methods</span></span>

<span data-ttu-id="6515f-115">La clase **MSVM \_ DVDDrive** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6515f-115">The **Msvm\_DVDDrive** class has these methods.</span></span>



| <span data-ttu-id="6515f-116">Método</span><span class="sxs-lookup"><span data-stu-id="6515f-116">Method</span></span>                                                         | <span data-ttu-id="6515f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6515f-117">Description</span></span>                              |
|:---------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="6515f-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="6515f-118">**EnableDevice**</span></span>                                               | <span data-ttu-id="6515f-119">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="6515f-119">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="6515f-120">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="6515f-120">**LockMedia**</span></span>](msvm-dvddrive-lockmedia.md)                   | <span data-ttu-id="6515f-121">Bloquea o libera los medios.</span><span class="sxs-lookup"><span data-stu-id="6515f-121">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="6515f-122">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="6515f-122">**OnlineDevice**</span></span>                                               | <span data-ttu-id="6515f-123">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="6515f-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="6515f-124">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="6515f-124">**QuiesceDevice**</span></span>                                              | <span data-ttu-id="6515f-125">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="6515f-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="6515f-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="6515f-126">**RequestStateChange**</span></span>](msvm-dvddrive-requeststatechange.md) | <span data-ttu-id="6515f-127">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="6515f-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="6515f-128">**Reset**</span><span class="sxs-lookup"><span data-stu-id="6515f-128">**Reset**</span></span>](msvm-dvddrive-reset.md)                           | <span data-ttu-id="6515f-129">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="6515f-129">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="6515f-130">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="6515f-130">**RestoreProperties**</span></span>                                          | <span data-ttu-id="6515f-131">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="6515f-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="6515f-132">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="6515f-132">**SaveProperties**</span></span>                                             | <span data-ttu-id="6515f-133">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="6515f-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="6515f-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6515f-134">**SetPowerState**</span></span>                                              | <span data-ttu-id="6515f-135">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="6515f-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6515f-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6515f-136">Properties</span></span>

<span data-ttu-id="6515f-137">La clase **MSVM \_ DVDDrive** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6515f-137">The **Msvm\_DVDDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6515f-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="6515f-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-139">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6515f-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-141">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="6515f-142">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en 6 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="6515f-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-143">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="6515f-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-144">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-146">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-146">The primary availability and status of the device.</span></span> <span data-ttu-id="6515f-147">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en 6 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="6515f-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-148">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="6515f-148">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-149">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-149">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6515f-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-151">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="6515f-151">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="6515f-152">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual del objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6515f-152">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="6515f-153">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="6515f-153">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="6515f-154">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="6515f-154">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="6515f-155">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6515f-155">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-156">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="6515f-156">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-157">Tipo de datos: **UInt32** array</span><span class="sxs-lookup"><span data-stu-id="6515f-157">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="6515f-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-159">Las capacidades del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="6515f-159">The capabilities of the media access device.</span></span> <span data-ttu-id="6515f-160">Esta propiedad se hereda de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y se establece en los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6515f-160">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="6515f-161">Value</span><span class="sxs-lookup"><span data-stu-id="6515f-161">Value</span></span>                                                                             | <span data-ttu-id="6515f-162">Significado</span><span class="sxs-lookup"><span data-stu-id="6515f-162">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6515f-163"><dt>{3, 7}</dt></span><span class="sxs-lookup"><span data-stu-id="6515f-163"><dt>{3, 7}</dt></span></span> </dl> |                                                                                                 |
| <dl> <span data-ttu-id="6515f-164"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6515f-164"><dt>3</dt></span></span> </dl>      | <span data-ttu-id="6515f-165">La entrada correspondiente en **CapabilityDescriptions** es "Random Access".</span><span class="sxs-lookup"><span data-stu-id="6515f-165">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>            |
| <dl> <span data-ttu-id="6515f-166"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="6515f-166"><dt>7</dt></span></span> </dl>      | <span data-ttu-id="6515f-167">La entrada correspondiente en **CapabilityDescriptions** es "Supported medios extraíbles".</span><span class="sxs-lookup"><span data-stu-id="6515f-167">The corresponding entry in **CapabilityDescriptions** is "Supports Removable Media".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6515f-168">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6515f-168">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-169">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="6515f-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6515f-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-171">Matriz de cadenas de formato libre que proporciona explicaciones detalladas para las características del dispositivo de acceso indicadas en la matriz de propiedades **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="6515f-171">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="6515f-172">Cada entrada de esta matriz está relacionada con la entrada de la matriz de propiedades **Capabilities** , que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="6515f-172">Each entry of this array is related to the entry in the **Capabilities** property array, located at the same index.</span></span> <span data-ttu-id="6515f-173">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-173">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-174">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6515f-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6515f-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-177">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="6515f-177">A short description of the object.</span></span> <span data-ttu-id="6515f-178">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6515f-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-179">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="6515f-179">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-180">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-182">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="6515f-182">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="6515f-183">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="6515f-183">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6515f-184">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6515f-184">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-185">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="6515f-185">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6515f-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-188">Cadena que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6515f-188">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="6515f-189">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="6515f-189">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="6515f-190">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="6515f-190">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="6515f-191">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="6515f-191">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="6515f-192">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-192">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

<span data-ttu-id="6515f-193">"No comprimido"</span><span class="sxs-lookup"><span data-stu-id="6515f-193">"Not Compressed"</span></span>

<span data-ttu-id="6515f-194">Unknown</span><span class="sxs-lookup"><span data-stu-id="6515f-194">"Unknown"</span></span>

<span data-ttu-id="6515f-195">Comprimido</span><span class="sxs-lookup"><span data-stu-id="6515f-195">"Compressed"</span></span>

<span data-ttu-id="6515f-196">"No comprimido"</span><span class="sxs-lookup"><span data-stu-id="6515f-196">"Not Compressed"</span></span>

</dd> <dt>

<span data-ttu-id="6515f-197">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6515f-197">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-198">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-200">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="6515f-200">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6515f-201">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-202">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="6515f-202">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-203">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6515f-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-205">Tamaño de bloque predeterminado, en bytes, para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-205">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="6515f-206">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-206">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-207">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6515f-207">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6515f-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-210">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="6515f-210">A description of the object.</span></span> <span data-ttu-id="6515f-211">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6515f-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-212">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="6515f-212">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-213">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-215">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="6515f-215">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="6515f-216">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="6515f-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6515f-217">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6515f-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-218">**ID**</span><span class="sxs-lookup"><span data-stu-id="6515f-218">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6515f-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-221">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en "Microsoft:*GUID* del \\ *dispositivo-datos específicos*".</span><span class="sxs-lookup"><span data-stu-id="6515f-221">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="6515f-222">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6515f-222">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6515f-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-225">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="6515f-225">A display name for the object.</span></span> <span data-ttu-id="6515f-226">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6515f-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-227">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="6515f-227">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-228">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-230">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="6515f-230">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="6515f-231">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6515f-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-232">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="6515f-232">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-233">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-235">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="6515f-235">The enabled and disabled states of an element.</span></span> <span data-ttu-id="6515f-236">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="6515f-236">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="6515f-237">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6515f-237">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-238">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="6515f-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-239">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6515f-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-241">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="6515f-241">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="6515f-242">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="6515f-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6515f-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-244">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6515f-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-246">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="6515f-246">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="6515f-247">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="6515f-247">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-248">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="6515f-248">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6515f-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-251">Cadena que describe los tipos de detección y corrección de errores admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-251">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="6515f-252">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-252">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-253">**FormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="6515f-253">**FormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-254">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-254">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6515f-255">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-256">Los formatos de CD y DVD que son compatibles con este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-256">The CD and DVD formats that are supported by this device.</span></span> <span data-ttu-id="6515f-257">Esta propiedad se hereda de [**\_ DVDDrive CIM**](/previous-versions//cc136812(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6515f-257">This property is inherited from [**CIM\_DVDDrive**](/previous-versions//cc136812(v=vs.85)).</span></span>

<span data-ttu-id="6515f-258">Esta matriz contiene los siguientes valores para ISO.</span><span class="sxs-lookup"><span data-stu-id="6515f-258">This array contains the following values for ISO.</span></span>

<dl> <dt>

<span data-ttu-id="6515f-259">{16, 22}</span><span class="sxs-lookup"><span data-stu-id="6515f-259">{16, 22}</span></span>
</dt> <dt>

<span data-ttu-id="6515f-260"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="6515f-260"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-261"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="6515f-261"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>
</dt> </dl>

<span data-ttu-id="6515f-262">Esta matriz contiene los siguientes valores para el paso físico.</span><span class="sxs-lookup"><span data-stu-id="6515f-262">This array contains the following values for physical pass-through.</span></span>

<dl> <dt>

<span data-ttu-id="6515f-263"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="6515f-263"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-264"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="6515f-264"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-265"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="6515f-265"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-266"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span><span class="sxs-lookup"><span data-stu-id="6515f-266"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-267"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span><span class="sxs-lookup"><span data-stu-id="6515f-267"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-268"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD grabable** (19)</span><span class="sxs-lookup"><span data-stu-id="6515f-268"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD Recordable** (19)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-269"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="6515f-269"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-270"><span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW +** (23)</span><span class="sxs-lookup"><span data-stu-id="6515f-270"><span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW+** (23)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-271"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span><span class="sxs-lookup"><span data-stu-id="6515f-271"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-272"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span><span class="sxs-lookup"><span data-stu-id="6515f-272"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-273"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-vídeo** (26)</span><span class="sxs-lookup"><span data-stu-id="6515f-273"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-274"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**DivX** (27)</span><span class="sxs-lookup"><span data-stu-id="6515f-274"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-275"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span><span class="sxs-lookup"><span data-stu-id="6515f-275"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-276"><span id="CD-DA"></span><span id="cd-da"></span>**CD-da** (34)</span><span class="sxs-lookup"><span data-stu-id="6515f-276"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-277"><span id="CD_"></span><span id="cd_"></span>**CD +** (35)</span><span class="sxs-lookup"><span data-stu-id="6515f-277"><span id="CD_"></span><span id="cd_"></span>**CD+** (35)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-278"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD grabable** (36)</span><span class="sxs-lookup"><span data-stu-id="6515f-278"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD Recordable** (36)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-279"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span><span class="sxs-lookup"><span data-stu-id="6515f-279"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-280"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-audio** (38)</span><span class="sxs-lookup"><span data-stu-id="6515f-280"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audio** (38)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-281"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span><span class="sxs-lookup"><span data-stu-id="6515f-281"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-282"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span><span class="sxs-lookup"><span data-stu-id="6515f-282"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-283"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span><span class="sxs-lookup"><span data-stu-id="6515f-283"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span></span>
</dt> <dt>

<span data-ttu-id="6515f-284"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span><span class="sxs-lookup"><span data-stu-id="6515f-284"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6515f-285">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="6515f-285">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-286">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-288">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="6515f-288">The current health of the element.</span></span> <span data-ttu-id="6515f-289">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="6515f-289">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="6515f-290">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="6515f-290">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="6515f-291">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6515f-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-292">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6515f-292">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-293">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="6515f-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6515f-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-295">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="6515f-295">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="6515f-296">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="6515f-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-297">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6515f-297">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-298">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6515f-298">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-300">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6515f-300">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="6515f-301">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6515f-301">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-302">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6515f-302">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6515f-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6515f-305">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="6515f-305">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6515f-306">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="6515f-306">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6515f-307">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6515f-307">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-308">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="6515f-308">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-309">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6515f-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-311">Fecha y hora en que se limpió por última vez el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-311">The date and time on which the device was last cleaned.</span></span> <span data-ttu-id="6515f-312">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-312">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-313">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6515f-313">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-314">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6515f-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-316">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6515f-316">The last error code reported by the logical device.</span></span> <span data-ttu-id="6515f-317">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="6515f-317">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-318">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="6515f-318">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-319">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6515f-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-321">Tiempo, en milisegundos, desde ' Load ' hasta la capacidad de leer o escribir un medio.</span><span class="sxs-lookup"><span data-stu-id="6515f-321">The time, in milliseconds, from 'load' to being able to read or write a media.</span></span> <span data-ttu-id="6515f-322">Por ejemplo, en el caso de las unidades de disco, es el intervalo entre un disco que no gira hasta el disco que informa de que está listo para lectura y escritura (es decir, el disco gira a velocidades nominales).</span><span class="sxs-lookup"><span data-stu-id="6515f-322">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="6515f-323">En el caso de las unidades de cinta, es el momento desde que se inserta un medio para informar de que está listo para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="6515f-323">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="6515f-324">Normalmente, se encuentra en el área de BOT de la cinta.</span><span class="sxs-lookup"><span data-stu-id="6515f-324">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="6515f-325">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-325">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-326">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="6515f-326">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-327">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6515f-327">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-329">Tiempo, en milisegundos, que se va a pasar de la primera ubicación del medio a la ubicación más lejana con respecto a la hora.</span><span class="sxs-lookup"><span data-stu-id="6515f-329">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="6515f-330">En el caso de una unidad de disco, representa una búsqueda completa + un retraso de rotación completo.</span><span class="sxs-lookup"><span data-stu-id="6515f-330">For a disk drive, this represents full seek + full rotational delay.</span></span> <span data-ttu-id="6515f-331">En el caso de las unidades de cinta, representa una búsqueda desde el principio de la cinta hasta el punto más alejado físicamente.</span><span class="sxs-lookup"><span data-stu-id="6515f-331">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="6515f-332">(El final de una cinta puede estar en su punto más lejano físicamente, pero esto no es necesariamente cierto). Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-332">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-333">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="6515f-333">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-334">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6515f-334">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-336">Tamaño máximo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-336">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="6515f-337">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-337">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-338">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="6515f-338">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-339">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6515f-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-341">Tamaño máximo, en kilobytes, de los medios admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-341">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="6515f-342">Los kilobytes se interpretan como el número de bytes multiplicado por 1000 (no por el número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="6515f-342">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="6515f-343">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-343">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-344">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="6515f-344">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-345">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6515f-345">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-347">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="6515f-347">This property has been deprecated.</span></span> <span data-ttu-id="6515f-348">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="6515f-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-349">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="6515f-349">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-350">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6515f-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-352">Las unidades máximas que se pueden usar antes de que se limpie el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-352">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="6515f-353">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-353">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-354">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="6515f-354">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-355">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6515f-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-357">**True** si el medio está bloqueado en el dispositivo y no se puede expulsar; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6515f-357">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="6515f-358">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-358">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-359">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="6515f-359">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-360">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6515f-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-362">Tamaño mínimo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-362">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="6515f-363">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-363">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-364">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="6515f-364">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-365">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6515f-365">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-367">En el caso de un dispositivo que admita medios extraíbles, el número de veces que los medios se han montado para la transferencia de datos o para limpiar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-367">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="6515f-368">En el caso de los dispositivos que tienen acceso a medios no extraíbles, como discos duros, esta propiedad no es aplicable y debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="6515f-368">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="6515f-369">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-369">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-370">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="6515f-370">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-371">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6515f-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-373">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="6515f-373">The label by which the object is known.</span></span> <span data-ttu-id="6515f-374">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y es igual que la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="6515f-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-375">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="6515f-375">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-376">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6515f-376">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-378">**True** si el dispositivo de acceso a medios necesita limpieza; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6515f-378">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="6515f-379">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-379">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-380">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="6515f-380">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-381">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6515f-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-383">Número máximo de medios individuales que se pueden admitir o insertar.</span><span class="sxs-lookup"><span data-stu-id="6515f-383">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="6515f-384">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-384">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-385">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="6515f-385">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-386">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-388">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="6515f-388">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="6515f-389">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="6515f-389">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6515f-390">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6515f-390">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-391">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="6515f-391">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-392">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-392">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6515f-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-394">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="6515f-394">The current statuses of the object.</span></span> <span data-ttu-id="6515f-395">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6515f-395">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-396">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="6515f-396">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-397">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6515f-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-398">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-399">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="6515f-399">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="6515f-400">Esta propiedad debe establecerse en **null** cuando la propiedad **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="6515f-400">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="6515f-401">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6515f-401">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-402">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="6515f-402">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-403">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="6515f-403">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6515f-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-405">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6515f-405">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="6515f-406">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="6515f-406">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-407">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6515f-407">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-408">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-408">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6515f-409">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-410">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-410">The power management capabilities of the device.</span></span> <span data-ttu-id="6515f-411">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="6515f-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-412">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="6515f-412">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-413">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6515f-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-414">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-415">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="6515f-415">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="6515f-416">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="6515f-416">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-417">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="6515f-417">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-418">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6515f-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-419">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-420">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="6515f-420">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="6515f-421">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="6515f-421">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-422">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="6515f-422">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-423">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-423">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-424">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-425">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="6515f-425">Provides high level status information.</span></span> <span data-ttu-id="6515f-426">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="6515f-426">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="6515f-427">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="6515f-427">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6515f-428">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6515f-428">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-429">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="6515f-429">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-430">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-430">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-431">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-432">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="6515f-432">The last requested or desired state for the element.</span></span> <span data-ttu-id="6515f-433">La propiedad **EnabledState** representa el estado real del elemento.</span><span class="sxs-lookup"><span data-stu-id="6515f-433">The actual state of the element is represented by the **EnabledState** property.</span></span> <span data-ttu-id="6515f-434">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="6515f-434">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="6515f-435">Una instancia concreta de [**\_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir el método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="6515f-435">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="6515f-436">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="6515f-436">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="6515f-437">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="6515f-437">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-438">**Seguridad**</span><span class="sxs-lookup"><span data-stu-id="6515f-438">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-439">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-441">La seguridad operativa definida para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-441">The operational security defined for the device.</span></span> <span data-ttu-id="6515f-442">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-442">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-443">**Estado**</span><span class="sxs-lookup"><span data-stu-id="6515f-443">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-444">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6515f-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-445">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-446">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="6515f-446">The current status of the object.</span></span> <span data-ttu-id="6515f-447">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="6515f-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-448">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6515f-448">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-449">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="6515f-449">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6515f-450">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-451">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="6515f-451">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="6515f-452">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6515f-452">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6515f-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-454">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-455">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-456">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6515f-456">The current state of the logical device.</span></span> <span data-ttu-id="6515f-457">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="6515f-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-458">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6515f-458">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-459">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6515f-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-460">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-461">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="6515f-461">The scoping system's creation class name.</span></span> <span data-ttu-id="6515f-462">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-463">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6515f-463">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-464">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6515f-464">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-465">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-466">Identificador único de la máquina virtual de ámbito.</span><span class="sxs-lookup"><span data-stu-id="6515f-466">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="6515f-467">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-467">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-468">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="6515f-468">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-469">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6515f-469">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-470">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-471">Para un dispositivo que admita medios extraíbles, la fecha y la hora más recientes en que se montó el medio en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-471">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="6515f-472">En el caso de los dispositivos que tienen acceso a medios no extraíbles, como discos duros, esta propiedad no tiene ningún significado y no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="6515f-472">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="6515f-473">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-473">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-474">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="6515f-474">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-475">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6515f-475">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-476">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-477">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="6515f-477">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="6515f-478">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="6515f-478">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-479">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="6515f-479">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-480">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6515f-480">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-481">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-482">En el caso de un dispositivo que admita medios extraíbles, el tiempo total (en segundos) que los medios se han montado para la transferencia de datos o para limpiar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-482">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="6515f-483">En el caso de los dispositivos que tienen acceso a medios no extraíbles, como discos duros, esta propiedad no es aplicable y debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="6515f-483">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="6515f-484">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-484">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-485">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="6515f-485">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-486">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6515f-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-487">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-488">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6515f-488">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="6515f-489">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="6515f-489">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-490">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="6515f-490">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-491">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6515f-491">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-492">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-493">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="6515f-493">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="6515f-494">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="6515f-494">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6515f-495">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="6515f-495">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-496">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6515f-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-497">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-498">La velocidad de transferencia de datos sostenida, en KB/s, que el dispositivo puede leer y escribir en un medio.</span><span class="sxs-lookup"><span data-stu-id="6515f-498">The sustained data transfer rate, in KB/sec, that the device can read from and write to a media.</span></span> <span data-ttu-id="6515f-499">Se trata de una velocidad de datos sin procesar y sostenida.</span><span class="sxs-lookup"><span data-stu-id="6515f-499">This is a sustained, raw data rate.</span></span> <span data-ttu-id="6515f-500">Las tarifas máximas o tarifas suponiendo que no se debería informar de la compresión en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="6515f-500">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="6515f-501">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-501">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-502">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="6515f-502">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-503">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6515f-503">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-504">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-505">Unidades relativas a su uso en **MaxUnitsBeforeCleaning**.</span><span class="sxs-lookup"><span data-stu-id="6515f-505">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="6515f-506">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-506">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-507">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="6515f-507">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-508">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6515f-508">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-509">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-510">Número actual de unidades utilizadas.</span><span class="sxs-lookup"><span data-stu-id="6515f-510">The current number of units used.</span></span> <span data-ttu-id="6515f-511">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-511">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="6515f-512">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="6515f-512">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6515f-513">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6515f-513">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6515f-514">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6515f-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6515f-515">Tiempo, en milisegundos, desde que se puede leer o escribir un elemento multimedia en su ' Unload '.</span><span class="sxs-lookup"><span data-stu-id="6515f-515">The time, in milliseconds, from being able to read or write a media to its 'unload'.</span></span> <span data-ttu-id="6515f-516">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="6515f-516">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6515f-517">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6515f-517">Remarks</span></span>

<span data-ttu-id="6515f-518">El acceso a la clase **MSVM \_ DVDDrive** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="6515f-518">Access to the **Msvm\_DVDDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6515f-519">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6515f-519">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6515f-520">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6515f-520">Requirements</span></span>



| <span data-ttu-id="6515f-521">Requisito</span><span class="sxs-lookup"><span data-stu-id="6515f-521">Requirement</span></span> | <span data-ttu-id="6515f-522">Value</span><span class="sxs-lookup"><span data-stu-id="6515f-522">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6515f-523">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6515f-523">Minimum supported client</span></span><br/> | <span data-ttu-id="6515f-524">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="6515f-524">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6515f-525">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6515f-525">Minimum supported server</span></span><br/> | <span data-ttu-id="6515f-526">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="6515f-526">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6515f-527">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6515f-527">Namespace</span></span><br/>                | <span data-ttu-id="6515f-528">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="6515f-528">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6515f-529">MOF</span><span class="sxs-lookup"><span data-stu-id="6515f-529">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6515f-530"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6515f-530"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6515f-531">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6515f-531">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6515f-532"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6515f-532"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6515f-533">Vea también</span><span class="sxs-lookup"><span data-stu-id="6515f-533">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6515f-534">**\_DVDDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="6515f-534">**CIM\_DVDDrive**</span></span>](cim-dvddrive.md)
</dt> <dt>

<span data-ttu-id="6515f-535">[**\_DVDDRIVE CIM**](/previous-versions//cc136812(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6515f-535">[**CIM\_DVDDrive**](/previous-versions//cc136812(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6515f-536">Clases de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="6515f-536">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

