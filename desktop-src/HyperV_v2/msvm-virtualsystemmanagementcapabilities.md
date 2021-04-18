---
description: Describe las capacidades de la VirtualSystemManagementService de MSVM asociada \_ .
ms.assetid: 3a167b06-bddd-4bac-95c0-ecf14e01eec0
title: Msvm_VirtualSystemManagementCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementCapabilities
- Msvm_VirtualSystemManagementCapabilities.InstanceID
- Msvm_VirtualSystemManagementCapabilities.Caption
- Msvm_VirtualSystemManagementCapabilities.Description
- Msvm_VirtualSystemManagementCapabilities.ElementName
- Msvm_VirtualSystemManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemManagementCapabilities.MaxElementNameLen
- Msvm_VirtualSystemManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemManagementCapabilities.ElementNameMask
- Msvm_VirtualSystemManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualSystemManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualSystemManagementCapabilities.IndicationsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24bc8ce66393a5e9ccd13848ab74640aec8d1760
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360157"
---
# <a name="msvm_virtualsystemmanagementcapabilities-class"></a><span data-ttu-id="2417d-103">MSVM \_ VirtualSystemManagementCapabilities (clase)</span><span class="sxs-lookup"><span data-stu-id="2417d-103">Msvm\_VirtualSystemManagementCapabilities class</span></span>

<span data-ttu-id="2417d-104">Describe las capacidades de la [**\_ VirtualSystemManagementService de MSVM**](msvm-virtualsystemmanagementservice.md)asociada.</span><span class="sxs-lookup"><span data-stu-id="2417d-104">Describes the capabilities of the associated [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md).</span></span>

<span data-ttu-id="2417d-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2417d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2417d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2417d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Management Service Capabilities";
  string  Description = "Defines Virtual System Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual System Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="2417d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2417d-107">Members</span></span>

<span data-ttu-id="2417d-108">La clase **MSVM \_ VirtualSystemManagementCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2417d-108">The **Msvm\_VirtualSystemManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="2417d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2417d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2417d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2417d-110">Properties</span></span>

<span data-ttu-id="2417d-111">La clase **MSVM \_ VirtualSystemManagementCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2417d-111">The **Msvm\_VirtualSystemManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2417d-112">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="2417d-112">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2417d-113">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2417d-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2417d-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2417d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2417d-115">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. AsynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="2417d-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="2417d-116">Especifica los métodos de [**\_ VirtualSystemManagementService de MSVM**](msvm-virtualsystemmanagementservice.md) que se admiten de forma asincrónica en la implementación de.</span><span class="sxs-lookup"><span data-stu-id="2417d-116">Specifies the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) methods that are supported asynchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2417d-117">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2417d-117">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

<span data-ttu-id="2417d-118">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span><span class="sxs-lookup"><span data-stu-id="2417d-118">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="2417d-119">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span><span class="sxs-lookup"><span data-stu-id="2417d-119">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

<span data-ttu-id="2417d-120">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span><span class="sxs-lookup"><span data-stu-id="2417d-120">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

<span data-ttu-id="2417d-121">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span><span class="sxs-lookup"><span data-stu-id="2417d-121">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span></span>


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="2417d-122">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span><span class="sxs-lookup"><span data-stu-id="2417d-122">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

<span data-ttu-id="2417d-123">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span><span class="sxs-lookup"><span data-stu-id="2417d-123">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

<span data-ttu-id="2417d-124">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span><span class="sxs-lookup"><span data-stu-id="2417d-124">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

<span data-ttu-id="2417d-125">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span><span class="sxs-lookup"><span data-stu-id="2417d-125">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

<span data-ttu-id="2417d-126">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span><span class="sxs-lookup"><span data-stu-id="2417d-126">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

<span data-ttu-id="2417d-127">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span><span class="sxs-lookup"><span data-stu-id="2417d-127">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

<span data-ttu-id="2417d-128">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span><span class="sxs-lookup"><span data-stu-id="2417d-128">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

<span data-ttu-id="2417d-129">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span><span class="sxs-lookup"><span data-stu-id="2417d-129">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

<span data-ttu-id="2417d-130">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span><span class="sxs-lookup"><span data-stu-id="2417d-130">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

<span data-ttu-id="2417d-131">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span><span class="sxs-lookup"><span data-stu-id="2417d-131">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

