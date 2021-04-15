---
description: Proporciona la capacidad de administrar las métricas.
ms.assetid: 39dee432-995d-472a-84c3-eede95dccb43
title: Msvm_MetricService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService
- Msvm_MetricService.InstanceID
- Msvm_MetricService.Caption
- Msvm_MetricService.Description
- Msvm_MetricService.ElementName
- Msvm_MetricService.InstallDate
- Msvm_MetricService.OperationalStatus
- Msvm_MetricService.StatusDescriptions
- Msvm_MetricService.Status
- Msvm_MetricService.HealthState
- Msvm_MetricService.CommunicationStatus
- Msvm_MetricService.DetailedStatus
- Msvm_MetricService.OperatingStatus
- Msvm_MetricService.PrimaryStatus
- Msvm_MetricService.EnabledState
- Msvm_MetricService.OtherEnabledState
- Msvm_MetricService.RequestedState
- Msvm_MetricService.EnabledDefault
- Msvm_MetricService.TimeOfLastStateChange
- Msvm_MetricService.AvailableRequestedStates
- Msvm_MetricService.TransitioningToState
- Msvm_MetricService.SystemCreationClassName
- Msvm_MetricService.SystemName
- Msvm_MetricService.Name
- Msvm_MetricService.CreationClassName
- Msvm_MetricService.PrimaryOwnerName
- Msvm_MetricService.PrimaryOwnerContact
- Msvm_MetricService.StartMode
- Msvm_MetricService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c4117e3adf3db5a2b0073615ae999b9f85bb9b18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688564"
---
# <a name="msvm_metricservice-class"></a><span data-ttu-id="992fd-103">MSVM \_ MetricService (clase)</span><span class="sxs-lookup"><span data-stu-id="992fd-103">Msvm\_MetricService class</span></span>

<span data-ttu-id="992fd-104">Proporciona la capacidad de administrar las métricas.</span><span class="sxs-lookup"><span data-stu-id="992fd-104">Provides the ability to manage metrics.</span></span>

<span data-ttu-id="992fd-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="992fd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="992fd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="992fd-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricService : CIM_MetricService
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service";
  string   Description = "Provides Hyper-V Metric WMI management";
  string   ElementName = "Hyper-V Metric Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
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
  string   Name = "metricsvc";
  string   CreationClassName = "Msvm_MetricService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="992fd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="992fd-107">Members</span></span>

<span data-ttu-id="992fd-108">La clase **MSVM \_ MetricService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="992fd-108">The **Msvm\_MetricService** class has these types of members:</span></span>

