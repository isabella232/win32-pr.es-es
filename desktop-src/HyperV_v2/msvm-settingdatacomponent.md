---
description: Establezca una relación entre una instancia de la \_ clase MSVM EmulatedEthernetPortSettingData o MSVM \_ SyntheticEthernetPortSettingData con una instancia de la \_ clase MSVM GuestNetworkAdapterConfiguration.
ms.assetid: 82262e67-1e72-4bad-974e-f18d00a94c3d
title: Msvm_SettingDataComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingDataComponent
- Msvm_SettingDataComponent.GroupComponent
- Msvm_SettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18ed2d4f37b88509a7517861a9b9d842be86bd97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002284"
---
# <a name="msvm_settingdatacomponent-class"></a><span data-ttu-id="4e4c9-103">MSVM \_ SettingDataComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="4e4c9-103">Msvm\_SettingDataComponent class</span></span>

<span data-ttu-id="4e4c9-104">Establezca una relación entre una instancia de la clase [**MSVM \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) o [**MSVM \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) con una instancia de la clase [**MSVM \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="4e4c9-104">Establish a relationship between an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class with an instance of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class.</span></span>

<span data-ttu-id="4e4c9-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4e4c9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e4c9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e4c9-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData     REF GroupComponent;
  Msvm_GuestNetworkAdapterConfiguration REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="4e4c9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4e4c9-107">Members</span></span>

<span data-ttu-id="4e4c9-108">La clase **MSVM \_ SettingDataComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4e4c9-108">The **Msvm\_SettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="4e4c9-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4e4c9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e4c9-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4e4c9-110">Properties</span></span>

<span data-ttu-id="4e4c9-111">La clase **MSVM \_ SettingDataComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4e4c9-111">The **Msvm\_SettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e4c9-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4e4c9-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e4c9-113">Tipo de datos: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="4e4c9-113">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="4e4c9-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e4c9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e4c9-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agregado**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4e4c9-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4e4c9-116">Una referencia a una instancia de la clase [**MSVM \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) o [**MSVM \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) que representa un puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="4e4c9-116">A reference to an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class that represents an Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="4e4c9-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4e4c9-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e4c9-118">Tipo de datos: **[ **MSVM \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)**</span><span class="sxs-lookup"><span data-stu-id="4e4c9-118">Data type: **[**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4e4c9-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e4c9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e4c9-120">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="4e4c9-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4e4c9-121">Una referencia a una instancia de la clase [**MSVM \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) que representa una configuración de adaptador de red invitado.</span><span class="sxs-lookup"><span data-stu-id="4e4c9-121">A reference to an instance of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class that represents a guest network adapter configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e4c9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e4c9-122">Requirements</span></span>



| <span data-ttu-id="4e4c9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e4c9-123">Requirement</span></span> | <span data-ttu-id="4e4c9-124">Value</span><span class="sxs-lookup"><span data-stu-id="4e4c9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e4c9-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e4c9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4e4c9-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e4c9-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4e4c9-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e4c9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4e4c9-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e4c9-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4e4c9-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4e4c9-129">Namespace</span></span><br/>                | <span data-ttu-id="4e4c9-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4e4c9-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4e4c9-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4e4c9-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e4c9-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e4c9-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e4c9-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e4c9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e4c9-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4e4c9-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

