---
description: Representa una asociación entre una instancia de la clase de ComputerSystem de CIM \_ que representa la réplica de máquina virtual y una instancia de la clase de ComputerSystem de CIM \_ que representa la réplica de la máquina virtual de prueba.
ms.assetid: c3216ddd-7f70-4287-9f7e-1fd7a60b1a0a
title: Msvm_ReplicaSystemDependency (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicaSystemDependency
- Msvm_ReplicaSystemDependency.Antecedent
- Msvm_ReplicaSystemDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8c0db6e476cb883ee1179fcfcc9ac4b212f0b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277048"
---
# <a name="msvm_replicasystemdependency-class"></a><span data-ttu-id="17e4d-103">MSVM \_ ReplicaSystemDependency (clase)</span><span class="sxs-lookup"><span data-stu-id="17e4d-103">Msvm\_ReplicaSystemDependency class</span></span>

<span data-ttu-id="17e4d-104">Representa una asociación entre una instancia de la clase de [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la réplica de máquina virtual y una instancia de la clase de **\_ ComputerSystem de CIM** que representa la réplica de la máquina virtual de prueba.</span><span class="sxs-lookup"><span data-stu-id="17e4d-104">Represents an association between an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine replica and an instance of the **CIM\_ComputerSystem** class that represents the test virtual machine replica.</span></span>

<span data-ttu-id="17e4d-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="17e4d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e4d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17e4d-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicaSystemDependency : CIM_Dependency
{
  CIM_ComputerSystem REF Antecedent;
  CIM_ComputerSystem REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="17e4d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="17e4d-107">Members</span></span>

<span data-ttu-id="17e4d-108">La clase **MSVM \_ ReplicaSystemDependency** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="17e4d-108">The **Msvm\_ReplicaSystemDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="17e4d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17e4d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17e4d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17e4d-110">Properties</span></span>

<span data-ttu-id="17e4d-111">La clase **MSVM \_ ReplicaSystemDependency** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="17e4d-111">The **Msvm\_ReplicaSystemDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17e4d-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="17e4d-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17e4d-113">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="17e4d-113">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="17e4d-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17e4d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17e4d-115">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. antecedente")</span><span class="sxs-lookup"><span data-stu-id="17e4d-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="17e4d-116">Referencia a una instancia de la clase [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la réplica de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="17e4d-116">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine replica.</span></span> <span data-ttu-id="17e4d-117">Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="17e4d-117">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="17e4d-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="17e4d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17e4d-119">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="17e4d-119">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="17e4d-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17e4d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17e4d-121">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Dependent")</span><span class="sxs-lookup"><span data-stu-id="17e4d-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="17e4d-122">Una referencia a una instancia de la clase de [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la réplica de la máquina virtual de prueba creada por el método [**MSVM \_ ReplicationService. TestReplicaSystem**](testreplicasystem-msvm-replicationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="17e4d-122">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the test virtual machine replica created by the [**Msvm\_ReplicationService.TestReplicaSystem**](testreplicasystem-msvm-replicationservice.md) method.</span></span> <span data-ttu-id="17e4d-123">Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="17e4d-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17e4d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17e4d-124">Requirements</span></span>



| <span data-ttu-id="17e4d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="17e4d-125">Requirement</span></span> | <span data-ttu-id="17e4d-126">Value</span><span class="sxs-lookup"><span data-stu-id="17e4d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17e4d-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17e4d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="17e4d-128">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="17e4d-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="17e4d-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17e4d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="17e4d-130">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="17e4d-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="17e4d-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="17e4d-131">Namespace</span></span><br/>                | <span data-ttu-id="17e4d-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="17e4d-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="17e4d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="17e4d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17e4d-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17e4d-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="17e4d-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="17e4d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17e4d-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="17e4d-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

