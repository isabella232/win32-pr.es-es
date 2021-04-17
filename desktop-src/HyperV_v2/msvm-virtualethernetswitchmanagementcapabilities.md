---
description: Describe las capacidades de la VirtualEthernetSwitchManagementService de MSVM asociada \_ .
ms.assetid: daed7a02-bae8-4bda-abc6-0657df7dc4f8
title: Msvm_VirtualEthernetSwitchManagementCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementCapabilities
- Msvm_VirtualEthernetSwitchManagementCapabilities.InstanceID
- Msvm_VirtualEthernetSwitchManagementCapabilities.Caption
- Msvm_VirtualEthernetSwitchManagementCapabilities.Description
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementName
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.MaxElementNameLen
- Msvm_VirtualEthernetSwitchManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameMask
- Msvm_VirtualEthernetSwitchManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IndicationsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupport
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d66d73773b956ecbbbf4ca102b18bb6f8ece4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652800"
---
# <a name="msvm_virtualethernetswitchmanagementcapabilities-class"></a><span data-ttu-id="c9101-103">MSVM \_ VirtualEthernetSwitchManagementCapabilities (clase)</span><span class="sxs-lookup"><span data-stu-id="c9101-103">Msvm\_VirtualEthernetSwitchManagementCapabilities class</span></span>

<span data-ttu-id="c9101-104">Describe las capacidades de la [**\_ VirtualEthernetSwitchManagementService de MSVM**](msvm-virtualethernetswitchmanagementservice.md)asociada.</span><span class="sxs-lookup"><span data-stu-id="c9101-104">Describes the capabilities of the associated [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md).</span></span>

<span data-ttu-id="c9101-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c9101-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9101-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9101-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  string  Description = "Defines Virtual Ethernet Switch Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a><span data-ttu-id="c9101-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c9101-107">Members</span></span>

<span data-ttu-id="c9101-108">La clase **MSVM \_ VirtualEthernetSwitchManagementCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c9101-108">The **Msvm\_VirtualEthernetSwitchManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="c9101-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c9101-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9101-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c9101-110">Properties</span></span>

<span data-ttu-id="c9101-111">La clase **MSVM \_ VirtualEthernetSwitchManagementCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c9101-111">The **Msvm\_VirtualEthernetSwitchManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9101-112">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="c9101-112">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9101-113">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9101-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c9101-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9101-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9101-115">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. AsynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="c9101-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="c9101-116">Una matriz de identificadores de método, cada uno de los cuales identifica un método de la clase [**MSVM \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) que la implementación admite de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c9101-116">An array of method identifiers, each identifying a method of the [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) class that is supported asynchronously by the implementation.</span></span> <span data-ttu-id="c9101-117">Esta propiedad se hereda de **\_ VirtualSystemManagementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="c9101-117">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

<dt>

<span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>

<span data-ttu-id="c9101-118">**DefineSystem** (2)</span><span class="sxs-lookup"><span data-stu-id="c9101-118">**DefineSystem** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>

<span data-ttu-id="c9101-119">**DestroySystem** (3)</span><span class="sxs-lookup"><span data-stu-id="c9101-119">**DestroySystem** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>

<span data-ttu-id="c9101-120">**DestroySystemConfiguration** (4)</span><span class="sxs-lookup"><span data-stu-id="c9101-120">**DestroySystemConfiguration** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>

<span data-ttu-id="c9101-121">**ModifyResourceSettings** (5)</span><span class="sxs-lookup"><span data-stu-id="c9101-121">**ModifyResourceSettings** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>

<span data-ttu-id="c9101-122">**ModifySystemSettings** (6)</span><span class="sxs-lookup"><span data-stu-id="c9101-122">**ModifySystemSettings** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>

<span data-ttu-id="c9101-123">**RemoveResources** (7)</span><span class="sxs-lookup"><span data-stu-id="c9101-123">**RemoveResources** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>

<span data-ttu-id="c9101-124">**SelectSystemConfiguration** (8)</span><span class="sxs-lookup"><span data-stu-id="c9101-124">**SelectSystemConfiguration** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>

