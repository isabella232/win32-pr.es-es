---
description: Representa el servicio de virtualización presente en un sistema host único. MSVM \_ VirtualEthernetSwitchManagementService se utiliza para controlar la definición, la modificación y la eliminación de conmutadores Ethernet virtuales.
ms.assetid: d29935d3-3a88-4186-97e9-b27c0c0d07d0
title: Msvm_VirtualEthernetSwitchManagementService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService
- Msvm_VirtualEthernetSwitchManagementService.InstanceID
- Msvm_VirtualEthernetSwitchManagementService.Caption
- Msvm_VirtualEthernetSwitchManagementService.Description
- Msvm_VirtualEthernetSwitchManagementService.ElementName
- Msvm_VirtualEthernetSwitchManagementService.InstallDate
- Msvm_VirtualEthernetSwitchManagementService.Name
- Msvm_VirtualEthernetSwitchManagementService.OperationalStatus
- Msvm_VirtualEthernetSwitchManagementService.StatusDescriptions
- Msvm_VirtualEthernetSwitchManagementService.Status
- Msvm_VirtualEthernetSwitchManagementService.HealthState
- Msvm_VirtualEthernetSwitchManagementService.CommunicationStatus
- Msvm_VirtualEthernetSwitchManagementService.DetailedStatus
- Msvm_VirtualEthernetSwitchManagementService.OperatingStatus
- Msvm_VirtualEthernetSwitchManagementService.PrimaryStatus
- Msvm_VirtualEthernetSwitchManagementService.EnabledState
- Msvm_VirtualEthernetSwitchManagementService.OtherEnabledState
- Msvm_VirtualEthernetSwitchManagementService.RequestedState
- Msvm_VirtualEthernetSwitchManagementService.EnabledDefault
- Msvm_VirtualEthernetSwitchManagementService.TimeOfLastStateChange
- Msvm_VirtualEthernetSwitchManagementService.AvailableRequestedStates
- Msvm_VirtualEthernetSwitchManagementService.TransitioningToState
- Msvm_VirtualEthernetSwitchManagementService.SystemCreationClassName
- Msvm_VirtualEthernetSwitchManagementService.SystemName
- Msvm_VirtualEthernetSwitchManagementService.CreationClassName
- Msvm_VirtualEthernetSwitchManagementService.PrimaryOwnerName
- Msvm_VirtualEthernetSwitchManagementService.PrimaryOwnerContact
- Msvm_VirtualEthernetSwitchManagementService.StartMode
- Msvm_VirtualEthernetSwitchManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e6c1d4dee775dc6fabbb5fb3c96c987d1f6bda5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689573"
---
# <a name="msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="4269a-104">MSVM \_ VirtualEthernetSwitchManagementService (clase)</span><span class="sxs-lookup"><span data-stu-id="4269a-104">Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="4269a-105">Representa el servicio de virtualización presente en un sistema host único.</span><span class="sxs-lookup"><span data-stu-id="4269a-105">Represents the virtualization service present on a single host system.</span></span> <span data-ttu-id="4269a-106">MSVM \_ VirtualEthernetSwitchManagementService se utiliza para controlar la definición, la modificación y la eliminación de conmutadores Ethernet virtuales.</span><span class="sxs-lookup"><span data-stu-id="4269a-106">Msvm\_VirtualEthernetSwitchManagementService is used to control the definition, modification, and deletion of virtual Ethernet switches.</span></span>

<span data-ttu-id="4269a-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4269a-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4269a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4269a-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual Networking Management Service";
  string   Description = "Provides Hyper-V Networking WMI management";
  string   ElementName = "Hyper-V Networking Management Service";
  datetime InstallDate;
  string   Name = "nvspwmi";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status = { "OK" };
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
  string   CreationClassName = "Msvm_VirtualEthernetSwitchManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="4269a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4269a-109">Members</span></span>

