---
description: Representa una asociación entre un servicio y un punto de acceso de servicio (SAP) que proporciona el servicio con funcionalidad.
ms.assetid: 9b82fad2-9731-4e0d-bdb0-d1be13ea20fc
title: CIM_ServiceSAPDependency (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Antecedent
- CIM_ServiceSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d49b63dfb37dfddf009f01122f4aa49af316fa58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667686"
---
# <a name="cim_servicesapdependency-class-hyper-v-management"></a><span data-ttu-id="28447-103">CIM_ServiceSAPDependency (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="28447-103">CIM_ServiceSAPDependency class (Hyper-V management)</span></span>

<span data-ttu-id="28447-104">Representa una asociación entre un servicio y un punto de acceso de servicio (SAP) que proporciona el servicio con funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="28447-104">Represents an association between a service and a service access point (SAP) that provides the service with functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="28447-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28447-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_Service            REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="28447-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="28447-106">Members</span></span>

<span data-ttu-id="28447-107">La clase **CIM \_ ServiceSAPDependency** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="28447-107">The **CIM\_ServiceSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="28447-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="28447-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="28447-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="28447-109">Properties</span></span>

<span data-ttu-id="28447-110">La clase **CIM \_ ServiceSAPDependency** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="28447-110">The **CIM\_ServiceSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="28447-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="28447-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28447-112">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="28447-112">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="28447-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="28447-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28447-114">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="28447-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="28447-115">Punto de acceso al servicio requerido.</span><span class="sxs-lookup"><span data-stu-id="28447-115">The required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="28447-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="28447-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28447-117">Tipo de datos **: \_ servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="28447-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="28447-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="28447-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28447-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="28447-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="28447-120">El servicio que depende de SAP.</span><span class="sxs-lookup"><span data-stu-id="28447-120">The service that is dependent on the SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28447-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28447-121">Requirements</span></span>



| <span data-ttu-id="28447-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="28447-122">Requirement</span></span> | <span data-ttu-id="28447-123">Value</span><span class="sxs-lookup"><span data-stu-id="28447-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28447-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28447-124">Minimum supported client</span></span><br/> | <span data-ttu-id="28447-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="28447-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="28447-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28447-126">Minimum supported server</span></span><br/> | <span data-ttu-id="28447-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="28447-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="28447-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="28447-128">Namespace</span></span><br/>                | <span data-ttu-id="28447-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="28447-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="28447-130">MOF</span><span class="sxs-lookup"><span data-stu-id="28447-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28447-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28447-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="28447-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28447-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28447-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="28447-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="28447-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="28447-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28447-135">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="28447-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