-   [<span data-ttu-id="992fd-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="992fd-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="992fd-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="992fd-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="992fd-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="992fd-111">Methods</span></span>

<span data-ttu-id="992fd-112">La clase **MSVM \_ MetricService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="992fd-112">The **Msvm\_MetricService** class has these methods.</span></span>



| <span data-ttu-id="992fd-113">Método</span><span class="sxs-lookup"><span data-stu-id="992fd-113">Method</span></span>                                                                    | <span data-ttu-id="992fd-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="992fd-114">Description</span></span>                                                                             |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="992fd-115">**ControlMetrics**</span><span class="sxs-lookup"><span data-stu-id="992fd-115">**ControlMetrics**</span></span>](controlmetrics-msvm-metricservice.md)               | <span data-ttu-id="992fd-116">Se utiliza para controlar la colección de métricas de un elemento o elementos administrados.</span><span class="sxs-lookup"><span data-stu-id="992fd-116">Used to control the collection of metrics for a managed element or elements.</span></span><br/> |
| [<span data-ttu-id="992fd-117">**ControlMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="992fd-117">**ControlMetricsByClass**</span></span>](msvm-metricservice-controlmetricsbyclass.md) | <span data-ttu-id="992fd-118">Controla las métricas por clase.</span><span class="sxs-lookup"><span data-stu-id="992fd-118">Controls the metrics by class.</span></span><br/>                                               |
| [<span data-ttu-id="992fd-119">**ControlSampleTimes**</span><span class="sxs-lookup"><span data-stu-id="992fd-119">**ControlSampleTimes**</span></span>](msvm-metricservice-controlsampletimes.md)       | <span data-ttu-id="992fd-120">Establece las horas de muestra del control.</span><span class="sxs-lookup"><span data-stu-id="992fd-120">Sets the control sample times.</span></span><br/>                                               |
| [<span data-ttu-id="992fd-121">**GetMetricValues**</span><span class="sxs-lookup"><span data-stu-id="992fd-121">**GetMetricValues**</span></span>](msvm-metricservice-getmetricvalues.md)             | <span data-ttu-id="992fd-122">Recupera los valores de la métrica.</span><span class="sxs-lookup"><span data-stu-id="992fd-122">Retrieves the metric values.</span></span><br/>                                                 |
| [<span data-ttu-id="992fd-123">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="992fd-123">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-metricservice.md) | <span data-ttu-id="992fd-124">Modifica los datos de configuración para el servicio.</span><span class="sxs-lookup"><span data-stu-id="992fd-124">Modifies the setting data for the service.</span></span><br/>                                   |
| [<span data-ttu-id="992fd-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="992fd-125">**RequestStateChange**</span></span>](msvm-metricservice-requeststatechange.md)       | <span data-ttu-id="992fd-126">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="992fd-126">Requests a state change.</span></span><br/>                                                     |
| [<span data-ttu-id="992fd-127">**ShowMetrics**</span><span class="sxs-lookup"><span data-stu-id="992fd-127">**ShowMetrics**</span></span>](msvm-metricservice-showmetrics.md)                     | <span data-ttu-id="992fd-128">Muestra las métricas especificadas.</span><span class="sxs-lookup"><span data-stu-id="992fd-128">Shows the specified metrics.</span></span><br/>                                                 |
| [<span data-ttu-id="992fd-129">**ShowMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="992fd-129">**ShowMetricsByClass**</span></span>](msvm-metricservice-showmetricsbyclass.md)       | <span data-ttu-id="992fd-130">Muestra las métricas por clase.</span><span class="sxs-lookup"><span data-stu-id="992fd-130">Shows the metrics by class.</span></span><br/>                                                  |
| [<span data-ttu-id="992fd-131">**StartService**</span><span class="sxs-lookup"><span data-stu-id="992fd-131">**StartService**</span></span>](msvm-metricservice-startservice.md)                   | <span data-ttu-id="992fd-132">inicia el servicio.</span><span class="sxs-lookup"><span data-stu-id="992fd-132">Starts the service.</span></span><br/>                                                          |
| [<span data-ttu-id="992fd-133">**StopService**</span><span class="sxs-lookup"><span data-stu-id="992fd-133">**StopService**</span></span>](msvm-metricservice-stopservice.md)                     | <span data-ttu-id="992fd-134">detiene el servicio.</span><span class="sxs-lookup"><span data-stu-id="992fd-134">Stops the service.</span></span><br/>                                                           |



 

### <a name="properties"></a><span data-ttu-id="992fd-135">Propiedades</span><span class="sxs-lookup"><span data-stu-id="992fd-135">Properties</span></span>

<span data-ttu-id="992fd-136">La clase **MSVM \_ MetricService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="992fd-136">The **Msvm\_MetricService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="992fd-137">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="992fd-137">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-138">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="992fd-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="992fd-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-140">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="992fd-140">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="992fd-141">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="992fd-141">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="992fd-142">**Caption**</span><span class="sxs-lookup"><span data-stu-id="992fd-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="992fd-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-145">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="992fd-145">A short description of the object.</span></span> <span data-ttu-id="992fd-146">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de métricas de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="992fd-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service".</span></span>

</dd> <dt>

<span data-ttu-id="992fd-147">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="992fd-147">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-148">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="992fd-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-150">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="992fd-150">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="992fd-151">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="992fd-151">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="992fd-152">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="992fd-152">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="992fd-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="992fd-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="992fd-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="992fd-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="992fd-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="992fd-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="992fd-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="992fd-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="992fd-160">)</span><span class="sxs-lookup"><span data-stu-id="992fd-160">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="992fd-161">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="992fd-161">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="992fd-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-164">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="992fd-164">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="992fd-165">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ MetricService".</span><span class="sxs-lookup"><span data-stu-id="992fd-165">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_MetricService".</span></span>

</dd> <dt>

<span data-ttu-id="992fd-166">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="992fd-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="992fd-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-169">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="992fd-169">A description of the object.</span></span> <span data-ttu-id="992fd-170">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "proporciona administración WMI de métricas de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="992fd-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Hyper-V Metric WMI management".</span></span>

</dd> <dt>

<span data-ttu-id="992fd-171">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="992fd-171">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-172">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="992fd-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-174">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="992fd-174">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="992fd-175">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="992fd-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="992fd-176">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="992fd-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="992fd-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="992fd-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-178"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="992fd-178"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-179"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="992fd-179"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-180"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="992fd-180"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-181"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="992fd-181"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-182"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="992fd-182"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-183"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="992fd-183"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-184"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="992fd-184"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="992fd-185">)</span><span class="sxs-lookup"><span data-stu-id="992fd-185">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="992fd-186">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="992fd-186">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="992fd-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-189">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="992fd-189">A display name for the object.</span></span> <span data-ttu-id="992fd-190">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de métricas de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="992fd-190">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service".</span></span>

</dd> <dt>

<span data-ttu-id="992fd-191">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="992fd-191">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-192">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="992fd-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-194">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="992fd-194">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="992fd-195">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="992fd-195">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="992fd-196">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="992fd-196">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="992fd-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-199">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="992fd-199">The enabled and disabled states of an element.</span></span> <span data-ttu-id="992fd-200">Esta propiedad también puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="992fd-200">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="992fd-201">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="992fd-201">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="992fd-202">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="992fd-202">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-203">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="992fd-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-205">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="992fd-205">The current health of the element.</span></span> <span data-ttu-id="992fd-206">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="992fd-206">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="992fd-207">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="992fd-207">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="992fd-208">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="992fd-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="992fd-209">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="992fd-209">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-210">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="992fd-210">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-212">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="992fd-212">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="992fd-213">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="992fd-213">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="992fd-214">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="992fd-214">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-215">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="992fd-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="992fd-217">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="992fd-217">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="992fd-218">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="992fd-218">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="992fd-219">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="992fd-219">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="992fd-220">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="992fd-220">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-221">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="992fd-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-223">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="992fd-223">The label by which the object is known.</span></span> <span data-ttu-id="992fd-224">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "metricsvc".</span><span class="sxs-lookup"><span data-stu-id="992fd-224">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "metricsvc".</span></span>

</dd> <dt>

<span data-ttu-id="992fd-225">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="992fd-225">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-226">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="992fd-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-227">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-228">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="992fd-228">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="992fd-229">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="992fd-229">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="992fd-230">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="992fd-230">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="992fd-231"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="992fd-231"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-232"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="992fd-232"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-233"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="992fd-233"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="992fd-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-235"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="992fd-235"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-236"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="992fd-236"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-237"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="992fd-237"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-238"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="992fd-238"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-239"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="992fd-239"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-240"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="992fd-240"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-241"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="992fd-241"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-242"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="992fd-242"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-243"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="992fd-243"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-244"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="992fd-244"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-245"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="992fd-245"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-246"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="992fd-246"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="992fd-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="992fd-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="992fd-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="992fd-250">)</span><span class="sxs-lookup"><span data-stu-id="992fd-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="992fd-251">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="992fd-251">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-252">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="992fd-252">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="992fd-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-254">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="992fd-254">The current statuses of the object.</span></span> <span data-ttu-id="992fd-255">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="992fd-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="992fd-256">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="992fd-256">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="992fd-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-259">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="992fd-259">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="992fd-260">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="992fd-260">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="992fd-261">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="992fd-261">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="992fd-262">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="992fd-262">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-263">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="992fd-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-265">Valor que proporciona información sobre cómo se puede alcanzar el propietario principal del servicio (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.).</span><span class="sxs-lookup"><span data-stu-id="992fd-265">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="992fd-266">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="992fd-266">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="992fd-267">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="992fd-267">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-268">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="992fd-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-270">Nombre del propietario principal del servicio, si se ha definido uno.</span><span class="sxs-lookup"><span data-stu-id="992fd-270">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="992fd-271">El propietario principal es el contacto de soporte inicial para el servicio.</span><span class="sxs-lookup"><span data-stu-id="992fd-271">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="992fd-272">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="992fd-272">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="992fd-273">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="992fd-273">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-274">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="992fd-274">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-276">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="992fd-276">Provides high level status information.</span></span> <span data-ttu-id="992fd-277">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="992fd-277">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="992fd-278">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="992fd-278">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="992fd-279">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="992fd-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="992fd-280"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="992fd-280"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-281"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="992fd-281"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-282"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="992fd-282"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-283"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="992fd-283"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-284"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="992fd-284"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="992fd-285"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="992fd-285"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="992fd-286">)</span><span class="sxs-lookup"><span data-stu-id="992fd-286">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="992fd-287">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="992fd-287">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-288">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="992fd-288">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-290">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="992fd-290">The last requested or desired state for the element.</span></span> <span data-ttu-id="992fd-291">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="992fd-291">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="992fd-292">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="992fd-292">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="992fd-293">Una instancia concreta de [**\_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir el método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="992fd-293">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="992fd-294">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="992fd-294">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="992fd-295">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM** y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="992fd-295">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="992fd-296">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="992fd-296">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-297">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="992fd-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-299">Indica si el servicio se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="992fd-299">Indicates whether the service is currently running.</span></span> <span data-ttu-id="992fd-300">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="992fd-300">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="992fd-301">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="992fd-301">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-302">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="992fd-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-304">Un valor de cadena que indica si el servicio se inicia automáticamente por un sistema, un sistema operativo o se inicia solo después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="992fd-304">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="992fd-305">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="992fd-305">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="992fd-306">**Estado**</span><span class="sxs-lookup"><span data-stu-id="992fd-306">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="992fd-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-309">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en "OK".</span><span class="sxs-lookup"><span data-stu-id="992fd-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="992fd-310">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="992fd-310">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-311">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="992fd-311">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="992fd-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-313">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="992fd-313">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="992fd-314">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y las cadenas siempre se establecen en "OK".</span><span class="sxs-lookup"><span data-stu-id="992fd-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and the strings are always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="992fd-315">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="992fd-315">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-316">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="992fd-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-318">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="992fd-318">The scoping system's creation class name.</span></span> <span data-ttu-id="992fd-319">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="992fd-319">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="992fd-320">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="992fd-320">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-321">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="992fd-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-323">Nombre del sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="992fd-323">The name of the hosting computer system.</span></span> <span data-ttu-id="992fd-324">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="992fd-324">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="992fd-325">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="992fd-325">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-326">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="992fd-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-328">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="992fd-328">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="992fd-329">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="992fd-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="992fd-330">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="992fd-330">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="992fd-331">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="992fd-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="992fd-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="992fd-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="992fd-333">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="992fd-333">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="992fd-334">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="992fd-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="992fd-335">Requisitos</span><span class="sxs-lookup"><span data-stu-id="992fd-335">Requirements</span></span>



| <span data-ttu-id="992fd-336">Requisito</span><span class="sxs-lookup"><span data-stu-id="992fd-336">Requirement</span></span> | <span data-ttu-id="992fd-337">Value</span><span class="sxs-lookup"><span data-stu-id="992fd-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="992fd-338">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="992fd-338">Minimum supported client</span></span><br/> | <span data-ttu-id="992fd-339">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="992fd-339">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="992fd-340">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="992fd-340">Minimum supported server</span></span><br/> | <span data-ttu-id="992fd-341">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="992fd-341">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="992fd-342">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="992fd-342">Namespace</span></span><br/>                | <span data-ttu-id="992fd-343">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="992fd-343">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="992fd-344">MOF</span><span class="sxs-lookup"><span data-stu-id="992fd-344">MOF</span></span><br/>                      | <dl> <span data-ttu-id="992fd-345"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="992fd-345"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="992fd-346">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="992fd-346">DLL</span></span><br/>                      | <dl> <span data-ttu-id="992fd-347"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="992fd-347"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

