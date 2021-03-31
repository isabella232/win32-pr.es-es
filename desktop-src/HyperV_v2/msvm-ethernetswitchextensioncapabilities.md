---
description: Representa la asociación entre las extensiones Ethernet y sus capacidades.
ms.assetid: 6b32235a-175d-48f9-af3a-2d40f748a518
title: Msvm_EthernetSwitchExtensionCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtensionCapabilities
- Msvm_EthernetSwitchExtensionCapabilities.ManagedElement
- Msvm_EthernetSwitchExtensionCapabilities.Capabilities
- Msvm_EthernetSwitchExtensionCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 950a8a0288487bf557e9dd201100b2a894417641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819499"
---
# <a name="msvm_ethernetswitchextensioncapabilities-class"></a><span data-ttu-id="31598-103">MSVM \_ EthernetSwitchExtensionCapabilities (clase)</span><span class="sxs-lookup"><span data-stu-id="31598-103">Msvm\_EthernetSwitchExtensionCapabilities class</span></span>

<span data-ttu-id="31598-104">Representa la asociación entre las extensiones Ethernet y sus capacidades.</span><span class="sxs-lookup"><span data-stu-id="31598-104">Represents the association between Ethernet extensions and their capabilities.</span></span>

<span data-ttu-id="31598-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="31598-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="31598-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31598-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtensionCapabilities : CIM_ElementCapabilities
{
  Msvm_InstalledEthernetSwitchExtension  REF ManagedElement;
  Msvm_EthernetSwitchFeatureCapabilities REF Capabilities;
  uint16                                     Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="31598-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="31598-107">Members</span></span>

<span data-ttu-id="31598-108">La clase **MSVM \_ EthernetSwitchExtensionCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="31598-108">The **Msvm\_EthernetSwitchExtensionCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="31598-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31598-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31598-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31598-110">Properties</span></span>

<span data-ttu-id="31598-111">La clase **MSVM \_ EthernetSwitchExtensionCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="31598-111">The **Msvm\_EthernetSwitchExtensionCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31598-112">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="31598-112">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31598-113">Tipo de datos: **[ **MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="31598-113">Data type: **[**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span></span>
</dt> <dt>

<span data-ttu-id="31598-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="31598-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31598-115">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("capacidades")</span><span class="sxs-lookup"><span data-stu-id="31598-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="31598-116">Referencia a una instancia de la clase [**MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) que representa el objeto Capabilities asociado al modificador.</span><span class="sxs-lookup"><span data-stu-id="31598-116">A reference to an instance of the [**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) class that represents the capabilities object associated with the switch.</span></span> <span data-ttu-id="31598-117">Esta propiedad se hereda de [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="31598-117">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="31598-118">**Características**</span><span class="sxs-lookup"><span data-stu-id="31598-118">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31598-119">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31598-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="31598-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="31598-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31598-121">Proporciona información descriptiva acerca de las capacidades de.</span><span class="sxs-lookup"><span data-stu-id="31598-121">Provides descriptive information about the capabilities.</span></span> <span data-ttu-id="31598-122">Esta propiedad se hereda de [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="31598-122">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>



| <span data-ttu-id="31598-123">Value</span><span class="sxs-lookup"><span data-stu-id="31598-123">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="31598-124">Significado</span><span class="sxs-lookup"><span data-stu-id="31598-124">Meaning</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="31598-125"><dt>**Valor predeterminado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="31598-125"><dt>**Default**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="31598-126">Las capacidades asociadas representan las funciones predeterminadas del elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="31598-126">The associated capabilities represent the default capabilities of the managed element.</span></span><br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <span data-ttu-id="31598-127"><dt>**Actual**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="31598-127"><dt>**Current**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="31598-128">Las capacidades asociadas representan las capacidades actuales del elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="31598-128">The associated capabilities represent the current capabilities of the managed element.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="31598-129">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="31598-129">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31598-130">Tipo de datos: **[ **MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="31598-130">Data type: **[**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="31598-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="31598-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31598-132">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ManagedElement")</span><span class="sxs-lookup"><span data-stu-id="31598-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ManagedElement")</span></span>
</dt> </dl>

<span data-ttu-id="31598-133">Referencia a una instancia de la clase [**MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) que representa la extensión instalada.</span><span class="sxs-lookup"><span data-stu-id="31598-133">A reference to an instance of the [**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) class that represents the installed extension.</span></span> <span data-ttu-id="31598-134">Esta propiedad se hereda de [**\_ ElementCapabilities CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span><span class="sxs-lookup"><span data-stu-id="31598-134">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31598-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31598-135">Requirements</span></span>



| <span data-ttu-id="31598-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="31598-136">Requirement</span></span> | <span data-ttu-id="31598-137">Value</span><span class="sxs-lookup"><span data-stu-id="31598-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31598-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31598-138">Minimum supported client</span></span><br/> | <span data-ttu-id="31598-139">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="31598-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="31598-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31598-140">Minimum supported server</span></span><br/> | <span data-ttu-id="31598-141">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="31598-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31598-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="31598-142">Namespace</span></span><br/>                | <span data-ttu-id="31598-143">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="31598-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="31598-144">MOF</span><span class="sxs-lookup"><span data-stu-id="31598-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31598-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31598-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="31598-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="31598-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31598-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="31598-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

