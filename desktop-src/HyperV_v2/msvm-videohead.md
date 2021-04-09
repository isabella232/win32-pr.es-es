---
description: Describe la superficie de dibujo principal en un controlador de pantalla.
ms.assetid: 280ABAD0-D91B-4683-9F12-32563D7FE6BF
title: Clase Msvm_VideoHead
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHead
- Msvm_VideoHead.SetPowerState
- Msvm_VideoHead.EnableDevice
- Msvm_VideoHead.OnlineDevice
- Msvm_VideoHead.QuiesceDevice
- Msvm_VideoHead.SaveProperties
- Msvm_VideoHead.RestoreProperties
- Msvm_VideoHead.InstanceID
- Msvm_VideoHead.Caption
- Msvm_VideoHead.Description
- Msvm_VideoHead.ElementName
- Msvm_VideoHead.InstallDate
- Msvm_VideoHead.Name
- Msvm_VideoHead.OperationalStatus
- Msvm_VideoHead.StatusDescriptions
- Msvm_VideoHead.Status
- Msvm_VideoHead.HealthState
- Msvm_VideoHead.CommunicationStatus
- Msvm_VideoHead.DetailedStatus
- Msvm_VideoHead.OperatingStatus
- Msvm_VideoHead.PrimaryStatus
- Msvm_VideoHead.EnabledState
- Msvm_VideoHead.OtherEnabledState
- Msvm_VideoHead.RequestedState
- Msvm_VideoHead.EnabledDefault
- Msvm_VideoHead.TimeOfLastStateChange
- Msvm_VideoHead.AvailableRequestedStates
- Msvm_VideoHead.TransitioningToState
- Msvm_VideoHead.SystemCreationClassName
- Msvm_VideoHead.SystemName
- Msvm_VideoHead.CreationClassName
- Msvm_VideoHead.DeviceID
- Msvm_VideoHead.PowerManagementSupported
- Msvm_VideoHead.PowerManagementCapabilities
- Msvm_VideoHead.Availability
- Msvm_VideoHead.StatusInfo
- Msvm_VideoHead.LastErrorCode
- Msvm_VideoHead.ErrorDescription
- Msvm_VideoHead.ErrorCleared
- Msvm_VideoHead.OtherIdentifyingInfo
- Msvm_VideoHead.PowerOnHours
- Msvm_VideoHead.TotalPowerOnHours
- Msvm_VideoHead.IdentifyingDescriptions
- Msvm_VideoHead.AdditionalAvailability
- Msvm_VideoHead.MaxQuiesceTime
- Msvm_VideoHead.CurrentBitsPerPixel
- Msvm_VideoHead.CurrentHorizontalResolution
- Msvm_VideoHead.CurrentVerticalResolution
- Msvm_VideoHead.MaxRefreshRate
- Msvm_VideoHead.MinRefreshRate
- Msvm_VideoHead.CurrentRefreshRate
- Msvm_VideoHead.CurrentScanMode
- Msvm_VideoHead.OtherCurrentScanMode
- Msvm_VideoHead.CurrentNumberOfRows
- Msvm_VideoHead.CurrentNumberOfColumns
- Msvm_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f40e0386fe42177484fc07296a2f4567f1ee47a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155165"
---
# <a name="msvm_videohead-class"></a><span data-ttu-id="e6cab-103">MSVM \_ Videohead (clase)</span><span class="sxs-lookup"><span data-stu-id="e6cab-103">Msvm\_VideoHead class</span></span>

<span data-ttu-id="e6cab-104">Describe la superficie de dibujo principal en un controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e6cab-104">Describes the primary drawing surface on a display controller.</span></span>

