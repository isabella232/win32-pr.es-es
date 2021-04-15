---
description: Representa una asociación entre un servicio y el sistema que hospeda el servicio. Un sistema puede hospedar muchos servicios; sin embargo, esta clase no representa servicios hospedados en varios sistemas.
ms.assetid: ede67a81-cf1b-41aa-b907-5b635cf80423
title: CIM_HostedService (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Antecedent
- CIM_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 841c0e26898ed3baa4b4947779a395ee9ce870d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496907"
---
# <a name="cim_hostedservice-class-hyper-v-management"></a><span data-ttu-id="30b03-104">CIM_HostedService (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="30b03-104">CIM_HostedService class (Hyper-V management)</span></span>

<span data-ttu-id="30b03-105">Representa una asociación entre un servicio y el sistema que hospeda el servicio.</span><span class="sxs-lookup"><span data-stu-id="30b03-105">Represents an association between a service and the system that hosts the service.</span></span> <span data-ttu-id="30b03-106">Un sistema puede hospedar muchos servicios; sin embargo, esta clase no representa servicios hospedados en varios sistemas.</span><span class="sxs-lookup"><span data-stu-id="30b03-106">A System can host many services, however this class does not represent services hosted across multiple systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="30b03-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30b03-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_HostedService : CIM_HostedDependency
{
  CIM_System  REF Antecedent;
  CIM_Service REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="30b03-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="30b03-108">Members</span></span>

<span data-ttu-id="30b03-109">La clase **CIM \_ HostedService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="30b03-109">The **CIM\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="30b03-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="30b03-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30b03-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="30b03-111">Properties</span></span>

<span data-ttu-id="30b03-112">La clase **CIM \_ HostedService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="30b03-112">The **CIM\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30b03-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="30b03-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b03-114">Tipo de datos **: \_ Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="30b03-114">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="30b03-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="30b03-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30b03-116">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="30b03-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="30b03-117">Sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="30b03-117">The hosting System.</span></span>

</dd> <dt>

<span data-ttu-id="30b03-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="30b03-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30b03-119">Tipo de datos **: \_ servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="30b03-119">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="30b03-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="30b03-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30b03-121">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="30b03-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="30b03-122">El servicio hospedado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="30b03-122">The Service hosted on the System.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30b03-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30b03-123">Requirements</span></span>



| <span data-ttu-id="30b03-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="30b03-124">Requirement</span></span> | <span data-ttu-id="30b03-125">Value</span><span class="sxs-lookup"><span data-stu-id="30b03-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30b03-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30b03-126">Minimum supported client</span></span><br/> | <span data-ttu-id="30b03-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="30b03-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="30b03-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30b03-128">Minimum supported server</span></span><br/> | <span data-ttu-id="30b03-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="30b03-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="30b03-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="30b03-130">Namespace</span></span><br/>                | <span data-ttu-id="30b03-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="30b03-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="30b03-132">MOF</span><span class="sxs-lookup"><span data-stu-id="30b03-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30b03-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30b03-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="30b03-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="30b03-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30b03-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="30b03-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="30b03-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="30b03-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b03-137">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="30b03-137">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

