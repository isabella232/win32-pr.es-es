---
description: Describe el servicio de GPU 3D sintético.
ms.assetid: fe3d6105-3def-453a-ad81-97cd0bb4613f
title: Msvm_Synthetic3DService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService
- Msvm_Synthetic3DService.RequestStateChange
- Msvm_Synthetic3DService.StartService
- Msvm_Synthetic3DService.StopService
- Msvm_Synthetic3DService.InstanceID
- Msvm_Synthetic3DService.Caption
- Msvm_Synthetic3DService.Description
- Msvm_Synthetic3DService.ElementName
- Msvm_Synthetic3DService.InstallDate
- Msvm_Synthetic3DService.OperationalStatus
- Msvm_Synthetic3DService.StatusDescriptions
- Msvm_Synthetic3DService.Status
- Msvm_Synthetic3DService.HealthState
- Msvm_Synthetic3DService.CommunicationStatus
- Msvm_Synthetic3DService.DetailedStatus
- Msvm_Synthetic3DService.OperatingStatus
- Msvm_Synthetic3DService.PrimaryStatus
- Msvm_Synthetic3DService.EnabledState
- Msvm_Synthetic3DService.OtherEnabledState
- Msvm_Synthetic3DService.RequestedState
- Msvm_Synthetic3DService.EnabledDefault
- Msvm_Synthetic3DService.TimeOfLastStateChange
- Msvm_Synthetic3DService.AvailableRequestedStates
- Msvm_Synthetic3DService.TransitioningToState
- Msvm_Synthetic3DService.SystemCreationClassName
- Msvm_Synthetic3DService.SystemName
- Msvm_Synthetic3DService.Name
- Msvm_Synthetic3DService.CreationClassName
- Msvm_Synthetic3DService.PrimaryOwnerName
- Msvm_Synthetic3DService.PrimaryOwnerContact
- Msvm_Synthetic3DService.StartMode
- Msvm_Synthetic3DService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e5bdacb764051f4bee2c9a646a00b09615ee5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687138"
---
# <a name="msvm_synthetic3dservice-class"></a><span data-ttu-id="428a5-103">MSVM \_ Synthetic3DService (clase)</span><span class="sxs-lookup"><span data-stu-id="428a5-103">Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="428a5-104">Describe el servicio de GPU 3D sintético.</span><span class="sxs-lookup"><span data-stu-id="428a5-104">Describes the synthetic 3-D GPU service.</span></span>

> [!Note]  
> <span data-ttu-id="428a5-105">Esta clase no está disponible para las máquinas virtuales de generación 2.</span><span class="sxs-lookup"><span data-stu-id="428a5-105">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="428a5-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="428a5-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="428a5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="428a5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Synthetic3D Service";
  string   Description = "Microsoft Synthetic3D Service";
  string   ElementName = "Synthetic3D Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The Synthetic 3D service is fully operational." };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "synth3d";
  string   CreationClassName = "Msvm_Synthetic3DService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="428a5-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="428a5-108">Members</span></span>

<span data-ttu-id="428a5-109">La clase **MSVM \_ Synthetic3DService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="428a5-109">The **Msvm\_Synthetic3DService** class has these types of members:</span></span>

-   [<span data-ttu-id="428a5-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="428a5-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="428a5-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="428a5-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="428a5-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="428a5-112">Methods</span></span>

<span data-ttu-id="428a5-113">La clase **MSVM \_ Synthetic3DService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="428a5-113">The **Msvm\_Synthetic3DService** class has these methods.</span></span>



| <span data-ttu-id="428a5-114">Método</span><span class="sxs-lookup"><span data-stu-id="428a5-114">Method</span></span>                                                                                     | <span data-ttu-id="428a5-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="428a5-115">Description</span></span>                                                         |
|:-------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="428a5-116">**DisableGPUForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="428a5-116">**DisableGPUForVirtualization**</span></span>](disablegpuforvirtualization-msvm-synthetic3dservice.md) | <span data-ttu-id="428a5-117">Deshabilita una GPU física para la virtualización.</span><span class="sxs-lookup"><span data-stu-id="428a5-117">Disables a physical GPU for virtualization.</span></span><br/>              |
| [<span data-ttu-id="428a5-118">**EnableGPUForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="428a5-118">**EnableGPUForVirtualization**</span></span>](enablegpuforvirtualization-msvm-synthetic3dservice.md)   | <span data-ttu-id="428a5-119">Habilita una GPU física para la virtualización.</span><span class="sxs-lookup"><span data-stu-id="428a5-119">Enables a physical GPU for virtualization.</span></span><br/>               |
| [<span data-ttu-id="428a5-120">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="428a5-120">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-synthetic3dservice.md)             | <span data-ttu-id="428a5-121">Modifica los datos de configuración para el servicio 3D sintético.</span><span class="sxs-lookup"><span data-stu-id="428a5-121">Modifies the setting data for the synthetic 3-D service.</span></span><br/> |
| <span data-ttu-id="428a5-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="428a5-122">**RequestStateChange**</span></span>                                                                     | <span data-ttu-id="428a5-123">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="428a5-123">This method is not supported.</span></span><br/>                            |
| <span data-ttu-id="428a5-124">**StartService**</span><span class="sxs-lookup"><span data-stu-id="428a5-124">**StartService**</span></span>                                                                           | <span data-ttu-id="428a5-125">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="428a5-125">This method is not supported.</span></span><br/>                            |
| <span data-ttu-id="428a5-126">**StopService**</span><span class="sxs-lookup"><span data-stu-id="428a5-126">**StopService**</span></span>                                                                            | <span data-ttu-id="428a5-127">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="428a5-127">This method is not supported.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="428a5-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="428a5-128">Properties</span></span>

