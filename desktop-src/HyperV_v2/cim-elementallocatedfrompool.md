---
description: Representa una asociación en la que un \_ objeto LogicalElement de CIM representa un recurso asignado de un \_ objeto RESOURCEPOOL de CIM.
ms.assetid: 5e3c95c5-1cbb-40de-b285-0bf9b34a5ca8
title: CIM_ElementAllocatedFromPool (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementAllocatedFromPool
- CIM_ElementAllocatedFromPool.Antecedent
- CIM_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5fc6d58f5ebf82013f38b39027e0cd02e0e3595a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908224"
---
# <a name="cim_elementallocatedfrompool-class"></a><span data-ttu-id="e7ea9-103">\_Clase ElementAllocatedFromPool de CIM</span><span class="sxs-lookup"><span data-stu-id="e7ea9-103">CIM\_ElementAllocatedFromPool class</span></span>

<span data-ttu-id="e7ea9-104">Representa una asociación en la que un objeto [**\_ LogicalElement de CIM**](cim-logicalelement.md) representa un recurso asignado de un objeto [**\_ ResourcePool de CIM**](cim-resourcepool.md) .</span><span class="sxs-lookup"><span data-stu-id="e7ea9-104">Represents an association in which a [**CIM\_LogicalElement**](cim-logicalelement.md) object represents a resource allocated from a [**CIM\_ResourcePool**](cim-resourcepool.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7ea9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7ea9-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ElementAllocatedFromPool : CIM_Dependency
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e7ea9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e7ea9-106">Members</span></span>

<span data-ttu-id="e7ea9-107">La clase **CIM \_ ElementAllocatedFromPool** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e7ea9-107">The **CIM\_ElementAllocatedFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="e7ea9-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7ea9-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7ea9-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7ea9-109">Properties</span></span>

<span data-ttu-id="e7ea9-110">La clase **CIM \_ ElementAllocatedFromPool** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e7ea9-110">The **CIM\_ElementAllocatedFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7ea9-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="e7ea9-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7ea9-112">Tipo de datos: **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="e7ea9-112">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="e7ea9-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7ea9-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7ea9-114">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e7ea9-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e7ea9-115">Grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e7ea9-115">The resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="e7ea9-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="e7ea9-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7ea9-117">Tipo de datos: **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="e7ea9-117">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="e7ea9-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7ea9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7ea9-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="e7ea9-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e7ea9-120">Recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="e7ea9-120">The allocated resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7ea9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7ea9-121">Requirements</span></span>



| <span data-ttu-id="e7ea9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7ea9-122">Requirement</span></span> | <span data-ttu-id="e7ea9-123">Value</span><span class="sxs-lookup"><span data-stu-id="e7ea9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ea9-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7ea9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e7ea9-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e7ea9-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e7ea9-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7ea9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e7ea9-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7ea9-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e7ea9-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e7ea9-128">Namespace</span></span><br/>                | <span data-ttu-id="e7ea9-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e7ea9-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e7ea9-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e7ea9-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7ea9-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7ea9-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7ea9-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e7ea9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7ea9-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e7ea9-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e7ea9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7ea9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ea9-135">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e7ea9-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