<span data-ttu-id="2417d-132">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span><span class="sxs-lookup"><span data-stu-id="2417d-132">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

<span data-ttu-id="2417d-133">**RequestStateChangeSupported** (32789)</span><span class="sxs-lookup"><span data-stu-id="2417d-133">**RequestStateChangeSupported** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

<span data-ttu-id="2417d-134">**StartServiceSupported** (32790)</span><span class="sxs-lookup"><span data-stu-id="2417d-134">**StartServiceSupported** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

<span data-ttu-id="2417d-135">**StopServiceSupported** (32791)</span><span class="sxs-lookup"><span data-stu-id="2417d-135">**StopServiceSupported** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

<span data-ttu-id="2417d-136">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span><span class="sxs-lookup"><span data-stu-id="2417d-136">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span></span>


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

<span data-ttu-id="2417d-137">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span><span class="sxs-lookup"><span data-stu-id="2417d-137">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

<span data-ttu-id="2417d-138">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span><span class="sxs-lookup"><span data-stu-id="2417d-138">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

<span data-ttu-id="2417d-139">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span><span class="sxs-lookup"><span data-stu-id="2417d-139">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span></span>


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

<span data-ttu-id="2417d-140">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span><span class="sxs-lookup"><span data-stu-id="2417d-140">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

<span data-ttu-id="2417d-141">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span><span class="sxs-lookup"><span data-stu-id="2417d-141">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span></span>


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

<span data-ttu-id="2417d-142">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span><span class="sxs-lookup"><span data-stu-id="2417d-142">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2417d-143">**Proveedor reservado** (32799.. 65535)</span><span class="sxs-lookup"><span data-stu-id="2417d-143">**Vendor Reserved** (32799..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2417d-144">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2417d-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2417d-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2417d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2417d-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2417d-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2417d-147">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="2417d-147">A short description of the object.</span></span> <span data-ttu-id="2417d-148">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2417d-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2417d-149">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2417d-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2417d-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2417d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2417d-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2417d-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2417d-152">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="2417d-152">A description of the object.</span></span> <span data-ttu-id="2417d-153">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2417d-153">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2417d-154">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2417d-154">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2417d-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2417d-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2417d-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2417d-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2417d-157">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="2417d-157">A display name for the object.</span></span> <span data-ttu-id="2417d-158">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2417d-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2417d-159">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="2417d-159">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2417d-160">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2417d-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2417d-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2417d-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2417d-162">Indica si se puede modificar la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="2417d-162">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="2417d-163">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="2417d-163">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="2417d-164">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="2417d-164">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2417d-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2417d-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2417d-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2417d-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2417d-167">Especifica las restricciones en **ElementName**, expresadas como una expresión regular.</span><span class="sxs-lookup"><span data-stu-id="2417d-167">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="2417d-168">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="2417d-168">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="2417d-169">**IndicationsSupported**</span><span class="sxs-lookup"><span data-stu-id="2417d-169">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2417d-170">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2417d-170">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2417d-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2417d-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2417d-172">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. IndicationsSupported")</span><span class="sxs-lookup"><span data-stu-id="2417d-172">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.IndicationsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="2417d-173">Especifica las indicaciones admitidas por la implementación de.</span><span class="sxs-lookup"><span data-stu-id="2417d-173">Specifies the indications supported by the implementation.</span></span>

<span data-ttu-id="2417d-174">Enumeración de identificadores de indicación que identifican una indicación que es compatible con la implementación.</span><span class="sxs-lookup"><span data-stu-id="2417d-174">Enumeration of indication identifiers each identifying an indication that is supported by the implementation.</span></span>

<dt>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="2417d-175"><span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualResourceStateChangeIndicationsSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="2417d-175"><span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualResourceStateChangeIndicationsSupported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2417d-176">La implementación de admite la notificación de cambios de estado de las instancias de [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) que representan recursos de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="2417d-176">The implementation supports notification of state changes of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) instances representing resources of virtual systems.</span></span>

</dd> <dt>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="2417d-177"><span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>**ConcreteJobStateChangeIndicationsSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="2417d-177"><span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>**ConcreteJobStateChangeIndicationsSupported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2417d-178">La implementación de admite la notificación de cambios de estado de las instancias de [**\_ ConcreteJob de CIM**](/previous-versions//cc136808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2417d-178">The implementation supports notification of state changes of [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) instances.</span></span>

