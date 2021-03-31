---
description: Asocia una instancia de máquina virtual con el objeto de sistema de equipo que representa el sistema de hospedaje físico.
ms.assetid: 755624D7-04D0-47EA-8623-DEDE6B1D5CBC
title: Msvm_HostedDependency (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedDependency
- Msvm_HostedDependency.Antecedent
- Msvm_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ce580e6b478dbdf320377c2738708d0eb7689fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907702"
---
# <a name="msvm_hosteddependency-class"></a><span data-ttu-id="23764-103">MSVM \_ HostedDependency (clase)</span><span class="sxs-lookup"><span data-stu-id="23764-103">Msvm\_HostedDependency class</span></span>

<span data-ttu-id="23764-104">Asocia una instancia de máquina virtual con el objeto de sistema de equipo que representa el sistema de hospedaje físico.</span><span class="sxs-lookup"><span data-stu-id="23764-104">Associates a virtual machine instance with the computer system object that represents the physical, hosting system.</span></span>

<span data-ttu-id="23764-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="23764-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="23764-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23764-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedDependency : CIM_HostedDependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="23764-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="23764-107">Members</span></span>

<span data-ttu-id="23764-108">La clase **MSVM \_ HostedDependency** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="23764-108">The **Msvm\_HostedDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="23764-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="23764-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23764-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="23764-110">Properties</span></span>

<span data-ttu-id="23764-111">La clase **MSVM \_ HostedDependency** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="23764-111">The **Msvm\_HostedDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23764-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="23764-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23764-113">Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="23764-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="23764-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23764-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23764-115">Referencia al sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="23764-115">A reference to the hosting computer system.</span></span> <span data-ttu-id="23764-116">Esta propiedad se hereda de [**\_ HostedDependency CIM**](/previous-versions//cc136861(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="23764-116">This property is inherited from [**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="23764-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="23764-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23764-118">Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="23764-118">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="23764-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23764-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23764-120">Referencia a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="23764-120">A reference to the virtual machine.</span></span> <span data-ttu-id="23764-121">Esta propiedad se hereda de [**\_ HostedDependency CIM**](/previous-versions//cc136861(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="23764-121">This property is inherited from [**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23764-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23764-122">Remarks</span></span>

<span data-ttu-id="23764-123">El acceso a la clase **MSVM \_ HostedDependency** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="23764-123">Access to the **Msvm\_HostedDependency** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="23764-124">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="23764-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="23764-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23764-125">Requirements</span></span>



| <span data-ttu-id="23764-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="23764-126">Requirement</span></span> | <span data-ttu-id="23764-127">Value</span><span class="sxs-lookup"><span data-stu-id="23764-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23764-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23764-128">Minimum supported client</span></span><br/> | <span data-ttu-id="23764-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="23764-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="23764-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23764-130">Minimum supported server</span></span><br/> | <span data-ttu-id="23764-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="23764-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23764-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="23764-132">Namespace</span></span><br/>                | <span data-ttu-id="23764-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="23764-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="23764-134">MOF</span><span class="sxs-lookup"><span data-stu-id="23764-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23764-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23764-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="23764-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23764-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23764-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="23764-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="23764-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="23764-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23764-139">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="23764-139">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> <dt>

<span data-ttu-id="23764-140">[**\_HOSTEDDEPENDENCY CIM**](/previous-versions//cc136861(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="23764-140">[**CIM\_HostedDependency**](/previous-versions//cc136861(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="23764-141">Clases de administración de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="23764-141">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

