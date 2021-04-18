---
description: Asocia una instancia de una asignación de recursos al grupo de recursos desde el que se asigna.
ms.assetid: A2B3996D-7886-4B5F-BC89-EFDC1A48249B
title: Msvm_ResourceAllocationFromPool (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationFromPool
- Msvm_ResourceAllocationFromPool.Antecedent
- Msvm_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5bb3db9bce86731b12730966a7a2f6d1c9dc8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687777"
---
# <a name="msvm_resourceallocationfrompool-class"></a><span data-ttu-id="f5459-103">MSVM \_ ResourceAllocationFromPool (clase)</span><span class="sxs-lookup"><span data-stu-id="f5459-103">Msvm\_ResourceAllocationFromPool class</span></span>

<span data-ttu-id="f5459-104">Asocia una instancia de una asignación de recursos al grupo de recursos desde el que se asigna.</span><span class="sxs-lookup"><span data-stu-id="f5459-104">Associates an instance of a resource allocation with the resource pool from which it is allocated.</span></span>

<span data-ttu-id="f5459-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f5459-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5459-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5459-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationFromPool : CIM_ResourceAllocationFromPool
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f5459-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f5459-107">Members</span></span>

<span data-ttu-id="f5459-108">La clase **MSVM \_ ResourceAllocationFromPool** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f5459-108">The **Msvm\_ResourceAllocationFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="f5459-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f5459-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5459-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f5459-110">Properties</span></span>

<span data-ttu-id="f5459-111">La clase **MSVM \_ ResourceAllocationFromPool** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f5459-111">The **Msvm\_ResourceAllocationFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5459-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="f5459-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5459-113">Tipo de datos: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="f5459-113">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="f5459-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5459-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5459-115">Calificadores: **invalidación**, **máx** . (1)</span><span class="sxs-lookup"><span data-stu-id="f5459-115">Qualifiers: **Override**, **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="f5459-116">Grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f5459-116">The resource pool.</span></span> <span data-ttu-id="f5459-117">Esta propiedad se hereda de [**\_ ResourceAllocationFromPool CIM**](/previous-versions//cc150673(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f5459-117">This property is inherited from [**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f5459-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="f5459-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5459-119">Tipo de datos: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="f5459-119">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="f5459-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f5459-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5459-121">Asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="f5459-121">The resource allocation.</span></span> <span data-ttu-id="f5459-122">Esta propiedad se hereda de [**\_ ResourceAllocationFromPool CIM**](/previous-versions//cc150673(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f5459-122">This property is inherited from [**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5459-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5459-123">Remarks</span></span>

<span data-ttu-id="f5459-124">El acceso a la clase **MSVM \_ ResourceAllocationFromPool** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="f5459-124">Access to the **Msvm\_ResourceAllocationFromPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f5459-125">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f5459-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5459-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5459-126">Requirements</span></span>



| <span data-ttu-id="f5459-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5459-127">Requirement</span></span> | <span data-ttu-id="f5459-128">Value</span><span class="sxs-lookup"><span data-stu-id="f5459-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5459-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5459-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f5459-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5459-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f5459-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5459-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f5459-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5459-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f5459-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f5459-133">Namespace</span></span><br/>                | <span data-ttu-id="f5459-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f5459-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f5459-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f5459-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5459-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5459-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5459-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f5459-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5459-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f5459-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f5459-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5459-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5459-140">**\_RESOURCEALLOCATIONFROMPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="f5459-140">**CIM\_ResourceAllocationFromPool**</span></span>](cim-resourceallocationfrompool.md)
</dt> <dt>

<span data-ttu-id="f5459-141">[**\_RESOURCEALLOCATIONFROMPOOL CIM**](/previous-versions//cc150673(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5459-141">[**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f5459-142">**MSVM \_ ResourceAllocationFromPool (V1)**</span><span class="sxs-lookup"><span data-stu-id="f5459-142">**Msvm\_ResourceAllocationFromPool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourceallocationfrompool)
</dt> <dt>

[<span data-ttu-id="f5459-143">Clases de administración de recursos</span><span class="sxs-lookup"><span data-stu-id="f5459-143">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

