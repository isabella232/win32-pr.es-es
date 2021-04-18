---
description: Asocia el \_ VirtualSystemCollection MSVM a los objetos MSVM \_ ComputerSystem incluidos.
ms.assetid: ad783188-b60a-4271-aa2d-8050c36e70eb
title: Msvm_CollectedVirtualSystems (clase)
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
ms.openlocfilehash: 0803eda14ffbaf21ee2bf4491bd835123b7191e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688371"
---
# <a name="msvm_collectedvirtualsystems-class"></a><span data-ttu-id="ef0a6-103">MSVM \_ CollectedVirtualSystems (clase)</span><span class="sxs-lookup"><span data-stu-id="ef0a6-103">Msvm\_CollectedVirtualSystems class</span></span>

<span data-ttu-id="ef0a6-104">Asocia el [**\_ VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md) a los objetos [**MSVM \_ ComputerSystem**](msvm-computersystem.md) incluidos.</span><span class="sxs-lookup"><span data-stu-id="ef0a6-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="ef0a6-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ef0a6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef0a6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef0a6-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedVirtualSystems : CIM_CollectedMSEs
{
  Msvm_VirtualSystemCollection REF Collection;
  Msvm_ComputerSystem          REF Member;
};
```

## <a name="members"></a><span data-ttu-id="ef0a6-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ef0a6-107">Members</span></span>

<span data-ttu-id="ef0a6-108">La clase **MSVM \_ CollectedVirtualSystems** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ef0a6-108">The **Msvm\_CollectedVirtualSystems** class has these types of members:</span></span>

-   [<span data-ttu-id="ef0a6-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ef0a6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef0a6-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ef0a6-110">Properties</span></span>

<span data-ttu-id="ef0a6-111">La clase **MSVM \_ CollectedVirtualSystems** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ef0a6-111">The **Msvm\_CollectedVirtualSystems** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef0a6-112">**Colección**</span><span class="sxs-lookup"><span data-stu-id="ef0a6-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0a6-113">Tipo de datos: **MSVM \_ VirtualSystemCollection**</span><span class="sxs-lookup"><span data-stu-id="ef0a6-113">Data type: **Msvm\_VirtualSystemCollection**</span></span>
</dt> <dt>

<span data-ttu-id="ef0a6-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef0a6-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0a6-115">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="ef0a6-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="ef0a6-116">Objeto de agrupación o contenedor de [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) que representa la colección.</span><span class="sxs-lookup"><span data-stu-id="ef0a6-116">An [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="ef0a6-117">**Member**</span><span class="sxs-lookup"><span data-stu-id="ef0a6-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0a6-118">Tipo de datos: **MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="ef0a6-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="ef0a6-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef0a6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0a6-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("miembro")</span><span class="sxs-lookup"><span data-stu-id="ef0a6-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="ef0a6-121">Objeto [**\_ ComputerSystem MSVM**](msvm-computersystem.md) que contiene los miembros de la colección.</span><span class="sxs-lookup"><span data-stu-id="ef0a6-121">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) object containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef0a6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef0a6-122">Requirements</span></span>



| <span data-ttu-id="ef0a6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef0a6-123">Requirement</span></span> | <span data-ttu-id="ef0a6-124">Value</span><span class="sxs-lookup"><span data-stu-id="ef0a6-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef0a6-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef0a6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ef0a6-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef0a6-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ef0a6-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef0a6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ef0a6-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ef0a6-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ef0a6-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ef0a6-129">Namespace</span></span><br/>                | <span data-ttu-id="ef0a6-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ef0a6-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ef0a6-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ef0a6-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef0a6-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef0a6-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef0a6-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef0a6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef0a6-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef0a6-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef0a6-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef0a6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef0a6-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="ef0a6-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