<span data-ttu-id="428a5-129">La clase **MSVM \_ Synthetic3DService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="428a5-129">The **Msvm\_Synthetic3DService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="428a5-130">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="428a5-130">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-131">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="428a5-131">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="428a5-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-133">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="428a5-133">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="428a5-134">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="428a5-134">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-135">**Caption**</span><span class="sxs-lookup"><span data-stu-id="428a5-135">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="428a5-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-138">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="428a5-138">A short description of the object.</span></span> <span data-ttu-id="428a5-139">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="428a5-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-140">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="428a5-140">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-141">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="428a5-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-143">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="428a5-143">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="428a5-144">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="428a5-144">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="428a5-145">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="428a5-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="428a5-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="428a5-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-147"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="428a5-147"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-148"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="428a5-148"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-149"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="428a5-149"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-150"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="428a5-150"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-151"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="428a5-151"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-152"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="428a5-152"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="428a5-153">)</span><span class="sxs-lookup"><span data-stu-id="428a5-153">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="428a5-154">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="428a5-154">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="428a5-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-157">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="428a5-157">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="428a5-158">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="428a5-158">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-159">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="428a5-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="428a5-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-162">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="428a5-162">A description of the object.</span></span> <span data-ttu-id="428a5-163">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="428a5-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-164">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="428a5-164">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-165">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="428a5-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-167">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="428a5-167">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="428a5-168">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="428a5-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="428a5-169">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="428a5-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="428a5-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="428a5-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="428a5-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="428a5-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="428a5-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="428a5-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="428a5-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="428a5-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="428a5-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="428a5-178">)</span><span class="sxs-lookup"><span data-stu-id="428a5-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="428a5-179">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="428a5-179">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="428a5-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-182">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="428a5-182">A display name for the object.</span></span> <span data-ttu-id="428a5-183">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="428a5-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-184">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="428a5-184">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-185">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="428a5-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-187">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="428a5-187">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="428a5-188">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="428a5-188">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-189">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="428a5-189">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="428a5-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-192">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="428a5-192">The enabled and disabled states of an element.</span></span> <span data-ttu-id="428a5-193">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="428a5-193">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="428a5-194">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="428a5-194">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-195">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="428a5-195">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-196">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="428a5-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-198">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="428a5-198">The current health of the element.</span></span> <span data-ttu-id="428a5-199">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="428a5-199">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="428a5-200">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="428a5-200">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="428a5-201">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="428a5-201">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-202">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="428a5-202">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-203">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="428a5-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-205">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="428a5-205">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="428a5-206">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="428a5-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-207">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="428a5-207">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="428a5-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="428a5-210">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="428a5-210">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="428a5-211">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="428a5-211">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="428a5-212">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="428a5-212">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="428a5-213">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="428a5-213">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-214">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="428a5-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-216">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="428a5-216">The label by which the object is known.</span></span> <span data-ttu-id="428a5-217">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="428a5-217">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-218">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="428a5-218">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-219">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="428a5-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-221">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="428a5-221">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="428a5-222">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="428a5-222">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="428a5-223">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="428a5-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="428a5-224"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="428a5-224"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-225"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="428a5-225"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-226"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="428a5-226"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-227"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="428a5-227"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-228"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="428a5-228"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-229"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="428a5-229"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-230"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="428a5-230"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-231"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="428a5-231"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-232"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="428a5-232"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-233"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="428a5-233"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-234"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="428a5-234"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-235"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="428a5-235"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-236"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="428a5-236"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-237"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="428a5-237"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-238"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="428a5-238"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-239"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="428a5-239"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-240"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="428a5-240"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-241"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="428a5-241"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-242"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="428a5-242"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="428a5-243">)</span><span class="sxs-lookup"><span data-stu-id="428a5-243">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="428a5-244">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="428a5-244">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-245">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="428a5-245">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="428a5-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-247">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="428a5-247">The current statuses of the object.</span></span> <span data-ttu-id="428a5-248">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="428a5-248">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-249">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="428a5-249">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-250">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="428a5-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-252">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="428a5-252">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="428a5-253">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="428a5-253">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="428a5-254">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="428a5-254">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-255">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="428a5-255">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-256">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="428a5-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-258">Valor que proporciona información sobre cómo se puede alcanzar el propietario principal del servicio (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.).</span><span class="sxs-lookup"><span data-stu-id="428a5-258">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="428a5-259">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="428a5-259">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-260">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="428a5-260">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="428a5-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-263">Nombre del propietario principal del servicio, si se ha definido uno.</span><span class="sxs-lookup"><span data-stu-id="428a5-263">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="428a5-264">El propietario principal es el contacto de soporte inicial para el servicio.</span><span class="sxs-lookup"><span data-stu-id="428a5-264">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="428a5-265">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="428a5-265">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-266">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="428a5-266">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-267">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="428a5-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-269">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="428a5-269">Provides high level status information.</span></span> <span data-ttu-id="428a5-270">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="428a5-270">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="428a5-271">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="428a5-271">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="428a5-272">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="428a5-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="428a5-273"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="428a5-273"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-274"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="428a5-274"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-275"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="428a5-275"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-276"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="428a5-276"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-277"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="428a5-277"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="428a5-278"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="428a5-278"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="428a5-279">)</span><span class="sxs-lookup"><span data-stu-id="428a5-279">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="428a5-280">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="428a5-280">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-281">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="428a5-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-283">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="428a5-283">The last requested or desired state for the element.</span></span> <span data-ttu-id="428a5-284">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="428a5-284">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="428a5-285">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="428a5-285">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="428a5-286">Una instancia concreta de la [**clase \_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir el método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="428a5-286">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="428a5-287">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="428a5-287">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="428a5-288">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="428a5-288">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="428a5-289">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="428a5-289">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-290">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="428a5-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-292">Indica si el servicio se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="428a5-292">Indicates whether the service is currently running.</span></span> <span data-ttu-id="428a5-293">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="428a5-293">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-294">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="428a5-294">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-295">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="428a5-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-297">Un valor de cadena que indica si el servicio se inicia automáticamente por un sistema, un sistema operativo o se inicia solo después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="428a5-297">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="428a5-298">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="428a5-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-299">**Estado**</span><span class="sxs-lookup"><span data-stu-id="428a5-299">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="428a5-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-302">Estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="428a5-302">The status of the element.</span></span> <span data-ttu-id="428a5-303">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="428a5-303">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-304">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="428a5-304">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-305">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="428a5-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="428a5-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-307">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="428a5-307">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="428a5-308">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="428a5-308">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-309">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="428a5-309">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-310">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="428a5-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-312">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="428a5-312">The scoping system's creation class name.</span></span> <span data-ttu-id="428a5-313">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="428a5-313">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-314">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="428a5-314">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-315">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="428a5-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-317">Nombre del sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="428a5-317">The name of the hosting computer system.</span></span> <span data-ttu-id="428a5-318">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="428a5-318">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-319">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="428a5-319">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-320">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="428a5-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-322">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="428a5-322">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="428a5-323">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="428a5-323">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="428a5-324">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="428a5-324">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="428a5-325">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="428a5-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="428a5-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="428a5-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="428a5-327">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="428a5-327">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="428a5-328">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="428a5-328">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="428a5-329">Requisitos</span><span class="sxs-lookup"><span data-stu-id="428a5-329">Requirements</span></span>



| <span data-ttu-id="428a5-330">Requisito</span><span class="sxs-lookup"><span data-stu-id="428a5-330">Requirement</span></span> | <span data-ttu-id="428a5-331">Value</span><span class="sxs-lookup"><span data-stu-id="428a5-331">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="428a5-332">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="428a5-332">Minimum supported client</span></span><br/> | <span data-ttu-id="428a5-333">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="428a5-333">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="428a5-334">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="428a5-334">Minimum supported server</span></span><br/> | <span data-ttu-id="428a5-335">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="428a5-335">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="428a5-336">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="428a5-336">Namespace</span></span><br/>                | <span data-ttu-id="428a5-337">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="428a5-337">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="428a5-338">MOF</span><span class="sxs-lookup"><span data-stu-id="428a5-338">MOF</span></span><br/>                      | <dl> <span data-ttu-id="428a5-339"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="428a5-339"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="428a5-340">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="428a5-340">DLL</span></span><br/>                      | <dl> <span data-ttu-id="428a5-341"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="428a5-341"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

