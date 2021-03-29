---
description: Asocia un conmutador Ethernet virtual a las extensiones enlazadas actualmente a él.
ms.assetid: d8c87fa2-6859-49ed-abd5-32a836b00e5a
title: Msvm_HostedEthernetSwitchExtension (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedEthernetSwitchExtension
- Msvm_HostedEthernetSwitchExtension.Antecedent
- Msvm_HostedEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cb952d42864fb6130ad6cbec09ef5eb68439f6a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810436"
---
# <a name="msvm_hostedethernetswitchextension-class"></a><span data-ttu-id="35e10-103">MSVM \_ HostedEthernetSwitchExtension (clase)</span><span class="sxs-lookup"><span data-stu-id="35e10-103">Msvm\_HostedEthernetSwitchExtension class</span></span>

<span data-ttu-id="35e10-104">Asocia un conmutador Ethernet virtual a las extensiones enlazadas actualmente a él.</span><span class="sxs-lookup"><span data-stu-id="35e10-104">Associates a virtual Ethernet switch to the extensions currently bound to it.</span></span>

<span data-ttu-id="35e10-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="35e10-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e10-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35e10-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedEthernetSwitchExtension : CIM_HostedDependency
{
  Msvm_VirtualEthernetSwitch   REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="35e10-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="35e10-107">Members</span></span>

<span data-ttu-id="35e10-108">La clase **MSVM \_ HostedEthernetSwitchExtension** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="35e10-108">The **Msvm\_HostedEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="35e10-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35e10-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35e10-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35e10-110">Properties</span></span>

<span data-ttu-id="35e10-111">La clase **MSVM \_ HostedEthernetSwitchExtension** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="35e10-111">The **Msvm\_HostedEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35e10-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="35e10-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e10-113">Tipo de datos: **[ **MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span><span class="sxs-lookup"><span data-stu-id="35e10-113">Data type: **[**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span></span>
</dt> <dt>

<span data-ttu-id="35e10-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35e10-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e10-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="35e10-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="35e10-116">Referencia a una instancia de la clase [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) que representa el conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="35e10-116">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="35e10-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="35e10-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35e10-118">Tipo de datos: **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="35e10-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="35e10-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35e10-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35e10-120">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="35e10-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="35e10-121">Referencia a una instancia de la clase [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) que representa la instancia de la extensión de conmutador enlazada al conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="35e10-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the switch extension instance bound to the virtual switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35e10-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35e10-122">Requirements</span></span>



| <span data-ttu-id="35e10-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="35e10-123">Requirement</span></span> | <span data-ttu-id="35e10-124">Value</span><span class="sxs-lookup"><span data-stu-id="35e10-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35e10-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35e10-125">Minimum supported client</span></span><br/> | <span data-ttu-id="35e10-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="35e10-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="35e10-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35e10-127">Minimum supported server</span></span><br/> | <span data-ttu-id="35e10-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="35e10-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35e10-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="35e10-129">Namespace</span></span><br/>                | <span data-ttu-id="35e10-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="35e10-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="35e10-131">MOF</span><span class="sxs-lookup"><span data-stu-id="35e10-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35e10-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35e10-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35e10-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35e10-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35e10-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35e10-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

