---
description: Asociación que se usa para establecer &\# 0034; parte de&\# 0034; relaciones entre una instancia de MSVM \_ VirtualEthernetSwitchSettingData y una o varias instancias de MSVM \_ EthernetSwitchFeatureSettingData.
ms.assetid: b3adac33-056e-4f39-8022-5d9ef78370e9
title: Msvm_VirtualEthernetSwitchSettingDataComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingDataComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.GroupComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8fa53514c5db3128e13f0504bb883cb802021c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276174"
---
# <a name="msvm_virtualethernetswitchsettingdatacomponent-class"></a><span data-ttu-id="ed684-103">MSVM \_ VirtualEthernetSwitchSettingDataComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="ed684-103">Msvm\_VirtualEthernetSwitchSettingDataComponent class</span></span>

<span data-ttu-id="ed684-104">Asociación que se usa para establecer las relaciones entre una instancia de [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) y una o varias instancias de [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="ed684-104">An association used to establish "part of" relationships between one instance of [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) and one or more instances of [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="ed684-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ed684-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed684-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed684-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingDataComponent : CIM_Component
{
  Msvm_VirtualEthernetSwitchSettingData REF GroupComponent;
  Msvm_EthernetSwitchFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="ed684-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ed684-107">Members</span></span>

<span data-ttu-id="ed684-108">La clase **MSVM \_ VirtualEthernetSwitchSettingDataComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ed684-108">The **Msvm\_VirtualEthernetSwitchSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="ed684-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ed684-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed684-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ed684-110">Properties</span></span>

<span data-ttu-id="ed684-111">La clase **MSVM \_ VirtualEthernetSwitchSettingDataComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ed684-111">The **Msvm\_VirtualEthernetSwitchSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed684-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="ed684-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed684-113">Tipo de datos: **MSVM \_ VirtualEthernetSwitchSettingData**</span><span class="sxs-lookup"><span data-stu-id="ed684-113">Data type: **Msvm\_VirtualEthernetSwitchSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="ed684-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed684-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed684-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agregado**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ed684-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ed684-116">Referencia a una instancia de la clase [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) que representa un puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="ed684-116">Reference to an instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that represents an Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="ed684-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="ed684-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed684-118">Tipo de datos: **MSVM \_ EthernetSwitchFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="ed684-118">Data type: **Msvm\_EthernetSwitchFeatureSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="ed684-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed684-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed684-120">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="ed684-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="ed684-121">Referencia a una instancia de la clase [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) que representa la configuración aplicada al modificador.</span><span class="sxs-lookup"><span data-stu-id="ed684-121">Reference to an instance of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class that represents the settings applied to the switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed684-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed684-122">Requirements</span></span>



| <span data-ttu-id="ed684-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed684-123">Requirement</span></span> | <span data-ttu-id="ed684-124">Value</span><span class="sxs-lookup"><span data-stu-id="ed684-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed684-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed684-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ed684-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed684-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ed684-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed684-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ed684-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed684-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed684-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ed684-129">Namespace</span></span><br/>                | <span data-ttu-id="ed684-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ed684-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ed684-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ed684-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed684-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed684-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed684-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed684-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed684-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ed684-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

