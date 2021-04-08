---
description: Representa una asociación en la que \_ se asigna una instancia de ResourceAllocationSettingData de CIM desde un grupo de recursos.
ms.assetid: ca9060e5-4434-4302-a840-a7d9cf5db714
title: CIM_ResourceAllocationFromPool (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationFromPool
- CIM_ResourceAllocationFromPool.Antecedent
- CIM_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 09bd7b70d49d2304062d35d29586fea886c86a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002488"
---
# <a name="cim_resourceallocationfrompool-class"></a><span data-ttu-id="d24b1-103">\_Clase ResourceAllocationFromPool de CIM</span><span class="sxs-lookup"><span data-stu-id="d24b1-103">CIM\_ResourceAllocationFromPool class</span></span>

<span data-ttu-id="d24b1-104">Representa una asociación en la que se asigna una instancia de [**\_ ResourceAllocationSettingData de CIM**](cim-resourceallocationsettingdata.md) desde un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d24b1-104">Represents an association in which a [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instance is allocated from a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="d24b1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d24b1-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::Resource"), AMENDMENT]
class CIM_ResourceAllocationFromPool : CIM_Dependency
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d24b1-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d24b1-106">Members</span></span>

<span data-ttu-id="d24b1-107">La clase **CIM \_ ResourceAllocationFromPool** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d24b1-107">The **CIM\_ResourceAllocationFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="d24b1-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d24b1-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d24b1-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d24b1-109">Properties</span></span>

<span data-ttu-id="d24b1-110">La clase **CIM \_ ResourceAllocationFromPool** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d24b1-110">The **CIM\_ResourceAllocationFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d24b1-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="d24b1-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24b1-112">Tipo de datos: **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="d24b1-112">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="d24b1-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d24b1-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d24b1-114">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="d24b1-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="d24b1-115">Grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d24b1-115">The resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="d24b1-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="d24b1-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d24b1-117">Tipo de datos: **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="d24b1-117">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="d24b1-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d24b1-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d24b1-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="d24b1-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d24b1-120">Los datos de asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="d24b1-120">The resource allocation data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d24b1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d24b1-121">Requirements</span></span>



| <span data-ttu-id="d24b1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d24b1-122">Requirement</span></span> | <span data-ttu-id="d24b1-123">Value</span><span class="sxs-lookup"><span data-stu-id="d24b1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d24b1-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d24b1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d24b1-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d24b1-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d24b1-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d24b1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d24b1-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d24b1-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d24b1-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d24b1-128">Namespace</span></span><br/>                | <span data-ttu-id="d24b1-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d24b1-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d24b1-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d24b1-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d24b1-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d24b1-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d24b1-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d24b1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d24b1-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d24b1-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d24b1-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d24b1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d24b1-135">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="d24b1-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

