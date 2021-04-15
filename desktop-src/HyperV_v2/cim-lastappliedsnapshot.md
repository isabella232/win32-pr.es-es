---
description: Representa una asociación entre un equipo y la instantánea del sistema virtual aplicada más recientemente.
ms.assetid: 722491a3-1c46-4d37-8bd6-7c7d6648a806
title: CIM_LastAppliedSnapshot (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSnapshot
- CIM_LastAppliedSnapshot.Antecedent
- CIM_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 38efa9c5f02cd0ea40d993cc39ba05ac0b6fde3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689592"
---
# <a name="cim_lastappliedsnapshot-class"></a><span data-ttu-id="2c239-103">\_Clase LastAppliedSnapshot de CIM</span><span class="sxs-lookup"><span data-stu-id="2c239-103">CIM\_LastAppliedSnapshot class</span></span>

<span data-ttu-id="2c239-104">Representa una asociación entre un equipo y la instantánea del sistema virtual aplicada más recientemente.</span><span class="sxs-lookup"><span data-stu-id="2c239-104">Represents an association between a computer system and its most recently applied virtual system snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c239-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c239-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_LastAppliedSnapshot : CIM_Dependency
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2c239-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="2c239-106">Members</span></span>

<span data-ttu-id="2c239-107">La clase **CIM \_ LastAppliedSnapshot** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2c239-107">The **CIM\_LastAppliedSnapshot** class has these types of members:</span></span>

-   [<span data-ttu-id="2c239-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2c239-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c239-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2c239-109">Properties</span></span>

<span data-ttu-id="2c239-110">La clase **CIM \_ LastAppliedSnapshot** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2c239-110">The **CIM\_LastAppliedSnapshot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c239-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="2c239-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c239-112">Tipo de datos: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="2c239-112">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="2c239-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c239-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c239-114">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="2c239-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="2c239-115">La instantánea del sistema virtual que se aplicó en último lugar al sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="2c239-115">The virtual system snapshot that was last applied to the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="2c239-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="2c239-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c239-117">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="2c239-117">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="2c239-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c239-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c239-119">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="2c239-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="2c239-120">Sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="2c239-120">The computer system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c239-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c239-121">Requirements</span></span>



| <span data-ttu-id="2c239-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c239-122">Requirement</span></span> | <span data-ttu-id="2c239-123">Value</span><span class="sxs-lookup"><span data-stu-id="2c239-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c239-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c239-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2c239-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2c239-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2c239-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c239-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2c239-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c239-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2c239-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2c239-128">Namespace</span></span><br/>                | <span data-ttu-id="2c239-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2c239-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2c239-130">MOF</span><span class="sxs-lookup"><span data-stu-id="2c239-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c239-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c239-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c239-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2c239-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c239-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2c239-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2c239-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c239-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c239-135">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2c239-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

