---
description: 'Msvm_CollectedVirtualSystems clase : asocia Msvm \_ VirtualSystemCollection a los objetos ComputerSystem de Msvm \_ contenidos.'
ms.assetid: ad783188-b60a-4271-aa2d-8050c36e70eb
title: Msvm_CollectedVirtualSystems clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedVirtualSystems
- Msvm_CollectedVirtualSystems.Collection
- Msvm_CollectedVirtualSystems.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6775f41a6e2ae7e45bac642fcd32b8deaec3fda
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119283"
---
# <a name="msvm_collectedvirtualsystems-class"></a><span data-ttu-id="7e9c3-103">Clase Msvm \_ CollectedVirtualSystems</span><span class="sxs-lookup"><span data-stu-id="7e9c3-103">Msvm\_CollectedVirtualSystems class</span></span>

<span data-ttu-id="7e9c3-104">Asocia [**Msvm \_ VirtualSystemCollection a**](msvm-virtualsystemcollection.md) los objetos [**\_ Msvm ComputerSystem contenidos.**](msvm-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="7e9c3-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="7e9c3-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7e9c3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e9c3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e9c3-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedVirtualSystems : CIM_CollectedMSEs
{
  Msvm_VirtualSystemCollection REF Collection;
  Msvm_ComputerSystem          REF Member;
};
```

## <a name="members"></a><span data-ttu-id="7e9c3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7e9c3-107">Members</span></span>

<span data-ttu-id="7e9c3-108">La **clase Msvm \_ CollectedVirtualSystems** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7e9c3-108">The **Msvm\_CollectedVirtualSystems** class has these types of members:</span></span>

-   [<span data-ttu-id="7e9c3-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e9c3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e9c3-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e9c3-110">Properties</span></span>

<span data-ttu-id="7e9c3-111">La **clase Msvm \_ CollectedVirtualSystems** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7e9c3-111">The **Msvm\_CollectedVirtualSystems** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e9c3-112">**Colección**</span><span class="sxs-lookup"><span data-stu-id="7e9c3-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e9c3-113">Tipo de datos: **Msvm \_ VirtualSystemCollection**</span><span class="sxs-lookup"><span data-stu-id="7e9c3-113">Data type: **Msvm\_VirtualSystemCollection**</span></span>
</dt> <dt>

<span data-ttu-id="7e9c3-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e9c3-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e9c3-115">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="7e9c3-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="7e9c3-116">Objeto [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) que agrupa o "bag" que representa la colección.</span><span class="sxs-lookup"><span data-stu-id="7e9c3-116">An [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="7e9c3-117">**Member**</span><span class="sxs-lookup"><span data-stu-id="7e9c3-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e9c3-118">Tipo de datos: **Msvm \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="7e9c3-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="7e9c3-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e9c3-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e9c3-120">Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="7e9c3-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="7e9c3-121">Objeto [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) que contiene los miembros de la colección.</span><span class="sxs-lookup"><span data-stu-id="7e9c3-121">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) object containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e9c3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e9c3-122">Requirements</span></span>



| <span data-ttu-id="7e9c3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e9c3-123">Requirement</span></span> | <span data-ttu-id="7e9c3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7e9c3-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e9c3-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e9c3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7e9c3-126">Windows 10 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="7e9c3-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7e9c3-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e9c3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7e9c3-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7e9c3-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7e9c3-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7e9c3-129">Namespace</span></span><br/>                | <span data-ttu-id="7e9c3-130">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="7e9c3-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7e9c3-131">MOF</span><span class="sxs-lookup"><span data-stu-id="7e9c3-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e9c3-132"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e9c3-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e9c3-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e9c3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e9c3-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e9c3-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7e9c3-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7e9c3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e9c3-136">**CIM \_ CollectedMSEs**</span><span class="sxs-lookup"><span data-stu-id="7e9c3-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

