---
description: Representa una asociación genérica que se usa para establecer relaciones de dependencia entre los elementos administrados.
ms.assetid: a81beedc-5473-49a6-8e7f-67e831d3e8bc
title: CIM_Dependency (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e85f59b190e0024fc34489315fa2fae1c0d6b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666698"
---
# <a name="cim_dependency-class-hyper-v-management"></a><span data-ttu-id="d6e9f-103">CIM_Dependency (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="d6e9f-103">CIM_Dependency class (Hyper-V management)</span></span>

<span data-ttu-id="d6e9f-104">Representa una asociación genérica que se usa para establecer relaciones de dependencia entre los elementos administrados.</span><span class="sxs-lookup"><span data-stu-id="d6e9f-104">Represents a generic association used to establish dependency relationships between managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6e9f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6e9f-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d6e9f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d6e9f-106">Members</span></span>

<span data-ttu-id="d6e9f-107">La clase de **\_ dependencia CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d6e9f-107">The **CIM\_Dependency** class has these types of members:</span></span>

-   [<span data-ttu-id="d6e9f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6e9f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d6e9f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6e9f-109">Properties</span></span>

<span data-ttu-id="d6e9f-110">La clase de **\_ dependencia CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d6e9f-110">The **CIM\_Dependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6e9f-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="d6e9f-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6e9f-112">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="d6e9f-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d6e9f-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6e9f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6e9f-114">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d6e9f-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d6e9f-115">Objeto independiente de esta asociación.</span><span class="sxs-lookup"><span data-stu-id="d6e9f-115">The independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="d6e9f-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="d6e9f-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6e9f-117">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="d6e9f-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d6e9f-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6e9f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6e9f-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d6e9f-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d6e9f-120">Objeto dependiente de la asociación.</span><span class="sxs-lookup"><span data-stu-id="d6e9f-120">The dependent object in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6e9f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6e9f-121">Requirements</span></span>



| <span data-ttu-id="d6e9f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6e9f-122">Requirement</span></span> | <span data-ttu-id="d6e9f-123">Value</span><span class="sxs-lookup"><span data-stu-id="d6e9f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6e9f-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6e9f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d6e9f-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d6e9f-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d6e9f-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6e9f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d6e9f-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d6e9f-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d6e9f-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d6e9f-128">Namespace</span></span><br/>                | <span data-ttu-id="d6e9f-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d6e9f-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d6e9f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d6e9f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6e9f-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6e9f-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6e9f-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6e9f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6e9f-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d6e9f-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