<span data-ttu-id="4269a-110">La clase **MSVM \_ VirtualEthernetSwitchManagementService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4269a-110">The **Msvm\_VirtualEthernetSwitchManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="4269a-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4269a-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4269a-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4269a-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4269a-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4269a-113">Methods</span></span>

<span data-ttu-id="4269a-114">La clase **MSVM \_ VirtualEthernetSwitchManagementService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4269a-114">The **Msvm\_VirtualEthernetSwitchManagementService** class has these methods.</span></span>



| <span data-ttu-id="4269a-115">Método</span><span class="sxs-lookup"><span data-stu-id="4269a-115">Method</span></span>                                                                                               | <span data-ttu-id="4269a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4269a-116">Description</span></span>                                                                       |
|:-----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="4269a-117">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="4269a-117">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)         | <span data-ttu-id="4269a-118">Agrega configuraciones de características a la configuración de un puerto de conmutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="4269a-118">Adds feature settings to the configuration of an Ethernet switch port.</span></span><br/> |
| [<span data-ttu-id="4269a-119">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="4269a-119">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)       | <span data-ttu-id="4269a-120">Agrega recursos a una configuración de conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="4269a-120">Adds resources to a virtual switch configuration.</span></span><br/>                      |
| [<span data-ttu-id="4269a-121">**DefineSystem**</span><span class="sxs-lookup"><span data-stu-id="4269a-121">**DefineSystem**</span></span>](definesystem-msvm-virtualethernetswitchmanagementservice.md)                     | <span data-ttu-id="4269a-122">Crea un nuevo conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="4269a-122">Creates a new virtual switch.</span></span><br/>                                          |
| [<span data-ttu-id="4269a-123">**DestroySystem**</span><span class="sxs-lookup"><span data-stu-id="4269a-123">**DestroySystem**</span></span>](destroysystem-msvm-virtualethernetswitchmanagementservice.md)                   | <span data-ttu-id="4269a-124">Destruye un conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="4269a-124">Destroys a virtual switch.</span></span><br/>                                             |
| [<span data-ttu-id="4269a-125">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="4269a-125">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)   | <span data-ttu-id="4269a-126">Modifica la configuración de características de un puerto de conmutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="4269a-126">Modifies the feature settings of an Ethernet switch port.</span></span><br/>              |
| [<span data-ttu-id="4269a-127">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="4269a-127">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md) | <span data-ttu-id="4269a-128">Modifica la configuración de recursos de un conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="4269a-128">Modifies resource settings for a virtual switch.</span></span><br/>                       |
| [<span data-ttu-id="4269a-129">**ModifySystemSettings**</span><span class="sxs-lookup"><span data-stu-id="4269a-129">**ModifySystemSettings**</span></span>](modifysystemsettings-msvm-virtualethernetswitchmanagementservice.md)     | <span data-ttu-id="4269a-130">Modifica la configuración del conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="4269a-130">Modifies virtual switch settings.</span></span><br/>                                      |
| [<span data-ttu-id="4269a-131">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="4269a-131">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)   | <span data-ttu-id="4269a-132">Quita la configuración de características de un puerto de conmutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="4269a-132">Removes feature settings from an Ethernet switch port.</span></span><br/>                 |
| [<span data-ttu-id="4269a-133">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="4269a-133">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md) | <span data-ttu-id="4269a-134">Quita la configuración de recursos virtuales de una configuración de conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="4269a-134">Removes virtual resource settings from a virtual switch configuration.</span></span><br/> |
| [<span data-ttu-id="4269a-135">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="4269a-135">**RequestStateChange**</span></span>](msvm-virtualethernetswitchmanagementservice-requeststatechange.md)         | <span data-ttu-id="4269a-136">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="4269a-136">Requests a state change.</span></span><br/>                                               |
| [<span data-ttu-id="4269a-137">**StartService**</span><span class="sxs-lookup"><span data-stu-id="4269a-137">**StartService**</span></span>](msvm-virtualethernetswitchmanagementservice-startservice.md)                     | <span data-ttu-id="4269a-138">inicia el servicio.</span><span class="sxs-lookup"><span data-stu-id="4269a-138">Starts the service.</span></span><br/>                                                    |
| [<span data-ttu-id="4269a-139">**StopService**</span><span class="sxs-lookup"><span data-stu-id="4269a-139">**StopService**</span></span>](msvm-virtualethernetswitchmanagementservice-stopservice.md)                       | <span data-ttu-id="4269a-140">detiene el servicio.</span><span class="sxs-lookup"><span data-stu-id="4269a-140">Stops the service.</span></span><br/>                                                     |



 

