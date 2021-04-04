---
description: Representa el aspecto de puente transparente de un \_ objeto SwitchService de CIM.
ms.assetid: 24f650ab-22a1-41c8-8498-c6c30e63c83c
title: CIM_TransparentBridgingService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingService
- CIM_TransparentBridgingService.AgingTime
- CIM_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ed2c21c0f00bd89b0054667274a559ef25ce9326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908730"
---
# <a name="cim_transparentbridgingservice-class"></a><span data-ttu-id="f2bf9-103">\_Clase TransparentBridgingService de CIM</span><span class="sxs-lookup"><span data-stu-id="f2bf9-103">CIM\_TransparentBridgingService class</span></span>

<span data-ttu-id="f2bf9-104">Representa el aspecto de puente transparente de un objeto [**\_ SwitchService de CIM**](cim-switchservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f2bf9-104">Represents the transparent bridging aspect of a [**CIM\_SwitchService**](cim-switchservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2bf9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2bf9-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingService : CIM_ForwardingService
{
  uint32 AgingTime = 300;
  uint32 FID;
};
```

## <a name="members"></a><span data-ttu-id="f2bf9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f2bf9-106">Members</span></span>

<span data-ttu-id="f2bf9-107">La clase **CIM \_ TransparentBridgingService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f2bf9-107">The **CIM\_TransparentBridgingService** class has these types of members:</span></span>

-   [<span data-ttu-id="f2bf9-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f2bf9-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2bf9-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f2bf9-109">Properties</span></span>

<span data-ttu-id="f2bf9-110">La clase **CIM \_ TransparentBridgingService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f2bf9-110">The **CIM\_TransparentBridgingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2bf9-111">**AgingTime**</span><span class="sxs-lookup"><span data-stu-id="f2bf9-111">**AgingTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2bf9-112">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2bf9-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2bf9-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2bf9-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2bf9-114">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Puente IETF-MIB. dot1dTpAgingTime ")</span><span class="sxs-lookup"><span data-stu-id="f2bf9-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Seconds"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpAgingTime")</span></span>
</dt> </dl>

<span data-ttu-id="f2bf9-115">Período de tiempo de espera, en segundos, durante el que se va a obtener la información de reenvío obtenida dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="f2bf9-115">The timeout period, in seconds, for aging out dynamically learned forwarding information.</span></span> <span data-ttu-id="f2bf9-116">El estándar 802.1 D-1990 recomienda un valor predeterminado de 300 segundos.</span><span class="sxs-lookup"><span data-stu-id="f2bf9-116">The 802.1D-1990 standard recommends a default of 300 seconds.</span></span>

</dd> <dt>

<span data-ttu-id="f2bf9-117">**FID**</span><span class="sxs-lookup"><span data-stu-id="f2bf9-117">**FID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2bf9-118">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f2bf9-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2bf9-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f2bf9-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2bf9-120">Filtrado de identificador de base de datos utilizado por conmutadores compatibles con VLAN que tienen más de una base de datos de filtrado.</span><span class="sxs-lookup"><span data-stu-id="f2bf9-120">Filtering Database Identifier used by VLAN-aware switches that have more than one filtering database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2bf9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2bf9-121">Requirements</span></span>



| <span data-ttu-id="f2bf9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2bf9-122">Requirement</span></span> | <span data-ttu-id="f2bf9-123">Value</span><span class="sxs-lookup"><span data-stu-id="f2bf9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2bf9-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2bf9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f2bf9-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f2bf9-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f2bf9-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2bf9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f2bf9-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2bf9-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f2bf9-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f2bf9-128">Namespace</span></span><br/>                | <span data-ttu-id="f2bf9-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f2bf9-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f2bf9-130">MOF</span><span class="sxs-lookup"><span data-stu-id="f2bf9-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2bf9-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2bf9-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2bf9-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2bf9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2bf9-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f2bf9-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f2bf9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2bf9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2bf9-135">**\_FORWARDINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="f2bf9-135">**CIM\_ForwardingService**</span></span>](cim-forwardingservice.md)
</dt> </dl>

 

