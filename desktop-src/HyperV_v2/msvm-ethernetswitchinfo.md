---
description: Define la asociación entre un conmutador Ethernet y un recurso switch.
ms.assetid: fb29f4cb-50c4-4865-b267-21ff99bb4a8b
title: Msvm_EthernetSwitchInfo (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchInfo
- Msvm_EthernetSwitchInfo.Antecedent
- Msvm_EthernetSwitchInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1106e0930716572b10a95846865d8f90aa991cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003227"
---
# <a name="msvm_ethernetswitchinfo-class"></a><span data-ttu-id="68020-103">MSVM \_ EthernetSwitchInfo (clase)</span><span class="sxs-lookup"><span data-stu-id="68020-103">Msvm\_EthernetSwitchInfo class</span></span>

<span data-ttu-id="68020-104">Define la asociación entre un conmutador Ethernet y un recurso switch.</span><span class="sxs-lookup"><span data-stu-id="68020-104">Defines the association between an Ethernet switch and a switch resource.</span></span>

<span data-ttu-id="68020-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="68020-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="68020-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68020-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchInfo : CIM_Dependency
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  Msvm_EthernetSwitchData    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="68020-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="68020-107">Members</span></span>

<span data-ttu-id="68020-108">La clase **MSVM \_ EthernetSwitchInfo** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="68020-108">The **Msvm\_EthernetSwitchInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="68020-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68020-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68020-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68020-110">Properties</span></span>

<span data-ttu-id="68020-111">La clase **MSVM \_ EthernetSwitchInfo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="68020-111">The **Msvm\_EthernetSwitchInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68020-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="68020-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68020-113">Tipo de datos: **MSVM \_ VirtualEthernetSwitch**</span><span class="sxs-lookup"><span data-stu-id="68020-113">Data type: **Msvm\_VirtualEthernetSwitch**</span></span>
</dt> <dt>

<span data-ttu-id="68020-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68020-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68020-115">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="68020-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="68020-116">Referencia a la clase [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) que representa el sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="68020-116">A reference to the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the hosting system.</span></span> <span data-ttu-id="68020-117">Esta propiedad se deriva de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="68020-117">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="68020-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="68020-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68020-119">Tipo de datos: **MSVM \_ EthernetSwitchData**</span><span class="sxs-lookup"><span data-stu-id="68020-119">Data type: **Msvm\_EthernetSwitchData**</span></span>
</dt> <dt>

<span data-ttu-id="68020-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68020-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68020-121">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="68020-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="68020-122">Referencia a la clase [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md) que representa el recurso switch.</span><span class="sxs-lookup"><span data-stu-id="68020-122">A reference to the [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md) class that represents the switch resource.</span></span> <span data-ttu-id="68020-123">Esta propiedad se deriva de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="68020-123">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68020-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68020-124">Requirements</span></span>



| <span data-ttu-id="68020-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="68020-125">Requirement</span></span> | <span data-ttu-id="68020-126">Value</span><span class="sxs-lookup"><span data-stu-id="68020-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68020-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68020-127">Minimum supported client</span></span><br/> | <span data-ttu-id="68020-128">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="68020-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="68020-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68020-129">Minimum supported server</span></span><br/> | <span data-ttu-id="68020-130">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="68020-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="68020-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="68020-131">Namespace</span></span><br/>                | <span data-ttu-id="68020-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="68020-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="68020-133">MOF</span><span class="sxs-lookup"><span data-stu-id="68020-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68020-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68020-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="68020-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68020-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68020-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="68020-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

