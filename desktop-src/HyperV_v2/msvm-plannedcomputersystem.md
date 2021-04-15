---
description: Representa una máquina virtual planeada.
ms.assetid: 4ce6d34c-66fb-4f4f-bf52-26d19bab6d4a
title: Msvm_PlannedComputerSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem
- Msvm_PlannedComputerSystem.SetPowerState
- Msvm_PlannedComputerSystem.InstanceID
- Msvm_PlannedComputerSystem.Caption
- Msvm_PlannedComputerSystem.Description
- Msvm_PlannedComputerSystem.ElementName
- Msvm_PlannedComputerSystem.InstallDate
- Msvm_PlannedComputerSystem.OperationalStatus
- Msvm_PlannedComputerSystem.StatusDescriptions
- Msvm_PlannedComputerSystem.Status
- Msvm_PlannedComputerSystem.HealthState
- Msvm_PlannedComputerSystem.CommunicationStatus
- Msvm_PlannedComputerSystem.DetailedStatus
- Msvm_PlannedComputerSystem.OperatingStatus
- Msvm_PlannedComputerSystem.PrimaryStatus
- Msvm_PlannedComputerSystem.EnabledState
- Msvm_PlannedComputerSystem.OtherEnabledState
- Msvm_PlannedComputerSystem.RequestedState
- Msvm_PlannedComputerSystem.EnabledDefault
- Msvm_PlannedComputerSystem.TimeOfLastStateChange
- Msvm_PlannedComputerSystem.AvailableRequestedStates
- Msvm_PlannedComputerSystem.TransitioningToState
- Msvm_PlannedComputerSystem.CreationClassName
- Msvm_PlannedComputerSystem.Name
- Msvm_PlannedComputerSystem.NameFormat
- Msvm_PlannedComputerSystem.PrimaryOwnerName
- Msvm_PlannedComputerSystem.PrimaryOwnerContact
- Msvm_PlannedComputerSystem.Roles
- Msvm_PlannedComputerSystem.OtherIdentifyingInfo
- Msvm_PlannedComputerSystem.IdentifyingDescriptions
- Msvm_PlannedComputerSystem.Dedicated
- Msvm_PlannedComputerSystem.OtherDedicatedDescriptions
- Msvm_PlannedComputerSystem.ResetCapability
- Msvm_PlannedComputerSystem.PowerManagementCapabilities
- Msvm_PlannedComputerSystem.AssignedNumaNodeList
- Msvm_PlannedComputerSystem.OnTimeInMilliseconds
- Msvm_PlannedComputerSystem.ProcessID
- Msvm_PlannedComputerSystem.TimeOfLastConfigurationChange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 54bd72567880e97ece02936348d5a091a11d8ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688553"
---
# <a name="msvm_plannedcomputersystem-class"></a><span data-ttu-id="934cf-103">MSVM \_ PlannedComputerSystem (clase)</span><span class="sxs-lookup"><span data-stu-id="934cf-103">Msvm\_PlannedComputerSystem class</span></span>

<span data-ttu-id="934cf-104">Representa una máquina virtual planeada.</span><span class="sxs-lookup"><span data-stu-id="934cf-104">Represents a planned virtual machine.</span></span>

