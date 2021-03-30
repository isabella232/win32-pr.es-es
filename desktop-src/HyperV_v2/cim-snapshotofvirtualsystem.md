---
description: Asocia un sistema virtual a una instantánea del sistema virtual.
ms.assetid: f85f6914-dbb8-42c9-a732-11d48613c15c
title: CIM_SnapshotOfVirtualSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SnapshotOfVirtualSystem
- CIM_SnapshotOfVirtualSystem.Antecedent
- CIM_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e8e0929f1198ececea5ea5ec144e2f7313ec35c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002381"
---
# <a name="cim_snapshotofvirtualsystem-class"></a><span data-ttu-id="22af2-103">\_Clase SnapshotOfVirtualSystem de CIM</span><span class="sxs-lookup"><span data-stu-id="22af2-103">CIM\_SnapshotOfVirtualSystem class</span></span>

<span data-ttu-id="22af2-104">Asocia un sistema virtual a una instantánea del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="22af2-104">Associates a virtual system a snapshot of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="22af2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22af2-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_SnapshotOfVirtualSystem : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="22af2-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="22af2-106">Members</span></span>

<span data-ttu-id="22af2-107">La clase **CIM \_ SnapshotOfVirtualSystem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="22af2-107">The **CIM\_SnapshotOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="22af2-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="22af2-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="22af2-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="22af2-109">Properties</span></span>

<span data-ttu-id="22af2-110">La clase **CIM \_ SnapshotOfVirtualSystem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="22af2-110">The **CIM\_SnapshotOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22af2-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="22af2-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22af2-112">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="22af2-112">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="22af2-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22af2-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22af2-114">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="22af2-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="22af2-115">Referencia al sistema del equipo que representa el sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="22af2-115">A reference to the computer system that represents the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="22af2-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="22af2-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22af2-117">Tipo de datos: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="22af2-117">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="22af2-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22af2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22af2-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="22af2-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="22af2-120">Referencia al objeto de datos de configuración que representa la instantánea del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="22af2-120">A reference to the settings data object that represents the snapshot of the virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22af2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22af2-121">Requirements</span></span>



| <span data-ttu-id="22af2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="22af2-122">Requirement</span></span> | <span data-ttu-id="22af2-123">Value</span><span class="sxs-lookup"><span data-stu-id="22af2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22af2-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22af2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="22af2-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="22af2-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="22af2-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22af2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="22af2-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="22af2-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="22af2-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="22af2-128">Namespace</span></span><br/>                | <span data-ttu-id="22af2-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="22af2-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="22af2-130">MOF</span><span class="sxs-lookup"><span data-stu-id="22af2-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22af2-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22af2-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="22af2-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="22af2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22af2-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="22af2-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="22af2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="22af2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22af2-135">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="22af2-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