</dd> <dt>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="2417d-179"><span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualSystemStateChangeIndicationsSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="2417d-179"><span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualSystemStateChangeIndicationsSupported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2417d-180">La implementación de admite la notificación de cambios de estado de las instancias de los equipos [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representan sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="2417d-180">The implementation supports notification of state changes of [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instances representing virtual systems.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2417d-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2417d-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2417d-182"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="2417d-182"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2417d-183">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2417d-183">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2417d-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2417d-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2417d-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2417d-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2417d-186">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="2417d-186">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2417d-187">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="2417d-187">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2417d-188">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2417d-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2417d-189">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="2417d-189">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2417d-190">Tipo de datos: **unit16**</span><span class="sxs-lookup"><span data-stu-id="2417d-190">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="2417d-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2417d-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2417d-192">Calificadores: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="2417d-192">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="2417d-193">Especifica la longitud máxima admitida de la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="2417d-193">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="2417d-194">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="2417d-194">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="2417d-195">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="2417d-195">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2417d-196">Tipo de datos: matriz **unit16**</span><span class="sxs-lookup"><span data-stu-id="2417d-196">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="2417d-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2417d-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2417d-198">Indica los posibles Estados que se pueden solicitar al utilizar el método **RequestStateChange** en el elemento lógico habilitado.</span><span class="sxs-lookup"><span data-stu-id="2417d-198">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="2417d-199">Esta propiedad se hereda de **\_ EnabledLogicalElementCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="2417d-199">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="2417d-200">Value</span><span class="sxs-lookup"><span data-stu-id="2417d-200">Value</span></span>                                                                         | <span data-ttu-id="2417d-201">Significado</span><span class="sxs-lookup"><span data-stu-id="2417d-201">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="2417d-202"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2417d-202"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="2417d-203">habilitado</span><span class="sxs-lookup"><span data-stu-id="2417d-203">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="2417d-204"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2417d-204"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="2417d-205">Impide</span><span class="sxs-lookup"><span data-stu-id="2417d-205">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="2417d-206"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2417d-206"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="2417d-207">Apagar</span><span class="sxs-lookup"><span data-stu-id="2417d-207">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="2417d-208"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2417d-208"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="2417d-209">Sin conexión</span><span class="sxs-lookup"><span data-stu-id="2417d-209">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="2417d-210"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="2417d-210"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="2417d-211">Prueba</span><span class="sxs-lookup"><span data-stu-id="2417d-211">Test</span></span><br/>      |
| <dl> <span data-ttu-id="2417d-212"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="2417d-212"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="2417d-213">Acepta</span><span class="sxs-lookup"><span data-stu-id="2417d-213">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="2417d-214"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="2417d-214"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="2417d-215">Modo de inactividad</span><span class="sxs-lookup"><span data-stu-id="2417d-215">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="2417d-216"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="2417d-216"><dt>10</dt></span></span> </dl> | <span data-ttu-id="2417d-217">Reboot</span><span class="sxs-lookup"><span data-stu-id="2417d-217">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="2417d-218"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="2417d-218"><dt>11</dt></span></span> </dl> | <span data-ttu-id="2417d-219">Reset</span><span class="sxs-lookup"><span data-stu-id="2417d-219">Reset</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="2417d-220">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="2417d-220">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2417d-221">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2417d-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2417d-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2417d-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2417d-223">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. SynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="2417d-223">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.SynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="2417d-224">Especifica los métodos de [**\_ VirtualSystemManagementService de MSVM**](msvm-virtualsystemmanagementservice.md) que la implementación admite sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="2417d-224">Specifies the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) methods that are supported synchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2417d-225">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2417d-225">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

<span data-ttu-id="2417d-226">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span><span class="sxs-lookup"><span data-stu-id="2417d-226">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="2417d-227">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span><span class="sxs-lookup"><span data-stu-id="2417d-227">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

<span data-ttu-id="2417d-228">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span><span class="sxs-lookup"><span data-stu-id="2417d-228">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

<span data-ttu-id="2417d-229">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span><span class="sxs-lookup"><span data-stu-id="2417d-229">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span></span>


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="2417d-230">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span><span class="sxs-lookup"><span data-stu-id="2417d-230">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

<span data-ttu-id="2417d-231">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span><span class="sxs-lookup"><span data-stu-id="2417d-231">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

