---
description: Asocia el \_ VirtualSystemReferencePoint MSVM a los objetos MSVM \_ VirtualSystem correspondientes.
ms.assetid: 5a9cb099-c0ae-4088-a64c-f2720a6cb9c8
title: Msvm_ReferencePointOfVirtualSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystem
- Msvm_ReferencePointOfVirtualSystem.Antecedent
- Msvm_ReferencePointOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debe1931154c5c7a7868e8ee301daf977076b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814219"
---
# <a name="msvm_referencepointofvirtualsystem-class"></a><span data-ttu-id="78a1f-103">MSVM \_ ReferencePointOfVirtualSystem (clase)</span><span class="sxs-lookup"><span data-stu-id="78a1f-103">Msvm\_ReferencePointOfVirtualSystem class</span></span>

<span data-ttu-id="78a1f-104">Asocia el [**\_ VirtualSystemReferencePoint MSVM**](msvm-virtualsystemreferencepoint.md) a los objetos [**MSVM \_ VirtualSystem**](msvm-virtualsystemresourcecomponent.md) correspondientes.</span><span class="sxs-lookup"><span data-stu-id="78a1f-104">Associates the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) to the corresponding [**Msvm\_VirtualSystem**](msvm-virtualsystemresourcecomponent.md) objects.</span></span>

<span data-ttu-id="78a1f-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="78a1f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="78a1f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78a1f-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystem : CIM_Dependency
{
  Msvm_ComputerSystem              REF Antecedent;
  Msvm_VirtualSystemReferencePoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="78a1f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="78a1f-107">Members</span></span>

<span data-ttu-id="78a1f-108">La clase **MSVM \_ ReferencePointOfVirtualSystem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="78a1f-108">The **Msvm\_ReferencePointOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="78a1f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="78a1f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78a1f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="78a1f-110">Properties</span></span>

<span data-ttu-id="78a1f-111">La clase **MSVM \_ ReferencePointOfVirtualSystem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="78a1f-111">The **Msvm\_ReferencePointOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78a1f-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="78a1f-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78a1f-113">Tipo de datos: **MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="78a1f-113">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="78a1f-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78a1f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78a1f-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="78a1f-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="78a1f-116">Un [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa el objeto independiente de esta asociación.</span><span class="sxs-lookup"><span data-stu-id="78a1f-116">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="78a1f-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="78a1f-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78a1f-118">Tipo de datos: **MSVM \_ VirtualSystemReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="78a1f-118">Data type: **Msvm\_VirtualSystemReferencePoint**</span></span>
</dt> <dt>

<span data-ttu-id="78a1f-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78a1f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78a1f-120">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="78a1f-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="78a1f-121">[**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que representa el objeto que depende del **antecedente**.</span><span class="sxs-lookup"><span data-stu-id="78a1f-121">An [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) that represents the object that is dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78a1f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78a1f-122">Requirements</span></span>



| <span data-ttu-id="78a1f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="78a1f-123">Requirement</span></span> | <span data-ttu-id="78a1f-124">Value</span><span class="sxs-lookup"><span data-stu-id="78a1f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78a1f-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78a1f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="78a1f-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="78a1f-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="78a1f-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78a1f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="78a1f-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="78a1f-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="78a1f-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="78a1f-129">Namespace</span></span><br/>                | <span data-ttu-id="78a1f-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="78a1f-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="78a1f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="78a1f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78a1f-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78a1f-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="78a1f-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="78a1f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78a1f-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="78a1f-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="78a1f-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="78a1f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78a1f-136">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="78a1f-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