<span data-ttu-id="e6cab-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e6cab-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6cab-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6cab-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHead : CIM_VideoHead
{
  string   InstanceID;
  string   Caption = "Video Head";
  string   Description = "Microsoft Virtual Video Head";
  string   ElementName = "Video Head";
  datetime InstallDate;
  string   Name = "Video Head";
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_VideoHead";
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint32   CurrentVerticalResolution;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  string   OtherCurrentScanMode;
  uint32   CurrentNumberOfRows;
  uint32   CurrentNumberOfColumns;
  uint64   CurrentNumberOfColors;
};
```

## <a name="members"></a><span data-ttu-id="e6cab-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e6cab-107">Members</span></span>

<span data-ttu-id="e6cab-108">La **clase \_ videohead de MSVM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e6cab-108">The **Msvm\_VideoHead** class has these types of members:</span></span>

-   [<span data-ttu-id="e6cab-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6cab-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="e6cab-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e6cab-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e6cab-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6cab-111">Methods</span></span>

<span data-ttu-id="e6cab-112">La clase **MSVM \_ videohead** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e6cab-112">The **Msvm\_VideoHead** class has these methods.</span></span>



| <span data-ttu-id="e6cab-113">Método</span><span class="sxs-lookup"><span data-stu-id="e6cab-113">Method</span></span>                                                          | <span data-ttu-id="e6cab-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6cab-114">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="e6cab-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="e6cab-115">**EnableDevice**</span></span>                                                | <span data-ttu-id="e6cab-116">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e6cab-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e6cab-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="e6cab-117">**OnlineDevice**</span></span>                                                | <span data-ttu-id="e6cab-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e6cab-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e6cab-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="e6cab-119">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="e6cab-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e6cab-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="e6cab-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e6cab-121">**RequestStateChange**</span></span>](msvm-videohead-requeststatechange.md) | <span data-ttu-id="e6cab-122">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="e6cab-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="e6cab-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="e6cab-123">**Reset**</span></span>](msvm-videohead-reset.md)                           | <span data-ttu-id="e6cab-124">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="e6cab-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="e6cab-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="e6cab-125">**RestoreProperties**</span></span>                                           | <span data-ttu-id="e6cab-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e6cab-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e6cab-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="e6cab-127">**SaveProperties**</span></span>                                              | <span data-ttu-id="e6cab-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e6cab-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e6cab-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e6cab-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="e6cab-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="e6cab-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e6cab-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e6cab-131">Properties</span></span>

<span data-ttu-id="e6cab-132">La **clase \_ Videohead de MSVM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e6cab-132">The **Msvm\_VideoHead** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e6cab-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="e6cab-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-134">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-136">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6cab-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="e6cab-137">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en 6 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="e6cab-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-138">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="e6cab-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-141">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6cab-141">The primary availability and status of the device.</span></span> <span data-ttu-id="e6cab-142">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e6cab-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="e6cab-143">Value</span><span class="sxs-lookup"><span data-stu-id="e6cab-143">Value</span></span>                                                                        | <span data-ttu-id="e6cab-144">Significado</span><span class="sxs-lookup"><span data-stu-id="e6cab-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="e6cab-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e6cab-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="e6cab-146">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="e6cab-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e6cab-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="e6cab-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-148">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-150">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e6cab-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="e6cab-151">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="e6cab-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-152">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e6cab-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6cab-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-155">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e6cab-155">A short description of the object.</span></span> <span data-ttu-id="e6cab-156">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e6cab-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="e6cab-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-158">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-160">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="e6cab-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e6cab-161">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e6cab-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e6cab-162">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6cab-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e6cab-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e6cab-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="e6cab-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="e6cab-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="e6cab-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="e6cab-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e6cab-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="e6cab-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e6cab-170">)</span><span class="sxs-lookup"><span data-stu-id="e6cab-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6cab-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e6cab-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-172">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-174">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="e6cab-174">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e6cab-175">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e6cab-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-176">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="e6cab-176">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-177">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6cab-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-179">Calificadores: **unidades** ("bits")</span><span class="sxs-lookup"><span data-stu-id="e6cab-179">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-180">Número de bits usados para mostrar cada píxel.</span><span class="sxs-lookup"><span data-stu-id="e6cab-180">The number of bits used to display each pixel.</span></span> <span data-ttu-id="e6cab-181">Esta propiedad se hereda de [**la \_ videopartida CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6cab-181">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-182">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="e6cab-182">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-183">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6cab-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-185">Calificadores: **unidades** ("píxeles")</span><span class="sxs-lookup"><span data-stu-id="e6cab-185">Qualifiers: **Units** ("Pixels")</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-186">Número actual de píxeles horizontales.</span><span class="sxs-lookup"><span data-stu-id="e6cab-186">The current number of horizontal pixels.</span></span> <span data-ttu-id="e6cab-187">Esta propiedad se hereda de [**la \_ videopartida CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6cab-187">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-188">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="e6cab-188">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-189">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e6cab-189">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-191">El número de colores admitidos en las resoluciones actuales.</span><span class="sxs-lookup"><span data-stu-id="e6cab-191">The number of colors supported at the current resolutions.</span></span> <span data-ttu-id="e6cab-192">Esta propiedad se hereda de [**la \_ videopartida CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6cab-192">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-193">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="e6cab-193">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-194">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6cab-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-196">Si está en modo de carácter, el número de columnas de este controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e6cab-196">If in character mode, the number of columns for this display controller.</span></span> <span data-ttu-id="e6cab-197">De lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="e6cab-197">Otherwise, 0.</span></span> <span data-ttu-id="e6cab-198">Esta propiedad se hereda de [**la \_ videopartida CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6cab-198">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-199">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="e6cab-199">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-200">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6cab-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-202">Si está en modo de carácter, el número de filas de este controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e6cab-202">If in character mode, the number of rows for this video controller.</span></span> <span data-ttu-id="e6cab-203">De lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="e6cab-203">Otherwise, 0.</span></span> <span data-ttu-id="e6cab-204">Esta propiedad se hereda de [**la \_ videopartida CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6cab-204">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-205">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="e6cab-205">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-206">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6cab-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-208">Calificadores: **unidades** ("hercios")</span><span class="sxs-lookup"><span data-stu-id="e6cab-208">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-209">Frecuencia de actualización actual, en hercios.</span><span class="sxs-lookup"><span data-stu-id="e6cab-209">The current refresh rate, in hertz.</span></span> <span data-ttu-id="e6cab-210">Esta propiedad se hereda de [**la \_ videopartida CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6cab-210">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-211">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="e6cab-211">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-212">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-214">El modo de exploración actual.</span><span class="sxs-lookup"><span data-stu-id="e6cab-214">The current scan mode.</span></span> <span data-ttu-id="e6cab-215">Esta propiedad se hereda de [**la \_ videopartida CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6cab-215">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="e6cab-216"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e6cab-216"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-217"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="e6cab-217"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-218"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="e6cab-218"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-219"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Operación no entrelazada** (3)</span><span class="sxs-lookup"><span data-stu-id="e6cab-219"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Non-Interlaced Operation** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-220"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Operación entrelazada** (4)</span><span class="sxs-lookup"><span data-stu-id="e6cab-220"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Interlaced Operation** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6cab-221">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="e6cab-221">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-222">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6cab-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-224">Calificadores: **unidades** ("píxeles")</span><span class="sxs-lookup"><span data-stu-id="e6cab-224">Qualifiers: **Units** ("Pixels")</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-225">Número actual de píxeles verticales.</span><span class="sxs-lookup"><span data-stu-id="e6cab-225">The current number of vertical pixels.</span></span> <span data-ttu-id="e6cab-226">Esta propiedad se hereda de [**la \_ videopartida CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6cab-226">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-227">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e6cab-227">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-228">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6cab-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-230">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e6cab-230">A description of the object.</span></span> <span data-ttu-id="e6cab-231">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e6cab-231">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-232">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e6cab-232">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-233">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-235">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="e6cab-235">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e6cab-236">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e6cab-236">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e6cab-237">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6cab-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e6cab-238"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="e6cab-238"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-239"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="e6cab-239"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-240"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="e6cab-240"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-241"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="e6cab-241"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="e6cab-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-243"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="e6cab-243"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-244"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e6cab-244"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-245"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="e6cab-245"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e6cab-246">)</span><span class="sxs-lookup"><span data-stu-id="e6cab-246">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6cab-247">**ID**</span><span class="sxs-lookup"><span data-stu-id="e6cab-247">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-248">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6cab-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-250">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en "Microsoft:*GUID* \\ Head \\ *index*".</span><span class="sxs-lookup"><span data-stu-id="e6cab-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\Head\\*Index*".</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-251">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e6cab-251">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6cab-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-254">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="e6cab-254">A display name for the object.</span></span> <span data-ttu-id="e6cab-255">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e6cab-255">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-256">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="e6cab-256">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-257">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-259">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e6cab-259">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e6cab-260">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="e6cab-260">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="e6cab-261">Value</span><span class="sxs-lookup"><span data-stu-id="e6cab-261">Value</span></span>                                                                        | <span data-ttu-id="e6cab-262">Significado</span><span class="sxs-lookup"><span data-stu-id="e6cab-262">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="e6cab-263"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e6cab-263"><dt>2</dt></span></span> </dl> | <span data-ttu-id="e6cab-264">habilitado</span><span class="sxs-lookup"><span data-stu-id="e6cab-264">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="e6cab-265"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e6cab-265"><dt>3</dt></span></span> </dl> | <span data-ttu-id="e6cab-266">Disabled</span><span class="sxs-lookup"><span data-stu-id="e6cab-266">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e6cab-267">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e6cab-267">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-268">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6cab-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-270">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e6cab-270">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e6cab-271">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="e6cab-271">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="e6cab-272">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6cab-272">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="e6cab-273">Value</span><span class="sxs-lookup"><span data-stu-id="e6cab-273">Value</span></span>                                                                        | <span data-ttu-id="e6cab-274">Significado</span><span class="sxs-lookup"><span data-stu-id="e6cab-274">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="e6cab-275"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e6cab-275"><dt>2</dt></span></span> </dl> | <span data-ttu-id="e6cab-276">habilitado</span><span class="sxs-lookup"><span data-stu-id="e6cab-276">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="e6cab-277"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e6cab-277"><dt>3</dt></span></span> </dl> | <span data-ttu-id="e6cab-278">Disabled</span><span class="sxs-lookup"><span data-stu-id="e6cab-278">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e6cab-279">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e6cab-279">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-280">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e6cab-280">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-282">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="e6cab-282">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="e6cab-283">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e6cab-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-284">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e6cab-284">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-285">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6cab-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-287">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="e6cab-287">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="e6cab-288">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e6cab-288">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-289">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e6cab-289">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-290">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-292">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="e6cab-292">The current health of the element.</span></span> <span data-ttu-id="e6cab-293">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="e6cab-293">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="e6cab-294">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="e6cab-294">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="e6cab-295">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6cab-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="e6cab-296">Value</span><span class="sxs-lookup"><span data-stu-id="e6cab-296">Value</span></span>                                                                        | <span data-ttu-id="e6cab-297">Significado</span><span class="sxs-lookup"><span data-stu-id="e6cab-297">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="e6cab-298"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e6cab-298"><dt>5</dt></span></span> </dl> | <span data-ttu-id="e6cab-299">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e6cab-299">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e6cab-300">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e6cab-300">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-301">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e6cab-301">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-303">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="e6cab-303">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="e6cab-304">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="e6cab-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-305">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e6cab-305">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-306">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e6cab-306">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-308">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e6cab-308">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="e6cab-309">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6cab-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-310">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e6cab-310">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-311">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6cab-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-313">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="e6cab-313">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-314">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="e6cab-314">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e6cab-315">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e6cab-315">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-316">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e6cab-316">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-317">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6cab-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-319">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e6cab-319">The last error code reported by the logical device.</span></span> <span data-ttu-id="e6cab-320">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e6cab-320">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-321">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="e6cab-321">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-322">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e6cab-322">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-324">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="e6cab-324">This property has been deprecated.</span></span> <span data-ttu-id="e6cab-325">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e6cab-325">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-326">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="e6cab-326">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-327">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6cab-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-329">Calificadores: **unidades** ("hercios")</span><span class="sxs-lookup"><span data-stu-id="e6cab-329">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-330">La frecuencia máxima de actualización del controlador de pantalla, en hercios.</span><span class="sxs-lookup"><span data-stu-id="e6cab-330">The maximum refresh rate of the display controller, in hertz.</span></span> <span data-ttu-id="e6cab-331">Esta propiedad se hereda de [**la \_ videopartida CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6cab-331">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-332">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="e6cab-332">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-333">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e6cab-333">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-335">Calificadores: **unidades** ("hercios")</span><span class="sxs-lookup"><span data-stu-id="e6cab-335">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-336">La frecuencia de actualización mínima del controlador de vídeo, en hercios.</span><span class="sxs-lookup"><span data-stu-id="e6cab-336">The minimum refresh rate of the video controller, in hertz.</span></span> <span data-ttu-id="e6cab-337">Esta propiedad se hereda de [**la \_ videopartida CIM**](/previous-versions//cc136948(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6cab-337">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-338">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="e6cab-338">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-339">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6cab-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-341">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="e6cab-341">The label by which the object is known.</span></span> <span data-ttu-id="e6cab-342">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y es igual que la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="e6cab-342">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-343">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="e6cab-343">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-344">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-346">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="e6cab-346">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e6cab-347">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e6cab-347">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e6cab-348">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6cab-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e6cab-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e6cab-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-350"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="e6cab-350"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-351"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="e6cab-351"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-352"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="e6cab-352"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-353"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="e6cab-353"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-354"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="e6cab-354"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-355"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="e6cab-355"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-356"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="e6cab-356"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-357"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="e6cab-357"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-358"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="e6cab-358"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-359"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="e6cab-359"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-360"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="e6cab-360"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-361"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="e6cab-361"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-362"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="e6cab-362"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-363"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="e6cab-363"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-364"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="e6cab-364"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-365"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="e6cab-365"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e6cab-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="e6cab-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e6cab-368">)</span><span class="sxs-lookup"><span data-stu-id="e6cab-368">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6cab-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e6cab-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-370">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-372">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="e6cab-372">The current statuses of the object.</span></span> <span data-ttu-id="e6cab-373">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6cab-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-374">**OtherCurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="e6cab-374">**OtherCurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-375">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6cab-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-376">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-377">El modo de exploración actual cuando la propiedad **CurrentScanMode** de la instancia es 1 (otra).</span><span class="sxs-lookup"><span data-stu-id="e6cab-377">The current scan mode when the instance's **CurrentScanMode** property is 1 (Other).</span></span> <span data-ttu-id="e6cab-378">Esta propiedad se hereda de [**la \_ videopartida CIM**](/previous-versions//cc136948(v=vs.85)) y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="e6cab-378">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)) and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-379">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="e6cab-379">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-380">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6cab-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-382">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="e6cab-382">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="e6cab-383">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="e6cab-383">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="e6cab-384">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="e6cab-384">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-385">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e6cab-385">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-386">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e6cab-386">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-388">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e6cab-388">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="e6cab-389">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="e6cab-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-390">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e6cab-390">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-391">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-391">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-392">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-393">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6cab-393">The power management capabilities of the device.</span></span> <span data-ttu-id="e6cab-394">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e6cab-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-395">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e6cab-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-396">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e6cab-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-398">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="e6cab-398">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="e6cab-399">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e6cab-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-400">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e6cab-400">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-401">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e6cab-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-403">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="e6cab-403">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="e6cab-404">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e6cab-404">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-405">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="e6cab-405">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-406">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-406">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-407">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-408">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="e6cab-408">Provides high level status information.</span></span> <span data-ttu-id="e6cab-409">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="e6cab-409">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="e6cab-410">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="e6cab-410">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e6cab-411">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6cab-411">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e6cab-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e6cab-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-413"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="e6cab-413"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-414"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="e6cab-414"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-415"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="e6cab-415"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="e6cab-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="e6cab-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e6cab-418">)</span><span class="sxs-lookup"><span data-stu-id="e6cab-418">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e6cab-419">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e6cab-419">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-420">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-422">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="e6cab-422">The last requested or desired state for the element.</span></span> <span data-ttu-id="e6cab-423">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="e6cab-423">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="e6cab-424">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6cab-424">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="e6cab-425">Value</span><span class="sxs-lookup"><span data-stu-id="e6cab-425">Value</span></span>                                                                         | <span data-ttu-id="e6cab-426">Significado</span><span class="sxs-lookup"><span data-stu-id="e6cab-426">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="e6cab-427"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="e6cab-427"><dt>12</dt></span></span> </dl> | <span data-ttu-id="e6cab-428">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="e6cab-428">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e6cab-429">**Estado**</span><span class="sxs-lookup"><span data-stu-id="e6cab-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-430">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6cab-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-431">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-432">Cadena que especifica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="e6cab-432">A string that specifies the current status of the object.</span></span> <span data-ttu-id="e6cab-433">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e6cab-433">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-434">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e6cab-434">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-435">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e6cab-435">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-436">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-437">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e6cab-437">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e6cab-438">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e6cab-438">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-439">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e6cab-439">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-440">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-441">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-442">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e6cab-442">The current state of the logical device.</span></span> <span data-ttu-id="e6cab-443">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e6cab-443">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-444">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e6cab-444">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-445">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6cab-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-446">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-447">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e6cab-447">The scoping system's creation class name.</span></span> <span data-ttu-id="e6cab-448">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e6cab-448">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-449">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e6cab-449">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-450">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e6cab-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-451">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-452">Identificador único de la máquina virtual de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e6cab-452">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="e6cab-453">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="e6cab-453">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-454">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="e6cab-454">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-455">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e6cab-455">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-456">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-457">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="e6cab-457">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e6cab-458">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="e6cab-458">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-459">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e6cab-459">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-460">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e6cab-460">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-461">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-462">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6cab-462">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="e6cab-463">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="e6cab-463">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e6cab-464">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="e6cab-464">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6cab-465">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e6cab-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e6cab-466">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e6cab-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e6cab-467">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="e6cab-467">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e6cab-468">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e6cab-468">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="e6cab-469">Value</span><span class="sxs-lookup"><span data-stu-id="e6cab-469">Value</span></span>                                                                         | <span data-ttu-id="e6cab-470">Significado</span><span class="sxs-lookup"><span data-stu-id="e6cab-470">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="e6cab-471"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="e6cab-471"><dt>12</dt></span></span> </dl> | <span data-ttu-id="e6cab-472">No es aplicable</span><span class="sxs-lookup"><span data-stu-id="e6cab-472">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6cab-473">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6cab-473">Remarks</span></span>

<span data-ttu-id="e6cab-474">El acceso a la clase **\_ videohead de MSVM** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="e6cab-474">Access to the **Msvm\_VideoHead** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e6cab-475">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e6cab-475">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6cab-476">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6cab-476">Requirements</span></span>



| <span data-ttu-id="e6cab-477">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6cab-477">Requirement</span></span> | <span data-ttu-id="e6cab-478">Value</span><span class="sxs-lookup"><span data-stu-id="e6cab-478">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6cab-479">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6cab-479">Minimum supported client</span></span><br/> | <span data-ttu-id="e6cab-480">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e6cab-480">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e6cab-481">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6cab-481">Minimum supported server</span></span><br/> | <span data-ttu-id="e6cab-482">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e6cab-482">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6cab-483">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e6cab-483">Namespace</span></span><br/>                | <span data-ttu-id="e6cab-484">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e6cab-484">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e6cab-485">MOF</span><span class="sxs-lookup"><span data-stu-id="e6cab-485">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6cab-486"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6cab-486"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6cab-487">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e6cab-487">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6cab-488"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6cab-488"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e6cab-489">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6cab-489">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6cab-490">**Videopartida CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e6cab-490">**CIM\_VideoHead**</span></span>](cim-videohead.md)
</dt> <dt>

<span data-ttu-id="e6cab-491">[**Videopartida CIM \_**](/previous-versions//cc136948(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e6cab-491">[**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e6cab-492">Clases de vídeo</span><span class="sxs-lookup"><span data-stu-id="e6cab-492">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

