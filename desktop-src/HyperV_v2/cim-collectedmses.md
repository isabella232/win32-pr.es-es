---
description: Representa una asociación genérica entre una colección de elementos del sistema administrados y los miembros de la colección.
ms.assetid: c9e2bbca-67be-41f2-a94c-cf4eaf5f4694
title: CIM_CollectedMSEs (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdf5c5d682f1b6e1b47b64100b3e00f5f79cebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668092"
---
# <a name="cim_collectedmses-class-hyper-v-management"></a><span data-ttu-id="e945c-103">CIM_CollectedMSEs (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="e945c-103">CIM_CollectedMSEs class (Hyper-V management)</span></span>

<span data-ttu-id="e945c-104">Representa una asociación genérica entre una colección de elementos del sistema administrados y los miembros de la colección.</span><span class="sxs-lookup"><span data-stu-id="e945c-104">Represents a generic association between a collection of managed system elements and the members of the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e945c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e945c-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectedMSEs : CIM_MemberOfCollection
{
  CIM_CollectionOfMSEs     REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="e945c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e945c-106">Members</span></span>

<span data-ttu-id="e945c-107">La clase **CIM \_ CollectedMSEs** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e945c-107">The **CIM\_CollectedMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="e945c-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e945c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e945c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e945c-109">Properties</span></span>

<span data-ttu-id="e945c-110">La clase **CIM \_ CollectedMSEs** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e945c-110">The **CIM\_CollectedMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e945c-111">**Colección**</span><span class="sxs-lookup"><span data-stu-id="e945c-111">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e945c-112">Tipo de datos: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="e945c-112">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="e945c-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e945c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e945c-114">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="e945c-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="e945c-115">La colección.</span><span class="sxs-lookup"><span data-stu-id="e945c-115">The collection.</span></span>

</dd> <dt>

<span data-ttu-id="e945c-116">**Member**</span><span class="sxs-lookup"><span data-stu-id="e945c-116">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e945c-117">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="e945c-117">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="e945c-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e945c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e945c-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("miembro")</span><span class="sxs-lookup"><span data-stu-id="e945c-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="e945c-120">Los miembros de la colección.</span><span class="sxs-lookup"><span data-stu-id="e945c-120">The members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e945c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e945c-121">Requirements</span></span>



| <span data-ttu-id="e945c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e945c-122">Requirement</span></span> | <span data-ttu-id="e945c-123">Value</span><span class="sxs-lookup"><span data-stu-id="e945c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e945c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e945c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e945c-125">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="e945c-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e945c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e945c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e945c-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e945c-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e945c-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e945c-128">Namespace</span></span><br/>                | <span data-ttu-id="e945c-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e945c-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e945c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e945c-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e945c-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e945c-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e945c-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e945c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e945c-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e945c-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e945c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e945c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e945c-135">**\_MEMBEROFCOLLECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="e945c-135">**CIM\_MemberOfCollection**</span></span>](cim-memberofcollection.md)
</dt> </dl>

 

