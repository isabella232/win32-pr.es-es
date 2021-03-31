---
description: Proporciona la administración activa de los grupos de recursos.
ms.assetid: 34ee3189-cb89-4d36-b12f-333449103968
title: Msvm_ResourcePoolConfigurationService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService
- Msvm_ResourcePoolConfigurationService.RequestStateChange
- Msvm_ResourcePoolConfigurationService.StartService
- Msvm_ResourcePoolConfigurationService.StopService
- Msvm_ResourcePoolConfigurationService.InstanceID
- Msvm_ResourcePoolConfigurationService.Caption
- Msvm_ResourcePoolConfigurationService.Description
- Msvm_ResourcePoolConfigurationService.ElementName
- Msvm_ResourcePoolConfigurationService.InstallDate
- Msvm_ResourcePoolConfigurationService.Name
- Msvm_ResourcePoolConfigurationService.OperationalStatus
- Msvm_ResourcePoolConfigurationService.StatusDescriptions
- Msvm_ResourcePoolConfigurationService.Status
- Msvm_ResourcePoolConfigurationService.HealthState
- Msvm_ResourcePoolConfigurationService.CommunicationStatus
- Msvm_ResourcePoolConfigurationService.DetailedStatus
- Msvm_ResourcePoolConfigurationService.OperatingStatus
- Msvm_ResourcePoolConfigurationService.PrimaryStatus
- Msvm_ResourcePoolConfigurationService.EnabledState
- Msvm_ResourcePoolConfigurationService.OtherEnabledState
- Msvm_ResourcePoolConfigurationService.RequestedState
- Msvm_ResourcePoolConfigurationService.EnabledDefault
- Msvm_ResourcePoolConfigurationService.TimeOfLastStateChange
- Msvm_ResourcePoolConfigurationService.AvailableRequestedStates
- Msvm_ResourcePoolConfigurationService.TransitioningToState
- Msvm_ResourcePoolConfigurationService.SystemCreationClassName
- Msvm_ResourcePoolConfigurationService.SystemName
- Msvm_ResourcePoolConfigurationService.CreationClassName
- Msvm_ResourcePoolConfigurationService.PrimaryOwnerName
- Msvm_ResourcePoolConfigurationService.PrimaryOwnerContact
- Msvm_ResourcePoolConfigurationService.StartMode
- Msvm_ResourcePoolConfigurationService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3160e8ac9ba011db70a5d7118e4d1f72733ff23f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913109"
---
# <a name="msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="a0a56-103">MSVM \_ ResourcePoolConfigurationService (clase)</span><span class="sxs-lookup"><span data-stu-id="a0a56-103">Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="a0a56-104">Proporciona la administración activa de los grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="a0a56-104">Provides for active management of resource pools.</span></span>

<span data-ttu-id="a0a56-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a0a56-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0a56-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0a56-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationService : CIM_Service
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
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="a0a56-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0a56-107">Members</span></span>

<span data-ttu-id="a0a56-108">La clase **MSVM \_ ResourcePoolConfigurationService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a0a56-108">The **Msvm\_ResourcePoolConfigurationService** class has these types of members:</span></span>

