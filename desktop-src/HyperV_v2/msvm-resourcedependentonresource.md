---
description: Establece que una instancia de CIM \_ ResourceAllocationSettingData que representa una asignación de recursos depende de otra asignación de recursos.
ms.assetid: 567ee36a-d47b-444d-8d2f-425873f95bef
title: Msvm_ResourceDependentOnResource (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceDependentOnResource
- Msvm_ResourceDependentOnResource.Antecedent
- Msvm_ResourceDependentOnResource.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 29cf3b607449c6a9145568e3ee858248af3c4248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687776"
---
# <a name="msvm_resourcedependentonresource-class"></a><span data-ttu-id="2002b-103">MSVM \_ ResourceDependentOnResource (clase)</span><span class="sxs-lookup"><span data-stu-id="2002b-103">Msvm\_ResourceDependentOnResource class</span></span>

<span data-ttu-id="2002b-104">Establece que una instancia de [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa una asignación de recursos depende de otra asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="2002b-104">Establishes that a [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instance representing a resource allocation depends on another resource allocation.</span></span>

<span data-ttu-id="2002b-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2002b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2002b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2002b-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceDependentOnResource : CIM_Dependency
{
  CIM_ResourceAllocationSettingData REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2002b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2002b-107">Members</span></span>

<span data-ttu-id="2002b-108">La clase **MSVM \_ ResourceDependentOnResource** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2002b-108">The **Msvm\_ResourceDependentOnResource** class has these types of members:</span></span>

-   [<span data-ttu-id="2002b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2002b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2002b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2002b-110">Properties</span></span>

<span data-ttu-id="2002b-111">La clase **MSVM \_ ResourceDependentOnResource** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2002b-111">The **Msvm\_ResourceDependentOnResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2002b-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="2002b-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2002b-113">Tipo de datos: **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="2002b-113">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="2002b-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2002b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2002b-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="2002b-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2002b-116">[**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) que representa el recurso independiente de esta asociación.</span><span class="sxs-lookup"><span data-stu-id="2002b-116">A [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that represents the independent resource in this association.</span></span>

</dd> <dt>

<span data-ttu-id="2002b-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="2002b-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2002b-118">Tipo de datos: **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="2002b-118">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="2002b-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2002b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2002b-120">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="2002b-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2002b-121">[**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) que representa el recurso que depende del antecedente.</span><span class="sxs-lookup"><span data-stu-id="2002b-121">A [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that represents the resource that is dependent on the Antecedent.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2002b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2002b-122">Requirements</span></span>



| <span data-ttu-id="2002b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2002b-123">Requirement</span></span> | <span data-ttu-id="2002b-124">Value</span><span class="sxs-lookup"><span data-stu-id="2002b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2002b-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2002b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2002b-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2002b-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2002b-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2002b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2002b-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2002b-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2002b-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2002b-129">Namespace</span></span><br/>                | <span data-ttu-id="2002b-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2002b-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2002b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2002b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2002b-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2002b-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2002b-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2002b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2002b-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2002b-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2002b-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="2002b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2002b-136">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2002b-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

