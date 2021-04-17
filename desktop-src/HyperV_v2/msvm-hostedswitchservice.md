---
description: Asociación que conecta un servicio de conmutador virtual a un servicio de puente transparente.
ms.assetid: 4DFD73CA-38F0-4C06-BEBE-C684590E50E8
title: Msvm_HostedSwitchService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedSwitchService
- Msvm_HostedSwitchService.Antecedent
- Msvm_HostedSwitchService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0b7319dbe58649ac7abce2d36201f3984c1b807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666333"
---
# <a name="msvm_hostedswitchservice-class"></a><span data-ttu-id="42e10-103">MSVM \_ HostedSwitchService (clase)</span><span class="sxs-lookup"><span data-stu-id="42e10-103">Msvm\_HostedSwitchService class</span></span>

<span data-ttu-id="42e10-104">Asociación que conecta un servicio de conmutador virtual a un servicio de puente transparente.</span><span class="sxs-lookup"><span data-stu-id="42e10-104">An association that connects a virtual switch service to a transparent bridging service.</span></span>

<span data-ttu-id="42e10-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="42e10-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="42e10-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42e10-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedSwitchService : CIM_HostedService
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  CIM_Service                REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="42e10-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="42e10-107">Members</span></span>

<span data-ttu-id="42e10-108">La clase **MSVM \_ HostedSwitchService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="42e10-108">The **Msvm\_HostedSwitchService** class has these types of members:</span></span>

-   [<span data-ttu-id="42e10-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42e10-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42e10-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42e10-110">Properties</span></span>

<span data-ttu-id="42e10-111">La clase **MSVM \_ HostedSwitchService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="42e10-111">The **Msvm\_HostedSwitchService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42e10-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="42e10-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42e10-113">Tipo de datos: **[ **MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span><span class="sxs-lookup"><span data-stu-id="42e10-113">Data type: **[**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**</span></span>
</dt> <dt>

<span data-ttu-id="42e10-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42e10-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42e10-115">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="42e10-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="42e10-116">Referencia a una instancia de la clase [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) que representa el conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="42e10-116">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="42e10-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="42e10-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42e10-118">Tipo de datos: **[ **\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="42e10-118">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="42e10-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42e10-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42e10-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="42e10-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="42e10-121">Referencia a una instancia de la clase [**MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) que representa el servicio de puente.</span><span class="sxs-lookup"><span data-stu-id="42e10-121">A reference to an instance of the [**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md) class that represents the bridging service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42e10-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42e10-122">Remarks</span></span>

<span data-ttu-id="42e10-123">El acceso a la clase **MSVM \_ HostedSwitchService** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="42e10-123">Access to the **Msvm\_HostedSwitchService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="42e10-124">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="42e10-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="42e10-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42e10-125">Requirements</span></span>



| <span data-ttu-id="42e10-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="42e10-126">Requirement</span></span> | <span data-ttu-id="42e10-127">Value</span><span class="sxs-lookup"><span data-stu-id="42e10-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42e10-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42e10-128">Minimum supported client</span></span><br/> | <span data-ttu-id="42e10-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="42e10-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="42e10-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42e10-130">Minimum supported server</span></span><br/> | <span data-ttu-id="42e10-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="42e10-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42e10-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="42e10-132">Namespace</span></span><br/>                | <span data-ttu-id="42e10-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="42e10-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="42e10-134">MOF</span><span class="sxs-lookup"><span data-stu-id="42e10-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42e10-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42e10-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42e10-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42e10-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42e10-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42e10-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="42e10-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="42e10-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42e10-139">**HostedService de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="42e10-139">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dt>

[<span data-ttu-id="42e10-140">**HostedService de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="42e10-140">**CIM\_HostedService**</span></span>](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> </dl>

 

