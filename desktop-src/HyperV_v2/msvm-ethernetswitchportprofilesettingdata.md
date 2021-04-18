---
description: Representa la configuración del perfil de puerto.
ms.assetid: 43ddb0a3-8621-4993-b0a9-8ddcfb0eaad5
title: Msvm_EthernetSwitchPortProfileSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortProfileSettingData
- Msvm_EthernetSwitchPortProfileSettingData.InstanceID
- Msvm_EthernetSwitchPortProfileSettingData.Caption
- Msvm_EthernetSwitchPortProfileSettingData.Description
- Msvm_EthernetSwitchPortProfileSettingData.ElementName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileId
- Msvm_EthernetSwitchPortProfileSettingData.VendorName
- Msvm_EthernetSwitchPortProfileSettingData.VendorId
- Msvm_EthernetSwitchPortProfileSettingData.ProfileData
- Msvm_EthernetSwitchPortProfileSettingData.NetCfgInstanceId
- Msvm_EthernetSwitchPortProfileSettingData.PciSegmentNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciBusNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciDeviceNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciFunctionNumber
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelId
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelString
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 611fd40b14b961369a847d6bb7b7746ceec2bb85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689580"
---
# <a name="msvm_ethernetswitchportprofilesettingdata-class"></a><span data-ttu-id="37ae2-103">MSVM \_ EthernetSwitchPortProfileSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="37ae2-103">Msvm\_EthernetSwitchPortProfileSettingData class</span></span>

<span data-ttu-id="37ae2-104">Representa la configuración del perfil de puerto.</span><span class="sxs-lookup"><span data-stu-id="37ae2-104">Represents the port profile settings.</span></span>

