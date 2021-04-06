---
description: Representa una asociación entre una instancia de MSVM \_ ComputerSystem que representa la máquina virtual y una instancia de MSVM \_ ReplicationRelationship que representa una relación de replicación de la máquina virtual.
ms.assetid: 23E7BF91-9527-434C-A571-05879E83950E
title: Msvm_SystemReplicationRelationship (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemReplicationRelationship
- Msvm_SystemReplicationRelationship.Antecedent
- Msvm_SystemReplicationRelationship.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dd5ada4eef811a7d542c01c0a3be66d53cca0916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000958"
---
# <a name="msvm_systemreplicationrelationship-class"></a><span data-ttu-id="a0289-103">MSVM \_ SystemReplicationRelationship (clase)</span><span class="sxs-lookup"><span data-stu-id="a0289-103">Msvm\_SystemReplicationRelationship class</span></span>

<span data-ttu-id="a0289-104">Representa una asociación entre una instancia de [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa la máquina virtual y una instancia de [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) que representa una relación de replicación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a0289-104">Represents an association between an instance of [**Msvm\_ComputerSystem**](msvm-computersystem.md) that represents the virtual machine and an instance of [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) that represents a replication relationship of the virtual machine.</span></span> <span data-ttu-id="a0289-105">Esta clase se deriva de la clase de [**\_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency) .</span><span class="sxs-lookup"><span data-stu-id="a0289-105">This class derives from the [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency) class.</span></span>

<span data-ttu-id="a0289-106">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a0289-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0289-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0289-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemReplicationRelationship : CIM_Dependency
{
  Msvm_ComputerSystem          REF Antecedent;
  Msvm_ReplicationRelationship REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="a0289-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0289-108">Members</span></span>

<span data-ttu-id="a0289-109">La clase **MSVM \_ SystemReplicationRelationship** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a0289-109">The **Msvm\_SystemReplicationRelationship** class has these types of members:</span></span>

-   [<span data-ttu-id="a0289-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0289-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a0289-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0289-111">Properties</span></span>

<span data-ttu-id="a0289-112">La clase **MSVM \_ SystemReplicationRelationship** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a0289-112">The **Msvm\_SystemReplicationRelationship** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0289-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="a0289-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0289-114">Tipo de datos: **MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="a0289-114">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a0289-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0289-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0289-116">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. antecedente")</span><span class="sxs-lookup"><span data-stu-id="a0289-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a0289-117">Referencia a la instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a0289-117">Reference to the instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="a0289-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="a0289-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0289-119">Tipo de datos: **MSVM \_ ReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="a0289-119">Data type: **Msvm\_ReplicationRelationship**</span></span>
</dt> <dt>

<span data-ttu-id="a0289-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0289-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0289-121">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Dependent")</span><span class="sxs-lookup"><span data-stu-id="a0289-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a0289-122">Referencia a la instancia de la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) que representa la relación de replicación de un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="a0289-122">Reference to the instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that represents the replication relationship of a virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0289-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0289-123">Requirements</span></span>



| <span data-ttu-id="a0289-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0289-124">Requirement</span></span> | <span data-ttu-id="a0289-125">Value</span><span class="sxs-lookup"><span data-stu-id="a0289-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0289-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0289-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a0289-127">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="a0289-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a0289-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0289-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a0289-129">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a0289-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a0289-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a0289-130">Namespace</span></span><br/>                | <span data-ttu-id="a0289-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a0289-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a0289-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a0289-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0289-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0289-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0289-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a0289-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0289-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a0289-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a0289-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0289-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0289-137">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a0289-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="a0289-138">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a0289-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

