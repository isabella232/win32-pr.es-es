---
description: Representa una asociación entre un punto de acceso de servicio (SAP) y el sistema que lo hospeda.
ms.assetid: 82db71d6-6d14-408e-87e0-fe869e454d4d
title: CIM_HostedAccessPoint (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Antecedent
- CIM_HostedAccessPoint.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0684c2855e7966a0c01d1d9f9bfa0cbd71c2397a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496912"
---
# <a name="cim_hostedaccesspoint-class-hyper-v-management"></a><span data-ttu-id="9fb24-103">CIM_HostedAccessPoint (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="9fb24-103">CIM_HostedAccessPoint class (Hyper-V management)</span></span>

<span data-ttu-id="9fb24-104">Representa una asociación entre un punto de acceso de servicio (SAP) y el sistema que lo hospeda.</span><span class="sxs-lookup"><span data-stu-id="9fb24-104">Represents an association between a service access point (SAP) and the system that hosts it.</span></span> <span data-ttu-id="9fb24-105">Un sistema puede hospedar varios puntos de acceso.</span><span class="sxs-lookup"><span data-stu-id="9fb24-105">A system can host multiple access points.</span></span> <span data-ttu-id="9fb24-106">Si se modela la implementación de SAP, debe implementarse mediante una característica de dispositivo o software que forme parte del sistema que hospeda SAP.</span><span class="sxs-lookup"><span data-stu-id="9fb24-106">If the implementation of the SAP is modeled, it must be implemented by a device or software feature that is part of the system that hosts the SAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb24-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fb24-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_HostedAccessPoint : CIM_HostedDependency
{
  CIM_System             REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9fb24-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9fb24-108">Members</span></span>

<span data-ttu-id="9fb24-109">La clase **CIM \_ HostedAccessPoint** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9fb24-109">The **CIM\_HostedAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="9fb24-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9fb24-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9fb24-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9fb24-111">Properties</span></span>

<span data-ttu-id="9fb24-112">La clase **CIM \_ HostedAccessPoint** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9fb24-112">The **CIM\_HostedAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9fb24-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="9fb24-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb24-114">Tipo de datos **: \_ Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="9fb24-114">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="9fb24-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb24-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb24-116">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="9fb24-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="9fb24-117">Sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="9fb24-117">The hosting System.</span></span>

</dd> <dt>

<span data-ttu-id="9fb24-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="9fb24-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fb24-119">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="9fb24-119">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="9fb24-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fb24-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fb24-121">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9fb24-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9fb24-122">Los SAP que se hospedan en el sistema.</span><span class="sxs-lookup"><span data-stu-id="9fb24-122">The SAPs that are hosted on the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9fb24-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fb24-123">Requirements</span></span>



| <span data-ttu-id="9fb24-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fb24-124">Requirement</span></span> | <span data-ttu-id="9fb24-125">Value</span><span class="sxs-lookup"><span data-stu-id="9fb24-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb24-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fb24-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9fb24-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9fb24-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9fb24-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fb24-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9fb24-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9fb24-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9fb24-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9fb24-130">Namespace</span></span><br/>                | <span data-ttu-id="9fb24-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9fb24-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9fb24-132">MOF</span><span class="sxs-lookup"><span data-stu-id="9fb24-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fb24-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fb24-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fb24-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9fb24-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fb24-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9fb24-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9fb24-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fb24-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fb24-137">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="9fb24-137">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

