---
description: Asocia un servicio a su sistema de hospedaje.
ms.assetid: 888ABA71-6D67-4933-89E6-40F731AA7153
title: Msvm_HostedService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedService
- Msvm_HostedService.Antecedent
- Msvm_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 284254d32e788e374d56b3822f5c00868552e1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686946"
---
# <a name="msvm_hostedservice-class"></a><span data-ttu-id="2b8d3-103">MSVM \_ HostedService (clase)</span><span class="sxs-lookup"><span data-stu-id="2b8d3-103">Msvm\_HostedService class</span></span>

<span data-ttu-id="2b8d3-104">Asocia un servicio a su sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-104">Associates a service with its hosting computer system.</span></span> <span data-ttu-id="2b8d3-105">Las instancias de [**MSVM \_ VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) se pueden detectar a través de su asociación con un host.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-105">Instances of [**Msvm\_VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) can be discovered through their association with a host.</span></span>

<span data-ttu-id="2b8d3-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b8d3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b8d3-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedService : CIM_HostedService
{
  CIM_ManagedElement REF Antecedent;
  CIM_Service        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2b8d3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2b8d3-108">Members</span></span>

<span data-ttu-id="2b8d3-109">La clase **MSVM \_ HostedService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2b8d3-109">The **Msvm\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="2b8d3-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2b8d3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b8d3-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2b8d3-111">Properties</span></span>

<span data-ttu-id="2b8d3-112">La clase **MSVM \_ HostedService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-112">The **Msvm\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b8d3-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="2b8d3-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b8d3-114">Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="2b8d3-114">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="2b8d3-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2b8d3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b8d3-116">Referencia al sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-116">A reference to the hosting computer system.</span></span> <span data-ttu-id="2b8d3-117">Esta propiedad se hereda de [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span><span class="sxs-lookup"><span data-stu-id="2b8d3-117">This property is inherited from [**CIM\_HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span></span>

</dd> <dt>

<span data-ttu-id="2b8d3-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="2b8d3-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b8d3-119">Tipo de datos: **[ **\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="2b8d3-119">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="2b8d3-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2b8d3-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b8d3-121">Referencia al servicio que se hospeda.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-121">A reference to the service being hosted.</span></span> <span data-ttu-id="2b8d3-122">Esta propiedad se hereda de [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span><span class="sxs-lookup"><span data-stu-id="2b8d3-122">This property is inherited from [**CIM\_HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b8d3-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b8d3-123">Remarks</span></span>

<span data-ttu-id="2b8d3-124">El acceso a la clase **MSVM \_ HostedService** podría estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="2b8d3-124">Access to the **Msvm\_HostedService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2b8d3-125">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2b8d3-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="2b8d3-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2b8d3-126">Examples</span></span>

<span data-ttu-id="2b8d3-127">Consulte [consultar objetos de red](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2b8d3-127">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b8d3-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b8d3-128">Requirements</span></span>



| <span data-ttu-id="2b8d3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b8d3-129">Requirement</span></span> | <span data-ttu-id="2b8d3-130">Value</span><span class="sxs-lookup"><span data-stu-id="2b8d3-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b8d3-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b8d3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2b8d3-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b8d3-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2b8d3-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b8d3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2b8d3-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b8d3-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2b8d3-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2b8d3-135">Namespace</span></span><br/>                | <span data-ttu-id="2b8d3-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2b8d3-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2b8d3-137">MOF</span><span class="sxs-lookup"><span data-stu-id="2b8d3-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b8d3-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b8d3-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b8d3-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b8d3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b8d3-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2b8d3-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2b8d3-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b8d3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b8d3-142">**HostedService de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2b8d3-142">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dt>

[<span data-ttu-id="2b8d3-143">**HostedService de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2b8d3-143">**CIM\_HostedService**</span></span>](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> <dt>

[<span data-ttu-id="2b8d3-144">Clases de administración de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="2b8d3-144">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

