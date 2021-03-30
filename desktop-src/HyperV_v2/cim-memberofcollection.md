---
description: Representa una relación en la que un elemento administrado es miembro de y se agrega mediante una colección.
ms.assetid: 324284fa-ece6-41df-9891-040a7561dce4
title: CIM_MemberOfCollection (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemberOfCollection
- CIM_MemberOfCollection.Collection
- CIM_MemberOfCollection.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9bcebfb08cbbc0cb18e00f1b0e5e2646ca086faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082941"
---
# <a name="cim_memberofcollection-class"></a><span data-ttu-id="6acbb-103">\_Clase MemberOfCollection de CIM</span><span class="sxs-lookup"><span data-stu-id="6acbb-103">CIM\_MemberOfCollection class</span></span>

<span data-ttu-id="6acbb-104">Representa una relación en la que un elemento administrado es miembro de y se agrega mediante una colección.</span><span class="sxs-lookup"><span data-stu-id="6acbb-104">Represents a relationship in which a managed element is a member of and is aggregated by a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6acbb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6acbb-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_MemberOfCollection
{
  CIM_Collection     REF Collection;
  CIM_ManagedElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="6acbb-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="6acbb-106">Members</span></span>

<span data-ttu-id="6acbb-107">La clase **CIM \_ MemberOfCollection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6acbb-107">The **CIM\_MemberOfCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="6acbb-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6acbb-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6acbb-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6acbb-109">Properties</span></span>

<span data-ttu-id="6acbb-110">La clase **CIM \_ MemberOfCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6acbb-110">The **CIM\_MemberOfCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6acbb-111">**Colección**</span><span class="sxs-lookup"><span data-stu-id="6acbb-111">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6acbb-112">Tipo de datos **: \_ colección CIM**</span><span class="sxs-lookup"><span data-stu-id="6acbb-112">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="6acbb-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6acbb-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6acbb-114">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**agregado**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6acbb-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6acbb-115">Colección que agrega miembros.</span><span class="sxs-lookup"><span data-stu-id="6acbb-115">The collection that aggregates members.</span></span>

</dd> <dt>

<span data-ttu-id="6acbb-116">**Member**</span><span class="sxs-lookup"><span data-stu-id="6acbb-116">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6acbb-117">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="6acbb-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="6acbb-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6acbb-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6acbb-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6acbb-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6acbb-120">Miembro de la colección.</span><span class="sxs-lookup"><span data-stu-id="6acbb-120">The member of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6acbb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6acbb-121">Requirements</span></span>



| <span data-ttu-id="6acbb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6acbb-122">Requirement</span></span> | <span data-ttu-id="6acbb-123">Value</span><span class="sxs-lookup"><span data-stu-id="6acbb-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6acbb-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6acbb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6acbb-125">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="6acbb-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6acbb-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6acbb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6acbb-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6acbb-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6acbb-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6acbb-128">Namespace</span></span><br/>                | <span data-ttu-id="6acbb-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="6acbb-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6acbb-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6acbb-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6acbb-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6acbb-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6acbb-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6acbb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6acbb-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6acbb-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

