---
description: Representa una asociación entre un sistema y un grupo de recursos que es un componente del sistema.
ms.assetid: 0ac60dbd-0498-4978-b2d6-f4c9926a83a8
title: CIM_HostedResourcePool (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedResourcePool
- CIM_HostedResourcePool.GroupComponent
- CIM_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dbb6d523b533d6e8b2f5bc1e21de93962cfd860f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666239"
---
# <a name="cim_hostedresourcepool-class"></a><span data-ttu-id="3ee2d-103">\_Clase HostedResourcePool de CIM</span><span class="sxs-lookup"><span data-stu-id="3ee2d-103">CIM\_HostedResourcePool class</span></span>

<span data-ttu-id="3ee2d-104">Representa una asociación entre un sistema y un grupo de recursos que es un componente del sistema.</span><span class="sxs-lookup"><span data-stu-id="3ee2d-104">Represents an association between a system and a resource pool that is a component of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ee2d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ee2d-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_HostedResourcePool : CIM_SystemComponent
{
  CIM_System       REF GroupComponent;
  CIM_ResourcePool REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="3ee2d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3ee2d-106">Members</span></span>

<span data-ttu-id="3ee2d-107">La clase **CIM \_ HostedResourcePool** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3ee2d-107">The **CIM\_HostedResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="3ee2d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ee2d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ee2d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ee2d-109">Properties</span></span>

<span data-ttu-id="3ee2d-110">La clase **CIM \_ HostedResourcePool** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3ee2d-110">The **CIM\_HostedResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ee2d-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3ee2d-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ee2d-112">Tipo de datos **: \_ Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="3ee2d-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="3ee2d-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ee2d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ee2d-114">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="3ee2d-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="3ee2d-115">Sistema primario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="3ee2d-115">The parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="3ee2d-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3ee2d-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ee2d-117">Tipo de datos: **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="3ee2d-117">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="3ee2d-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ee2d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ee2d-119">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="3ee2d-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="3ee2d-120">Grupo de recursos que es un componente del sistema.</span><span class="sxs-lookup"><span data-stu-id="3ee2d-120">The resource pool that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ee2d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ee2d-121">Requirements</span></span>



| <span data-ttu-id="3ee2d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ee2d-122">Requirement</span></span> | <span data-ttu-id="3ee2d-123">Value</span><span class="sxs-lookup"><span data-stu-id="3ee2d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ee2d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ee2d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3ee2d-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3ee2d-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3ee2d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ee2d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3ee2d-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3ee2d-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3ee2d-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3ee2d-128">Namespace</span></span><br/>                | <span data-ttu-id="3ee2d-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3ee2d-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3ee2d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="3ee2d-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ee2d-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ee2d-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ee2d-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ee2d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ee2d-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ee2d-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ee2d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ee2d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ee2d-135">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3ee2d-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

