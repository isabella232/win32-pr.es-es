---
description: Representa un puerto de conmutador que envía y recibe tramas de datos.
ms.assetid: 015eed2a-1393-40ef-a190-832ab48766f9
title: CIM_SwitchPort (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPort
- CIM_SwitchPort.PortNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf63843fc5a246012d3af6a059c897956d6f19b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002016"
---
# <a name="cim_switchport-class"></a><span data-ttu-id="bf6db-103">\_Clase de SWITCHPORT CIM</span><span class="sxs-lookup"><span data-stu-id="bf6db-103">CIM\_SwitchPort class</span></span>

<span data-ttu-id="bf6db-104">Representa un puerto de conmutador que envía y recibe tramas de datos.</span><span class="sxs-lookup"><span data-stu-id="bf6db-104">Represents a switch port that sends and receives data frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf6db-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf6db-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints")]
class CIM_SwitchPort : CIM_ProtocolEndpoint
{
  uint16 PortNumber;
};
```

## <a name="members"></a><span data-ttu-id="bf6db-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="bf6db-106">Members</span></span>

<span data-ttu-id="bf6db-107">La clase de **\_ SwitchPort de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bf6db-107">The **CIM\_SwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="bf6db-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf6db-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf6db-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf6db-109">Properties</span></span>

<span data-ttu-id="bf6db-110">La clase de **\_ SwitchPort de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bf6db-110">The **CIM\_SwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf6db-111">**NúmeroDePuerto**</span><span class="sxs-lookup"><span data-stu-id="bf6db-111">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf6db-112">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bf6db-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bf6db-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf6db-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf6db-114">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Puente IETF-MIB. dot1dPort ")</span><span class="sxs-lookup"><span data-stu-id="bf6db-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dPort")</span></span>
</dt> </dl>

<span data-ttu-id="bf6db-115">El identificador numérico del puerto del conmutador.</span><span class="sxs-lookup"><span data-stu-id="bf6db-115">The numeric identifier of the switch port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf6db-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf6db-116">Requirements</span></span>



| <span data-ttu-id="bf6db-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf6db-117">Requirement</span></span> | <span data-ttu-id="bf6db-118">Value</span><span class="sxs-lookup"><span data-stu-id="bf6db-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf6db-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf6db-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bf6db-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bf6db-120">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="bf6db-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf6db-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bf6db-122">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bf6db-122">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="bf6db-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bf6db-123">Namespace</span></span><br/>                | <span data-ttu-id="bf6db-124">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bf6db-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bf6db-125">MOF</span><span class="sxs-lookup"><span data-stu-id="bf6db-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf6db-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf6db-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf6db-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bf6db-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf6db-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bf6db-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bf6db-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf6db-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf6db-130">**ProtocolEndpoint de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="bf6db-130">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

