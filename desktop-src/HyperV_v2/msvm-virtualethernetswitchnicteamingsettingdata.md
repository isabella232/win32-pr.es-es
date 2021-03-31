---
description: Representa la configuración de formación de equipos NIC del conmutador.
ms.assetid: 7a48bdae-1953-4011-aaa8-1e3ca73494ff
title: Msvm_VirtualEthernetSwitchNicTeamingSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingSettingData
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.TeamingMode
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.LoadBalancingAlgorithm
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 45f306f9ddb388ef4e8124d7ab2c8dd125a62e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819491"
---
# <a name="msvm_virtualethernetswitchnicteamingsettingdata-class"></a><span data-ttu-id="e7120-103">MSVM \_ VirtualEthernetSwitchNicTeamingSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="e7120-103">Msvm\_VirtualEthernetSwitchNicTeamingSettingData class</span></span>

<span data-ttu-id="e7120-104">Representa la configuración de formación de equipos NIC del conmutador.</span><span class="sxs-lookup"><span data-stu-id="e7120-104">Represents the switch nic teaming settings.</span></span>

<span data-ttu-id="e7120-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e7120-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7120-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7120-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("17AD26F1-DD6F-4ED9-BD2F-3750ADE6B68B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Nic Teaming Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  UINT32 TeamingMode = 0;
  UINT32 LoadBalancingAlgorithm = 5;
};
```

## <a name="members"></a><span data-ttu-id="e7120-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e7120-107">Members</span></span>

<span data-ttu-id="e7120-108">La clase **MSVM \_ VirtualEthernetSwitchNicTeamingSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e7120-108">The **Msvm\_VirtualEthernetSwitchNicTeamingSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e7120-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7120-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7120-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7120-110">Properties</span></span>

<span data-ttu-id="e7120-111">La clase **MSVM \_ VirtualEthernetSwitchNicTeamingSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e7120-111">The **Msvm\_VirtualEthernetSwitchNicTeamingSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7120-112">**LoadBalancingAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="e7120-112">**LoadBalancingAlgorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7120-113">Tipo de datos: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="e7120-113">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="e7120-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e7120-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7120-115">Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e7120-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e7120-116">Algoritmo de equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="e7120-116">The load balancing algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="e7120-117">**TeamingMode**</span><span class="sxs-lookup"><span data-stu-id="e7120-117">**TeamingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7120-118">Tipo de datos: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="e7120-118">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="e7120-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e7120-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e7120-120">Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="e7120-120">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="e7120-121">Modo de formación de equipos.</span><span class="sxs-lookup"><span data-stu-id="e7120-121">The teaming mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7120-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7120-122">Requirements</span></span>



| <span data-ttu-id="e7120-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7120-123">Requirement</span></span> | <span data-ttu-id="e7120-124">Value</span><span class="sxs-lookup"><span data-stu-id="e7120-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7120-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7120-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e7120-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7120-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e7120-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7120-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e7120-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e7120-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e7120-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e7120-129">Namespace</span></span><br/>                | <span data-ttu-id="e7120-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e7120-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e7120-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e7120-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7120-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7120-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7120-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e7120-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7120-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e7120-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e7120-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7120-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7120-136">**MSVM \_ EthernetSwitchFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="e7120-136">**Msvm\_EthernetSwitchFeatureSettingData**</span></span>](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




