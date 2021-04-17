---
description: Representa un servicio de conmutador.
ms.assetid: cf6319fa-7d69-4820-b0e0-775aad8b190c
title: CIM_SwitchService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchService
- CIM_SwitchService.BridgeAddress
- CIM_SwitchService.NumPorts
- CIM_SwitchService.BridgeType
- CIM_SwitchService.BridgeAddressType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9abe6869c5b8ac61630091315e476ae232630717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666914"
---
# <a name="cim_switchservice-class"></a><span data-ttu-id="27d49-103">\_Clase SwitchService de CIM</span><span class="sxs-lookup"><span data-stu-id="27d49-103">CIM\_SwitchService class</span></span>

<span data-ttu-id="27d49-104">Representa un servicio de conmutador.</span><span class="sxs-lookup"><span data-stu-id="27d49-104">Represents a switch service.</span></span>

## <a name="syntax"></a><span data-ttu-id="27d49-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27d49-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchService : CIM_ForwardingService
{
  string BridgeAddress;
  uint16 NumPorts;
  uint8  BridgeType;
  uint16 BridgeAddressType;
};
```

## <a name="members"></a><span data-ttu-id="27d49-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="27d49-106">Members</span></span>

<span data-ttu-id="27d49-107">La clase **CIM \_ SwitchService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="27d49-107">The **CIM\_SwitchService** class has these types of members:</span></span>

-   [<span data-ttu-id="27d49-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27d49-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27d49-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27d49-109">Properties</span></span>

<span data-ttu-id="27d49-110">La clase **CIM \_ SwitchService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="27d49-110">The **CIM\_SwitchService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="27d49-111">**BridgeAddress**</span><span class="sxs-lookup"><span data-stu-id="27d49-111">**BridgeAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d49-112">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="27d49-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27d49-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27d49-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27d49-114">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseBridgeAddress "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SwitchService**.**BridgeAddressType**")</span><span class="sxs-lookup"><span data-stu-id="27d49-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseBridgeAddress"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SwitchService**.**BridgeAddressType**")</span></span>
</dt> </dl>

<span data-ttu-id="27d49-115">La dirección del servicio del modificador, que es una parte del identificador único del servicio.</span><span class="sxs-lookup"><span data-stu-id="27d49-115">The address of the switch service, which is a portion of the unique identifier of the service.</span></span>

</dd> <dt>

<span data-ttu-id="27d49-116">**BridgeAddressType**</span><span class="sxs-lookup"><span data-stu-id="27d49-116">**BridgeAddressType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d49-117">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d49-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d49-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27d49-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27d49-119">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SwitchService**.**BridgeAddress**")</span><span class="sxs-lookup"><span data-stu-id="27d49-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SwitchService**.**BridgeAddress**")</span></span>
</dt> </dl>

<span data-ttu-id="27d49-120">El formato de direccionamiento usado para el puente y la propiedad **BridgeAddress** .</span><span class="sxs-lookup"><span data-stu-id="27d49-120">The addressing format used for the bridge and the **BridgeAddress** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="27d49-121">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="27d49-121">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="27d49-122">**IPv4** (2)</span><span class="sxs-lookup"><span data-stu-id="27d49-122">**IPv4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="27d49-123">**IPv6** (3)</span><span class="sxs-lookup"><span data-stu-id="27d49-123">**IPv6** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC"></span><span id="mac"></span>

<span data-ttu-id="27d49-124">**Mac** (4)</span><span class="sxs-lookup"><span data-stu-id="27d49-124">**MAC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC___Spanning_Tree_Priority"></span><span id="mac___spanning_tree_priority"></span><span id="MAC___SPANNING_TREE_PRIORITY"></span>

<span data-ttu-id="27d49-125">**Mac + prioridad del árbol de expansión** (5)</span><span class="sxs-lookup"><span data-stu-id="27d49-125">**MAC + Spanning Tree Priority** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="27d49-126">**BridgeType**</span><span class="sxs-lookup"><span data-stu-id="27d49-126">**BridgeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d49-127">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="27d49-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="27d49-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27d49-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27d49-129">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Puente IETF-MIB. dot1dBaseType ")</span><span class="sxs-lookup"><span data-stu-id="27d49-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseType")</span></span>
</dt> </dl>

<span data-ttu-id="27d49-130">Tipo de servicio de conmutación que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="27d49-130">The type of switching service to perform.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27d49-131">**Desconocido** (1)</span><span class="sxs-lookup"><span data-stu-id="27d49-131">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparent-only"></span><span id="transparent-only"></span><span id="TRANSPARENT-ONLY"></span>

<span data-ttu-id="27d49-132">**Solo transparente** (2)</span><span class="sxs-lookup"><span data-stu-id="27d49-132">**Transparent-only** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SourceRoute-only"></span><span id="sourceroute-only"></span><span id="SOURCEROUTE-ONLY"></span>

<span data-ttu-id="27d49-133">**Solo** 2 (3)</span><span class="sxs-lookup"><span data-stu-id="27d49-133">**SourceRoute-only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SRT"></span><span id="srt"></span>

<span data-ttu-id="27d49-134">**SRT** (4)</span><span class="sxs-lookup"><span data-stu-id="27d49-134">**SRT** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="27d49-135">**NumPorts**</span><span class="sxs-lookup"><span data-stu-id="27d49-135">**NumPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27d49-136">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27d49-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27d49-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27d49-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27d49-138">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Puente IETF-MIB. dot1dBaseNumPorts ")</span><span class="sxs-lookup"><span data-stu-id="27d49-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseNumPorts")</span></span>
</dt> </dl>

<span data-ttu-id="27d49-139">El número de puertos de conmutador controlados por este servicio de conmutación.</span><span class="sxs-lookup"><span data-stu-id="27d49-139">The number of switch ports controlled by this switching service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27d49-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27d49-140">Requirements</span></span>



| <span data-ttu-id="27d49-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="27d49-141">Requirement</span></span> | <span data-ttu-id="27d49-142">Value</span><span class="sxs-lookup"><span data-stu-id="27d49-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27d49-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27d49-143">Minimum supported client</span></span><br/> | <span data-ttu-id="27d49-144">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="27d49-144">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="27d49-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27d49-145">Minimum supported server</span></span><br/> | <span data-ttu-id="27d49-146">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="27d49-146">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="27d49-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="27d49-147">Namespace</span></span><br/>                | <span data-ttu-id="27d49-148">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="27d49-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="27d49-149">MOF</span><span class="sxs-lookup"><span data-stu-id="27d49-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27d49-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27d49-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="27d49-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="27d49-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27d49-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="27d49-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="27d49-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="27d49-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27d49-154">**\_FORWARDINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="27d49-154">**CIM\_ForwardingService**</span></span>](cim-forwardingservice.md)
</dt> </dl>

 

