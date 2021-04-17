---
description: Representa una asociación entre un sistema virtual y la instantánea más actual del sistema. Esta asociación solo puede existir si el sistema virtual se creó con una instantánea o si se creó una instantánea a partir del sistema virtual.
ms.assetid: e6040818-84cf-4cec-ab7b-a733fe5d01d2
title: CIM_MostCurrentSnapshotInBranch (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MostCurrentSnapshotInBranch
- CIM_MostCurrentSnapshotInBranch.Antecedent
- CIM_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 078a7c9f1669a2aa0449dce01022eba0eadcb2c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687354"
---
# <a name="cim_mostcurrentsnapshotinbranch-class"></a><span data-ttu-id="8c13f-104">\_Clase MostCurrentSnapshotInBranch de CIM</span><span class="sxs-lookup"><span data-stu-id="8c13f-104">CIM\_MostCurrentSnapshotInBranch class</span></span>

<span data-ttu-id="8c13f-105">Representa una asociación entre un sistema virtual y la instantánea más actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="8c13f-105">Represents an association between a virtual system and the most current snapshot of the system.</span></span> <span data-ttu-id="8c13f-106">Esta asociación solo puede existir si el sistema virtual se creó con una instantánea o si se creó una instantánea a partir del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="8c13f-106">This association can only exist if the virtual system was create using a snapshot or if a snapshot was created from the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c13f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c13f-107">Syntax</span></span>

``` syntax
[Association, Experimental, Version("2.16.0"), AMENDMENT]
class CIM_MostCurrentSnapshotInBranch : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="8c13f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c13f-108">Members</span></span>

<span data-ttu-id="8c13f-109">La clase **CIM \_ MostCurrentSnapshotInBranch** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8c13f-109">The **CIM\_MostCurrentSnapshotInBranch** class has these types of members:</span></span>

-   [<span data-ttu-id="8c13f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c13f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c13f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c13f-111">Properties</span></span>

<span data-ttu-id="8c13f-112">La clase **CIM \_ MostCurrentSnapshotInBranch** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8c13f-112">The **CIM\_MostCurrentSnapshotInBranch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c13f-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="8c13f-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c13f-114">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="8c13f-114">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="8c13f-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c13f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c13f-116">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8c13f-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8c13f-117">Referencia a la instancia de un [**\_ ComputerSystem de CIM**](cim-computersystem.md) que representa el sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="8c13f-117">A reference to the instance of [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="8c13f-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="8c13f-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c13f-119">Tipo de datos: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="8c13f-119">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="8c13f-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c13f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c13f-121">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8c13f-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8c13f-122">Referencia a la instancia de [**\_ VirtualSystemSettingData de CIM**](cim-virtualsystemsettingdata.md) que representa la instantánea del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="8c13f-122">A reference to the instance of [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that represents the virtual system snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c13f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c13f-123">Requirements</span></span>



| <span data-ttu-id="8c13f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c13f-124">Requirement</span></span> | <span data-ttu-id="8c13f-125">Value</span><span class="sxs-lookup"><span data-stu-id="8c13f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c13f-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c13f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8c13f-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8c13f-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8c13f-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c13f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8c13f-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8c13f-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8c13f-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8c13f-130">Namespace</span></span><br/>                | <span data-ttu-id="8c13f-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="8c13f-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8c13f-132">MOF</span><span class="sxs-lookup"><span data-stu-id="8c13f-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c13f-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c13f-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c13f-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c13f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c13f-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8c13f-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8c13f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c13f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c13f-137">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="8c13f-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

