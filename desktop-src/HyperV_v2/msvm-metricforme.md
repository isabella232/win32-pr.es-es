---
description: Esta asociación vincula un elemento administrado con los valores de métricas que se mantienen para él.
ms.assetid: 89b43736-90ae-49e0-a0ed-7918ddec8558
title: Msvm_MetricForME (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricForME
- Msvm_MetricForME.Antecedent
- Msvm_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 554f77390737b336b8660d09f737049be193b448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688567"
---
# <a name="msvm_metricforme-class"></a><span data-ttu-id="f9529-103">MSVM \_ MetricForME (clase)</span><span class="sxs-lookup"><span data-stu-id="f9529-103">Msvm\_MetricForME class</span></span>

<span data-ttu-id="f9529-104">Esta asociación vincula un elemento administrado con los valores de métricas que se mantienen para él.</span><span class="sxs-lookup"><span data-stu-id="f9529-104">This association links a managed element to the metric values being maintained for it.</span></span>

<span data-ttu-id="f9529-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f9529-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9529-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9529-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricForME : CIM_MetricForME
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f9529-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f9529-107">Members</span></span>

<span data-ttu-id="f9529-108">La clase **MSVM \_ MetricForME** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f9529-108">The **Msvm\_MetricForME** class has these types of members:</span></span>

-   [<span data-ttu-id="f9529-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f9529-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9529-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f9529-110">Properties</span></span>

<span data-ttu-id="f9529-111">La clase **MSVM \_ MetricForME** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f9529-111">The **Msvm\_MetricForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9529-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="f9529-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9529-113">Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="f9529-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="f9529-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9529-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9529-115">Una referencia a una instancia de la clase de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que representa el elemento administrado que tiene métricas definidas por los mantenidos de forma **dependiente** .</span><span class="sxs-lookup"><span data-stu-id="f9529-115">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the managed element that has metrics defined by **Dependent** maintained for it.</span></span> <span data-ttu-id="f9529-116">Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="f9529-116">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="f9529-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="f9529-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9529-118">Tipo de datos: \* \* \* \* CIM BaseMetricValue \* \* \* \* \_</span><span class="sxs-lookup"><span data-stu-id="f9529-118">Data type: \*\*\*\*CIM\_BaseMetricValue\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="f9529-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9529-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9529-120">Referencia a una instancia de la clase **\_ BaseMetricValue de CIM** que representa la métrica recopilada por el **antecedente** .</span><span class="sxs-lookup"><span data-stu-id="f9529-120">A reference to an instance of the **CIM\_BaseMetricValue** class that represents the metric that the **Antecedent** has collected for it.</span></span> <span data-ttu-id="f9529-121">Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="f9529-121">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9529-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9529-122">Requirements</span></span>



| <span data-ttu-id="f9529-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9529-123">Requirement</span></span> | <span data-ttu-id="f9529-124">Value</span><span class="sxs-lookup"><span data-stu-id="f9529-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9529-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9529-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f9529-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f9529-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f9529-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9529-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f9529-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f9529-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f9529-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f9529-129">Namespace</span></span><br/>                | <span data-ttu-id="f9529-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f9529-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f9529-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f9529-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9529-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9529-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9529-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9529-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9529-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f9529-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

