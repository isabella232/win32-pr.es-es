---
description: Representa una asociación en la que un servicio de puente es un componente de un servicio de conmutador.
ms.assetid: 737d5ba1-0759-40cf-bc46-a059d19902c8
title: CIM_SwitchServiceTransparentBridging (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchServiceTransparentBridging
- CIM_SwitchServiceTransparentBridging.GroupComponent
- CIM_SwitchServiceTransparentBridging.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04bce4bf673dc029b7b3a2d2b837670b01300c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666912"
---
# <a name="cim_switchservicetransparentbridging-class"></a><span data-ttu-id="3649b-103">\_Clase SwitchServiceTransparentBridging de CIM</span><span class="sxs-lookup"><span data-stu-id="3649b-103">CIM\_SwitchServiceTransparentBridging class</span></span>

<span data-ttu-id="3649b-104">Representa una asociación en la que un servicio de puente es un componente de un servicio de conmutador.</span><span class="sxs-lookup"><span data-stu-id="3649b-104">Represents an association in which a bridge service is a component of a switch service.</span></span>

## <a name="syntax"></a><span data-ttu-id="3649b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3649b-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchServiceTransparentBridging : CIM_ServiceComponent
{
  CIM_SwitchService              REF GroupComponent;
  CIM_TransparentBridgingService REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="3649b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3649b-106">Members</span></span>

<span data-ttu-id="3649b-107">La clase **CIM \_ SwitchServiceTransparentBridging** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3649b-107">The **CIM\_SwitchServiceTransparentBridging** class has these types of members:</span></span>

-   [<span data-ttu-id="3649b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3649b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3649b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3649b-109">Properties</span></span>

<span data-ttu-id="3649b-110">La clase **CIM \_ SwitchServiceTransparentBridging** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3649b-110">The **CIM\_SwitchServiceTransparentBridging** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3649b-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3649b-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3649b-112">Tipo de datos: **CIM \_ SwitchService**</span><span class="sxs-lookup"><span data-stu-id="3649b-112">Data type: **CIM\_SwitchService**</span></span>
</dt> <dt>

<span data-ttu-id="3649b-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3649b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3649b-114">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="3649b-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="3649b-115">Una [**referencia \_ SwitchService de CIM**](cim-switchservice.md) al servicio del conmutador.</span><span class="sxs-lookup"><span data-stu-id="3649b-115">A [**CIM\_SwitchService**](cim-switchservice.md) reference to the switch service.</span></span>

</dd> <dt>

<span data-ttu-id="3649b-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3649b-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3649b-117">Tipo de datos: **CIM \_ TransparentBridgingService**</span><span class="sxs-lookup"><span data-stu-id="3649b-117">Data type: **CIM\_TransparentBridgingService**</span></span>
</dt> <dt>

<span data-ttu-id="3649b-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3649b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3649b-119">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="3649b-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="3649b-120">Una [**referencia \_ TransparentBridgingService de CIM**](cim-transparentbridgingservice.md) al servicio de puente de componentes.</span><span class="sxs-lookup"><span data-stu-id="3649b-120">A [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) reference to the component bridging service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3649b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3649b-121">Requirements</span></span>



| <span data-ttu-id="3649b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3649b-122">Requirement</span></span> | <span data-ttu-id="3649b-123">Value</span><span class="sxs-lookup"><span data-stu-id="3649b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3649b-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3649b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3649b-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3649b-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3649b-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3649b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3649b-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3649b-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3649b-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3649b-128">Namespace</span></span><br/>                | <span data-ttu-id="3649b-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3649b-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3649b-130">MOF</span><span class="sxs-lookup"><span data-stu-id="3649b-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3649b-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3649b-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3649b-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3649b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3649b-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3649b-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3649b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3649b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3649b-135">**\_SERVICECOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3649b-135">**CIM\_ServiceComponent**</span></span>](cim-servicecomponent.md)
</dt> </dl>

 