<span data-ttu-id="c9101-125">**SnapshotSystem** (9)</span><span class="sxs-lookup"><span data-stu-id="c9101-125">**SnapshotSystem** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>

<span data-ttu-id="c9101-126">**AddResources** (10)</span><span class="sxs-lookup"><span data-stu-id="c9101-126">**AddResources** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="c9101-127">**AddFeatureSettingsSupported** (32779)</span><span class="sxs-lookup"><span data-stu-id="c9101-127">**AddFeatureSettingsSupported** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="c9101-128">**ModifyFeatureSettingsSupported** (32780)</span><span class="sxs-lookup"><span data-stu-id="c9101-128">**ModifyFeatureSettingsSupported** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="c9101-129">**RemoveFeatureSettingsSupported** (32781)</span><span class="sxs-lookup"><span data-stu-id="c9101-129">**RemoveFeatureSettingsSupported** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="c9101-130">**AddFeatureSettingsSupported** (32779)</span><span class="sxs-lookup"><span data-stu-id="c9101-130">**AddFeatureSettingsSupported** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="c9101-131">**ModifyFeatureSettingsSupported** (32780)</span><span class="sxs-lookup"><span data-stu-id="c9101-131">**ModifyFeatureSettingsSupported** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="c9101-132">**RemoveFeatureSettingsSupported** (32781)</span><span class="sxs-lookup"><span data-stu-id="c9101-132">**RemoveFeatureSettingsSupported** (32781)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c9101-133">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c9101-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9101-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9101-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9101-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9101-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9101-136">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c9101-136">A short description of the object.</span></span> <span data-ttu-id="c9101-137">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades del servicio de administración de conmutadores de Ethernet Virtual de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="c9101-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="c9101-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9101-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9101-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9101-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9101-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9101-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9101-141">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c9101-141">A description of the object.</span></span> <span data-ttu-id="c9101-142">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "define las capacidades del servicio de administración de conmutadores Ethernet virtuales".</span><span class="sxs-lookup"><span data-stu-id="c9101-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="c9101-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c9101-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9101-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9101-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9101-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9101-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9101-146">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="c9101-146">A display name for the object.</span></span> <span data-ttu-id="c9101-147">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades del servicio de administración de conmutadores de Ethernet Virtual de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="c9101-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="c9101-148">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="c9101-148">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9101-149">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c9101-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9101-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9101-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9101-151">Indica si se puede modificar la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="c9101-151">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="c9101-152">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="c9101-152">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="c9101-153">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="c9101-153">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9101-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9101-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9101-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9101-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9101-156">Especifica las restricciones en **ElementName**, expresadas como una expresión regular.</span><span class="sxs-lookup"><span data-stu-id="c9101-156">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="c9101-157">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="c9101-157">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="c9101-158">**IndicationsSupported**</span><span class="sxs-lookup"><span data-stu-id="c9101-158">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9101-159">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9101-159">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c9101-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9101-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9101-161">Una matriz de identificadores de indicación, cada uno de los cuales identifica una indicación que es compatible con la implementación de.</span><span class="sxs-lookup"><span data-stu-id="c9101-161">An array of indication identifiers, each identifying an indication that is supported by the implementation.</span></span> <span data-ttu-id="c9101-162">Esta propiedad se hereda de **\_ VirtualSystemManagementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="c9101-162">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>