### <a name="properties"></a><span data-ttu-id="4269a-141">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4269a-141">Properties</span></span>

<span data-ttu-id="4269a-142">La clase **MSVM \_ VirtualEthernetSwitchManagementService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4269a-142">The **Msvm\_VirtualEthernetSwitchManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4269a-143">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="4269a-143">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-144">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4269a-144">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4269a-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-146">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="4269a-146">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="4269a-147">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="4269a-147">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4269a-148">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4269a-148">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4269a-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-151">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="4269a-151">A short description of the object.</span></span> <span data-ttu-id="4269a-152">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "servicio de administración de redes virtuales de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="4269a-152">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Networking Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="4269a-153">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="4269a-153">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-154">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4269a-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-156">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="4269a-156">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="4269a-157">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="4269a-157">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4269a-158">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4269a-158">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4269a-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="4269a-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-160"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="4269a-160"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-161"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="4269a-161"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-162"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="4269a-162"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-163"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="4269a-163"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="4269a-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-165"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="4269a-165"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4269a-166">)</span><span class="sxs-lookup"><span data-stu-id="4269a-166">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4269a-167">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4269a-167">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4269a-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4269a-170">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="4269a-170">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="4269a-171">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="4269a-171">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4269a-172">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ VirtualEthernetSwitchManagementService".</span><span class="sxs-lookup"><span data-stu-id="4269a-172">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualEthernetSwitchManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="4269a-173">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4269a-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4269a-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-176">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="4269a-176">A description of the object.</span></span> <span data-ttu-id="4269a-177">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "proporciona administración WMI de redes de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="4269a-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Hyper-V Networking WMI management".</span></span>

</dd> <dt>

<span data-ttu-id="4269a-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="4269a-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-179">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4269a-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-181">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="4269a-181">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="4269a-182">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="4269a-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4269a-183">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4269a-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4269a-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="4269a-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="4269a-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="4269a-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="4269a-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="4269a-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="4269a-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="4269a-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="4269a-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4269a-192">)</span><span class="sxs-lookup"><span data-stu-id="4269a-192">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4269a-193">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4269a-193">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4269a-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-196">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="4269a-196">A display name for the object.</span></span> <span data-ttu-id="4269a-197">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de administración de redes de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="4269a-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Networking Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="4269a-198">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="4269a-198">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-199">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4269a-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-201">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="4269a-201">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="4269a-202">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="4269a-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="4269a-203">Value</span><span class="sxs-lookup"><span data-stu-id="4269a-203">Value</span></span>                                                                        | <span data-ttu-id="4269a-204">Significado</span><span class="sxs-lookup"><span data-stu-id="4269a-204">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="4269a-205"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4269a-205"><dt>2</dt></span></span> </dl> | <span data-ttu-id="4269a-206">habilitado</span><span class="sxs-lookup"><span data-stu-id="4269a-206">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4269a-207">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="4269a-207">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-208">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4269a-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-210">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="4269a-210">The enabled and disabled states of an element.</span></span> <span data-ttu-id="4269a-211">Esta propiedad también puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="4269a-211">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="4269a-212">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="4269a-212">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not applicable).</span></span>

</dd> <dt>

