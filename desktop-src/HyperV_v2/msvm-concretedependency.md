---
description: Define la asociación entre una extensión de conmutador Ethernet instalada y una extensión de conmutador Ethernet.
ms.assetid: 306658ed-03a4-49fa-8704-f4b83a4bdd4f
title: Msvm_ConcreteDependency (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteDependency
- Msvm_ConcreteDependency.Antecedent
- Msvm_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c74a8431b03389a106cd127933a2c78b842385f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276181"
---
# <a name="msvm_concretedependency-class"></a><span data-ttu-id="4364d-103">MSVM \_ ConcreteDependency (clase)</span><span class="sxs-lookup"><span data-stu-id="4364d-103">Msvm\_ConcreteDependency class</span></span>

<span data-ttu-id="4364d-104">Define la asociación entre una extensión de conmutador Ethernet instalada y una extensión de conmutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="4364d-104">Defines the association between an installed Ethernet switch extension and an Ethernet switch extension.</span></span>

<span data-ttu-id="4364d-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4364d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4364d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4364d-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteDependency : CIM_ConcreteDependency
{
  Msvm_InstalledEthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension          REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4364d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4364d-107">Members</span></span>

<span data-ttu-id="4364d-108">La clase **MSVM \_ ConcreteDependency** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4364d-108">The **Msvm\_ConcreteDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="4364d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4364d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4364d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4364d-110">Properties</span></span>

<span data-ttu-id="4364d-111">La clase **MSVM \_ ConcreteDependency** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4364d-111">The **Msvm\_ConcreteDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4364d-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="4364d-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4364d-113">Tipo de datos: **[ **MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="4364d-113">Data type: **[**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4364d-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4364d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4364d-115">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="4364d-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4364d-116">Una referencia a una instancia de la clase [**MSVM \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) que representa un componente de extensión de conmutador Ethernet Virtual instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="4364d-116">A reference to an instance of the [**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) class that represents a virtual Ethernet switch extension component installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="4364d-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="4364d-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4364d-118">Tipo de datos: **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="4364d-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4364d-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4364d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4364d-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="4364d-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4364d-121">Una referencia a una instancia de la clase [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) que representa la aparición del **antecedente** enlazado a un conmutador Ethernet virtual específico.</span><span class="sxs-lookup"><span data-stu-id="4364d-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the occurrence of the **Antecedent** bound to a specific virtual Ethernet switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4364d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4364d-122">Requirements</span></span>



| <span data-ttu-id="4364d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4364d-123">Requirement</span></span> | <span data-ttu-id="4364d-124">Value</span><span class="sxs-lookup"><span data-stu-id="4364d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4364d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4364d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4364d-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4364d-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4364d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4364d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4364d-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4364d-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4364d-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4364d-129">Namespace</span></span><br/>                | <span data-ttu-id="4364d-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4364d-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4364d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4364d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4364d-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4364d-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4364d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4364d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4364d-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4364d-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