-   [<span data-ttu-id="a0a56-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0a56-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="a0a56-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0a56-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a0a56-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0a56-111">Methods</span></span>

<span data-ttu-id="a0a56-112">La clase **MSVM \_ ResourcePoolConfigurationService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a0a56-112">The **Msvm\_ResourcePoolConfigurationService** class has these methods.</span></span>



| <span data-ttu-id="a0a56-113">Método</span><span class="sxs-lookup"><span data-stu-id="a0a56-113">Method</span></span>                                                                                   | <span data-ttu-id="a0a56-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0a56-114">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0a56-115">**CreatePool**</span><span class="sxs-lookup"><span data-stu-id="a0a56-115">**CreatePool**</span></span>](createpool-msvm-resourcepoolconfigurationservice.md)                   | <span data-ttu-id="a0a56-116">Crea un grupo de recursos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a0a56-116">Creates a child resource pool.</span></span><br/>                                                    |
| [<span data-ttu-id="a0a56-117">**DeletePool**</span><span class="sxs-lookup"><span data-stu-id="a0a56-117">**DeletePool**</span></span>](deletepool-msvm-resourcepoolconfigurationservice.md)                   | <span data-ttu-id="a0a56-118">Elimina un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a0a56-118">Deletes a resource pool.</span></span><br/>                                                          |
| [<span data-ttu-id="a0a56-119">**ModifyPoolResources**</span><span class="sxs-lookup"><span data-stu-id="a0a56-119">**ModifyPoolResources**</span></span>](modifypoolresources-msvm-resourcepoolconfigurationservice.md) | <span data-ttu-id="a0a56-120">Cambia la configuración de recursos del grupo primario para los recursos asignados a un grupo secundario.</span><span class="sxs-lookup"><span data-stu-id="a0a56-120">Changes the parent pool resource settings for resources assigned to a child pool.</span></span><br/> |
| [<span data-ttu-id="a0a56-121">**ModifyPoolSettings**</span><span class="sxs-lookup"><span data-stu-id="a0a56-121">**ModifyPoolSettings**</span></span>](modifypoolsettings-msvm-resourcepoolconfigurationservice.md)   | <span data-ttu-id="a0a56-122">Cambia la configuración de un grupo secundario que no está relacionado con la asignación.</span><span class="sxs-lookup"><span data-stu-id="a0a56-122">Changes the settings of a child pool that are not allocation related.</span></span><br/>             |
| <span data-ttu-id="a0a56-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="a0a56-123">**RequestStateChange**</span></span>                                                                   | <span data-ttu-id="a0a56-124">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="a0a56-124">This method is not supported.</span></span><br/>                                                     |
| <span data-ttu-id="a0a56-125">**StartService**</span><span class="sxs-lookup"><span data-stu-id="a0a56-125">**StartService**</span></span>                                                                         | <span data-ttu-id="a0a56-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="a0a56-126">This method is not supported.</span></span><br/>                                                     |
| <span data-ttu-id="a0a56-127">**StopService**</span><span class="sxs-lookup"><span data-stu-id="a0a56-127">**StopService**</span></span>                                                                          | <span data-ttu-id="a0a56-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="a0a56-128">This method is not supported.</span></span><br/>                                                     |



 

### <a name="properties"></a><span data-ttu-id="a0a56-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0a56-129">Properties</span></span>

<span data-ttu-id="a0a56-130">La clase **MSVM \_ ResourcePoolConfigurationService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a0a56-130">The **Msvm\_ResourcePoolConfigurationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0a56-131">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="a0a56-131">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-132">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0a56-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-134">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="a0a56-134">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="a0a56-135">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="a0a56-135">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-136">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a0a56-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0a56-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-139">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a0a56-139">A short description of the object.</span></span> <span data-ttu-id="a0a56-140">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a0a56-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-141">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="a0a56-141">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-142">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0a56-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-144">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="a0a56-144">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a0a56-145">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a0a56-145">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a0a56-146">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0a56-146">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a0a56-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a0a56-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-148"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="a0a56-148"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-149"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="a0a56-149"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-150"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="a0a56-150"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-151"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="a0a56-151"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-152"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a0a56-152"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-153"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="a0a56-153"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a0a56-154">)</span><span class="sxs-lookup"><span data-stu-id="a0a56-154">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0a56-155">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a0a56-155">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0a56-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-158">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="a0a56-158">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-159">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="a0a56-159">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a0a56-160">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="a0a56-160">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a0a56-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0a56-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-164">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a0a56-164">A description of the object.</span></span> <span data-ttu-id="a0a56-165">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a0a56-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a0a56-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-167">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0a56-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-169">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="a0a56-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a0a56-170">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a0a56-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a0a56-171">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0a56-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a0a56-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="a0a56-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="a0a56-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="a0a56-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="a0a56-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="a0a56-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="a0a56-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a0a56-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="a0a56-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a0a56-180">)</span><span class="sxs-lookup"><span data-stu-id="a0a56-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0a56-181">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a0a56-181">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0a56-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-184">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="a0a56-184">A display name for the object.</span></span> <span data-ttu-id="a0a56-185">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a0a56-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-186">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="a0a56-186">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-187">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0a56-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-189">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a0a56-189">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="a0a56-190">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="a0a56-190">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="a0a56-191">Value</span><span class="sxs-lookup"><span data-stu-id="a0a56-191">Value</span></span>                                                                        | <span data-ttu-id="a0a56-192">Significado</span><span class="sxs-lookup"><span data-stu-id="a0a56-192">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="a0a56-193"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a0a56-193"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a0a56-194">habilitado</span><span class="sxs-lookup"><span data-stu-id="a0a56-194">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a0a56-195">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a0a56-195">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-196">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0a56-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-198">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a0a56-198">The enabled and disabled states of an element.</span></span> <span data-ttu-id="a0a56-199">Esta propiedad también puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="a0a56-199">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="a0a56-200">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="a0a56-200">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="a0a56-201">Value</span><span class="sxs-lookup"><span data-stu-id="a0a56-201">Value</span></span>                                                                        | <span data-ttu-id="a0a56-202">Significado</span><span class="sxs-lookup"><span data-stu-id="a0a56-202">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="a0a56-203"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a0a56-203"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a0a56-204">habilitado</span><span class="sxs-lookup"><span data-stu-id="a0a56-204">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a0a56-205">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a0a56-205">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-206">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0a56-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-208">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="a0a56-208">The current health of the element.</span></span> <span data-ttu-id="a0a56-209">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="a0a56-209">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="a0a56-210">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="a0a56-210">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="a0a56-211">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0a56-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-212">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a0a56-212">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-213">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a0a56-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-215">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a0a56-215">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="a0a56-216">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0a56-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-217">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a0a56-217">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-218">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0a56-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-220">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="a0a56-220">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-221">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="a0a56-221">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a0a56-222">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a0a56-222">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-223">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a0a56-223">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-224">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0a56-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-226">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="a0a56-226">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-227">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="a0a56-227">The label by which the object is known.</span></span> <span data-ttu-id="a0a56-228">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0a56-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-229">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="a0a56-229">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-230">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0a56-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-232">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="a0a56-232">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a0a56-233">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a0a56-233">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a0a56-234">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0a56-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a0a56-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a0a56-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="a0a56-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="a0a56-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="a0a56-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="a0a56-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="a0a56-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="a0a56-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="a0a56-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="a0a56-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="a0a56-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="a0a56-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="a0a56-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="a0a56-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="a0a56-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="a0a56-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="a0a56-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="a0a56-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a0a56-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="a0a56-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a0a56-254">)</span><span class="sxs-lookup"><span data-stu-id="a0a56-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0a56-255">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a0a56-255">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-256">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0a56-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-258">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="a0a56-258">The current statuses of the object.</span></span> <span data-ttu-id="a0a56-259">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0a56-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-260">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="a0a56-260">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0a56-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-263">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="a0a56-263">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="a0a56-264">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="a0a56-264">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="a0a56-265">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="a0a56-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-266">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="a0a56-266">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-267">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0a56-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-269">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="a0a56-269">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-270">Cualquier información sobre cómo se puede alcanzar el propietario principal del servicio (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.).</span><span class="sxs-lookup"><span data-stu-id="a0a56-270">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="a0a56-271">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="a0a56-271">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-272">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="a0a56-272">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-273">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0a56-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-275">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="a0a56-275">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-276">Nombre del propietario principal del servicio, si se ha definido uno.</span><span class="sxs-lookup"><span data-stu-id="a0a56-276">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="a0a56-277">El propietario principal es el contacto de soporte inicial para el servicio.</span><span class="sxs-lookup"><span data-stu-id="a0a56-277">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="a0a56-278">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="a0a56-278">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-279">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="a0a56-279">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-280">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0a56-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-282">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="a0a56-282">Provides high level status information.</span></span> <span data-ttu-id="a0a56-283">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="a0a56-283">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="a0a56-284">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a0a56-284">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a0a56-285">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0a56-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a0a56-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a0a56-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-287"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="a0a56-287"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-288"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="a0a56-288"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-289"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="a0a56-289"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-290"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a0a56-290"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-291"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="a0a56-291"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a0a56-292">)</span><span class="sxs-lookup"><span data-stu-id="a0a56-292">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0a56-293">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="a0a56-293">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-294">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0a56-294">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-296">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="a0a56-296">The last requested or desired state for the element.</span></span> <span data-ttu-id="a0a56-297">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="a0a56-297">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="a0a56-298">Esta propiedad se proporciona para comparar el último estado solicitado y el actual para un elemento.</span><span class="sxs-lookup"><span data-stu-id="a0a56-298">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="a0a56-299">Una instancia concreta de la [**clase \_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir la propiedad **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="a0a56-299">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="a0a56-300">Si esto ocurre, se usa el valor 12 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="a0a56-300">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="a0a56-301">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM** y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="a0a56-301">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="a0a56-302">Value</span><span class="sxs-lookup"><span data-stu-id="a0a56-302">Value</span></span>                                                                         | <span data-ttu-id="a0a56-303">Significado</span><span class="sxs-lookup"><span data-stu-id="a0a56-303">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="a0a56-304"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a0a56-304"><dt>12</dt></span></span> </dl> | <span data-ttu-id="a0a56-305">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="a0a56-305">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a0a56-306">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="a0a56-306">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-307">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a0a56-307">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-309">Indica si el servicio se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="a0a56-309">Indicates whether the service is currently running.</span></span> <span data-ttu-id="a0a56-310">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="a0a56-310">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-311">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="a0a56-311">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-312">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0a56-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-314">Calificadores: **MaxLen** (10)</span><span class="sxs-lookup"><span data-stu-id="a0a56-314">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-315">Un valor de cadena que indica si el servicio se inicia automáticamente por un sistema, un sistema operativo o se inicia solo después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a0a56-315">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="a0a56-316">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="a0a56-316">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-317">**Estado**</span><span class="sxs-lookup"><span data-stu-id="a0a56-317">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-318">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0a56-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-320">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="a0a56-320">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-321">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a0a56-321">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-322">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="a0a56-322">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-324">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="a0a56-324">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a0a56-325">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a0a56-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-326">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a0a56-326">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-327">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0a56-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-329">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="a0a56-329">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-330">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a0a56-330">The scoping system's creation class name.</span></span> <span data-ttu-id="a0a56-331">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="a0a56-331">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-332">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a0a56-332">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-333">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0a56-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-335">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="a0a56-335">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-336">Nombre NetBIOS del sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="a0a56-336">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="a0a56-337">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="a0a56-337">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-338">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="a0a56-338">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-339">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a0a56-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-341">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="a0a56-341">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="a0a56-342">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0a56-342">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-343">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="a0a56-343">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a56-344">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0a56-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0a56-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0a56-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a56-346">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="a0a56-346">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="a0a56-347">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="a0a56-347">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0a56-348">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0a56-348">Requirements</span></span>



| <span data-ttu-id="a0a56-349">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0a56-349">Requirement</span></span> | <span data-ttu-id="a0a56-350">Value</span><span class="sxs-lookup"><span data-stu-id="a0a56-350">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a56-351">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0a56-351">Minimum supported client</span></span><br/> | <span data-ttu-id="a0a56-352">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="a0a56-352">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a0a56-353">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0a56-353">Minimum supported server</span></span><br/> | <span data-ttu-id="a0a56-354">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a0a56-354">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a0a56-355">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a0a56-355">Namespace</span></span><br/>                | <span data-ttu-id="a0a56-356">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a0a56-356">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a0a56-357">MOF</span><span class="sxs-lookup"><span data-stu-id="a0a56-357">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0a56-358"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0a56-358"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0a56-359">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a0a56-359">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0a56-360"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a0a56-360"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