| <span data-ttu-id="c9101-163">Value</span><span class="sxs-lookup"><span data-stu-id="c9101-163">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="c9101-164">Significado</span><span class="sxs-lookup"><span data-stu-id="c9101-164">Meaning</span></span>                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="c9101-165"><dt>**VirtualResourceStateChangeIndicationsSupported**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c9101-165"><dt>**VirtualResourceStateChangeIndicationsSupported**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="c9101-166">Indica si la implementación admite la notificación de cambios de estado de las instancias de [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) que representan recursos de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="c9101-166">Indicates whether the implementation supports notification on state changes of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) instances that represent resources of virtual systems.</span></span><br/> |
| <span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="c9101-167"><dt>**ConcreteJobStateChangeIndicationsSupported**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c9101-167"><dt>**ConcreteJobStateChangeIndicationsSupported**</dt> <dt>3</dt></span></span> </dl>                 | <span data-ttu-id="c9101-168">Indica si la implementación admite la notificación de cambios de estado de las instancias de [**\_ ConcreteJob de CIM**](/previous-versions//cc136808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c9101-168">Indicates whether the implementation supports notification on state changes of [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) instances.</span></span><br/>                                                      |
| <span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="c9101-169"><dt>**VirtualSystemStateChangeIndicationsSupported**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c9101-169"><dt>**VirtualSystemStateChangeIndicationsSupported**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="c9101-170">Indica si la implementación admite la notificación de cambios de estado de las instancias de los equipos [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representan sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="c9101-170">Indicates whether the implementation supports notification on state changes of [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instances that represent virtual systems.</span></span><br/>            |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="c9101-171"><dt>**DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="c9101-171"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                                                                                                                                    |                                                                                                                                                                                                       |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="c9101-172">El <dt> **proveedor ha reservado**</dt> <dt>32767.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="c9101-172"><dt>**Vendor Reserved** </dt> <dt>32767..65535 </dt></span></span> </dl>                                                                                                             |                                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="c9101-173">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c9101-173">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9101-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9101-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9101-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9101-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9101-176">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="c9101-176">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c9101-177">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="c9101-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c9101-178">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c9101-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c9101-179">**IOVSupport**</span><span class="sxs-lookup"><span data-stu-id="c9101-179">**IOVSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9101-180">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c9101-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9101-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9101-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9101-182">Valor booleano que indica si la plataforma admite la virtualización de e/s (IOV).</span><span class="sxs-lookup"><span data-stu-id="c9101-182">A boolean value that indicates whether I/O virtualization (IOV) is supported by the platform.</span></span> <span data-ttu-id="c9101-183">Si el valor es **true**, la plataforma admite IOV y **iovsupportreasons incluirán** estará vacío.</span><span class="sxs-lookup"><span data-stu-id="c9101-183">If the value is **True**, then IOV is supported by the platform and **IOVSupportReasons** will be empty.</span></span> <span data-ttu-id="c9101-184">De lo contrario, la propiedad **iovsupportreasons incluirán** tendrá los motivos por los que no se admite IOV.</span><span class="sxs-lookup"><span data-stu-id="c9101-184">Otherwise the **IOVSupportReasons** property will have the reasons why IOV cannot be supported.</span></span>

</dd> <dt>

<span data-ttu-id="c9101-185">**Iovsupportreasons incluirán**</span><span class="sxs-lookup"><span data-stu-id="c9101-185">**IOVSupportReasons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9101-186">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c9101-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c9101-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9101-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9101-188">Matriz de cadenas que indica los posibles motivos por los que no se admite IOV.</span><span class="sxs-lookup"><span data-stu-id="c9101-188">An array of strings that indicates the possible reasons why IOV is not supported.</span></span> <span data-ttu-id="c9101-189">Si el valor de **IOVSupport** es **true**, esta matriz estará vacía.</span><span class="sxs-lookup"><span data-stu-id="c9101-189">If the value of **IOVSupport** is **True**, this array will be empty.</span></span>

</dd> <dt>

<span data-ttu-id="c9101-190">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="c9101-190">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9101-191">Tipo de datos: **unit16**</span><span class="sxs-lookup"><span data-stu-id="c9101-191">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="c9101-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9101-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9101-193">Calificadores: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="c9101-193">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c9101-194">Especifica la longitud máxima admitida de la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="c9101-194">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="c9101-195">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="c9101-195">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="c9101-196">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="c9101-196">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9101-197">Tipo de datos: matriz **unit16**</span><span class="sxs-lookup"><span data-stu-id="c9101-197">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="c9101-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9101-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9101-199">Indica los posibles Estados que se pueden solicitar al utilizar el método **RequestStateChange** en el elemento lógico habilitado.</span><span class="sxs-lookup"><span data-stu-id="c9101-199">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="c9101-200">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM** y siempre es **null**.</span><span class="sxs-lookup"><span data-stu-id="c9101-200">This property is inherited from **CIM\_EnabledLogicalElementCapabilities** and is always **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c9101-201">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="c9101-201">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9101-202">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9101-202">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c9101-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9101-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9101-204">Una matriz de identificadores de método, cada uno de los cuales identifica un método de la clase [**MSVM \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) que la implementación admite sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="c9101-204">An array of method identifiers, each identifying a method of the [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) class that is supported synchronously by the implementation.</span></span> <span data-ttu-id="c9101-205">Esta propiedad se hereda de **\_ VirtualSystemManagementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="c9101-205">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

