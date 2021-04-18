---
description: Asocia una instancia de un recurso asignado al grupo de recursos desde el que se asignó.
ms.assetid: BA3168C7-E4F1-414B-827B-1A811069F223
title: Msvm_ElementAllocatedFromPool (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromPool
- Msvm_ElementAllocatedFromPool.Antecedent
- Msvm_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4d798c31fbcd8429007c53f3b156fc7c5922e7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687950"
---
# <a name="msvm_elementallocatedfrompool-class"></a><span data-ttu-id="c7eaa-103">MSVM \_ ElementAllocatedFromPool (clase)</span><span class="sxs-lookup"><span data-stu-id="c7eaa-103">Msvm\_ElementAllocatedFromPool class</span></span>

<span data-ttu-id="c7eaa-104">Asocia una instancia de un recurso asignado al grupo de recursos desde el que se asignó.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-104">Associates an instance of an allocated resource with the resource pool from which it was allocated.</span></span>

<span data-ttu-id="c7eaa-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7eaa-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7eaa-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromPool : CIM_ElementAllocatedFromPool
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c7eaa-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c7eaa-107">Members</span></span>

<span data-ttu-id="c7eaa-108">La clase **MSVM \_ ElementAllocatedFromPool** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c7eaa-108">The **Msvm\_ElementAllocatedFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="c7eaa-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c7eaa-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7eaa-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c7eaa-110">Properties</span></span>

<span data-ttu-id="c7eaa-111">La clase **MSVM \_ ElementAllocatedFromPool** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-111">The **Msvm\_ElementAllocatedFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7eaa-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="c7eaa-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7eaa-113">Tipo de datos: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="c7eaa-113">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="c7eaa-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7eaa-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7eaa-115">Calificadores: **invalidación**, **máx** . (1)</span><span class="sxs-lookup"><span data-stu-id="c7eaa-115">Qualifiers: **Override**, **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="c7eaa-116">Grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-116">The resource pool.</span></span> <span data-ttu-id="c7eaa-117">Esta propiedad se hereda de [**\_ ElementAllocatedFromPool CIM**](/previous-versions//cc150668(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7eaa-117">This property is inherited from [**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7eaa-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="c7eaa-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7eaa-119">Tipo de datos: **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span><span class="sxs-lookup"><span data-stu-id="c7eaa-119">Data type: **[**CIM\_LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span></span>
</dt> <dt>

<span data-ttu-id="c7eaa-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c7eaa-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7eaa-121">Recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-121">The allocated resource.</span></span> <span data-ttu-id="c7eaa-122">Esta propiedad se hereda de [**\_ ElementAllocatedFromPool CIM**](/previous-versions//cc150668(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7eaa-122">This property is inherited from [**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7eaa-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7eaa-123">Remarks</span></span>

<span data-ttu-id="c7eaa-124">El acceso a la clase **MSVM \_ ElementAllocatedFromPool** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="c7eaa-124">Access to the **Msvm\_ElementAllocatedFromPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c7eaa-125">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c7eaa-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7eaa-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7eaa-126">Requirements</span></span>



| <span data-ttu-id="c7eaa-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7eaa-127">Requirement</span></span> | <span data-ttu-id="c7eaa-128">Value</span><span class="sxs-lookup"><span data-stu-id="c7eaa-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7eaa-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7eaa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c7eaa-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c7eaa-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c7eaa-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7eaa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c7eaa-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c7eaa-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7eaa-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c7eaa-133">Namespace</span></span><br/>                | <span data-ttu-id="c7eaa-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c7eaa-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c7eaa-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c7eaa-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7eaa-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7eaa-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7eaa-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7eaa-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7eaa-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7eaa-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c7eaa-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7eaa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7eaa-140">**\_ELEMENTALLOCATEDFROMPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="c7eaa-140">**CIM\_ElementAllocatedFromPool**</span></span>](cim-elementallocatedfrompool.md)
</dt> <dt>

<span data-ttu-id="c7eaa-141">[**\_ELEMENTALLOCATEDFROMPOOL CIM**](/previous-versions//cc150668(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c7eaa-141">[**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c7eaa-142">**MSVM \_ ElementAllocatedFromPool (V1)**</span><span class="sxs-lookup"><span data-stu-id="c7eaa-142">**Msvm\_ElementAllocatedFromPool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-elementallocatedfrompool)
</dt> <dt>

[<span data-ttu-id="c7eaa-143">Clases de administración de recursos</span><span class="sxs-lookup"><span data-stu-id="c7eaa-143">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