<span data-ttu-id="4269a-213">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="4269a-213">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-214">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4269a-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-216">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="4269a-216">The current health of the element.</span></span> <span data-ttu-id="4269a-217">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="4269a-217">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="4269a-218">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="4269a-218">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="4269a-219">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="4269a-219">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="4269a-220">Value</span><span class="sxs-lookup"><span data-stu-id="4269a-220">Value</span></span>                                                                        | <span data-ttu-id="4269a-221">Significado</span><span class="sxs-lookup"><span data-stu-id="4269a-221">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="4269a-222"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4269a-222"><dt>5</dt></span></span> </dl> | <span data-ttu-id="4269a-223">El estado de mantenimiento es normal.</span><span class="sxs-lookup"><span data-stu-id="4269a-223">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4269a-224">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4269a-224">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-225">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4269a-225">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-227">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4269a-227">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="4269a-228">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4269a-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4269a-229">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4269a-229">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4269a-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4269a-232">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="4269a-232">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4269a-233">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="4269a-233">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4269a-234">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4269a-234">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4269a-235">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="4269a-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-236">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4269a-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4269a-238">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="4269a-238">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="4269a-239">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="4269a-239">The label by which the object is known.</span></span> <span data-ttu-id="4269a-240">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre se establece en "vMMS".</span><span class="sxs-lookup"><span data-stu-id="4269a-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vmms".</span></span>

</dd> <dt>

