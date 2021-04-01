---
description: Representa los datos de configuración del dominio de enrutamiento.
ms.assetid: 6216cc4e-b2aa-4344-b8fa-489b986c14be
title: Msvm_EthernetSwitchPortRoutingDomainSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRoutingDomainSettingData
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainGuid
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainName
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdList
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdNameList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 40e16a3c952e63ab89c345201742dafe24cdde7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913889"
---
# <a name="msvm_ethernetswitchportroutingdomainsettingdata-class"></a><span data-ttu-id="25af0-103">MSVM \_ EthernetSwitchPortRoutingDomainSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="25af0-103">Msvm\_EthernetSwitchPortRoutingDomainSettingData class</span></span>

<span data-ttu-id="25af0-104">Representa los datos de configuración del dominio de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="25af0-104">Represents the routing domain setting data.</span></span>

<span data-ttu-id="25af0-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="25af0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="25af0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25af0-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("BF874DF0-F729-4312-A0FA-194271B88990"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Routing Domain Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRoutingDomainSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string RoutingDomainGuid = "";
  string RoutingDomainName = "";
  uint32 IsolationIdList[] = {};
  string IsolationIdNameList[] = {};
};
```

## <a name="members"></a><span data-ttu-id="25af0-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="25af0-107">Members</span></span>

<span data-ttu-id="25af0-108">La clase **MSVM \_ EthernetSwitchPortRoutingDomainSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="25af0-108">The **Msvm\_EthernetSwitchPortRoutingDomainSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="25af0-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25af0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="25af0-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25af0-110">Properties</span></span>

<span data-ttu-id="25af0-111">La clase **MSVM \_ EthernetSwitchPortRoutingDomainSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="25af0-111">The **Msvm\_EthernetSwitchPortRoutingDomainSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25af0-112">**IsolationIdList**</span><span class="sxs-lookup"><span data-stu-id="25af0-112">**IsolationIdList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25af0-113">Tipo de datos: **UInt32** array</span><span class="sxs-lookup"><span data-stu-id="25af0-113">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="25af0-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="25af0-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25af0-115">Calificadores: **WmiDataId** (3), [**versión**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisión**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="25af0-115">Qualifiers: **WmiDataId** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="25af0-116">Los identificadores de VirtualSubnetId o VLAN para los dominios de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="25af0-116">The VirtualSubnetId or VLAN IDs for the routing domains.</span></span>

</dd> <dt>

<span data-ttu-id="25af0-117">**IsolationIdNameList**</span><span class="sxs-lookup"><span data-stu-id="25af0-117">**IsolationIdNameList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25af0-118">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="25af0-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="25af0-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="25af0-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25af0-120">Calificadores: **WmiDataId** (4), [**versión**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisión**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="25af0-120">Qualifiers: **WmiDataId** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="25af0-121">La matriz de nombres descriptivos de VirtualSubnetId o VLAN.</span><span class="sxs-lookup"><span data-stu-id="25af0-121">The VirtualSubnetId or VLAN friendly name array.</span></span>

</dd> <dt>

<span data-ttu-id="25af0-122">**RoutingDomainGuid**</span><span class="sxs-lookup"><span data-stu-id="25af0-122">**RoutingDomainGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25af0-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25af0-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25af0-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="25af0-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25af0-125">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**versión**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisión**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="25af0-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="25af0-126">GUID del dominio de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="25af0-126">The routing domain GUID.</span></span>

</dd> <dt>

<span data-ttu-id="25af0-127">**RoutingDomainName**</span><span class="sxs-lookup"><span data-stu-id="25af0-127">**RoutingDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25af0-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25af0-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25af0-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="25af0-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25af0-130">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**versión**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisión**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="25af0-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="25af0-131">Nombre descriptivo del dominio de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="25af0-131">The routing domain friendly name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25af0-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25af0-132">Requirements</span></span>



| <span data-ttu-id="25af0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="25af0-133">Requirement</span></span> | <span data-ttu-id="25af0-134">Value</span><span class="sxs-lookup"><span data-stu-id="25af0-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25af0-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25af0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="25af0-136">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="25af0-136">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="25af0-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25af0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="25af0-138">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="25af0-138">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="25af0-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="25af0-139">Namespace</span></span><br/>                | <span data-ttu-id="25af0-140">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="25af0-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="25af0-141">MOF</span><span class="sxs-lookup"><span data-stu-id="25af0-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25af0-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25af0-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="25af0-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="25af0-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25af0-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="25af0-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="25af0-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="25af0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25af0-146">**MSVM \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="25af0-146">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

