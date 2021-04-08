---
description: Asocia una instancia de un recurso asignado al nodo NUMA físico desde el que se asignó.
ms.assetid: 811ed19f-9084-4e30-8604-860d2bf722c7
title: Msvm_ElementAllocatedFromNumaNode (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromNumaNode
- Msvm_ElementAllocatedFromNumaNode.Antecedent
- Msvm_ElementAllocatedFromNumaNode.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98940306f25d46c6af1be31133ee336765f8f1a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911025"
---
# <a name="msvm_elementallocatedfromnumanode-class"></a><span data-ttu-id="1d991-103">MSVM \_ ElementAllocatedFromNumaNode (clase)</span><span class="sxs-lookup"><span data-stu-id="1d991-103">Msvm\_ElementAllocatedFromNumaNode class</span></span>

<span data-ttu-id="1d991-104">Asocia una instancia de un recurso asignado al nodo NUMA físico desde el que se asignó.</span><span class="sxs-lookup"><span data-stu-id="1d991-104">Associates an instance of an allocated resource with the physical NUMA node from which it was allocated.</span></span>

<span data-ttu-id="1d991-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1d991-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d991-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d991-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromNumaNode : CIM_Dependency
{
  Msvm_NumaNode      REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1d991-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1d991-107">Members</span></span>

<span data-ttu-id="1d991-108">La clase **MSVM \_ ElementAllocatedFromNumaNode** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1d991-108">The **Msvm\_ElementAllocatedFromNumaNode** class has these types of members:</span></span>

-   [<span data-ttu-id="1d991-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1d991-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d991-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1d991-110">Properties</span></span>

<span data-ttu-id="1d991-111">La clase **MSVM \_ ElementAllocatedFromNumaNode** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1d991-111">The **Msvm\_ElementAllocatedFromNumaNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d991-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="1d991-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d991-113">Tipo de datos: **[ **MSVM \_ NumaNode**](msvm-numanode.md)**</span><span class="sxs-lookup"><span data-stu-id="1d991-113">Data type: **[**Msvm\_NumaNode**](msvm-numanode.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1d991-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d991-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d991-115">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="1d991-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="1d991-116">Nodo NUMA físico.</span><span class="sxs-lookup"><span data-stu-id="1d991-116">The physical NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="1d991-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="1d991-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d991-118">Tipo de datos: **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span><span class="sxs-lookup"><span data-stu-id="1d991-118">Data type: **[**CIM\_LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span></span>
</dt> <dt>

<span data-ttu-id="1d991-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d991-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d991-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="1d991-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1d991-121">Recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="1d991-121">The allocated resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d991-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d991-122">Requirements</span></span>



| <span data-ttu-id="1d991-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d991-123">Requirement</span></span> | <span data-ttu-id="1d991-124">Value</span><span class="sxs-lookup"><span data-stu-id="1d991-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d991-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d991-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1d991-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d991-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1d991-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d991-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1d991-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d991-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1d991-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1d991-129">Namespace</span></span><br/>                | <span data-ttu-id="1d991-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1d991-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1d991-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1d991-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d991-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d991-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d991-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1d991-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d991-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1d991-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