<span data-ttu-id="4269a-241">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="4269a-241">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-242">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4269a-242">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-244">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="4269a-244">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="4269a-245">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="4269a-245">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4269a-246">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4269a-246">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4269a-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="4269a-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-248"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="4269a-248"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-249"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="4269a-249"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-250"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="4269a-250"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-251"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="4269a-251"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-252"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="4269a-252"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="4269a-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-254"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="4269a-254"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-255"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="4269a-255"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-256"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="4269a-256"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-257"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="4269a-257"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-258"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="4269a-258"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-259"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="4269a-259"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-260"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="4269a-260"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-261"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="4269a-261"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-262"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="4269a-262"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-263"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="4269a-263"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="4269a-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="4269a-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4269a-266">)</span><span class="sxs-lookup"><span data-stu-id="4269a-266">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4269a-267">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="4269a-267">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-268">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4269a-268">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4269a-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-270">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="4269a-270">The current statuses of the object.</span></span> <span data-ttu-id="4269a-271">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="4269a-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="4269a-272">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="4269a-272">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-273">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4269a-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-275">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="4269a-275">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="4269a-276">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="4269a-276">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="4269a-277">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="4269a-277">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4269a-278">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="4269a-278">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-279">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4269a-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4269a-281">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="4269a-281">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="4269a-282">Cualquier información sobre cómo se puede alcanzar el propietario principal del servicio (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.).</span><span class="sxs-lookup"><span data-stu-id="4269a-282">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="4269a-283">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="4269a-283">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4269a-284">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="4269a-284">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-285">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4269a-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4269a-287">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="4269a-287">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="4269a-288">Nombre del propietario principal del servicio, si se ha definido uno.</span><span class="sxs-lookup"><span data-stu-id="4269a-288">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="4269a-289">El propietario principal es el contacto de soporte inicial para el servicio.</span><span class="sxs-lookup"><span data-stu-id="4269a-289">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="4269a-290">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="4269a-290">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4269a-291">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="4269a-291">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-292">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4269a-292">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-294">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="4269a-294">Provides high level status information.</span></span> <span data-ttu-id="4269a-295">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="4269a-295">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="4269a-296">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="4269a-296">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4269a-297">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4269a-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4269a-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="4269a-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-299"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="4269a-299"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-300"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="4269a-300"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-301"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="4269a-301"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-302"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="4269a-302"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4269a-303"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="4269a-303"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4269a-304">)</span><span class="sxs-lookup"><span data-stu-id="4269a-304">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4269a-305">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="4269a-305">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-306">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4269a-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-308">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="4269a-308">The last requested or desired state for the element.</span></span> <span data-ttu-id="4269a-309">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="4269a-309">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="4269a-310">Esta propiedad se proporciona para comparar el último estado solicitado y el actual para un elemento.</span><span class="sxs-lookup"><span data-stu-id="4269a-310">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="4269a-311">Una instancia concreta de la [**clase \_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir la propiedad **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="4269a-311">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="4269a-312">Si esto ocurre, se usa el valor 12 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="4269a-312">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="4269a-313">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM** y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="4269a-313">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="4269a-314">Value</span><span class="sxs-lookup"><span data-stu-id="4269a-314">Value</span></span>                                                                         | <span data-ttu-id="4269a-315">Significado</span><span class="sxs-lookup"><span data-stu-id="4269a-315">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="4269a-316"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="4269a-316"><dt>12</dt></span></span> </dl> | <span data-ttu-id="4269a-317">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="4269a-317">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4269a-318">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="4269a-318">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-319">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4269a-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-321">Indica si el servicio se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="4269a-321">Indicates whether the service is currently running.</span></span> <span data-ttu-id="4269a-322">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="4269a-322">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="4269a-323">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="4269a-323">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4269a-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4269a-326">Calificadores: **MaxLen** (10)</span><span class="sxs-lookup"><span data-stu-id="4269a-326">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="4269a-327">Un valor de cadena que indica si el servicio se inicia automáticamente por un sistema, un sistema operativo o se inicia solo después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4269a-327">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="4269a-328">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="4269a-328">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4269a-329">**Estado**</span><span class="sxs-lookup"><span data-stu-id="4269a-329">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-330">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4269a-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-332">Describe el estado actual del servicio.</span><span class="sxs-lookup"><span data-stu-id="4269a-332">Describes the current status of the service.</span></span> <span data-ttu-id="4269a-333">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en "OK".</span><span class="sxs-lookup"><span data-stu-id="4269a-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="4269a-334">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4269a-334">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-335">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="4269a-335">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4269a-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-337">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="4269a-337">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="4269a-338">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "OK".</span><span class="sxs-lookup"><span data-stu-id="4269a-338">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="4269a-339">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4269a-339">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4269a-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4269a-342">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="4269a-342">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="4269a-343">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="4269a-343">The scoping system's creation class name.</span></span> <span data-ttu-id="4269a-344">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="4269a-344">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="4269a-345">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4269a-345">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-346">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4269a-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4269a-348">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="4269a-348">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="4269a-349">Nombre NetBIOS del sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="4269a-349">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="4269a-350">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="4269a-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="4269a-351">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="4269a-351">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-352">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4269a-352">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-354">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="4269a-354">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="4269a-355">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4269a-355">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4269a-356">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="4269a-356">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4269a-357">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4269a-357">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4269a-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4269a-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4269a-359">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="4269a-359">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="4269a-360">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="4269a-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4269a-361">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4269a-361">Requirements</span></span>



| <span data-ttu-id="4269a-362">Requisito</span><span class="sxs-lookup"><span data-stu-id="4269a-362">Requirement</span></span> | <span data-ttu-id="4269a-363">Value</span><span class="sxs-lookup"><span data-stu-id="4269a-363">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4269a-364">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4269a-364">Minimum supported client</span></span><br/> | <span data-ttu-id="4269a-365">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4269a-365">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4269a-366">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4269a-366">Minimum supported server</span></span><br/> | <span data-ttu-id="4269a-367">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4269a-367">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4269a-368">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4269a-368">Namespace</span></span><br/>                | <span data-ttu-id="4269a-369">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4269a-369">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4269a-370">MOF</span><span class="sxs-lookup"><span data-stu-id="4269a-370">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4269a-371"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4269a-371"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4269a-372">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4269a-372">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4269a-373"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4269a-373"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

