---
description: Representa un dispositivo de teclado.
ms.assetid: 2a59fe90-12e2-471c-b49e-dfb4f4a31e0c
title: Msvm_Keyboard (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard
- Msvm_Keyboard.SetPowerState
- Msvm_Keyboard.EnableDevice
- Msvm_Keyboard.OnlineDevice
- Msvm_Keyboard.QuiesceDevice
- Msvm_Keyboard.SaveProperties
- Msvm_Keyboard.RestoreProperties
- Msvm_Keyboard.InstanceID
- Msvm_Keyboard.Caption
- Msvm_Keyboard.Description
- Msvm_Keyboard.ElementName
- Msvm_Keyboard.InstallDate
- Msvm_Keyboard.Name
- Msvm_Keyboard.OperationalStatus
- Msvm_Keyboard.StatusDescriptions
- Msvm_Keyboard.Status
- Msvm_Keyboard.HealthState
- Msvm_Keyboard.CommunicationStatus
- Msvm_Keyboard.DetailedStatus
- Msvm_Keyboard.OperatingStatus
- Msvm_Keyboard.PrimaryStatus
- Msvm_Keyboard.EnabledState
- Msvm_Keyboard.OtherEnabledState
- Msvm_Keyboard.RequestedState
- Msvm_Keyboard.EnabledDefault
- Msvm_Keyboard.TimeOfLastStateChange
- Msvm_Keyboard.AvailableRequestedStates
- Msvm_Keyboard.TransitioningToState
- Msvm_Keyboard.SystemCreationClassName
- Msvm_Keyboard.SystemName
- Msvm_Keyboard.CreationClassName
- Msvm_Keyboard.DeviceID
- Msvm_Keyboard.PowerManagementSupported
- Msvm_Keyboard.PowerManagementCapabilities
- Msvm_Keyboard.Availability
- Msvm_Keyboard.StatusInfo
- Msvm_Keyboard.LastErrorCode
- Msvm_Keyboard.ErrorDescription
- Msvm_Keyboard.ErrorCleared
- Msvm_Keyboard.OtherIdentifyingInfo
- Msvm_Keyboard.PowerOnHours
- Msvm_Keyboard.TotalPowerOnHours
- Msvm_Keyboard.IdentifyingDescriptions
- Msvm_Keyboard.AdditionalAvailability
- Msvm_Keyboard.MaxQuiesceTime
- Msvm_Keyboard.IsLocked
- Msvm_Keyboard.Layout
- Msvm_Keyboard.NumberOfFunctionKeys
- Msvm_Keyboard.Password
- Msvm_Keyboard.UnicodeSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37c4faceb9072c1851868eb23c031e715cb6e1c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082630"
---
# <a name="msvm_keyboard-class"></a><span data-ttu-id="425f6-103">\_Clase de teclado MSVM</span><span class="sxs-lookup"><span data-stu-id="425f6-103">Msvm\_Keyboard class</span></span>

<span data-ttu-id="425f6-104">Representa un dispositivo de teclado.</span><span class="sxs-lookup"><span data-stu-id="425f6-104">Represents a keyboard device.</span></span> <span data-ttu-id="425f6-105">Los teclados son dispositivos lógicos que siempre están presentes en una máquina virtual y, por tanto, no se asignan a través de un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="425f6-105">Keyboards are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="425f6-106">Siempre hay una instancia en un sistema de equipo virtual.</span><span class="sxs-lookup"><span data-stu-id="425f6-106">One instance is always present in a virtual computer system.</span></span>

<span data-ttu-id="425f6-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="425f6-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="425f6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="425f6-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Keyboard : CIM_UserDevice
{
  string   InstanceID;
  string   Caption = "Keyboard";
  string   Description = "Microsoft Virtual Keyboard";
  string   ElementName = "Keyboard";
  datetime InstallDate;
  string   Name = "Keyboard";
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
  string   CreationClassName = "Msvm_Keyboard";
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
  boolean  IsLocked = False;
  string   Layout = "00000409";
  uint16   NumberOfFunctionKeys = 12;
  uint16   Password = 5;
  boolean  UnicodeSupported;
};
```

## <a name="members"></a><span data-ttu-id="425f6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="425f6-109">Members</span></span>

<span data-ttu-id="425f6-110">La clase de **\_ teclado MSVM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="425f6-110">The **Msvm\_Keyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="425f6-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="425f6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="425f6-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="425f6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="425f6-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="425f6-113">Methods</span></span>

<span data-ttu-id="425f6-114">La clase de **\_ teclado MSVM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="425f6-114">The **Msvm\_Keyboard** class has these methods.</span></span>



| <span data-ttu-id="425f6-115">Método</span><span class="sxs-lookup"><span data-stu-id="425f6-115">Method</span></span>                                                         | <span data-ttu-id="425f6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="425f6-116">Description</span></span>                                                   |
|:---------------------------------------------------------------|:--------------------------------------------------------------|
| <span data-ttu-id="425f6-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="425f6-117">**EnableDevice**</span></span>                                               | <span data-ttu-id="425f6-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="425f6-118">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="425f6-119">**IsKeyPressed**</span><span class="sxs-lookup"><span data-stu-id="425f6-119">**IsKeyPressed**</span></span>](iskeypressed-msvm-keyboard.md)             | <span data-ttu-id="425f6-120">Recupera el estado de clave de una clave.</span><span class="sxs-lookup"><span data-stu-id="425f6-120">Retrieves the key state of a key.</span></span><br/>                  |
| <span data-ttu-id="425f6-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="425f6-121">**OnlineDevice**</span></span>                                               | <span data-ttu-id="425f6-122">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="425f6-122">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="425f6-123">**PressKey**</span><span class="sxs-lookup"><span data-stu-id="425f6-123">**PressKey**</span></span>](presskey-msvm-keyboard.md)                     | <span data-ttu-id="425f6-124">Simula una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="425f6-124">Simulates a key press.</span></span><br/>                             |
| <span data-ttu-id="425f6-125">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="425f6-125">**QuiesceDevice**</span></span>                                              | <span data-ttu-id="425f6-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="425f6-126">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="425f6-127">**ReleaseKey**</span><span class="sxs-lookup"><span data-stu-id="425f6-127">**ReleaseKey**</span></span>](releasekey-msvm-keyboard.md)                 | <span data-ttu-id="425f6-128">Simula una versión de clave.</span><span class="sxs-lookup"><span data-stu-id="425f6-128">Simulates a key release.</span></span><br/>                           |
| [<span data-ttu-id="425f6-129">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="425f6-129">**RequestStateChange**</span></span>](msvm-keyboard-requeststatechange.md) | <span data-ttu-id="425f6-130">Solicita que se cambie el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="425f6-130">Requests that the state of the element be changed.</span></span><br/> |
| [<span data-ttu-id="425f6-131">**Reset**</span><span class="sxs-lookup"><span data-stu-id="425f6-131">**Reset**</span></span>](msvm-keyboard-reset.md)                           | <span data-ttu-id="425f6-132">Restablece el teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="425f6-132">Resets the virtual keyboard.</span></span><br/>                       |
| <span data-ttu-id="425f6-133">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="425f6-133">**RestoreProperties**</span></span>                                          | <span data-ttu-id="425f6-134">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="425f6-134">This method is not supported.</span></span><br/>                      |
| <span data-ttu-id="425f6-135">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="425f6-135">**SaveProperties**</span></span>                                             | <span data-ttu-id="425f6-136">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="425f6-136">This method is not supported.</span></span><br/>                      |
| <span data-ttu-id="425f6-137">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="425f6-137">**SetPowerState**</span></span>                                              | <span data-ttu-id="425f6-138">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="425f6-138">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="425f6-139">**TypeCtrlAltDel**</span><span class="sxs-lookup"><span data-stu-id="425f6-139">**TypeCtrlAltDel**</span></span>](typectrlaltdel-msvm-keyboard.md)         | <span data-ttu-id="425f6-140">Simula una secuencia de teclas Ctrl + Alt + Supr.</span><span class="sxs-lookup"><span data-stu-id="425f6-140">Simulates a Ctrl+Alt+Del key sequence.</span></span><br/>             |
| [<span data-ttu-id="425f6-141">**TypeKey**</span><span class="sxs-lookup"><span data-stu-id="425f6-141">**TypeKey**</span></span>](typekey-msvm-keyboard.md)                       | <span data-ttu-id="425f6-142">Simula una secuencia de teclas de la versión de lanzamiento.</span><span class="sxs-lookup"><span data-stu-id="425f6-142">Simulates a press-release key sequence.</span></span><br/>            |
| [<span data-ttu-id="425f6-143">**TypeScancodes**</span><span class="sxs-lookup"><span data-stu-id="425f6-143">**TypeScancodes**</span></span>](msvm-keyboard-typescancodes.md)           | <span data-ttu-id="425f6-144">Simula una secuencia de teclas mediante códigos de recorrido.</span><span class="sxs-lookup"><span data-stu-id="425f6-144">Simulates a key sequence using scan codes.</span></span><br/>         |
| [<span data-ttu-id="425f6-145">**TypeText**</span><span class="sxs-lookup"><span data-stu-id="425f6-145">**TypeText**</span></span>](typetext-msvm-keyboard.md)                     | <span data-ttu-id="425f6-146">Simula una serie de caracteres con tipo.</span><span class="sxs-lookup"><span data-stu-id="425f6-146">Simulates a series of typed characters.</span></span><br/>            |



 

### <a name="properties"></a><span data-ttu-id="425f6-147">Propiedades</span><span class="sxs-lookup"><span data-stu-id="425f6-147">Properties</span></span>

<span data-ttu-id="425f6-148">La clase de **\_ teclado MSVM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="425f6-148">The **Msvm\_Keyboard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="425f6-149">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="425f6-149">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-150">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="425f6-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-152">Cualquier disponibilidad adicional y estado del dispositivo, más allá de lo especificado en la propiedad **Availability** .</span><span class="sxs-lookup"><span data-stu-id="425f6-152">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="425f6-153">La propiedad **Availability** denota el estado principal y la disponibilidad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="425f6-153">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="425f6-154">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="425f6-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="425f6-155">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="425f6-155">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-156">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-158">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="425f6-158">The primary availability and status of the device.</span></span> <span data-ttu-id="425f6-159">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="425f6-159">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="425f6-160">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="425f6-160">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-161">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-161">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="425f6-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-163">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="425f6-163">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="425f6-164">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="425f6-164">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="425f6-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="425f6-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="425f6-168">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="425f6-168">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="425f6-169">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="425f6-169">A short description of the object.</span></span> <span data-ttu-id="425f6-170">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="425f6-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="425f6-171">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="425f6-171">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-172">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-174">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="425f6-174">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="425f6-175">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="425f6-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="425f6-176">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="425f6-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="425f6-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="425f6-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-178"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="425f6-178"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-179"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="425f6-179"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="425f6-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-181"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="425f6-181"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="425f6-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-183"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="425f6-183"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="425f6-184">)</span><span class="sxs-lookup"><span data-stu-id="425f6-184">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="425f6-185">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="425f6-185">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="425f6-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="425f6-188">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="425f6-188">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="425f6-189">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="425f6-189">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="425f6-190">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="425f6-190">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="425f6-191">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="425f6-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="425f6-192">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="425f6-192">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-193">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="425f6-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-195">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="425f6-195">A description of the object.</span></span> <span data-ttu-id="425f6-196">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="425f6-196">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="425f6-197">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="425f6-197">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-198">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-200">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="425f6-200">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="425f6-201">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="425f6-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="425f6-202">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="425f6-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="425f6-203"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="425f6-203"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-204"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="425f6-204"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-205"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="425f6-205"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-206"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="425f6-206"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-207"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="425f6-207"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-208"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="425f6-208"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-209"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="425f6-209"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-210"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="425f6-210"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="425f6-211">)</span><span class="sxs-lookup"><span data-stu-id="425f6-211">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="425f6-212">**ID**</span><span class="sxs-lookup"><span data-stu-id="425f6-212">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="425f6-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-215">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="425f6-215">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="425f6-216">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "Microsoft:*GUID*".</span><span class="sxs-lookup"><span data-stu-id="425f6-216">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="425f6-217">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="425f6-217">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-218">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="425f6-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-220">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="425f6-220">A display name for the object.</span></span> <span data-ttu-id="425f6-221">Esta propiedad permite a cada instancia definir un nombre para mostrar además de las propiedades de clave, los datos de identidad y la información de descripción.</span><span class="sxs-lookup"><span data-stu-id="425f6-221">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="425f6-222">La propiedad [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) de la clase del **\_ ManagedSystemElement de CIM** también se define como un nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="425f6-222">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="425f6-223">Sin embargo, a menudo se considera una clave.</span><span class="sxs-lookup"><span data-stu-id="425f6-223">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="425f6-224">No es razonable que la misma propiedad pueda transmitir tanto la identidad como un nombre para mostrar, sin incoherencias.</span><span class="sxs-lookup"><span data-stu-id="425f6-224">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="425f6-225">Donde el **nombre** existe y no es una clave (por ejemplo, para las instancias del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), la misma información puede estar presente en las propiedades **nombre** y **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="425f6-225">Where **Name** exists and is not a Key (such as for instances of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="425f6-226">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="425f6-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="425f6-227">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="425f6-227">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-228">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-230">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="425f6-230">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="425f6-231">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="425f6-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="425f6-232">Value</span><span class="sxs-lookup"><span data-stu-id="425f6-232">Value</span></span>                                                                        | <span data-ttu-id="425f6-233">Significado</span><span class="sxs-lookup"><span data-stu-id="425f6-233">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="425f6-234"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-234"><dt>2</dt></span></span> </dl> | <span data-ttu-id="425f6-235">habilitado</span><span class="sxs-lookup"><span data-stu-id="425f6-235">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="425f6-236">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="425f6-236">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-237">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-239">Indica los Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="425f6-239">Indicates the enabled and disabled states of an element.</span></span> <span data-ttu-id="425f6-240">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="425f6-240">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="425f6-241">Por ejemplo, el apagado (valor = 4) e inicio (valor = 10) son Estados transitorios entre habilitado y deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="425f6-241">For example, shutting down (value=4) and starting (value=10) are transient states between enabled and disabled.</span></span>



| <span data-ttu-id="425f6-242">Value</span><span class="sxs-lookup"><span data-stu-id="425f6-242">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="425f6-243">Significado</span><span class="sxs-lookup"><span data-stu-id="425f6-243">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="425f6-244"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-244"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="425f6-245">Unknown</span><span class="sxs-lookup"><span data-stu-id="425f6-245">Unknown</span></span><br/>                                                                                                                                                                                              |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="425f6-246"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-246"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         | <span data-ttu-id="425f6-247">Otros</span><span class="sxs-lookup"><span data-stu-id="425f6-247">Other</span></span><br/>                                                                                                                                                                                                |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="425f6-248"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-248"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="425f6-249">El elemento es o puede ejecutar comandos, procesará cualquier comando en cola y pondrá en cola nuevas solicitudes.</span><span class="sxs-lookup"><span data-stu-id="425f6-249">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                            |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="425f6-250"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-250"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="425f6-251">El elemento no ejecutará comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="425f6-251">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="425f6-252"><dt>**Cerrando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-252"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="425f6-253">El elemento está en el proceso de pasar a un Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="425f6-253">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="425f6-254"><dt>**No aplicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-254"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="425f6-255">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="425f6-255">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="425f6-256"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-256"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="425f6-257">Es posible que el elemento esté completando comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="425f6-257">The element might be completing commands and will drop any new requests.</span></span><br/>                                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="425f6-258"><dt>**En la prueba**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-258"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="425f6-259">El elemento está en un estado de prueba.</span><span class="sxs-lookup"><span data-stu-id="425f6-259">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="425f6-260"><dt>**Aplazado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-260"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="425f6-261">Es posible que el elemento esté completando los comandos, pero pondrá en cola todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="425f6-261">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="425f6-262">Modo <dt>**inactivo**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-262"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="425f6-263">El elemento está habilitado pero en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="425f6-263">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="425f6-264">El comportamiento del elemento es similar al estado habilitado (2), pero solo procesa un conjunto restringido de comandos.</span><span class="sxs-lookup"><span data-stu-id="425f6-264">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="425f6-265">Todas las demás solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="425f6-265">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="425f6-266"><dt>**Inicio**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-266"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="425f6-267">El elemento está en proceso de pasar a un estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="425f6-267">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="425f6-268">Las nuevas solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="425f6-268">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="425f6-269"><dt>**DMTF reservado**</dt> <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-269"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="425f6-270">Este valor está reservado.</span><span class="sxs-lookup"><span data-stu-id="425f6-270">This value is reserved.</span></span><br/>                                                                                                                                                                              |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="425f6-271"><dt>**Proveedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-271"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="425f6-272">Este valor está reservado.</span><span class="sxs-lookup"><span data-stu-id="425f6-272">This value is reserved.</span></span><br/>                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="425f6-273">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="425f6-273">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-274">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="425f6-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-276">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="425f6-276">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="425f6-277">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="425f6-277">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-278">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="425f6-278">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-279">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="425f6-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-281">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="425f6-281">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="425f6-282">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="425f6-282">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-283">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="425f6-283">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-284">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-286">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="425f6-286">The current health of the element.</span></span> <span data-ttu-id="425f6-287">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="425f6-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="425f6-288">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="425f6-288">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-289">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="425f6-289">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="425f6-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-291">Matriz de cadenas de formato libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="425f6-291">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="425f6-292">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="425f6-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="425f6-293">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="425f6-293">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-294">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="425f6-294">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-296">Fecha y hora en que se creó la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="425f6-296">The date and time when the virtual machine was created.</span></span> <span data-ttu-id="425f6-297">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="425f6-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="425f6-298">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="425f6-298">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-299">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="425f6-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="425f6-301">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="425f6-301">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="425f6-302">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="425f6-302">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="425f6-303">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="425f6-303">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="425f6-304">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="425f6-304">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-305">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="425f6-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-307">Indica si el dispositivo está bloqueado, lo que impide la entrada o salida del usuario.</span><span class="sxs-lookup"><span data-stu-id="425f6-307">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="425f6-308">Esta propiedad se hereda de [**\_ UserDevice CIM**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span><span class="sxs-lookup"><span data-stu-id="425f6-308">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="425f6-309">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="425f6-309">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-310">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="425f6-310">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-312">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="425f6-312">The last error code reported by the logical device.</span></span> <span data-ttu-id="425f6-313">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="425f6-313">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-314">**Diseño**</span><span class="sxs-lookup"><span data-stu-id="425f6-314">**Layout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-315">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="425f6-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-317">Cadena que indica el formato y el diseño del teclado.</span><span class="sxs-lookup"><span data-stu-id="425f6-317">A string indicating the format and layout of the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-318">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="425f6-318">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-319">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="425f6-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-321">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="425f6-321">This property has been deprecated.</span></span> <span data-ttu-id="425f6-322">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="425f6-322">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-323">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="425f6-323">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="425f6-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="425f6-326">Calificadores: **MaxLen** (1024)</span><span class="sxs-lookup"><span data-stu-id="425f6-326">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="425f6-327">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="425f6-327">The label by which the object is known.</span></span> <span data-ttu-id="425f6-328">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="425f6-328">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="425f6-329">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="425f6-329">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="425f6-330">**NumberOfFunctionKeys**</span><span class="sxs-lookup"><span data-stu-id="425f6-330">**NumberOfFunctionKeys**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-331">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-333">Número de teclas de función del teclado.</span><span class="sxs-lookup"><span data-stu-id="425f6-333">The number of function keys on the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-334">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="425f6-334">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-335">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-337">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="425f6-337">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="425f6-338">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="425f6-338">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="425f6-339">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="425f6-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="425f6-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="425f6-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-341"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="425f6-341"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-342"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="425f6-342"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-343"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="425f6-343"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-344"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="425f6-344"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-345"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="425f6-345"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-346"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="425f6-346"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-347"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="425f6-347"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-348"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="425f6-348"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-349"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="425f6-349"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-350"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="425f6-350"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-351"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="425f6-351"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-352"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="425f6-352"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-353"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="425f6-353"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-354"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="425f6-354"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-355"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="425f6-355"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-356"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="425f6-356"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="425f6-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="425f6-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="425f6-359">)</span><span class="sxs-lookup"><span data-stu-id="425f6-359">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="425f6-360">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="425f6-360">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-361">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-361">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="425f6-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-363">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="425f6-363">The current status of the element.</span></span> <span data-ttu-id="425f6-364">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 2 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="425f6-364">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="425f6-365">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="425f6-365">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-366">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="425f6-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-368">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="425f6-368">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="425f6-369">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="425f6-369">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="425f6-370">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="425f6-370">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="425f6-371">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="425f6-371">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-372">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="425f6-372">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="425f6-373">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-374">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="425f6-374">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="425f6-375">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="425f6-375">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-376">**Contraseña**</span><span class="sxs-lookup"><span data-stu-id="425f6-376">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-377">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-378">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-379">Indica si se ha habilitado una contraseña de nivel de hardware en el teclado, evitando la entrada local.</span><span class="sxs-lookup"><span data-stu-id="425f6-379">Indicates whether a hardware-level password is enabled at the keyboard, preventing local input.</span></span>

<dt>

<span data-ttu-id="425f6-380">5</span><span class="sxs-lookup"><span data-stu-id="425f6-380">5</span></span>
</dt> <dd>

<span data-ttu-id="425f6-381">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="425f6-381">Not implemented.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="425f6-382">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="425f6-382">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-383">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-383">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="425f6-384">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-385">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="425f6-385">The power management capabilities of the device.</span></span> <span data-ttu-id="425f6-386">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="425f6-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-387">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="425f6-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-388">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="425f6-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-389">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-390">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="425f6-390">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="425f6-391">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="425f6-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-392">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="425f6-392">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-393">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="425f6-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-395">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="425f6-395">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="425f6-396">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="425f6-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-397">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="425f6-397">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-398">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-400">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="425f6-400">Provides high level status information.</span></span> <span data-ttu-id="425f6-401">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="425f6-401">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="425f6-402">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="425f6-402">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="425f6-403">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="425f6-403">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="425f6-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="425f6-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-405"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="425f6-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="425f6-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="425f6-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="425f6-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="425f6-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="425f6-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="425f6-410">)</span><span class="sxs-lookup"><span data-stu-id="425f6-410">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="425f6-411">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="425f6-411">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-412">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-414">Último estado solicitado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="425f6-414">The last requested state for the element.</span></span>



| <span data-ttu-id="425f6-415">Value</span><span class="sxs-lookup"><span data-stu-id="425f6-415">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="425f6-416">Significado</span><span class="sxs-lookup"><span data-stu-id="425f6-416">Meaning</span></span>                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="425f6-417"><dt>**No aplicable**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-417"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl> | <span data-ttu-id="425f6-418">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="425f6-418">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="425f6-419">**Estado**</span><span class="sxs-lookup"><span data-stu-id="425f6-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-420">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="425f6-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-422">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="425f6-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-423">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="425f6-423">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-424">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="425f6-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="425f6-425">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-426">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="425f6-426">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="425f6-427">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en "OK".</span><span class="sxs-lookup"><span data-stu-id="425f6-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="425f6-428">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="425f6-428">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-429">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-430">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-431">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="425f6-431">The current state of the logical device.</span></span> <span data-ttu-id="425f6-432">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="425f6-432">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-433">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="425f6-433">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-434">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="425f6-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="425f6-436">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="425f6-436">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="425f6-437">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="425f6-437">The scoping system's creation class name.</span></span> <span data-ttu-id="425f6-438">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y se establece en "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="425f6-438">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="425f6-439">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="425f6-439">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-440">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="425f6-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-441">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="425f6-442">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="425f6-442">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="425f6-443">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="425f6-443">The scoping system's name.</span></span> <span data-ttu-id="425f6-444">Este valor corresponde al valor de la propiedad **Name** de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) para el ámbito de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="425f6-444">This value corresponds to the value of the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for the scoping virtual machine.</span></span> <span data-ttu-id="425f6-445">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="425f6-445">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="425f6-446">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="425f6-446">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-447">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="425f6-447">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-448">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-449">Fecha y hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="425f6-449">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="425f6-450">Si el estado del elemento no ha cambiado y se rellena esta propiedad, debe establecerse en un valor de intervalo 0.</span><span class="sxs-lookup"><span data-stu-id="425f6-450">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="425f6-451">Si se solicitó un cambio de estado, pero se rechazó o no se procesó todavía, la propiedad no se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="425f6-451">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="425f6-452">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="425f6-452">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-453">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="425f6-453">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-454">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="425f6-454">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-455">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-456">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="425f6-456">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="425f6-457">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="425f6-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-458">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="425f6-458">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-459">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="425f6-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-460">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-461">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="425f6-461">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="425f6-462">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="425f6-462">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="425f6-463">**UnicodeSupported**</span><span class="sxs-lookup"><span data-stu-id="425f6-463">**UnicodeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="425f6-464">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="425f6-464">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="425f6-465">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="425f6-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="425f6-466">Indica si el teclado virtual admite caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="425f6-466">Indicates if the virtual keyboard supports Unicode characters.</span></span> <span data-ttu-id="425f6-467">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="425f6-467">This can be one of the following values.</span></span>



| <span data-ttu-id="425f6-468">Value</span><span class="sxs-lookup"><span data-stu-id="425f6-468">Value</span></span>                                                                            | <span data-ttu-id="425f6-469">Significado</span><span class="sxs-lookup"><span data-stu-id="425f6-469">Meaning</span></span>                                                              |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="425f6-470"><dt>True</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-470"><dt>True</dt></span></span> </dl>  | <span data-ttu-id="425f6-471">El teclado virtual admite caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="425f6-471">The virtual keyboard supports Unicode characters.</span></span><br/>         |
| <dl> <span data-ttu-id="425f6-472"><dt>False</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-472"><dt>False</dt></span></span> </dl> | <span data-ttu-id="425f6-473">El teclado virtual no admite caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="425f6-473">The virtual keyboard does not support Unicode characters.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="425f6-474">Observaciones</span><span class="sxs-lookup"><span data-stu-id="425f6-474">Remarks</span></span>

<span data-ttu-id="425f6-475">El acceso a la clase de **\_ teclado MSVM** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="425f6-475">Access to the **Msvm\_Keyboard** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="425f6-476">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="425f6-476">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="425f6-477">Requisitos</span><span class="sxs-lookup"><span data-stu-id="425f6-477">Requirements</span></span>



| <span data-ttu-id="425f6-478">Requisito</span><span class="sxs-lookup"><span data-stu-id="425f6-478">Requirement</span></span> | <span data-ttu-id="425f6-479">Value</span><span class="sxs-lookup"><span data-stu-id="425f6-479">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="425f6-480">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="425f6-480">Minimum supported client</span></span><br/> | <span data-ttu-id="425f6-481">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="425f6-481">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="425f6-482">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="425f6-482">Minimum supported server</span></span><br/> | <span data-ttu-id="425f6-483">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="425f6-483">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="425f6-484">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="425f6-484">Namespace</span></span><br/>                | <span data-ttu-id="425f6-485">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="425f6-485">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="425f6-486">MOF</span><span class="sxs-lookup"><span data-stu-id="425f6-486">MOF</span></span><br/>                      | <dl> <span data-ttu-id="425f6-487"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-487"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="425f6-488">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="425f6-488">DLL</span></span><br/>                      | <dl> <span data-ttu-id="425f6-489"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="425f6-489"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="425f6-490">Vea también</span><span class="sxs-lookup"><span data-stu-id="425f6-490">See also</span></span>

<dl> <dt>

[<span data-ttu-id="425f6-491">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="425f6-491">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> <dt>

[<span data-ttu-id="425f6-492">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="425f6-492">**CIM\_UserDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-userdevice)
</dt> <dt>

[<span data-ttu-id="425f6-493">Clases de entrada</span><span class="sxs-lookup"><span data-stu-id="425f6-493">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

