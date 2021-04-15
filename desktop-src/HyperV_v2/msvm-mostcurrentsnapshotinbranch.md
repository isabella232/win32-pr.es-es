---
description: Asocia una instancia de la \_ clase MSVM ComputerSystem o MSVM \_ PlannedComputerSystem que representa un sistema virtual, con una instancia de la \_ clase MSVM VirtualSystemSettingData que representa la instantánea del sistema virtual que es la instantánea más reciente de una rama de instantáneas dependientes.
ms.assetid: EEB9D2C1-C463-4EFE-862F-95E8AD8E1753
title: Msvm_MostCurrentSnapshotInBranch (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MostCurrentSnapshotInBranch
- Msvm_MostCurrentSnapshotInBranch.Antecedent
- Msvm_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3ed0824fd68670245e2c8d09b73733ff23be16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669768"
---
# <a name="msvm_mostcurrentsnapshotinbranch-class"></a><span data-ttu-id="f5b87-103">MSVM \_ MostCurrentSnapshotInBranch (clase)</span><span class="sxs-lookup"><span data-stu-id="f5b87-103">Msvm\_MostCurrentSnapshotInBranch class</span></span>

<span data-ttu-id="f5b87-104">Asocia una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) o [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) que representa un sistema virtual, con una instancia de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa la instantánea del sistema virtual que es la instantánea más reciente de una rama de instantáneas dependientes.</span><span class="sxs-lookup"><span data-stu-id="f5b87-104">Associates an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) or [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) class representing a virtual system, with an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class representing the virtual system snapshot that is the most current snapshot in a branch of dependent snapshots.</span></span>

<span data-ttu-id="f5b87-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f5b87-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5b87-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5b87-106">Syntax</span></span>

``` syntax
[Association, Experimental, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MostCurrentSnapshotInBranch : CIM_MostCurrentSnapshotInBranch
{
  CIM_ComputerSystem            REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f5b87-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f5b87-107">Members</span></span>

<span data-ttu-id="f5b87-108">La clase **MSVM \_ MostCurrentSnapshotInBranch** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f5b87-108">The **Msvm\_MostCurrentSnapshotInBranch** class has these types of members:</span></span>

-   [<span data-ttu-id="f5b87-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f5b87-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5b87-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f5b87-110">Properties</span></span>

<span data-ttu-id="f5b87-111">La clase **MSVM \_ MostCurrentSnapshotInBranch** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f5b87-111">The **Msvm\_MostCurrentSnapshotInBranch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5b87-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="f5b87-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5b87-113">Tipo de datos: **[ **CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="f5b87-113">Data type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>
</dt> <dt>

<span data-ttu-id="f5b87-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5b87-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5b87-115">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="f5b87-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f5b87-116">Referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) o [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) que representa el sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="f5b87-116">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) or [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) class representing the virtual system.</span></span> <span data-ttu-id="f5b87-117">Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="f5b87-117">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="f5b87-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="f5b87-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5b87-119">Tipo de datos: **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="f5b87-119">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f5b87-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5b87-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5b87-121">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="f5b87-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f5b87-122">Referencia a una instancia de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa la instantánea del sistema virtual que es la instantánea más reciente de una rama de instantáneas dependientes.</span><span class="sxs-lookup"><span data-stu-id="f5b87-122">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the virtual system snapshot that is the most current snapshot in a branch of dependent snapshots.</span></span> <span data-ttu-id="f5b87-123">Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="f5b87-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5b87-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5b87-124">Requirements</span></span>



| <span data-ttu-id="f5b87-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5b87-125">Requirement</span></span> | <span data-ttu-id="f5b87-126">Value</span><span class="sxs-lookup"><span data-stu-id="f5b87-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b87-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5b87-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f5b87-128">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5b87-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f5b87-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5b87-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f5b87-130">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5b87-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f5b87-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f5b87-131">Namespace</span></span><br/>                | <span data-ttu-id="f5b87-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f5b87-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f5b87-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f5b87-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5b87-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5b87-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5b87-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f5b87-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5b87-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f5b87-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

