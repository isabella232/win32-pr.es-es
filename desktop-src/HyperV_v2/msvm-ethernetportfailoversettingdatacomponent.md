---
description: Asociación que se usa para establecer relaciones entre una instancia de un \_ EmulatedEthernetPortSettingData de MSVM y una o más instancias de una MSVM \_ EthernetSwitchFeatureSettingData.
ms.assetid: A2929D81-ED86-4C5A-9280-276204EDE89B
title: Msvm_EthernetPortFailoverSettingDataComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortFailoverSettingDataComponent
- Msvm_EthernetPortFailoverSettingDataComponent.GroupComponent
- Msvm_EthernetPortFailoverSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 50fff8688beea91495014dd75b1f1c33020869f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545702"
---
# <a name="msvm_ethernetportfailoversettingdatacomponent-class"></a><span data-ttu-id="b1e5b-103">MSVM \_ EthernetPortFailoverSettingDataComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="b1e5b-103">Msvm\_EthernetPortFailoverSettingDataComponent class</span></span>

<span data-ttu-id="b1e5b-104">Asociación que se usa para establecer relaciones entre una instancia de [**un \_ EmulatedEthernetPortSettingData de MSVM**](msvm-emulatedethernetportsettingdata.md) y una o más instancias de una [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="b1e5b-104">An association used to establish relationships between one instance of an [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) and one or more instances of an [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="b1e5b-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1e5b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1e5b-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortFailoverSettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData      REF GroupComponent;
  Msvm_FailoverNetworkAdapterSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="b1e5b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b1e5b-107">Members</span></span>

<span data-ttu-id="b1e5b-108">La clase **MSVM \_ EthernetPortFailoverSettingDataComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b1e5b-108">The **Msvm\_EthernetPortFailoverSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="b1e5b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b1e5b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1e5b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b1e5b-110">Properties</span></span>

<span data-ttu-id="b1e5b-111">La clase **MSVM \_ EthernetPortFailoverSettingDataComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-111">The **Msvm\_EthernetPortFailoverSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1e5b-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b1e5b-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e5b-113">Tipo de datos: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="b1e5b-113">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="b1e5b-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1e5b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1e5b-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agregado**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b1e5b-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b1e5b-116">Una referencia a una instancia de la clase [**MSVM \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) o [**MSVM \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) que representa el puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-116">A reference to an instance of the [**Msvm\_EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) or [**Msvm\_SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) class that represents the Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="b1e5b-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b1e5b-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e5b-118">Tipo de datos: **[ **MSVM \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="b1e5b-118">Data type: **[**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b1e5b-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1e5b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1e5b-120">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="b1e5b-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="b1e5b-121">Referencia a una instancia de la clase [**MSVM \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) que representa la configuración del adaptador de red invitado.</span><span class="sxs-lookup"><span data-stu-id="b1e5b-121">A reference to an instance of the [**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) class that represents the guest network adapter configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1e5b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1e5b-122">Requirements</span></span>



| <span data-ttu-id="b1e5b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1e5b-123">Requirement</span></span> | <span data-ttu-id="b1e5b-124">Value</span><span class="sxs-lookup"><span data-stu-id="b1e5b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e5b-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1e5b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b1e5b-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1e5b-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b1e5b-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1e5b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b1e5b-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1e5b-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b1e5b-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b1e5b-129">Namespace</span></span><br/>                | <span data-ttu-id="b1e5b-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b1e5b-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b1e5b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b1e5b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1e5b-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1e5b-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1e5b-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b1e5b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1e5b-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b1e5b-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

