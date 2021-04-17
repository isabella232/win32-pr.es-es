---
description: Representa las capacidades de un \_ objeto VirtualSystemManagementService de CIM.
ms.assetid: 484b0378-b354-49c4-b98b-a960a7b07b92
title: CIM_VirtualSystemManagementCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementCapabilities
- CIM_VirtualSystemManagementCapabilities.VirtualSystemTypesSupported
- CIM_VirtualSystemManagementCapabilities.SynchronousMethodsSupported
- CIM_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported
- CIM_VirtualSystemManagementCapabilities.IndicationsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2772068ed011a2a61cdd4f5c1396e057838b7720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666897"
---
# <a name="cim_virtualsystemmanagementcapabilities-class"></a><span data-ttu-id="cee14-103">\_Clase VirtualSystemManagementCapabilities de CIM</span><span class="sxs-lookup"><span data-stu-id="cee14-103">CIM\_VirtualSystemManagementCapabilities class</span></span>

<span data-ttu-id="cee14-104">Representa las capacidades de un [**objeto \_ VirtualSystemManagementService de CIM**](cim-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="cee14-104">Represents the capabilities of a [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cee14-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cee14-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string VirtualSystemTypesSupported[];
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 IndicationsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="cee14-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="cee14-106">Members</span></span>

<span data-ttu-id="cee14-107">La clase **CIM \_ VirtualSystemManagementCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cee14-107">The **CIM\_VirtualSystemManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="cee14-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cee14-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cee14-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cee14-109">Properties</span></span>

<span data-ttu-id="cee14-110">La clase **CIM \_ VirtualSystemManagementCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cee14-110">The **CIM\_VirtualSystemManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cee14-111">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="cee14-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cee14-112">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cee14-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cee14-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cee14-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cee14-114">Una matriz que contiene los nombres de método para los métodos de clase [**\_ VirtualSystemManagementService de CIM**](cim-virtualsystemmanagementservice.md) que se admiten para las operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="cee14-114">An array that contains method names for the [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) class methods that are supported for asynchronous operations.</span></span>

<dt>

<span id="DefineSystemSupported"></span><span id="definesystemsupported"></span><span id="DEFINESYSTEMSUPPORTED"></span>

<span data-ttu-id="cee14-115">**DefineSystemSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="cee14-115">**DefineSystemSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemSupported"></span><span id="destroysystemsupported"></span><span id="DESTROYSYSTEMSUPPORTED"></span>

<span data-ttu-id="cee14-116">**DestroySystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="cee14-116">**DestroySystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfigurationSupported"></span><span id="destroysystemconfigurationsupported"></span><span id="DESTROYSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="cee14-117">**DestroySystemConfigurationSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="cee14-117">**DestroySystemConfigurationSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettingsSupported"></span><span id="modifyresourcesettingssupported"></span><span id="MODIFYRESOURCESETTINGSSUPPORTED"></span>

<span data-ttu-id="cee14-118">**ModifyResourceSettingsSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="cee14-118">**ModifyResourceSettingsSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettingsSupported"></span><span id="modifysystemsettingssupported"></span><span id="MODIFYSYSTEMSETTINGSSUPPORTED"></span>

<span data-ttu-id="cee14-119">**ModifySystemSettingsSupported** (6)</span><span class="sxs-lookup"><span data-stu-id="cee14-119">**ModifySystemSettingsSupported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesSupported"></span><span id="removeresourcessupported"></span><span id="REMOVERESOURCESSUPPORTED"></span>

<span data-ttu-id="cee14-120">**RemoveResourcesSupported** (7)</span><span class="sxs-lookup"><span data-stu-id="cee14-120">**RemoveResourcesSupported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfigurationSupported"></span><span id="selectsystemconfigurationsupported"></span><span id="SELECTSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="cee14-121">**SelectSystemConfigurationSupported** (8)</span><span class="sxs-lookup"><span data-stu-id="cee14-121">**SelectSystemConfigurationSupported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystemSupported"></span><span id="snapshotsystemsupported"></span><span id="SNAPSHOTSYSTEMSUPPORTED"></span>

<span data-ttu-id="cee14-122">**SnapshotSystemSupported** (9)</span><span class="sxs-lookup"><span data-stu-id="cee14-122">**SnapshotSystemSupported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesSupported"></span><span id="addresourcessupported"></span><span id="ADDRESOURCESSUPPORTED"></span>

<span data-ttu-id="cee14-123">**AddResourcesSupported** (10)</span><span class="sxs-lookup"><span data-stu-id="cee14-123">**AddResourcesSupported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cee14-124">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="cee14-124">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="cee14-125">**Proveedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="cee14-125">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cee14-126">**IndicationsSupported**</span><span class="sxs-lookup"><span data-stu-id="cee14-126">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cee14-127">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cee14-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cee14-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cee14-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cee14-129">Una matriz que contiene los tipos de indicación admitidos de la implementación.</span><span class="sxs-lookup"><span data-stu-id="cee14-129">An array that contains the supported indications types of the implementation.</span></span>

<dt>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="cee14-130">**VirtualResourceStateChangeIndicationsSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="cee14-130">**VirtualResourceStateChangeIndicationsSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="cee14-131">**ConcreteJobStateChangeIndicationsSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="cee14-131">**ConcreteJobStateChangeIndicationsSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="cee14-132">**VirtualSystemStateChangeIndicationsSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="cee14-132">**VirtualSystemStateChangeIndicationsSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cee14-133">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="cee14-133">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="cee14-134">**Proveedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="cee14-134">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cee14-135">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="cee14-135">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cee14-136">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cee14-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cee14-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cee14-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cee14-138">Una matriz que contiene los nombres de método para los métodos de clase [**\_ VirtualSystemManagementService de CIM**](cim-virtualsystemmanagementservice.md) que se admiten para las operaciones sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="cee14-138">An array that contains method names for the [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) class methods that are supported for synchronous operations.</span></span>

<dt>

<span id="DefineSystemSupported"></span><span id="definesystemsupported"></span><span id="DEFINESYSTEMSUPPORTED"></span>

<span data-ttu-id="cee14-139">**DefineSystemSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="cee14-139">**DefineSystemSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemSupported"></span><span id="destroysystemsupported"></span><span id="DESTROYSYSTEMSUPPORTED"></span>

<span data-ttu-id="cee14-140">**DestroySystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="cee14-140">**DestroySystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfigurationSupported"></span><span id="destroysystemconfigurationsupported"></span><span id="DESTROYSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="cee14-141">**DestroySystemConfigurationSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="cee14-141">**DestroySystemConfigurationSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettingsSupported"></span><span id="modifyresourcesettingssupported"></span><span id="MODIFYRESOURCESETTINGSSUPPORTED"></span>

<span data-ttu-id="cee14-142">**ModifyResourceSettingsSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="cee14-142">**ModifyResourceSettingsSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettingsSupported"></span><span id="modifysystemsettingssupported"></span><span id="MODIFYSYSTEMSETTINGSSUPPORTED"></span>

<span data-ttu-id="cee14-143">**ModifySystemSettingsSupported** (6)</span><span class="sxs-lookup"><span data-stu-id="cee14-143">**ModifySystemSettingsSupported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesSupported"></span><span id="removeresourcessupported"></span><span id="REMOVERESOURCESSUPPORTED"></span>

<span data-ttu-id="cee14-144">**RemoveResourcesSupported** (7)</span><span class="sxs-lookup"><span data-stu-id="cee14-144">**RemoveResourcesSupported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfigurationSupported"></span><span id="selectsystemconfigurationsupported"></span><span id="SELECTSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="cee14-145">**SelectSystemConfigurationSupported** (8)</span><span class="sxs-lookup"><span data-stu-id="cee14-145">**SelectSystemConfigurationSupported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystemSupported"></span><span id="snapshotsystemsupported"></span><span id="SNAPSHOTSYSTEMSUPPORTED"></span>

<span data-ttu-id="cee14-146">**SnapshotSystemSupported** (9)</span><span class="sxs-lookup"><span data-stu-id="cee14-146">**SnapshotSystemSupported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesSupported"></span><span id="addresourcessupported"></span><span id="ADDRESOURCESSUPPORTED"></span>

<span data-ttu-id="cee14-147">**AddResourcesSupported** (10)</span><span class="sxs-lookup"><span data-stu-id="cee14-147">**AddResourcesSupported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cee14-148">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="cee14-148">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="cee14-149">**Proveedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="cee14-149">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cee14-150">**VirtualSystemTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="cee14-150">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cee14-151">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="cee14-151">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cee14-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cee14-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cee14-153">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md).**VirtualSystemType**")</span><span class="sxs-lookup"><span data-stu-id="cee14-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md).**VirtualSystemType**")</span></span>
</dt> </dl>

<span data-ttu-id="cee14-154">El tipo de sistemas virtuales que admite la implementación.</span><span class="sxs-lookup"><span data-stu-id="cee14-154">The type of virtual systems supported by the implementation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cee14-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cee14-155">Requirements</span></span>



| <span data-ttu-id="cee14-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="cee14-156">Requirement</span></span> | <span data-ttu-id="cee14-157">Value</span><span class="sxs-lookup"><span data-stu-id="cee14-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cee14-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cee14-158">Minimum supported client</span></span><br/> | <span data-ttu-id="cee14-159">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cee14-159">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="cee14-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cee14-160">Minimum supported server</span></span><br/> | <span data-ttu-id="cee14-161">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cee14-161">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="cee14-162">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cee14-162">Namespace</span></span><br/>                | <span data-ttu-id="cee14-163">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="cee14-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cee14-164">MOF</span><span class="sxs-lookup"><span data-stu-id="cee14-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cee14-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cee14-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cee14-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cee14-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cee14-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cee14-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cee14-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="cee14-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cee14-169">**\_ENABLEDLOGICALELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="cee14-169">**CIM\_EnabledLogicalElementCapabilities**</span></span>](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