<span data-ttu-id="2417d-232">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span><span class="sxs-lookup"><span data-stu-id="2417d-232">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

<span data-ttu-id="2417d-233">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span><span class="sxs-lookup"><span data-stu-id="2417d-233">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

<span data-ttu-id="2417d-234">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span><span class="sxs-lookup"><span data-stu-id="2417d-234">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

<span data-ttu-id="2417d-235">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span><span class="sxs-lookup"><span data-stu-id="2417d-235">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

<span data-ttu-id="2417d-236">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span><span class="sxs-lookup"><span data-stu-id="2417d-236">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

<span data-ttu-id="2417d-237">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span><span class="sxs-lookup"><span data-stu-id="2417d-237">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

<span data-ttu-id="2417d-238">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span><span class="sxs-lookup"><span data-stu-id="2417d-238">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

<span data-ttu-id="2417d-239">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span><span class="sxs-lookup"><span data-stu-id="2417d-239">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

<span data-ttu-id="2417d-240">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span><span class="sxs-lookup"><span data-stu-id="2417d-240">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

<span data-ttu-id="2417d-241">**RequestStateChangeSupported** (32789)</span><span class="sxs-lookup"><span data-stu-id="2417d-241">**RequestStateChangeSupported** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

<span data-ttu-id="2417d-242">**StartServiceSupported** (32790)</span><span class="sxs-lookup"><span data-stu-id="2417d-242">**StartServiceSupported** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

<span data-ttu-id="2417d-243">**StopServiceSupported** (32791)</span><span class="sxs-lookup"><span data-stu-id="2417d-243">**StopServiceSupported** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

<span data-ttu-id="2417d-244">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span><span class="sxs-lookup"><span data-stu-id="2417d-244">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span></span>


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

<span data-ttu-id="2417d-245">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span><span class="sxs-lookup"><span data-stu-id="2417d-245">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

<span data-ttu-id="2417d-246">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span><span class="sxs-lookup"><span data-stu-id="2417d-246">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

<span data-ttu-id="2417d-247">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span><span class="sxs-lookup"><span data-stu-id="2417d-247">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span></span>


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

<span data-ttu-id="2417d-248">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span><span class="sxs-lookup"><span data-stu-id="2417d-248">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

<span data-ttu-id="2417d-249">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span><span class="sxs-lookup"><span data-stu-id="2417d-249">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span></span>


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

<span data-ttu-id="2417d-250">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span><span class="sxs-lookup"><span data-stu-id="2417d-250">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2417d-251">**Proveedor reservado** (32799.. 65535)</span><span class="sxs-lookup"><span data-stu-id="2417d-251">**Vendor Reserved** (32799..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2417d-252">**VirtualSystemTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="2417d-252">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2417d-253">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2417d-253">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2417d-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2417d-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2417d-255">Una matriz de cadenas que designa un tipo de sistema virtual que admite la implementación.</span><span class="sxs-lookup"><span data-stu-id="2417d-255">An array of strings each designating a type of virtual system that the implementation supports.</span></span> <span data-ttu-id="2417d-256">El valor de cada elemento de matriz no **null** debe ajustarse a las cadenas definidas para la propiedad [**MSVM \_ VirtualSystemSettingData. VirtualSystemType**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="2417d-256">The value of each non-**NULL** array element must conform to the strings defined for the [**Msvm\_VirtualSystemSettingData.VirtualSystemType**](msvm-virtualsystemsettingdata.md) property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2417d-257">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2417d-257">Requirements</span></span>



| <span data-ttu-id="2417d-258">Requisito</span><span class="sxs-lookup"><span data-stu-id="2417d-258">Requirement</span></span> | <span data-ttu-id="2417d-259">Value</span><span class="sxs-lookup"><span data-stu-id="2417d-259">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2417d-260">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2417d-260">Minimum supported client</span></span><br/> | <span data-ttu-id="2417d-261">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2417d-261">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2417d-262">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2417d-262">Minimum supported server</span></span><br/> | <span data-ttu-id="2417d-263">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="2417d-263">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2417d-264">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2417d-264">Namespace</span></span><br/>                | <span data-ttu-id="2417d-265">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2417d-265">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2417d-266">MOF</span><span class="sxs-lookup"><span data-stu-id="2417d-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2417d-267"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2417d-267"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2417d-268">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2417d-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2417d-269"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2417d-269"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

