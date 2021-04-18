---
description: Representa la configuración de ancho de banda para un conmutador virtual.
ms.assetid: bc6f8cd3-f74a-4f4a-9ffe-a88def3966d9
title: Msvm_VirtualEthernetSwitchBandwidthSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchBandwidthSettingData
- Msvm_VirtualEthernetSwitchBandwidthSettingData.InstanceID
- Msvm_VirtualEthernetSwitchBandwidthSettingData.Caption
- Msvm_VirtualEthernetSwitchBandwidthSettingData.Description
- Msvm_VirtualEthernetSwitchBandwidthSettingData.ElementName
- Msvm_VirtualEthernetSwitchBandwidthSettingData.DefaultFlowReservation
- Msvm_VirtualEthernetSwitchBandwidthSettingData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec94409366761ee208d3e8a6af59a4d07527d82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652843"
---
# <a name="msvm_virtualethernetswitchbandwidthsettingdata-class"></a><span data-ttu-id="5f1b2-103">MSVM \_ VirtualEthernetSwitchBandwidthSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="5f1b2-103">Msvm\_VirtualEthernetSwitchBandwidthSettingData class</span></span>

<span data-ttu-id="5f1b2-104">Representa la configuración de ancho de banda para un conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="5f1b2-104">Represents the bandwidth settings for a virtual switch.</span></span>

<span data-ttu-id="5f1b2-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5f1b2-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f1b2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f1b2-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("3EB2B8E8-4ABF-4DBF-9071-16DD47481FBE"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchBandwidthSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  string InstanceID = "Microsoft:Definition\GUID\Default";
  string Caption = "Ethernet Switch Bandwidth Settings";
  string Description = "Represents the switch bandwidth settings.";
  string ElementName = "Ethernet Switch Bandwidth Settings";
  UINT64 DefaultFlowReservation = 0;
  UINT64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="5f1b2-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5f1b2-107">Members</span></span>

<span data-ttu-id="5f1b2-108">La clase **MSVM \_ VirtualEthernetSwitchBandwidthSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5f1b2-108">The **Msvm\_VirtualEthernetSwitchBandwidthSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5f1b2-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5f1b2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f1b2-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5f1b2-110">Properties</span></span>

<span data-ttu-id="5f1b2-111">La clase **MSVM \_ VirtualEthernetSwitchBandwidthSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5f1b2-111">The **Msvm\_VirtualEthernetSwitchBandwidthSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f1b2-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5f1b2-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f1b2-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5f1b2-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f1b2-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5f1b2-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f1b2-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="5f1b2-115">A short description of the object.</span></span> <span data-ttu-id="5f1b2-116">Esta propiedad se hereda de la clase [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) y siempre se establece en "configuración de ancho de banda del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="5f1b2-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Ethernet Switch Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="5f1b2-117">**DefaultFlowReservation**</span><span class="sxs-lookup"><span data-stu-id="5f1b2-117">**DefaultFlowReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f1b2-118">Tipo de datos: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="5f1b2-118">Data type: **UINT64**</span></span>
</dt> <dt>

<span data-ttu-id="5f1b2-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f1b2-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5f1b2-120">Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5f1b2-120">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5f1b2-121">Especifica la reserva de ancho de banda absoluta para los flujos no clasificados en el adaptador subyacente.</span><span class="sxs-lookup"><span data-stu-id="5f1b2-121">Specifies the absolute bandwidth reservation for unclassified flows on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5f1b2-122">**DefaultFlowWeight**</span><span class="sxs-lookup"><span data-stu-id="5f1b2-122">**DefaultFlowWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f1b2-123">Tipo de datos: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="5f1b2-123">Data type: **UINT64**</span></span>
</dt> <dt>

<span data-ttu-id="5f1b2-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f1b2-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5f1b2-125">Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5f1b2-125">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5f1b2-126">Especifica la reserva de ancho de banda en peso para los flujos no clasificados en el adaptador subyacente.</span><span class="sxs-lookup"><span data-stu-id="5f1b2-126">Specifies the bandwidth reservation in weight for unclassified flows on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5f1b2-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f1b2-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f1b2-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5f1b2-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f1b2-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5f1b2-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f1b2-130">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="5f1b2-130">A description of the object.</span></span> <span data-ttu-id="5f1b2-131">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "representa la configuración del ancho de banda del conmutador".</span><span class="sxs-lookup"><span data-stu-id="5f1b2-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the switch bandwidth settings.".</span></span>

</dd> <dt>

<span data-ttu-id="5f1b2-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5f1b2-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f1b2-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5f1b2-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f1b2-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5f1b2-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f1b2-135">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="5f1b2-135">A display name for the object.</span></span> <span data-ttu-id="5f1b2-136">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85))y siempre se establece en "configuración de ancho de banda del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="5f1b2-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Ethernet Switch Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="5f1b2-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5f1b2-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f1b2-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5f1b2-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f1b2-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5f1b2-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f1b2-140">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="5f1b2-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5f1b2-141">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="5f1b2-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5f1b2-142">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)) y siempre se establece en "Microsoft: \\ *GUID* de definición \\ default".</span><span class="sxs-lookup"><span data-stu-id="5f1b2-142">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:Definition\\*GUID*\\Default".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f1b2-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f1b2-143">Requirements</span></span>



| <span data-ttu-id="5f1b2-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f1b2-144">Requirement</span></span> | <span data-ttu-id="5f1b2-145">Value</span><span class="sxs-lookup"><span data-stu-id="5f1b2-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f1b2-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f1b2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5f1b2-147">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f1b2-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5f1b2-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f1b2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5f1b2-149">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f1b2-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5f1b2-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5f1b2-150">Namespace</span></span><br/>                | <span data-ttu-id="5f1b2-151">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="5f1b2-151">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5f1b2-152">MOF</span><span class="sxs-lookup"><span data-stu-id="5f1b2-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f1b2-153"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f1b2-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f1b2-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f1b2-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f1b2-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5f1b2-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

