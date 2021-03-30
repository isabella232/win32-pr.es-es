---
description: Representa la asociación entre un ExternalEthernetPort de equipo y un ExternalEthernetPort de miembro.
ms.assetid: e21bea94-d6a8-4788-958e-78ce255837aa
title: Msvm_VirtualEthernetSwitchNicTeamingMember (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingMember
- Msvm_VirtualEthernetSwitchNicTeamingMember.Antecedent
- Msvm_VirtualEthernetSwitchNicTeamingMember.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbf83f4605d6ab1b7bc9740b14c493393eb93163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279662"
---
# <a name="msvm_virtualethernetswitchnicteamingmember-class"></a><span data-ttu-id="cd320-103">MSVM \_ VirtualEthernetSwitchNicTeamingMember (clase)</span><span class="sxs-lookup"><span data-stu-id="cd320-103">Msvm\_VirtualEthernetSwitchNicTeamingMember class</span></span>

<span data-ttu-id="cd320-104">Representa la asociación entre un ExternalEthernetPort de equipo y un ExternalEthernetPort de miembro.</span><span class="sxs-lookup"><span data-stu-id="cd320-104">Represents the association between a team ExternalEthernetPort and a member ExternalEthernetPort.</span></span>

<span data-ttu-id="cd320-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cd320-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd320-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd320-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingMember : CIM_Dependency
{
  Msvm_ExternalEthernetPort REF Antecedent;
  Msvm_ExternalEthernetPort REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="cd320-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="cd320-107">Members</span></span>

<span data-ttu-id="cd320-108">La clase **MSVM \_ VirtualEthernetSwitchNicTeamingMember** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cd320-108">The **Msvm\_VirtualEthernetSwitchNicTeamingMember** class has these types of members:</span></span>

-   [<span data-ttu-id="cd320-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd320-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd320-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd320-110">Properties</span></span>

<span data-ttu-id="cd320-111">La clase **MSVM \_ VirtualEthernetSwitchNicTeamingMember** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cd320-111">The **Msvm\_VirtualEthernetSwitchNicTeamingMember** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd320-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="cd320-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd320-113">Tipo de datos: **MSVM \_ ExternalEthernetPort**</span><span class="sxs-lookup"><span data-stu-id="cd320-113">Data type: **Msvm\_ExternalEthernetPort**</span></span>
</dt> <dt>

<span data-ttu-id="cd320-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd320-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd320-115">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="cd320-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="cd320-116">Un [**\_ ExternalEthernetPort de MSVM**](msvm-externalethernetport.md) que hace referencia a la instancia del puerto Ethernet externo del equipo.</span><span class="sxs-lookup"><span data-stu-id="cd320-116">An [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md) that references the team external ethernet port instance.</span></span>

</dd> <dt>

<span data-ttu-id="cd320-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="cd320-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd320-118">Tipo de datos: **MSVM \_ ExternalEthernetPort**</span><span class="sxs-lookup"><span data-stu-id="cd320-118">Data type: **Msvm\_ExternalEthernetPort**</span></span>
</dt> <dt>

<span data-ttu-id="cd320-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd320-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd320-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="cd320-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="cd320-121">Referencia a la instancia miembro de [**MSVM \_ ExternalEthernetPort**](msvm-externalethernetport.md) .</span><span class="sxs-lookup"><span data-stu-id="cd320-121">Reference to the member [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md) instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd320-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd320-122">Requirements</span></span>



| <span data-ttu-id="cd320-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd320-123">Requirement</span></span> | <span data-ttu-id="cd320-124">Value</span><span class="sxs-lookup"><span data-stu-id="cd320-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd320-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd320-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cd320-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="cd320-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="cd320-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd320-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cd320-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cd320-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cd320-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cd320-129">Namespace</span></span><br/>                | <span data-ttu-id="cd320-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="cd320-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cd320-131">MOF</span><span class="sxs-lookup"><span data-stu-id="cd320-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd320-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd320-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd320-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cd320-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd320-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd320-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd320-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd320-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd320-136">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="cd320-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

