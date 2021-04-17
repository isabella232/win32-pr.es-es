---
description: Representa una asociación genérica en la que un elemento administrado depende de otro. CIM \_ ConcreteDependency subclasses CIM \_ Dependency para proporcionar una versión de clase concreta de la \_ dependencia CIM.
ms.assetid: c0e1527d-d350-410d-9b5f-c9d4dedf7393
title: CIM_ConcreteDependency (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteDependency
- CIM_ConcreteDependency.Antecedent
- CIM_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 253f57b1fd29c3844f0e87d488974ced7bec98bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688080"
---
# <a name="cim_concretedependency-class"></a><span data-ttu-id="beeea-104">\_Clase ConcreteDependency de CIM</span><span class="sxs-lookup"><span data-stu-id="beeea-104">CIM\_ConcreteDependency class</span></span>

<span data-ttu-id="beeea-105">Representa una asociación genérica en la que un elemento administrado depende de otro.</span><span class="sxs-lookup"><span data-stu-id="beeea-105">Represents a generic association in which a managed element depends on another.</span></span> <span data-ttu-id="beeea-106">**CIM \_ ConcreteDependency** subclasses [**CIM \_ Dependency**](cim-dependency.md) para proporcionar una versión de clase concreta de la **\_ dependencia CIM**.</span><span class="sxs-lookup"><span data-stu-id="beeea-106">**CIM\_ConcreteDependency** subclasses [**CIM\_Dependency**](cim-dependency.md) to provide a concrete class version of **CIM\_Dependency**.</span></span>

## <a name="syntax"></a><span data-ttu-id="beeea-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="beeea-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="beeea-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="beeea-108">Members</span></span>

<span data-ttu-id="beeea-109">La clase **CIM \_ ConcreteDependency** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="beeea-109">The **CIM\_ConcreteDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="beeea-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="beeea-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="beeea-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="beeea-111">Properties</span></span>

<span data-ttu-id="beeea-112">La clase **CIM \_ ConcreteDependency** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="beeea-112">The **CIM\_ConcreteDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="beeea-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="beeea-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="beeea-114">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="beeea-114">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="beeea-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="beeea-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="beeea-116">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="beeea-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="beeea-117">Objeto independiente de la asociación.</span><span class="sxs-lookup"><span data-stu-id="beeea-117">The independent object in the association.</span></span>

</dd> <dt>

<span data-ttu-id="beeea-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="beeea-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="beeea-119">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="beeea-119">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="beeea-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="beeea-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="beeea-121">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="beeea-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="beeea-122">Objeto dependiente de la asociación.</span><span class="sxs-lookup"><span data-stu-id="beeea-122">The dependent object in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="beeea-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beeea-123">Requirements</span></span>



| <span data-ttu-id="beeea-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="beeea-124">Requirement</span></span> | <span data-ttu-id="beeea-125">Value</span><span class="sxs-lookup"><span data-stu-id="beeea-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="beeea-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beeea-126">Minimum supported client</span></span><br/> | <span data-ttu-id="beeea-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="beeea-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="beeea-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beeea-128">Minimum supported server</span></span><br/> | <span data-ttu-id="beeea-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="beeea-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="beeea-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="beeea-130">Namespace</span></span><br/>                | <span data-ttu-id="beeea-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="beeea-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="beeea-132">MOF</span><span class="sxs-lookup"><span data-stu-id="beeea-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="beeea-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="beeea-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="beeea-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="beeea-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="beeea-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="beeea-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="beeea-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="beeea-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beeea-137">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="beeea-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

