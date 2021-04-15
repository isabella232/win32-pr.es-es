---
description: Asocia el \_ VirtualSystemCollection MSVM a los objetos MSVM \_ ComputerSystem incluidos.
ms.assetid: bbf7713a-b331-4b40-bcb4-3545c26c6f3a
title: Msvm_CollectedCollections (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedCollections
- Msvm_CollectedCollections.Collection
- Msvm_CollectedCollections.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16ec6ad77c44e0a4e9001a0cb77d227573635ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669944"
---
# <a name="msvm_collectedcollections-class"></a><span data-ttu-id="47308-103">MSVM \_ CollectedCollections (clase)</span><span class="sxs-lookup"><span data-stu-id="47308-103">Msvm\_CollectedCollections class</span></span>

<span data-ttu-id="47308-104">Asocia el [**\_ VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md) a los objetos [**MSVM \_ ComputerSystem**](msvm-computersystem.md) incluidos.</span><span class="sxs-lookup"><span data-stu-id="47308-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="47308-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="47308-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="47308-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47308-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a><span data-ttu-id="47308-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="47308-107">Members</span></span>

<span data-ttu-id="47308-108">La clase **MSVM \_ CollectedCollections** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="47308-108">The **Msvm\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="47308-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="47308-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47308-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="47308-110">Properties</span></span>

<span data-ttu-id="47308-111">La clase **MSVM \_ CollectedCollections** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="47308-111">The **Msvm\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47308-112">**Colección**</span><span class="sxs-lookup"><span data-stu-id="47308-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47308-113">Tipo de datos: **MSVM \_ ManagementCollection**</span><span class="sxs-lookup"><span data-stu-id="47308-113">Data type: **Msvm\_ManagementCollection**</span></span>
</dt> <dt>

<span data-ttu-id="47308-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="47308-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47308-115">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="47308-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="47308-116">Objeto de agrupación o contenedor de [**MSVM \_ ManagementCollection**](msvm-managementcollection.md) que representa la colección.</span><span class="sxs-lookup"><span data-stu-id="47308-116">An [**Msvm\_ManagementCollection**](msvm-managementcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="47308-117">**Member**</span><span class="sxs-lookup"><span data-stu-id="47308-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47308-118">Tipo de datos: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="47308-118">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="47308-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="47308-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47308-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("miembro")</span><span class="sxs-lookup"><span data-stu-id="47308-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="47308-121">[**\_ CollectionOfMSEs de CIM**](cim-collectionofmses.md) que contiene los miembros de la colección.</span><span class="sxs-lookup"><span data-stu-id="47308-121">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47308-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47308-122">Requirements</span></span>



| <span data-ttu-id="47308-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="47308-123">Requirement</span></span> | <span data-ttu-id="47308-124">Value</span><span class="sxs-lookup"><span data-stu-id="47308-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47308-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47308-125">Minimum supported client</span></span><br/> | <span data-ttu-id="47308-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="47308-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="47308-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47308-127">Minimum supported server</span></span><br/> | <span data-ttu-id="47308-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="47308-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="47308-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="47308-129">Namespace</span></span><br/>                | <span data-ttu-id="47308-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="47308-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="47308-131">MOF</span><span class="sxs-lookup"><span data-stu-id="47308-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47308-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47308-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="47308-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="47308-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47308-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="47308-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="47308-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="47308-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47308-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="47308-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

