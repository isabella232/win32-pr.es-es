---
description: Representa una especialización de la Asociación de componentes del sistema que establece que el grupo de recursos de recurso se define en el contexto del sistema.
ms.assetid: 72b68687-2b5f-4fef-bdca-a5c0bbfa3564
title: Msvm_HostedResourcePool (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedResourcePool
- Msvm_HostedResourcePool.GroupComponent
- Msvm_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d64488a845e8d51bfe27829b01ebcf0ac7d944c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907701"
---
# <a name="msvm_hostedresourcepool-class"></a><span data-ttu-id="96e37-103">MSVM \_ HostedResourcePool (clase)</span><span class="sxs-lookup"><span data-stu-id="96e37-103">Msvm\_HostedResourcePool class</span></span>

<span data-ttu-id="96e37-104">Representa una especialización de la Asociación de componentes del sistema que establece que el grupo de recursos de recurso se define en el contexto del sistema.</span><span class="sxs-lookup"><span data-stu-id="96e37-104">Represents a specialization of the system component association that establishes that the resource pool is defined in the context of the system.</span></span>

<span data-ttu-id="96e37-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="96e37-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e37-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96e37-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedResourcePool : CIM_SystemComponent
{
  Msvm_ComputerSystem REF GroupComponent;
  CIM_ResourcePool    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="96e37-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="96e37-107">Members</span></span>

<span data-ttu-id="96e37-108">La clase **MSVM \_ HostedResourcePool** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="96e37-108">The **Msvm\_HostedResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="96e37-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96e37-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96e37-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96e37-110">Properties</span></span>

<span data-ttu-id="96e37-111">La clase **MSVM \_ HostedResourcePool** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="96e37-111">The **Msvm\_HostedResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96e37-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="96e37-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96e37-113">Tipo de datos: **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="96e37-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="96e37-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96e37-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96e37-115">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="96e37-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="96e37-116">Sistema primario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="96e37-116">The parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="96e37-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="96e37-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96e37-118">Tipo de datos: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="96e37-118">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="96e37-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96e37-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96e37-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="96e37-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="96e37-121">Grupo de recursos que es un componente del sistema.</span><span class="sxs-lookup"><span data-stu-id="96e37-121">The resource pool that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96e37-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96e37-122">Requirements</span></span>



| <span data-ttu-id="96e37-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="96e37-123">Requirement</span></span> | <span data-ttu-id="96e37-124">Value</span><span class="sxs-lookup"><span data-stu-id="96e37-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96e37-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96e37-125">Minimum supported client</span></span><br/> | <span data-ttu-id="96e37-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="96e37-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="96e37-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96e37-127">Minimum supported server</span></span><br/> | <span data-ttu-id="96e37-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="96e37-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96e37-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="96e37-129">Namespace</span></span><br/>                | <span data-ttu-id="96e37-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="96e37-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="96e37-131">MOF</span><span class="sxs-lookup"><span data-stu-id="96e37-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96e37-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96e37-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="96e37-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="96e37-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96e37-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="96e37-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

