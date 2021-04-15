---
description: Representa la asociación entre una extensión de conmutador Ethernet primaria y una extensión de conmutador Ethernet secundaria.
ms.assetid: a0a60214-d85d-4c64-b720-1c34abc25287
title: Msvm_ParentEthernetSwitchExtension (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentEthernetSwitchExtension
- Msvm_ParentEthernetSwitchExtension.Antecedent
- Msvm_ParentEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8e215a01c9de98baa545dbb32b8279db4555f9cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688557"
---
# <a name="msvm_parentethernetswitchextension-class"></a><span data-ttu-id="978ec-103">MSVM \_ ParentEthernetSwitchExtension (clase)</span><span class="sxs-lookup"><span data-stu-id="978ec-103">Msvm\_ParentEthernetSwitchExtension class</span></span>

<span data-ttu-id="978ec-104">Representa la asociación entre una extensión de conmutador Ethernet primaria y una extensión de conmutador Ethernet secundaria.</span><span class="sxs-lookup"><span data-stu-id="978ec-104">Represents the association between a parent Ethernet switch extension and a child Ethernet switch extension.</span></span>

<span data-ttu-id="978ec-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="978ec-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="978ec-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="978ec-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentEthernetSwitchExtension : CIM_Dependency
{
  Msvm_EthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="978ec-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="978ec-107">Members</span></span>

<span data-ttu-id="978ec-108">La clase **MSVM \_ ParentEthernetSwitchExtension** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="978ec-108">The **Msvm\_ParentEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="978ec-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="978ec-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="978ec-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="978ec-110">Properties</span></span>

<span data-ttu-id="978ec-111">La clase **MSVM \_ ParentEthernetSwitchExtension** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="978ec-111">The **Msvm\_ParentEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="978ec-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="978ec-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="978ec-113">Tipo de datos: **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="978ec-113">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="978ec-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="978ec-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="978ec-115">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="978ec-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="978ec-116">Referencia a una instancia de la clase [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) que representa la extensión del conmutador primario.</span><span class="sxs-lookup"><span data-stu-id="978ec-116">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the parent switch extension.</span></span>

</dd> <dt>

<span data-ttu-id="978ec-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="978ec-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="978ec-118">Tipo de datos: **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="978ec-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="978ec-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="978ec-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="978ec-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="978ec-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="978ec-121">Referencia a una instancia de la clase [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) que representa la extensión de conmutador secundario.</span><span class="sxs-lookup"><span data-stu-id="978ec-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the child switch extension.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="978ec-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="978ec-122">Requirements</span></span>



| <span data-ttu-id="978ec-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="978ec-123">Requirement</span></span> | <span data-ttu-id="978ec-124">Value</span><span class="sxs-lookup"><span data-stu-id="978ec-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="978ec-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="978ec-125">Minimum supported client</span></span><br/> | <span data-ttu-id="978ec-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="978ec-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="978ec-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="978ec-127">Minimum supported server</span></span><br/> | <span data-ttu-id="978ec-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="978ec-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="978ec-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="978ec-129">Namespace</span></span><br/>                | <span data-ttu-id="978ec-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="978ec-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="978ec-131">MOF</span><span class="sxs-lookup"><span data-stu-id="978ec-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="978ec-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="978ec-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="978ec-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="978ec-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="978ec-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="978ec-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

