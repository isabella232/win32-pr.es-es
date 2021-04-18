---
description: Asociación entre una instancia de MSVM \_ VssComponent y una instancia de MSVM \_ VssService que representa un servicio para realizar operaciones en el componente de VSS.
ms.assetid: 19fdf2e3-48c4-452b-89d0-ec0b8681fca2
title: Msvm_ServiceOfVssComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceOfVssComponent
- Msvm_ServiceOfVssComponent.Antecedent
- Msvm_ServiceOfVssComponent.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5787dcdd4d8ce1aeefdc1fbafb2c156aec4d467a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687844"
---
# <a name="msvm_serviceofvsscomponent-class"></a><span data-ttu-id="600a8-103">MSVM \_ ServiceOfVssComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="600a8-103">Msvm\_ServiceOfVssComponent class</span></span>

<span data-ttu-id="600a8-104">Asociación entre una instancia de [**MSVM \_ VssComponent**](msvm-vsscomponent.md) y una instancia de [**MSVM \_ VssService**](msvm-vssservice.md) que representa un servicio para realizar operaciones en el componente de VSS.</span><span class="sxs-lookup"><span data-stu-id="600a8-104">An association between an instance of [**Msvm\_VssComponent**](msvm-vsscomponent.md) and an instance of [**Msvm\_VssService**](msvm-vssservice.md) that represents a service for performing operations on the VSS component.</span></span>

<span data-ttu-id="600a8-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="600a8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="600a8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="600a8-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceOfVssComponent : CIM_Dependency
{
  Msvm_VssComponent REF Antecedent;
  Msvm_VssService   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="600a8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="600a8-107">Members</span></span>

<span data-ttu-id="600a8-108">La clase **MSVM \_ ServiceOfVssComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="600a8-108">The **Msvm\_ServiceOfVssComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="600a8-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="600a8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="600a8-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="600a8-110">Properties</span></span>

<span data-ttu-id="600a8-111">La clase **MSVM \_ ServiceOfVssComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="600a8-111">The **Msvm\_ServiceOfVssComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="600a8-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="600a8-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600a8-113">Tipo de datos: **MSVM \_ VssComponent**</span><span class="sxs-lookup"><span data-stu-id="600a8-113">Data type: **Msvm\_VssComponent**</span></span>
</dt> <dt>

<span data-ttu-id="600a8-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600a8-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600a8-115">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. antecedente")</span><span class="sxs-lookup"><span data-stu-id="600a8-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="600a8-116">A, [**MSVM \_ VssComponent**](msvm-vsscomponent.md) que representa el componente de VSS.</span><span class="sxs-lookup"><span data-stu-id="600a8-116">A, [**Msvm\_VssComponent**](msvm-vsscomponent.md) that represents the VSS component.</span></span>

</dd> <dt>

<span data-ttu-id="600a8-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="600a8-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600a8-118">Tipo de datos: **MSVM \_ VssService**</span><span class="sxs-lookup"><span data-stu-id="600a8-118">Data type: **Msvm\_VssService**</span></span>
</dt> <dt>

<span data-ttu-id="600a8-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600a8-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600a8-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Dependent")</span><span class="sxs-lookup"><span data-stu-id="600a8-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="600a8-121">Un [**\_ VssService de MSVM**](msvm-vssservice.md) que representa el servicio de VSS IC.</span><span class="sxs-lookup"><span data-stu-id="600a8-121">An [**Msvm\_VssService**](msvm-vssservice.md) that represents the VSS IC service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="600a8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="600a8-122">Requirements</span></span>



| <span data-ttu-id="600a8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="600a8-123">Requirement</span></span> | <span data-ttu-id="600a8-124">Value</span><span class="sxs-lookup"><span data-stu-id="600a8-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="600a8-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="600a8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="600a8-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="600a8-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="600a8-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="600a8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="600a8-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="600a8-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="600a8-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="600a8-129">Namespace</span></span><br/>                | <span data-ttu-id="600a8-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="600a8-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="600a8-131">MOF</span><span class="sxs-lookup"><span data-stu-id="600a8-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="600a8-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="600a8-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="600a8-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="600a8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="600a8-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="600a8-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="600a8-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="600a8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="600a8-136">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="600a8-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

