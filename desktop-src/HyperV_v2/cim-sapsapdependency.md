---
description: Representa una asociación entre dos puntos de acceso de servicio (SAP), en la que un SAP depende de otro para que lo use o se conecte con un servicio.
ms.assetid: fba4144b-833f-469f-93df-e8a79aa37811
title: CIM_SAPSAPDependency (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Antecedent
- CIM_SAPSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6888cbb74ea03b85bc9abfcea24e65660fd65953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542398"
---
# <a name="cim_sapsapdependency-class-hyper-v-management"></a><span data-ttu-id="d328d-103">CIM_SAPSAPDependency (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="d328d-103">CIM_SAPSAPDependency class (Hyper-V management)</span></span>

<span data-ttu-id="d328d-104">Representa una asociación entre dos puntos de acceso de servicio (SAP), en la que un SAP depende de otro para que lo use o se conecte con un servicio.</span><span class="sxs-lookup"><span data-stu-id="d328d-104">Represents an association between two service access points (SAP), in which one SAP is dependant on the other to utilize or connect with a service.</span></span> <span data-ttu-id="d328d-105">Por ejemplo, para imprimir en una impresora de red, los puntos de acceso de impresión locales deben emplear SAP relacionado con la red subyacente para enviar la solicitud de impresión.</span><span class="sxs-lookup"><span data-stu-id="d328d-105">For example, to print on a network printer, local print access points must utilize underlying network-related SAPs to send the print request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d328d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d328d-106">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d328d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d328d-107">Members</span></span>

<span data-ttu-id="d328d-108">La clase **CIM \_ SAPSAPDependency** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d328d-108">The **CIM\_SAPSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="d328d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d328d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d328d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d328d-110">Properties</span></span>

<span data-ttu-id="d328d-111">La clase **CIM \_ SAPSAPDependency** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d328d-111">The **CIM\_SAPSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d328d-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="d328d-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d328d-113">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="d328d-113">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="d328d-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d328d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d328d-115">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="d328d-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d328d-116">Referencia al SAP requerido.</span><span class="sxs-lookup"><span data-stu-id="d328d-116">A reference to the required SAP.</span></span>

</dd> <dt>

<span data-ttu-id="d328d-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="d328d-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d328d-118">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="d328d-118">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="d328d-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d328d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d328d-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="d328d-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d328d-121">Referencia a SAP dependiente.</span><span class="sxs-lookup"><span data-stu-id="d328d-121">A reference to the dependant SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d328d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d328d-122">Requirements</span></span>



| <span data-ttu-id="d328d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d328d-123">Requirement</span></span> | <span data-ttu-id="d328d-124">Value</span><span class="sxs-lookup"><span data-stu-id="d328d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d328d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d328d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d328d-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d328d-126">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d328d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d328d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d328d-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d328d-128">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d328d-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d328d-129">Namespace</span></span><br/>                | <span data-ttu-id="d328d-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d328d-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d328d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d328d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d328d-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d328d-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d328d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d328d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d328d-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d328d-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d328d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d328d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d328d-136">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="d328d-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

