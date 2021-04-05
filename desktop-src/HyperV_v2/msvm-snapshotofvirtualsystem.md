---
description: Asocia un sistema virtual a una instantánea que se capturó del sistema virtual.
ms.assetid: CF1C1C04-02BC-4AC3-8327-FEE54ECE8541
title: Msvm_SnapshotOfVirtualSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystem
- Msvm_SnapshotOfVirtualSystem.Antecedent
- Msvm_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bd006093347d7eb9354944409082a0e069b0cd54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001491"
---
# <a name="msvm_snapshotofvirtualsystem-class"></a><span data-ttu-id="70a4d-103">MSVM \_ SnapshotOfVirtualSystem (clase)</span><span class="sxs-lookup"><span data-stu-id="70a4d-103">Msvm\_SnapshotOfVirtualSystem class</span></span>

<span data-ttu-id="70a4d-104">Asocia un sistema virtual a una instantánea que se capturó del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="70a4d-104">Associates a virtual system with a snapshot that was captured from the virtual system.</span></span>

<span data-ttu-id="70a4d-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="70a4d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a4d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70a4d-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystem : CIM_SnapshotOfVirtualSystem
{
  Msvm_ComputerSystem           REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="70a4d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="70a4d-107">Members</span></span>

<span data-ttu-id="70a4d-108">La clase **MSVM \_ SnapshotOfVirtualSystem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="70a4d-108">The **Msvm\_SnapshotOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="70a4d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="70a4d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70a4d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="70a4d-110">Properties</span></span>

<span data-ttu-id="70a4d-111">La clase **MSVM \_ SnapshotOfVirtualSystem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="70a4d-111">The **Msvm\_SnapshotOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70a4d-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="70a4d-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a4d-113">Tipo de datos: **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="70a4d-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="70a4d-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70a4d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70a4d-115">Referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa el sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="70a4d-115">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual system.</span></span> <span data-ttu-id="70a4d-116">Esta propiedad se deriva de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="70a4d-116">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="70a4d-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="70a4d-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a4d-118">Tipo de datos: **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="70a4d-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="70a4d-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70a4d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70a4d-120">Referencia a una instancia de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa la instantánea.</span><span class="sxs-lookup"><span data-stu-id="70a4d-120">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the snapshot.</span></span> <span data-ttu-id="70a4d-121">Esta propiedad se deriva de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="70a4d-121">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70a4d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70a4d-122">Requirements</span></span>



| <span data-ttu-id="70a4d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="70a4d-123">Requirement</span></span> | <span data-ttu-id="70a4d-124">Value</span><span class="sxs-lookup"><span data-stu-id="70a4d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70a4d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70a4d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="70a4d-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="70a4d-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="70a4d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70a4d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="70a4d-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="70a4d-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70a4d-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="70a4d-129">Namespace</span></span><br/>                | <span data-ttu-id="70a4d-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="70a4d-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="70a4d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="70a4d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70a4d-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70a4d-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="70a4d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="70a4d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70a4d-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="70a4d-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="70a4d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="70a4d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70a4d-136">**\_SNAPSHOTOFVIRTUALSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="70a4d-136">**CIM\_SnapshotOfVirtualSystem**</span></span>](cim-snapshotofvirtualsystem.md)
</dt> <dt>

[<span data-ttu-id="70a4d-137">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="70a4d-137">**CreateSnapshot**</span></span>](createsnapshot-msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

