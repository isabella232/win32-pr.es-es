---
description: Representa la asociación entre dos definiciones de métricas o dos valores de métricas.
ms.assetid: 78fb926d-8981-443a-a82d-ebac34d38e13
title: Msvm_MetricCollectionDependency (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricCollectionDependency
- Msvm_MetricCollectionDependency.Antecedent
- Msvm_MetricCollectionDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dc24cf72975f9d4e47e414425ac4cfbfe5d11847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688568"
---
# <a name="msvm_metriccollectiondependency-class"></a><span data-ttu-id="80050-103">MSVM \_ MetricCollectionDependency (clase)</span><span class="sxs-lookup"><span data-stu-id="80050-103">Msvm\_MetricCollectionDependency class</span></span>

<span data-ttu-id="80050-104">Representa la asociación entre dos definiciones de métricas o dos valores de métricas.</span><span class="sxs-lookup"><span data-stu-id="80050-104">Represents the association between two metric definitions or two metric values.</span></span>

<span data-ttu-id="80050-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="80050-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="80050-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80050-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricCollectionDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="80050-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="80050-107">Members</span></span>

<span data-ttu-id="80050-108">La clase **MSVM \_ MetricCollectionDependency** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="80050-108">The **Msvm\_MetricCollectionDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="80050-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80050-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80050-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80050-110">Properties</span></span>

<span data-ttu-id="80050-111">La clase **MSVM \_ MetricCollectionDependency** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="80050-111">The **Msvm\_MetricCollectionDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80050-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="80050-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80050-113">Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="80050-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="80050-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80050-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80050-115">Referencia a una instancia de la clase [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que representa la definición de métrica independiente o el valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="80050-115">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the independent metric definition or metric value.</span></span> <span data-ttu-id="80050-116">Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="80050-116">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="80050-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="80050-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80050-118">Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="80050-118">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="80050-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80050-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80050-120">Referencia a una instancia de la clase [**de \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que representa la definición de métricas o el valor de métrica que depende del **antecedente**.</span><span class="sxs-lookup"><span data-stu-id="80050-120">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the metric definition or metric value that is dependent on the **Antecedent**.</span></span> <span data-ttu-id="80050-121">Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="80050-121">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80050-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80050-122">Requirements</span></span>



| <span data-ttu-id="80050-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="80050-123">Requirement</span></span> | <span data-ttu-id="80050-124">Value</span><span class="sxs-lookup"><span data-stu-id="80050-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80050-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80050-125">Minimum supported client</span></span><br/> | <span data-ttu-id="80050-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="80050-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="80050-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80050-127">Minimum supported server</span></span><br/> | <span data-ttu-id="80050-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="80050-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80050-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="80050-129">Namespace</span></span><br/>                | <span data-ttu-id="80050-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="80050-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="80050-131">MOF</span><span class="sxs-lookup"><span data-stu-id="80050-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80050-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80050-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="80050-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="80050-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80050-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80050-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