<span data-ttu-id="37ae2-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="37ae2-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ae2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37ae2-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("9940CD46-8B06-43BB-B9D5-93D50381FD56"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Profile Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortProfileSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Profile Settings";
  string Description = "Represents the port profile settings.";
  string ElementName = "Ethernet Switch Port Profile Settings";
  string ProfileName = "";
  string ProfileId = "";
  string VendorName = "";
  string VendorId = 00000000-0000-0000-0000-000000000000}";
  uint32 ProfileData = 0;
  string NetCfgInstanceId = 00000000-0000-0000-0000-000000000000}";
  uint32 PciSegmentNumber = 0;
  uint32 PciBusNumber = 0;
  uint32 PciDeviceNumber = 0;
  uint32 PciFunctionNumber = 0;
  uint32 CdnLabelId = 0;
  string CdnLabelString = 0;
};
```

## <a name="members"></a><span data-ttu-id="37ae2-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="37ae2-107">Members</span></span>

<span data-ttu-id="37ae2-108">La clase **MSVM \_ EthernetSwitchPortProfileSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="37ae2-108">The **Msvm\_EthernetSwitchPortProfileSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="37ae2-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="37ae2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37ae2-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="37ae2-110">Properties</span></span>

<span data-ttu-id="37ae2-111">La clase **MSVM \_ EthernetSwitchPortProfileSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="37ae2-111">The **Msvm\_EthernetSwitchPortProfileSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37ae2-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="37ae2-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37ae2-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37ae2-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="37ae2-115">A short description of the object.</span></span> <span data-ttu-id="37ae2-116">Esta propiedad se hereda de [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración de Perfil de puerto de conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="37ae2-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Profile Settings".</span></span>

</dd> <dt>

<span data-ttu-id="37ae2-117">**CdnLabelId**</span><span class="sxs-lookup"><span data-stu-id="37ae2-117">**CdnLabelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-118">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37ae2-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="37ae2-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-120">Calificadores: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="37ae2-120">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-121">Identificador de la etiqueta de la red CDN.</span><span class="sxs-lookup"><span data-stu-id="37ae2-121">The CDN label identifier.</span></span>

</dd> <dt>

<span data-ttu-id="37ae2-122">**CdnLabelString**</span><span class="sxs-lookup"><span data-stu-id="37ae2-122">**CdnLabelString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37ae2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="37ae2-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-125">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (12), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="37ae2-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (12), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-126">Cadena de la etiqueta de la red CDN.</span><span class="sxs-lookup"><span data-stu-id="37ae2-126">The CDN label string.</span></span>

</dd> <dt>

<span data-ttu-id="37ae2-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37ae2-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37ae2-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37ae2-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-130">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="37ae2-130">A description of the object.</span></span> <span data-ttu-id="37ae2-131">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "representa la configuración del perfil de puerto".</span><span class="sxs-lookup"><span data-stu-id="37ae2-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port profile settings.".</span></span>

</dd> <dt>

<span data-ttu-id="37ae2-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="37ae2-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37ae2-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37ae2-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-135">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="37ae2-135">A display name for the object.</span></span> <span data-ttu-id="37ae2-136">Esta propiedad se hereda de [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración de Perfil de puerto de conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="37ae2-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Profile Settings".</span></span>

</dd> <dt>

<span data-ttu-id="37ae2-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="37ae2-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37ae2-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37ae2-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-140">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="37ae2-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-141">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="37ae2-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="37ae2-142">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="37ae2-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="37ae2-143">**NetCfgInstanceId**</span><span class="sxs-lookup"><span data-stu-id="37ae2-143">**NetCfgInstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37ae2-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="37ae2-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-146">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="37ae2-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-147">Identificador único del dispositivo de la subinterfaz.</span><span class="sxs-lookup"><span data-stu-id="37ae2-147">An unique device identifier of the subinterface.</span></span>

</dd> <dt>

<span data-ttu-id="37ae2-148">**PciBusNumber**</span><span class="sxs-lookup"><span data-stu-id="37ae2-148">**PciBusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37ae2-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="37ae2-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-151">Calificadores: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="37ae2-151">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-152">Número de bus PCI.</span><span class="sxs-lookup"><span data-stu-id="37ae2-152">The PCI bus number.</span></span>

</dd> <dt>

<span data-ttu-id="37ae2-153">**PciDeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="37ae2-153">**PciDeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-154">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37ae2-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-155">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="37ae2-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-156">Calificadores: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="37ae2-156">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-157">El número de dispositivo PCI.</span><span class="sxs-lookup"><span data-stu-id="37ae2-157">The PCI device number.</span></span>

</dd> <dt>

<span data-ttu-id="37ae2-158">**PciFunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="37ae2-158">**PciFunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-159">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37ae2-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="37ae2-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-161">Calificadores: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="37ae2-161">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-162">Número de función PCI.</span><span class="sxs-lookup"><span data-stu-id="37ae2-162">The PCI function number.</span></span>

</dd> <dt>

<span data-ttu-id="37ae2-163">**PciSegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="37ae2-163">**PciSegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-164">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37ae2-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="37ae2-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-166">Calificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="37ae2-166">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-167">Número de segmento PCI.</span><span class="sxs-lookup"><span data-stu-id="37ae2-167">The PCI segment number.</span></span>

</dd> <dt>

<span data-ttu-id="37ae2-168">**ProfileData**</span><span class="sxs-lookup"><span data-stu-id="37ae2-168">**ProfileData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-169">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37ae2-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-170">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="37ae2-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-171">Calificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="37ae2-171">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-172">Datos adicionales para el perfil de puerto.</span><span class="sxs-lookup"><span data-stu-id="37ae2-172">Additional data for the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="37ae2-173">**ProfileId**</span><span class="sxs-lookup"><span data-stu-id="37ae2-173">**ProfileId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37ae2-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="37ae2-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-176">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="37ae2-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-177">Identificador del perfil de puerto.</span><span class="sxs-lookup"><span data-stu-id="37ae2-177">The identifier of the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="37ae2-178">**ProfileName**</span><span class="sxs-lookup"><span data-stu-id="37ae2-178">**ProfileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37ae2-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-180">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="37ae2-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-181">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="37ae2-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-182">Nombre del perfil de puerto.</span><span class="sxs-lookup"><span data-stu-id="37ae2-182">The name of the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="37ae2-183">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="37ae2-183">**VendorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37ae2-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-185">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="37ae2-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-186">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="37ae2-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-187">Identificador del proveedor que define el perfil.</span><span class="sxs-lookup"><span data-stu-id="37ae2-187">The identifier of the vendor defining the profile.</span></span>

</dd> <dt>

<span data-ttu-id="37ae2-188">**VendorName**</span><span class="sxs-lookup"><span data-stu-id="37ae2-188">**VendorName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37ae2-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37ae2-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="37ae2-190">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="37ae2-191">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="37ae2-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="37ae2-192">Nombre del proveedor que define el perfil.</span><span class="sxs-lookup"><span data-stu-id="37ae2-192">The name of the vendor defining the profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37ae2-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37ae2-193">Requirements</span></span>



| <span data-ttu-id="37ae2-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="37ae2-194">Requirement</span></span> | <span data-ttu-id="37ae2-195">Value</span><span class="sxs-lookup"><span data-stu-id="37ae2-195">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37ae2-196">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37ae2-196">Minimum supported client</span></span><br/> | <span data-ttu-id="37ae2-197">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="37ae2-197">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="37ae2-198">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37ae2-198">Minimum supported server</span></span><br/> | <span data-ttu-id="37ae2-199">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="37ae2-199">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37ae2-200">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="37ae2-200">Namespace</span></span><br/>                | <span data-ttu-id="37ae2-201">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="37ae2-201">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="37ae2-202">MOF</span><span class="sxs-lookup"><span data-stu-id="37ae2-202">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37ae2-203"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37ae2-203"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37ae2-204">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="37ae2-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37ae2-205"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37ae2-205"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

