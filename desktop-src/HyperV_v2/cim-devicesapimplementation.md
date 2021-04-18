---
description: Representa una asociación entre un punto de acceso de servicio (SAP) y un dispositivo lógico que lo implementa.
ms.assetid: 40c8111a-d439-4c0f-805e-9c10d7182eb4
title: CIM_DeviceSAPImplementation (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Antecedent
- CIM_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e32676077cccd5c7e17fa551e904079f457b8d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687040"
---
# <a name="cim_devicesapimplementation-class-hyper-v-management"></a><span data-ttu-id="36a06-103">CIM_DeviceSAPImplementation (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="36a06-103">CIM_DeviceSAPImplementation class (Hyper-V management)</span></span>

<span data-ttu-id="36a06-104">Representa una asociación entre un punto de acceso de servicio (SAP) y un dispositivo lógico que lo implementa.</span><span class="sxs-lookup"><span data-stu-id="36a06-104">Represents an association between a service access point (SAP) and a logical device that implements it.</span></span>

## <a name="syntax"></a><span data-ttu-id="36a06-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36a06-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="36a06-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="36a06-106">Members</span></span>

<span data-ttu-id="36a06-107">La clase **CIM \_ DeviceSAPImplementation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="36a06-107">The **CIM\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="36a06-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36a06-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36a06-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36a06-109">Properties</span></span>

<span data-ttu-id="36a06-110">La clase **CIM \_ DeviceSAPImplementation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="36a06-110">The **CIM\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36a06-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="36a06-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a06-112">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="36a06-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="36a06-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a06-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a06-114">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="36a06-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="36a06-115">El dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="36a06-115">The logical device.</span></span>

</dd> <dt>

<span data-ttu-id="36a06-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="36a06-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a06-117">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="36a06-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="36a06-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a06-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a06-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="36a06-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="36a06-120">SAP implementado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="36a06-120">The SAP implemented by the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36a06-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36a06-121">Requirements</span></span>



| <span data-ttu-id="36a06-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="36a06-122">Requirement</span></span> | <span data-ttu-id="36a06-123">Value</span><span class="sxs-lookup"><span data-stu-id="36a06-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36a06-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36a06-124">Minimum supported client</span></span><br/> | <span data-ttu-id="36a06-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="36a06-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="36a06-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36a06-126">Minimum supported server</span></span><br/> | <span data-ttu-id="36a06-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36a06-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="36a06-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="36a06-128">Namespace</span></span><br/>                | <span data-ttu-id="36a06-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="36a06-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="36a06-130">MOF</span><span class="sxs-lookup"><span data-stu-id="36a06-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36a06-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36a06-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="36a06-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="36a06-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36a06-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="36a06-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="36a06-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="36a06-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36a06-135">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="36a06-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

