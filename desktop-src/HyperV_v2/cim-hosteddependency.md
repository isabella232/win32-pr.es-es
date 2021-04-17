---
description: Representa una asociación en la que un elemento administrado está hospedado por otro.
ms.assetid: ae8476f7-38a4-4d08-a7dc-21e120d3cbe1
title: CIM_HostedDependency (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedDependency
- CIM_HostedDependency.Antecedent
- CIM_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 551931fd88fac88f85bcc8ffd51423538de3bb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686512"
---
# <a name="cim_hosteddependency-class"></a><span data-ttu-id="4ca94-103">\_Clase HostedDependency de CIM</span><span class="sxs-lookup"><span data-stu-id="4ca94-103">CIM\_HostedDependency class</span></span>

<span data-ttu-id="4ca94-104">Representa una asociación en la que un elemento administrado está hospedado por otro.</span><span class="sxs-lookup"><span data-stu-id="4ca94-104">Represents an association where a managed element is hosted by another.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca94-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ca94-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_HostedDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4ca94-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="4ca94-106">Members</span></span>

<span data-ttu-id="4ca94-107">La clase **CIM \_ HostedDependency** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4ca94-107">The **CIM\_HostedDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="4ca94-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4ca94-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ca94-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4ca94-109">Properties</span></span>

<span data-ttu-id="4ca94-110">La clase **CIM \_ HostedDependency** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4ca94-110">The **CIM\_HostedDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ca94-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="4ca94-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ca94-112">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="4ca94-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="4ca94-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ca94-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ca94-114">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="4ca94-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4ca94-115">Elemento administrado por el host.</span><span class="sxs-lookup"><span data-stu-id="4ca94-115">The host managed element.</span></span>

</dd> <dt>

<span data-ttu-id="4ca94-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="4ca94-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ca94-117">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="4ca94-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="4ca94-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ca94-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ca94-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="4ca94-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4ca94-120">Elemento administrado hospedado.</span><span class="sxs-lookup"><span data-stu-id="4ca94-120">The hosted managed element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ca94-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ca94-121">Requirements</span></span>



| <span data-ttu-id="4ca94-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ca94-122">Requirement</span></span> | <span data-ttu-id="4ca94-123">Value</span><span class="sxs-lookup"><span data-stu-id="4ca94-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca94-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ca94-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4ca94-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4ca94-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4ca94-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ca94-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4ca94-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ca94-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4ca94-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4ca94-128">Namespace</span></span><br/>                | <span data-ttu-id="4ca94-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4ca94-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4ca94-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4ca94-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ca94-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ca94-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ca94-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4ca94-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ca94-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4ca94-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4ca94-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ca94-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca94-135">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="4ca94-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