<span data-ttu-id="934cf-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="934cf-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="934cf-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="934cf-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PlannedComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption = "Planned Virtual Machine";
  string   Description = "Microsoft Planned Virtual Machine";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability;
  uint16   PowerManagementCapabilities[];
  uint16   AssignedNumaNodeList[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
};
```

## <a name="members"></a><span data-ttu-id="934cf-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="934cf-107">Members</span></span>

<span data-ttu-id="934cf-108">La clase **MSVM \_ PlannedComputerSystem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="934cf-108">The **Msvm\_PlannedComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="934cf-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="934cf-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="934cf-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="934cf-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="934cf-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="934cf-111">Methods</span></span>

<span data-ttu-id="934cf-112">La clase **MSVM \_ PlannedComputerSystem** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="934cf-112">The **Msvm\_PlannedComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="934cf-113">Método</span><span class="sxs-lookup"><span data-stu-id="934cf-113">Method</span></span>                                                                      | <span data-ttu-id="934cf-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="934cf-114">Description</span></span>                                                                                 |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="934cf-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="934cf-115">**RequestStateChange**</span></span>](requeststatechange-msvm-plannedcomputersystem.md) | <span data-ttu-id="934cf-116">Solicita que el estado del sistema planeado cambie al valor especificado.</span><span class="sxs-lookup"><span data-stu-id="934cf-116">Requests that the state of the planned system be changed to the value specified.</span></span><br/> |
| <span data-ttu-id="934cf-117">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="934cf-117">**SetPowerState**</span></span>                                                           | <span data-ttu-id="934cf-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="934cf-118">This method is not supported.</span></span><br/>                                                    |



 

### <a name="properties"></a><span data-ttu-id="934cf-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="934cf-119">Properties</span></span>

<span data-ttu-id="934cf-120">La clase **MSVM \_ PlannedComputerSystem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="934cf-120">The **Msvm\_PlannedComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="934cf-121">**AssignedNumaNodeList**</span><span class="sxs-lookup"><span data-stu-id="934cf-121">**AssignedNumaNodeList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-122">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="934cf-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="934cf-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="934cf-124">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="934cf-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="934cf-125">Matriz de nodos de acceso a memoria no uniforme (NUMA) que están asignados actualmente a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="934cf-125">An array of nonuniform memory access (NUMA) nodes that are currently assigned to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-126">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="934cf-126">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-127">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="934cf-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="934cf-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-129">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="934cf-129">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="934cf-130">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual del objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="934cf-130">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="934cf-131">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="934cf-131">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="934cf-132">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="934cf-132">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="934cf-133">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="934cf-133">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="934cf-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="934cf-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="934cf-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="934cf-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="934cf-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="934cf-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="934cf-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="934cf-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="934cf-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="934cf-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="934cf-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="934cf-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="934cf-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="934cf-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="934cf-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="934cf-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="934cf-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="934cf-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="934cf-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="934cf-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="934cf-144">)</span><span class="sxs-lookup"><span data-stu-id="934cf-144">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="934cf-145">**Caption**</span><span class="sxs-lookup"><span data-stu-id="934cf-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="934cf-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-148">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="934cf-148">A short description of the object.</span></span> <span data-ttu-id="934cf-149">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "máquina virtual planeada".</span><span class="sxs-lookup"><span data-stu-id="934cf-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Planned Virtual Machine".</span></span>

</dd> <dt>

<span data-ttu-id="934cf-150">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="934cf-150">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-151">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="934cf-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-153">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="934cf-153">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="934cf-154">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="934cf-154">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="934cf-155">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="934cf-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="934cf-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="934cf-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="934cf-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="934cf-159">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="934cf-159">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="934cf-160">Indica el nombre de la clase o la subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="934cf-160">Indicates the name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="934cf-161">Cuando se usa con las otras propiedades de clave de esta clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="934cf-161">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="934cf-162">Esta propiedad se hereda de la [**clase \_ del sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="934cf-162">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-163">**Dedicado**</span><span class="sxs-lookup"><span data-stu-id="934cf-163">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-164">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="934cf-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="934cf-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-166">Matriz de valores que indican los propósitos a los que está dedicado el sistema planeado, si existe, y qué funcionalidad se proporciona.</span><span class="sxs-lookup"><span data-stu-id="934cf-166">An array of values that indicate the purposes to which the planned system is dedicated, if any, and what functionality is provided.</span></span> <span data-ttu-id="934cf-167">Por ejemplo, puede especificar que el sistema esté dedicado a "Print" (valor = 11) o que actúe como un "concentrador" (valor = 8).</span><span class="sxs-lookup"><span data-stu-id="934cf-167">For example, one could specify that the System is dedicated to "Print" (value=11) or acts as a "Hub" (value=8).</span></span> <span data-ttu-id="934cf-168">También se pueden indicar varios propósitos.</span><span class="sxs-lookup"><span data-stu-id="934cf-168">Multiple purposes can also be indicated.</span></span> <span data-ttu-id="934cf-169">Por ejemplo, se trata de un sistema de uso general que indica "no dedicado" (valor = 0), pero también hospeda los servicios "Imprimir" (valor = 11) o "dispositivo de usuario móvil" (valor = 17).</span><span class="sxs-lookup"><span data-stu-id="934cf-169">For example, this is a general purpose system indicating "Not Dedicated" (value=0) but that it also hosts "Print" (value=11) or "Mobile User Device" (value=17) services.</span></span>

<span data-ttu-id="934cf-170">Esta propiedad se hereda de la clase de [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) .</span><span class="sxs-lookup"><span data-stu-id="934cf-170">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>



| <span data-ttu-id="934cf-171">Value</span><span class="sxs-lookup"><span data-stu-id="934cf-171">Value</span></span>                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="934cf-172">Significado</span><span class="sxs-lookup"><span data-stu-id="934cf-172">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span><dl> <span data-ttu-id="934cf-173"><dt>**No dedicado**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-173"><dt>**Not Dedicated**</dt> <dt>0</dt></span></span> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="934cf-174"><dt>**Desconocido**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-174"><dt>**Unknown**</dt> <dt>1</dt></span></span> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="934cf-175"><dt>**Otros**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-175"><dt>**Other**</dt> <dt>2</dt></span></span> </dl>                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span><dl> <span data-ttu-id="934cf-176"><dt>**Almacenamiento**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-176"><dt>**Storage**</dt> <dt>3</dt></span></span> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Router"></span><span id="router"></span><span id="ROUTER"></span><dl> <span data-ttu-id="934cf-177"><dt>**Enrutador**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-177"><dt>**Router**</dt> <dt>4</dt></span></span> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span><dl> <span data-ttu-id="934cf-178"><dt>**Conmutador**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-178"><dt>**Switch**</dt> <dt>5</dt></span></span> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span><dl> <span data-ttu-id="934cf-179"><dt>**Conmutador de nivel 3**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-179"><dt>**Layer 3 Switch**</dt> <dt>6</dt></span></span> </dl>                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span><dl> <span data-ttu-id="934cf-180"><dt>**Conmutador de oficina central**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-180"><dt>**Central Office Switch**</dt> <dt>7</dt></span></span> </dl>                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Hub"></span><span id="hub"></span><span id="HUB"></span><dl> <span data-ttu-id="934cf-181"><dt>**Concentrador**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-181"><dt>**Hub**</dt> <dt>8</dt></span></span> </dl>                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span><dl> <span data-ttu-id="934cf-182"><dt>**Access Server**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-182"><dt>**Access Server**</dt> <dt>9</dt></span></span> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span><dl> <span data-ttu-id="934cf-183"><dt>**Firewall**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-183"><dt>**Firewall**</dt> <dt>10</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Print"></span><span id="print"></span><span id="PRINT"></span><dl> <span data-ttu-id="934cf-184"><dt>**Imprimir**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-184"><dt>**Print**</dt> <dt>11</dt></span></span> </dl>                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="I_O"></span><span id="i_o"></span><dl> <span data-ttu-id="934cf-185"><dt>**E/s**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-185"><dt>**I/O**</dt> <dt>12</dt></span></span> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span><dl> <span data-ttu-id="934cf-186"><dt>**Almacenamiento en caché Web**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-186"><dt>**Web Caching**</dt> <dt>13</dt></span></span> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span><dl> <span data-ttu-id="934cf-187"><dt>**Administración**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-187"><dt>**Management**</dt> <dt>14</dt></span></span> </dl>                                                                 | <span data-ttu-id="934cf-188">Indica que esta instancia está dedicada a hospedar el software de administración del sistema.</span><span class="sxs-lookup"><span data-stu-id="934cf-188">Indicates this instance is dedicated to hosting system management software.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span><dl> <span data-ttu-id="934cf-189"><dt>**Bloquear servidor**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-189"><dt>**Block Server**</dt> <dt>15</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span><dl> <span data-ttu-id="934cf-190"><dt>**Servidor de archivos**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-190"><dt>**File Server**</dt> <dt>16</dt></span></span> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span><dl> <span data-ttu-id="934cf-191"><dt>**Dispositivo de usuario móvil**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-191"><dt>**Mobile User Device**</dt> <dt>17</dt></span></span> </dl>                                 | <span data-ttu-id="934cf-192">Un ejemplo de dispositivo de usuario móvil dedicado es un teléfono móvil o un escáner de código de barras en un almacén que se comunica a través de la frecuencia de radio.</span><span class="sxs-lookup"><span data-stu-id="934cf-192">An example of a dedicated mobile user device is a mobile phone or a bar code scanner in a store that communicates through radio frequency.</span></span> <span data-ttu-id="934cf-193">Estos sistemas están bastante limitados en cuanto a funcionalidad y programación, y no se consideran plataformas de informática de uso general.</span><span class="sxs-lookup"><span data-stu-id="934cf-193">These systems are quite limited in functionality and programmability, and are not considered general purpose computing platforms.</span></span> <span data-ttu-id="934cf-194">Como alternativa, un ejemplo de un sistema móvil que es de uso general (es decir, no está dedicado) es un equipo que se mantiene a mano.</span><span class="sxs-lookup"><span data-stu-id="934cf-194">Alternately, an example of a mobile system that is general purpose (that is, is NOT dedicated) is a hand-held computer.</span></span> <span data-ttu-id="934cf-195">Aunque está limitado en su programación, el nuevo software se puede descargar y su funcionalidad se expande por el usuario.</span><span class="sxs-lookup"><span data-stu-id="934cf-195">Although limited in its programmability, new software can be downloaded and its functionality expanded by the user.</span></span> <br/> |
| <span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span><dl> <span data-ttu-id="934cf-196"><dt>**Repetidor**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-196"><dt>**Repeater**</dt> <dt>18</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span><dl> <span data-ttu-id="934cf-197"><dt>**Bridge/extender**</dt> <dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-197"><dt>**Bridge/Extender**</dt> <dt>19</dt></span></span> </dl>                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span><dl> <span data-ttu-id="934cf-198"><dt>**Puerta de enlace**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-198"><dt>**Gateway**</dt> <dt>20</dt></span></span> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span><dl> <span data-ttu-id="934cf-199"><dt>**Virtualizador de almacenamiento**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-199"><dt>**Storage Virtualizer**</dt> <dt>21</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span><dl> <span data-ttu-id="934cf-200"><dt>**Biblioteca multimedia**</dt> <dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-200"><dt>**Media Library**</dt> <dt>22</dt></span></span> </dl>                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span><dl> <span data-ttu-id="934cf-201"><dt>**ExtenderNode**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-201"><dt>**ExtenderNode**</dt> <dt>23</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span><dl> <span data-ttu-id="934cf-202"><dt>**Director de NAS**</dt> <dt>24</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-202"><dt>**NAS Head**</dt> <dt>24</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span><dl> <span data-ttu-id="934cf-203"><dt>**NAS independiente**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-203"><dt>**Self-contained NAS**</dt> <dt>25</dt></span></span> </dl>                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="UPS"></span><span id="ups"></span><dl> <span data-ttu-id="934cf-204"><dt>**UPS**</dt> <dt>26</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-204"><dt>**UPS**</dt> <dt>26</dt></span></span> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span><dl> <span data-ttu-id="934cf-205"><dt>**Teléfono IP**</dt> <dt>27</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-205"><dt>**IP Phone**</dt> <dt>27</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span><dl> <span data-ttu-id="934cf-206"><dt>**Controlador de administración**</dt> <dt>28</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-206"><dt>**Management Controller**</dt> <dt>28</dt></span></span> </dl>                     | <span data-ttu-id="934cf-207">Indica que esta instancia representa el hardware especializado dedicado a la administración de sistemas (es decir, un controlador de administración de placa base (BMC) o un procesador de servicio).</span><span class="sxs-lookup"><span data-stu-id="934cf-207">Indicates this instance represents specialized hardware dedicated to systems management (that is, a Baseboard Management Controller (BMC) or service processor).</span></span> <span data-ttu-id="934cf-208">El ámbito de administración de un controlador de administración suele ser un único sistema administrado en el que está contenido.</span><span class="sxs-lookup"><span data-stu-id="934cf-208">The management scope of a Management Controller is typically a single managed system in which it is contained.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span><dl> <span data-ttu-id="934cf-209"><dt>**Administrador de chasis**</dt> <dt>29</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-209"><dt>**Chassis Manager**</dt> <dt>29</dt></span></span> </dl>                                             | <span data-ttu-id="934cf-210">Indica que esta instancia representa un sistema dedicado a la administración de un chasis de hoja y sus dispositivos contenidos.</span><span class="sxs-lookup"><span data-stu-id="934cf-210">Indicates this instance represents a system dedicated to management of a blade chassis and its contained devices.</span></span> <span data-ttu-id="934cf-211">Este valor se utiliza para representar un controlador de estantería.</span><span class="sxs-lookup"><span data-stu-id="934cf-211">This value would be used to represent a Shelf Controller.</span></span> <span data-ttu-id="934cf-212">Un administrador de chasis es un punto de agregación para la administración y puede depender de controladores de administración subordinados para la administración de partes constituyentes.</span><span class="sxs-lookup"><span data-stu-id="934cf-212">A Chassis Manager is an aggregation point for management and may rely on subordinate management controllers for the management of constituent parts.</span></span> <br/>                                                                                                                                                                                         |
| <span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span><dl> <span data-ttu-id="934cf-213"><dt>**Controladora RAID basado en host**</dt> <dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-213"><dt>**Host-based RAID controller**</dt> <dt>30</dt></span></span> </dl> | <span data-ttu-id="934cf-214">Indica que esta instancia representa un controlador de almacenamiento RAID incluido en un equipo host.</span><span class="sxs-lookup"><span data-stu-id="934cf-214">Indicates this instance represents a RAID storage controller contained within a host computer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span><dl> <span data-ttu-id="934cf-215"><dt>**Contenedor de dispositivos de almacenamiento**</dt> <dt>31</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-215"><dt>**Storage Device Enclosure**</dt> <dt>31</dt></span></span> </dl>         | <span data-ttu-id="934cf-216">Indica que esta instancia representa un contenedor que contiene dispositivos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="934cf-216">Indicates this instance represents an enclosure that contains storage devices.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span><dl> <span data-ttu-id="934cf-217"><dt>**Escritorio**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-217"><dt>**Desktop**</dt> <dt>32</dt></span></span> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span><dl> <span data-ttu-id="934cf-218"><dt>**Portátil**</dt> <dt>33</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-218"><dt>**Laptop**</dt> <dt>33</dt></span></span> </dl>                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span><dl> <span data-ttu-id="934cf-219"><dt>**Biblioteca de cintas virtuales**</dt> <dt>34</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-219"><dt>**Virtual Tape Library**</dt> <dt>34</dt></span></span> </dl>                         | <span data-ttu-id="934cf-220">La emulación de una biblioteca de cintas por un sistema de biblioteca virtual.</span><span class="sxs-lookup"><span data-stu-id="934cf-220">The emulation of a tape library by a Virtual Library System.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span><dl> <span data-ttu-id="934cf-221"><dt>**Sistema de Biblioteca Virtual**</dt> <dt>35</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-221"><dt>**Virtual Library System**</dt> <dt>35</dt></span></span> </dl>                 | <span data-ttu-id="934cf-222">Usa el almacenamiento en disco para emular las bibliotecas de cintas.</span><span class="sxs-lookup"><span data-stu-id="934cf-222">Uses disk storage to emulate tape libraries.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span><dl> <span data-ttu-id="934cf-223"><dt>**PC de red/cliente ligero**</dt> <dt>36</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-223"><dt>**Network PC/Thin Client**</dt> <dt>36</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span><dl> <span data-ttu-id="934cf-224"><dt>**Conmutador FC**</dt> <dt>37</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-224"><dt>**FC Switch**</dt> <dt>37</dt></span></span> </dl>                                                                     | <span data-ttu-id="934cf-225">Indica que esta instancia está dedicada a cambiar los fotogramas de la capa 2 Canal de fibra.</span><span class="sxs-lookup"><span data-stu-id="934cf-225">Indicates this instance is dedicated to switching layer 2 Fibre Channel frames.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span><dl> <span data-ttu-id="934cf-226"><dt>**Conmutador Ethernet**</dt> <dt>38</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-226"><dt>**Ethernet Switch**</dt> <dt>38</dt></span></span> </dl>                                             | <span data-ttu-id="934cf-227">Indica que esta instancia está dedicada a cambiar los fotogramas Ethernet de capa 2.</span><span class="sxs-lookup"><span data-stu-id="934cf-227">Indicates this instance is dedicated to switching layer 2 Ethernet frames.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="934cf-228"><dt>**DMTF reservado**</dt> <dt>39.. 32567</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-228"><dt>**DMTF Reserved**</dt> <dt>39..32567</dt></span></span> </dl>                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="934cf-229">32568 <dt> **reservada de proveedor**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-229"><dt>**Vendor Reserved** </dt> <dt>32568..65535</dt></span></span> </dl>                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="934cf-230">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="934cf-230">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-231">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="934cf-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-233">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="934cf-233">A description of the object.</span></span> <span data-ttu-id="934cf-234">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "máquina virtual planeada de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="934cf-234">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Planned Virtual Machine".</span></span>

</dd> <dt>

<span data-ttu-id="934cf-235">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="934cf-235">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-236">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="934cf-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-238">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="934cf-238">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="934cf-239">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="934cf-239">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="934cf-240">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="934cf-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="934cf-241">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="934cf-241">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-242">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="934cf-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-244">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="934cf-244">A display name for the object.</span></span> <span data-ttu-id="934cf-245">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="934cf-245">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="934cf-246">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="934cf-246">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-247">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="934cf-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-249">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="934cf-249">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="934cf-250">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="934cf-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and can be one of the following values.</span></span>



| <span data-ttu-id="934cf-251">Value</span><span class="sxs-lookup"><span data-stu-id="934cf-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="934cf-252">Significado</span><span class="sxs-lookup"><span data-stu-id="934cf-252">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="934cf-253"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-253"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="934cf-254">El sistema está desactivado.</span><span class="sxs-lookup"><span data-stu-id="934cf-254">The system is turned off.</span></span><br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="934cf-255"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-255"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="934cf-256">El sistema está habilitado, pero sin conexión.</span><span class="sxs-lookup"><span data-stu-id="934cf-256">The system is enabled, but offline.</span></span> <span data-ttu-id="934cf-257">Se quitarán las nuevas solicitudes.</span><span class="sxs-lookup"><span data-stu-id="934cf-257">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="934cf-258">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="934cf-258">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-259">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="934cf-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-260">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-261">Especifica el estado habilitado del sistema planeado.</span><span class="sxs-lookup"><span data-stu-id="934cf-261">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="934cf-262">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="934cf-262">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="934cf-263">Value</span><span class="sxs-lookup"><span data-stu-id="934cf-263">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="934cf-264">Significado</span><span class="sxs-lookup"><span data-stu-id="934cf-264">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="934cf-265"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-265"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="934cf-266">El sistema está desactivado.</span><span class="sxs-lookup"><span data-stu-id="934cf-266">The system is turned off.</span></span><br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="934cf-267"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-267"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="934cf-268">El sistema está habilitado, pero sin conexión.</span><span class="sxs-lookup"><span data-stu-id="934cf-268">The system is enabled, but offline.</span></span> <span data-ttu-id="934cf-269">Se quitarán las nuevas solicitudes.</span><span class="sxs-lookup"><span data-stu-id="934cf-269">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="934cf-270">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="934cf-270">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-271">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="934cf-271">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-273">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="934cf-273">The current health of the element.</span></span> <span data-ttu-id="934cf-274">Esta propiedad expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="934cf-274">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="934cf-275">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="934cf-275">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="934cf-276">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="934cf-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="934cf-277">Value</span><span class="sxs-lookup"><span data-stu-id="934cf-277">Value</span></span>                                                                        | <span data-ttu-id="934cf-278">Significado</span><span class="sxs-lookup"><span data-stu-id="934cf-278">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="934cf-279"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-279"><dt>5</dt></span></span> </dl> | <span data-ttu-id="934cf-280">El estado de mantenimiento es normal.</span><span class="sxs-lookup"><span data-stu-id="934cf-280">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="934cf-281">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="934cf-281">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-282">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="934cf-282">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="934cf-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-284">Una matriz de cadenas que proporcionan explicaciones y detalles detrás de las entradas de la matriz **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="934cf-284">An array of strings providing explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="934cf-285">Cada entrada de esta matriz está relacionada con la entrada de **OtherIdentifyingInfo** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="934cf-285">Each entry of this array is related to the entry in **OtherIdentifyingInfo** that is located at the same index.</span></span> <span data-ttu-id="934cf-286">Esta propiedad se hereda de la [**clase \_ del sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="934cf-286">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-287">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="934cf-287">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-288">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="934cf-288">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-290">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="934cf-290">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="934cf-291">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="934cf-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="934cf-292">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="934cf-292">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-293">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="934cf-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="934cf-295">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="934cf-295">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="934cf-296">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="934cf-296">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="934cf-297">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="934cf-297">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="934cf-298">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="934cf-298">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-299">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="934cf-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="934cf-301">Calificadores: **clave**, **invalidación**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="934cf-301">Qualifiers: **Key**, **Override**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="934cf-302">El nombre heredado actúa como la clave de una instancia del sistema en un entorno empresarial.</span><span class="sxs-lookup"><span data-stu-id="934cf-302">The inherited name serves as the key of a system instance in an enterprise environment.</span></span> <span data-ttu-id="934cf-303">Esta propiedad se hereda de la [**clase \_ del sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="934cf-303">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-304">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="934cf-304">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-305">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="934cf-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="934cf-307">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="934cf-307">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="934cf-308">Identifica cómo se generó el nombre del sistema, mediante la heurística de la subclase.</span><span class="sxs-lookup"><span data-stu-id="934cf-308">Identifies how the system name was generated, using the heuristic of the subclass.</span></span> <span data-ttu-id="934cf-309">El objeto del sistema y sus derivados son objetos de nivel superior de CIM.</span><span class="sxs-lookup"><span data-stu-id="934cf-309">The system object and its derivatives are top-level objects of CIM.</span></span> <span data-ttu-id="934cf-310">Proporcionan el ámbito para numerosos componentes.</span><span class="sxs-lookup"><span data-stu-id="934cf-310">They provide the scope for numerous components.</span></span> <span data-ttu-id="934cf-311">Se requiere tener claves de sistema únicas.</span><span class="sxs-lookup"><span data-stu-id="934cf-311">Having unique system keys is required.</span></span> <span data-ttu-id="934cf-312">Se puede definir una heurística en subclases del sistema individuales para intentar generar siempre la misma clave de nombre del sistema.</span><span class="sxs-lookup"><span data-stu-id="934cf-312">A heuristic can be defined in individual system subclasses to attempt to always generate the same system name key.</span></span> <span data-ttu-id="934cf-313">Esta propiedad se hereda de la [**clase \_ del sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="934cf-313">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-314">**OnTimeInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="934cf-314">**OnTimeInMilliseconds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-315">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="934cf-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="934cf-317">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos")</span><span class="sxs-lookup"><span data-stu-id="934cf-317">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="934cf-318">Tiempo total, en milisegundos, transcurrido desde que la máquina virtual se activó, restableció o restauró por última vez.</span><span class="sxs-lookup"><span data-stu-id="934cf-318">The total time, in milliseconds, since the virtual machine was last turned on, reset, or restored.</span></span> <span data-ttu-id="934cf-319">Esta vez excluye la hora en que la máquina virtual estaba en estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="934cf-319">This time excludes the time the virtual machine was in the paused state.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="934cf-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-321">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="934cf-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-323">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="934cf-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="934cf-324">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="934cf-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="934cf-325">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="934cf-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="934cf-326">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="934cf-326">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-327">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="934cf-327">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="934cf-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-329">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="934cf-329">The current statuses of the object.</span></span> <span data-ttu-id="934cf-330">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="934cf-330">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="934cf-331">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="934cf-331">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-332">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="934cf-332">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="934cf-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-334">Cadena que describe cómo o por qué el sistema está dedicado cuando la matriz dedicada incluye el valor 2, "Other".</span><span class="sxs-lookup"><span data-stu-id="934cf-334">A string describing how or why the system is dedicated when the Dedicated array includes the value 2, "Other".</span></span> <span data-ttu-id="934cf-335">Esta propiedad se hereda de la clase de [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) .</span><span class="sxs-lookup"><span data-stu-id="934cf-335">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-336">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="934cf-336">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-337">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="934cf-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-339">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="934cf-339">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="934cf-340">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="934cf-340">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="934cf-341">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="934cf-341">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-342">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="934cf-342">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-343">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="934cf-343">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="934cf-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="934cf-345">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="934cf-345">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="934cf-346">Contiene datos adicionales, más allá de la información del nombre del sistema, que se pueden usar para identificar un ComputerSystem.</span><span class="sxs-lookup"><span data-stu-id="934cf-346">Contains additional data, beyond system name information, that can be used to identify a ComputerSystem.</span></span> <span data-ttu-id="934cf-347">Un ejemplo sería mantener el Canal de fibra nombre World Wide Name (WWN) de un nodo.</span><span class="sxs-lookup"><span data-stu-id="934cf-347">One example would be to hold the Fibre Channel World-Wide Name (WWN) of a node.</span></span> <span data-ttu-id="934cf-348">Si solo el nombre del Canal de fibra está disponible y es único (se puede usar como clave del sistema), esta propiedad sería **null** y el WWN se convertiría en la clave del sistema, sus datos se colocan en la propiedad **nombre** .</span><span class="sxs-lookup"><span data-stu-id="934cf-348">If only the Fibre Channel name is available and is unique (able to be used as the system key), then this property would be **Null** and the WWN would become the system key, its data placed in the **Name** property.</span></span> <span data-ttu-id="934cf-349">Esta propiedad se hereda de la [**clase \_ del sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="934cf-349">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-350">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="934cf-350">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-351">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="934cf-351">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="934cf-352">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-353">Esta propiedad se hereda de la clase de [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) , pero no se admite.</span><span class="sxs-lookup"><span data-stu-id="934cf-353">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class, but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-354">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="934cf-354">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-355">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="934cf-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-356">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="934cf-356">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="934cf-357">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="934cf-357">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="934cf-358">Una cadena que proporciona información sobre cómo se puede alcanzar el propietario del sistema principal (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.).</span><span class="sxs-lookup"><span data-stu-id="934cf-358">A string that provides information on how the primary system owner can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="934cf-359">Esta propiedad se hereda de la [**clase \_ del sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="934cf-359">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-360">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="934cf-360">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-361">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="934cf-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-362">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="934cf-362">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="934cf-363">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="934cf-363">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="934cf-364">Nombre del propietario del sistema principal.</span><span class="sxs-lookup"><span data-stu-id="934cf-364">The name of the primary system owner.</span></span> <span data-ttu-id="934cf-365">El propietario del sistema es el usuario principal del sistema.</span><span class="sxs-lookup"><span data-stu-id="934cf-365">The system owner is the primary user of the system.</span></span> <span data-ttu-id="934cf-366">Esta propiedad se hereda de la [**clase \_ del sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="934cf-366">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-367">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="934cf-367">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-368">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="934cf-368">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-370">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="934cf-370">Provides high level status information.</span></span> <span data-ttu-id="934cf-371">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="934cf-371">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="934cf-372">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="934cf-372">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="934cf-373">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="934cf-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="934cf-374">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="934cf-374">**ProcessID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-375">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="934cf-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-376">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-377">El identificador del proceso en el que se está ejecutando esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="934cf-377">The identifier of the process under which this virtual machine is running.</span></span> <span data-ttu-id="934cf-378">Este valor se puede usar para identificar de forma única la instancia de Vmwp.exe en el sistema que ejecuta la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="934cf-378">This value can be used to uniquely identify the instance of Vmwp.exe on the system that is running the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-379">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="934cf-379">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-380">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="934cf-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-382">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="934cf-382">The last requested or desired state for the element.</span></span> <span data-ttu-id="934cf-383">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="934cf-383">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="934cf-384">Esta propiedad se proporciona para comparar el último estado solicitado y el actual para un elemento.</span><span class="sxs-lookup"><span data-stu-id="934cf-384">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="934cf-385">Una instancia concreta de la [**clase \_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir la propiedad **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="934cf-385">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="934cf-386">Si esto ocurre, se usa el valor 12 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="934cf-386">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="934cf-387">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM** y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="934cf-387">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="934cf-388">Value</span><span class="sxs-lookup"><span data-stu-id="934cf-388">Value</span></span>                                                                         | <span data-ttu-id="934cf-389">Significado</span><span class="sxs-lookup"><span data-stu-id="934cf-389">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="934cf-390"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-390"><dt>12</dt></span></span> </dl> | <span data-ttu-id="934cf-391">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="934cf-391">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="934cf-392">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="934cf-392">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-393">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="934cf-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-395">Especifica las capacidades de restablecimiento del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="934cf-395">Specifies the reset capabilities of the computer system.</span></span> <span data-ttu-id="934cf-396">Esta propiedad se hereda de la clase de [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) .</span><span class="sxs-lookup"><span data-stu-id="934cf-396">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>



| <span data-ttu-id="934cf-397">Value</span><span class="sxs-lookup"><span data-stu-id="934cf-397">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="934cf-398">Significado</span><span class="sxs-lookup"><span data-stu-id="934cf-398">Meaning</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="934cf-399"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-399"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                              |                                                                                                            |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="934cf-400"><dt>**Desconocido**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-400"><dt>**Unknown**</dt> <dt>2</dt></span></span> </dl>                                      |                                                                                                            |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="934cf-401"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-401"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                  | <span data-ttu-id="934cf-402">No se permite el restablecimiento de hardware.</span><span class="sxs-lookup"><span data-stu-id="934cf-402">Hardware reset is not allowed.</span></span> <br/>                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="934cf-403"><dt>**Habilitado**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-403"><dt>**Enabled**</dt> <dt>4</dt></span></span> </dl>                                      | <span data-ttu-id="934cf-404">El equipo se puede restablecer mediante hardware (por ejemplo, los botones de encendido y restablecimiento).</span><span class="sxs-lookup"><span data-stu-id="934cf-404">The computer system can be reset by using hardware (for example, the power and reset buttons).</span></span> <br/> |
| <span id="Not_Implemented_"></span><span id="not_implemented_"></span><span id="NOT_IMPLEMENTED_"></span><dl> <span data-ttu-id="934cf-405"><dt> **No implementado**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-405"><dt>**Not Implemented** </dt> <dt>5 </dt></span></span> </dl> |                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="934cf-406">**Roles**</span><span class="sxs-lookup"><span data-stu-id="934cf-406">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-407">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="934cf-407">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="934cf-408">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="934cf-408">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="934cf-409">Matriz de cadenas que especifica los roles definidos por el administrador que este sistema desempeña en el entorno administrado.</span><span class="sxs-lookup"><span data-stu-id="934cf-409">An array of strings that specifies the administrator-defined roles this system plays in the managed environment.</span></span> <span data-ttu-id="934cf-410">Algunos ejemplos podrían ser "compilar 8 servidores de impresión" o "directorios de usuario de Boise".</span><span class="sxs-lookup"><span data-stu-id="934cf-410">Examples might be "Building 8 print server" or "Boise user directories".</span></span> <span data-ttu-id="934cf-411">Un solo sistema puede realizar varios roles.</span><span class="sxs-lookup"><span data-stu-id="934cf-411">A single system may perform multiple roles.</span></span> <span data-ttu-id="934cf-412">La vista de instrumentación de los roles de un sistema se define creando una instancia de una subclase específica del sistema, o bien mediante las propiedades de una subclase o ambos.</span><span class="sxs-lookup"><span data-stu-id="934cf-412">The instrumentation view of the roles of a system is defined by instantiating a specific subclass of system, or by properties in a subclass, or both.</span></span> <span data-ttu-id="934cf-413">Por ejemplo, el propósito de un ComputerSystem se define mediante las propiedades **dedicadas** y **OtherDedicatedDescription** .</span><span class="sxs-lookup"><span data-stu-id="934cf-413">For example, the purpose of a ComputerSystem is defined using the **Dedicated** and **OtherDedicatedDescription** properties.</span></span> <span data-ttu-id="934cf-414">Esta propiedad se hereda de la [**clase \_ del sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="934cf-414">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-415">**Estado**</span><span class="sxs-lookup"><span data-stu-id="934cf-415">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-416">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="934cf-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-417">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-418">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="934cf-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-419">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="934cf-419">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-420">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="934cf-420">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="934cf-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-422">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="934cf-422">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="934cf-423">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "el servicio se está ejecutando normalmente".</span><span class="sxs-lookup"><span data-stu-id="934cf-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="934cf-424">**TimeOfLastConfigurationChange**</span><span class="sxs-lookup"><span data-stu-id="934cf-424">**TimeOfLastConfigurationChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-425">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="934cf-425">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-426">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-427">Fecha y hora en que se modificó por última vez el archivo de configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="934cf-427">The date and time when the virtual machine configuration file was last modified.</span></span> <span data-ttu-id="934cf-428">El archivo de configuración se modifica durante ciertas operaciones de máquina virtual, así como cuando se agrega, modifica o quita cualquiera de las configuraciones de dispositivo o máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="934cf-428">The configuration file is modified during certain virtual machine operations, as well as when any of the virtual machine or device settings are added, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-429">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="934cf-429">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-430">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="934cf-430">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-431">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-432">Fecha y hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="934cf-432">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="934cf-433">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se admite.</span><span class="sxs-lookup"><span data-stu-id="934cf-433">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="934cf-434">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="934cf-434">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934cf-435">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="934cf-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="934cf-436">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="934cf-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934cf-437">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="934cf-437">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="934cf-438">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="934cf-438">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="934cf-439">Value</span><span class="sxs-lookup"><span data-stu-id="934cf-439">Value</span></span>                                                                                                                                                                                                                                                     | <span data-ttu-id="934cf-440">Significado</span><span class="sxs-lookup"><span data-stu-id="934cf-440">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="934cf-441"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-441"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="934cf-442"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-442"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="934cf-443"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-443"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <span data-ttu-id="934cf-444"><dt>**Apagar**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-444"><dt>**Shut Down**</dt> <dt>4</dt></span></span> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <span data-ttu-id="934cf-445"><dt>**Sin cambio**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-445"><dt>**No Change**</dt> <dt>5</dt></span></span> </dl>                       | <span data-ttu-id="934cf-446">No hay ninguna transición en curso.</span><span class="sxs-lookup"><span data-stu-id="934cf-446">No transition is in progress.</span></span><br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <span data-ttu-id="934cf-447"><dt>**Sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-447"><dt>**Offline**</dt> <dt>6</dt></span></span> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <span data-ttu-id="934cf-448"><dt>**Prueba**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-448"><dt>**Test**</dt> <dt>7</dt></span></span> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <span data-ttu-id="934cf-449"><dt>**Aplazar**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-449"><dt>**Defer**</dt> <dt>8</dt></span></span> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="934cf-450">Modo <dt>**inactivo**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-450"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <span data-ttu-id="934cf-451"><dt>**Reiniciar**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-451"><dt>**Reboot**</dt> <dt>10</dt></span></span> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <span data-ttu-id="934cf-452"><dt>**Restablecer**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-452"><dt>**Reset**</dt> <dt>11</dt></span></span> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="934cf-453"><dt>**No aplicable**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-453"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl>  | <span data-ttu-id="934cf-454">La implementación de no admite la representación de transiciones en curso.</span><span class="sxs-lookup"><span data-stu-id="934cf-454">The implementation does not support representing ongoing transitions.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="934cf-455"><dt> **DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-455"><dt>**DMTF Reserved** </dt> <dt>.. </dt></span></span> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="934cf-456">Requisitos</span><span class="sxs-lookup"><span data-stu-id="934cf-456">Requirements</span></span>



| <span data-ttu-id="934cf-457">Requisito</span><span class="sxs-lookup"><span data-stu-id="934cf-457">Requirement</span></span> | <span data-ttu-id="934cf-458">Value</span><span class="sxs-lookup"><span data-stu-id="934cf-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="934cf-459">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="934cf-459">Minimum supported client</span></span><br/> | <span data-ttu-id="934cf-460">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="934cf-460">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="934cf-461">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="934cf-461">Minimum supported server</span></span><br/> | <span data-ttu-id="934cf-462">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="934cf-462">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="934cf-463">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="934cf-463">Namespace</span></span><br/>                | <span data-ttu-id="934cf-464">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="934cf-464">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="934cf-465">MOF</span><span class="sxs-lookup"><span data-stu-id="934cf-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="934cf-466"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="934cf-467">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="934cf-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="934cf-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="934cf-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="934cf-469">Vea también</span><span class="sxs-lookup"><span data-stu-id="934cf-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="934cf-470">**ComputerSystem de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="934cf-470">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dt>

[<span data-ttu-id="934cf-471">**MSVM \_ VirtualSystemManagementService. Método ImportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="934cf-471">**Msvm\_VirtualSystemManagementService .ImportSystemDefinition method**</span></span>](importsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