<dl> <dt>

<span data-ttu-id="c9101-206"><span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**DefineSystem** (2)</span><span class="sxs-lookup"><span data-stu-id="c9101-206"><span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**DefineSystem** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c9101-207"><span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**DestroySystem** (3)</span><span class="sxs-lookup"><span data-stu-id="c9101-207"><span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**DestroySystem** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c9101-208"><span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**DestroySystemConfiguration** (4)</span><span class="sxs-lookup"><span data-stu-id="c9101-208"><span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**DestroySystemConfiguration** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c9101-209"><span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**ModifyResourceSettings** (5)</span><span class="sxs-lookup"><span data-stu-id="c9101-209"><span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**ModifyResourceSettings** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c9101-210"><span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**ModifySystemSettings** (6)</span><span class="sxs-lookup"><span data-stu-id="c9101-210"><span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**ModifySystemSettings** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c9101-211"><span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**RemoveResources** (7)</span><span class="sxs-lookup"><span data-stu-id="c9101-211"><span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**RemoveResources** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c9101-212"><span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**SelectSystemConfiguration** (8)</span><span class="sxs-lookup"><span data-stu-id="c9101-212"><span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**SelectSystemConfiguration** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c9101-213"><span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**SnapshotSystem** (9)</span><span class="sxs-lookup"><span data-stu-id="c9101-213"><span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**SnapshotSystem** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c9101-214"><span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**AddResources** (10)</span><span class="sxs-lookup"><span data-stu-id="c9101-214"><span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**AddResources** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c9101-215"><span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**AddFeatureSettings** (32779)</span><span class="sxs-lookup"><span data-stu-id="c9101-215"><span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**AddFeatureSettings** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="c9101-216"><span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**ModifyFeatureSettings** (32780)</span><span class="sxs-lookup"><span data-stu-id="c9101-216"><span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**ModifyFeatureSettings** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="c9101-217"><span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**RemoveFeatureSettings** (32781)</span><span class="sxs-lookup"><span data-stu-id="c9101-217"><span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**RemoveFeatureSettings** (32781 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c9101-218">**VirtualSystemTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="c9101-218">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9101-219">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c9101-219">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c9101-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9101-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9101-221">Matriz de cadenas, cada una de las cuales designa un tipo de sistema virtual que admite la implementación.</span><span class="sxs-lookup"><span data-stu-id="c9101-221">An array of strings, each designating a type of virtual system that the implementation supports.</span></span> <span data-ttu-id="c9101-222">El valor de cada elemento de matriz no **null** debe ajustarse al formato definido para la propiedad **VirtualSystemType** de la [**clase \_ VirtualSystemSettingData de MSVM**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="c9101-222">The value of each non-**Null** array element must conform to the format defined for the **VirtualSystemType** property of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class.</span></span> <span data-ttu-id="c9101-223">Esta propiedad se hereda de **\_ VirtualSystemManagementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="c9101-223">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9101-224">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9101-224">Requirements</span></span>



| <span data-ttu-id="c9101-225">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9101-225">Requirement</span></span> | <span data-ttu-id="c9101-226">Value</span><span class="sxs-lookup"><span data-stu-id="c9101-226">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9101-227">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9101-227">Minimum supported client</span></span><br/> | <span data-ttu-id="c9101-228">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9101-228">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c9101-229">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9101-229">Minimum supported server</span></span><br/> | <span data-ttu-id="c9101-230">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9101-230">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9101-231">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c9101-231">Namespace</span></span><br/>                | <span data-ttu-id="c9101-232">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c9101-232">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c9101-233">MOF</span><span class="sxs-lookup"><span data-stu-id="c9101-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9101-234"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9101-234"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9101-235">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c9101-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9101-236"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c9101-236"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

